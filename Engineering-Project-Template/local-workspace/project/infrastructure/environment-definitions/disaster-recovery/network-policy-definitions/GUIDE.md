# Recovery routing and controlled failover

## Intended outcome

A recovery site can be commissioned in isolation, then receive approved traffic without leaving conflicting routes or writers.

## Policy inputs

Define nonoverlapping prefixes, independent resolver, route advertisement authority, peer access, data replication paths and how clients select the active endpoint.

## Implementation sequence

1. Build an isolated rehearsal namespace. Establish connectivity to backups, keys and telemetry without advertising the drill target to production clients.
2. Before activation, establish writer fencing and check reverse paths, certificate names, TTLs and partner allowlists. Route a bounded consumer to the recovery endpoint first.
3. Sequence failback around catch-up, fencing and routing reversal. Retain observability on old and new paths until long-lived connections and caches have drained.

## Evidence and handoff

In a drill, query from two client locations and trace a new session and an existing session. Measure response convergence and check old endpoints reject writes. Document who can withdraw a bad advertisement if the primary management path is down.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
