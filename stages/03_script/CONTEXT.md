# Stage 03: Script (Layer 2)

## What This Stage Does
Script phase. Takes research → writes two tailor-ready scripts: one teaching-tuned, one enterprise-tuned.

Scripts are ready to READ (for recording), PRESENT (from slides), UNDERSTAND (standalone clarity), and TAILOR (audience-specific notes provided).

NOT a polished screenplay — a working script. Actor can read it and own it.

## Inputs (From Stage 02)
```
research_output.md         (data, quotes, analogies, examples)
discovery_brief.md         (learning outcomes, enterprise angles)
stream: "teaching" | "enterprise" | "both"
teaching_voice.md          (config: tone, audience, pacing)
enterprise_voice.md        (config: tone, risk frame, soundbite style)
```

## Process
1. **Teaching Script** (If stream includes teaching)
   - Open with relatable problem or analogy
   - Progress: simple → complex (layer by layer)
   - Use analogies from research (compare to familiar)
   - Include 2-3 worked examples (code, workflow, diagram call-outs)
   - Close: recap + "what you now know" (learning outcome check)
   - Target: 30 min (~6,000 words, ~150-180 wpm delivery)
   - Tone: curious, learning-focused, non-judgmental

2. **Enterprise Script** (If stream includes enterprise)
   - Open with business problem (risk, opportunity, competitive edge)
   - Frame around executive decision: "Should we do this? How? What's the risk?"
   - Use data + ROI impact from research
   - Include 2-3 real-world implementation stories (who did it, result, lesson)
   - Include 1-2 catchy soundbites (quotable, memorable)
   - Close: "3 things you should do Monday" (action items)
   - Target: 30 min (~6,000 words)
   - Tone: confident, decisive, risk-aware

3. **Markup for Multiplication**
   - [SLIDE: X] → signals where deck needs a visual
   - [PAUSE: X sec] → timing for pacing
   - [NOTE: audience-specific] → tailoring hints for Stage 04
   - [OPTIONAL: can cut if time] → for adaptation to shorter formats

## Outputs (To Stage 04)
```markdown
# [Topic] — Scripts

## Teaching Stream Script
[Full script, ready to read/present/tailor]
[6000 words, 30 min delivery]
[Markup: [SLIDE:...], [PAUSE:...], [NOTE:...]]

### Learning Outcomes
- Student can explain [outcome 1]
- Student can identify [outcome 2]
- Student can apply [outcome 3]

### Tailor Notes
- For [audience X]: emphasize [angle]
- Cut optional sections if time limited
- Demo can be [live coding / recorded / slides]

---

## Enterprise Stream Script
[Full script, ready to read/present/tailor]
[6000 words, 30 min delivery]
[Markup: [SLIDE:...], [PAUSE:...], [NOTE:...]]

### Executive Takeaway (one-liner)
[What does the exec walk away believing/doing?]

### Soundbites (for social/PR)
- "..." — [context: when to use]
- "..." — [context: when to use]

### Tailor Notes
- For C-suite: emphasize [angle]
- For board: include [risk/compliance framing]
- For all-hands: cut internal acronyms, define jargon

---

## Production Specs
### Both Scripts
- Duration: 30 min (verified by reading aloud at 150-180 wpm)
- Vocabulary: [teaching: accessible, enterprise: precise]
- Examples: [list of demos/code/visuals needed]
- Deck slides needed: [count + topics]

### Visual Call-outs
- [SLIDE: X] appears at [location in script]
- [DEMO: code] appears at [location in script]
- [ANIMATION: X scene] appears at [location in script]
```

## Success Criteria
✓ Both scripts (or single script if stream="both") are 30 min each (~6,000 words)
✓ Teaching script uses analogies, builds from simple→complex, checks learning outcomes
✓ Enterprise script includes risk/ROI, real stories, 2+ soundbites
✓ Scripts are ready to READ (grammatically complete, stage directions clear)
✓ Scripts are ready to TAILOR (notes document audience-specific adaptations)
✓ All [SLIDE:...], [DEMO:...], [PAUSE:...] markup clear
✓ Human can read script in 15 min and greenlight for Stage 04 multiplication

## Produced Files
- `teaching_script.md` → Stage 04 input (if stream="teaching" or "both")
- `enterprise_script.md` → Stage 04 input (if stream="enterprise" or "both")
- (optional) `script_notes.md` → Scratchpad, reasoning

## Templates Used
- See `references/script_template.md` (structure)
- See `_config/teaching-voice.md` (teaching tone guide)
- See `_config/enterprise-voice.md` (enterprise tone guide)
- See `_config/catchphrases.md` (soundbites library)

## Next Stage Trigger
When human reviews scripts for completeness + readability + soundness, greenlight Stage 04 (Multiply).
