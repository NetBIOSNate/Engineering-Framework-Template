# Network reachability and isolation

## Service goal

Deliver authorized flows between named endpoints and preserve an independent management path for diagnosis.

## Contract

Publish prefix and DNS ownership, peering and transit rules, address families, MTU, route preference, transport policy, bandwidth and supported failure paths.

## Build and commission

1. Construct a flow matrix from source identity/zone to destination identity/service, protocol and port. Include name resolution, time, identity, telemetry and backup traffic.
2. Allocate nonoverlapping prefixes with surge and recovery headroom. Confirm return routes at stateful enforcement points, effective MTU through tunnels, NAT port and connection-tracking limits.
3. Agree on route advertisements and ownership at each transit boundary. Use separately reachable console or management access for changes capable of cutting off the operator.

## Acceptance exercise

From approved and denied segments, force IPv4 and IPv6 independently where enabled. Verify DNS and authenticated service access separately. Withdraw one test path and measure convergence. If small probes pass but bulk transfer stalls, inspect fragmentation and path MTU signaling.

## Revisit the design

Review prefix overlap and delegated route filters before onboarding a partner or acquisition. Record the actual physical path of nominally diverse circuits.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
