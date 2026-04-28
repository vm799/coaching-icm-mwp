# Root CONTEXT — Layer 1 (Workspace Routing)

## "Where am I?" (Workspace Identity)
Coaching content factory. Dual-stream video series production:
- **Teaching Stream:** ICM/MWP zero-to-hero (10 videos × 30min)
- **Enterprise Stream:** AI safety leadership (10 videos × 30min)

Both produce scripts → multiplied to: speak/deck/blog/video/animation.

## "Where do I go?" (Stage Routing)
User brings a **topic** (e.g., "Token efficiency and why it matters").

Pipeline routes it:
1. **01_discovery/** → What's the topic? Who needs to know? Why now?
2. **02_research/** → Data, sources, expert commentary, examples
3. **03_script/** → Write script ready to tailor for both streams
4. **04_multiply/** → From script → speak/deck/blog/video/animation

## Inputs per Stage

### User Input (initial)
- **Topic:** (e.g., "Progressive disclosure in ICM")
- **Stream:** Teaching OR Enterprise (or both)
- **Scope:** Estimated research hours, sources available

### Stage 01 Output → Stage 02 Input
- Topic summary, discovery notes, research brief

### Stage 02 Output → Stage 03 Input
- Researched outline, sources, expert quotes, data, examples, analogies

### Stage 03 Output → Stage 04 Input
- **Two scripts:** One teaching-tuned, one enterprise-tuned (or unified if applicable)
- Ready to tailor, speak from, build deck from

### Stage 04 Output → Deliverables
- Spoken version (recorded)
- Deck (slide presentation)
- Blog post (written)
- LinkedIn post + video clip
- Animation/visual spec
- YouTube thumbnail + description

## Configuration (Layer 3)
- `_config/teaching-voice.md` → Tone for learning content
- `_config/enterprise-voice.md` → Tone for executive content
- `_config/icm-mwp-framework.md` → Reference knowledge (static)
- `_config/catchphrases.md` → Enterprise soundbites library
- `_config/systems-thinking.md` → Meta-lens: load during Stage 03 for all scripts

## Systems Thinking: The Meta-Lens
All content uses systems thinking as the underlying intellectual framework.
ICM/MWP is systems thinking applied to AI context management.

Every script (teaching + enterprise) should thread in:
- The relevant archetype (what failure pattern does this topic prevent?)
- The leverage point (where is the high-impact change?)
- The feedback loop (what reinforcing or balancing loop is at play?)
- The mental model shift (what belief needs to change?)

See `_config/systems-thinking.md` for full concept library + ICM/MWP mappings.
- `references/` → Stable templates, examples, analogies

## Working State (Layer 4)
- `output/` → Final scripts, deliverables
- Each topic gets its own subfolder: `output/[topic-slug]/`

## Execution Model
Same agent orchestrates all stages. Folder structure routes context.
- Stage 01: reads topic → produces discovery brief
- Stage 02: reads discovery → produces research output
- Stage 03: reads research → produces two tuned scripts
- Stage 04: reads scripts → produces all derivatives

No handoff needed. Human reviews & edits at each boundary before next stage runs.
