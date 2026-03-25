# MVP Analysis File Format

Analysis files are markdown documents with the following structure. All
sections are required unless noted otherwise.

```
# MVP Analysis: <name>

## Result

**Outcome:** Pass / Fail
**Threshold:** <restate the pre-committed threshold>
**Observed:** <what actually happened>

## Data Summary

<concise summary of the results data>

## Interpretation

<what the outcome means in terms of revealed preference>

## Assumptions Review

| Assumption | Held? | Evidence |
|------------|-------|----------|
| <assumption> | Yes/No/Unclear | <evidence> |

## Surprises

<unexpected findings worth noting>

## Decision

**Action:** Pivot / Persevere / Kill / Retest
**Rationale:** <why this decision follows from the data>

Note: The decision is independent of whether the threshold was met. A passing
result may lead to a pivot (e.g., the hypothesis held but a more valuable
problem emerged), and a failing result may lead to perseverance (e.g., the
experiment was flawed but the signal is strong enough to retest). The decision
reflects what the team believes is the highest-value next move given
everything learned.

## Next Experiment (if applicable)

<brief description of what to test next and why>

## Additional Comments

<free-form space for the user to record context, observations, or notes that
do not fit the sections above — team dynamics, market timing, resource
constraints, gut feelings worth revisiting later, etc.>
```
