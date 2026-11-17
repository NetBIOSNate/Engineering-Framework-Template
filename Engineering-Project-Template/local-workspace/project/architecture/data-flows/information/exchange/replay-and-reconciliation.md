# Reconcile attempts, facts and effects

Delivery counts, unique facts and business effects have different denominators. Define the entity you are counting and the boundaries of the cohort. Use a stable producer identity, generation and sequence or an equivalent durable key. Define the response to the same key with different content before enabling automated redelivery.

## A ledger for a bounded cohort

Suppose 1,000 delivery attempts include 30 byte-equivalent repeats of accepted observations and 10 distinct invalid first deliveries. After all attempts terminate, one consistent accounting is 960 first-time accepted + 30 duplicate + 10 quarantined = 1,000 attempts. If work is still in flight, give those attempts their own state. Count attempts exactly once in this balance. Reconciliation of unique observations or downstream actions requires a second balance on unique keys.

Acknowledge only at the documented durability boundary. A missing acknowledgment after commit makes another delivery legitimate. Atomically couple the consumer's effect to its deduplication record where possible. An external side effect may require an external idempotency key, read-back by reference or a named manual reconciliation procedure.

## Order, replay and repair

1. Define the smallest ordering scope that matters. Partitioning by device can preserve per-device order without imposing a fleet-wide order.
2. Set a maximum replay horizon that covers disconnection, retry, restore and operator-driven reprocessing. If old records outlive the deduplication history, route older replays to reconciliation or supply a durable effect ledger.
3. Define correction versus conflict. A correction has a new identity or revision and references the original. Same identity and incompatible content is evidence of a defect or misuse.
4. Exercise replay with external effects suppressed in a test environment. Compare the rebuilt aggregate against the current one and account for intentional changes in interpretation.

Ask a reviewer to interrupt processing after effect but before acknowledgment and after local persistence but before upload. Reconcile using durable IDs across all three boundaries. Require an owner for every unexplained gap, repeated effect or quarantined observation. See [the field-system contracts](../../../framework/examples/field-observations/02-design/views-and-contracts.md).

[Architecture field guide](../../../framework/README.md)
