---
name: premortem-analysis
description: Helps Claude, Codex or another AI agent run a premortem on a plan before it is committed: imagine the plan has already failed, work backwards to the causes, triage them by likelihood and impact, and attach prevention, mitigation, early-warning signs, owners and measurable kill criteria to the ones that matter. Use it before a launch, migration, hire, campaign, big spend or any one-way-door decision, or when someone asks "what could go wrong", "how might this fail", "stress-test this plan", "run a premortem", "pre-mortem" or "red team this". Do NOT use it to choose between options (use decision-frameworks or trade-off-analysis), to review something that has already finished (that is a post-mortem or lessons-learned), or to stall a reversible, low-stakes decision that should just be made.
---

# Premortem and Decision Risk

A premortem is the opposite of a post-mortem. Instead of explaining a failure after it happens, you assume the failure has already happened and work backwards to find the causes while you can still prevent them. This skill runs that exercise on a plan before it is committed, then turns the raw list of fears into owned risks with triggers and kill criteria.

It works because of a quirk of how people reason. Asking "why might this fail?" invites loyal, hedged answers. Telling people "it is a year from now and this failed completely, explain how" removes the hedging. In a classic study, treating a future event as already certain, called prospective hindsight, raised the number of reasons people could generate for an outcome by about 30% (Mitchell, Russo and Pennington, 1989, cited in Klein, HBR 2007).

## When to use this, and when not to

Use it before you commit to something that is hard to undo or expensive to get wrong: a product launch, a tool migration, a reorganisation, a senior hire, a large campaign or spend, a public commitment, or any one-way-door decision. The best moment is after the plan exists but before money, people or reputation are locked in.

Do not use it for:

- Choosing between options. That is `decision-frameworks` for the overall call, or `trade-off-analysis` for a weighted comparison. A premortem stress-tests one chosen direction; it does not pick the direction.
- Reviewing something that has already finished. That is a post-mortem or a lessons-learned review.
- Stalling a reversible, low-stakes decision. If the choice is a two-way door, the cost of being wrong is small, so skip the premortem and decide. Running heavy risk analysis on a cheap, reversible call is its own failure mode.

This skill structures and records risk. It does not give legal, medical, financial or safety assurances, and it says so for any plan with those consequences.

## Inputs the agent must have before starting

Ask for any that are missing rather than guessing:

1. **The plan or decision** being stress-tested, in enough detail that failure causes can be specific.
2. **Success criteria.** What "it worked" means, and by when. Without this, failure is undefined.
3. **The timeframe** to jump to for the failure scenario (for example, six months after launch).
4. **Reversibility and stakes.** Used to gate the depth, and to decide whether a premortem is warranted at all.
5. **Who is involved**, if this is a team exercise, or whether it is a solo run with one person and the agent.
6. **The stage.** The plan must still be changeable. If it cannot change, say so, because a premortem on a locked plan is theatre.

## Workflow

### 1. Gate the premortem

Confirm this decision earns one. Run it when the decision is a one-way door, or high-stakes, or both, and the plan can still change. If the decision is reversible and low-stakes, say that a premortem is not needed and that the decision should simply be made or tested cheaply. Do not pad a small, reversible call with risk theatre.

### 2. State the plan and success criteria

Write the plan in two or three sentences, and the success criteria as something measurable. "Launch the new pricing page" is not enough. "Launch the new pricing page by 30 November, lifting trial-to-paid conversion from its current rate without raising refund requests" gives the premortem something to fail against.

### 3. Jump to the failure

Set the scene as fact, not possibility: "It is [date]. We shipped this, and it failed completely. The outcome was [a vivid, specific disaster]." State it in the past tense. The vividness matters; "the migration corrupted customer data and we lost three enterprise accounts" surfaces more than "something went wrong."

### 4. Generate the failure causes

Generate at least 8 to 12 plausible causes, and more for a big plan. Do not filter for likelihood yet; the point of this step is to get everything on the table, including the uncomfortable. Spread causes across categories so the list is not all of one kind:

- **Execution:** the work itself slipped, broke or was done badly.
- **External:** market, competitor, regulation, supplier, timing.
- **People:** a key person left, teams misaligned, no owner, skills missing.
- **Technical:** systems, data, integrations, scale, security.
- **Assumptions:** a belief the plan depended on turned out to be wrong.
- **Financial and legal:** cost overran, budget pulled, a compliance or contract problem.

In a group, have people write causes silently for 5 to 10 minutes first, then share round-robin with no debate, so the loudest voice does not set the agenda and juniors raise what seniors miss (Klein, HBR 2007). Solo, with one agent, brainstorm widely across the categories before judging any.

### 5. Add the outside view

Before scoring, ask how plans like this one usually fail. Reference-class failure, the base rate, catches risks the team is too close to see. Most migrations overrun; most launches miss their first forecast; most acquisitions underdeliver on synergy. Add the typical failure of the reference class to the list even if no one named it from the inside.

### 6. Triage the causes

Score each cause on likelihood and impact (high, medium, low), then sort them into three groups, after Shreyas Doshi's risk triage:

- **Tigers:** real threats that can kill the plan. High impact, credible likelihood. These get full treatment.
- **Paper tigers:** frightening but unlikely or low-impact. Name them, then set them aside, so they stop absorbing attention.
- **Elephants:** large risks everyone can see but no one wants to say out loud, often about people, politics or a shaky core assumption. Name these explicitly; they are the ones premortems exist to surface.

Keep the Tigers list short, five to eight, each with an owner. A premortem that produces forty unranked risks and acts on none has failed.

### 7. Respond to each top risk

For every Tiger and every named Elephant, write:

- **Prevention:** how to reduce the likelihood it happens.
- **Mitigation:** how to reduce the damage if it happens anyway.
- **Early-warning signs:** the observable signal that this risk is materialising.
- **Owner:** one named person who watches it.
- **Contingency and trigger:** the fallback, and the specific condition that sets it off.

### 8. Set kill criteria

Agree, in advance, the measurable conditions under which the plan stops or pivots. A kill criterion is a number and a date, not a feeling: "if paid conversion has not reached X by [date], we revert." Pre-committing to kill criteria is the strongest defence against the sunk-cost trap, where a failing plan survives because of what has already been spent on it. Write them before launch, while judgement is still cool.

### 9. Give a revised go, no-go or adjust

Close with a clear recommendation: proceed, proceed with the changes above, delay, or do not proceed, and what would raise confidence. A premortem that does not change the plan or the confidence in it was not worth running. Equally, a premortem is not a reason to never act: its job is to make a risk-aware commitment, not to feed loss aversion into permanent delay.

### 10. Log and schedule a review

Move the Tigers, owners, triggers and kill criteria into a risk register or RAID log, and schedule a short check at the plan's midpoint to see which early-warning signs have appeared. The human owner makes and commits the go or no-go call; the skill produces the analysis and the register, not the commitment.

## Worked example

**Plan:** Migrate the support team from the current help-desk tool to a new one, live in six weeks.

**Success criteria:** All tickets and macros migrated, first-response time no worse than today within two weeks of go-live, no data loss.

**Failure jump:** "It is three months later. The migration was a disaster. First-response time doubled, two macros silently dropped, and the team quietly kept using the old tool in parallel."

**Causes (sample):** macros did not map one-to-one (technical); the team was not trained before go-live (people); the import underestimated attachment volume (assumptions); the vendor's API rate-limited the bulk import (external); the project had no single owner across support and IT (people); go-live clashed with the busiest week of the quarter (execution).

**Outside view:** most tool migrations overrun their schedule and lose some automation, so the macro and timeline risks move up.

**Triage:** Tigers: macro mapping, no single owner, go-live timing. Paper tiger: total data loss (the import is reversible and backed up). Elephant: the team prefers the old tool and may not adopt the new one, which no one had said out loud.

**Response (one Tiger shown):** Macro mapping. Prevention: audit all macros and map them two weeks early. Mitigation: keep the old tool read-only for 30 days. Early-warning sign: more than 5% of macros fail a dry-run import. Owner: support operations lead. Trigger and contingency: if the dry run fails, slip go-live by one week rather than ship broken.

**Kill criterion:** if first-response time is still worse than baseline four weeks after go-live, revert to the old tool and re-plan.

**Recommendation:** proceed, but move go-live out of the busy week, name one cross-functional owner, and run the macro dry-run first. The human lead approves the revised plan; the skill does not reschedule anything itself.

## Templates to use verbatim

### Premortem prompt

```
It is [date, after the plan should have succeeded].
We went ahead with [plan]. It failed completely.
The outcome: [write the specific, vivid disaster].
Working backwards, list every reason this could have happened.
Do not filter for likelihood yet. Include the uncomfortable ones.
```

### Failure-cause capture

```
| Category | Failure cause | How it played out |
| Execution / External / People / Technical / Assumptions / Financial-legal | ... | ... |
```

### Risk triage and response

```
| Risk | Likelihood | Impact | Tiger / Paper tiger / Elephant | Owner |
| ...  | H/M/L      | H/M/L  | ...                            | ...   |

For each Tiger and Elephant:
- Prevention: ______
- Mitigation: ______
- Early-warning sign: ______
- Contingency + trigger: ______
```

### Kill criteria

```
We will stop or pivot this plan if:
- [measurable condition] by [date]
- [measurable condition] by [date]
Owner of the kill decision: ______
Midpoint review date: ______
```

## Failure modes and anti-patterns

1. **Run too late.** The premortem happens after the plan is locked, so nothing can change and it becomes a ritual. Spot it when no finding could alter the plan. Fix: run it while the plan is still editable, before commitment.
2. **Vague plan, vague causes.** A fuzzy plan produces causes that all reduce to "it was not well defined." Spot it when every cause is a planning complaint. Fix: sharpen the plan and success criteria first (step 2), then re-run.
3. **Causes but no action.** The session produces a long list of fears and acts on none. Spot it when there are more than ten unowned risks. Fix: triage to five to eight Tigers, each with an owner and a response.
4. **Grudges and blame.** The exercise turns into relitigating past projects or blaming people. Spot it when causes are about who, not what. Fix: keep it about how this plan could fail, and thank people who raise hard risks.
5. **Premortem as a veto.** The risks become an excuse to never act, feeding loss aversion. Spot it when every option is talked out of existence. Fix: the output is a risk-aware go or no-go, not permanent delay; pair each Tiger with a response, not a reason to stop.

## Quality bar

Before handing over, confirm:

- A premortem was warranted (one-way door or high stakes, and the plan can still change).
- The plan has a measurable success criterion and a dated failure scenario.
- At least 8 to 12 causes were generated across multiple categories, including an outside-view risk.
- Causes are triaged into Tigers, paper tigers and elephants, with the elephant named.
- Each Tiger has prevention, mitigation, an early-warning sign, an owner and a trigger.
- Kill criteria are measurable, dated and written before commitment.
- The output ends on a clear go, no-go or adjust, and a risk register with a review date.
- The human owns the final go or no-go; the skill has not committed anything.

## Guardrails

- **The human commits.** The premortem informs a go or no-go, but a person makes and owns the commitment. The skill does not launch, buy, migrate, hire or schedule anything. Any irreversible action waits for explicit human sign-off.
- **Never fabricate risk numbers.** Base rates, likelihoods and costs carry a source and a date, or are labelled estimates and given as ranges. Do not invent a probability to fill a cell.
- **Not professional advice.** For plans with legal, medical, financial, safety or employment consequences, say plainly that the analysis is not professional advice and must be reviewed by a qualified professional.
- **PII and confidential inputs.** Plans often name people, customers, salaries or commercial terms. Do not store, log or send these beyond the user's own workspace, and keep them in the risk register only if the user asks.
- **Scope boundary.** This skill stress-tests one chosen plan. It does not choose between options (`decision-frameworks`, `trade-off-analysis`) and it is not a post-mortem of finished work.
- **Not a licence for inaction.** Flagging risk is not the same as advising against the plan. Pair risks with responses and a confidence call, so the premortem improves the decision rather than freezing it.

## Appendix: using this in Claude, Cursor and other agents

This core is tool-agnostic. The notes below are for AI agents and are separate from the method.

- **Install** as `premortem-analysis/SKILL.md`. It loads on wording like "what could go wrong", "stress-test this", "premortem" or "red team this".
- **Solo and async runs.** With one user and no group, the agent plays the round-robin itself: it generates causes widely across every category before judging any, then triages. For a team, it can produce the silent-write prompt and collate the shared list.
- **Where this sits.** `decision-frameworks` calls this skill at the point of committing to a one-way door. Use `trade-off-analysis` first if you are still choosing between options; use this once a direction is chosen.
- **Writing the register.** Write the risk register to wherever the team tracks risks: a Markdown table, a sheet, a RAID log, or a ticket. Ask before creating anything in a shared workspace.
- **No autonomous action.** Even with tools connected, the skill produces analysis and a register. It does not act on the plan.
- **Cost.** The exercise is cheap. If stress-testing triggers large research runs to establish base rates, say the expected cost first and offer a lighter version.

## Sources

- Gary Klein, "Performing a Project Premortem," Harvard Business Review, September 2007 (the method, facilitation, prospective hindsight). Last verified 24 October 2026.
- Deborah J. Mitchell, J. Edward Russo and Nancy Pennington, "Back to the future: Temporal perspective in the explanation of events," Journal of Behavioral Decision Making, 1989 (prospective hindsight raised reasons generated by about 30%). Last verified 24 October 2026.
- Daniel Kahneman, Dan Lovallo and Olivier Sibony, "Before You Make That Big Decision," Harvard Business Review, June 2011 (premortem as the worst-case check; the outside view). Last verified 24 October 2026.
- Shreyas Doshi, writing on premortems and risk triage (Tigers, paper tigers and elephants). Last verified 24 October 2026.
- Annie Duke, "Thinking in Bets" (2018) and "Quit" (2022) (kill criteria, pre-committing to stop conditions, the sunk-cost trap). Last verified 24 October 2026.

---
Use, adapt and share this skill under CC BY 4.0, with credit to Afeez Adebayo (https://afeezadebayo.com) and this page.
