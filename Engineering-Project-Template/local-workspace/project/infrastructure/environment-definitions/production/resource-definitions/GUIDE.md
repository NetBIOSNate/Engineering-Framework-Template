# Production capacity and ownership

## Intended outcome

Critical resources have a named operator, enough tested capacity for the selected failure and a verified path through replacement or restore.

## Policy inputs

Declare capacity envelope, data class, retention, ownership, placement, policy revision, billing allocation and maintenance constraints.

## Implementation sequence

1. Place resources across the domains assumed by the design. Verify quotas, IPs, storage and workforce needed for replacement while the largest planned failure persists.
2. Protect state and review changes capable of destroying durable resources. Pin released inputs, capture live IDs and sequence stateful changes around writer handoff.
3. Assign targets for consumer service, saturation and recovery. Include capacity and support lead time in scaling triggers and supplier escalation.

## Evidence and handoff

Before release, demonstrate a consumer operation on the canary, retained data recovery and a second preview with understood drift. Record which domain-loss claims were measured and which remain modeled. Hand over the owner, paged signals, capacity horizon and next review trigger.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
