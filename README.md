# Coaching Content Factory — ICM/MWP Edition

Dual-stream video series production: Teaching (ICM zero-to-hero) + Enterprise (AI safety leadership).

This workspace uses **Integrated Context Management (ICM)** and **Model Workspace Protocol (MWP)** to organize knowledge work and produce content at scale.

---

## Quick Start: Running Your First Topic

### Step 1: Gather Topic Input
Answer the questionnaire: `setup/questionnaire.md`

Input needed:
- Topic (e.g., "Token Efficiency and Why It Matters")
- Stream (Teaching / Enterprise / Both)
- Scope (estimated research hours)
- Any background context

### Step 2: Run Stage 01 — Discovery
- Agent reads: `CLAUDE.md` (workspace identity) + `CONTEXT.md` (routing) + `stages/01_discovery/CONTEXT.md` (stage contract)
- Agent produces: `output/[topic-slug]/discovery_brief.md`
- **Human review:** Is research scope clear? Green-light to proceed? → Yes → Continue

### Step 3: Run Stage 02 — Research
- Agent reads: Discovery brief + reference sources + `stages/02_research/CONTEXT.md`
- Agent produces: `output/[topic-slug]/research_output.md`
- **Human review:** Are sources credible? Data backed? → Yes → Continue

### Step 4: Run Stage 03 — Script
- Agent reads: Research output + voice guides (`_config/teaching-voice.md`, `_config/enterprise-voice.md`) + `stages/03_script/CONTEXT.md`
- Agent produces: `output/[topic-slug]/teaching_script.md` (and/or `enterprise_script.md`)
- **Human review:** Can you read this aloud? Does it flow? Tailor notes clear? → Yes → Continue

### Step 5: Run Stage 04 — Multiply
- Agent reads: Scripts + format templates (`references/`) + `stages/04_multiply/CONTEXT.md`
- Agent produces: `output/[topic-slug]/` with all derivatives:
  - `spoken_notes.md` (for recording)
  - `deck_outline.md` (for slide design)
  - `blog_post.md` (for publishing)
  - `linkedin_post.md` (for social)
  - `animation_spec.md` (for animator)
  - `youtube_package.md` (for upload)

### Step 6: Deliver
- All assets ready. Record video, design deck, publish blog, schedule social.

---

## Workspace Architecture (ICM 5 Layers)

```
coaching-icm-mwp/
│
├─ CLAUDE.md              ← Layer 0 (Workspace Identity)
│  └─ Persona: Content architect for dual-stream
│  └─ Constraints: Complete scripts only, safety-first, research-backed
│  └─ Success criteria: 10 teaching × 10 enterprise, each multiply-ready
│
├─ CONTEXT.md             ← Layer 1 (Workspace Routing)
│  └─ "Where am I?" Dual-stream video factory
│  └─ "Where do I go?" 4-stage pipeline (01 discovery → 02 research → 03 script → 04 multiply)
│  └─ Execution model: Folder structure routes work, plain text interface
│
├─ stages/                ← Layer 2 (Stage Contracts)
│  ├─ 01_discovery/       What discovery does (inputs, process, outputs)
│  ├─ 02_research/        What research does
│  ├─ 03_script/          What scripting does (dual-stream output)
│  └─ 04_multiply/        What multiplication does (6 formats from script)
│
├─ _config/               ← Layer 3 (Reference Knowledge & Configuration)
│  ├─ teaching-voice.md           (Tone for teaching stream: analogies, layers, learning outcomes)
│  ├─ enterprise-voice.md          (Tone for enterprise stream: risk, ROI, soundbites)
│  ├─ icm-mwp-framework.md         (Static reference: what ICM/MWP are, why they work)
│  └─ catchphrases.md              (Soundbites library for enterprise scripts)
│
├─ references/            ← Layer 3 Templates (Reusable Formats)
│  ├─ script_template.md           (Dual-stream script structure)
│  ├─ deck_template.md             (Slide outlines, 10-12 slides)
│  ├─ blog_template.md             (Article conversion from script)
│  ├─ animation_template.md        (Visual storytelling spec, scene-by-scene)
│  └─ youtube_template.md          (Title, description, timestamps, tags, metadata)
│
├─ setup/                 ← Layer 3 Configuration (Questionnaire)
│  └─ questionnaire.md    (Topic intake form: topic, stream, scope, context)
│
└─ output/                ← Layer 4 (Working Artifacts & Products)
   └─ [topic-slug]/
      ├─ discovery_brief.md       (Stage 01 output)
      ├─ research_output.md       (Stage 02 output)
      ├─ teaching_script.md       (Stage 03 output, if teaching stream)
      ├─ enterprise_script.md     (Stage 03 output, if enterprise stream)
      ├─ spoken_notes.md          (Stage 04 output)
      ├─ deck_outline.md          (Stage 04 output)
      ├─ blog_post.md             (Stage 04 output)
      ├─ linkedin_post.md         (Stage 04 output)
      ├─ animation_spec.md        (Stage 04 output)
      ├─ youtube_package.md       (Stage 04 output)
      └─ source/
         ├─ discovery_brief.md    (Reference)
         ├─ research_output.md    (Reference)
         └─ [other inputs]        (Reference)
```

---

## How to Use Each Layer

### Layer 0: CLAUDE.md (Workspace Identity)
**When:** Agent starts. Agent reads this to understand workspace persona + constraints.
**What it says:** "I'm a content architect for ICM/MWP teaching. I will NOT ship incomplete scripts. I will NOT merge streams. I WILL research before scripting."

### Layer 1: CONTEXT.md (Workspace Routing)
**When:** Agent reads this after CLAUDE.md to understand the 4-stage pipeline.
**What it says:** "Here are your 4 stages: discovery → research → script → multiply. This is how they connect."

### Layer 2: Stage CONTEXT.md (Contracts)
**When:** Agent navigates to a stage folder. Agent reads this to understand that stage's job.
**Examples:**
- Stage 01: "Read user input (topic, stream, scope). Produce discovery brief with research scope."
- Stage 02: "Read discovery brief. Fetch sources. Produce research output with data, quotes, analogies."
- Stage 03: "Read research. Write dual scripts (teaching + enterprise). Both ready to tailor + deliver."
- Stage 04: "Read scripts. Convert to 6 formats (spoken, deck, blog, LinkedIn, animation, YouTube)."

### Layer 3: Reference Files (_config/ and references/)
**When:** During execution of that stage, agent loads only what it needs.
**Examples:**
- Stage 03 script writing loads: `_config/teaching-voice.md` + `_config/enterprise-voice.md` + `references/script_template.md`
- Stage 04 blog generation loads: `references/blog_template.md` + research + original script
- No stage loads everything; each stage loads 10-15KB context (not 45KB)

### Layer 4: output/ (Working Artifacts)
**When:** Each stage produces files here. Previous stage's output = next stage's input.
**Structure:** One folder per topic (`token-efficiency`, `progressive-disclosure`, etc.). All versions (discovery, research, scripts, derivatives) in one place.

---

## Token Efficiency: Why 5 Layers?

Problem: "Lost in the Middle" — When context is too long, LLM performance degrades.

Solution: Progressive disclosure.

**Example:**

❌ **Load everything at once (all 45KB):**
```
- Workspace identity (5KB)
- All 4 stage contracts (8KB)
- All reference docs (15KB)
- All templates (12KB)
- + topic research (5KB)
= 45KB context for Stage 01 discovery
Result: Token-heavy, slower, less accurate
```

✅ **Load only what Stage 01 needs (12KB):**
```
- Workspace identity (5KB)
- Stage 01 contract (3KB)
- Questionnaire template (2KB)
- + topic input (2KB)
= 12KB context
Result: Fast, cheap, accurate. Stage 01 focused.

Next stage (Stage 02):
- Workspace identity (5KB)
- Stage 02 contract (4KB)
- Research templates (3KB)
- + discovery output (2KB)
= 14KB context
```

**Benefit:** Each stage gets ~12-15KB context (what it needs), not 45KB (noise). Cheaper, faster, more accurate.

---

## Workflow: From Topic to Delivery

### Phase 1: Setup (5 min)
1. User fills `setup/questionnaire.md`
2. Save to `output/[topic-slug]/` folder
3. Ready to run stages

### Phase 2: Research (1-3 hours, depending on scope)
1. **Stage 01 (Discovery):** Agent produces research brief (30 min)
2. **Human review:** Is scope clear? Approve or iterate (15 min)
3. **Stage 02 (Research):** Agent fetches sources, produces research output (1-2 hours)
4. **Human review:** Are sources credible? Data solid? Approve or iterate (15 min)

### Phase 3: Production (2-4 hours, depending on scope)
1. **Stage 03 (Script):** Agent writes 2 scripts (teaching + enterprise) (1-2 hours)
2. **Human review:** Can you read it? Does it flow? Approve or iterate (30 min)
3. **Stage 04 (Multiply):** Agent produces 6 formats (1-2 hours)
4. **Human review:** All assets ready? Approve for delivery (30 min)

### Phase 4: Delivery (Varies)
- Spoken: Record script (professional or DIY, 1-2 hours)
- Deck: Designer converts outline → PowerPoint/Keynote (4-8 hours)
- Blog: Publish markdown → blog platform (30 min)
- LinkedIn: Edit post + trim video clip (30 min)
- Animation: Animator creates spec → MP4 (16-40 hours, depending on complexity)
- YouTube: Upload package (title, description, captions, timestamps, tags) (30 min)

**Total time, soup to nuts:** ~20-50 hours per topic (research + scripting + delivery)

---

## Success Criteria (How to Know It's Working)

✓ **Completeness:** Each script is ready to read aloud, present from deck, understand without context.

✓ **Quality:** Scripts are research-backed. Every claim is sourced. Data cited. Examples work.

✓ **Dual-stream integrity:** Teaching and enterprise scripts are separate. Same truth, different angle. No merged content.

✓ **Multiply-ready:** Scripts have [SLIDE: ...], [DEMO: ...], [PAUSE: ...] markup. Stage 04 can produce all 6 formats without additional scripting.

✓ **Scalability:** 10 topics use same structure. No special handling. Process is repeatable.

✓ **Auditability:** `git log` shows evolution. Human reviews gate each stage. Decisions are documented.

---

## File Naming Convention

**Stage outputs:**
```
[topic-slug]_[stage]_[version].md
Examples:
- token-efficiency_01-discovery_v1.md
- token-efficiency_02-research_v2.md
- token-efficiency_03-script-teaching_v1.md
- token-efficiency_03-script-enterprise_v1.md
```

**Final output:** Keep simple, no versioning (publish-ready)
```
output/token-efficiency/
├─ discovery_brief.md
├─ research_output.md
├─ teaching_script.md
├─ enterprise_script.md
├─ spoken_notes.md
├─ deck_outline.md
├─ blog_post.md
├─ linkedin_post.md
├─ animation_spec.md
└─ youtube_package.md
```

---

## Configuration: Editing Layer 3

Layer 3 (reference files) is where you customize voice, tone, templates, and soundbites library.

**Don't touch:** Stages, Layer 0-2 (workspace structure)
**Do customize:** _config/ and references/ (voice, templates, soundbites)

### Teaching Voice (_config/teaching-voice.md)
Edit this if you want to change how teaching content sounds. Examples:
- More casual? More formal?
- More analogies? More code?
- Different learning progression? (simple-first vs. background-first)

### Enterprise Voice (_config/enterprise-voice.md)
Edit if executive framing changes. Examples:
- More risk-focused? More opportunity-focused?
- Different business angles? (cost savings vs. competitive advantage)
- Different audience? (C-suite vs. board vs. product leaders)

### Catchphrases (_config/catchphrases.md)
Add soundbites as you write scripts. This becomes your enterprise voice signature.

### Templates (references/)
Edit templates if your delivery format changes. Examples:
- Script structure: teaching scripts are 15 min instead of 30 min? Edit `script_template.md`
- Deck: you prefer 20 slides instead of 12? Edit `deck_template.md`
- Blog: your blog uses different sections? Edit `blog_template.md`

---

## Troubleshooting

### "Script isn't ready to read aloud"
Check: Does script have all [SLIDE:...], [DEMO:...], [PAUSE:...] markup? Can you read it without stumbling? If not, re-read script_template.md and iterate.

### "Research is incomplete"
Check: Do you have 5+ sources cited? Is every claim backed by data? If not, run Stage 02 again.

### "I don't know if this is teaching or enterprise angle"
Check: Review `_config/teaching-voice.md` and `_config/enterprise-voice.md`. Teaching = learning outcomes + analogies. Enterprise = ROI + soundbites. Usually both work for most topics.

### "Stage 04 output looks wrong"
Check: Stage 03 markup. [SLIDE:...] too vague? [DEMO:...] missing timing? Markup drives all stage 04 outputs. Fix markup, re-run stage 04.

### "How many topics should I produce?"
Target: 10 teaching + 10 enterprise (20 topics total, 30 min each). Start with 3 teaching (build momentum + confidence), then do 3 enterprise, then scale to 10+10.

---

## Git & Versioning

**Commit each stage:**
```bash
git add output/[topic-slug]/
git commit -m "Stage 01: Discovery brief for [topic]"
git commit -m "Stage 02: Research output for [topic]"
git commit -m "Stage 03: Scripts (teaching + enterprise) for [topic]"
git commit -m "Stage 04: All derivatives for [topic]"
```

**Why:** Easier to track changes. Revert if needed. See evolution over time.

---

## Next Steps

1. Fill out `setup/questionnaire.md` for your first topic
2. Run Stage 01: Read `stages/01_discovery/CONTEXT.md`
3. Produce discovery brief
4. Human review
5. Run Stage 02, Stage 03, Stage 04 (same process)
6. Deliver all assets

You're ready. Start with one topic. The system will guide you.

---

## Reference

- `CLAUDE.md` — Workspace identity
- `CONTEXT.md` — Routing + execution model
- `_config/icm-mwp-framework.md` — Static reference (what ICM/MWP are)
- Original MWP paper: `../../../Interpretable_Context_Methodology_.pdf`

Questions? Check the relevant CONTEXT.md for that stage. Answers are there.
