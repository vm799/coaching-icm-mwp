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
1. **Create Spoken Delivery Assets**
   - Extract speaker notes (pacing, emphasis, pauses)
   - Output as: `spoken_notes.md` (for recording talent)
   - Include: [PAUSE: X sec], [EMPHASIS: X], [LOOKCAM: X]

2. **Create Deck (Slide Presentation)**
   - Parse [SLIDE:...] markers from script
   - 1 slide per major section (typically 8-12 slides for 30 min)
   - Structure: Title → Problems/Concepts → Examples → Conclusion
   - Output: `deck_outline.md` (markdown outline, not PowerPoint)
   - Include: Slide text, call-outs for visuals, speaker notes per slide

3. **Create Blog Post**
   - Convert script → article form (prose, not spoken)
   - Add citations + links (from research)
   - Add section headers for scannability
   - Include code blocks, images (as [IMAGE: description])
   - Add CTA (call-to-action: subscribe, next lesson, etc.)
   - Output: `blog_post.md`
   - Length: usually 1500-2500 words (script text → prose)

4. **Create LinkedIn Post + Video Clip**
   - Extract 1-3 catchy quotes/soundbites from script
   - Create LinkedIn post: short text (100-300 chars) + hook + CTA
   - Identify where video clip should be: [CLIP: X min:sec from spoken recording]
   - Length: 15-60 sec recommended
   - Output: `linkedin_post.md` (post text + clip timestamp)

5. **Create Animation Spec** (If needed)
   - Parse [ANIMATION: scene description] from script
   - Detail what visuals are needed (characters, transitions, text overlays)
   - Scene-by-scene breakdown with script match (which words, which visuals)
   - Output: `animation_spec.md`

6. **Create YouTube Package**
   - Title: [title + variant for SEO]
   - Description: [500 char summary + links + timestamps]
   - Timestamps: [Rough breakdown of video sections]
   - Tags: [SEO keywords from topic + research]
   - Thumbnail description: [Visual concept for thumbnail design]
   - Output: `youtube_package.md`

## Outputs (To output/ folder)
```
output/[topic-slug]/
├─ spoken_notes.md              [For recording artist]
├─ deck_outline.md              [For deck designer]
├─ blog_post.md                 [For blog publishing]
├─ linkedin_post.md             [Text + clip spec]
├─ animation_spec.md            [For animator/designer]
├─ youtube_package.md           [For video upload]
├─ README.md                    [Index of all deliverables]
└─ source/
   ├─ teaching_script.md        [Original script]
   ├─ enterprise_script.md      [If both streams]
   ├─ research_output.md        [For reference]
   └─ discovery_brief.md        [For reference]
```

## Success Criteria
✓ Every [SLIDE:...] marker → one slide outline
✓ Every [DEMO:...] marker → identified in deck + blog + animation spec
✓ Every [PAUSE:...] marker → preserved in spoken notes
✓ Script text → blog post (prose conversion, not copy-paste)
✓ LinkedIn post: <300 chars, includes hook + CTA
✓ YouTube package: description, timestamps, tags, thumbnail spec
✓ Animation spec: scene-by-scene with script timestamps
✓ All deliverables link back to research (citations, quotes credited)

## Produced Files
- `spoken_notes.md` → recording artist
- `deck_outline.md` → designer/presenter
- `blog_post.md` → blog publishing
- `linkedin_post.md` → social media
- `animation_spec.md` → animator
- `youtube_package.md` → video uploader
- `README.md` → deliverables index
- `output/[topic-slug]/` folder structure → final delivery package

## Templates Used
- See `references/deck_template.md` (slide structure)
- See `references/blog_template.md` (article structure)
- See `references/animation_template.md` (visual storytelling)
- See `references/youtube_template.md` (SEO + packaging)

## Final Stage: Delivery
Human reviews all deliverables:
- [ ] Spoken notes are clear (no ambiguity for talent)
- [ ] Deck is visually scannable (short text, clear structure)
- [ ] Blog is prose, not copied text (reads naturally)
- [ ] LinkedIn post has hook + CTA (shareable)
- [ ] Animation spec matches script pacing
- [ ] YouTube package is SEO-optimized

Once approved → ready for recording/publication.
