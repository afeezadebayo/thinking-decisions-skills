---
name: trade-off-analysis
description: Helps Claude, Codex or another AI agent compare several options against weighted criteria with a decision matrix, without the false precision that makes scorecards misleading. It gates options on must-haves first, caps and weights the criteria before scoring, scores on an anchored 1 to 5 scale, computes weighted totals, then runs a sensitivity check to see whether the ranking is real or noise. Use it when someone has three or more options and several competing criteria and asks to "compare these options", "score these", "build a decision matrix", "weighted scoring", "pros and cons is not enough", "which vendor/tool/candidate/supplier", or "help me choose between". Do NOT use it for a yes-or-no decision or the overall call (use decision-frameworks), to stress-test one chosen option (use premortem-analysis), or when one criterion clearly dominates and a matrix would add false rigour.
---

# Trade-off Analysis

A decision matrix compares several options against the criteria that matter, weights those criteria, and scores each option so the comparison is explicit rather than a feeling. Used well, it makes trade-offs visible and a choice defensible. Used badly, it dresses a guess in decimals and hides the judgement inside the weights. This skill runs the method and defends it against its own failure modes.

The core warning first: a weighted scorecard can make a hard call look clean on paper, and "the decimals look rigorous; they are theatre" (practitioner critique, 2026). The matrix is an aid to thinking, never the decision-maker. Everything below keeps it honest.

## When to use this, and when not to

Use it when there are three or more real options and several criteria that pull against each other, so no option is obviously best and a simple pros and cons list is not enough. Typical cases: choosing a vendor, tool, supplier, platform, candidate shortlist, location or design, where cost, quality, speed, risk and fit pull in different directions.

Do not use it for:

- A yes-or-no decision, or the overall call about how much process a decision deserves. That is `decision-frameworks`.
- Stress-testing one option that is already chosen. That is `premortem-analysis`.
- A choice where one criterion clearly dominates (for example, anything over budget is out, full stop). Apply that as a gate and decide; a matrix would add false rigour.
- Two options. With two, a direct pros and cons comparison is usually clearer than a matrix.

This skill produces a comparison and a recommendation. It does not give legal, medical or financial advice, and a person makes the final call.

## Inputs the agent must have before starting

Ask for any that are missing rather than inventing them:

1. **The options.** Ideally three or more. If there are fewer than three, say a matrix may be overkill and offer pros and cons instead.
2. **The criteria that matter**, or enough context to propose them. These should be things that differ between options.
3. **Must-haves and constraints.** Hard requirements that an option must meet (budget ceiling, legal, security, a non-negotiable feature).
4. **The decision owner** and the deadline.
5. **Data per option.** What is known for each option on each criterion, and which values are facts versus estimates.

## Workflow

### 1. Confirm a matrix is the right tool

Before building anything, check three things. If there are fewer than three options, stop and use pros and cons. If one criterion dominates every other (the choice is really about one thing), apply it as a gate and decide. If the options are already known to be within a hair of each other, treat it as a close call and decide fast rather than manufacturing a ranking. A matrix is for genuine multi-criteria trade-offs, not for every choice.

### 2. Apply must-have gates first

List the hard pass-or-fail requirements and drop any option that fails one. Do this before scoring. It is the single most important defence against a documented flaw of naive scoring: a stack of minor strengths outweighing a critical weakness. An applicant tracking system that cannot meet your security requirement does not get to win on price. Gate first, score the survivors.

### 3. Choose and cap the criteria

Pick the criteria that differ between the surviving options, and cap the list at five to seven. More than that usually means padding, and padding is where false precision and criteria-gaming creep in. Define each criterion so it is observable, not vague: "integration effort in engineer-days" beats "ease of integration".

### 4. Weight the criteria before you score

Distribute 100 points across the criteria by importance, so the weights sum to 100. Set the weights before scoring the options, and ideally before looking closely at any option, so you are not reverse-engineering the weights to favour one you already like. Write down why the top one or two criteria carry the most weight.

### 5. Score on an anchored 1 to 5 scale

Score each surviving option on each criterion from 1 to 5, using whole numbers only. No decimals: a 7.4 implies a precision you do not have. For each criterion, anchor what 1 and 5 mean before scoring, for example cost: 5 = under 10k, 3 = 10 to 20k, 1 = over 30k. Anchored rubrics turn a vibe into a defensible judgement and let two people score the same option the same way.

### 6. Compute the weighted totals

For each option, multiply each score by its criterion weight, then sum. The highest total ranks first. Present the full matrix, not just the winner, so the trade-offs are visible.

### Keep cost honest

Cost often does not belong inside the weighted sum. Fold price in as one more criterion and a cheap but weak option can win on points, while a dearer, clearly better option loses. For a big-ticket choice, score only the benefits in the matrix, then set each option's benefit score against its cost separately, as value for money. Present both, the benefit ranking and the cost, so the owner can judge whether the stronger option is worth the premium. Keep cost inside the matrix only when the options are close in price and cost is just one trade-off among several. The same logic applies to effort and risk: a single dominating, hard-to-weigh factor is often clearer kept beside the matrix than buried inside it.

### 7. Run the sensitivity check

This is the step that separates an honest matrix from theatre. Ask: would a small, defensible change in the weights or a one-point change in a close score flip the ranking? If the top two options are within about 10% of each other, the matrix is telling you it is a tie, not that one is better. In that case, do not pretend the decimals decide it. Break the tie on something the matrix does not capture well: reversibility, cost of being wrong, strategic fit or gut. A sensitivity study also shows how much a judgement would have to change for a lower-ranked option to win, which tells you how robust the result is (Pugh method).

### 8. Sanity-check against judgement

If the winning option feels wrong, do not override the matrix silently and do not blindly obey it. A result that clashes with informed intuition usually means a criterion is missing or mis-weighted. Interrogate the matrix, fix it, and re-run. The matrix exists to improve judgement, not to replace it.

### 9. Record and recommend

Present the matrix, the recommended option, the single most important reason it wins, what would change the result, and which values were estimates. Hand the decision to the owner. For an irreversible commitment, pass the chosen option to `premortem-analysis` before it is locked in.

## Worked example

**Decision:** Choose a CRM for a 20-person sales team, four options shortlisted.

**Gate (step 2):** must support single sign-on and export all data. Option D cannot export, so it is dropped before scoring. Three options remain.

**Criteria and weights (steps 3 to 4):** fit for the sales workflow (30), total cost over three years (25), integration effort (20), reporting (15), support quality (10). Weights sum to 100, set before scoring.

**Anchored scoring (step 5), 1 to 5:**

| Criterion (weight) | Option A | Option B | Option C |
| --- | --- | --- | --- |
| Workflow fit (30) | 5 | 4 | 3 |
| Cost over 3 years (25) | 1 | 4 | 5 |
| Integration effort (20) | 2 | 4 | 4 |
| Reporting (15) | 3 | 3 | 4 |
| Support (10) | 3 | 4 | 3 |

**Weighted totals (step 6):** A = 290, B = 385, C = 385 (out of 500).

**Sensitivity (step 7):** B and C tie at 385, with A well behind at 290. Because B and C are level, the matrix cannot separate them, though a one-point change on cost or fit would. The matrix does not decide between B and C.

**Tie-break and recommendation (steps 8 to 9):** B and C tie, so break it on reversibility: Option C is month-to-month, Option B needs a two-year contract. The agent recommends C as the more reversible choice at a near-identical score, notes cost figures are vendor estimates, and hands C to a premortem before signing. The owner approves.

## Templates to use verbatim

### Decision matrix

```
Must-have gates (pass/fail): ______   [drop any option that fails]

| Criterion (weight /100) | Option A | Option B | Option C |
| criterion 1 (  )        |   1-5    |   1-5    |   1-5    |
| criterion 2 (  )        |          |          |          |
| ...                     |          |          |          |
| Weighted total (/500)   |   sum    |   sum    |   sum    |
```

### Anchored scoring rubric (per criterion)

```
Criterion: ______
5 = ______ (clearly best)
3 = ______ (acceptable)
1 = ______ (clearly worst)
Values are facts / estimates: ______
```

### Sensitivity check

```
Top two options and their totals: ______
Gap between them (as % of scale): ______
If < ~10%: treat as a tie, break on [reversibility / cost of error / fit].
One-point score change or 5-point weight change that flips the result: ______
```

## Failure modes and anti-patterns

1. **False precision.** Options scored to one decimal, weighted to produce a 78.4 versus 76.9, and the 1.5-point gap treated as decisive. Spot it when scores have decimals or the winner is within a few percent. Fix: whole-number 1 to 5 scores, anchored rubrics, and a sensitivity check that calls close results ties.
2. **Criteria and weight gaming.** The criteria or weights are chosen after the options, to justify a pre-selected favourite. Spot it when the weights were set once the options were on the table. Fix: set criteria and weights before scoring, write down why, and have a second person sanity-check them.
3. **Too many criteria.** Ten or fifteen criteria, most of them minor, which dilutes the ones that matter and lets trivia accumulate into a false winner. Spot it when the list runs past seven. Fix: cap at five to seven, and fold or drop the rest.
4. **Ignoring must-haves.** A minor-criteria stack lets an option that fails a hard requirement win on points. Spot it when the winner cannot actually do something non-negotiable. Fix: gate on must-haves before scoring, so failing options never enter the matrix.
5. **The matrix as the decision.** The total is treated as the answer and no one checks it against judgement or the cost of being wrong. Spot it when the recommendation is "the spreadsheet says B". Fix: sanity-check the winner, run the sensitivity test, and have a person make the call the matrix informs.

## Quality bar

Before handing over, confirm:

- A matrix was the right tool (three or more options, competing criteria).
- Must-have gates were applied before scoring, and failing options were dropped.
- Criteria are capped at five to seven and each is observable, not vague.
- Weights sum to 100 and were set before scoring.
- Scores are whole numbers on an anchored 1 to 5 scale, with 1 and 5 defined per criterion.
- The full matrix is shown, not just the winner.
- A sensitivity check was run, and a result within about 10% is called a tie and broken on something else.
- Estimated values are labelled, and the winner was sanity-checked against judgement.
- A person makes the final call; an irreversible choice goes to a premortem first.

## Guardrails

- **The matrix informs, a human decides.** Present the ranking and the reason; the owner chooses. Never treat the weighted total as the decision, and never act on it (buy, sign, hire) without explicit human sign-off.
- **No false precision.** Whole-number scores, estimates labelled and given as ranges, and close results called ties. Do not invent data to fill a cell; a missing value is marked unknown, not guessed.
- **Not professional advice.** For choices with legal, medical, financial or employment consequences, say the comparison is not professional advice and must be reviewed by a qualified professional.
- **PII and commercial data.** Vendor quotes, candidate details and customer data stay in the user's workspace. Do not log them or send them to third parties, and keep them in the saved matrix only if the user asks.
- **Scope boundary.** This skill compares options. It does not frame the overall decision (`decision-frameworks`) or stress-test the winner (`premortem-analysis`).
- **Honest uncertainty.** If the data is too thin to score fairly, say so and recommend gathering the one or two inputs that would settle it, rather than producing a confident-looking matrix on guesses.

## Appendix: pairwise comparison, spreadsheets and agents

This core is tool-agnostic. The notes below are for AI agents and advanced methods, separate from the method above.

- **Install** as `trade-off-analysis/SKILL.md`. It loads on wording like "compare these options", "decision matrix" or "weighted scoring".
- **When weights are hard to set directly**, use pairwise comparison: compare criteria two at a time to derive weights, as in the Analytic Hierarchy Process (AHP). AHP also offers a consistency check: its consistency ratio should be below about 0.10, or the judgements are too contradictory to trust (Saaty; treat the exact threshold as a convention and verify before relying on it). AHP is heavier and can suffer rank reversal when an option is added, so prefer simple weighted scoring unless the extra rigour is justified.
- **Spreadsheets.** The matrix maps directly to a sheet: criteria in rows, options in columns, a weight column, and a SUMPRODUCT of weights and scores per option. Keep scores as whole numbers and add a row that shows each gap as a percentage of the scale for the sensitivity check.
- **No autonomous action.** Even with tools connected, the skill outputs a matrix and a recommendation. It does not purchase, sign or commit.
- **Cost.** The method is cheap. If scoring needs large research runs to gather data per option, say the expected cost first and offer to score only the top criteria.

## Sources

- Stuart Pugh, "Concept selection: a method that works," 1981, and the decision-matrix (Pugh) method (criteria, reference option, sensitivity study, documented limits). Last verified 24 October 2026.
- Thomas L. Saaty, the Analytic Hierarchy Process (pairwise comparison, 1 to 9 scale, consistency ratio around 0.10, rank-reversal criticism). Last verified 24 October 2026.
- Practitioner critique of weighted scoring and false precision ("the decimals look rigorous; they are theatre"), 2026, and the Wikipedia decision-matrix method entry on minor-criteria stacking. Last verified 24 October 2026.
- Chip Heath and Dan Heath, "Decisive" (2013), on widening options and testing assumptions before comparing. Last verified 24 October 2026.

---
Use, adapt and share this skill under CC BY 4.0, with credit to Afeez Adebayo (https://afeezadebayo.com) and this page.
