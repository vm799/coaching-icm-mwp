# Capture: 2026-04-29 — Linus Torvalds-Inspired AI Coding Guidelines

**Source:** GitHub repository (inspired by forrestchang/andrej-karpathy-skills)
**Author:** Unknown
**Selective extract — tone/persona not V's. Principles + taxonomy only.**
**Status:** PROCESSED ✓

---

## What's Useful (3 things)

### 1. Four Principles — Map to ICM Design Principles

| Principle | What it attacks | ICM equivalent |
|-----------|----------------|---------------|
| **Data First** | Wrong structures, hidden edge cases, branchy garbage | Stage 01 Discovery: scope before building |
| **Simplicity First** | Overengineering, bogus abstractions, speculative features | Single responsibility, one stage one job |
| **Surgical Changes** | Drive-by refactors, collateral edits, random cleanup | Human review gates: touch only what's in scope |
| **Show Me the Code** | Vague claims, unverified patches, hand-wavy specs | Stage outputs are readable files — provable, auditable |

**V's reframe for technical stream:**
> "Torvalds has four principles. ICM/MWP has five. They're the same idea: design the structure first, do one thing, touch only what you must, prove it works. These aren't framework opinions — they're 50 years of production engineering compressed."

**Use in:** Tech-9 "MWP as software architecture" — map across SWE lineage table.

---

### 2. "Enterprise Sludge" — Best Name Yet for the LangChain Problem

From the "bogus shit detector":
> "Enterprise sludge — factories, managers, strategies, builders, and config layers for a one-function task."

**This is the LangChain critique, named perfectly.** LangChain produces enterprise sludge: abstractions, registries, prompt templates, chain factories, tool managers — for what could be a staged folder structure with plain text files.

**V's use:**
> "Enterprise sludge is what happens when you solve a simple problem with a complex framework. ICM doesn't add layers — it removes them. One stage. One job. One file."

**Use in:** T9 "Why not LangChain" (teaching) + E5 "Framework lock-in" (enterprise). Best vocabulary yet for the LangChain objection.

**Also useful from the taxonomy:**
- "Voodoo programming" — random barriers, loops, helpers added without understanding → what vibe coders add when AI output breaks
- "Hack upon hack" — piling new ugliness on top of old → sediment problem made visible
- "Random churn" — broad cleanup noise with no connection to the task → what AI does without surgical changes discipline

---

### 3. Torvalds Test Checklist (Adapted for V)

Original tests, adapted to V's register:

| Check | Original (Torvalds) | V's teaching version |
|-------|-------------------|---------------------|
| Data test | "Can you explain the memory layout in one paragraph without lying?" | "Can you explain the context structure in one paragraph without hand-waving?" |
| Simplicity test | "Would a sane maintainer call this total and utter crap?" | "Does this add complexity nobody asked for?" |
| Change test | "Every changed line should have a direct reason to exist." | "Every stage output should have a direct reason to exist." |
| Proof test | "If you cannot prove it, it is not done." | "If you cannot show the output file, the stage is not done." |

**Use in:** Tech-4 (TDD) + Tech-3 (deep modules) as a self-check heuristic. Also maps to ICM human review gates — the gate IS the Torvalds test for the stage.

---

## Routed to:

- `analogies_bank.md` → "Enterprise sludge" as named vocabulary for LangChain critique
- `objections_bank.md` → Enrich "Why not LangChain" with enterprise sludge framing
- Does NOT spawn new topic — enriches Tech-3, Tech-9, T9 (existing series)
- Attribution: GitHub repo, unknown author, inspired by Karpathy skills repo
