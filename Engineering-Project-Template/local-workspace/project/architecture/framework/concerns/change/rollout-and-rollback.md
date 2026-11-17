# Plan rollout, rollback and forward recovery

A rollout introduces intermediate architectures. For each stage specify the active writer, the readers, the contract versions, the observable health of the user outcome and the allowed recovery action. Define where a seemingly reversible deployment makes an irreversible change to data, external effects or physical state.

## Design a phased transition

| Phase | Question that must have an answer |
| --- | --- |
| Expand | Can the old version still operate against the expanded storage or interface? |
| Shadow | Can the candidate observe representative work while external effects are suppressed? |
| Limited release | Which representative cohort is exposed and who can halt further admission? |
| Transfer | Who owns new writes and how is a former writer prevented from acting? |
| Contract | What proves the last old reader and restore procedure can tolerate removal? |

A canary percentage is meaningful only when the cohort exercises the relevant behavior. A low-volume pilot may never hit peak concurrency, a rare permission or old firmware. Specify what the sample covers, how long it must span and the signals that could falsify the release hypothesis. Keep an independent view of the baseline.

## State the rollback boundary

A binary can be restored quickly while newly accepted records remain unreadable by the old version. Identify the first incompatible write and label the available response at that point. Options include reversible encoding, dual-compatible readers, reconciliation to the old store, isolation of affected records or a forward repair. For a physical change, address field stock and installed equipment whose configuration cannot be changed remotely.

Exercise rollback or recovery after an acknowledgment and an in-flight transfer. Verify observed user effects, record completeness and who owns resolution of mismatches. Retain old readers and keys for as long as archives or field assets depend on them. The release owner can then distinguish “stop admitting new work” from “restore the former architecture.” See [modernization](../../profiles/evolution/legacy-modernization.md) and [recovery](../resilience/failure-domains-and-recovery.md).

[Architecture field guide](../../README.md)
