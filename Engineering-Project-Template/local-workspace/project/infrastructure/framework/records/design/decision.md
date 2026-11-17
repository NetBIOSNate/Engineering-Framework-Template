# Architecture decision record

## Copy for one decision

| Field | Fill in |
| --- | --- |
| Decision ID, scope, date, status | [Proposed, accepted, superseded, or retired. Name related decisions.] |
| Owner and consulted operators | [Who can accept the consequences and who repairs the result?] |
| Trigger | [What changed, or which commitment is now necessary?] |
| Requirements and evidence | [Consumer targets, observed demand, failure model, constraints and sources.] |
| Options | [At least two viable ways to meet the need, including a simpler option when one exists.] |
| Selected option and reasoning | [Identify the deciding constraint, evidence supporting it and uncertain assumptions.] |
| Consequences | [Operations effort, recurring and exit cost, security, failure modes and coupling.] |
| Verification | [Exact probe, location, workload, failure, threshold, owner and date.] |
| Revisit or reversal | [Trigger, last reversible point, dependency to unwind and funded alternatives.] |

## Compare on equal terms

For each option, document normal and degraded throughput, restore time and loss, shared dependencies, control ownership and effort to exit. If the evidence is a model, include the equation and the measurement that would invalidate it. A precise estimate without a known input remains uncertain.

**Worked decision fragment.** Two candidate recovery paths serve a 2 TiB archive. A 100 MiB/s transfer takes roughly 5.83 hours before setup and checks. With a four-hour objective, the owner chooses a warmer restore source and exercises it at full volume. Revisit when observed recovery exceeds three hours or retained data grows by 25%.

## Close the record

Attach the review date and the observed test result when available. Preserve the assumptions of a superseded decision so the next owner can understand what changed.
