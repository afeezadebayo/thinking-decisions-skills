---
name: brainstorming
description: "Generates a wide, varied set of ideas and then narrows it, built to beat the default failure of AI ideation: ideas that cluster around one obvious answer. Separates divergence from judgement, forces range with named techniques (constraints, the opposite, SCAMPER, random stimulus, personas, the worst possible idea, remix), runs a distinctness check so no single theme dominates, then clusters and converges to a shortlist the person chooses. Use whenever someone asks to brainstorm, generate ideas, come up with options, names, angles or approaches, run an ideation session, do a diverge-converge, or says the ideas they are getting feel generic, samey or obvious. Do NOT use for defining the problem first (use problem-framing), choosing between options already generated (use decision-frameworks or trade-off-analysis), stress-testing a chosen idea (use premortem-analysis) or writing the final copy or plan."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/productivity/thinking-decisions/brainstorming/
  category: productivity
  subcategory: thinking-decisions
  version: "1.0.0"
  created: "2026-10-24"
  updated: "2026-10-24"
---

# Brainstorming: Ideas That Are Not Generic

Ask an AI to brainstorm and you usually get ten versions of the same obvious idea. That is not a quirk of one model. A 2024 Nature Human Behaviour study found that generative AI narrows the range of ideas people produce, and in one toy-design task 94% of the AI-assisted ideas shared a single core concept. This skill is built to fight that. It forces range before it allows judgement, and it checks that the ideas are actually different from each other.

It is built for an agent working with one person or a small group, on any ideation task: product features, names, campaign angles, research questions, ways to cut a cost, approaches to a stuck problem. The techniques are tool-agnostic. The only tool-specific notes sit in one fenced appendix at the end.

Two rules run through it. First, generation and judgement never happen at the same time: you widen, then you narrow, and mixing them kills both. Second, quantity with variety beats a tidy shortlist of safe ideas, because it is easier to tame a wild idea than to make a dull one interesting. The person picks the winners. The agent does not decide.

## When to use this skill, and when not to

Use it when you need options and the obvious ones are not enough:

- Generating features, names, angles, headlines, research questions or approaches.
- Getting unstuck on a problem where the usual answers have not worked.
- Running a structured diverge-then-converge session, solo or with a group.
- Opening up a space before committing to a direction.
- Fixing a batch of ideas that all feel the same.

Do not use it for:

- Working out what problem to solve. Use `problem-framing` first. Brainstorming the wrong question wastes the whole session.
- Choosing between ideas you already have. Use `decision-frameworks` or `trade-off-analysis`.
- Pressure-testing an idea you have chosen. Use `premortem-analysis`.
- Writing the final copy, plan or spec. Brainstorming produces raw options, not finished work.
- Advice on health, money, legal standing or employment outcomes. Ideas in these areas are labelled as needing a qualified professional, and the skill does not present them as recommendations.

## Guardrails that apply to every run

1. **Diverge and judge separately.** During divergence, no idea is criticised, ranked or dismissed, including by the agent. Judgement happens only in the converge phase. Breaking this is the fastest way back to safe, generic output.
2. **No fabricated facts dressed as ideas.** A wild idea is welcome. A claim stated as fact is not, unless it carries its source. Any figure, or any assertion that a real company or person did something, is tagged `[unverified]` until checked. Do not invent evidence to make an idea sound proven.
3. **Variety is the deliverable, not volume.** A hundred near-identical ideas fail this skill. The distinctness check in step 4 is mandatory.
4. **Sensitive data stays out.** Prompts and ideas can carry names, client details, salaries and figures under NDA. Redact them before processing (see step 0). Never send them to a third-party service without asking.
5. **The person converges.** The agent can score and shortlist, but it does not pick the single answer or act on one. Turning an idea into a decision, a commitment or a sent message is out of scope and handed off.
6. **Scope boundary.** The skill refuses to present generic ideas as novel, to skip the divergence techniques, or to converge to one idea on its own.

## Inputs the agent must have before starting

Do not start until the first four are answered. Ask for what is missing in one message and wait.

| # | Input | What to ask if missing |
|---|---|---|
| 1 | The challenge, as a "how might we" | "State it as 'How might we ...?' One sentence. If you only have a topic, I will turn it into a question with you." |
| 2 | What a good idea looks like | "What would make an idea good here: novelty, feasibility, cheapness, impact? Name the two or three that matter, for the converge phase only." |
| 3 | Constraints and non-negotiables | "What is fixed (budget, time, platform, brand, legal) and what is off the table?" |
| 4 | How many ideas, and for whom | "Roughly how many ideas do you want to see, and who will use them? Default is 20 to 40." |
| 5 | Material to build on | "Any existing ideas, examples, competitors or research to start from or avoid repeating?" |
| 6 | Sensitivity | "Does any of this contain personal data, client names under NDA or unpublished figures?" |

If input 1 is a vague topic ("ideas for the app"), turn it into a "how might we" question before generating. A sharp question is the single biggest lever on idea quality.

## Workflow

### Step 0. Sensitivity triage

1. Scan for names, client references under NDA, salaries and unpublished figures.
2. Replace each with `[redacted: type]` in the working copy and report counts by type, without repeating values.
3. If the material is under NDA or the model is not approved for it, stop and ask how to proceed.

### Step 1. Frame the question

1. Write the challenge as "How might we ...?" It should be neither too narrow (a solution in disguise) nor too broad (unanswerable).
2. If it is too narrow, widen it one level: "How might we get people to click the button" becomes "How might we get people to the next step".
3. Confirm the question with the person before generating. Everything downstream inherits this question.

### Step 2. Diverge with techniques, not a plain list

Do not ask the model, or the room, for "ideas". That is what produces the single-concept cluster. Instead run at least four of these techniques, labelling which produced each idea. Aim for the target count from input 4 (default 20 to 40).

| Technique | Prompt |
|---|---|
| **Quantity first** | Generate many fast, no filtering. Quantity is the most reliable route to a good idea. |
| **Constraints** | "What if we could only use one [screen / minute / person / no budget / no internet]?" |
| **The opposite** | "What if we did the reverse of the standard approach here?" |
| **Worst possible idea** | List deliberately terrible ideas, then invert each into something usable. This frees people from the safe zone. |
| **SCAMPER on a seed** | Take one existing idea and push it: Substitute, Combine, Adapt, Modify, Put to another use, Eliminate, Reverse. |
| **Random stimulus** | Pick an unrelated object or domain and force a connection to the challenge. |
| **Personas** | Generate from different viewpoints: a child, a rival, a regulator, a first-time user, a cost-cutter. |
| **Remix** | "What if we combined idea X with idea Y?" |
| **Borrow** | How has this been solved in an unrelated field? |

For an AI agent, do not stop at one request. Research shows that restating the challenge, generating 25 diverse ideas, then applying a technique such as SCAMPER and reasoning through each, raised unique ideas by about 27% over a plain prompt (chain-of-thought ideation study, reported 2026; verify before relying on the exact figure). Default to that pattern.

### Step 3. Group-session option (people, not just an agent)

If more than one person is involved, prefer brainwriting over talking. In 6-3-5 brainwriting, six people each write three ideas in five minutes, then pass the sheet right; after six rounds you have up to 108 ideas in about 30 minutes. Writing in silence removes two known causes of weak group sessions: people blocking each other because only one can talk at a time, and holding back for fear of judgement. A group talking out loud typically produces fewer and less varied ideas than the same people working separately, so collect first, discuss second.

### Step 4. Distinctness check (mandatory)

This is the step that defeats generic output.

1. Cluster the ideas into themes by their core concept.
2. Apply two thresholds: there should be at least five distinct themes, and no single theme should hold more than about 40% of the ideas.
3. If one theme dominates, the batch is too narrow. Do not proceed. Return to step 2 and run techniques that pull away from that theme (the opposite, random stimulus, a distant persona), then re-cluster.
4. Record the theme counts, so the check is visible and not just asserted.

### Step 5. Converge

Only now does judgement start. Use the criteria from input 2.

1. Keep the raw list intact; converging never deletes ideas, it selects from them.
2. Score the ideas against the criteria. A quick impact-versus-effort sort, or a weighted score if the criteria carry different weight. For a full weighing of a few finalists, hand off to `trade-off-analysis`.
3. Shortlist three to five. For each, note why it was chosen and what it trades away.
4. Keep a "parked" list of promising ideas not chosen, with a one-line reason, so they can come back.
5. The person makes the final pick. The agent presents, it does not decide.

### Step 6. Document and hand off

1. Produce the output using the template: the question, the full idea list by technique, the theme clusters with counts, the scored shortlist, and the parked list.
2. Mark any idea that rests on an unchecked claim `[unverified]`.
3. Hand off: to `decision-frameworks` or `trade-off-analysis` to choose, to `premortem-analysis` to stress-test the chosen idea, and to `problem-framing` if the session revealed the question was wrong.

## Worked example

The example is invented for illustration. No figures come from a real company.

**Inputs.**

- Challenge (input 1): "Ideas to reduce no-shows for our online fitness classes." Reframed to "How might we make people who booked actually turn up?"
- Good idea (input 2): cheap to try and likely to lift attendance. Novelty is a bonus, not the main criterion.
- Constraints (input 3): no new app build this quarter; email and SMS available; small budget.
- Count and audience (input 4): 24 ideas; the growth team will test the top three.
- Material (input 5): current no-show rate 35%; reminder email already sent 24 hours before.
- Sensitivity (input 6): none.

**Step 0.** No personal data. Zero redactions.

**Step 2. Diverge (techniques labelled).** A sample of the 24:

- Quantity: SMS reminder two hours before `[quantity]`; calendar invite on booking `[quantity]`.
- Constraints (no budget): a public leaderboard of attendance streaks `[constraint]`.
- Opposite (make it harder to book, not easier): a small refundable deposit returned on attendance `[opposite]`.
- Worst idea (then inverted): "fine people who miss" to "reward people who show" with a loyalty credit `[worst-inverted]`.
- SCAMPER (Combine): pair each booking with a buddy so one person's absence lets the other down `[scamper]`.
- Persona (a rushed parent): a one-tap "I'm coming" confirm that sets a reminder `[persona]`.
- Random stimulus (restaurant): a waitlist that texts someone the spot if the booker drops, so the slot feels scarce `[random]`.

**Step 4. Distinctness check.** Clusters: reminders (7), commitment and stakes (6), social and buddy (4), rewards (4), scarcity (3). Five themes, largest is reminders at 7 of 24, which is 29%, under the 40% cap. The batch passes. Had 18 of 24 been reminder variants, the agent would have gone back and run the opposite and random-stimulus prompts again.

**Step 5. Converge (cheap and likely to work).**

| Idea | Likely lift | Cost to try | Note |
|---|---|---|---|
| SMS two hours before | Medium | Low | Fills the gap after the 24-hour email |
| Refundable deposit | High | Medium | Changes incentives; test with one class first |
| Buddy pairing | Medium | Low | Social pressure; needs opt-in |

Shortlist: SMS two-hour reminder (cheapest test), refundable deposit (highest expected lift, test small), buddy pairing (low cost, social). Parked: leaderboard (fun, but slower to build), loyalty credit (revisit if deposit underperforms).

**Step 6.** Handed to `trade-off-analysis` to choose the first test, and `premortem-analysis` for the deposit idea before it ships, since charging a deposit is harder to reverse.

## Templates

### Session output

```markdown
# Brainstorm: [short name]

How might we: [the framed question]
Good idea = [criteria, for converge only]
Constraints: [fixed things]

## Ideas (by technique)
- [idea] [technique tag]  ([unverified] if it rests on an unchecked claim)
... (target 20-40)

## Theme clusters (distinctness check)
- [theme]: [count]
Largest theme = [n]% (must be under ~40%). Distinct themes = [n] (must be 5+).

## Shortlist (converged)
| Idea | [criterion] | [criterion] | Why / trade-off |

## Parked (not chosen, keep)
- [idea] - [one-line reason]

Hand off to: [trade-off-analysis / decision-frameworks / premortem-analysis]
```

### Diverge prompt for an AI agent

```text
Challenge: How might we [question]?
Do NOT give me the obvious answers. Generate 25 ideas, no filtering, no criticism.
Then run these and label each idea with the technique:
- 5 under a hard constraint: [constraint]
- 5 doing the opposite of the standard approach
- 5 worst possible ideas, each inverted into something usable
- 5 via SCAMPER on this seed idea: [seed]
- 5 from these personas: [list]
Keep wild ideas in. We will judge later, separately.
```

### Brainwriting (group)

```text
6-3-5: 6 people, 3 ideas each, 5 minutes, then pass the sheet right.
Repeat 6 rounds. Silence during writing. Build on what you receive or start fresh.
Result: up to 108 ideas in ~30 minutes. Cluster and converge afterwards.
```

### Starting prompt

```text
Brainstorm with the brainstorming skill.
Challenge (How might we ...): [one sentence, or a topic to shape]
Good idea = [2-3 criteria, converge only]
Constraints / off the table: [...]
How many ideas and who uses them: [default 20-40]
Build on / avoid repeating: [...]
Sensitivity: [none / describe]
Diverge first with techniques, run the distinctness check, then converge. Do not pick the winner for me.
```

## Failure modes and anti-patterns

| # | Failure | How to spot it | What to do instead |
|---|---|---|---|
| 1 | **The single-concept cluster.** Every idea is a variant of the first obvious one, the known default of AI ideation. | The distinctness check fails: one theme holds most of the ideas. | Run the opposite, worst-idea, random-stimulus and distant-persona techniques (step 2), then re-cluster. Variety is the deliverable. |
| 2 | **Judging while generating.** Someone, including the agent, critiques ideas during divergence, so people stop offering bold ones. | "That won't work" appears before the converge phase. | Enforce guardrail 1. No judgement until step 5. Park doubts, do not voice them yet. |
| 3 | **Volume mistaken for range.** A hundred ideas, all alike, treated as a good session. | High count, few themes. | Count themes, not ideas. The distinctness thresholds in step 4 are the test. |
| 4 | **The loud-room effect.** In a group, a few voices dominate and quiet people hold back, so output shrinks. | One or two people produce most ideas out loud. | Switch to brainwriting (step 3). Write in silence, then discuss. |
| 5 | **Converging to the safe idea.** The shortlist quietly drops every wild idea and keeps the obvious one. | The chosen ideas are all the ones you could have named without the session. | Score against the stated criteria, keep a parked list, and make sure at least one non-obvious idea reaches the shortlist for a cheap test. |

## Quality bar

Run every item before handing over. Each is checkable.

1. The challenge is written as a "how might we" question and confirmed with the person.
2. At least four divergence techniques were used, and every idea is labelled with the technique that produced it.
3. The target number of ideas (default 20 to 40) was generated.
4. The distinctness check was run: five or more themes, and no theme over about 40% of the ideas, with the counts shown.
5. Divergence and convergence were kept separate; no idea was criticised before the converge phase.
6. The shortlist of three to five names why each was chosen and what it trades away, and a parked list is kept.
7. Any idea resting on an unchecked claim is marked `[unverified]`.
8. The person, not the agent, makes the final pick; no idea was acted on.
9. No redacted value appears in the output.

## Cost and effort

The agent work is cheap in tokens: generating 20 to 40 ideas and clustering them is a few thousand output tokens. The temptation is to accept the first batch, which is exactly where genericness hides, so the extra divergence rounds are the cost worth paying. For a group, brainwriting costs about 30 minutes and produces far more than a talking session of the same length. The cheap way to go wrong is to ask once, get ten similar ideas, and stop; the distinctness check exists to make that visible before it reaches the person.

## Handoffs to related skills

- `problem-framing`: run first if the question itself is unclear, or if the session shows you are solving the wrong problem.
- `decision-frameworks`: to choose between the shortlisted ideas with the right method.
- `trade-off-analysis`: to weigh a few finalists on multiple criteria.
- `premortem-analysis`: to stress-test the chosen idea before committing, especially if it is costly to reverse.
- `prioritisation`: to order a shortlist of ideas for a backlog.

## Appendix: tool-specific notes

Everything above is tool-agnostic. This appendix is the only place that names a product. Verify each point before relying on it, because products change.

**Running this with an AI agent.** The default failure is a single-concept cluster, so never accept the first list. Ask for quantity with no filtering, then force the named techniques in separate turns, and label each idea. Mixing your own ideas with the model's, and feeding in real examples or research, widens the range further. Keep the generation prompt free of evaluation criteria; judge in a separate prompt. Treat any figure or claim the model offers as `[unverified]` until checked.

**Whiteboards (Miro, FigJam) and brainwriting.** The 6-3-5 method works well with sticky notes or a shared grid: one row per person, one column per round, written in silence before any discussion. Cluster by dragging into themes, which makes the distinctness check visual.

**Claude Agent Skills.** `name` is limited to 64 characters (lowercase letters, numbers, hyphens) and `description` to 1,024 characters. Only the metadata loads at start-up, so the description decides whether the skill fires. Use skills from trusted sources only. Verify limits in the Anthropic documentation.

## Sources

Last verified 24 October 2026 for every source below.

- Alex Osborn's origin of brainstorming and his four rules (defer judgement, go for quantity, welcome wild ideas, combine and improve), via Wikipedia: https://en.wikipedia.org/wiki/Brainstorming. Also the research that interacting groups produce fewer ideas than individuals, reviewed by Diehl and Stroebe (1987, 22 studies), and the causes: production blocking, evaluation apprehension and social loafing.
- 6-3-5 brainwriting method, via Wikipedia: https://en.wikipedia.org/wiki/6-3-5_Brainwriting. Six people, three ideas, five minutes, six rounds, up to 108 ideas in 30 minutes, and why silent writing beats a talking session.
- The finding that generative AI narrows the range of ideas, and that 94% of AI-assisted ideas in a toy-design task shared one core concept (Nature Human Behaviour, 2024), reported by Design Buddy: https://designbuddy.substack.com/p/the-techniques-that-boost-your-ideation. Also constraints, the opposite, remix, 2x2 spectrums, Crazy 8s, SCAMPER, and the chain-of-thought ideation pattern that raised unique ideas by about 27%.
- Design Buddy, brainstorming fundamentals (defer judgement, quantity, wild ideas, build and remix; diverge then converge): https://designbuddy.substack.com/p/before-the-ai-the-brainstorming-fundamentals.
- SCAMPER (Bob Eberle): Substitute, Combine, Adapt, Modify, Put to another use, Eliminate, Reverse, via Haaga-Helia: https://www.haaga-helia.fi/sites/default/files/file/2020-11/scamper-lab8.pdf.
- Anthropic, Agent Skills overview: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview. Frontmatter limits, the description's role in triggering, and security advice.
- Existing agent skills reviewed as benchmarks: lyndonkl `brainstorm-diverge-converge` (clean phase separation and bounded counts, but no check against generic ideas), and obra/superpowers `brainstorming`. This skill adds an explicit distinctness check, named divergence techniques and a tool-agnostic core.
