# Twitter/X Thread Template

Stage 04 produces thread from script soundbites + key points.
Source: enterprise soundbites + teaching analogies + data from research.

---

# [Topic] — Twitter/X Thread

## Thread Structure (6-10 tweets)

**Tweet 1 — Hook (stop the scroll)**
Bold claim, surprising stat, or polarizing opinion.
Max: 280 chars. No context. Just the hook.

Pattern: "[Surprising statement that creates a gap — they need to read more to understand]"

Examples:
- "Most AI projects fail not because of bad models. Because of bad context. A thread on why."
- "Tokens are attention. Attention is expensive. Here's how most teams waste theirs. 🧵"
- "Safe AI isn't slower AI. Here's what that actually means (and what to do Monday):"

---

**Tweet 2 — The Problem**
What's broken? Who feels this pain?

Max 280 chars. One sentence problem statement + one stat (if available).

Example:
> "Most teams dump all available data into prompts and hope the model figures it out. Result: bloated contexts, slower responses, and wasted API costs. This is the #1 token efficiency mistake."

---

**Tweet 3 — The Insight / Analogy**
Core concept. Teaching moment. Make it quotable.

Example:
> "A library doesn't hand you every book in the building when you ask a question. It gives you the catalog. You request the book. That's context efficiency. Load only what the decision needs."

---

**Tweet 4 — How It Works (Step 1)**
One mechanism. Simple. Short.

Example:
> "The fix: selective context loading.
> Instead of: load everything
> Do: ask 'what does this decision actually need?'
> Load only that.
> Token count drops. Accuracy rises. Cost falls."

---

**Tweet 5 — How It Works (Step 2) or Proof**
Evidence. Data. Real example.

Example:
> "We tested this in a production system:
> Before: 4,200 tokens per request
> After (selective loading): 1,800 tokens
> Same accuracy. 57% cost reduction.
> The bottleneck was never the model. It was the context."

---

**Tweet 6 — Common Objection / Counterintuitive Point**
Address pushback. Shows you've thought it through.

Example:
> "You might think: less context = less information = worse answers.
> Actually the opposite.
> LLMs perform worse with too much context ('lost in the middle' degradation).
> Precision > completeness."

---

**Tweet 7 — Real-World Application**
How to actually use this. Practical.

Example:
> "Practical application:
> Before loading context, ask:
> - What stage is this decision at?
> - What information is actually needed?
> - What can be fetched on-demand vs loaded upfront?
> This single habit reduces your token budget by 30-50%."

---

**Tweet 8 — Soundbite / Quotable**
The phrase they'll screenshot and share.

Example:
> "'Tokens are attention. Attention is expensive. This is how we spend them wisely.'
> Context efficiency isn't a nice-to-have. It's the difference between a bottleneck and scale."

---

**Tweet 9 — Action Items**
3 things to do now.

Example:
> "Start this week:
> 1. Audit one prompt — what's in it that isn't needed?
> 2. Move large reference docs to on-demand load
> 3. Measure token count before/after
> Share what you find."

---

**Tweet 10 — CTA**
Drive somewhere. Video, blog, newsletter, follow.

Example:
> "Full 30-min breakdown: [YouTube link]
> Written version: [Blog link]
> If this was useful, follow for more on context engineering + AI systems.
> Retweet if your team needs to see this."

---

## Thread Metadata

- **Topic tag:** Include in Tweet 1 ([concept name], topic hashtag)
- **Hashtags:** 3-5 max (in Tweet 1 or final tweet — not every tweet)
- **Thread indicator:** Add 🧵 to Tweet 1 to signal it's a thread
- **Image:** Add diagram/visual to Tweet 3 or 5 (gets 2x engagement)
- **Links:** Only in last tweet (algorithm penalizes links in early tweets)

---

## Thread Spec Format (Stage 04 Output)

```markdown
## Twitter/X Thread: [Topic]

### Tweet 1 (Hook)
[Exact text, under 280 chars]
[Hashtags, if any]

### Tweet 2 (Problem)
[Exact text]

### Tweet 3 (Insight)
[Exact text]
[IMAGE: description of image to attach]

### Tweet 4 (Mechanism)
[Exact text]

### Tweet 5 (Proof)
[Exact text]
[IMAGE: screenshot of data or code output, if available]

### Tweet 6 (Objection)
[Exact text]

### Tweet 7 (Application)
[Exact text]

### Tweet 8 (Soundbite)
[Exact text]

### Tweet 9 (Action)
[Exact text]

### Tweet 10 (CTA)
[Exact text]
[LINKS: YouTube, Blog]
```

---

## Best Practices

**Engagement:**
- Tweet 1 must stop scroll — test hook on yourself: "Would I read on?"
- Tweet 3 or 5 = image or diagram (gets reshared)
- Tweet 8 = screenshot bait (make it quotable)
- Thread finisher: "If this was useful, retweet Tweet 1" (drives reach)

**Formatting:**
- Short paragraphs (2-3 lines per tweet)
- Line breaks between ideas
- Bold claims stand alone on one line
- Lists use plain dashes or numbers (not markdown — doesn't render on X)

**Timing:**
- Post day of YouTube / blog publish
- Best times: 8-10am or 6-8pm in your audience's timezone
- Schedule with Typefully or Buffer (drafts saved, easy to reuse)

**Don't:**
- Put links in early tweets (algorithm penalty)
- Use more than 5 hashtags
- End every tweet with a question (annoying pattern)
- Thread longer than 12 tweets (engagement drops after 10)
