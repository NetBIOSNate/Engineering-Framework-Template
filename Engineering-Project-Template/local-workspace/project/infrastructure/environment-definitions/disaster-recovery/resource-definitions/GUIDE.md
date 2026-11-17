# Recovery footprint, clean rebuild and failback

## Intended outcome

The recovery footprint can become a minimum usable service within the agreed recovery time and data-loss limits.

## Policy inputs

List the chosen standby tier, reserved quotas, artifact digests, recovery point, data size, sustained restore rate, historical keys, operator and capacity source.

## Implementation sequence

1. Build a dependency sequence that works with the primary inaccessible. Include bootstrap images, policy, clock, identity, state mapping and restore catalogs.
2. Separate retrieval delay, transfer time, replay and consumer validation. For 2 TiB at 200 MiB/s, transfer alone takes about 2.91 h. Compare the whole interval with the target.
3. Schedule a clean recovery of a representative data set. Start health checks only after consistent data is present. Rebuild redundancy after failover and quantify the exposure while operating on the recovery site.

## Evidence and handoff

Validate a dated marker, record actual data age and outage, and test both a read and an allowed new write. Reconcile results after failback and retire drill resources. Give any capacity shortfall or untested supplier dependency an owner.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
