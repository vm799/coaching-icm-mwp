# Capture: 2026-05-09 — "AI-Assisted Visual Workflow + SKILL.md" (Unknown author)

**Source:** Unknown author — AI visual workflow walkthrough (Claude Code + Nano Banana 2)
**Selective extract — SKILL.md architecture + consistency argument only. Tool specifics skipped.**
**Status:** PROCESSED ✓

---

## What's Useful (3 things)

### 1. SKILL.md = Stage Contract for Visual Output ⭐⭐⭐⭐⭐

> "Your SKILL.md told it what you value, what your style looks like, and how you want things structured. The output carries your colors, your layout preferences, your brand."

**Direct ICM mapping:**
- SKILL.md = CONTEXT.md for Stage 04 (Multiply / visual output)
- Defines WHAT the output should look like, not HOW to generate it
- Declarative (style preferences, brand rules) not imperative (step-by-step prompt instructions)

**SKILL.md vs prompt comparison (from source):**
> "A detailed prompt and a SKILL.md file can produce similar results once. The difference shows up the second time, the tenth time, six months later."

**V's frame:** "Prompts are one-shot. SKILL.md compounds. Detailed prompt = recipe you repeat every time. SKILL.md = kitchen that runs every time. This is exactly the skills-vs-scripts argument made visual."

**Use in:** T6 (stage contracts), Tech-2, personal brand content workflow, Stage 04 (Multiply) design. Also: "Skills compound, scripts depreciate" — most visual demonstration possible.

---

### 2. Two-Phase Architecture: Thinking + Rendering

> "Phase 1: Claude Code handles all the thinking — structure, layout, quality checking, reference gathering. Phase 2: image model handles rendering. By the time content reaches the image model, most creative decisions have already been made and checked."

**ICM parallel:**
- Phase 1 = Stages 01-03 (thinking: discovery, research, script, quality check)
- Phase 2 = Stage 04 (rendering: multiply into formats)
- Agent doesn't decide what the visual looks like — it executes a brief that was already built

**Teaching frame:** "The image model isn't making creative decisions. It's executing a brief. That separation — thinking here, rendering there — is exactly the stage separation ICM codifies."

**Use in:** Tech-2 (stage contract design), T3 (why stages matter), Stage 04 workflow explanation.

### 3. Quality Check Before Rendering = Stage Gate

> "Before any image gets generated, a second process reviews the blueprint and looks for problems: overlapping text, misaligned elements, arrows that point to nothing. It fixes what it finds and checks again. The image you eventually see has already been corrected at least once."

**ICM parallel:** Human review gate between Stage 02 (research) and Stage 03 (script). Agent corrects at stage boundary before passing to next stage. Quality check is architectural — not manual firefighting after the fact.

**V's frame:** "Quality at the source, not quality at the output. By the time something reaches publication, it has already been reviewed — at the stage boundary where problems are cheapest to fix."

**Use in:** T5 (stage contracts), E4 (governance), Tech-2.

---

## The Core Teaching Moment (V's synthesis)

> "Are you using the tool to move faster while staying true to your voice? Or are you reaching for it because it generates something that looks cool in under a minute, and moving on without a second thought? Those are two very different relationships with the same tool."

**V's teaching angle:** This is the "vibe coding" question applied to content. Vibe content = generate and post. ICM content = thinking phase first, rendering phase second, brand voice preserved across both. Same discipline. Different domain.

**V's version:**
> "Every piece of content you publish says something about how you think. AI can generate it fast. Your CONTEXT.md is what makes it say something worth following."

---

## What Was NOT Captured

- Nano Banana 2 specific features — tooling detail
- Step-by-step implementation of the search/download pipeline — out of scope
- Base64 encoding, API specifics — technical detail not V's teaching angle
- Specific image examples (carousel, diagram formats)

## Routed to:

- `quotes_raw.md` → "A detailed prompt can produce similar results once. The difference shows up the second time, the tenth time, six months later." ⭐⭐⭐⭐⭐
- `analogies_bank.md` → Two-phase architecture (thinking → rendering = stages 01-03 → 04)
- Enriches: V1→V5 discovery brief (adds visual domain example), T6, Tech-2, Stage 04 design
- **Possible new topic:** "Your Brand Voice as Infrastructure" — SKILL.md + CONTEXT.md as brand consistency architecture. Connects ICM to personal brand + content creation. Flag for V to greenlight.
