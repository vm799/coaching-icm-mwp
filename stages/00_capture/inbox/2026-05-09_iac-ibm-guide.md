# Capture: 2026-05-09 — "What is Infrastructure as Code (IaC)?" (IBM Think)

**Source:** IBM Think / Jim Holdsworth & Annie Badman, September 2025
**Selective extract — definitions + principles only. No tool descriptions captured.**
**Status:** PROCESSED ✓

---

## What's Useful (4 things)

### 1. IaC Definition — The Core Analogy

> "Infrastructure as code treats infrastructure as software. Teams use IaC to version, test and deploy infrastructure by using the same practices they use for application code."

**V's connection:** ICM/MWP IS IaC for AI workflows. CLAUDE.md = config file. CONTEXT.md = contract. Git = version control. Stage gates = automated testing. Markdown outputs = idempotent provisioned resources.

**V's frame:** "ICM doesn't just borrow from software engineering. It IS software engineering — applied to the infrastructure of intelligence."

**Use in:** T4 (ICM layers), T9 (why not LangChain), Tech-2, any talk positioning ICM as engineering discipline not prompting.

---

### 2. Configuration Drift — Names the Problem IaC Solves

> "Drift is a common problem with mutable infrastructure, where manual changes accumulate over time, making it harder to maintain consistency across environments."

> "Most organizations choose immutable infrastructure. To change a server or configuration, teams must replace the entire infrastructure with new resources."

**Maps exactly to ICM:**
- **Mutable AI workflow** = vibe coding. Patch over patch. Context fills with sediment. Drift accumulates. Nothing matches what was intended.
- **Immutable AI workflow** = ICM. Stage output is a discrete artifact. To change it, run the stage again clean. No drift.

**V's frame:** "Configuration drift kills AI workflows the same way it kills infrastructure. The fix is the same: immutable stages with versioned outputs."

**Use in:** Tech-1 (vibe coding is a trap), T5 (stage contracts), E6 (consistency at scale).

---

### 3. Idempotency — The Stage Contract Principle

> "The provisioning process is idempotent, meaning it can run multiple times without creating duplicate resources."

**ICM equivalent:** Run Stage 02 (Research) twice — same inputs, same outputs. Stage is deterministic by design. Human review gate is the idempotency check.

**Teaching angle:** "Idempotent stages = reliable pipeline. Run it fresh, run it again — same result. That's what a stage contract guarantees."

**Use in:** T2 (how ICM works), Tech-2 (contracts + testing), stage contract deep-dives.

---

### 4. Knowledge Preservation Argument — Enterprise Angle

> "Organizations without IaC typically rely on a few specialists for provisioning. When one of these specialists leaves, their knowledge often goes with them. IaC preserves infrastructure knowledge in code."

**ICM parallel:** Organizations without ICM rely on a few AI-literate people. When they leave, prompting knowledge goes with them. ICM preserves it in CONTEXT.md files, stage contracts, voice guides.

**V's enterprise line:** "If your AI capability lives in someone's head — or someone's chat history — it will leave when they leave. ICM is how you keep it."

**Use in:** E3 (knowledge preservation / institutional memory), E8 (systems that improve over time), any CHRO/people leader talk.

---

## The Master Analogy (V's framing — not in source)

| IaC concept | ICM/MWP equivalent |
|-------------|-------------------|
| Configuration files | CLAUDE.md + CONTEXT.md |
| Version control (Git) | Git audit trail |
| Automation engine | Claude Code sessions |
| Idempotent provisioning | Stage outputs (run again = same result) |
| Immutable infrastructure | Stage outputs as discrete artifacts |
| Configuration drift | Sediment / vibe coding accumulation |
| CI/CD pipeline | Stage gate pipeline (00→01→02→03→04) |
| Declarative approach | CONTEXT.md: defines WHAT, not HOW |
| Modules | Stage contracts (composable, reusable) |
| Knowledge preservation | CONTEXT.md = institutional memory |

**V's frame:** "IaC taught enterprises to treat infrastructure as software. ICM teaches you to treat intelligence as infrastructure."

---

## What Was NOT Captured

- Terraform, AWS CloudFormation, Azure ARM, Google Cloud Deployment Manager descriptions — tool landscape, not V's angle
- Configuration management tools (Ansible, Chef, Puppet) — not relevant
- Specific IBM product integrations
- CI/CD implementation details

## Routed to:

- `quotes_raw.md` → IaC definition + configuration drift quote
- `analogies_bank.md` → IaC → ICM master analogy table
- New topic → `output/iac-for-ai-workflows/` → Stage 01 to follow
- Enriches: T2 (how ICM works), T4 (ICM layers), Tech-1 (vibe coding), Tech-2, E3 (institutional memory), E6 (consistency)
