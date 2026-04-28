# Email Template — Newsletter + Executive Summary

Stage 04 produces email from blog/script. Two types: newsletter (teaching list) and executive summary (enterprise).

---

# [Topic] — Email Package

---

## Type A: Newsletter Email (Teaching Stream)

**Audience:** Subscribers who opted in to learn about ICM/MWP
**Length:** 300-500 words
**Tone:** Personal, curious, direct
**Goal:** Drive to YouTube video / blog post

### Subject Line
Must open. 3 subject line options:

```
Option 1 (Curiosity): "Why more context actually makes AI worse"
Option 2 (Benefit): "Cut your AI costs by 40% — here's how"
Option 3 (Personal): "The mistake I made with context (and how I fixed it)"
```

**Rules:**
- Under 50 chars (truncated on mobile otherwise)
- No clickbait (respect trust, don't oversell)
- Test 2 options (A/B split if list is large enough)

### Email Body

```
Hi [First name] / Hi there,

[HOOK: 1 sentence — bold claim or personal story that leads to topic]

[PROBLEM: 2-3 sentences — the problem this topic solves]

[BRIDGE: 1 sentence — "This week I published X covering Y"]

[3 BULLETS: What they'll learn from watching/reading]
• [Learning 1]
• [Learning 2]
• [Learning 3]

[CTA BUTTON / LINK]: Watch the video →  [link]
OR: Read the post → [link]

[BRIEF PERSONAL NOTE: 1 sentence — why I made this, or what surprised me in research]

[SIGNATURE]
[Your name]
[Title / Context: "Teaching ICM/MWP at [channel]"]

---
P.S. [Optional: second CTA or teaser for next topic]
```

### Example

```
Hi there,

More context doesn't mean better AI answers. I spent three months thinking it did.

Most teams stuff every document, instruction, and history into the prompt. It feels thorough. The model feels more "informed." But accuracy drops. Costs spike. And nobody knows why.

This week I broke down exactly why this happens — and what to do about it.

In 30 minutes you'll understand:
• Why "lost in the middle" degrades LLM performance
• How selective context loading works (with code)
• The 3-question framework I use before loading any context

Watch: [link] (30 min) →

The research surprised me — the fix is simpler than I expected once you see the mechanism.

V

---
P.S. Next week: Progressive disclosure — the same principle, applied to how we teach AI systems to explain themselves.
```

---

## Type B: Executive Summary Email (Enterprise Stream)

**Audience:** Executive list, decision-makers, clients
**Length:** 200-350 words
**Tone:** Professional, data-forward, action-oriented
**Goal:** Drive to LinkedIn article, video, or consultation

### Subject Line Options

```
Option 1 (Data): "57% token cost reduction — what we found"
Option 2 (Risk): "The AI governance gap your competitors are closing"
Option 3 (Action): "3 things to do this week on AI context efficiency"
```

### Email Body

```
[FIRST NAME] / Hi,

[1-SENTENCE BUSINESS HOOK: Problem or opportunity they care about]

[BRIEF CONTEXT: 2-3 sentences on what you've been working on / researching]

[THE INSIGHT: 2-3 sentences — the core finding, with data]

[WHAT IT MEANS FOR THEM: 2 sentences]

[3 ACTION ITEMS]:
1. [Action 1]
2. [Action 2]
3. [Action 3]

Full breakdown: [link to LinkedIn article or video]

[OPTIONAL: Open door for conversation]
If you're navigating this in your organisation, I'm happy to walk through what we've seen. Reply to this email.

[SIGNATURE]
[Name] | [Title]
[Company] | [URL]
```

### Example

```
Hi Sarah,

Most enterprise AI deployments are spending 2-3x more on API costs than they need to. The reason: context hoarding.

I've been tracking this pattern across 12 enterprise deployments in the last year. Teams load everything — every document, every history, every rule — into every prompt. It feels safe. It's expensive.

The fix: selective context loading. We tested this in production. Token count dropped 57%. Accuracy held.

What this means for your team:
1. Audit your current prompts — what's in there that isn't needed?
2. Define context budgets per use case
3. Measure: token count + accuracy before and after

Full breakdown with implementation detail: [link] (10 min read)

If you're working through this, happy to spend 30 minutes. Just reply here.

V
Process Pro AI | processpro.uk
```

---

## Email Checklist

- [ ] Subject line: under 50 chars, specific, no clickbait
- [ ] First sentence: hook (no warm-up, no "hope you're well")
- [ ] 3 learning bullets (newsletter) or 3 actions (enterprise)
- [ ] One clear CTA (not three links)
- [ ] Personal sign-off (not corporate boilerplate)
- [ ] Plain text renders correctly (no markdown, no fancy HTML)
- [ ] Mobile readable: short paragraphs, no wide tables

---

## Email Sequence (Per Topic Launch)

| Email | Type | Timing | Goal |
|-------|------|--------|------|
| Email 1 | Launch (newsletter or exec) | Day of publish | Drive to content |
| Email 2 | Follow-up (what reader did) | Day +3 | Re-engage non-openers |
| Email 3 | Digest | End of month | Recap all month's content |

**Re-engagement subject (Email 2 to non-openers):**
```
"In case you missed: [new subject line, slightly different angle]"
```
