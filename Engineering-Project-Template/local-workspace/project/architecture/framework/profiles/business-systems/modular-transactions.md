# Profile for a modular business system

Use this path for an internal application, case-management workflow or commercial transaction system. Begin with a real business rule in the words of the people who apply it. Identify who owns the fact, who can change it and which external effects occur once a decision is made.

## Choose module boundaries

Trace a transaction from request to committed outcome. Group decisions that need atomic consistency around their authoritative state. Separate modules with different meanings for the same term, different ownership or independent change pressure. Modules can share a deployment while maintaining explicit entry points and data ownership. A report that bypasses a module and writes its tables creates a second writer regardless of organizational diagrams.

One unit remains and two people submit reservations concurrently. The stock owner performs an atomic conditional allocation and stores the result against a caller-scoped idempotency key. Include a fingerprint or canonical representation to detect changed requests under the same key. The same local transaction stores an intent to notify. A worker publishes the intent and records enough state to reconcile uncertain delivery.

## Review the failure cases

| Disturbance | Expected observation |
| --- | --- |
| Two concurrent requests for the last unit | One accepted allocation and stock stays at or above zero |
| Receipt lost after commit | Replaying the accepted key returns the prior outcome |
| Same key with changed contents | Explicit conflict with an owned resolution path |
| Downstream message repeated | One business effect or a visible reconciliation item with an owner |

If another organization owns notification delivery or settlement, establish what idempotency, lookup or reconciliation it provides. Describe how long an operator can leave work pending and who can compensate a mistaken action. Capture a glossary of business terms, an invariant table, an ownership map and a runtime failure sequence. See [component design](../../../component-design/structure/responsibility-and-state.md) and [concurrent operations](../../../component-design/structure/runtime/concurrency-and-invariants.md).

[Architecture field guide](../../README.md)
