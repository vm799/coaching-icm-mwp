# Distribution Matrix — Create Once, Publish Everywhere

One script → all formats. Choose your channels. This matrix maps what to produce and where it goes.

---

## Channel Map

| Format | Teaching | Enterprise | Stage Talk | Live/Demo | Effort |
|--------|----------|------------|------------|-----------|--------|
| YouTube long-form (30 min) | ✓ | ✓ | — | — | Low (upload) |
| YouTube Shorts (60 sec) | ✓ | ✓ | — | — | Med (clip) |
| LinkedIn video post | ✓ | ✓ | ✓ | — | Low (clip) |
| LinkedIn article | — | ✓ | ✓ | — | Med (rewrite) |
| Blog post (long-form) | ✓ | ✓ | — | — | Low (convert) |
| Email newsletter | ✓ | ✓ | — | — | Low (extract) |
| Twitter/X thread | ✓ | ✓ | — | — | Low (extract) |
| Stage talk (deck + notes) | ✓ | ✓ | ✓ | — | Med (tailor) |
| Live webinar / 121 | ✓ | ✓ | — | ✓ | Med (adapt) |
| Interactive demo | ✓ | — | — | ✓ | High (build) |
| Podcast audio | ✓ | ✓ | — | — | Low (extract) |
| Quote graphics (social) | ✓ | ✓ | ✓ | — | Low (design) |
| Animation (explainer) | ✓ | ✓ | — | — | High (produce) |
| Internal wiki / docs | — | ✓ | — | ✓ | Low (adapt) |
| Slide deck (standalone) | ✓ | ✓ | ✓ | ✓ | Med (design) |

---

## Stream Defaults

### Teaching Stream → Produce These
1. YouTube long-form (core delivery)
2. YouTube Shorts (3-5 clips, 30-60 sec highlights)
3. Blog post (SEO + reference)
4. Twitter/X thread (distribution, reach)
5. Email (if list exists)
6. Interactive demo (if topic is code-heavy)

### Enterprise Stream → Produce These
1. LinkedIn article (thought leadership)
2. LinkedIn video post (executive visibility)
3. Stage talk (deck + speaker notes) — conference, all-hands, board
4. Email (executive summary version)
5. Quote graphics (soundbites as images)
6. Internal wiki (if deployment-relevant)

### Both Streams → Also Produce These (if resources allow)
- Animation (evergreen, high ROI)
- Podcast audio extract (zero extra effort — rip narration from video)
- Live webinar / 121 version (Q&A script, shorter deck)

---

## Priority Order (Time-Constrained Run)

### Minimum Viable Run (~4 hours post-script)
1. YouTube package (upload + metadata) — 30 min
2. Blog post — 1 hour
3. LinkedIn post + video clip — 30 min
4. Deck outline (for stage + 121) — 1 hour
5. Email draft — 30 min

### Full Run (~8-10 hours post-script)
Everything above, plus:
6. Twitter/X thread — 30 min
7. YouTube Shorts spec (3 clips) — 45 min
8. LinkedIn article — 1 hour
9. Quote graphics brief — 30 min
10. Podcast audio spec — 20 min

### Premium Run (~20+ hours, with design support)
Everything above, plus:
11. Animation spec → production — 16-40 hours
12. Interactive demo — 8-24 hours
13. Stage talk tailoring (conference version) — 3-4 hours

---

## Channel Details

### YouTube Long-Form
- **Source:** Full script (30 min) → record → upload
- **Template:** `references/youtube_template.md`
- **SEO:** Title, description, timestamps, tags
- **Repurpose from:** Script spoken notes

### YouTube Shorts / TikTok / Reels
- **Source:** Identify 3-5 best moments from long-form video
- **Length:** 30-60 sec each
- **Template:** `references/shorts_template.md`
- **Hook pattern:** [Problem/surprise statement] + [Quick answer] + [CTA: watch full video]

### LinkedIn Video Post
- **Source:** 60-90 sec clip from recording
- **Caption:** 3-5 lines + CTA (watch full / read blog)
- **Template:** Part of `references/linkedin_article_template.md`
- **When:** Same day as YouTube upload (cross-promote)

### LinkedIn Article
- **Source:** Enterprise script → article form (800-1500 words)
- **Template:** `references/linkedin_article_template.md`
- **Tone:** Executive. Data. Risk + opportunity. Soundbites.
- **When:** 1-2 days after YouTube (algorithm: separate it)

### Blog Post
- **Source:** Teaching or enterprise script → prose
- **Template:** `references/blog_template.md`
- **When:** Same day as YouTube (embed video in post = SEO boost)

### Email Newsletter
- **Source:** Blog post → short summary (300-400 words)
- **Template:** `references/email_template.md`
- **When:** 1-2 days after publish

### Twitter/X Thread
- **Source:** Script soundbites + data + key points
- **Template:** `references/twitter_thread_template.md`
- **Length:** 6-10 tweets
- **When:** Day of publish

### Stage Talk
- **Source:** Script → deck + speaker notes (tailored for 30 min on stage)
- **Template:** `references/stage_talk_template.md`
- **For:** Conference keynote, internal all-hands, team talk
- **When:** Produced once per topic; reused for each speaking event

### Live Webinar / 121
- **Source:** Stage talk materials + live Q&A script
- **Template:** `references/live_session_template.md`
- **For:** Recorded webinar, 1:1 exec briefing, team workshop
- **When:** On-demand; tailor per audience

### Interactive Demo
- **Source:** Research + script examples → runnable code / walkthrough
- **Template:** `references/demo_template.md`
- **For:** Live demos, workshop hands-on, YouTube show-and-tell
- **When:** Only for code-heavy topics; high effort but high retention

### Podcast Audio
- **Source:** Record video → extract audio → clean up
- **No extra writing:** Narration from video IS the podcast
- **Template:** `references/podcast_template.md`
- **When:** After video is recorded (zero content cost)

### Quote Graphics
- **Source:** Soundbites from enterprise script
- **Format:** 1080x1080 image (Instagram / LinkedIn square)
- **Template:** Part of `references/social_graphics_template.md`
- **When:** Batch-produce 3-5 per topic from catchphrases

---

## Input → Output Traceability

```
[TOPIC]
└─ research_output.md
└─ teaching_script.md
   ├─ → youtube_package.md         (upload now)
   ├─ → spoken_notes.md            (record today)
   ├─ → blog_post.md               (publish same day)
   ├─ → shorts_spec.md             (clip after recording)
   ├─ → twitter_thread.md          (post day of publish)
   ├─ → email_draft.md             (send 2 days later)
   └─ → interactive_demo.md        (if code-heavy topic)
└─ enterprise_script.md
   ├─ → linkedin_article.md        (publish 2 days after YT)
   ├─ → linkedin_video_post.md     (same day as article)
   ├─ → stage_talk_deck.md         (for conference / all-hands)
   ├─ → live_session_notes.md      (for webinar / 121)
   ├─ → quote_graphics_brief.md    (batch: 3-5 images)
   └─ → internal_wiki_post.md      (if enterprise deployment)
└─ both scripts
   └─ → podcast_spec.md            (audio extract after recording)
   └─ → animation_spec.md          (if budget/time allows)
```

---

## Scheduling Template (Per Topic)

| Day | Action |
|-----|--------|
| D-7 | Script finalized (teaching + enterprise) |
| D-5 | Record video (30 min) |
| D-4 | Edit video + create clips + upload to YouTube (scheduled) |
| D-3 | Blog post written + scheduled |
| D-2 | LinkedIn article written; email draft ready |
| D-1 | YouTube thumbnail uploaded; all assets staged |
| D0 | YouTube goes live; blog published; tweet thread goes out |
| D+1 | LinkedIn video post |
| D+2 | LinkedIn article + email send |
| D+7 | YouTube Shorts released (algorithm reset) |
| D+30 | Review analytics → update metadata if needed |

---

## Tooling Needed

| Output | Tool |
|--------|------|
| Video recording | Loom / OBS / Riverside.fm |
| Video editing | CapCut / DaVinci Resolve / Descript |
| Shorts clipping | Descript / CapCut auto-clip |
| Deck design | Google Slides / Canva / PowerPoint |
| Blog publishing | Substack / Medium / Ghost / Company site |
| Email | Mailchimp / Beehiiv / ConvertKit |
| Twitter thread | Typefully / Buffer |
| LinkedIn | Native (best reach) |
| Animation | Motion Bro / After Effects / Runway ML |
| Quote graphics | Canva |
| Interactive demo | CodeSandbox / Replit / Jupyter |
| Podcast distribution | Spotify for Podcasters / Anchor |
