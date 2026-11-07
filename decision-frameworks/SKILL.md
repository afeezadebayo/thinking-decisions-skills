---
name: decision-frameworks
description: Helps Claude, Codex or another AI agent run a decision properly, from first framing to a documented call. It frames the real question, classifies the decision by reversibility, stakes and urgency, then picks the lightest method that fits (just decide, pros and cons, a weighted trade-off, or role-based frameworks such as RAPID and DACI), sets criteria before options, matches rigour to the stakes and writes a decision record with a revisit date. Use it when someone says "help me decide", "which option should we pick", "I'm stuck between X and Y", "how do we make this call", "who owns this decision", "should we do this", or shares a choice between vendors, tools, candidates, plans, strategies or trade-offs. Do NOT use it to stress-test a decision already made (use premortem-analysis), to score many options on a scorecard (use trade-off-analysis), to record a decision already taken (use decision-records), or to give regulated legal, medical or financial advice.
---

# Decision-Making Frameworks

Run a decision well, from the first framing to a written call that someone owns. This skill does not make the decision for the user. It makes sure the right question is being answered, the method matches the stakes, and the reasoning is written down so the decision can be reviewed later.

Most poor decisions are not poor choices. They are good choices to the wrong question, or the right question answered with the wrong amount of effort: a reversible call agonised over for a week, or a one-way door walked through in an afternoon. This skill fixes both.

## When to use this, and when not to

Use it when a person or team faces a choice and wants help making it: picking between vendors, tools, candidates, plans or strategies; deciding whether to start, stop or continue something; or working out who should even make the call and how much process it deserves.

Do not use it for these neighbours, which have their own skills:

- To pressure-test a direction that is already chosen, imagine how it could fail and build mitigations: use `premortem-analysis`.
- To compare several options against weighted criteria on a scorecard: use `trade-off-analysis`. This skill will point you there when a weighted comparison is the right method.
- To write up a decision that has already been made, in a durable record: use `decision-records`.
- To rank a backlog of tasks by priority: use `prioritisation`.

Do not use it to give legal, medical, financial or regulated professional advice. The skill can structure the thinking around such a decision, but it must say plainly that the output is not professional advice and that a qualified professional should review anything with legal, medical, financial or employment consequences.

## Inputs the agent must have before starting

Gather these before running the workflow. If any are missing, ask for them in one short message rather than guessing.

1. **The decision.** What is being decided, in the user's own words. If it arrives as a yes or no ("should we do X"), expect to reframe it.
2. **The options**, if any exist yet. "None yet" is a valid answer and changes the workflow.
3. **The owner.** Who actually makes the final call, and who must be consulted or informed.
4. **The deadline.** When the decision must be made, and the cost of deciding late.
5. **What good looks like.** The outcome the user wants, and how they would know it worked.
6. **Constraints.** Budget, legal or policy limits, non-negotiables, resources.
7. **Reversibility.** How hard and costly it would be to undo the choice later.
8. **What has already been tried or ruled out,** so the skill does not re-open settled ground.

If the user cannot answer 3, 4 or 7, ask for those first. Ownership, deadline and reversibility change the whole approach, and a decision with no named owner tends not to get made.

## Workflow

Run these steps in order. Each step has a rule, not a suggestion.

### 1. Frame the real question

Write the decision as one clear question. If the user gave a yes or no, widen it: "Should we hire a second designer?" becomes "What is the best way to clear the design backlog this quarter?" A yes or no question hides the alternatives and invites a biased search for reasons to agree.

Apply two tests:

- **The single-question test.** If the framing contains two decisions, split them and decide the upstream one first. "Should we move to tool X and migrate this quarter" is two questions.
- **The real-choice test.** If only one option is actually viable, there is no decision to make. Say so and stop. Running a framework over a foregone conclusion wastes time and manufactures false confidence.

Where the choice is tangled, find the decisive question: the one that, once answered, settles most of the rest. State it back to the user and confirm it before going further.

### 2. Classify the decision

Score the decision on three axes. This is the step most people skip, and it determines everything that follows.

- **Reversibility.** Ask: "What would it cost, in time, money and reputation, to undo this within about six months?" If the answer is "little", it is a **two-way door** (reversible). If "a lot" or "we cannot", it is a **one-way door** (irreversible or nearly so). Source: Bezos, Amazon 2015 shareholder letter.
- **Stakes.** Low, medium or high, by the size of the effect on money, people and strategy if it goes wrong.
- **Urgency.** How soon it must be decided, and the cost of delay.

### 3. Match the rigour to the decision

Use this routing rule. Pick the lightest row that fits, never a heavier one.

| Reversibility and stakes | Method | Time to spend |
|---|---|---|
| Two-way door, low stakes | Just decide now, or delegate to one person. Do not build a framework. | Minutes |
| Two-way door, medium stakes | Quick pros and cons, or run a cheap reversible test or pilot, then set a revisit date. | An hour or less |
| One-way door, or high stakes, single owner | Structured: set criteria, list real options, run `trade-off-analysis` if options compete on several criteria, then `premortem-analysis` before committing. | Hours to days |
| Many stakeholders or cross-functional | Assign decision roles with RAPID or DACI so one person decides, then apply the structured method above. | Days |

The common error runs one way: applying a heavy process to a two-way door. Bezos named this directly, warning that as organisations grow they tend to use the slow, Type 1 process on reversible Type 2 decisions, which produces "slowness, unthoughtful risk aversion, failure to experiment." If the decision is reversible and low-stakes, the correct output of this skill is "decide it now and move on."

### 4. Set the criteria before you see the options

Write down what a good option must do, and what would make one better, before comparing specific options. Deciding the criteria after seeing the options lets people reverse-engineer the criteria to favour the option they already like.

Separate two kinds:

- **Must-haves (gates).** A hard pass or fail. An option that fails a must-have is out, regardless of how well it scores elsewhere. This prevents a stack of minor strengths from outweighing a critical weakness, a documented flaw of naive scoring (Pugh method criticism).
- **Nice-to-haves (weighted).** Things that make an option better, ranked by how much they matter.

Cap the criteria at five to seven. More than that usually hides padding added to avoid committing.

### 5. Generate real options

Require at least two genuine alternatives. A decision with one option is not a decision. Always include the status quo, "do nothing", as an explicit option, because it has costs and benefits that deserve the same scrutiny.

Widen the set before narrowing it. The Heath brothers' WRAP research found that most decisions are framed too narrowly, as "whether or not" rather than "which of these". Ask: "What would we do if this option disappeared?" and "Is there a way to get the benefits of more than one option?"

### 6. Gather the right amount of information

Take the outside view first. Ask how similar decisions have usually turned out, the base rate, before diving into the specifics of this one. People systematically over-weight the vivid details of their own case and under-weight how the same situation plays out on average (Kahneman, Lovallo and Sibony, HBR 2011).

Decide when you have about 70% of the information you wish you had. Waiting for more past that point usually costs more in delay than it saves in accuracy, especially for reversible decisions. Mark clearly which inputs are facts and which are estimates, and express estimates as ranges, not false-precise single numbers.

### 7. Make the call

- **If the top options are close**, within the margin of your own uncertainty, decide quickly and pick one. Closeness means the cost of choosing "wrong" is small, so the expensive thing is the delay, not the error (Annie Duke).
- **Otherwise**, apply the method chosen in step 3: pros and cons for simple calls, `trade-off-analysis` for multi-criteria comparisons, RAPID or DACI roles where many people are involved.
- **For one-way doors and high-stakes calls**, run `premortem-analysis` before committing. Imagining the decision has already failed surfaces risks that a forward-looking review misses.
- **Run a fast bias check** before finalising. Five questions, from the Kahneman HBR 2011 checklist: Is anyone's self-interest shaping this? Have we only looked for evidence that agrees? Are our numbers anchored to a starting figure no one questioned? Are sunk costs keeping a failing option alive? Is the base case too optimistic?

### 8. Record the decision

Write a short decision record. This is the single most useful habit in decision-making, because it lets you separate a good decision from a lucky outcome later. Capture: the question, the options considered, the call, the single decisive reason, the key assumptions, what would change the decision, the kill criteria and revisit date, and the owner. Hand this to `decision-records` if a durable, searchable record is needed; do not duplicate that skill's storage work here.

### 9. Guardrail before any action

Making the decision is not the same as executing it. If carrying out the decision means an irreversible action, sending, publishing, paying, hiring, firing, deleting, booking, or any bulk change, stop and present the recommendation for explicit human confirmation. Default to a draft or a recommendation, never to acting on the user's behalf. See Guardrails below.

## Worked example

**User request:** "Should we switch our team from Tool A to Tool B for project management?"

**Step 1, frame.** Reframed from yes or no to: "What is the best way to run project tracking for the team over the next year?" Confirmed with the user. The real-choice test passes: staying on Tool A, moving to Tool B, and moving to Tool C are all live.

**Step 2, classify.** Reversibility: moving tools means migrating data and retraining ten people, and moving back would repeat that cost, so it leans one-way, at least over six months. Stakes: medium, it affects daily work but not revenue. Urgency: the Tool A contract renews in eight weeks.

**Step 3, rigour.** One-way-ish and medium stakes, single owner (the team lead). Route: structured method with criteria, a trade-off comparison, and a premortem before committing. Not a full cross-functional RAPID, because one person owns it.

**Step 4, criteria.** Must-haves: single sign-on and data export are gates (two options that cannot export are out). Weighted nice-to-haves: migration effort, monthly cost, reporting, and how much the team already likes it.

**Step 5, options.** Tool A (status quo), Tool B, Tool C. A fourth idea, "keep Tool A but add a reporting add-on", emerges from widening and is kept.

**Step 6, information.** Base rate first: most tool migrations overrun their time estimate, so the migration-effort estimate is widened to a range of two to five weeks. The team's dislike of Tool A is noted as an opinion, not a fact.

**Step 7, call.** The agent hands the four options to `trade-off-analysis`, which ranks "Tool A plus reporting add-on" and "Tool B" within a few points of each other. Because they are close and one (the add-on) is far cheaper and reversible, the agent recommends the add-on as a reversible test for one quarter, with a decision to migrate deferred. A quick premortem flags "the add-on does not fix the real complaint" as the top risk.

**Step 8, record.** Decision: trial the reporting add-on this quarter. Decisive reason: it is reversible and tests the actual complaint cheaply. Kill criterion: if reporting satisfaction has not improved by the end of the quarter, revisit Tool B. Owner: the team lead. Revisit date: in 12 weeks.

**Step 9, guardrail.** The agent does not purchase the add-on. It presents the recommendation and the draft record for the team lead to approve.

## Templates to use verbatim

### Decision brief

```
Decision (one question): ______
Owner (one person): ______    Consulted: ______    Informed: ______
Deadline: ______    Cost of deciding late: ______
Reversibility: two-way door / one-way door  (cost to undo in 6 months: ______)
Stakes: low / medium / high
What good looks like: ______
Must-haves (pass/fail gates): ______
Nice-to-haves (weighted): ______
Options (at least 2, include status quo): ______
```

### Classification quick-test

```
1. If this goes wrong, what does it cost to undo within 6 months?
   Little -> two-way door   A lot / cannot -> one-way door
2. Worst realistic downside? -> low / medium / high stakes
3. When must this be decided, and what does waiting cost?
-> Use the routing table. Pick the lightest method that fits.
```

### Decision record

```
Date: ______    Owner: ______
Question decided: ______
Options considered: ______
Decision: ______
Single decisive reason: ______
Key assumptions (fact vs estimate): ______
What would change this decision: ______
Kill criteria / revisit date: ______
```

### Framework-selection cheat

- Reversible and small: decide now or delegate. No framework.
- Reversible and medium: pros and cons, or run a cheap test. Set a revisit date.
- Irreversible or high stakes: criteria, then `trade-off-analysis`, then `premortem-analysis`.
- Many stakeholders: assign RAPID or DACI roles so one person decides.

## Failure modes and anti-patterns

1. **Yes-or-no framing.** The decision is posed as "should we do X", which hides alternatives and biases the search towards agreement. Spot it when there is only one option on the table. Fix: reframe to "which of these", and force at least two options plus the status quo.
2. **Heavy process on a two-way door.** Weeks of analysis on a reversible, low-stakes call. Spot it when the time being spent dwarfs the cost of being wrong. Fix: classify first; if reversible and low-stakes, decide now and move on.
3. **Resulting.** Judging the quality of a past decision purely by how it turned out, good or bad. Spot it in phrases like "that was a terrible decision" said only because the outcome was bad. Fix: judge the decision by what was known at the time and whether the process was sound; a good decision can still lose (Annie Duke).
4. **Analysis paralysis by criteria creep.** New criteria and more research keep appearing, and the decision never lands. Spot it when the criteria list grows past seven or the deadline slips with no new real information. Fix: freeze the criteria, decide at about 70% information, and set a deadline for the decision itself, not just the analysis.
5. **Consensus with no owner.** The group seeks total agreement and no single person is accountable, so the decision waters down or stalls. Spot it when no one can name the decider. Fix: assign one Approver or Decider (DACI or RAPID); everyone is heard, one person calls it.

## Quality bar

Before handing over, confirm every item:

- The decision is written as one clear question, and the real-choice test passed.
- There are at least two genuine options, including the status quo.
- Criteria were set before options were compared, with must-haves separated from nice-to-haves.
- Reversibility, stakes and urgency are classified, and the method matches the routing table.
- One person is named as the owner or decider.
- The call names a single decisive reason, not a long list of weak ones.
- Assumptions are marked as fact or estimate, and estimates are ranges.
- A bias check was run.
- The record includes kill criteria and a revisit date.
- No irreversible action has been taken without explicit human sign-off.

## Guardrails

- **Irreversible actions need a human.** Sending, publishing, paying, hiring, firing, deleting, booking or any bulk change requires explicit human confirmation. Default to a draft or recommendation. Never execute on the user's behalf.
- **Never fabricate numbers.** Every figure, base rate, cost or probability carries a source and a date, or is labelled an estimate and given as a range. Do not invent benchmarks to fill a cell.
- **Not professional advice.** For decisions with legal, medical, financial or employment consequences, state that the output is not professional advice and must be reviewed by a qualified professional. Do not recommend a specific regulated course of action as if it were advice.
- **PII and confidential inputs.** Decisions often involve salaries, candidate details, customer data or commercial terms. Do not store, log or send these anywhere beyond the user's own workspace, and do not paste them into third-party tools. Keep sensitive inputs in the decision record only if the user asks.
- **Scope boundary.** This skill structures and records a decision. It will not pretend certainty it does not have, will not rank many options on a scorecard (that is `trade-off-analysis`), and will not take the action the decision implies.
- **No duplication.** For failure stress-testing use `premortem-analysis`; for weighted scoring use `trade-off-analysis`; for durable records use `decision-records`. Cross-link, do not re-implement.

## Appendix: using this in Claude, Cursor and other agents

This core is tool-agnostic. The notes below are specific to AI agents and are separate from the method above.

- **Install** as `decision-frameworks/SKILL.md`. It loads when a user asks for help deciding something.
- **Running order with sibling skills.** This skill is the hub. It calls `trade-off-analysis` at step 7 for multi-criteria comparisons and `premortem-analysis` at step 7 for one-way doors, then `decision-records` at step 8 for storage. If those skills are not installed, run the inline templates above instead.
- **Writing the record.** Write the decision record to wherever the user keeps decisions: a Markdown file, a doc, a Confluence or Notion page, or a project ticket. Ask before creating a page in a shared workspace.
- **No autonomous execution.** Even with tools connected (email, calendar, payments, repositories), this skill produces a recommendation and a record. It does not act on the decision. Executing is a separate, human-approved step.
- **Cost.** The method itself is cheap. If a decision triggers large research runs or many model calls, tell the user the expected cost first and offer the lighter path from the routing table.

## Sources

- Jeff Bezos, Amazon 2015 Letter to Shareholders (Type 1 and Type 2, one-way and two-way doors). Last verified 24 October 2026.
- Daniel Kahneman, Dan Lovallo and Olivier Sibony, "Before You Make That Big Decision," Harvard Business Review, June 2011 (12-question quality-control checklist, outside view). Last verified 24 October 2026.
- Annie Duke, "Thinking in Bets" (2018) and "How to Decide" (2020) (resulting, decisions as bets, deciding fast when options are close). Last verified 24 October 2026.
- Stuart Pugh, "Concept selection: a method that works," 1981, and the decision-matrix method (must-have gates, minor-criteria stacking). Last verified 24 October 2026.
- Bain & Company, RAPID decision framework; Atlassian Team Playbook, DACI play (role-based decision-making, one decider). Last verified 24 October 2026.
- Chip Heath and Dan Heath, "Decisive" (2013), WRAP process (widen options, avoid narrow framing). Last verified 24 October 2026.

---
Use, adapt and share this skill under CC BY 4.0, with credit to Afeez Adebayo (https://afeezadebayo.com) and this page.
