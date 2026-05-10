# Capture: 2026-05-09 — "Prompting 101: Multimodal Claims Assessment" (NotebookLM Strategic Report)

**Source:** NotebookLM strategic report — "Automating Multimodal Claims Assessment through Iterative AI Development"
**Domain:** Swedish car insurance claims adjudication (multimodal)
**Selective extract — V1→V5 roadmap + failure examples + reasoning architecture only.**
**Status:** PROCESSED ✓

---

## What's Useful (4 things)

### 1. The V1→V5 Transformation Roadmap ⭐⭐⭐⭐⭐

| Stage | Mechanism Added | Business Value |
|-------|-----------------|----------------|
| V1: Basic Prompt | Simple task description | High hallucination risk |
| V2: Persona + Tone | Professional role + factual style | Domain alignment, drift reduction |
| V3: Structural Context | XML tags + Prompt Caching | Token efficiency, precision referencing |
| V4: Reasoning Order | Text-before-Sketch protocol | Logic-based verdicts, ambiguity resolution |
| V5: Output Control | Pre-filling + Serialization | SQL-compatible, automated ingestion |

**V's connection:** ICM stages = V1→V5 codified as repeatable architecture. Every ICM pipeline runs at V5. Every ad hoc prompt starts at V1. The question isn't "which LLM?" — it's "which version of your workflow?"

**Teaching angle:** Show this table. Ask: "Where is your AI workflow today? V1 or V5? Most teams are V2 at best."

**V's frame:**
> "Everyone's prompting. V5 is engineering. V1 is hoping. The difference between them is architecture — not model."

**Use in:** T2 (how ICM works), T7 (stages as version upgrades), Tech-3, any teaching opener that needs a concrete maturity model.

---

### 2. The Chappangan Failure — Perfect Teaching Story ⭐⭐⭐⭐⭐

> "Without an anchored persona, the model interpreted a car accident report as a skiing incident because 'Chappangan' is a common Swedish location associated with skiing activities. This error is not a model failure — it is a failure of contextual anchoring."

**V's use:** Classic zero-context failure. No persona → model uses statistical association → wrong domain → wrong output. This is not a bug in the model. It is a missing L0 (identity/persona) in the workflow.

**Teaching analogy:** "You hired a new analyst. Gave them a document. No briefing. No context. They made a reasonable guess — and guessed wrong. That's not incompetence. That's missing onboarding. CLAUDE.md is the onboarding."

**Enterprise angle:** "Chappangan isn't an edge case. It's what happens at scale when your AI team runs without context architecture. Every workflow running at V1 has its own Chappangan waiting."

**Use in:** T1 (what is ICM), T3 (why context matters), E1 (enterprise risk opener), Tech-1 (vibe coding).

---

### 3. Reasoning Order = ICM's Progressive Disclosure ⭐⭐⭐⭐

> "Prioritize Low-Entropy Evidence Channels (Text) over High-Entropy Visual Noise (Sketches). Analyze structured text first → document factual claims → corroborate with sketch."

**V's connection:** Text-before-Sketch = ICM's selective context loading. Load structured, deterministic context first (L0-L2). Introduce high-entropy, interpretive content later (stage-specific research, user input). Same principle.

**Technical frame:** Low-entropy first = stage contracts (deterministic). High-entropy later = research, ideation, creative stages. Reasoning order is architecture, not accident.

**Use in:** Tech-2 (stage contract design), T5 (progressive disclosure), any technical talk on context loading order.

---

### 4. Extended Thinking = Audit Trail Argument

> "Extended Thinking capabilities generate a 'scratchpad' accessible via thinking tags that allow human auditors to analyze the transcript of the model's logic. Essential for insurance compliance."

**V's connection:** MWP stage outputs are the audit trail. Every intermediate file = scratchpad made permanent. EU AI Act Article 14 (human oversight) satisfied architecturally — not via debugging. V's glass-box framing.

**Use in:** E4/E5 (safe AI / glass-box), EU AI Act talks, any regulated industry audience (insurance, FS, healthcare).

---

## The V1→V5 ICM Mapping (V's frame, not in source)

| V stage | ICM equivalent |
|---------|---------------|
| V1: Basic prompt | No CLAUDE.md, no context |
| V2: Persona + tone | CLAUDE.md identity layer (L0) |
| V3: Structural context | Stage CONTEXT.md + reference knowledge (L2-L3) |
| V4: Reasoning order | Stage gate pipeline (00→01→02→03→04) |
| V5: Output control | Stage contract: defined inputs, outputs, schema |

**V's frame:** "V5 isn't a prompt. V5 is a workspace. V5 is ICM."

---

---

## Delta Capture — Second NotebookLM Version (2026-05-09)

Same source, different framing ("Structural Prompting: Building Clearer Paths for AI Intelligence"). Three new concepts not in original extract:

### Delta 1: "Context Bleed" — Named Problem ICM Solves ⭐⭐⭐⭐

> "XML tags prevent the AI from mistaking background evidence for a new instruction — preventing 'context bleed' between instructions and data."

**V's connection:** Context bleed between stages = exactly what stage separation prevents. Stage 02 research doesn't bleed into Stage 03 script instructions. Each CONTEXT.md is a sealed boundary.

**New term for analogies_bank.md:** "Context bleed" — when model confuses instructions with data. ICM stage contracts are the XML tags of AI workflow design.

**Use in:** Tech-2 (stage contract design), T5 (one job per stage), any talk explaining why you can't run all stages in one prompt.

### Delta 2: Prompt Caching = ICM L0-L2 Static Layers

> "Putting static structure in the system prompt allows for Prompt Caching, which dramatically reduces costs and latency for repetitive tasks."

**V's connection:** ICM L0 (CLAUDE.md) + L1 (workspace CONTEXT.md) = static layers. Loaded once per session. Change per-topic only at L3-L4. This IS prompt caching by architecture.

**Use in:** Tech-3 (token efficiency), enterprise cost argument, any CTO/platform engineer talk.

### Delta 3: "Single Message vs Conversational" — Enterprise API Frame

> "Enterprise-grade applications require a 'single message' approach — the AI must nail the task on the first attempt. One-shot success reduces costs, lowers latency, builds systems reliable enough for industrial-scale deployment."

**V's connection:** ICM stage outputs = one-shot by design. Stage contract defines exact inputs + expected output → agent produces complete deliverable in one pass. Human review gate is NOT a re-prompt. It is approval or rejection of a complete artifact.

**Use in:** E2 (ICM vs ad hoc), Tech-3, any enterprise talk on moving from chat to API-driven pipeline.

---

---

## Delta Capture — Third NotebookLM Version (2026-05-09)

"Technical Standard: High-Reliability Prompt Architecture for Production Environments." Three new concepts not in prior extracts:

### Delta 4: System/User Bifurcation = ICM L0-L3 vs L4 ⭐⭐⭐⭐⭐

| Element | Message Tier | ICM Equivalent |
|---------|-------------|---------------|
| Task Role | System Prompt | CLAUDE.md — L0 identity |
| Background Data | System Prompt | _config/ references — L3 |
| Core Instructions | System Prompt | Stage CONTEXT.md — L2 |
| Few-Shot Examples | System Prompt | references/ templates — L3 |
| Dynamic User Input | User Prompt | Topic input, stage-specific data — L4 |
| Final Reminder | User Prompt | Stage gate constraints |

**V's frame:** "System vs User prompt bifurcation IS the ICM layer separation — made explicit. L0-L3 = system prompt (static, cached, loaded once). L4 = user prompt (dynamic, per-topic). This is not a metaphor. This is why ICM's layers are architecturally correct."

**Use in:** Tech-2 (stage contract design), T4 (ICM layers explained), any talk bridging API prompt architecture to ICM workspace design.

### Delta 5: Analytical Verbs — Persona Engineering

> "The role definition must command the model to audit, extract, reconcile, and adjudicate data. 'Helpful assistant' is not a persona — it is an instruction to guess."

**V's connection:** CLAUDE.md persona verbs matter. V's stage contracts use: "You are a research specialist. Extract, synthesise, cite." Not "You are a helpful assistant." Precision verbs constrain reasoning space.

**New rule for script writers:** Every CONTEXT.md persona uses analytical verbs (audit, extract, reconcile, synthesise, adjudicate, validate). Never "helpful," "assist," or "support."

**Use in:** Tech-2 (CONTEXT.md design), T6 (stage contract deep-dive), enterprise prompt hygiene talks.

### Delta 6: Temperature 0.0 + CoT vs Extended Thinking

> "Temperature must be set to 0.0 for all production tasks to ensure deterministic, consistent results."

> "Chain-of-Thought = explicit instructions for model to narrate its reasoning. Extended Thinking = dedicated thinking transcript (Claude 3.7+) for engineer review."

**V's connection:** ICM stage outputs are deterministic by design (temperature 0 = idempotent stages). CoT = reasoning visible in stage output. Extended Thinking = scratchpad = ICM audit trail made explicit.

**Use in:** Tech-3 (production pipeline settings), E4 (audit trail / compliance), technical audiences on determinism.

---

## What Was NOT Captured

- Full Swedish form structure details (17 checkboxes, specific field names) — domain-specific, not V's angle
- XML tag implementation specifics — tooling detail, not teaching content
- Pre-filling / output steering implementation code — out of scope
- Prompt Caching implementation specifics

## Routed to:

- `quotes_raw.md` → V1→V5 table + Chappangan failure quote
- `analogies_bank.md` → "Chappangan = missing onboarding" analogy
- New topic → `output/v1-to-v5-the-pipeline-argument/` → Stage 01 to follow
- Enriches: T2, T7, Tech-1, Tech-3, E1, E4
