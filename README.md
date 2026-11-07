# Thinking and Decisions Skills for AI Agents

[![5 skills](https://img.shields.io/badge/skills-5-0b7285)](#all-skills)
[![Format: Agent Skills](https://img.shields.io/badge/format-SKILL.md-5f3dc4)](https://agentskills.io/specification)
[![Licence: CC BY 4.0](https://img.shields.io/badge/licence-CC%20BY%204.0-2b8a3e)](https://creativecommons.org/licenses/by/4.0/)

Free **Agent Skills** (`SKILL.md`) that help Claude, Claude Code, OpenAI Codex and other AI agents support better thinking: define the right problem first, generate ideas that are genuinely different, choose with the right method, weigh trade-offs honestly and stress-test a plan before committing. The agent frames, widens and challenges; you decide.

By [**Afeez Adebayo**](https://afeezadebayo.com) · [Browse online](https://afeezadebayo.com/skills-md/productivity/thinking-decisions/) · [LinkedIn](https://www.linkedin.com/in/afeez-adebayo/) · [X](https://x.com/za_icon)

Part of the [Productivity skills](https://github.com/afeezadebayo/productivity-skills) library.

## All skills

| Skill | What it does |
|---|---|
| [`problem-framing`](problem-framing) | Tests whether a problem is framed well and offers better frames before anyone solves it |
| [`brainstorming`](brainstorming) | Generates a wide, varied set of ideas, then narrows them, with a check that ideas are not all the same |
| [`decision-frameworks`](decision-frameworks) | Picks the right method to choose between defined options |
| [`trade-off-analysis`](trade-off-analysis) | Weighs a few options on several criteria and shows what each gives up |
| [`premortem-analysis`](premortem-analysis) | Imagines the plan has failed and works back to the causes |

More skills in this set are planned. See the [full list online](https://afeezadebayo.com/skills-md/productivity/thinking-decisions/).

## Install

```bash
git clone https://github.com/afeezadebayo/thinking-decisions-skills.git
# Claude Code
cp -r thinking-decisions-skills/problem-framing ~/.claude/skills/
# Codex and other agents
cp -r thinking-decisions-skills/problem-framing ~/.agents/skills/
```

In Claude.ai or Claude Desktop, zip a single skill folder and upload it under **Settings → Capabilities → Skills**.

Then ask your agent, for example: *"Frame this problem before we solve it"* or *"Brainstorm options, and make sure they are not all the same."*

## A sensible order

1. `problem-framing`: make sure it is the right problem.
2. `brainstorming`: widen the options.
3. `decision-frameworks` or `trade-off-analysis`: choose.
4. `premortem-analysis`: stress-test the choice before committing.

## Safety first

These skills do not choose for you, invent evidence or give legal, financial or medical advice. Claims are tagged by source, and the agent keeps sensitive details out of its working notes.

## Licence

Released under [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/). Use, share and adapt, including commercially, with credit to Afeez Adebayo and a link to the source page in each file.
