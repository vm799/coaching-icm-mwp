# Technical Voice Config — AI-Native Engineering Stream

## Audience
Developers, technical leads, senior engineers, architects.
Already building with AI. Want to do it properly. Frustrated by vibe coding.
Familiar with: TDD, TypeScript, Git, CI/CD, clean architecture, DDD.
NOT familiar with (necessarily): ICM/MWP, context engineering, agentic pipelines at scale.

## Voice Characteristics

**Tone:** Peer-to-peer. Practitioner-to-practitioner. No hand-holding, no jargon theatre.
**Register:** Direct. Pattern-name it, show the code, explain the tradeoff.
**Style:** Pragmatic over theoretical. Show the failure mode, then show the fix.
**Analogies:** SWE-grounded. Unix pipes, compiler passes, SOLID, DDD, TDD. Engineers already know these.
**Depth:** Go deep on the "why" before the "how." Engineers distrust unexplained rules.

## What Works With This Audience

- **Show the failure first.** Vibe coding failure → then the pattern that prevents it.
- **Name things precisely.** "Sediment" not "context issues." "Smart Zone" not "token limits."
- **Use SWE precedent.** "This is Ousterhout's deep module principle applied to AI."
- **Admit tradeoffs.** "TDD with LLMs is slower up front. It pays back fast. Here's when it doesn't."
- **Show the loop.** Red-green-refactor, Ralph Wiggum, tracer bullet — name the loop and demonstrate it.
- **Code is expected.** Include code examples, CLI patterns, config snippets. Not just concepts.

## What Doesn't Work

- Enterprise-style soundbites ("your moat is draining")
- Non-technical analogies without SWE equivalent ("think of it like a recipe")
- Over-explaining basics (they know what TDD is — explain the AI-specific adaptation)
- Passive voice or hedging ("it might be worth considering")
- Treating them as buyers — they're builders

## Framing Principles

**Vibe coder vs AI engineer:** The foil is the vibe coder. The hero is the engineer who masters the behavior of a non-deterministic tool through deterministic practices (types, tests, architecture).

**The fundamental constraint:** Architecture is the primary constraint on AI reasoning. The model quality ceiling doesn't matter if the codebase floor is mud.

**The engineer's path:** Between "delegate everything" (ball of mud) and "delegate nothing" (burnout) is the gray box — human owns the interface, agent owns the implementation.

**Smart Zone:** Every session keeps agent inside the Smart Zone (~100K effective tokens). Every pattern (stage contracts, sediment clearing, vertical slices) exists to maintain this.

## Technical Stream Video Arc (10 videos)

| Video | Topic | Core Pattern |
|-------|-------|-------------|
| Tech-1 | Vibe coding is a trap | Software entropy, "ball of mud", the bounty |
| Tech-2 | Context engineering for engineers | Smart Zone, sediment, selective loading |
| Tech-3 | Deep modules for agentic codebases | Ousterhout deep/shallow, gray box strategy |
| Tech-4 | AI-native TDD | Red-green-refactor, cheating LLM, enforced failing tests |
| Tech-5 | TypeScript + AI: structural feedback | Types as deterministic safety net, preventing context pollution |
| Tech-6 | The Ralph Wiggum loop | Plan-Execute-Clear, AFK autonomy, Memento management |
| Tech-7 | Tracer bullets and vertical slices | Feature-complete paths, preventing horizontal coding |
| Tech-8 | Ubiquitous language in AI systems | DDD + ICM: glossary as shared map, CONTEXT.md as contract |
| Tech-9 | MWP as software architecture | ICM stages = Unix pipes = compiler passes = deep modules |
| Tech-10 | Building AI-native pipelines | Full pipeline demo: ICM in production, human gates, eval loop |

## Script Markers (Technical Stream)

Use same markup as other streams, plus:
- `[CODE:]` — include runnable code example
- `[DEMO:]` — show in terminal/IDE, not just narrate
- `[TRADEOFF:]` — name the cost explicitly before recommending
- `[FAILURE MODE:]` — show what breaks without this pattern
- `[SOUNDBITE:]` — practitioner-friendly line (repeatable in PR reviews, 1:1s)

## Connections to Teaching + Enterprise Streams

Technical stream goes deeper on SWE foundations.
Teaching stream explains the same concepts without code.
Enterprise stream explains the business impact of same concepts.

| Technical Stream | Teaching Stream | Enterprise Stream |
|-----------------|-----------------|------------------|
| Deep modules | Stage contracts | "Human owns interface, agent executes" |
| TDD loop | Human review gates | "Deterministic safety for non-deterministic AI" |
| Sediment clearing | Progressive context loading | "Token efficiency = cost architecture" |
| Smart Zone | "Lost in the middle" (Liu et al.) | "40% cost reduction per query" |
| Ralph Wiggum loop | Stage pipeline | "Tight loop beats planning cycle" |
| Vibe coding failure | "Prompt engineering is dead end" | "Bolt-on AI doesn't change what's underneath" |

## Sources for Technical Stream

- Ousterhout, "A Philosophy of Software Design" (2018) — deep modules
- Hunt & Thomas, "The Pragmatic Programmer" (1999/2019) — software entropy, tracer bullets
- Beck, "Test-Driven Development: By Example" (2002) — TDD
- Brooks, "The Mythical Man-Month" (1975) — shared design concept
- Evans, "Domain-Driven Design" (2003) — ubiquitous language
- Van Clief & McDermott (2026) — MWP as SWE architecture
- Karpathy (Feb 2025) — vibe coding (coined term)
- Karpathy (June 2025) — context engineering
- Liu et al. (2024) — "lost in the middle" (sediment scientific basis)
