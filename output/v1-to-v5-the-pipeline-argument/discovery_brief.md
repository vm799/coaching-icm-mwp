# Discovery Brief: "Everyone's Prompting. V5 Is Engineering. V1 Is Hoping."

**Topic slug:** v1-to-v5-the-pipeline-argument
**Stage:** 01 — Discovery
**Date:** 2026-05-09
**Streams:** Teaching (primary), Technical (secondary), Enterprise (secondary)
**Status:** AWAITING HUMAN REVIEW — proceed to Stage 02 when greenlit

---

## One-Line Hook

> "V1 is a prompt. V5 is a workspace. The difference between them is architecture — and most teams are running at V2."

---

## The Core Claim

Every AI workflow has a version. V1 — basic prompt, no context, no persona — produces probabilistic drift and hallucination. V5 — defined persona, structured context, reasoning order, output schema — produces production-grade, auditable results. The gap between V1 and V5 is not model capability. It is architectural discipline.

ICM/MWP is V5 codified as a repeatable system. Every stage (00→04) is a version upgrade applied systematically. The question for any team isn't "which AI tool?" — it's "what version is your workflow running?"

The Chappangan failure is the canonical teaching example: a Swedish car accident report misread as a skiing incident because the model had no persona, no domain anchor, no context. Not a model failure. A V1 failure.

---

## Triple-Stream Angles

### Teaching Angle (30 min — PRIMARY)
**Audience:** BAs, managers, non-technical learners getting started with AI
**Hook:** "You've been prompting. There are five versions of what prompting can be. Most teams are at V2. Here's what V5 looks like — and how to get there."
**Thesis:** The V1→V5 maturity model is a practical roadmap. Each version adds one architectural discipline. ICM stages encode V5 permanently so you never fall back to V1.
**Payoff:** "By the end of this session, you'll know exactly what version your workflow is — and what to add to reach V5."
**Format:** Chappangan story → V1→V5 table → ICM mapping → stage-by-stage upgrade → V5 checklist

### Technical Angle (25 min — SECONDARY)
**Audience:** Developers, platform engineers, technical leads
**Hook:** "The Chappangan failure isn't an edge case. It's what V1 looks like in production. Here's the engineering path from V1 to V5 — and why ICM encodes it systematically."
**Thesis:** V3 (structural context + XML tags) → V4 (reasoning order: text before sketch / low-entropy before high-entropy) → V5 (output schema + serialization) map directly to ICM stage contracts. Each stage is a V-version upgrade applied once, reused for every topic.
**Payoff:** "You don't re-engineer for every prompt. You build V5 once. Every topic runs inside it."
**Format:** V1→V5 walkthrough → ICM stage mapping table → demo: same input at V1 vs V5 → output comparison

### Enterprise Angle (15 min — SECONDARY)
**Audience:** CTO, Head of Digital, risk/compliance
**Hook:** "Chappangan isn't a curiosity. Every enterprise AI deployment without context architecture has its own Chappangan waiting. Here's the risk profile — and how V5 eliminates it."
**Thesis:** V1 = probabilistic drift = business risk. V5 = deterministic, auditable, schema-compliant = enterprise-grade. The extended thinking audit trail (scratchpad) = ICM stage outputs = EU AI Act compliance by architecture.
**Payoff:** "V5 isn't about better prompts. It's about building a system where audit, compliance, and confidence are structural properties — not afterthoughts."
**Format:** Risk frame (Chappangan at scale) → V1→V5 business risk table → V5 as compliance architecture → ICM as V5 deployed

---

## Confirmed Sources (Stage 00)

1. **NotebookLM Strategic Report (2026-05-09)** — V1→V5 roadmap, Chappangan failure, text-before-sketch protocol, extended thinking audit trail
2. **Van Clief & McDermott (2026)** — ICM stages as V5 equivalent, stage contracts as output control, Figure 3 (token load)
3. **Karpathy (Feb 2025)** — vibe coding = V1 applied to software development (from Tech-1 research)
4. **Liu et al. (2024) — "Lost in the Middle"** — scientific basis for reasoning order (low-entropy first)
5. **Hunt & Thomas, Pragmatic Programmer** — tracer bullets as V4-equivalent (vertical slices, structured feedback)

**Additional sources needed (Stage 02):**
- Real production failure examples beyond Chappangan (enterprise AI incidents with root cause = missing context)
- Anthropic documentation on Extended Thinking / thinking tags (for technical accuracy)
- EU AI Act Article 14 exact wording (human oversight requirement — for enterprise/compliance angle)
- Gartner or similar: AI pilot failure rate attributed to prompt/context quality vs model quality

---

## Key Analogies

**Chappangan = Missing Onboarding**
> "You hired a new analyst. Gave them a document. No briefing, no context, no domain framing. They made a reasonable guess — and guessed wrong. That's not incompetence. That's missing onboarding. CLAUDE.md is the onboarding."

**V1→V5 = Code Quality Levels**
> "Every developer knows the difference between a V1 prototype and production code. Same logic applies to AI workflows. V1 runs. V5 ships. The difference is architecture."

**Low-Entropy First = Signal Before Noise**
> "Expert analysts read the structured form before looking at the hand-drawn sketch. Low-entropy evidence first, high-entropy later. ICM stages encode this order permanently — structured context loads before interpretive work begins."

**V5 Is Not a Prompt — It's a Workspace**
> "V5 doesn't live in a chat window. It lives in a folder structure. CLAUDE.md, CONTEXT.md, stage contracts, voice guides — that's V5. That's ICM. You build it once; every topic runs inside it."

---

## The Kitchen/Recipes Connection

This topic directly extends the kitchen/recipes catchphrase already in catchphrases.md:

- V1 = optimising a recipe with no kitchen
- V2 = buying one piece of kitchen equipment
- V5 = designing the kitchen (context engineering = kitchen design)

**V's integrated frame:**
> "Prompt engineering taught you to write better recipes. V5 is when you stop writing recipes and start designing kitchens. ICM is the kitchen."

---

## Objection Map

**"Our prompts are already working."**
Teaching: V2 "works" until it doesn't — first edge case, first language boundary, first context shift. V2 is fragile. V5 is resilient. What version are you willing to ship to production?

**"This seems complex."**
Technical: V5 is not one complex thing. It's five simple additions, each adding one layer. ICM encodes all five once. Every topic after that runs at V5 automatically.

**"The model will improve and handle this."**
Enterprise: Model improvement ≠ context discipline. V1 on a better model is still V1. Chappangan on GPT-5 is still a Chappangan. The version of your workflow is independent of the model.

---

## Script Structure (30 min — Teaching Primary)

```
0:00 — Hook: Chappangan story — "This is what V1 looks like in production"
3:00 — The V1→V5 maturity model: introduce the table
5:00 — V1: what goes wrong (Chappangan, probabilistic drift, missing persona)
8:00 — V2: persona + tone — what changes (domain alignment, drift reduction)
11:00 — V3: structural context — what changes (XML anchors, prompt caching, token efficiency)
14:00 — V4: reasoning order — low-entropy first (text before sketch = stage contracts)
18:00 — V5: output control — schema, pre-filling, serialization (stage output contracts)
22:00 — ICM mapping: "V5 isn't a prompt. It's a workspace."
25:00 — Kitchen/recipes connection: context engineering = designing the kitchen
27:00 — Checklist: What version is your workflow?
30:00 — Close: "Everyone's prompting. V5 is engineering."
```

---

## Human Review Gate Questions

1. Is V1→V5 teaching model standalone (own video) or part of an existing T-series slot?
2. Does the Chappangan example land for non-insurance audiences — or need a more generic failure story alongside it?
3. Kitchen/recipes connection — include in this topic or keep those separate to avoid dilution?
4. Should Technical angle cover pre-filling / output steering implementation or stay conceptual?
5. Is "Extended Thinking" audit trail angle strong enough for EU AI Act / compliance talk — or needs its own dedicated session?
