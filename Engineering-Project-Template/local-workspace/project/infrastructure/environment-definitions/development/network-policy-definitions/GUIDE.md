# Development network boundaries

## Intended outcome

A workstation or disposable runner can reach required development services without creating a transit path into sensitive networks.

## Policy inputs

Record developer entry point, sandbox prefixes, resolver namespace, package mirrors, permitted outbound destinations and the owner of any temporary exception.

## Implementation sequence

1. Allocate nonoverlapping space where future peering is likely. Publish naming and address conventions for short-lived environments.
2. Permit the minimum route to required mocks, test services, time and package sources. Bind public preview endpoints to a designated owner, authentication setting and expiry.
3. Isolate shared development services from one another. Document the proxy or gateway that attributes egress to a fixture and the path used to remove stale names.

## Evidence and handoff

Resolve a private development name, prove the required connection, then test a denied management endpoint from the same source. Verify stale preview names disappear on cleanup. Keep the flow matrix close to the team that accepts new exceptions.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
