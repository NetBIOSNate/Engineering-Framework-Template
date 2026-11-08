# Preserve invariants under concurrency

State an invariant in words a stakeholder recognizes. Examples include “available inventory never falls below zero,” “one operator holds motion authority at a time,” and “each accepted event has one financial effect.” Define the period and scope over which the rule must hold and which temporary inconsistencies users may observe.

## Trace the conflicting operations

1. List every writer, including maintenance tools, restoration jobs and external callbacks. Mark the instant at which a change becomes authoritative.
2. Interleave two operations on the same item. Draw the last read on which each decision relies and the first durable write. If both can see the same prior state, identify what prevents both from succeeding.
3. Choose an enforcement mechanism at the owning boundary. Candidates include an atomic conditional update, serialized command stream, unique constraint, lock or an explicit reconciliation workflow. State the liveness and recovery assumptions each adds.
4. Test restart, timeout, stale ownership and reordered completion. Give a repeated request an identity with an explicit scope and a definition of equivalent content.

## One remaining unit

Two users each request the last unit. An inventory owner checks and decrements stock in a single conditional state change. Store the response against the caller-scoped request identity with the committed update. Replaying an accepted request returns the recorded result. Reusing its identity with different contents yields a conflict. A notification worker owns delivery and must be able to reconcile an uncertain external effect.

A distributed lease can expire during a paused writer's operation. When stale writes matter, allocate increasing ownership generations and have the resource reject an older generation. Check the resource actually sees and enforces that generation. A timestamp on a client alone cannot prevent a stale writer's commit.

Review by injecting a pause across the ownership transfer, resuming the earlier worker and reading back the state. Record overlapping attempts, committed effects and how clients distinguish rejection from unknown completion. See the [transactional system profile](../../../framework/profiles/business-systems/modular-transactions.md).

[Architecture field guide](../../../framework/README.md)
