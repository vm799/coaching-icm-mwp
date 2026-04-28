# Script Template — Dual-Stream Ready

Use this template for Stage 03 (Script) output. Produces teaching-tuned and enterprise-tuned scripts.

---

# [Topic Title] — Scripts

## Teaching Stream Script

[OPEN: Hook (30 sec)]
Start with a problem the learner recognizes, or a surprising fact that makes them want to understand why.

"Have you ever [relatable problem]? That's because..."

[BODY: Layer 1 — What (2 min)]
Simplest explanation. One analogy, one concrete example.

"X is like Y because..."

[SLIDE: Simple diagram or concept visual]

[PAUSE: 15 sec — give learner time to absorb]

[BODY: Layer 2 — Why (2-3 min)]
Why do we care? Where does this show up in your work?

Include one worked example. If teaching code, show 3-5 lines.

[DEMO: Show what this looks like in practice]

[PAUSE: 10 sec]

[BODY: Layer 3 — How (3-4 min)]
How to actually use this. Second worked example, slightly more complex.

Where will you encounter this?

[DEMO: More detailed example or walkthrough]

[OPTIONAL: Can cut if time short — advanced variant or edge case]

[PAUSE: 15 sec]

[CLOSE: Recap + Learning Outcome (30 sec)]
"Now you understand X. Here's what you'll notice next time you [see this in your work]."

"Next time, we'll explore [teaser for next video]."

---

### Teaching Script Metadata
- **Duration:** 30 min (~6,000 words, 150-180 wpm delivery)
- **Learning Outcomes:**
  1. Learner can explain [outcome 1] in own words
  2. Learner can identify [outcome 2] in real code/system
  3. Learner can apply [outcome 3] to their own project

- **Tailor Notes:**
  - For [audience A]: emphasize [angle]
  - For [audience B]: emphasize [different angle]
  - [OPTIONAL: X] sections can be cut if time limited
  - [DEMO: Y] can be live coding or pre-recorded video

---

## Enterprise Stream Script

[OPEN: Hook (30 sec)]
Start with business problem or opportunity.

"Your [problem that costs money/creates risk]. Your competitors [what they're doing]. Here's the gap."

[PROBLEM: Business Context (1-2 min)]
What's at stake?

Numbers first: "This costs $X/year" or "This creates Y% risk"

[SLIDE: Cost/risk visualization]

[PAUSE: 10 sec]

[SOLUTION: Why This Matters (2-3 min)]
Data + ROI. What's the upside if we do this right?

Include case study: "Company X implemented this. Result: [metric]."

[SOUNDBITE: "Memorable phrase about solution/impact"]

[PAUSE: 10 sec]

[IMPLEMENTATION: How It Works (2-3 min)]
What does this look like in practice? What changes?

Include: "Time to implement: X weeks. Cost: $Y. Team size: Z people."

Address objection: "You might worry [concern]. Here's why [concern is manageable or worth the tradeoff]."

[OPTIONAL: For product leaders / For engineering leaders — different angle]

[CLOSE: Action Items + Future (30 sec)]
"Three things to do Monday:
1. [Action 1]
2. [Action 2]
3. [Action 3]"

"Six months from now, this unlocks [future capability/risk reduction]."

---

### Enterprise Script Metadata
- **Duration:** 30 min (~6,000 words)
- **Executive Takeaway (one-liner):** [What does exec walk away believing?]
- **Business Impact:** [Quantified: cost savings, risk reduction, revenue, velocity]
- **Confidence Level:** [Proven / Validated / Promising]

- **Soundbites (for social/marketing):**
  1. "[First catchphrase]" — Context: [when to use]
  2. "[Second catchphrase]" — Context: [when to use]

- **Tailor Notes:**
  - For C-suite: emphasize [ROI / risk]
  - For board: include [compliance / long-term strategy]
  - For product: emphasize [customer impact / velocity]
  - For engineering: include [tooling / hiring needs]

---

## Production Markup (Both Scripts)

Use these markers so Stage 04 (Multiply) knows what to do:

```
[SLIDE: description of visual needed]
  ↳ Stage 04 → creates deck slide
  ↳ Stage 04 → marks location in blog post

[DEMO: description of code/system example]
  ↳ Stage 04 → notes where demo is in timeline
  ↳ Stage 04 → includes in animation spec

[PAUSE: Xsec]
  ↳ Stage 04 → spoken notes include pause timing

[OPTIONAL: description of section]
  ↳ Stage 04 → marks as cuttable (for shorter versions)

[SOUNDBITE: "exact phrase"]
  ↳ Stage 04 → extracts for LinkedIn, Twitter, marketing

[NOTE: audience-specific instruction]
  ↳ Stage 04 → creates variant version if needed

[ANIMATION: scene description]
  ↳ Stage 04 → detailed scene-by-scene animation spec
```

---

## Quality Checklist (Before Sending to Stage 04)

- [ ] Script reads aloud at natural pace (150-180 wpm)
- [ ] Every [SLIDE: ...] marker is specific (not vague: "concept diagram" → "comparison table: Context vs. Token vs. Attention")
- [ ] Every [DEMO: ...] has context (what code, what system, what outcome?)
- [ ] Every claim backed by research (cite source in Stage 04 output, not needed here)
- [ ] Teaching script: learning outcomes are checkable
- [ ] Enterprise script: 2-3 soundbites included, [SOUNDBITE: ...] clearly marked
- [ ] No jargon without definition (or note that audience knows term)
- [ ] Tone consistent (read through — does voice shift?)
- [ ] Pacing: roughly [PAUSE: ...] every 2-3 min

---

## Tips for Script Writers

**Make it speakable:**
- Read aloud. If you stumble, edit it.
- Short sentences (15-25 words) for complex ideas
- Contractions OK ("we're" not "we are")
- Avoid: double-nested clauses, lists over 3 items

**Make it visual:**
- [SLIDE: ...] roughly every 3-4 minutes (gives presenter something to point to)
- [DEMO: ...] in middle section (hold attention)
- Describe visuals in words (animator reads script, creates slides from description)

**Make it memorable:**
- Teaching: analogies + examples (stick in brain)
- Enterprise: data + soundbites (repeatable, shareable)

**Make it tactical:**
- Scripts aren't essays. Skim-able even if read aloud.
- Bullet points OK in [SLIDE: ...] call-outs
- Short paragraphs
