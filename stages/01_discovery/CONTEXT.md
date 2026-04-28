# Stage 01: Discovery (Layer 2)

## What This Stage Does
Intake phase. Takes raw topic + stream choice → produces focused research brief.

Does NOT research yet. Maps scope, identifies who needs to know, flags why-now urgency.

## Inputs (From User)
```
topic: string              (e.g., "Progressive disclosure in ICM")
stream: "teaching" | "enterprise" | "both"
scope_hours: number        (estimated research effort)
background_context: string (optional — why this topic, any constraints)
sources_available: string  (optional — known references, internal data)
```

## Process
1. **Clarify the topic**
   - What is it? (definition + scope)
   - Who needs this? (persona + role + pain point)
   - Why now? (urgency, trend, business driver)

2. **Map research scope**
   - Data sources needed (external, internal, expert commentary)
   - Expert interviews required? Which roles?
   - Analogies/examples to research (case studies, demos)

3. **Identify delivery constraints**
   - Teaching stream: what prior knowledge assumed? (ICM basics? None?)
   - Enterprise stream: executive framing? Security angle? Risk narrative?
   - Visual/demo needs: Animation? Code examples? Slides?

## Outputs (To Stage 02)
```markdown
# [Topic] — Discovery Brief

## Topic Summary
[one-paragraph: what, who, why-now]

## Research Brief
- [ ] Sources to pull (with URLs/references)
- [ ] Expert interviews needed (roles, questions)
- [ ] Data/stats to find (what metric, why relevant)
- [ ] Examples/case studies (what to research)

## Teaching Stream Notes
- Prior knowledge assumed: [e.g., "ICM Layers basics", "None — start from scratch"]
- Learning outcomes: [3-5 things learner should understand]
- Analogy angle: [e.g., "Compare to X; metaphor is Y"]

## Enterprise Stream Notes
- Executive frame: [e.g., "Risk + competitive advantage", "AI governance + safety"]
- Catchy angle: [soundbite/framing that sells it]
- Decision maker pain: [e.g., "How do we scale AI safely?"]
- Business hook: [revenue, risk reduction, compliance, talent]

## Scope & Deliverables
- Research effort: [hours estimated]
- Script length: 30 min (~6000 words)
- Additional assets: [animation? code? deck only?]
- Deadline: [user input]
```

## Success Criteria
✓ Topic is clear and scoped (not "AI basics" but "Token efficiency in recursive ICM patterns")
✓ Research brief lists 5+ concrete sources/experts/examples
✓ Dual-stream angles documented (what makes each stream different?)
✓ Human can review brief in <10 min and greenlight research phase

## Produced Files
- `discovery_brief.md` → Stage 02 input
- (optional) `discovery_notes.md` → Scratchpad for agent reasoning

## Next Stage Trigger
When brief is greenlit by human review, move to Stage 02 (Research).
