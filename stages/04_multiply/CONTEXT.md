# Stage 04: Multiply (Layer 2)

## What This Stage Does
Production phase. Takes approved scripts → multiplies into all formats: spoken (video), deck, blog, LinkedIn+video, animation spec, YouTube package.

One script → many deliverables. Agent is format translator, not content generator.

## Inputs (From Stage 03)
```
teaching_script.md         (or enterprise_script.md, or both)
research_output.md         (for citations, stats, links)
discovery_brief.md         (learning outcomes, catchy angles)
production_specs.md        (visual needs, demo details, animation scenes)
```

## Process

### Tier 1 — Always Produce

1. **Create Spoken Delivery Assets**
   - Extract speaker notes (pacing, emphasis, pauses)
   - Output: `spoken_notes.md`
   - Include: [PAUSE: X sec], [EMPHASIS: X], [LOOKCAM: X]

2. **Create Deck (Slide Presentation)**
   - Parse [SLIDE:...] markers from script
   - 8-12 slides for 30 min
   - Output: `deck_outline.md`
   - Template: `references/deck_template.md`

3. **Create Blog Post**
   - Script → prose (not copy-paste, rewrite for reading)
   - Add citations, section headers, CTA
   - Output: `blog_post.md`
   - Template: `references/blog_template.md`

4. **Create LinkedIn Post + Video Clip**
   - Extract 1-3 soundbites from script
   - Short post (100-300 chars) + clip timestamp
   - Output: `linkedin_post.md`

5. **Create YouTube Package**
   - Title, description, timestamps, tags, thumbnail spec
   - Output: `youtube_package.md`
   - Template: `references/youtube_template.md`

6. **Create Email (Newsletter)**
   - Script → 300-500 word newsletter
   - Output: `email_newsletter.md`
   - Template: `references/email_template.md`

### Tier 2 — Full Run

7. **Create Twitter/X Thread**
   - Extract soundbites + data points + analogy → 6-10 tweets
   - Output: `twitter_thread.md`
   - Template: `references/twitter_thread_template.md`

8. **Create LinkedIn Article (Enterprise)**
   - Enterprise script → 800-1500 word thought leadership article
   - Output: `linkedin_article.md`
   - Template: `references/linkedin_article_template.md`

9. **Create Executive Email**
   - Enterprise script → 200-350 word executive summary
   - Output: `email_executive.md`
   - Template: `references/email_template.md` (Type B)

10. **Create Shorts Spec (YouTube / Reels / TikTok)**
    - Identify 3-5 best 60-sec moments from full video
    - Output: `shorts_spec.md`
    - Template: `references/shorts_template.md`

11. **Create Stage Talk Package**
    - Script → stage-ready talk (deck for projection, speaker notes, Q&A prep)
    - Output: `stage_talk_notes.md`
    - Template: `references/stage_talk_template.md`

12. **Create Live Session Notes**
    - Script → webinar/121/workshop version (shorter, more Q&A)
    - Output: `live_session_notes.md`
    - Template: `references/live_session_template.md`

### Tier 3 — Premium (Resource/Budget Required)

13. **Create Animation Spec**
    - Parse [ANIMATION: scene description] from script
    - Scene-by-scene with timing, motion, narration sync
    - Output: `animation_spec.md`
    - Template: `references/animation_template.md`

14. **Create Interactive Demo Package**
    - Script code examples → runnable demo with problem/solution/compare
    - Output: `demo/` (code repo) + `demo_spec.md`
    - Template: `references/demo_template.md`

15. **Create Podcast Spec**
    - Notes for audio extraction from video recording
    - Output: `podcast_spec.md`

16. **Create Quote Graphics Brief**
    - Extract 3-5 soundbites from enterprise script → Canva brief
    - Output: `quote_graphics_brief.md`

## Outputs (To output/ folder)
```
output/[topic-slug]/
├─ README.md                    [Index of all deliverables + publish status]
├─ spoken_notes.md              [Recording talent]
├─ deck_outline.md              [Deck designer + stage presenter]
├─ blog_post.md                 [Blog publishing]
├─ linkedin_post.md             [Video post + clip spec]
├─ linkedin_article.md          [Enterprise thought leadership]
├─ youtube_package.md           [Video upload: title/desc/timestamps/tags]
├─ shorts_spec.md               [3-5 clips: hook/body/CTA/edit notes]
├─ email_newsletter.md          [Teaching audience email]
├─ email_executive.md           [Enterprise decision-maker email]
├─ twitter_thread.md            [6-10 tweet thread]
├─ stage_talk_notes.md          [Conference / all-hands / board talk]
├─ live_session_notes.md        [Webinar / 121 / workshop]
├─ animation_spec.md            [Animator/designer — scene-by-scene]
├─ demo_spec.md                 [Interactive demo spec]
├─ podcast_spec.md              [Audio extraction notes]
├─ quote_graphics_brief.md      [Soundbite graphics for social]
└─ source/
   ├─ teaching_script.md
   ├─ enterprise_script.md
   ├─ research_output.md
   └─ discovery_brief.md
```

## Success Criteria
✓ Tier 1 always complete: spoken, deck, blog, linkedin_post, youtube, email
✓ Every [SLIDE:...] → one slide in deck_outline
✓ Every [DEMO:...] → identified in deck + blog + demo_spec
✓ Every [PAUSE:...] → preserved in spoken_notes
✓ Every [SOUNDBITE:...] → in linkedin_post + linkedin_article + twitter_thread + quote_graphics
✓ Script → blog post prose conversion (not copy-paste, fully rewritten for reading)
✓ LinkedIn post: <300 chars hook + CTA
✓ LinkedIn article: 800-1500 words, data + soundbite + one CTA
✓ YouTube: title/description/timestamps/tags/thumbnail spec
✓ Shorts: 3-5 clips, each with hook/body/CTA/caption/edit notes
✓ Stage talk: deck formatted for projection (6 words/slide max), Q&A prep included
✓ All deliverables traceable to research (citations in blog + linkedin_article)
✓ README.md index created (publish checklist for all formats)

## Produced Files
- `spoken_notes.md` → recording artist
- `deck_outline.md` → designer/presenter
- `blog_post.md` → blog publishing
- `linkedin_post.md` → social media
- `animation_spec.md` → animator
- `youtube_package.md` → video uploader
- `README.md` → deliverables index
- `output/[topic-slug]/` folder structure → final delivery package

## Templates Used (Full Reference Library)

### Always Load (Tier 1)
- `references/deck_template.md` — slide structure
- `references/blog_template.md` — article conversion
- `references/youtube_template.md` — SEO + packaging
- `references/email_template.md` — newsletter + executive summary

### Full Run (Tier 2)
- `references/twitter_thread_template.md` — thread structure
- `references/linkedin_article_template.md` — thought leadership
- `references/shorts_template.md` — 60-sec clips
- `references/stage_talk_template.md` — live speaking
- `references/live_session_template.md` — webinar / 121 / workshop

### Premium (Tier 3)
- `references/animation_template.md` — visual storytelling, scene-by-scene
- `references/demo_template.md` — interactive demo, show-and-tell
- `references/distribution_matrix.md` — channel map, scheduling calendar

### Publishing Guide
- `references/publishing_checklist.md` — full run checklist, day-by-day calendar

## Final Stage: Delivery
Human reviews all deliverables:
- [ ] Spoken notes are clear (no ambiguity for talent)
- [ ] Deck is visually scannable (short text, clear structure)
- [ ] Blog is prose, not copied text (reads naturally)
- [ ] LinkedIn post has hook + CTA (shareable)
- [ ] Animation spec matches script pacing
- [ ] YouTube package is SEO-optimized

Once approved → ready for recording/publication.
