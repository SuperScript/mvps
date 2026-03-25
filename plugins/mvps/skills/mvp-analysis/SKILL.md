---
name: MVP Analysis
description: >-
  This skill should be used when the user asks to "analyze MVP results",
  "review experiment results", "evaluate MVP outcome", "what do the results
  mean", "post-experiment analysis", "did the MVP pass", "interpret my
  experiment data", "analyze my test results", or "review my MVP experiment".
  Guides structured post-experiment analysis against the pre-committed
  threshold test.
allowed-tools:
  - Read
  - Write
  - AskUserQuestion
---

# MVP Analysis

## Purpose

Guide post-experiment analysis of MVP results. The threshold test was set
before the experiment — pass or fail is unambiguous. The analysis focuses
entirely on what the outcome means and what to do next.

## References

- `../../references/mvp-file-format.md` — structure of the MVP file being
  analyzed. Read it to understand the input.
- `../../references/mvp-analysis-format.md` — structure of the analysis output
  file. Read it before writing output.

## Conversation Flow

Work through these phases in order using AskUserQuestion. Do not skip phases.

### Phase 1: Load the MVP File

Ask the user for the path to their MVP file. Read it. Confirm the hypothesis
and threshold test back to the user before proceeding.

### Phase 2: Gather Results Data

Ask the user to provide their experiment results. Accept any format — raw
numbers, a file path to data, a verbal summary, screenshots, or a
spreadsheet. If the user provides a file path, read the file. Ask clarifying
questions until the data is sufficient to evaluate against the threshold test.

### Phase 3: Apply the Threshold Test

State the result plainly: pass or fail. The threshold was pre-committed — do
not negotiate, soften, or qualify the binary outcome. If the data is
incomplete or ambiguous relative to the threshold, say so directly and ask
what additional data is available before declaring a result.

### Phase 4: Interpret the Outcome

Distinguish between what happened and what it means. Address these questions:

- **What did the data show?** Summarize the key observations.
- **Was the hypothesis supported?** Based on revealed preference, not stated
  preference.
- **What assumptions held? Which broke?** Cross-reference against the Key
  Assumptions section of the MVP file.
- **What was surprising?** Unexpected findings often matter more than the
  primary result.

### Phase 5: Challenge Confirmation Bias

Push back on the user's interpretation. Common traps:

- **Rationalizing a fail**: "We almost passed" or "the audience wasn't right"
  are excuses, not analysis. A fail is a fail. The question is what to learn
  from it.
- **Over-celebrating a pass**: Passing the threshold means the hypothesis was
  not disproven — it does not prove product-market fit or guarantee success.
- **Cherry-picking**: If the aggregate failed but a subgroup passed, note it
  as a signal worth investigating — but do not let it override the overall
  result.
- **Ignoring the threshold**: If the user tries to reinterpret the threshold
  after seeing results, name it directly: "The threshold was set before the
  experiment to prevent exactly this kind of post-hoc rationalization."

State objections directly. Do not soften with "just playing devil's advocate."

### Phase 6: Decide Next Steps

Guide the user to a concrete decision. The options are:

- **Pivot**: Change the problem, audience, or approach and design a new
  experiment.
- **Persevere**: Move to the next riskiest assumption and design a new
  experiment to test it.
- **Kill**: Stop work on this idea entirely.
- **Retest**: The data was insufficient or the experiment was flawed. Design a
  better experiment for the same hypothesis.

These decisions are independent of whether the threshold was met. A passing
result may lead to a pivot if a more valuable problem emerged during the
experiment. A failing result may lead to perseverance if the experiment itself
was flawed but the underlying signal is strong enough to retest differently.
The decision reflects the highest-value next move given everything learned,
not a mechanical mapping from pass/fail.

Do not let the user defer the decision. An MVP without a follow-through
decision is wasted effort.

### Phase 7: Write Output

Ask the user where to save the analysis. Read the output format from
`../../references/mvp-analysis-format.md` and write the file accordingly.
Before finalizing, ask the user if they have additional comments to include in
the Additional Comments section.

## Guidance

The value of this skill is intellectual honesty. Most teams struggle to accept
negative results or to avoid inflating positive ones. Treat the threshold test
as sacred — it exists precisely to prevent post-hoc rationalization. Every
claim about what the results mean must be grounded in observable behavior, not
in what the team hopes is true.

A team that passes every hypothesis test is not a team that picks winners — it
is a team that sets weak thresholds or avoids testing hard assumptions. The
optimal learning rate from hypothesis testing is around 50%. If every
experiment passes, the experiments are too easy. If every experiment fails,
the ideas are too disconnected from reality. A roughly even split between
passes and fails means the team is testing at the frontier of its knowledge,
where the most learning happens. Frame failed experiments as expected and
valuable, not as setbacks.
