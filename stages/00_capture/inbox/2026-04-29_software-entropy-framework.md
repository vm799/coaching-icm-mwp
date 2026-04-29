# Capture: 2026-04-29 — "Strategic Framework for AI-Native Software Modernization"

**Source:** Unknown author (no attribution in content)
**Captured by:** V
**Selective extract — NOT full document. Take only what serves V's content.**
**Status:** PROCESSED ✓

## What's Useful (4 things)

### 1. "Vibe Coding" as Teaching Foil

**Concept:** "Vibe coding" = reactive, prompt-heavy, iterate-until-it-works. No structure. No design. AI as black-box compiler.

> "As AI tools become ubiquitous, the true competitive advantage is no longer the ability to generate code, but the ability to apply rigorous engineering to a non-deterministic process."

**V's reframe for teaching stream:**
> "Vibe coding is fun until production. ICM is what you build when you need things to actually work."

**Use in:** T9 "Why not LangChain" (LangChain encourages vibe coding; ICM enforces structure). Teaching Video 2 or 3.

**Note:** "Vibe coding" is already a known term (Andrej Karpathy coined it, Feb 2025). Attribute correctly when using.

---

### 2. "Sediment" = Better Word for Context Degradation

**Concept:** Sediment = accumulated context from previous turns that strains LLM attention. The longer you run without clearing context, the worse reasoning becomes.

> "Sediment is the accumulation of tokens and context from previous turns that strains the LLM's attention. By clearing context and starting fresh from the system prompt, we keep the agent in the 'Smart Zone' for every new issue."

**V's existing argument** (Liu et al. [25]): "lost in the middle" — LLMs perform worse when relevant info buried in long contexts.

**New word to add to teaching vocabulary:** "Sediment" is more vivid than "context degradation." Easier to explain to non-engineers. Connects to ICM stage contracts: each stage clears sediment by scoping context deliberately.

**Use in:** T4 "ICM layers explained" — "Stage contracts prevent sediment buildup. Each stage starts clean."

---

### 3. "Smart Zone" Validates V's Token Efficiency Argument

**Concept:** Effective reasoning ends around 100K tokens regardless of model's claimed window. Beyond = "Dumb Zone" — quadratic attention scaling, reasoning failures.

> "Regardless of whether a model has a 1M+ token window, the 'Smart Zone' effectively ends at 100,000 tokens. Beyond this, attention relationships scale quadratically."

**Connects to:** Van Clief Figure 3 (2,000-8,000 tokens per ICM stage vs 40,000+ monolithic). ICM keeps every stage deep inside the Smart Zone. Monolithic prompts push into the Dumb Zone.

**Use in:** T4 (ICM layers) + E4 (cost case). "Smart Zone" is a better teaching frame than raw token numbers.

---

### 4. Deep Modules = ICM Stages (Architecture Analogy)

From John Ousterhout, "A Philosophy of Software Design":

| Shallow Module | Deep Module |
|---------------|-------------|
| Complex interface | Simple interface |
| Logic scattered | Logic contained |
| Hard to test | Easy to test |
| Agent jumps across dozens of files | Agent owns the boundary |

**V's mapping:**
- ICM stage = deep module. One job. Simple input/output interface (CONTEXT.md). Logic contained.
- Monolithic prompt = shallow module. Complex interface. Logic scattered.
- "The agent owns the implementation. The human owns the interface." ← strong teaching line.

**Use in:** T5 "5 principles of MWP" + T6 "Stage contracts". SWE precedent (Ousterhout) adds academic grounding alongside Van Clief/McIlroy.

---

## Routed to:

- `analogies_bank.md` → "Sediment" + "Smart Zone" + "Deep module vs shallow module"
- `quotes_raw.md` → 2 quotes (vibe coding framing + sediment)
- Does NOT spawn new topic — enriches T4, T5, T6, T9 (existing series)
- Attribution needed: "vibe coding" = Karpathy (Feb 2025), "deep modules" = Ousterhout. Author of this document unknown — do not cite document directly.
