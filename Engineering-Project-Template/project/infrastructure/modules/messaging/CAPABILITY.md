# Queues, replay and overload

## Service goal

Absorb bursts while preserving the consumer's agreed delivery, ordering and recovery semantics.

## Contract

Publish payload and envelope limits, durable acknowledgement point, retry and visibility limits, ordering scope, retention, replay authority and tenant quota.

## Build and commission

1. Size using ingress, consumer service rate and outage length. With 250 items/s arriving and 400/s served, a 90,000-item backlog drains in 600 s if downstream capacity holds.
2. Give messages stable event IDs. Define when the consumer acknowledges work and how repeated delivery is handled across a crash after processing. For keyed order, define partition placement and what happens during rebalance.
3. Bound retries with backoff and jitter. Quarantine poison items with reason, attempt count and a controlled replay path. Reserve retention for the longest planned interruption and drain.

## Acceptance exercise

Interrupt a consumer after its side effect and before acknowledgement. Verify redelivery produces the expected external effect. Introduce a malformed item, prove other partitions make progress and replay the corrected item once. Record oldest age, loss, duplicates and drain time.

## Revisit the design

Review when ordering guarantees, consumer concurrency, partition skew or retention change. A declining queue count can hide one old, blocked partition.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
