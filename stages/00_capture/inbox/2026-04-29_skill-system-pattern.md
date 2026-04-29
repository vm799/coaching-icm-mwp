# Capture: 2026-04-29 — Ken Huang, "The Skill System Pattern (Claude Code vs Hermes Agent)"

**Source:** Ken Huang, Agentic AI Substack, April 29 2026
**Captured by:** V
**Selective extract only. Code samples not captured — not V's domain for this series.**
**Status:** PROCESSED ✓

---

## Why This Matters for V

This article shows where the field is heading for agent skill systems. Four direct connections to V's content:

---

### 1. Tier 0-3 Progressive Disclosure = ICM L0-L4 (Validates Architecture)

Hermes Agent's four-tier skill discovery:

| Tier | What loads | Token cost |
|------|-----------|------------|
| 0 | Category names + counts only | Minimal |
| 1 | Name + description per skill | Low |
| 2 | Full SKILL.md content + file list | Medium |
| 3 | Individual supporting file on demand | Targeted |

**This is ICM's L0-L4 progressive loading described in a production agent system.**
- L0 = Tier 0 (workspace identity only)
- L1 = Tier 1 (pipeline routing)
- L2 = Tier 2 (stage contract)
- L3-L4 = Tier 3 (load only when task needs it)

**V's framing:** "ICM isn't a V invention. It's the pattern that every serious agent framework independently converges on. Hermes calls it Tier 0-3. ICM calls it L0-L4. The principle is identical: load only what the current task needs."

**Use in:** T4 "ICM layers explained" + any enterprise talk where V needs to defend layered architecture against "why not just one big prompt?"

---

### 2. SKILL.md = The "Executable Skills File" YC Described

Tom Blomfield (YC): "A system that... turns [knowledge] into an executable skills file for AI."

Hermes does this literally: every skill = a `SKILL.md` file with YAML frontmatter (name, version, platforms, prerequisites, environment variables) + markdown procedure body.

**V's connection:**
- CLAUDE.md = V's executable skills file
- ICM L0-L3 stack = V's skill library
- Stage contracts (CONTEXT.md) = individual skills in the Hermes sense

YC said the Company Brain layer doesn't exist. Hermes is building one version of it. V is building another — simpler, filesystem-native, no framework dependency.

**Use in:** Enterprise talk on Company Brain. "YC named the gap. Here's one industry implementation. Here's V's implementation. Same principle, different complexity level."

---

### 3. Security Scanning for Skills = Enterprise Governance Angle

Hermes scans every externally-sourced or agent-created skill before installation. Nine threat categories: exfiltration, injection, destructive operations, persistence, network (reverse shells), obfuscation, supply chain, privilege escalation, credential exposure.

Trust tiers:
- Built-in: always allowed
- Trusted (e.g. openai/skills, anthropics/skills): allowed unless dangerous
- Community: blocked on anything above safe verdict
- Agent-created: ask user on dangerous

**V's enterprise angle:**
> "When agents write agents — or skills teach other skills — you need a trust model. Not just for the output. For the capability itself. Who wrote this skill? What can it do? Has it been scanned? Hermes has an answer. Most enterprise AI deployments have none."

**Use in:** E7 "Glass-box AI" + any enterprise governance talk. The field is moving toward skill marketplaces — V's clients need to know governance is a first-class concern.

---

### 4. /.well-known/skills Standard = "Software for Agents" YC Topic (#12)

Any domain can expose a skill registry at `/.well-known/skills/index.json`. Standard format. Any agent that understands the protocol can discover and install skills from any domain.

**YC's Aaron Epstein (#12):** "Machine-readable interfaces: APIs, MCPs, CLIs. Tools that agents can discover, sign up for, and start using programmatically without a human in the loop."

**This is that standard, applied to skills specifically.**

**V's framing:** "The infrastructure for agents to consume capabilities is being standardised now. /.well-known/skills is to agent skills what DNS is to domains — a discovery mechanism. Whoever builds skill registries for enterprise domains owns a strategic asset."

**Use in:** Topics backlog — new enterprise topic: "Who owns your agent's skill library?" Skill governance as next-layer enterprise concern after context governance.

---

## Routed to:

- `enterprise_angles.md` → Add skill governance section: trust tiers, scanning, /.well-known standard
- `topics_backlog.md` → New enterprise topic: "Agent skill governance: who controls what your agent can do?"
- `analogies_bank.md` → Progressive disclosure Tier 0-3 as external validation of ICM L0-L4
- Does NOT change technical series topics — already covered adequately
