# Regional placement and custodial boundaries

## Goal

Determine where infrastructure data, administration and recovery actually travel when the project has residency or custody requirements. Obtain the approved locations, contractual scope and data classes from the accountable owner before designing placement.

1. Make one row per primary object, replica, backup, log, metric label, support bundle, crash dump and key. Record capture location, processing location, custody, replicated destinations, retention and deletion mechanism. Include identity and network control-plane metadata where the project scope includes it.
2. Follow one create, one support escalation and one restore. Document regional endpoint choices, staff access paths, upload defaults, telemetry exporters, caches and provider support subprocessors. Require specific evidence where a supplier controls part of the path.
3. Model failure of the only permitted site. If the approved boundary excludes an alternate location, show the resulting recovery time and surviving capacity. Ask the owner to choose among an additional permitted facility, a different recovery tier, or a revised target.
4. Enforce placement through the available provisioning controls and independently check observed placement. Deny deployment of a fixture to an unapproved location and verify the creation event identifies the deciding policy. Verify a recovery copy can be read with authorized in-boundary access.

## Handoff

Keep a dated flow map, provider evidence, owner-approved interpretations and explicit unresolved dependencies. Record how a location change, new telemetry field, support contract or backup target triggers another review. Restrict sensitive topology and audit records according to their own classification.
