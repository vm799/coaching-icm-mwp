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
