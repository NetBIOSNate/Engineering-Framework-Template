# Infrastructure change and reversal packet

## Plan

| Field | Enter before execution |
| --- | --- |
| Target | [Environment, tenant, resource IDs, deployment cohort and maximum impact.] |
| Inputs | [Desired revision, digest, tool version, state generation, known-good baseline.] |
| Diff | [Creates, replacements, deletions, changed routes or grants, durable format changes.] |
| Operator | [Execution identity, authorized person, owner of independent console, stop authority.] |
| Preconditions | [Healthy baseline, spare quota, tested recovery point, old/new compatibility.] |
| Observation | [Consumer metric and independent probe, sample period, specific abort threshold.] |
| Recovery | [Last reversible point, exact previous reference, roll-forward procedure, data reconciliation.] |

## During the change

Log UTC time, action, target, observed response and operator after each cohort. If state generation differs from the reviewed generation, re-observe and replan. On a timeout, inspect live resource identity and events before retrying. A second creation request can allocate another resource when the first succeeded but its acknowledgement was lost.

**Example stop rule.** A management route change advances beyond the first site only after a fresh management session and an independent consumer probe both pass. If independent visibility is lost, stop expansion and use the out-of-band console to inspect or restore the previous route.

## Close

Record final desired and observed state, duration, unexpected changes, remaining temporary grants, outcome of cleanup and decision on the next cohort. Link any emergency manual action to its reviewed permanent disposition. A second authorized operator should be able to determine the final state from this packet alone.
