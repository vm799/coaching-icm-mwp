# Topics Backlog — Candidate Topics for Stage 01

Ideas not yet through discovery. Add anytime. Stage 01 picks from here.

Format: Priority (1=urgent) | Topic | Stream | Source | Notes

---

## Technical Stream — Full Series (10 Videos)

**Audience:** Developers, technical leads, engineers building with AI.
**Source:** Software entropy framework (2026-04-29) + SWE precedents (Ousterhout, Pragmatic Programmer, Brooks, Evans, McIlroy)
**Status:** All 10 topics ready for Stage 01. Research brief = full technical capture file.

### Tech-1: "Vibe coding is a trap: software entropy in the AI era"
- **Hook:** "Vibe coding offers an illusion of speed. Architecture is the primary constraint on AI reasoning. Ignored code is rotting code."
- **Core:** Software entropy (Pragmatic Programmer), ball of mud, bounty of modernization
- **Research:** Hunt & Thomas (entropy), Karpathy (vibe coding Feb 2025)

### Tech-2: "Context engineering for engineers: Smart Zone, sediment, and selective loading"
- **Hook:** "The context window is the claim. The Smart Zone is the reality."
- **Core:** Smart Zone (~100K effective), sediment clearing, ICM as architectural solution
- **Research:** Liu et al. (2024) "lost in the middle", Van Clief Figure 3, Van Clief sediment

### Tech-3: "Deep modules for agentic codebases: the gray box strategy"
- **Hook:** "Human owns the interface. Agent owns the implementation. That's the gray box."
- **Core:** Ousterhout deep/shallow modules, gray box, Quiz Scoring Service example
- **Research:** Ousterhout "A Philosophy of Software Design" (2018)

### Tech-4: "AI-native TDD: how to stop the cheating LLM"
- **Hook:** "The test isn't for you. It's for the LLM that will try to cheat it."
- **Core:** Red-Green-Refactor enforced, cheating LLM failure mode, TDD as Smart Zone preserver
- **Research:** Beck "Test-Driven Development: By Example" (2002)

### Tech-5: "TypeScript + AI: types as deterministic safety net"
- **Hook:** "The LLM produces what you accept. TypeScript decides what you accept."
- **Core:** Structural feedback, typed stage interfaces, tradeoff analysis (strict vs loose)
- **Research:** TypeScript docs, typed interface pattern for MWP stages

### Tech-6: "The Ralph Wiggum loop: AFK autonomy without the chaos"
- **Hook:** "Plan, Execute, Clear. The Clear step is the one everyone skips. It's also the one that saves the project."
- **Core:** Three-step loop, Memento management, sediment prevention, context-fresh-per-task
- **Research:** Memento (film) as metaphor, ICM stage pipeline as implementation

### Tech-7: "Tracer bullets and vertical slices: why AI agents code horizontally and why that's wrong"
- **Hook:** "Horizontal coding delays feedback. Vertical slices accelerate it."
- **Core:** Tracer bullets (Pragmatic Programmer), feature-complete thin paths, feedback earliness
- **Research:** Hunt & Thomas "tracer bullets", feature slicing pattern

### Tech-8: "Ubiquitous language in AI systems: your glossary is your codebase's constitution"
- **Hook:** "If the agent and the human use different words for the same thing, the codebase will too."
- **Core:** DDD ubiquitous language, markdown glossary, Grill Me / shared design concept (Brooks)
- **Research:** Evans "Domain-Driven Design" (2003), Brooks "Mythical Man-Month" (1975)

### Tech-9: "MWP as software architecture: Unix pipes, deep modules, and the engineer's path"
- **Hook:** "I didn't invent this. I inherited 50 years of SWE wisdom and applied it to AI."
- **Core:** Full SWE lineage table, engineer's path (gray box), ICM as architecture not framework
- **Research:** Van Clief & McDermott (2026), McIlroy, Ousterhout, Evans, Shaw & Garlan

### Tech-10: "Building AI-native pipelines: live demo from vibe coding to production"
- **Hook:** "Software fundamentals — types, tests, architecture — matter more now than they ever did."
- **Core:** Full pipeline live demo, Stage 00-04 walkthrough, from entropy to AI hero
- **Research:** Full repo as demo, all prior technical series videos as foundation

---

## Priority 1 — Ready for Stage 01

### "Company Brain: what YC says doesn't exist yet — and how ICM builds it"
- **Stream:** Enterprise (primary) — CTO, CEO, board, investors
- **Source:** YC Summer 2026 RFS, Tom Blomfield (#4: Company Brain), Diana Hu (#15: AI OS for Companies)
- **Hook:** "YC just published 15 problems they'll fund. Problem 4 is called 'Company Brain.' Tom Blomfield — co-founder of Monzo — wrote: 'The AI tools exist. The company brain layer does not yet.' I've been building it for two years."
- **Enterprise angle:** YC's #4 describes ICM exactly: structured knowledge, executable skills file for AI, living map of how the company works. V has the answer. The market doesn't know it yet.
- **Teaching angle:** What "Company Brain" is technically: L0-L4 context hierarchy. CLAUDE.md = the skills file. Stage contracts = the map.
- **Soundbites ready:** YES — Blomfield quote is ⭐⭐⭐⭐⭐
- **Market validation:** YC = the most credible signal in tech startup funding. This is investor-grade positioning.
- **Systems thinking:** Company Brain = feedback loop closure. Open loop (scattered knowledge) → closed loop (queryable, agent-executable knowledge). Diana Hu: "turns a company from an open loop into a closed loop."
- **Notes:** STRONGEST EXTERNAL VALIDATION V HAS RECEIVED. Lead enterprise talks with this. Open: "YC tells founders what to build. They just described my practice."

---

### "Why questions matter more than answers in the AI age"
- **Stream:** Both (teaching + enterprise)
- **Source:** Instagram video capture 2026-04-28
- **Hook:** "In a world where answers are cheap, questions are precious"
- **Teaching angle:** ICM as a question-engineering system. Expert = best questions.
- **Enterprise angle:** Question quality = moat. Not AI adoption — AI questioning.
- **Soundbite ready:** YES — "Questions are gold. Experts are the ones that can ask the right questions."
- **Links to:** AI history (McCarthy 1956, Claude researcher) — good hook for credibility
- **Notes:** V wants this in multiple talks. Strong opening topic for enterprise stream.

### "Why not LangChain / LangGraph — the case for ICM/MWP"
- **Stream:** Teaching (engineers) primarily; enterprise secondary
- **Source:** Instagram video + V's recurring Q&A question (2026-04-28)
- **Hook:** "Building agents is just organized software around tools and data with an LLM wrapped around a GitHub repo"
- **Teaching angle:** What libraries do vs don't do. Context design is the real work.
- **Enterprise angle:** Vendor risk. Debuggability. Auditability. ICM is vendor-independent.
- **Objection rebuttal ready:** YES — see `objections_bank.md`
- **Notes:** This is the "why we build the way we build" topic. Core differentiator for V's brand.

---

### "Systems thinking: the lens beneath everything V does"
- **Stream:** Both — teaching (Video 2 or 3) + enterprise (Video 2)
- **Source:** V's approach — explicit now (2026-04-28)
- **Hook:** "AI is not a tool. It's a node in a system you design."
- **Teaching angle:** ICM/MWP as systems design. Every stage = stock, flow, feedback loop, leverage point.
- **Enterprise angle:** Most AI problems are systems problems. Archetypes, leverage points, iceberg model.
- **Soundbite ready:** YES — "One change at the right leverage point outperforms ten at the wrong one."
- **Config ready:** YES — `_config/systems-thinking.md` (full lens, concepts, mappings, references)
- **Cross-link:** Every other topic references this. It's the meta-frame.
- **Notes:** Don't make this an isolated video — thread systems thinking language through ALL content. Explicit video + implicit lens throughout series.

---

### "Glass-box AI: what boards actually need to see"
- **Stream:** Enterprise (primary) — board, legal, compliance, CISO
- **Source:** Van Clief & McDermott (2026), Section 5.3; Rudin (2019); EU AI Act (2024) Article 14
- **Hook:** "Your regulator doesn't want a dashboard. They want a file they can read."
- **Enterprise angle:** EU AI Act compliance. Glass-box vs black-box architecture. No XAI retrofitting needed.
- **Soundbites ready:** YES — Rudin + Van Clief + V's own framing
- **Data ready:** 52-person practitioner study, Article 14 requirements table
- **Systems thinking:** Observability = feedback loop health. Can't improve what you can't see.
- **Notes:** Strong for legal/compliance audience + board. Makes V the EU AI Act practitioner. High differentiation.

### "Don't patch binaries: the edit-source principle for AI"
- **Stream:** Teaching (engineers/BAs primary)
- **Source:** Van Clief & McDermott (2026), Section 6.3
- **Hook:** "Editing the output is patching the binary. It works, but it does not improve the compiler."
- **Teaching angle:** Root cause vs symptom fix. Where corrections belong in ICM (L3 config, not L4 output).
- **Enterprise angle:** Technical debt framing. Every output fix that doesn't update source = recurring cost.
- **Soundbites ready:** YES — "edit source not output" catchphrase
- **Notes:** Great follow-on after T5/T6. Shows practitioners how to improve the system, not just the output.

---

### "Agent skill governance: who controls what your agent can do?"
- **Stream:** Enterprise (primary) — CISO, CTO, Compliance, AI governance teams
- **Source:** Ken Huang, "The Skill System Pattern" (Hermes Agent), April 2026
- **Hook:** "When agents write agents — and skills teach other skills — you need a trust model. Not just for the output. For the capability itself."
- **Enterprise angle:** Skill trust tiers (built-in vs trusted vs community vs agent-created). Security scanning for agent capabilities. /.well-known/skills as emerging standard (= YC #12 Software for Agents).
- **Governance frame:** Who wrote this skill? What can it access? Has it been scanned? Most enterprise AI deployments have no answer.
- **Systems thinking:** Reinforcing loop risk — agent-created skills that teach agents to create more skills. Without governance, capability drift is unbounded.
- **Notes:** Emerging topic. Field is moving toward skill marketplaces. V's clients need governance framework before they need the marketplace. Strong CISO / legal angle alongside CTO.

---

### "Agentic commerce: what UCP means for enterprise AI teams"
- **Stream:** Enterprise (primary) — CTO, CPO, product leaders, digital commerce
- **Source:** Ken Huang, Agentic AI Substack, April 2026
- **Hook:** "Checkout is the final mile of commerce. It is not commerce. The same is true for your AI."
- **Enterprise angle:** $1.2T US ecommerce market restructuring around AI agents. UCP = context negotiation protocol, not checkout API. ICM/MWP is the internal architecture equivalent.
- **ICM connection:** UCP's "ugly middle" (product data, rules, fulfillment, loyalty, fraud) = same problem ICM solves for enterprise AI. Context architecture is the competitive layer.
- **Data ready:** $1.2T market, 70.22% cart abandonment, Walmart 1/3 conversion rate in ACP test, Amazon/Meta/Microsoft/Stripe/Salesforce all joined UCP Tech Council Apr 24 2026
- **Soundbites ready:** YES — "Checkout is the final mile. Not commerce." + "Universal but not uniform." + Huang "ugly middle" quote
- **Systems thinking:** Protocol wars → governance wars → context layer ownership. Reinforcing loop: whoever sets the context standard shapes the value extraction.
- **EU AI Act angle:** AP2 cryptographic mandates = agent non-repudiation. Parallel to ICM audit trail.
- **Notes:** New vertical for enterprise stream. Works as standalone "future of commerce" talk OR as concrete illustration of context architecture problem. Strong for digital commerce, retail, fintech audiences.

---

## Priority 2 — Strong Candidates

### "The AI Value Gap: why enterprises pay for AI and don't get the value"
- **Stream:** Enterprise (primary) — CTO, CFO, CPO, board
- **Source:** Molham Aref / RelationalAI + Ashley Kramer / OpenAI VP Enterprise (April 2026)
- **Hook:** "Model capabilities aren't the issue. There's a huge gap between what models can provide and the value enterprises are actually extracting." — Ashley Kramer, OpenAI
- **Enterprise angle:** Three-part gap: missing context, missing decision tooling, missing business-specific training. ICM closes gap 1 (and enables 2 and 3).
- **Cost data ready:** AT&T 27B tokens/day, MIT $25B savings, Foundation Capital trillion-dollar context opportunity
- **Soundbites ready:** YES — 5 quotes ⭐⭐⭐⭐⭐ from OpenAI VP + Aref
- **Systems thinking:** Decision-making under uncertainty = complex system, no counterfactuals, context quality = only lever
- **Notes:** Strong for board/CFO. Validates V's entire practice with investor + enterprise executive sources. High credibility.

### "Why large organisations lose to small teams — and how to fight back"
- **Stream:** Enterprise (primary) — board, C-suite, product leaders
- **Source:** Hardik Pandya article + Cursor/Copilot case study (2026-04-28)
- **Hook:** "Twelve people beat Microsoft. Not because they were smarter. Because they had a tighter context loop."
- **Enterprise angle:** Incentive inversion + immune system + blunted edge = three reasons large orgs can't operate at frontier. ICM/MWP = the fix.
- **Case study ready:** YES — Cursor ($1B, 12 people) vs GitHub Copilot (Microsoft, full moat)
- **Soundbites ready:** YES (5 Pandya quotes, all ⭐⭐⭐⭐⭐)
- **Systems thinking:** Reinforcing loops (narrators → narrators), balancing loops gone wrong (immune system), delays (frontier gap), leverage points (context architecture)
- **Notes:** Strong standalone enterprise video AND enriches every other enterprise topic. Attribution to Pandya required.

### "AI is 70 years old — and why that matters now"
- **Stream:** Enterprise (intro talk) + Teaching (Video 1 of series)
- **Source:** Instagram capture 2026-04-28
- **Hook:** "John McCarthy coined 'AI' in 1956. Claude the researcher was in that room."
- **Teaching angle:** History grounds the learner. AI isn't magic — it's engineered.
- **Enterprise angle:** The inflection point isn't intelligence. It's accessibility.
- **Notes:** Good opening for either stream's first video. Sets "this isn't new, you're not late" tone.

### "Token efficiency: why selective context beats comprehensive context"
- **Stream:** Teaching (engineers/BAs) + Enterprise (cost + scale)
- **Source:** ICM framework — core concept
- **Hook:** "Tokens are attention. Attention is expensive."
- **Notes:** Core technical topic for Teaching stream. Has measurable ROI for Enterprise.

### "Progressive disclosure: the teaching principle that scales to AI"
- **Stream:** Teaching primarily
- **Source:** MWP paper + teaching voice config
- **Hook:** "Experts think in layers. Teach in layers."
- **Notes:** Good follow-on after "Questions" topic.

---

## Priority 3 — Park For Later

### "How to structure multi-agent systems without losing control"
- **Stream:** Enterprise (AI safety) + Teaching (advanced)
- **Source:** V's consulting experience
- **Notes:** Too advanced for Video 1-3. Save for Video 7-9.

### "AI incidents: what breaks and how to recover"
- **Stream:** Enterprise (risk)
- **Source:** V's consulting + industry incidents
- **Notes:** Strong enterprise topic. Need case studies. Research-heavy.

### "The human-in-the-loop problem: where to draw the line"
- **Stream:** Enterprise (governance)
- **Source:** ICM framework
- **Notes:** Good for board talks. Compliance angle strong.

---

## Backlog Template (Add New Topic)

```markdown
### "[Topic title]"
- **Stream:** Teaching / Enterprise / Both
- **Source:** [Where idea came from]
- **Hook:** [Opening line or frame]
- **Teaching angle:** [What learner gains]
- **Enterprise angle:** [What exec cares about]
- **Soundbite ready:** YES / NO
- **Objection to address:** [If applicable]
- **Notes:** [Priority, dependencies, readiness]
```
