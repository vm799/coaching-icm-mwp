# Topic Intake Questionnaire

Fill this out before starting Stage 01 (Discovery) for a new topic.

Save completed questionnaire to `output/[topic-slug]/setup_questionnaire.md` for reference.

---

## Project Metadata

**Topic Title:**
[e.g., "Token Efficiency and Why It Matters"]

**Topic Slug:** (used in filenames, no spaces)
[e.g., "token-efficiency"]

**Date Started:**
[YYYY-MM-DD]

**Owner/Creator:**
[Your name]

---

## Topic Definition

### What Is This Topic?
[One paragraph: What is the core concept? What is the simplest definition?]

Example:
> Token efficiency means knowing which information matters for a decision, loading only that information, and ignoring the rest. It's the difference between "explain everything" and "explain what matters."

### Why This Topic Now?
[Why does this matter right now? Any trends, events, or business drivers?]

Examples:
- "AI costs are rising. Execs want to understand why tokens matter to budgeting."
- "We're scaling team. Need to teach new engineers how we route context."
- "Competitor announced similar feature. We need thought leadership angle."

### Who Needs to Know This?
[Target audience(s) — be specific]

Teaching stream examples:
- BAs (business analysts, non-technical, want to understand decision flows)
- Managers (lead technical teams, want to explain constraints to direct reports)
- Engineers (building AI systems, want to know why we design this way)

Enterprise stream examples:
- C-suite (CEO, CFO, COO — care about cost, risk, competitive edge)
- Board (long-term strategy, risk governance, market position)
- Product leaders (how does this feature work? How do we sell it?)
- Engineering leaders (what's the implementation cost? Team size?)

---

## Stream Selection

### Which Stream(s)?
Pick one or both.

- [ ] **Teaching stream** (zero-to-hero, learn from basics)
- [ ] **Enterprise stream** (safety-first leadership, decision-making)

---

## Teaching Stream Details (If Selected)

### Learning Outcomes
[What should learner understand by the end? List 3-5 outcomes, one per line]

Examples:
- Learner can explain what tokens are and why they have a cost
- Learner can identify when context might be "too much"
- Learner can apply selective context to their own code decisions
- Learner can justify to non-technical peers why we cut unnecessary details

### Prior Knowledge Assumed?
[What can we assume learner already knows?]

Options:
- None (start from absolute basics)
- Basic understanding of [specific topic]
- Advanced knowledge of [specific topic]

Example:
> Assume learner understands: "What is a language model (LLM)?" at high level. Do NOT assume they understand tokens, embeddings, or transformers.

### Analogy Angle
[What familiar concept maps to this topic? What's the teaching metaphor?]

Examples:
- "Tokens are like pages in a book. A long book takes longer to read than a short one."
- "Context is like a library. Give the LLM just the books it needs, not the whole collection."
- "Selective attention is like a student focusing on the chapter they need for the test, not the whole textbook."

### Complexity Progression
[How do we layer the complexity? Simple → medium → advanced]

Example:
- **Simple:** What is a token? How much do they cost?
- **Medium:** Why do we filter context? How do we decide what to load?
- **Advanced:** How do we measure good context? Real-world tradeoffs.

### Demo / Code Example Needed?
- [ ] Yes — what should it show? [e.g., "Python code that shows token counting"]
- [ ] No — teaching with analogies + diagrams only

---

## Enterprise Stream Details (If Selected)

### Business Problem
[What business problem does this solve? What costs it? What risks it?]

Examples:
- "API costs are rising 2% month-over-month as we scale. Token efficiency can reduce costs by 30-40%."
- "Regulatory risk: we need to prove AI decisions are explainable. Context selection helps."
- "Competitive: if we can deploy AI 2x faster than competitors, that's market advantage."

### Key Business Impact
[Quantify the impact. What metric changes?]

Options:
- Cost savings: $X/month or Y% reduction
- Speed: Z% faster deployment
- Risk reduction: reduces X risk by Y%
- Revenue: enables new product/feature
- Talent: helps recruit/retain AI engineers

Example:
> "If we reduce tokens used by 40%, and we process 1M requests/month at $0.0001/token, we save $4K/month in API costs. Over 12 months, that's $48K for a single product."

### Audience Variant
[Who is the exec? What angle matters most to THEM?]

Examples:
- **CFO:** Cost savings, ROI timeline, implementation cost
- **CEO:** Competitive advantage, market timing, strategic positioning
- **CTO:** Implementation complexity, team hiring, technical feasibility
- **Board:** Long-term risk, regulatory alignment, market opportunity

Pick primary audience. Script will tailor for them.

### Soundbite / Catchy Angle
[What's the memorable phrase for this topic? Something an exec will repeat.]

Examples:
- "Tokens are attention. Attention is expensive. This is how we spend them wisely."
- "Safe AI isn't slower AI. It's AI with clarity."
- "The cost of a bad decision grows with scale. Get the decision structure right before you scale."

[You'll refine this during Stage 03 scripting. Just brainstorm here.]

### Risk or Opportunity Frame?
[Is this about preventing risk or capturing opportunity?]

- [ ] **Risk frame:** "Here's what breaks if we ignore this. Here's how we avoid it."
- [ ] **Opportunity frame:** "Here's how we win if we do this right. Here's the competitive edge."

Example risk: "If we don't control context, costs spiral. How we prevent it: selective context."
Example opportunity: "If we master context, we deploy 2x faster. Competitor advantage: speed to market."

### Implementation Roadmap (Optional)
[If presenting this to execs, what's the implied roadmap?]

Example:
> "Month 1: Pilot selective context with one team (cost: $50K in engineering time).
> Month 2-3: Measure impact on API costs and deployment speed.
> Month 4+: Roll out to all teams (cost savings: $48K/month)."

---

## Research Scope

### Estimated Research Hours
[How much research do we need? Conservative estimate.]

Options:
- **Light (2-4 hours):** Topic is familiar. 2-3 sources. Quick examples.
- **Medium (4-8 hours):** Some gaps. Need expert quotes. Real case studies.
- **Heavy (8-16 hours):** New domain. Need original research. Multiple sources. Interviews.

### Sources You Know Of
[What sources should we pull? Be specific. URLs preferred.]

Examples:
- Paper: "Attention Is All You Need" (arXiv:1706.03762)
- Blog: "How to Reduce LLM Costs" by [Company]
- Internal: [Your internal docs, case studies, metrics]
- Expert: "[Name, role]" — interview this person?
- Competitor: [Competitor's blog/talk on this topic]

### Data or Stats You Want
[What metrics or benchmarks matter? Where are they?]

Examples:
- Cost benchmarks: "Average token cost per request, by provider"
- Performance: "Speed improvement from selective context"
- Industry: "% of AI teams struggling with costs"

### Expert Interviews Needed?
[Do we need quotes from experts? Who?]

- [ ] Yes — who?
  - [ ] Internal [role/name]
  - [ ] External [company/person]
  - [ ] Industry expert [type]
- [ ] No — use existing quotes / research

### Visual / Demo Assets
[Do we need visual assets? Where can we source them?]

- [ ] Diagrams (flowcharts, architecture, process)
  - [ ] Design ourselves (describe what's needed)
  - [ ] Find existing (where? link?)
- [ ] Code examples (if teaching)
  - [ ] Write new (what should it show?)
  - [ ] Use existing (what? link?)
- [ ] Screenshots (system, UI, dashboard)
  - [ ] Record ourselves (what system?)
  - [ ] Find existing (where?)
- [ ] Animation needs (if enterprise or visual storytelling)
  - [ ] Describe what (e.g., "process flow animation")
  - [ ] Budget for (time/cost)

---

## Delivery Constraints

### Timeline
[When do you want this done?]

- Rough estimate: Stage 01 (1 day) → Stage 02 (1-3 days) → Stage 03 (1-2 days) → Stage 04 (1-2 days) = 4-9 days
- Hard deadline? [Date]

### Format Priorities
[What's most important? Rank the 6 Stage 04 outputs.]

Outputs: Spoken (video), Deck (slides), Blog, LinkedIn, Animation, YouTube metadata

Ranking (1 = most important, 6 = least important):
- Spoken video: ___
- Deck: ___
- Blog: ___
- LinkedIn: ___
- Animation: ___
- YouTube metadata: ___

Example: You care most about "Spoken video", then "YouTube metadata", then "Deck". Blog and LinkedIn are lower priority. Animation is nice-to-have.

### Recording / Production Constraints
[Any constraints on delivery?]

- Who records the spoken version? [You / Professional talent / TBD]
- Who designs the deck? [You / Designer / TBD]
- Animation budget? [Yes/No/TBD — if yes, how much?]
- Blog platform? [Medium / Substack / Company blog / TBD]
- YouTube channel? [Which channel?]

---

## Success Criteria

How will you know this topic is successful?

- [ ] Script is ready to record (clear, no stumbling, tailor notes work)
- [ ] Research is credible (sources cited, data sound)
- [ ] Dual streams are distinct (teaching ≠ enterprise, not merged)
- [ ] All 6 Stage 04 formats are production-ready
- [ ] Learner/exec can act on it (learning outcomes met / action items clear)
- [ ] Can be repeated (same process for next topic, no special handling)

---

## Notes / Additional Context

[Anything else we should know about this topic?]

Examples:
- "This is part of a 10-part series. Assumes learner watched Part 1."
- "Exec is concerned about X risk. Make sure we address that."
- "Competitor just published on this. Let's differentiate by emphasizing Y angle."
- "Internal team is building X feature. This content will help sell it internally."

---

## Sign-Off

**Completed by:** [Your name]
**Date:** [YYYY-MM-DD]
**Ready for Stage 01?** 
- [ ] Yes, start discovery
- [ ] No, needs more clarity (see notes above)

---

## How This Feeds Into Stage 01

Agent uses this questionnaire + your inputs to produce `discovery_brief.md`:
- Topic summary (from "What Is This Topic?" + "Why This Topic Now?")
- Learning/business outcomes (from Teaching/Enterprise Details)
- Research brief (from "Research Scope")
- Tailor notes (from "Stream Selection" + "Implementation Roadmap")

Don't overthink it. Your best guesses are enough. Agent will clarify during discovery.
