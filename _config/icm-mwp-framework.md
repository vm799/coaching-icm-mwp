# ICM/MWP Framework — Static Reference

This file documents the ICM (Integrated Context Management) and MWP (Model Workspace Protocol) concepts used throughout coaching series.

Use this as reference knowledge. Copy relevant sections into scripts + research outputs.

## ICM: 5-Layer Context Hierarchy

### Layer 0: Global Identity
**What:** Shared constraints, principles, and persona across all workspaces
**Where:** `~/.claude/CLAUDE.md` (user's global rules)
**Why:** Consistency. One set of rules that all agents follow.
**Example:** "We will NOT fabricate data. If missing, we flag [MISSING] and halt."

### Layer 1: Domain / Workspace Identity
**What:** Project-specific persona, constraints, success criteria
**Where:** `{project}/CLAUDE.md` (this workspace's identity)
**Why:** Each project has different client, domain, scope.
**Example:** "Coaching Content Workspace. Teaching + Enterprise streams. Non-negotiable: produce complete scripts only."

### Layer 2: Stage Contracts
**What:** What each phase does (inputs, process, outputs), success criteria
**Where:** `{project}/stages/{phase}/CONTEXT.md`
**Why:** Clear handoff. Agent knows exactly what stage consumes, produces, validates.
**Example:** "Stage 02 reads discovery brief, produces research output. Success: 5+ sources cited."

### Layer 3: Reference Knowledge + Configuration
**What:** Stable rules, templates, domain knowledge, tone guides
**Where:** `{project}/_config/`, `{project}/references/`
**Why:** Reusable. Don't rewrite tone guide in every script; reference it.
**Example:** `teaching-voice.md`, `enterprise-voice.md`, `script_template.md`

### Layer 4: Working Artifacts + Products
**What:** In-progress work, final scripts, deliverables
**Where:** `{project}/output/`, `{project}/stages/*/working/`
**Why:** Separation. Rules live in L0-L3. Work lives in L4.
**Example:** `output/token-efficiency-icm/teaching_script.md`

## Why 5 Layers Matter (Token Efficiency)

### Problem: "Lost in the Middle"
When context is too long, LLM performance degrades. Mid-document information is less precise.
More context ≠ better answers. Selective context = better answers.

### Solution: Progressive Disclosure
- Stage 01 (Discovery): Load only L0, L1, L2.01 (what discovery does)
- Stage 02 (Research): Load L0, L1, L2.02 + research sources
- Stage 03 (Script): Load L0, L1, L2.03 + teaching/enterprise voice guides
- Stage 04 (Multiply): Load L0, L1, L2.04 + format templates

Result: Each stage gets ~15KB context (what it needs), not 45KB (everything).

### Benefit: Sustainability
- Cheaper (fewer tokens loaded per stage)
- Faster (less context to parse)
- More accurate (relevant context, less noise)
- Scalable (add 100 topics; context doesn't grow for each stage)

## MWP: Model Workspace Protocol

MWP applies Unix principles to AI work:
- One stage, one job
- Folder structure = routing logic (agent reads folder → knows its job)
- Plain text (markdown) = universal interface
- Output of one = input of next (no context loss)

### Pattern: Folder-Driven Routing

```
coaching-icm-mwp/
├── CLAUDE.md                    ← Agent reads: "I'm a content architect for teaching+enterprise"
├── CONTEXT.md                   ← Agent reads: "Here are my 4 stages and how they flow"
├── stages/
│   ├── 01_discovery/            ← Agent in this folder reads: "I intake topics, produce briefs"
│   │   └── CONTEXT.md
│   ├── 02_research/             ← Agent in this folder reads: "I fetch sources, produce research output"
│   │   └── CONTEXT.md
│   ├── 03_script/               ← Agent in this folder reads: "I write 2 scripts: teaching + enterprise"
│   │   └── CONTEXT.md
│   └── 04_multiply/             ← Agent in this folder reads: "I produce 6 formats from scripts"
│       └── CONTEXT.md
├── _config/
│   ├── teaching-voice.md        ← Reference: how to sound as teaching expert
│   ├── enterprise-voice.md      ← Reference: how to sound as business advisor
│   ├── icm-mwp-framework.md     ← Reference: what ICM/MWP are (this file)
│   └── catchphrases.md          ← Reference: soundbites library
├── references/
│   ├── script_template.md
│   ├── deck_template.md
│   ├── blog_template.md
│   ├── animation_template.md
│   └── youtube_template.md
└── output/
    └── [topic-slug]/            ← One folder per topic
        ├── teaching_script.md
        ├── enterprise_script.md
        ├── blog_post.md
        ├── deck_outline.md
        ├── linkedin_post.md
        ├── animation_spec.md
        └── youtube_package.md
```

### Agent Workflow (Using MWP)
1. Agent lands in `coaching-icm-mwp/` → reads CLAUDE.md (workspace identity) + CONTEXT.md (4 stages)
2. User: "Run discovery on 'Token Efficiency in ICM'"
3. Agent navigates to `stages/01_discovery/` → reads CONTEXT.md → understands job
4. Agent produces `discovery_brief.md` → places in output
5. Human reviews, approves
6. User: "Run research phase"
7. Agent navigates to `stages/02_research/` → reads CONTEXT.md + input (discovery brief)
8. Agent produces `research_output.md` → places in output
9. [Repeat: script phase, multiply phase]

**Key insight:** Agent knows what to do purely from folder structure + CONTEXT.md. No "run stage 2 now" prompt needed. Folder routes the work.

## Key Concepts (Teach/Enterprise Angles)

### 1. Context vs. Tokens
**Teaching angle:** "Tokens are words. Context is the story. Good context = fewer tokens needed to get right answer."
**Enterprise angle:** "Context efficiency = cost reduction. Every token costs money. Lean context = faster responses + lower bills."
**Core idea:** Selective context beats comprehensive context.

### 2. Progressive Disclosure
**Teaching angle:** "Learn simple first, complex later. Brain works better that way."
**Enterprise angle:** "Executive decisions get interrupted. Deliver key insight first, detail later. Respect their time."
**Core idea:** Layer complexity. Always lead with simplest answer.

### 3. One Job per Stage
**Teaching angle:** "Specialization works. A researcher shouldn't script-write. A script-writer shouldn't multiply. Experts own their stage."
**Enterprise angle:** "Clear ownership = fewer handoff bugs. Stage 02 guarantees research quality. Stage 03 guarantees script quality."
**Core idea:** Separation of concerns. Clean interfaces between stages.

### 4. Plain Text as Interface
**Teaching angle:** "Markdown is simple. Anyone can read it. No proprietary tools needed."
**Enterprise angle:** "Git-able. Auditable. No lock-in. If the tool dies, your content survives."
**Core idea:** Durability. Content lives beyond the tool.

## SWE Principles Behind ICM/MWP

### Unix Philosophy
- Do one thing well
- Expect output to be input to another program
- Write tools to work together
- Use text streams as universal interface

### DDD (Domain-Driven Design)
- Bounded contexts (each stage is a bounded context)
- Ubiquitous language (CLAUDE.md + CONTEXT.md define terms)
- Clear contracts (inputs, process, outputs)

### Infrastructure as Code
- Folder structure IS the specification
- CONTEXT.md IS the contract
- No documentation separate from code/structure

### GitOps
- Everything is versionable (no hidden state)
- History is auditable (git log shows evolution)
- Rollback is possible (revert to prior version)

## Anti-Patterns to Avoid

### ❌ Monolithic Script
Writing entire training program in one 6000-word script without layering.
**Better:** 10 scripts, each 6000 words, progressive (simple→complex)

### ❌ One Agent Does Everything
One agent tries to discovery + research + script + multiply.
**Better:** One agent per stage (clean handoff, easy to debug, reusable)

### ❌ Context Hoarding
Loading all research, all templates, all config at every stage.
**Better:** Load only what this stage needs (faster, cheaper, more accurate)

### ❌ Merged Outputs
Teaching + enterprise content mixed in one script.
**Better:** Two scripts, edited separately, both deliver the same truth (different angle)

### ❌ Proprietary Formats
Scripts in Word docs, research in Google Docs, no Git history.
**Better:** Markdown in Git (auditable, portable, tool-independent)

## Measurement: Is ICM/MWP Working?

✓ **Token efficiency:** Stage context <20KB (L0-L2 only), not 50KB (everything)
✓ **Handoff clarity:** Human review takes <10 min (CONTEXT.md was clear)
✓ **Reusability:** Same output/ structure for 10 topics (no special handling)
✓ **Auditability:** `git log` shows who, what, when for every script iteration
✓ **Scalability:** Add new topic without changing stage code (just folder + topic input)

## Reference Links
- MWP Paper: `../../../Interpretable_Context_Methodology_.pdf` (user's copy)
- SWE Principles: `~/.claude/rules/best_practices.md` (global rules)
- This file is Layer 3: stable, reused by all stages, updated quarterly
