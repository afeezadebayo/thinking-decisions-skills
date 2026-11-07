---
name: problem-framing
description: "Defines the right problem before anyone solves it. Takes a problem someone has stated (a brief, a goal, a complaint, a 'why is X happening' question, a request to fix or improve something) and tests whether it is framed well, then produces two to four candidate frames, a chosen problem statement and success criteria. Surfaces the stated frame, gathers short written definitions from several people, asks what the description leaves out, checks the objective, analyses cases where the problem did not occur, and treats problems as multicausal rather than finding one root cause. Use whenever someone asks to frame or reframe a problem, write a problem statement, scope a project, run a root-cause or 5 Whys session, work out the real problem, or says a solution is not working and they do not know why. Do NOT use for choosing between options already defined (use decision-frameworks), stress-testing a chosen plan (use premortems), ranking a backlog (use prioritisation) or running desk research (use research-planning)."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/productivity/thinking-decisions/problem-framing/
  category: productivity
  subcategory: thinking-decisions
  version: "1.0.0"
  created: "2026-10-24"
  updated: "2026-10-24"
---

# Problem Framing: Define the Right Problem Before You Solve It

Most wasted work is a good answer to the wrong question. A team spends a quarter speeding up a process that nobody minded, because the first sentence of the brief named the wrong problem and no one checked it. This skill slows down that first sentence. It takes a stated problem and tests whether it is the problem worth solving, then offers better frames before any solution is designed.

It is built for an agent working with one person or a small group. It works for a product issue, an operations bottleneck, a growth target that is missing, a team friction or a personal decision that keeps stalling. The method is tool-agnostic. The only tool-specific notes sit in one fenced appendix at the end.

The goal is not to find the single true problem. A problem can be framed in several defensible ways, and the point is to find a better one to solve than the one you started with. The skill produces candidate frames and a recommendation, and the human chooses. It does not pick a solution, and it does not act.

## When to use this skill, and when not to

Use it when the problem is still soft and the solution is not yet fixed:

- A brief or ticket that starts with "we need to" or "the problem is", where the fix is assumed.
- A goal that is being missed and the reason is unclear.
- A recurring complaint ("support is slow", "the site is confusing", "the team is not aligned").
- A project about to start, where the scope and the real aim are worth pinning down first.
- A root-cause or 5 Whys session that is about to settle on one cause.
- A solution that has been tried and has not moved the number.

Do not use it for:

- Choosing between options that are already defined. Use `decision-frameworks`.
- Stress-testing a plan you have already chosen. Use `premortems`.
- Ordering a list of tasks or features. Use `prioritisation`.
- Gathering evidence from sources or data. Use `research-planning` and `desk-research`, then bring the findings back here.
- Recording a decision once it is made. Use `decision-records`.
- Advice on health, money, legal standing or employment outcomes. The skill can help frame the question, but it labels any such frame as needing a qualified person and does not give the advice itself.

## Guardrails that apply to every run

1. **Frame, do not solve.** The output is a problem statement and candidate frames with success criteria. Do not propose, design or rank solutions. If the user asks for a solution, finish the framing first and hand off to `decision-frameworks`.
2. **No fabricated facts, numbers or causes.** Every figure and every claimed cause carries its source: a person who said it, a document, or a dataset with a date. A cause with no evidence is listed as an assumption to test, not as a finding. Anything that may have changed is marked `verify before relying on this`.
3. **Separate observation from inference.** What people reported, what the data shows and what the agent concluded are tagged apart (see step 4). Never state an inference as a fact.
4. **Sensitive data stays out.** Problem descriptions often carry names, customer details, salaries, health information, client names under NDA and unpublished figures. Redact them before processing (see step 0). Never write them into the brief or send them to a third-party service without asking.
5. **No speculation about motives.** State what a person said or what the data shows. Do not assert what a customer, a competitor or a colleague "really wants" unless they said so. Label inference as inference.
6. **Scope boundary.** The skill refuses to choose the solution, commit the team to a frame on its own, or present one frame as the only correct one. The human picks the frame.

## Inputs the agent must have before starting

Do not start until the first four are answered. Ask for what is missing in one message and wait.

| # | Input | What to ask if missing |
|---|---|---|
| 1 | The problem as currently stated | "In one or two sentences, what is the problem as you see it right now? Use the exact words you would use with a colleague." |
| 2 | Who owns and who feels the problem | "Who is accountable for solving this, and who actually experiences it day to day? They may be different people." |
| 3 | What a good outcome looks like | "If this were handled well, what would be different, and how would you know? Name the measure if there is one." |
| 4 | Stakes and reversibility | "How big is this, and how hard would it be to undo a wrong move? Low stakes, or a one-way door?" |
| 5 | Other people who can define it | "Can I get a one or two sentence definition of the problem from two or three other people close to it?" |
| 6 | Evidence available | "What do we already know: data, tickets, interviews, past attempts? What has been tried?" |
| 7 | Sensitivity | "Does any of this contain personal data, client names under NDA, salaries or health details?" |

If input 1 is a solution in disguise ("we need a new CRM", "we should run more ads"), record it, then ask: "What problem would that solve? Describe the problem without naming the fix." That answer becomes input 1.

## Workflow

### Step 0. Sensitivity triage

1. Scan the inputs for names, email addresses, phone numbers, long digit strings, salaries, health terms and client names flagged under NDA.
2. Replace each with `[redacted: type]` in the working copy. Tell the user how many were redacted and of which type, without repeating the values.
3. If the material is under NDA or the model is not approved for it, stop and ask how to proceed.

### Step 1. Capture the stated frame exactly

1. Write down the problem in the user's own words from input 1. Do not tidy it.
2. Underline the nouns and the verb. These carry the hidden frame. "The elevator is too slow" frames the problem as the elevator; "the wait is annoying" frames it as the person waiting.
3. Note any solution baked into the sentence. "We need more staff" assumes the problem is capacity. Record the assumed cause separately so it can be tested, not inherited.

### Step 2. Gather short definitions from several people

1. Collect a one to two sentence definition of the problem from the owner and from two or three others close to it (input 5). Ask for full sentences, not phrases.
2. Keep them unattributed when you show them back, so word choice can be compared without rank getting in the way.
3. Compare the wording. Different nouns mean different frames. Note where the word "I" or "we" is absent, because a problem stated only as "the market" or "the system" often hides a frame where no one owns it.
4. If only one definition is available, say so in the brief and treat the single frame as lower-confidence.

### Step 3. Generate candidate frames

Produce at least two and at most four distinct frames. A frame is distinct when it changes what a good solution would look like, not just the wording. Use these prompts, in order, and stop when you have three strong frames:

1. **Shift the subject.** Re-state the problem with a different noun as the subject. Elevator to waiter; churn to onboarding; "sales are low" to "the pipeline is thin" versus "the close rate is low".
2. **Ask what is missing.** List what the stated description leaves out. The gap is often the better frame. A dip in a metric framed as a quality problem may be a measurement problem.
3. **Change the category.** Ask whether the problem is one of incentives, skill, information, expectations, attitude, process or tooling. Name two categories other than the one assumed, and frame the problem in each.
4. **Question the objective.** Write the goal behind the problem, then ask whether that goal is the right one. A programme aimed at more sign-ups may do better aimed at keeping the users it already has.
5. **Analyse positive exceptions.** Find a time, place or team where the problem did not happen. Ask what was different there. That difference is often the real frame.

For each candidate, write one sentence: "The problem is [frame], which matters because [consequence]."

### Step 4. Tag the evidence behind each frame

For every frame, mark what supports it:

| Tag | Meaning |
|---|---|
| `[reported]` | Someone said it. Name who (or the role, if redacted). |
| `[data]` | Shown in a dataset or document. Give the source and date. |
| `[inference]` | A conclusion drawn by the user or the agent. Say which. |
| `[assumption]` | Believed but unevidenced. Must be tested before the frame is trusted. |

A frame resting only on `[assumption]` tags is a hypothesis, not a finding. Say so. Do not promote it to the recommendation without at least one `[reported]` or `[data]` tag, or a named test.

### Step 5. Test each frame against the problem-statement bar

Put each candidate frame through six checks. A frame that fails checks 1 to 4 is reworded or dropped.

1. It is a full sentence and names who experiences the problem, not only "the team" or "the market".
2. It does not name or assume the solution.
3. It states the gap: the difference between what is happening and what should be, with a measure where one exists.
4. It is falsifiable: you could show it is the wrong frame with evidence.
5. It does not collapse to a single root cause. Note two or more plausible causes; most real problems are multicausal.
6. It survives the "so what": if solved, something the owner cares about (input 3) moves.

### Step 6. Score and recommend

1. Score each surviving frame on three axes, each 1 to 5: evidence (how well supported), reach (how much of the outcome it affects), and tractability (how feasible it is to act on). Do not add the scores into one number, because that hides the trade-off. Show the three.
2. Recommend the frame with the strongest combination, and name what it trades away.
3. If no frame scores 3 or more on evidence, the honest recommendation is to run `research-planning` or a small round of interviews before committing, not to pick the best guess.
4. If the stakes are low and the move is reversible (input 4), say so and recommend deciding quickly rather than framing further. Over-framing a two-way door wastes more than it saves.

### Step 7. Write the problem brief and hand off

1. Fill the problem brief template.
2. State the chosen frame, the runners-up, the success measure and the top assumptions to test.
3. Hand off: if the frame is firm and options now need choosing, point to `decision-frameworks`; if a plan exists and needs stress-testing, point to `premortems`.
4. Do not start designing solutions. The brief is the deliverable.

## Worked example

The example is invented for illustration. No figures come from a real company.

**Inputs.**

- Stated problem (input 1): "Our onboarding emails are not working, we need to rewrite them."
- Owner and who feels it (input 2): the growth lead owns it; new users and the support team feel it.
- Good outcome (input 3): "More new users reach their first real use of the product in week one. We measure activation: the share of sign-ups who complete a first project within seven days. It sits at 28 percent."
- Stakes and reversibility (input 4): medium stakes, reversible. Rewriting emails is a two-way door.
- Other definitions (input 5): support lead says "People sign up and then do not know what to do first." A product manager says "The product asks for too much before it shows any value."
- Evidence (input 6): activation 28 percent for three months [data, product analytics, Jul to Sep 2026]; 40 percent of new-user support tickets ask "how do I start" [data, support export, Sep 2026]; email open rate 52 percent, click rate 11 percent [data, email tool, Sep 2026].
- Sensitivity (input 7): none.

**Step 0.** No personal data. Zero redactions.

**Step 1. Stated frame.** Subject: the emails. Verb: not working. Baked-in solution: rewrite the emails. Assumed cause recorded: "the email copy is the blocker." That assumption is untested.

**Step 2. Definitions compared.** Three definitions, three subjects: the emails (growth lead), the user's first step (support lead), the product's demands before value (product manager). Only one of the three names the emails. The word "I" or "we" appears in none, so the frame of who owns the first-run experience is unclear.

**Step 3. Candidate frames.**

- F1 (stated): The onboarding emails do not drive action, which matters because new users do not return to activate.
- F2 (what is missing): New users do not know their first step inside the product, which matters because 40 percent of early tickets ask how to start.
- F3 (change the objective): The product asks for too much before showing value, which matters because users leave before the first payoff.
- F4 (positive exception): Users who invite a teammate in the first session activate far more often, which matters because the single-user path may be the weak one.

**Step 4. Evidence.**

- F1: email click rate 11 percent `[data]`; "copy is the blocker" `[assumption]`. The open rate of 52 percent suggests the emails are read, which weakens F1.
- F2: 40 percent of tickets ask how to start `[data]`; support lead's account `[reported]`.
- F3: product manager's account `[reported]`; no data yet `[assumption]`.
- F4: invite-then-activate pattern `[data]`, but direction of cause is `[inference]`.

**Step 5. Bar.** F1 names the solution and the open rate contradicts it, so it is reworded to "something after the email open is not landing" and demoted. F2, F3 and F4 pass: each names who feels it, states a gap with a measure, is falsifiable and has more than one plausible cause.

**Step 6. Score (evidence / reach / tractability).**

| Frame | Evidence | Reach | Tractability |
|---|---|---|---|
| F2 first step unclear | 4 | 4 | 4 |
| F3 value asked too late | 2 | 5 | 2 |
| F4 single-user path weak | 3 | 3 | 3 |

Recommendation: frame the problem as F2, "new users do not know their first step inside the product." It has the strongest evidence and is tractable. It trades away the deeper F3 question of product value, which should be tested next, not now. The email rewrite (F1) is not the problem to solve first.

**Step 7. Brief.** Produced below, handed to `decision-frameworks` to choose between an in-product first-run guide, a checklist and a setup call.

```markdown
# Problem brief: first-week activation

Stated as: "Onboarding emails are not working, we need to rewrite them."
Reframed as: New users do not know their first step inside the product.

Who feels it: new users in week one; the support team.
Success measure: seven-day activation, now 28% (product analytics, Jul to Sep 2026). Target set by owner.

Chosen frame: first step unclear [data: 40% of early tickets ask how to start, Sep 2026].
Runners-up: product asks for value too late (test next); single-user path is weak.
Dropped: email copy is the blocker (open rate 52% shows emails are read).

Top assumptions to test:
1. Users who see a clear first step activate more. (A/B a first-run guide.)
2. The value-too-late frame (F3) needs one round of user interviews.

Reversibility: two-way door. Decide and test rather than frame further.
Hand off to: decision-frameworks.
```

## Templates

### Problem brief

```markdown
# Problem brief: [short name]

Stated as: [the user's original words]
Reframed as: [the chosen frame, one sentence]

Who owns it: [role]
Who feels it: [role]
Success measure: [metric, current value, source and date]

Chosen frame: [sentence]. [evidence tag]
Runners-up: [one line each]
Dropped frames: [frame] - [why dropped]

Top assumptions to test:
1. [assumption] - [how to test it]
2. [assumption] - [how to test it]

Stakes and reversibility: [low/medium/high; one-way or two-way door]
Hand off to: [decision-frameworks / premortems / research-planning]
```

### Definition-gathering prompt (send to each person)

```text
In one or two full sentences, what is the problem here, in your own words?
Please describe the problem, not the fix. I will keep it unattributed.
```

### Reframing prompts (run in order, stop at three strong frames)

```text
1. Shift the subject: re-state with a different noun as the subject.
2. What is missing: what does the description leave out?
3. Change the category: incentives, skill, information, expectations, attitude, process, tooling. Pick two others and reframe.
4. Question the objective: is the goal behind this the right goal?
5. Positive exception: where did this NOT happen, and what was different?
```

### Starting prompt

```text
Frame this problem with the problem-framing skill before we solve it.
Stated problem: [your words]
Owner / who feels it: [roles]
Good outcome and measure: [one sentence]
Stakes and reversibility: [low/medium/high; one-way or two-way door]
Other definitions: [paste 2-3, or say you will get them]
Evidence and past attempts: [paste or link]
Sensitivity: [none / describe]
Do not propose solutions. Produce a problem brief.
```

## Failure modes and anti-patterns

| # | Failure | How to spot it | What to do instead |
|---|---|---|---|
| 1 | **Framing as the solution in disguise.** The "problem" is a fix with a problem painted on ("we need an app"). | The stated problem names a tool, a channel or a hire. | Apply step 1. Strip the solution, ask what problem it would solve, reframe from there. |
| 2 | **The law of the instrument.** The framer sees every problem through their own speciality, so the marketer frames it as messaging and the engineer as architecture. | Every candidate frame sits in one discipline. | Use step 3's "change the category" prompt and gather definitions from people in other roles (step 2). |
| 3 | **Single-root-cause tunnel.** A 5 Whys or root-cause session stops at the first clean cause and treats the problem as solved once that cause is named. | The brief names exactly one cause and one fix. | Enforce check 5 in step 5: name two or more plausible causes. Problems are usually multicausal. |
| 4 | **Turning the method into a checklist.** The agent runs the prompts mechanically and produces frames nobody believes. | Frames that are reworded versions of the same idea; no one disagrees with any of them. | Require frames to be distinct (step 3) and to pass the "so what" and falsifiability checks. A checklist run without thinking discourages the thinking it was meant to prompt. |
| 5 | **Framing in the room, never testing.** The group settles on a frame from opinion alone and skips evidence. | The chosen frame rests only on `[assumption]` and `[inference]` tags. | Apply step 6, rule 3: if evidence is weak, recommend a small research or interview round before committing. |

## Quality bar

Run every item before handing over. Each is checkable.

1. The stated problem is recorded in the user's exact words, with the baked-in solution, if any, named separately.
2. At least two and at most four distinct candidate frames are produced, each a full sentence.
3. Each frame names who experiences the problem and does not name the solution.
4. Each frame carries at least one evidence tag, and frames resting only on `[assumption]` are labelled as hypotheses.
5. The chosen frame scores 3 or more on evidence, or the brief recommends research first.
6. At least two plausible causes are named; no frame is reduced to one root cause.
7. The success measure names its source and date.
8. Definitions were gathered from more than one person, or the brief says only one was available.
9. No solution is proposed anywhere in the output.
10. No redacted value appears in the brief, and no sensitive data was sent to a third party without asking.
11. The brief states stakes and reversibility and hands off to the right next skill.

## Cost and effort

The cost is mostly input tokens plus the time to gather definitions from a few people. The agent work is light: a few hundred to about two thousand output tokens for a brief. The slow part is human, and it is worth it. The cheap way to go wrong is to skip step 2 and frame from a single viewpoint; the time saved there is lost many times over if the team then solves the wrong problem. For a low-stakes, reversible problem, do not over-invest: step 6 tells you to decide and move rather than frame on.

## Handoffs to related skills

- `decision-frameworks`: once the frame is firm and options need choosing.
- `premortems`: once a plan exists, to stress-test it before committing.
- `prioritisation`: when there are several framed problems and you must order them.
- `research-planning` and `desk-research`: when the best frame needs evidence before it can be trusted.
- `decision-records`: to record the chosen frame and why, once a decision follows.
- `project-breakdown`: to turn the chosen frame into a plan of work.

## Appendix: tool-specific notes

Everything above is tool-agnostic. This appendix is the only place that names a product. Verify each point before relying on it, because products change.

**Running this with an AI agent.** Paste the stated problem and the inputs, and ask the agent to produce candidate frames and a brief, not solutions. Agents tend to jump to fixes, so repeat the "frame, do not solve" instruction in the prompt. Have the agent tag every claim with an evidence tag; an untagged claim is usually an invented one.

**Whiteboards and docs (Miro, FigJam, a shared doc).** The definition-gathering step works well as sticky notes collected before discussion, kept unattributed until they are compared. Group by the subject noun, not by who wrote them.

**Claude Agent Skills.** `name` is limited to 64 characters (lowercase letters, numbers, hyphens) and `description` to 1,024 characters. Only the metadata loads at start-up, so the description decides whether the skill fires. Use skills from trusted sources only. Verify limits in the Anthropic documentation.

## Sources

Last verified 24 October 2026 for every source below.

- Thomas Wedell-Wedellsborg, "Are You Solving the Right Problems?", Harvard Business Review, January to February 2017: https://hbr.org/2017/01/are-you-solving-the-right-problems. The slow-elevator example, the seven reframing practices, boundary spanners, positive-exception analysis, questioning the objective, and the warning that a checklist discourages real thinking.
- Chip Heath and Dan Heath, "Decisive" (2013), WRAP process summary via Michael Kitces: https://www.kitces.com/blog/how-to-be-more-decisive-in-your-own-decision-making-process/. Narrow framing as the first villain of decision-making; widening the frame; the outside view.
- Samuel Thomas Davies, summary of "Decisive": https://samuelthomasdavies.com/the-wrap-process. Avoiding binary framing, laddering from local to distant analogies, finding someone who has solved your problem.
- Daniel Kahneman, Dan Lovallo and Olivier Sibony, "Before You Make That Big Decision", Harvard Business Review, June 2011: https://thecne.org/wp-content/uploads/2016/04/The-Big-Idea_-Before-You-Make-That-Big-Decision.pdf. Checking whether credible alternatives were considered and whether the diagnosis leans on a salient analogy.
- Anthropic, Agent Skills overview: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview. Frontmatter limits, the description's role in triggering, and security advice.
- obra/superpowers, `brainstorming` and `writing-plans` skills (via the superpowers skills framework): https://github.com/obra/superpowers. Reviewed as the nearest existing skills; they draw out intent and plan the work, but assume the problem is already stated correctly.
