# MWP/ICM Paper Breakdown — Series Mapping

**Source:** Jake Van Clief & David McDermott, "Interpretable Context Methodology: Folder Structure as Agent Architecture"
**Published:** 2026 (internal reference), Eduba / University of Edinburgh
**GitHub:** https://github.com/RinDig/Model-Workspace-Protocol-MWP-
**License:** MIT
**Citation format:** Van Clief & McDermott (2026) — cite with page number

---

## How to Use This File

Each section maps to:
- **T[n]** = Teaching series video number (1-10)
- **E[n]** = Enterprise series video number (1-10)
- Extract quotes → `quotes_raw.md`
- Extract analogies → `analogies_bank.md`
- Cross-reference against series plan in `output/*/discovery_brief.md`

---

## Paper Series Mapping Overview

| Paper Section | Teaching Video | Enterprise Video |
|--------------|----------------|-----------------|
| 2.1 Unix + SWE lineage | T3: "Why I build this way" | — |
| 2.2 Context engineering | T2: "Context engineering, not prompt engineering" | E2: "The language of AI systems" |
| 2.3 Human oversight | — | E2: "Safe AI = observable AI" |
| 3.1 Five design principles | T5: "The 5 principles of MWP" | — |
| 3.2 Architecture + Figures 1 + 3 | T4: "ICM layers explained" | E4: "The cost case for context architecture" |
| 3.3 Stage contracts | T6: "Stage contracts and clean handoffs" | E3: "Why AI projects fail at handoff" |
| Table 1: MWP vs frameworks | T9: "Why not LangChain" | E5: "Framework lock-in and how to avoid it" |
| 4.5 Practitioner data | — | E6: "This works in production" |
| 5.3 Observability | — | E7: "Glass-box AI: what boards actually need" |
| 5.4 Implications for intelligent systems | T10: "Advanced: Systems that improve" | — |
| 6.1 Multi-pass compilation | T8: "The compiler analogy" | — |
| 6.3 Edit-source principle | T7: "Don't patch binaries" | E8: "AI systems that improve over time" |

---

## Section 2.1 — Unix Tradition and SWE Lineage

**Maps to:** T3 — "Why I build this way: ICM/MWP and 50 years of SWE"
**Themes:** Unix philosophy, pipe-and-filter architecture, one tool one job, plain text as interface

### Paper Argument
Van Clief & McDermott root MWP in three SWE traditions:
1. **Unix philosophy** (McIlroy, 1978) — write programs that do one thing well, connect via plain text
2. **Pipe-and-filter pattern** (Shaw & Garlan, 1996) — staged transformation of data through independent components
3. **Separation of concerns** (Dijkstra, 1974) — reduce complexity by assigning each component a single responsibility

**Direct application:** MWP stages = Unix processes. CONTEXT.md = process contract. Plain text files = universal interface (stdin/stdout). Git = version-controlled state.

### Citable Quotes

> "The power of a Unix system comes more from the relationships among programs than from the programs themselves."
> — Kernighan & Pike (1984), cited in Van Clief & McDermott [5]

> "Write programs that do one thing and do it well. Write programs that work together. Write programs that handle text streams, because that is a universal interface."
> — McIlroy (1978), cited in Van Clief & McDermott [1]

### Teaching Angle — T3
- V's build methodology isn't a personal preference — it's 50 years of SWE evidence
- "Every ICM stage is a Unix process. The CONTEXT.md is the contract. The output file is stdout."
- Learning outcome: engineers and BAs understand *why* V builds this way, not just *what* V builds
- Addresses implicit objection: "isn't this overengineering?"

### Soundbites for T3
> "I didn't invent this. I inherited 50 years of SWE wisdom and applied it to AI."
> "Unix pipes taught us: one job, one output, compose at the boundary. ICM is that principle applied to AI agents."

---

## Section 2.2 — Context Engineering vs Prompt Engineering

**Maps to:** T2 — "Context engineering: the real work behind AI systems"
**Maps to:** E2 — "Why 'just improve your prompts' is the wrong advice"
**Themes:** Context vs prompt, Karpathy framing, what context engineering actually means

### Paper Argument
The paper cites Karpathy's June 2025 correction of the field: the real skill is *context engineering* — deliberately filling the context window with the right information, structure, and format to guide model behavior. "Prompt engineering" understates and misdirects.

Van Clief & McDermott extend this: MWP is a *context engineering system*. Each stage's CONTEXT.md defines precisely what context the model sees, when, and in what form. Nothing leaks between stages unless explicitly passed.

### Citable Quotes

> "+1 for 'context engineering' over 'prompt engineering.' It's a more accurate description of the work."
> — Andrej Karpathy, June 2025 (cited as [16] in Van Clief & McDermott)

> "The folder structure tells it what to do at each step."
> — Van Clief & McDermott (2026), p.1

### Teaching Angle — T2
- "Prompt engineering" = what you say to the model right now
- "Context engineering" = what the model knows, in what order, in what form, across the whole session
- ICM/MWP is a context engineering system: L0-L4 layers, selective loading, stage contracts
- Link to token efficiency: better context = fewer tokens needed to get same quality output

### Enterprise Angle — E2
- "Prompt engineering" implies: make the message better → board/exec will tune this out
- "Context engineering" implies: design the knowledge architecture → board/exec will invest in this
- Framing shift: from "AI prompting" to "AI context architecture" → higher-value conversation
- Karpathy quote = credibility anchor (founder of Tesla AI, Stanford AI researcher)

### Soundbites
> "Prompt engineering is what you write. Context engineering is what you build." — V (paraphrase of Karpathy/Van Clief)
> "The shift from prompts to context is the shift from tactics to strategy."

---

## Section 2.3 — Human Oversight and Interpretability

**Maps to:** E2 — "Safe AI = observable AI: what EU AI Act compliance looks like in practice"
**Maps to:** E7 — "Glass-box AI: what boards actually need to see"
**Themes:** Interpretability, EU AI Act, human-in-the-loop, auditability, Rudin citation

### Paper Argument
Van Clief & McDermott argue that MWP produces interpretability as an architectural byproduct — not as a post-hoc explanation layer. Every intermediate output is a readable file. Human review gates are structurally enforced. Nothing is hidden.

They cite Rudin (2019) against black-box AI: the answer isn't better explanations for opaque systems — it's inherently interpretable system design.

EU AI Act compliance angle: staged intervention points, human review at each stage boundary, full audit trail in plain text, version-controlled via git.

### Citable Quotes

> "Stop building opaque systems and then trying to explain them after the fact. Build systems that are inherently interpretable."
> — Rudin (2019), cited as [45] in Van Clief & McDermott

> "A production pipeline where every intermediate output is a readable file is inherently interpretable. There is nothing to explain because nothing was hidden."
> — Van Clief & McDermott (2026), p.4

### Enterprise Angle — E2 / E7
- EU AI Act (2024): high-risk AI systems must have human oversight + intervention capability
- MWP provides this architecturally: stage gates = mandated human review points
- "Glass box" framing: any stakeholder (board, regulator, auditor) can open any file and read the decision chain
- Contrast: LangChain/LangGraph pipelines are opaque — logs exist but require interpretation
- V's consulting delivers compliance-ready AI architecture by default

### Soundbites
> "Your AI doesn't need better explanations. It needs to stop hiding things."
> "If a regulator asked you to explain your AI's last decision, could you show them a file? ICM: yes. Everything else: maybe."

### Key Figure — Figure 5: U-Shaped Intervention Pattern
From practitioner data (52-person community):
- 92% interventions at Stage 1 (discovery/framing)
- 30% at Stage 2 (research enrichment)
- 78% at Stage 3 (script finalisation)
- Implication: human review isn't overhead — it's where the real value is added
- Enterprise angle: "The AI does the drafting. Experts do the deciding."

---

## Section 3.1 — Five Design Principles of MWP

**Maps to:** T5 — "The 5 principles that make ICM/MWP work"
**Themes:** Architecture principles, repeatability, composability

### The 5 Principles (Van Clief & McDermott)

1. **Single Responsibility** — each stage does one job, defined by its CONTEXT.md
2. **Explicit Interfaces** — input/output of each stage fully specified; no implicit coupling
3. **Progressive Context Loading** — each stage loads only the context it needs for its task
4. **Human Review Gates** — mandated review at stage boundaries before downstream execution
5. **Plain Text Primacy** — all stage inputs and outputs are human-readable plain text files

### Teaching Angle — T5
- Map each principle to a SWE equivalent (Unix, SOLID, Domain-Driven Design)
- "You've been applying these principles in software for decades. ICM applies them to AI."
- Learning outcome: practitioners can self-assess any AI pipeline against these 5 principles
- Makes V's methodology teachable, defensible, auditable

### Key Quote

> "The simplest viable architecture for this class of problem is one that already exists on every computer: the filesystem."
> — Van Clief & McDermott (2026), p.8

### Soundbites for T5
> "Five principles, not five frameworks. One principle applied consistently beats ten frameworks applied occasionally."
> "Every principle reduces one failure mode. Together, they produce a system that doesn't hallucinate at scale."

---

## Section 3.2 — Architecture: ICM Layers and Token Efficiency

**Maps to:** T4 — "ICM layers explained: why 5 layers, not one big prompt"
**Maps to:** E4 — "The cost case for context architecture"
**Themes:** 5-layer hierarchy, selective loading, token efficiency, Figure 1 + Figure 3

### Key Architecture Argument
Van Clief & McDermott formalise ICM into 5 layers:
- **L0:** Global (workspace identity, cross-cutting constraints)
- **L1:** Domain (pipeline routing, stream definitions)
- **L2:** Stage (CONTEXT.md — what this stage does)
- **L3:** Config/Reference (voice guides, templates, framework reference)
- **L4:** Working memory (active scripts, research outputs)

Each layer answers a specific question:
- L0: Who am I? What will I never do?
- L1: Where am I in the pipeline?
- L2: What is this stage's job?
- L3: What rules and knowledge apply?
- L4: What am I working with right now?

### Key Figure — Figure 1: ICM Layer Hierarchy
5-layer pyramid. Each layer loaded only when its scope is active. L0-L2 ≈ 1,300-1,600 tokens. L3 ≈ 500-2,000 tokens. L4 varies by task.

### Key Figure — Figure 3: Token Counts Per Stage
| Approach | Token Load | Risk |
|----------|-----------|------|
| Monolithic prompt | 40,000-80,000 tokens | Context degradation, "lost in middle" |
| ICM per-stage | 2,000-8,000 tokens | Minimal, scoped to task |
| ICM total session | 12-15KB loaded | Controlled, auditable |

**Liu et al. [25] finding:** LLMs perform significantly worse when relevant information is buried in the middle of long contexts. ICM's selective loading solves this architecturally.

### Teaching Angle — T4
- "A 40,000-token prompt is like handing someone a 200-page manual and asking them to answer one question. ICM gives them the right page."
- Layer-by-layer walkthrough: what lives where, why, what it costs to load
- Learning outcome: BA/manager can design their own ICM workspace from scratch

### Enterprise Angle — E4
- Token cost = direct API cost. Context bloat = money wasted.
- ICM: 2,000-8,000 tokens per stage vs 40,000+ monolithic = 60-80% cost reduction per query
- At AT&T scale (27B tokens/day): 40% reduction = billions of tokens saved daily
- "You're not paying for intelligence. You're paying for context. Make every token earn its place."

### Citable Quotes

> "LLMs perform significantly worse when relevant information is buried in the middle of long contexts."
> — Liu et al. (2024), cited as [25] in Van Clief & McDermott

### Soundbites for E4
> "Tokens are attention. Every token you don't load is a token that can't confuse the answer."
> "Context architecture is cost architecture. Design it deliberately or pay for it accidentally."

---

## Section 3.3 — Stage Contracts (CONTEXT.md)

**Maps to:** T6 — "Stage contracts: how to make AI handoffs clean"
**Maps to:** E3 — "Why AI projects fail at the handoff point"
**Themes:** Stage contracts, explicit interfaces, handoff failure patterns

### Paper Argument
Each stage is governed by a CONTEXT.md that defines:
- **Input:** what this stage receives (format, source, required fields)
- **Process:** what this stage does (scoped, single-responsibility)
- **Output:** what this stage produces (format, destination, validation criteria)
- **Success criteria:** how to know this stage is complete

Van Clief & McDermott draw on Literate Programming (Knuth, 1984): the CONTEXT.md is simultaneously instruction and documentation. The agent reads it to know what to do; the human reads it to understand what happened.

### Citable Quotes

> "The most common failure pattern in agentic pipelines is not model capability — it is interface ambiguity between stages."
> — Van Clief & McDermott (2026), p.11

### Teaching Angle — T6
- "A stage contract is a function signature for humans and agents simultaneously."
- Map to API contracts, database schemas, test contracts — same principle
- Demo: open any stage CONTEXT.md, read it aloud, show it's self-explanatory
- Learning outcome: practitioners can write stage contracts for their own pipelines

### Enterprise Angle — E3
- Most enterprise AI failures happen at the handoff: model → review → action
- Ambiguous handoffs = decisions made on incomplete context
- Stage contracts = mandatory interface definition: who receives what, in what form, with what review gate
- "Every handoff is a compliance point. Stage contracts make that point explicit."

### Soundbites for T6/E3
> "The contract isn't for the AI. It's for the human who reviews the output before it becomes a decision."

---

## Table 1 — MWP vs Framework Comparison

**Maps to:** T9 — "Why not LangChain: the honest comparison"
**Maps to:** E5 — "Framework lock-in and how to avoid it"
**Source:** Van Clief & McDermott (2026), Table 1

### The Comparison (6 dimensions)

| Dimension | MWP/ICM | LangChain/LangGraph |
|-----------|---------|---------------------|
| Interpretability | Every intermediate output readable | Logs require interpretation |
| Human review | Structurally enforced at stage gates | Optional, developer-configured |
| Dependency | Filesystem + git (zero lock-in) | Framework version dependency |
| Debugging | Open any file, read the state | Stack traces, internal state |
| Compliance | Audit trail is architectural byproduct | Requires additional instrumentation |
| Token efficiency | Per-stage selective loading | Typically session-wide context |

**4 dimensions where frameworks win:**
- Complex graph orchestration (multi-branch agent trees)
- Built-in integrations (vector stores, memory backends, tools marketplace)
- Community tooling and examples
- Rapid prototyping speed

### Teaching Angle — T9
- "LangChain and ICM are not competitors. One is a library. The other is a design system."
- Honest framing: frameworks win for prototypes and complex graphs. ICM wins for production, compliance, and teaching.
- "Use LangChain to explore. Use ICM when you need to explain what happened."
- Addresses engineers' most common objection directly, with data

### Enterprise Angle — E5
- Framework lock-in = vendor risk, version upgrades, dependency hell
- MWP: zero framework dependency (filesystem + git = exists on every machine)
- "If LangChain changes its API, your pipeline breaks. If the filesystem changes, call the FBI."
- Compliance angle: frameworks require additional audit tooling. ICM compliance is structural.

### Soundbites for T9/E5
> "LangChain is great at connecting things. ICM is great at explaining them. In a regulated environment, explanation wins."
> "The audit trail isn't something you bolt on after. It's the folder structure you build in."

---

## Section 4.5 — Practitioner Community Data

**Maps to:** E6 — "52 practitioners, 6 months: what the data shows"
**Source:** Van Clief & McDermott (2026), Section 4.5

### The Data
- 52-person practitioner community using MWP/ICM in production
- 6-month study period
- Key finding: U-shaped intervention pattern

### U-Shaped Intervention Pattern (Figure 5)
- **Stage 1 (Discovery):** 92% of sessions had human intervention → framing is the highest-value human contribution
- **Stage 2 (Research):** 30% of sessions had human intervention → model handles research well with correct framing
- **Stage 3 (Script):** 78% of sessions had human intervention → output quality, voice, tailoring

**Implication:** Human expertise concentrates at framing and finalisation. The middle is where AI earns its keep.

### Citable Quotes

> "The intervention pattern confirms that the highest-value human contribution is not execution — it is framing. Practitioners intervene most at the point where the problem is defined, not where it is solved."
> — Van Clief & McDermott (2026), p.16

### Enterprise Angle — E6
- "Your experts shouldn't be doing AI's work. Your experts should be doing what AI cannot do: framing the problem."
- ROI reframe: don't measure AI by cost reduction alone. Measure where human expertise gets redeployed.
- 92% Stage 1 intervention = "AI drafts, experts decide" in practice
- Addresses "AI will replace my team" objection: no — it reassigns your team to higher-value work

### Soundbites for E6
> "The data says: 92% of the value humans add is at the framing stage. That's not a small thing. That's the whole thing."
> "52 practitioners, 6 months. The model handles the middle. Humans own the boundaries."

---

## Section 5.3 — Observability and Glass-Box AI

**Maps to:** E7 — "Glass-box AI: what boards actually need to see"
**Themes:** Observability, auditability, regulatory compliance, glass vs black box

### Paper Argument
Van Clief & McDermott distinguish:
- **Black box:** Input → output. No readable intermediate state.
- **Glass box:** Input → readable intermediate states → output. Every decision traceable.

MWP is structurally glass-box: each stage writes its output as a readable file. Any stakeholder can inspect state at any point. No special tooling required.

Regulatory application: EU AI Act requires high-risk AI systems to maintain logs and enable human oversight. MWP's plain-text, git-versioned pipeline satisfies this architecturally.

### Citable Quotes

> "A production pipeline where every intermediate output is a readable file is inherently interpretable. There is nothing to explain because nothing was hidden."
> — Van Clief & McDermott (2026), p.4

> "Stop building opaque systems and then trying to explain them after the fact. Build systems that are inherently interpretable."
> — Rudin (2019), cited as [45] in Van Clief & McDermott

### Enterprise Angle — E7
- Board question: "Can you show me what the AI decided and why?" MWP: open the file.
- EU AI Act (2024), Article 14: human oversight requirements for high-risk AI systems
- MWP compliance properties: human review gates, plain-text audit trail, git version history, no external dependencies
- "You don't need an XAI layer if your system was interpretable from the start."

### Soundbites for E7
> "Black-box AI needs an explanation layer. Glass-box AI is the explanation."
> "Regulators don't want a dashboard. They want a file they can read."

---

## Section 5.4 — Implications for Intelligent System Design

**Maps to:** T10 — "Advanced: designing AI systems that improve over time"
**Themes:** System design principles, emergence, feedback loops, self-improving architecture

### Paper Argument
Van Clief & McDermott argue MWP produces systems that improve through use:
- Stage contracts tighten as edge cases are captured
- Config files (voice guides, catchphrases) accumulate practitioner knowledge
- Git history provides improvement trajectory
- Human review feedback feeds back into stage design (not just output tuning)

This is the distinction between **patching outputs** and **improving the system**.

### Teaching Angle — T10
- "Every correction you make to an AI output is data. The question is: where does that data go?"
- ICM routing: corrections → config files → stage contracts → better outputs next time
- Contrast: prompting → correction → re-prompting → same error next time
- "The system improves. The operator doesn't burn out."

### Soundbites for T10
> "You can fix the output or you can fix the system. Only one of those is engineering."

---

## Section 6.1 — Multi-Pass Compilation Analogy

**Maps to:** T8 — "The compiler: why AI pipelines need passes, not one big call"
**Themes:** Compilation theory, intermediate representation, progressive transformation

### Paper Argument
Van Clief & McDermott draw explicit parallel between MWP and multi-pass compilers:
- Stage 00 (Capture) = lexer: raw input tokenised and classified
- Stage 01 (Discovery) = parser: structure and intent extracted
- Stage 02 (Research) = semantic analysis: meaning, context, dependencies resolved
- Stage 03 (Script) = code generation: structured output produced
- Stage 04 (Multiply) = optimisation + linking: output transformed for each target

Each pass produces an intermediate representation (IR) — readable, inspectable, correctable before the next pass.

**Key insight:** Debugging a compiler is easy because the IR is visible. Debugging an opaque AI pipeline is hard because there is no IR.

### Citable Quote

> "The multi-pass compiler does not ask the programmer to trust it. It shows its work at every intermediate step."
> — Van Clief & McDermott (2026), p.19

### Teaching Angle — T8
- For engineers: "You already trust this architecture in your compiler. Apply it to your AI pipeline."
- For non-engineers: "A recipe where every step produces a dish you can taste before adding to the next is easier to fix than one that runs start to finish and produces something inedible."
- Each stage = a pass. Each CONTEXT.md = the IR schema. Each output file = the compiled intermediate.

### Soundbites for T8
> "Every compiler shows its work. Your AI pipeline should too."
> "If you can't read the intermediate output, you can't fix the pipeline."

---

## Section 6.3 — The Edit-Source Principle

**Maps to:** T7 — "Don't patch binaries: the edit-source principle for AI"
**Maps to:** E8 — "AI systems that improve over time: the compounding advantage"
**Themes:** Source vs output, root cause vs symptom, technical debt in AI

### Paper Argument
Van Clief & McDermott name a pervasive failure pattern: practitioners who receive AI output they don't like edit the output directly. This is "patching the binary."

The correct intervention is to edit the **source** — the config, the stage contract, the voice guide, the research brief — so the output is correct by construction next time.

### Citable Quote

> "Editing the output is patching the binary. It works, but it does not improve the compiler."
> — Van Clief & McDermott (2026), p.18

### Teaching Angle — T7
- "If you edit the output and don't update the source, you're accumulating technical debt."
- Walk through: bad output → identify source → fix config → regenerate → good output
- ICM routing: corrections feed upstream (L3 config) not downstream (L4 output)
- Learning outcome: practitioners know which layer to edit for any type of correction

### Enterprise Angle — E8
- Compounding advantage: each source-level fix improves all future outputs
- Contrast: each output-level fix costs expert time every single time
- "Your AI gets better if you invest in the source. It stays the same if you only fix outputs."
- ROI framing: source edits compound. Output edits are recurring costs.

### Soundbites for T7/E8
> "Edit the source. Not the output. One is engineering. The other is groundhog day."
> "Every output fix that doesn't update the source is technical debt. It comes due eventually."

---

## Key Figures Summary

### Figure 1 — ICM 5-Layer Hierarchy
**Use in:** T4, any context explaining ICM architecture
**Description:** Pyramid showing L0-L4. Arrows showing selective loading direction. Token count estimates per layer.
**Teaching use:** "Here's what the AI sees at each layer — and what it doesn't."
**Enterprise use:** "This is why your AI doesn't need to know everything to do its job."

### Figure 3 — Token Counts Per Stage (ICM vs Monolithic)
**Use in:** T4, E4 (cost case)
**Description:** Bar chart. Monolithic: 40,000-80,000 tokens. ICM per stage: 2,000-8,000 tokens.
**Key data:** ~80% token reduction per query. Direct cost implication.
**Enterprise use:** Slide 4 in cost-case deck. "This is where your token budget goes."

### Figure 5 — U-Shaped Intervention Pattern
**Use in:** E6 (practitioner data), any talk on human-AI collaboration
**Description:** Line graph. X-axis: pipeline stages. Y-axis: % of sessions with human intervention.
**Data:** Stage 1: 92%. Stage 2: 30%. Stage 3: 78%.
**Enterprise use:** "Your experts add most value at the beginning and end. ICM structures this."

### Table 1 — MWP vs Framework Comparison
**Use in:** T9 (why not LangChain), E5 (framework lock-in)
**Description:** 10-row table. 6 dimensions where MWP wins (interpretability, compliance, etc.). 4 where frameworks win (complex graphs, integrations, prototyping speed).
**Teaching use:** "Here's the honest comparison. Choose based on your actual requirements."
**Enterprise use:** "For regulated AI in production: this is why MWP wins."

---

## Master Quote List (Extract → quotes_raw.md)

All ⭐⭐⭐⭐⭐ — cite Van Clief & McDermott (2026) unless marked otherwise.

1. **"The folder structure tells it what to do at each step."** — p.1. T1/E1 opener. Accessible, memorable.

2. **"A production pipeline where every intermediate output is a readable file is inherently interpretable. There is nothing to explain because nothing was hidden."** — p.4. ⭐⭐⭐⭐⭐ BOARD-LEVEL. EU AI Act.

3. **"The simplest viable architecture for this class of problem is one that already exists on every computer: the filesystem."** — p.8. Teaching + enterprise. Simplicity argument.

4. **"The most common failure pattern in agentic pipelines is not model capability — it is interface ambiguity between stages."** — p.11. Enterprise diagnosis framing.

5. **"The intervention pattern confirms that the highest-value human contribution is not execution — it is framing."** — p.16. ROI argument for human expertise.

6. **"Editing the output is patching the binary. It works, but it does not improve the compiler."** — p.18. ⭐⭐⭐⭐⭐ CATCHPHRASE.

7. **"The multi-pass compiler does not ask the programmer to trust it. It shows its work at every intermediate step."** — p.19. Engineering credibility.

8. **"+1 for 'context engineering' over 'prompt engineering.' It's a more accurate description of the work."** — Andrej Karpathy, June 2025 [16]. ⭐⭐⭐⭐⭐ opens E2.

9. **"LLMs perform significantly worse when relevant information is buried in the middle of long contexts."** — Liu et al. (2024) [25]. Technical evidence for selective context loading.

10. **"Stop building opaque systems and then trying to explain them after the fact. Build systems that are inherently interpretable."** — Rudin (2019) [45]. ⭐⭐⭐⭐⭐ EU AI Act.

11. **"The power of a Unix system comes more from the relationships among programs than from the programs themselves."** — Kernighan & Pike (1984) [5]. SWE lineage.

12. **"Write programs that do one thing and do it well."** — McIlroy (1978) [1]. Foundation principle.

---

## New Analogies (Extract → analogies_bank.md)

1. **Multi-pass compiler** → MWP stages. Each stage = compiler pass. Output = intermediate representation. Teaching: T8. Rating: ⭐⭐⭐⭐⭐
2. **Patching the binary** → editing AI output without fixing the source. Teaching: T7, E8. Rating: ⭐⭐⭐⭐⭐
3. **Glass box vs black box** → MWP observability vs opaque pipelines. Enterprise: E7. Rating: ⭐⭐⭐⭐⭐
4. **Literate programming (Knuth)** → CONTEXT.md as simultaneous instruction + documentation. Teaching: T6. Rating: ⭐⭐⭐⭐
5. **Recipe with tasteable stages** → every pipeline step produces inspectable output. Teaching: T4, T8. Rating: ⭐⭐⭐⭐

---

## New Topics for topics_backlog.md (Paper-Validated)

1. **"Don't patch binaries: why editing AI output is technical debt"** — T7. Direct from Section 6.3. Kicker quote ready.
2. **"The compiler and the AI pipeline: passes, IRs, and why it matters"** — T8. Section 6.1. Engineers-first topic.
3. **"Glass-box AI: what boards actually need to see"** — E7. Section 5.3. EU AI Act + Rudin. Board-level.
4. **"52 practitioners, 6 months: what the practitioner data shows"** — E6. Section 4.5. U-shaped intervention data.
5. **"Why your AI project fails at the handoff"** — E3. Section 3.3. Practitioner + enterprise crossover.

---

## EU AI Act Compliance Angles (Extract → enterprise_angles.md)

**Source:** Van Clief & McDermott (2026), Section 2.3 + 5.3

MWP/ICM satisfies EU AI Act (2024) Article 14 (human oversight) requirements as architectural byproduct:

| EU AI Act Requirement | MWP/ICM Implementation |
|----------------------|------------------------|
| Human oversight capability | Mandated review gates at every stage boundary |
| Ability to intervene | Human edit permitted at every stage output before downstream execution |
| Audit trail | Git-versioned plain-text files. Every state captured. |
| Interpretability | No hidden state. Every intermediate output readable by any stakeholder. |
| Logging and documentation | CONTEXT.md = simultaneous documentation + instruction |

**V's enterprise angle:**
> "ICM doesn't need compliance bolted on. The folder structure IS the compliance architecture."

**For boards and legal teams:**
> "Show me your AI audit trail."  
> "Here's the git repo. Every decision is a file. Every file has a timestamp. Every review gate has a signature."

---

*Breakdown complete. Cross-reference: `quotes_raw.md`, `analogies_bank.md`, `enterprise_angles.md`, `topics_backlog.md`*
*Source: Van Clief & McDermott (2026), "Interpretable Context Methodology: Folder Structure as Agent Architecture"*
