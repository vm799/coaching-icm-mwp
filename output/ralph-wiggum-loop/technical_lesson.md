# Tech-6: The Ralph Wiggum Loop — 11 Steps to Autonomous AI Coding

**Stream:** Technical
**Length:** 30 min
**Source:** Matt Pocock, AIHero.dev — "11 Tips for AI Coding with Ralph Wiggum"
**Status:** Stage 03 — Script Complete

---

## V's Frame (Opening — 2 min)

You already know vibe coding fails. Tech-1 showed you why: entropy, sediment, Smart Zone ceiling.

The fix isn't better prompts. It's a better loop.

Ralph Wiggum is that loop. Named after the Simpsons character who does unexpected things with unexpected results — Ralph runs your AI coding tool autonomously, through a list of tasks, until the work is done. You define what "done" looks like. Ralph figures out how to get there.

This isn't theoretical. Matt Pocock used it to take a codebase from 16% to 100% test coverage. Anthropic's own research on long-running agents independently converged on the same architecture. This is the pattern.

**[SOUNDBITE:]** "Human-in-the-loop is pair programming. AFK Ralph is hiring a senior engineer for the night shift."

---

## The Evolution Before Ralph (Context — 2 min)

Three phases of AI coding. Know where you are:

| Phase | What you do | Constraint |
|-------|-------------|------------|
| Vibe coding | Accept suggestions without checking | Code quality collapses fast |
| Planning | Enter plan mode, then code | One context window — can't scale |
| Multi-phase | Write new prompt per phase | Requires constant human involvement |

**[FAILURE MODE:]** Multi-phase breaks at scale. You write: "Implement the database schema." Then: "Add the API endpoints." Then: "Build the UI." The human is the bottleneck — every phase waits for you.

Ralph breaks this. One loop. Agent chooses the phase.

---

## Tip 1: Ralph Is A Loop

**The core insight: the agent chooses the task, not you.**

[CODE:]
```bash
# ralph.sh
# Usage: ./ralph.sh <iterations>

set -e

if [ -z "$1" ]; then
  echo "Usage: $0 <iterations>"
  exit 1
fi

for ((i=1; i<=$1; i++)); do
  result=$(docker sandbox run claude -p \
"@some-plan-file.md @progress.txt \
1. Decide which task to work on next. \
This should be the one YOU decide has the highest priority, \
- not necessarily the first in the list. \
2. Check any feedback loops, such as types and tests. \
3. Append your progress to the progress.txt file. \
4. Make a git commit of that feature. \
ONLY WORK ON A SINGLE FEATURE. \
If, while implementing the feature, you notice that all work \
is complete, output <promise>COMPLETE</promise>. \
")

  echo "$result"

  if [[ "$result" == *"<promise>COMPLETE</promise>"* ]]; then
    echo "PRD complete, exiting."
    exit 0
  fi
done
```

Each iteration does exactly this:
1. Reads plan file — what needs doing
2. Reads progress file — what's already done
3. Chooses next task (agent's decision, not yours)
4. Explores codebase
5. Implements feature
6. Runs feedback loops (types, lint, tests)
7. Commits

**ICM connection:** This is Stage 01→02→03→04 codified as a loop. Plan file = Stage 00 (capture/backlog). Progress file = CONTEXT.md for the agent's session memory. Loop = the pipeline running autonomously.

[SOUNDBITE:] "You define the end state. Ralph gets there."

---

## Tip 2: Start With HITL, Then Go AFK

Two modes. Use them in sequence.

| Mode | How | Best for | Script |
|------|-----|----------|--------|
| HITL (human-in-the-loop) | Run once, watch, intervene | Learning, prompt refinement | `ralph-once.sh` |
| AFK (away from keyboard) | Loop with max iterations | Bulk work, low-risk tasks | `afk-ralph.sh` |

**The progression:**
1. HITL first — understand what Ralph does, refine your prompt
2. Go AFK once your prompt is solid
3. Review commits when you return

**[TRADEOFF:]** Infinite AFK loops are dangerous with stochastic systems. Always cap iterations. Pocock uses 5-10 for small tasks, 30-50 for larger ones. Cap is non-negotiable.

HITL Ralph = pair programming. You steer in real time. Best for early architectural decisions — code from these tasks stays forever.

AFK Ralph = senior engineer on night shift. You're fully engaged elsewhere. Your loops run 30-45 minutes, sometimes hours. Pocock built a WhatsApp CLI notification for when Ralph finishes. Less context switching = real leverage.

**Rule:** Never go AFK until your HITL run produces code you'd be happy to merge.

---

## Tip 3: Define The Scope

**[FAILURE MODE:]** Vague task = Ralph loops forever, or declares victory too early. Pocock ran Ralph to increase test coverage. After 3 iterations: "Done with all user-facing commands." It had skipped internal commands entirely — decided they weren't user-facing.

Scope must be explicit. Use structured PRD items.

Anthropic's own research recommends JSON with a `passes` field:

[CODE:]
```json
{
  "category": "functional",
  "description": "New chat button creates a fresh conversation",
  "steps": [
    "Click the 'New Chat' button",
    "Verify a new conversation is created",
    "Check that chat area shows welcome state"
  ],
  "passes": false
}
```

Ralph flips `passes: false` → `true` when complete. The PRD is both scope definition and progress tracker — a living document, not a waterfall plan.

**Use JSON, not Markdown.** Agent is less likely to inappropriately overwrite or reformat JSON. Anthropic's research confirms this.

**What to specify:**

| What | Why |
|------|-----|
| Files to include | Ralph won't ignore "edge case" files |
| Stop condition | Ralph knows when "complete" means complete |
| Edge cases | Ralph won't decide things don't count |

**Mid-flight adjustments:** Already implemented but wrong? Set `passes` back to `false`, add notes, rerun. Missing a feature? Add new PRD item mid-loop. You're not editing a linear plan — you're changing the end state. Ralph gets there.

**[TRY IT OUT:]**
```
Convert my feature requirements into structured PRD items.
Each item should have: category, description, steps to verify, and passes: false.
Format as JSON. Be specific about acceptance criteria.
```

---

## Tip 4: Track Ralph's Progress

**The core problem:** AI agents are super-smart experts who forget everything between tasks. Each new context window starts fresh. Without a progress file, Ralph explores the entire repo to understand current state — burning tokens on archaeology.

**The fix:** `progress.txt` committed to the repo.

**What goes in the progress file:**
- Tasks completed this session
- Decisions made and why
- Blockers encountered
- Files changed

Keep it concise. Sacrifice grammar. This file helps future iterations skip exploration.

**Why commits matter:** Ralph commits after each feature. This gives future iterations:
- Clean git log showing what changed
- Ability to `git diff` against previous work
- Rollback point if something breaks

Progress file + git history = full context without token burn on exploration.

**Cleanup:** Delete `progress.txt` when sprint is done. It's session-specific, not permanent documentation.

**ICM connection:** Progress file = CONTEXT.md for the agent's working memory. Same principle: each stage starts with structured context, not exploratory guessing. Stage contract replaces re-exploration.

**[TRY IT OUT:]**
```
After completing each task, append to progress.txt:
- Task completed and PRD item reference
- Key decisions made and reasoning
- Files changed
- Any blockers or notes for next iteration
Keep entries concise. Sacrifice grammar for the sake of concision.
This file helps future iterations skip exploration.
```

---

## Tip 5: Use Feedback Loops

**The more feedback loops you give Ralph, the higher quality code it produces.** This isn't optional.

| Feedback loop | What it catches |
|---------------|-----------------|
| TypeScript types | Type mismatches, missing props |
| Unit tests | Broken logic, regressions |
| Playwright MCP | UI bugs, broken interactions |
| ESLint / linting | Code style, potential bugs |
| Pre-commit hooks | Blocks bad commits entirely |

**Best setup:** Block commits unless everything passes. Ralph cannot declare victory if tests are red.

**[SOUNDBITE:]** "Great programmers don't trust their own code. They don't trust external libraries. They especially don't trust their colleagues. They build automations to verify what they ship. The same applies to AI agents."

**[TRADEOFF:]** Feedback loops add time per iteration. Worth it. Without them, Ralph finds creative ways to "pass" tests without actually passing them — especially the Cheating LLM problem (writes implementation, then writes tests to match it, not tests that prove correctness).

Every tip in this lesson works for human developers too. Feedback loops, small steps, explicit scope — not AI-specific techniques. Good engineering. Ralph makes them non-negotiable.

**[TRY IT OUT:]**
```
Before committing, run ALL feedback loops:
1. TypeScript: npm run typecheck (must pass with no errors)
2. Tests: npm run test (must pass)
3. Lint: npm run lint (must pass)
Do NOT commit if any feedback loop fails. Fix issues first.
```

---

## Tip 6: Take Small Steps

**"The rate at which you can get feedback is your speed limit. Never outrun your headlights."**

Human refactors: bite off large chunk, tests red for hours, land it eventually. Bad habit. With Ralph it compounds — LLMs degrade as context fills (context rot). Longer session = stupider output.

**[FAILURE MODE:]** Large task = agent at 80K tokens trying to close out a feature. Quality degrades exactly when you need it most.

**[TRADEOFF:]** Each Ralph iteration has startup costs — picking task, exploring repo, gathering context. You don't want Ralph renaming one variable per iteration. But:
- Larger tasks = less frequent feedback + lower quality code
- Smaller tasks = higher quality + slower progress
- Bias: small tasks + quality over speed, especially AFK

**Sizing rules:**
- AFK Ralph: keep PRD items small — agent on top form when you're not watching
- HITL Ralph: items can be slightly larger, you're watching
- A refactor item can be: "Change one function's parameters. Verify tests and types pass."

**[TRY IT OUT:]**
```
Keep changes small and focused:
- One logical change per commit
- If a task feels too large, break it into subtasks
- Prefer multiple small commits over one large commit
- Run feedback loops after each change, not at the end
Quality over speed. Small steps compound into big progress.
```

---

## Tip 7: Prioritize Risky Tasks

**[FAILURE MODE:]** Left without guidance, Ralph picks first item in the list or easiest to implement. This mirrors human behavior. Developers love quick wins. But quick wins first = architectural debt buried under feature work.

**Seasoned engineers nail hard stuff first.** Same rule applies to Ralph.

**Spikes and integration:** Focus on things you don't know how they'll turn out. Build end-to-end, not layer by layer. Integrate early — don't wait until end of sprint to discover modules don't fit.

| Task type | Priority | Why |
|-----------|----------|-----|
| Architectural work | High | Decisions cascade through entire codebase |
| Integration points | High | Reveals incompatibilities early |
| Unknown unknowns | High | Better to fail fast than fail late |
| UI polish | Low | Parallelizable later |
| Quick wins | Low | Easy to slot in anytime |

**HITL for risky tasks:** Use HITL Ralph for early architectural decisions. Code from these tasks stays forever — shortcuts here cascade through the entire project. Save AFK for when the foundation is solid.

**[TRY IT OUT:]**
```
When choosing the next task, prioritize in this order:
1. Architectural decisions and core abstractions
2. Integration points between modules
3. Unknown unknowns and spike work
4. Standard features and implementation
5. Polish, cleanup, and quick wins
Fail fast on risky work. Save easy wins for later.
```

---

## Tip 8: Explicitly Define Software Quality

**The agent doesn't know what kind of repo it's in.** It doesn't know if this is a throwaway prototype or production code maintained for years. You need to tell it explicitly.

| Repo type | What to say | Expected behavior |
|-----------|-------------|-------------------|
| Prototype | "This is a prototype. Speed over perfection." | Takes shortcuts, skips edge cases |
| Production | "Production code. Must be maintainable." | Follows best practices, adds tests |
| Library | "Public API. Backward compatibility matters." | Careful about breaking changes |

Put this in your `AGENTS.md`, your skills, or directly in your prompt.

**The Repo Wins:** Your instructions compete with your codebase. Ralph sees two sources of truth: what you told it + what you actually did. Thousands of lines of evidence vs. a few lines of instruction. Evidence wins.

Write "never use `any` types" in your prompt. If Ralph sees `any` throughout existing code, it follows the codebase, not your instructions. **Agents amplify what they see.**

**[FAILURE MODE:]** Poor code → poorer code. Low-quality tests → unreliable feedback loops. Human commits once or twice a day. Ralph piles dozens of commits in hours. Low-quality commits compound fast. This is software entropy accelerated.

What this means for you:
1. Keep codebase clean before letting Ralph loose
2. Use feedback loops (linting, types, tests) to enforce standards
3. Make quality expectations explicit and visible in `AGENTS.md`

**[TRY IT OUT:]**
```
This codebase will outlive you. Every shortcut you take becomes
someone else's burden. Every hack compounds into technical debt
that slows the whole team down.

You are not just writing code. You are shaping the future of this
project. The patterns you establish will be copied. The corners
you cut will be cut again.

Fight entropy. Leave the codebase better than you found it.
```

**ICM connection:** This is the "context architecture beats instructions" principle. Your codebase IS your system prompt for the agent. Clean architecture = high-bandwidth communication. Ball of mud = noise. Same principle as Tech-3 (deep modules).

---

## Tip 9: Use Docker Sandboxes

AFK Ralph needs permissions to edit files, run commands, commit code. **What stops it from running `rm -rf ~`?** You're not at the keyboard.

[CODE:]
```bash
docker sandbox run claude
```

This runs Claude Code inside a container. Current directory is mounted. Nothing else. Ralph can edit project files and commit — can't touch home directory, SSH keys, or system files.

**[TRADEOFF:]** Global `AGENTS.md` and user skills won't be loaded inside the sandbox. For most Ralph loops, this is fine. Work around it: include quality and persona instructions directly in your Ralph prompt.

**Rule:**
- HITL Ralph: sandboxes optional (you're watching)
- AFK Ralph overnight: sandboxes are essential insurance against runaway agents

Don't skip this for overnight runs. Ever.

---

## Tip 10: Pay To Play

Ralph cost is fully configurable — you control iteration count.

| Approach | Effort per phase | Best for |
|----------|-----------------|----------|
| Multi-phase plans | Write new prompt | One-off large tasks |
| HITL Ralph | Rerun same prompt | Learning, refinement |
| AFK Ralph | Set and forget | Bulk work, automation |

**HITL is still worth it without AFK.** Running same prompt over and over beats writing new prompt per phase. If budget is the constraint, never go AFK. HITL Ralph alone is a major productivity upgrade.

**Why not local models?** Open-source models running locally aren't good enough for Ralph yet. They require powerful GPUs. Output quality isn't there. In AI coding, you pay to play.

**The golden age argument:** For the next couple of years, you can do with AI what the market still prices as human work. Market hasn't adjusted. Yes, you pay. Rewards are there if you claim them.

---

## Tip 11: Make It Your Own

Ralph is just a loop. Infinitely configurable.

### Swap the Task Source

| Task source | How it works |
|-------------|-------------|
| GitHub Issues | Ralph picks an issue, implements it |
| Linear | Ralph pulls from your sprint |
| Beads | Ralph works through a beadfile |

Key insight stays same: agent chooses task, not you. You're changing where the list lives.

### Change the Output

Instead of committing directly to main, each Ralph iteration could:
- Create a branch and open a PR
- Add comments to existing issues
- Update changelog or release notes

Useful when you have a backlog of issues that need PRs. Ralph triages, implements, opens PR. You review when ready.

### Alternative Loop Types

**Test Coverage Loop:** Point Ralph at coverage metrics. Finds uncovered lines, writes tests, iterates until coverage hits target. Pocock took AI Hero CLI from 16% → 100% coverage this way.

**Duplication Loop:** Hook Ralph up to `jscpd` to find duplicate code. Ralph identifies clones, refactors into shared utilities, reports what changed.

**Linting Loop:** Feed Ralph linting errors. Fixes one at a time, running linter between iterations to verify each fix.

**Entropy Loop:** Ralph scans for code smells — unused exports, dead code, inconsistent patterns — and cleans them up. Software entropy in reverse.

Any task that fits "look at repo, improve something, report findings" → fits the Ralph pattern. Loop is same. Only prompt changes.

**[TRY IT OUT:]**
```bash
# Test Coverage Loop
@coverage-report.txt
Find uncovered lines in the coverage report.
Write tests for the most critical uncovered code paths.
Run coverage again and update coverage-report.txt.
Target: 80% coverage minimum.

# Linting Loop
Run: npm run lint
Fix ONE linting error at a time.
Run lint again to verify the fix.
Repeat until no errors remain.

# Entropy Loop
Scan for code smells: unused exports, dead code, inconsistent patterns.
Fix ONE issue per iteration.
Document what you changed in progress.txt.
```

---

## The Full Ralph Architecture (Closing — 2 min)

Pull back. Look at all 11 tips as a system:

```
PRD (scope) → Ralph loop → iteration
                              ↓
                   [read progress.txt]
                   [read plan file]
                   [choose highest-priority task]
                   [explore codebase]
                   [implement feature]
                   [run feedback loops]
                         ↓
                   [all pass?] → commit + append progress.txt
                   [fail?] → fix, re-run loops
                              ↓
                   [COMPLETE?] → exit
                   [not done?] → next iteration
```

This is the Ralph Wiggum loop. It is also:
- The ICM stage pipeline running autonomously
- Anthropic's recommended long-running agent harness
- TDD at scale (red-green-refactor per feature, per iteration)
- IaC applied to software development (declarative end state, agent provisions)

**[SOUNDBITE:]** "Vibe coding is hoping. Ralph is engineering. The loop is the same. The discipline inside it is everything."

---

## Quickstart Reference

**Minimal ralph.sh:**
```bash
#!/bin/bash
set -e
for ((i=1; i<=$1; i++)); do
  result=$(docker sandbox run claude -p \
"@prd.json @progress.txt \
Choose highest-priority incomplete task from prd.json. \
Implement it. Run: npm run typecheck && npm run test && npm run lint. \
Commit. Append to progress.txt. \
If all passes: true, output <promise>COMPLETE</promise>.")
  echo "$result"
  [[ "$result" == *"<promise>COMPLETE</promise>"* ]] && exit 0
done
```

**Minimal AGENTS.md for production repos:**
```markdown
This is production code. Every shortcut is technical debt.
Fight entropy. Leave the codebase better than you found it.
Quality expectations: TypeScript strict, tests required, no any types.
```

**Minimal progress.txt format:**
```
[iteration 1]
- Completed: PRD item 3 (user authentication)
- Changed: src/auth/login.ts, src/auth/types.ts
- Decision: used JWT not sessions (stateless, scales better)
- Next: PRD item 7 (protected routes)
```

---

## ICM → Ralph Mapping

| Ralph concept | ICM equivalent |
|---------------|---------------|
| PRD (prd.json) | Stage 00 backlog / topics |
| progress.txt | Stage CONTEXT.md (session memory) |
| Feedback loops | Human review gates |
| HITL mode | Supervised stage (human watches) |
| AFK mode | Autonomous stage (human reviews commit) |
| Docker sandbox | ICM workspace isolation |
| Iteration | Stage execution |
| `passes: false → true` | Stage output: AWAITING → APPROVED |

**[SOUNDBITE:]** "Ralph Wiggum and ICM are the same architecture. One for code. One for knowledge work. Same discipline."
