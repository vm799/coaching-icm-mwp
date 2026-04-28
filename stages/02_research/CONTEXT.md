# Stage 02: Research (Layer 2)

## What This Stage Does
Enrichment phase. Takes discovery brief → pulls data, interviews, sources → produces research output.

Output is raw research: quotes, stats, examples, analogies. Not yet scripted. Ready to be shaped into teaching OR enterprise voice.

## Inputs (From Stage 01)
```
discovery_brief.md         (topic summary, research scope, learning angles)
sources_list: URLs/refs    (papers, docs, expert contacts)
scope_hours: number        (research budget)
stream: "teaching" | "enterprise" | "both"
```

## Process
1. **Fetch sources**
   - Pull cited papers, blog posts, docs
   - Extract quotes + data + key findings
   - Note source credibility + recency

2. **Expert commentary** (if needed)
   - Extract quotes from interviews (or use cached expert commentary from ref/)
   - Extract key insights (why does this expert matter for this topic?)
   - Use as anecdotes, validation, or counterpoint

3. **Build teaching-angle research**
   - Find analogies (compare concept to familiar thing)
   - Find simple examples (code snippet, diagram, workflow)
   - Find progressive layers (explain basics before complexity)
   - Extract data that educates (benchmarks, comparisons, trends)

4. **Build enterprise-angle research**
   - Find risk angles (what breaks if we ignore this?)
   - Find business impact (revenue, cost, competitive advantage, talent, compliance)
   - Find implementation stories (who did this successfully? What went wrong?)
   - Find catchy stats (headline-worthy numbers)

## Outputs (To Stage 03)
```markdown
# [Topic] — Research Output

## Executive Summary
[one-para distill of research: key insight, business implication, confidence level]

## Data & Facts
### Sources
- [Ref Title]: [key finding] — [URL/page#]
- [Expert Name]: [quote, context] — [date/role]
- [Internal data]: [metric, relevance] — [source]

### Key Stats
- Stat 1: [number], [why it matters]
- Stat 2: [number], [why it matters]

## Analogies & Examples

### Teaching Analogies
- "X is like Y because..." [explain mapping]
- [Code example / diagram description]

### Enterprise Analogies
- "X is like Y for executives..." [risk/business framing]
- [Case study: who did it, result, lesson]

## Common Questions & Answers
- Q: "Why does this matter?"
  A: [teaching answer], [enterprise answer]
- Q: "How do we implement?"
  A: [teaching perspective], [enterprise perspective]

## Quotes (Full)
[Pull full quotes, attributed, with context]

## Confidence & Gaps
- Confidence: [High/Medium/Low]
- Known gaps: [what research is missing, why]
- Expert review needed: [Yes/No — who?]

## Visual Specs (Optional)
- Animation needed: [Yes/No — what scene?]
- Code demo: [Yes/No — which language, which system?]
- Slide illustrations: [Yes/No — what diagrams?]
```

## Success Criteria
✓ 5+ sources cited (academic, expert, real-world examples)
✓ 3+ analogies mapped (teaching + enterprise each)
✓ Data backs every major claim (cite source)
✓ Gaps documented (what we don't know, why it matters)
✓ Ready to hand off: script writer can read output + write dual scripts without additional research

## Produced Files
- `research_output.md` → Stage 03 input
- (optional) `research_notes.md` → Raw notes, raw quotes before packaging

## Next Stage Trigger
When human reviews research for accuracy + completeness, move to Stage 03 (Script).
