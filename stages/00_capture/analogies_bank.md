# Analogies Bank — Teaching Metaphors + Mappings

Used by Stage 02 (Research) and Stage 03 (Script) to make concepts tangible.
Add every analogy that lands — from talks, videos, conversations, reading.

---

## Active Analogies

### "Questions are gold" (AI expertise)
**Concept:** In AI age, question quality = expertise
**Analogy:** "A world where answers are cheap makes questions precious. A Google search gives you an answer. An expert gives you the right question to ask next."
**Teaching use:** Video on expert framing, ICM as question-engineering
**Enterprise use:** Competitive moat framing — "your AI strategy is only as good as your questions"
**Source:** Instagram 2026-04-28
**Rating:** ⭐⭐⭐⭐⭐

---

### "Agents = organized software" (LangChain objection)
**Concept:** Agents aren't magic — just tools + data + LLM + code
**Analogy:** "A GitHub repo with prompts, API calls, and Python. The LLM is wrapped around it. The intelligence comes from the design, not the framework."
**Teaching use:** De-mystify agents for engineers and BAs
**Enterprise use:** "You don't need a framework. You need a design system."
**Source:** Instagram 2026-04-28 (V's paraphrase)
**Rating:** ⭐⭐⭐⭐

---

### "Context = library card, not library" (token efficiency)
**Concept:** Load a pointer to knowledge, not all knowledge
**Analogy:** "A library doesn't hand you every book when you ask a question. It gives you the catalog. You request the book. That's context efficiency."
**Teaching use:** Token efficiency, selective context
**Enterprise use:** Cost reduction framing
**Source:** Existing (in _config/icm-mwp-framework.md)
**Rating:** ⭐⭐⭐⭐⭐

---

### "Tokens are attention" (cost + focus)
**Concept:** Tokens represent cognitive focus — limited and expensive
**Analogy:** "Tokens are attention. Attention is expensive. Every token you load that isn't needed is borrowed from the answer."
**Teaching use:** Why we filter context
**Enterprise use:** API cost framing
**Source:** Existing catchphrase
**Rating:** ⭐⭐⭐⭐⭐

---

### "Stages = Unix pipes" (MWP architecture)
**Concept:** One job per stage, output feeds next
**Analogy:** "Unix pipes: `ls | grep | sort`. Each command does one thing. The output of one becomes the input of the next. MWP is the same — discovery pipes to research pipes to script pipes to multiply."
**Teaching use:** Why MWP uses staged pipeline (for engineers)
**Enterprise use:** "Each stage has one owner. Each stage has a clear contract."
**Source:** ICM framework, SWE principles
**Rating:** ⭐⭐⭐⭐

---

### "AI is 70 years old" (expectation setting)
**Concept:** AI isn't new magic — it's matured engineering
**Analogy:** "John McCarthy coined 'AI' in 1956. Your grandparents were alive. This isn't magic — it's 70 years of theory finally meeting accessible compute and plain-English interfaces."
**Teaching use:** Video 1 opener — remove mysticism
**Enterprise use:** "The inflection isn't intelligence. It's accessibility."
**Source:** Instagram 2026-04-28
**Rating:** ⭐⭐⭐⭐

---

---

### "Multi-pass compiler" (MWP pipeline architecture)
**Concept:** MWP stages = compiler passes. Each transforms intermediate representation.
**Analogy:** "A compiler doesn't convert source to binary in one shot. It lexes, parses, analyses, optimises, links. Each pass reads the output of the last. MWP is identical: capture → discover → research → script → multiply. Each stage reads the previous stage's output."
**Teaching use:** T8 — "The compiler and the AI pipeline". Engineers: instant recognition.
**Enterprise use:** "Your AI pipeline should work like a compiler — show its work at each step."
**Source:** Van Clief & McDermott (2026), Section 6.1
**Rating:** ⭐⭐⭐⭐⭐

---

### "Patching the binary" (edit-source principle)
**Concept:** Editing AI output without fixing the source = technical debt
**Analogy:** "If a compiler produces wrong output and you edit the binary directly, it works once. The next time you compile, the bug is back. ICM: every correction belongs in the source — the config, the stage contract, the voice guide. Not the output."
**Teaching use:** T7 — "Don't patch binaries". Core productivity principle.
**Enterprise use:** "Every output fix that doesn't update the source is a recurring cost."
**Source:** Van Clief & McDermott (2026), Section 6.3. Quote: "Editing the output is patching the binary."
**Rating:** ⭐⭐⭐⭐⭐

---

### "Glass box vs black box" (AI observability)
**Concept:** MWP is inherently observable — no explanation layer needed
**Analogy:** "A black box: you push input in, output comes out. If it's wrong, you guess why. A glass box: every intermediate state is visible. MWP is a glass box by design. Every stage output is a file you can open and read."
**Teaching use:** T6 — Stage contracts and handoffs.
**Enterprise use:** E7 — "Glass-box AI: what boards actually need to see." EU AI Act.
**Source:** Van Clief & McDermott (2026), Section 5.3. Rudin (2019) [45].
**Rating:** ⭐⭐⭐⭐⭐

---

### "Tasteable recipe stages" (pipeline observability, non-technical)
**Concept:** Every pipeline step produces an inspectable intermediate result
**Analogy:** "Imagine a recipe where every step produces a dish you can taste before adding it to the next. Wrong flavour? Fix it here, not at the end. That's ICM. Every stage output is tasteable: readable, editable, correctable before it feeds downstream."
**Teaching use:** T4, T8 — for non-engineers. Accessible version of compiler analogy.
**Enterprise use:** "Readable outputs at each stage = human review at each stage."
**Source:** Adapted from Van Clief & McDermott (2026) pipeline architecture
**Rating:** ⭐⭐⭐⭐

---

### "Literate programming" (CONTEXT.md as instruction + documentation)
**Concept:** Stage contracts are simultaneously instruction for agents and documentation for humans
**Analogy:** "Donald Knuth's literate programming: code and documentation woven into one document. The CONTEXT.md is this — the agent reads it to know what to do; the human reads it to understand what happened. One file, two audiences, zero ambiguity."
**Teaching use:** T6 — Stage contracts.
**Enterprise use:** "No separate documentation. The system documents itself."
**Source:** Van Clief & McDermott (2026), citing Knuth (1984) [literps citation]
**Rating:** ⭐⭐⭐⭐

---

---

### "Football League" (quadratic attention scaling)
**Concept:** Adding tokens to a context window scales attention quadratically, not linearly
**Analogy:** "Adding teams to a football league. Two teams: one match. Three teams: three matches. Every new team adds relationships with every existing team — the number explodes. LLMs work the same way. Every new token must relate to every other token already in the window. That's why the Smart Zone has a real ceiling — it's physics, not a product limitation."
**Teaching use:** Tech-2 — why Smart Zone matters. Non-engineers: use "football league." Engineers: use "O(n²) attention complexity."
**Enterprise use:** "Context window claims are marketing. The physics are quadratic. ICM keeps every stage inside the curve."
**Source:** NotebookLM synthesis of software entropy framework (2026-04-29). Underlying concept: transformer attention mechanism.
**Rating:** ⭐⭐⭐⭐⭐

---

### "Day Shift / Night Shift" (human-AI division of labour)
**Concept:** Human owns the Day Shift (planning, alignment, design). AI owns the Night Shift (execution, AFK autonomy).
**Analogy:** "You are the Day Shift: planning, grilling, aligning, designing interfaces. The AI is the Night Shift: executing, coding, testing — while you sleep. The Day Shift determines whether the Night Shift produces gold or garbage."
**Teaching use:** Tech-1, Tech-6 — division of labour. Accessible to non-technical audiences too (T7/T8).
**Enterprise use:** "Your knowledge workers become Day Shift strategists. AI becomes Night Shift executors. The value of the Day Shift goes up, not down."
**Source:** NotebookLM synthesis (2026-04-29).
**Rating:** ⭐⭐⭐⭐⭐

---

### "Phosphorescent feedback" (tracer bullets)
**Concept:** Tracer bullets leave a visible trail — immediate feedback on whether aim is correct
**Analogy:** "A tracer round fired in the dark glows as it travels. You can see exactly where your aim is. That's what a vertical slice gives you — a glowing line through every layer of the system, showing whether the architecture holds before you've built everything. Without it, you're firing blind in the dark."
**Teaching use:** Tech-7 — tracer bullets. Replaces "immediate feedback" with a memorable image.
**Enterprise use:** "You're building for six months before you know if the architecture works. Tracer bullets compress that to six hours."
**Source:** NotebookLM synthesis (2026-04-29). Underlying concept: Hunt & Thomas, Pragmatic Programmer.
**Rating:** ⭐⭐⭐⭐⭐

---

### "Sediment" (context accumulation / why stages reset)
**Concept:** Context from previous turns accumulates and degrades reasoning quality
**Analogy:** "Sediment builds in a river. The longer it runs without clearing, the murkier the water. LLMs work the same way — accumulated context from earlier turns clouds reasoning in later ones. ICM stage contracts clear the sediment. Each stage starts with clean, scoped context."
**Teaching use:** T4 — why ICM stages load selectively, not cumulatively. Better word than "context degradation" for non-technical audiences.
**Enterprise use:** "Your AI isn't getting worse — it's accumulating sediment. ICM prevents it architecturally."
**Source:** Software entropy framework (2026-04-29 capture). Connects to Liu et al. (2024) "lost in the middle" finding.
**Rating:** ⭐⭐⭐⭐⭐

---

### "Smart Zone vs Dumb Zone" (effective reasoning window)
**Concept:** LLMs have an effective reasoning limit ~100K tokens regardless of stated context window
**Analogy:** "Every LLM has a Smart Zone — where it reasons well — and a Dumb Zone — where attention scales quadratically and reasoning fails. The context window claim is marketing. The Smart Zone is the engineering reality. ICM keeps every stage inside the Smart Zone. Monolithic prompts push into the Dumb Zone."
**Teaching use:** T4 — why selective context loading isn't about saving money, it's about staying in the zone where the model actually works.
**Enterprise use:** E4 cost case — "You're paying for 100K tokens. The model reasons well on 8K. ICM closes that gap."
**Source:** Software entropy framework (2026-04-29 capture).
**Rating:** ⭐⭐⭐⭐⭐

---

### "Deep module vs shallow module" (ICM stage architecture)
**Concept:** Deep modules = simple interface, complex implementation contained inside. Shallow = scattered logic, complex interface.
**Analogy:** "Ousterhout's deep module: simple interface, complex internals hidden. A shallow codebase scatters logic across dozens of files — the agent jumps around and loses coherence. A deep module wraps all that logic behind one clean boundary. ICM stages are deep modules: one input spec (CONTEXT.md), one output contract, all logic contained. The agent owns the implementation. The human owns the interface."
**Teaching use:** T5/T6 — maps SWE principle (Ousterhout) directly to ICM architecture.
**Enterprise use:** "Your AI fails on shallow systems. Deep module design = the AI can reason without getting lost."
**Source:** John Ousterhout, "A Philosophy of Software Design" (cited in software entropy framework 2026-04-29). Cite Ousterhout directly.
**Rating:** ⭐⭐⭐⭐⭐

---

## Template: Add New Analogy

```markdown
### "[Concept shorthand]"
**Concept:** [What ICM/MWP idea does this explain?]
**Analogy:** "[The actual analogy — as you'd say it aloud]"
**Teaching use:** [Where in teaching stream this fits]
**Enterprise use:** [Where in enterprise stream this fits]
**Source:** [Where it came from]
**Rating:** ⭐ to ⭐⭐⭐⭐⭐
```
