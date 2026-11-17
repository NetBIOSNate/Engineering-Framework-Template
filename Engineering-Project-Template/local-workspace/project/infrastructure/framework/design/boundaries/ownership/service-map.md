# Map ownership and shared dependencies

## Goal

Establish which team can detect and repair each failure on a critical path. A system boundary should predict who can restore a consumer's operation at 03:00.

1. Follow one representative read or write from a consumer. Record the identity issuer, resolver, route, termination point, compute placement, persistence acknowledgement and response. Label dependencies with owner, service agreement, credential and observable sign of failure.
2. Draw a second path from a blank recovery host. Include image repository, package mirror, management network, state store, key service, backup catalog, name resolution and operator authentication. Mark systems hosted inside the system they must rebuild. Break cycles with a verified offline item, independent management service or documented bootstrap.
3. Group components that can fail together. Two racks on distinct switches may share a UPS, maintenance crew or management controller. Record physical, administrative and provider-level common causes. Include quota pools and configuration rollouts that cross placement boundaries.
4. Give each handoff an output a receiver can test. For a circuit this could be bidirectional reachability at a specified MTU, convergence after path failure and an escalation contact available through an outage. For backup it could be a successful restore by a recovery identity using an older key.

Remove one shared dependency from the drawing. Ask what happens to existing sessions, new sessions and a cold start. Ask the team that repairs that dependency to review the interpretation. Retain the criticality, cached behavior, degraded mode and date each claim was demonstrated.
