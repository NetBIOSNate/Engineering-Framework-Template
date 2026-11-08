# Stage representative traffic and cutovers

## Intended outcome

Staging verifies routing and security behavior on the paths likely to fail during a real promotion.

## Policy inputs

Inventory ingress, egress, resolver, TLS termination, transit, MTU and circuits. List cost-driven differences in capacity and external endpoints.

## Implementation sequence

1. Reproduce the sequence of policy enforcement and return paths. Use representative payload sizes, client placement and authenticated endpoints.
2. Exercise a bounded DNS or route cutover while observing old and new targets. Include existing connections, new sessions and clients whose caches hold the previous answer.
3. Verify external callbacks and failure behavior against controlled peers. Keep a separate console or management path during test changes.

## Evidence and handoff

Compare client symptoms with routing and firewall observations before, during and after failover. Time restoration and record where a staging substitute limits confidence. Hand production operators the expected transient behavior and stop conditions.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
