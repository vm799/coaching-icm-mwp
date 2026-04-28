# Stage 00: Capture (Layer 2)

## What This Stage Does
Raw intake. Dump anything here. No structure required at capture time.

Agent reads raw content → extracts signal → routes to:
- Existing topic in output/ (enriches research or script)
- New topic candidate (flags for Stage 01 discovery)
- Catchphrases library (_config/catchphrases.md)
- Reference knowledge (_config/icm-mwp-framework.md)

**One rule:** Capture now. Route later. Never let "where does this go?" stop you from capturing.

## Inputs (Anything)
```
Source types accepted:
- Voice memo transcript (spoken, rough, unedited)
- Instagram / TikTok / YouTube video summary
- Email draft or idea
- Paper extract or quote
- Speaker notes from event
- Q&A moment you want to remember
- Analogy or metaphor that struck you
- Someone else's content you want to respond to
- Random thought at 2am

Format: any. Markdown, plain text, paste, bullet list, stream of consciousness.
```

## Process
1. **Extract signal** — what's the core idea? (even if buried in noise)
2. **Tag** — what topic, stream, format does this serve?
3. **Route** — where does it go?

### Routing Rules

| Signal Type | Route To |
|-------------|----------|
| Quote / soundbite | `_config/catchphrases.md` |
| Framework concept (ICM/MWP) | `_config/icm-mwp-framework.md` |
| Research data / stat / source | `output/[topic]/research_output.md` (append) |
| New topic idea | `stages/00_capture/topics_backlog.md` |
| Teaching analogy | `stages/00_capture/analogies_bank.md` |
| Enterprise angle / business story | `stages/00_capture/enterprise_angles.md` |
| Personal story / speaker moment | `stages/00_capture/speaker_notes.md` |
| Counter-argument (defend ICM/MWP) | `stages/00_capture/objections_bank.md` |
| Demo / code idea | `stages/00_capture/demo_ideas.md` |

## Output Files (Living Documents — Always Append, Never Overwrite)

```
stages/00_capture/
├─ inbox/                       ← Raw dumps (timestamped, any format)
│  ├─ YYYY-MM-DD_[source].md    ← One file per capture session
│  └─ ...
├─ topics_backlog.md            ← Topic ideas not yet in Stage 01
├─ analogies_bank.md            ← Teaching analogies + metaphors
├─ enterprise_angles.md         ← Business angles, ROI stories, exec framings
├─ speaker_notes.md             ← Talk ideas, Q&A prep, event moments
├─ objections_bank.md           ← Common objections + your rebuttals
├─ quotes_raw.md                ← Raw quotes (not yet vetted for catchphrases.md)
├─ demo_ideas.md                ← Code/demo ideas for Stage 04
└─ processed/                   ← Items fully routed (archive, don't delete)
```

## How Stage 00 Feeds Other Stages

- **Stage 01 Discovery:** Pulls from `topics_backlog.md` to seed next topic
- **Stage 02 Research:** Pulls from `analogies_bank.md`, `enterprise_angles.md`, `quotes_raw.md`
- **Stage 03 Script:** Pulls from `speaker_notes.md`, `objections_bank.md`
- **Stage 04 Multiply:** Pulls catchphrases from `_config/catchphrases.md` (fed by quotes_raw.md)
- **Any stage:** Can reference `objections_bank.md` for anticipated Q&A

## Capture Format (Fast, No Friction)

Minimum viable capture:
```markdown
## [Source + Date]
[Paste or dump here — no editing required]
```

Full capture (if you have 2 extra minutes):
```markdown
## [Source + Date]
**Source:** [Instagram / YouTube / Email / Paper / Own thought]
**Topic hint:** [Which teaching or enterprise topic might this relate to?]
**Signal:** [What's the core idea in 1 sentence?]
**Raw content:**
[Paste here]
**Route to:** [Which output file above?]
```

## Success Criteria
✓ Zero friction to capture (anything goes in)
✓ Every capture is routed (within 24h or next session)
✓ Routed items are findable when Stage 01/02/03 needs them
✓ Nothing lost — no idea, quote, or story that could enrich content

## How to Use (Session Start)
If you have captures since last session:
1. Open `inbox/` — find unprocessed files
2. Agent reads each → extracts signal → routes to correct living document
3. Mark processed (move to `processed/` folder)
4. Now Stage 01/02/03 have richer material to pull from
