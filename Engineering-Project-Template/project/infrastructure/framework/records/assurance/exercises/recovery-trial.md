# Recovery trial evidence sheet

## Before starting

Name the service, target failure, approved test boundary, observer, operator, stop authority and independent contact. Define the minimum usable operation, agreed RTO/RPO, probe interval, disposal plan and whether the exercise includes detection. Record data size, backup generation, image revision, available key versions and the location of recovery instructions.

| UTC timestamp or measurement | Observed value |
| --- | --- |
| Last acknowledged synthetic write before impact | [Timestamp, monotonic sequence, integrity digest.] |
| Impact begins / detection / declaration | [Three timestamps with sources.] |
| Access and keys obtained | [Time and identity reference, no secret values.] |
| Target provisioned / retrieval begins / replay completes | [Separate timings and retry delays.] |
| Latest consistent recovered write | [Sequence, time, cross-store consistency check.] |
| First successful consumer validation | [Time, operation, identity and expected result.] |
| Redundancy and backup coverage restored | [Time and evidence.] |

Compute observed interruption from agreed impact start to verified usable service. Compute the recovery-point gap from impact to the most recent consistent recovered marker, and state marker granularity. Record alarm delay and hands-on time separately so the next improvement addresses the real bottleneck.

## Decision

Target met [ ], uncertainty [ ], unresolved missing records [ ], unexpected dependency [ ], rollback/failback result [ ], owner and deadline for remediation [ ], retest fixture [ ]. Illustrative result: an event at 13:00, a last consistent marker at 12:52 and a first passing consumer read at 13:42 indicate an eight-minute point gap and a 42-minute interruption at the stated sampling precision.
