# Profile for intermittently connected systems

Use this path when a field unit, mobile workflow or remote team must continue useful work during a partition. Ask the operator which actions can safely occur offline, which decisions require fresh shared state and what should happen when the local store reaches capacity.

## Define the offline contract

Assign each producer a stable identity and a sequence or equivalent unique key that survives restart. Define the local and remote durability points, the deletion permission, the deduplication horizon and how a replaced device receives a new identity. Specify how clock uncertainty and retransmission affect the age displayed to a user. Give the person at the edge a visible state for accepted, waiting, refused or requiring review.

## Size and drain the buffer

One unit produces two records/s of 600 payload bytes each. Twelve hours of disconnection create 86,400 records and 51,840,000 bytes of payload. A 1.5 planning multiplier gives 77,760,000 bytes. Measure the actual journal, indexes, filesystem reserve and service-life wear to learn what the multiplier covers. Define whether high-priority work has separately reserved space.

At 10 confirmed records/s with two new records/s continuing, the ideal net drain is eight/s and catch-up takes three hours. Average-day throughput hides connection setup, small writes and starvation of the oldest records. If all units reconnect together, repeat the calculation and measurement at the fleet bottleneck.

Test power loss after local commit, after remote commit but before acknowledgment, and during cleanup of locally acknowledged records. Restore the link under load and track age as well as count. Expect accepted identities to reconcile, duplicate transmissions to cause one business effect within the contract, and deadlines to hold in the stated envelope. Start with [the worked case](../../examples/field-observations/01-frame/mission-and-options.md) and carry local policy to [revocation handling](../../../trust-boundaries/protection/identity-and-authority.md) and [overload](../../../capacity-planning/modeling/saturation/backlog-and-load-shedding.md).

[Architecture field guide](../../README.md)
