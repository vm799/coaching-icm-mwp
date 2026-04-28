# Interactive Demo Template — Show and Tell

Stage 04 produces this for code-heavy or system-heavy topics.
Used in: YouTube show-and-tell, live demos, workshops, 121 briefings.

---

# [Topic] — Interactive Demo Package

## Demo Metadata
- **Topic:** [What concept does this demo illustrate?]
- **Demo type:** [Live coding / Walkthrough / Interactive tool / Before-after comparison]
- **Platform:** [Python / JS / Browser / CLI / Notebook / App UI]
- **Audience:** [Teaching (curious learners) / Enterprise (decision makers) / Technical (engineers)]
- **Duration:** [5 min / 10 min / 20 min]
- **Repo:** [GitHub link to runnable demo code]

---

## Demo Structure (Show-and-Tell Arc)

### 1. Setup The Problem (1-2 min)
What breaks without this? What is the learner about to witness?

**Live script:**
> "Here's the problem we're solving. Watch what happens when I [action]..."
> [Show the BROKEN version first — make the problem visible]

**What to show:**
- System without the concept applied → show the failure
- OR: naive implementation → show inefficiency
- OR: common mistake → show the consequence

**Goal:** Audience thinks "oh, I recognize that problem"

---

### 2. Build/Run The Solution (3-5 min)
Step by step. Narrate every action as you do it.

**Template:**

```
Step 1: [Action]
# Narrate: "First, I [action]. Notice that..."

Step 2: [Action]
# Narrate: "Now I [action]. This is the key line — [explain why]"

Step 3: [Action]
# Narrate: "And here we see the result..."
```

**Key rule:** Narrate what you're DOING, not what the code IS.
- Bad: "This is a for loop"
- Good: "This loops through each context item and filters out anything below our relevance threshold"

**Pause after each step:** "Any questions before I go to the next step?" (if live)

---

### 3. Show The Output (1-2 min)
What changed? What does success look like?

**Before/after comparison:**
- Before: [metric / output / failure state]
- After: [metric / output / success state]

**Narrate:**
> "Before: [bad thing]. After: [good thing]. The difference is X."

**Show visually:** Side-by-side, graph, or print statement showing improvement.

---

### 4. What Just Happened? (1 min)
Explain the mechanism. Why did that work?

> "What we just saw was [concept] in action. Specifically: [mechanism in 2 sentences]."

Connect back to core concept from script.

---

### 5. Try It Yourself (Optional, For Workshops)
Give audience a task.

**Pattern:**
> "Now you try. Here's a variation: [slightly different problem]. What does your version do? [5 min pause / exercise]"

**Setup:** They have repo cloned or notebook open before session.

---

## Demo Repo Structure

```
demo-[topic-slug]/
├─ README.md            ← How to run, what to expect
├─ requirements.txt     ← Pinned dependencies
├─ problem.py           ← Broken version (what we're fixing)
├─ solution.py          ← Fixed version (what we're building)
├─ compare.py           ← Before/after comparison + output
├─ interactive.ipynb    ← Jupyter notebook (if educational)
├─ data/
│  └─ sample_input.json ← Sample data to run demo with
└─ output/
   ├─ before.txt        ← Expected output before fix
   └─ after.txt         ← Expected output after fix
```

---

## Demo Code Template

```python
# demo/solution.py — [Topic] Demo
# This demo shows: [what concept in 1 line]
# Run: python solution.py

# --- SETUP ---
import [libraries]

SAMPLE_INPUT = """
[Realistic sample input that learner can relate to]
"""

# --- THE PROBLEM (without solution) ---
def naive_approach(input_text):
    """
    The naive/common approach. Show what's wrong with this.
    """
    # [Naive implementation — intentionally bad or inefficient]
    return result

# --- THE SOLUTION ---
def [concept_name](input_text):
    """
    [What this does in one sentence].
    
    Key mechanism:
    1. [Step 1 in plain language]
    2. [Step 2 in plain language]
    3. [Step 3 in plain language]
    """
    # [Implementation — well-commented, readable]
    return result

# --- COMPARISON ---
if __name__ == "__main__":
    print("=== NAIVE APPROACH ===")
    naive_result = naive_approach(SAMPLE_INPUT)
    print(f"Output: {naive_result}")
    print(f"Tokens used: {len(naive_result.split())}")  # or relevant metric
    
    print("\n=== WITH [CONCEPT] ===")
    solution_result = [concept_name](SAMPLE_INPUT)
    print(f"Output: {solution_result}")
    print(f"Tokens used: {len(solution_result.split())}")
    
    print("\n=== COMPARISON ===")
    print(f"Reduction: {100 - (len(solution_result.split()) / len(naive_result.split()) * 100):.0f}%")
```

---

## Demo Script (What You Say While Running It)

This is the narration track for the demo. Used in:
- YouTube show-and-tell (say this while showing screen)
- Live demo (read-from notes or memorized)
- Async recording (narrate into Loom)

```
[0:00] "Let me show you [concept] in practice."
        "First, the problem we're solving: [1 sentence]."

[0:30] "Here's the naive approach most people start with."
        [Run naive_approach]
        "See the output: [describe it]. Notice: [what's wrong]."

[1:30] "Now let's apply [concept]."
        [Open solution.py]
        "Key idea is here [point to key line]. This is where [mechanism] happens."

[2:30] [Run solution]
        "See the difference: [before metric] vs [after metric]."
        "That's a [X]% improvement in [what metric]."

[3:30] "Why does this work? [1-2 sentences on mechanism]"
        "The principle here maps to what we discussed: [connect to script concept]"

[4:30] "Want to see a harder version?" [if time / audience engaged]
        OR
        "That's the core of it. [Close with takeaway]"
```

---

## YouTube Show-and-Tell Specific

For YouTube format, demo needs:

1. **Screen + face cam** (split: screen 70%, face 30%)
2. **Code readable** (font size: 16-18pt minimum; VS Code light theme reads better on video)
3. **Fast pace:** Edit out dead time (typing, waiting for output)
4. **Chapters:** Mark demo section with timestamp

**YouTube edit notes:**
```
[EDIT: Cut wait time between run and output]
[EDIT: Zoom into key line when narrating "this is the key line"]
[EDIT: Add callout box highlighting the metric comparison]
[CAPTION: Key concept as text overlay when explaining mechanism]
```

---

## Demo Variants (Match to Audience)

### For Non-Technical Audience (BAs, Managers, Execs)
- Use pre-built output comparison (not live coding)
- Show RESULT, not CODE
- "Imagine a system that..." → show UI or slide
- Script: "You don't need to understand the code. Here's what the output looks like before and after."

### For Technical Audience (Engineers)
- Run live code
- Show errors too (makes it more real)
- Let them ask questions during demo
- Share repo link immediately: "Fork this and run it yourself"

### For Mixed Audience
- Start non-technical (show result)
- "For the engineers in the room, here's the code" (pivot to technical)
- Keep technical section brief enough for non-tech to follow conceptually

---

## Failure Recovery (Live Demo)

**Demo doesn't run:**
> "Let me pull up the pre-run output — I have that standing by."
[Show screenshot or output/ directory]

**Unexpected error:**
> "Interesting — this is actually a useful failure mode. What's happening here is [explain error]. This is exactly why [concept] matters."
[Turn failure into teaching moment]

**Wrong output:**
> "Hmm, that's not what I expected. Let me [check X]. Ah — [reason]. Good lesson: [takeaway from debugging live]"
[Never panic; live debugging = good content]

---

## Demo Checklist

Before running (live or recording):
- [ ] Repo cloned, dependencies installed, code tested (not 30 min before — day before)
- [ ] Output files regenerated (no stale cache)
- [ ] Font size: 16pt min in editor
- [ ] Dark or light theme: consistent (don't switch mid-demo)
- [ ] Terminal: clear before starting
- [ ] Backup screenshots: run demo once ahead of time, screenshot each step
- [ ] No sensitive data in sample input (public demos only)
- [ ] README tested by someone else (they should be able to run without your help)

For recording:
- [ ] Screen resolution: 1920x1080 (or 1440p for retina)
- [ ] Close notifications (phone, Slack, email)
- [ ] Silence phone
- [ ] Empty browser tabs (only what demo needs)

---

## Demo → Other Formats

After demo is built:

| Demo Component | Repurpose As |
|----------------|--------------|
| problem.py + output | "What breaks without X" blog section |
| solution.py walkthrough | YouTube Show-and-Tell video |
| compare.py output | "Before/after" LinkedIn post |
| Jupyter notebook | Workshop hands-on exercise |
| README.md | Tutorial article (expand steps) |
| Error recovery moments | FAQ: "What can go wrong?" section |
