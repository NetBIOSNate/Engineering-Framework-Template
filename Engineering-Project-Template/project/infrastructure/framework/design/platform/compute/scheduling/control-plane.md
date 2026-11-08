# Cluster scheduling and control-plane continuity

## Goal

Place work across nodes with repeatable admission, bounded resource contention and a functioning recovery path for the cluster itself. Use this guide for orchestrated containers, virtual-machine clusters and batch schedulers that make placement decisions from shared state.

1. Define requests, limits, priority, permitted device types, placement spread and disruption tolerance per workload class. Distinguish a scheduler's allocation estimate from actual memory demand. Check what a workload can do when its host loses memory or temporary disk.
2. Map controller quorum, state persistence, API access, worker heartbeats, image distribution, network forwarding and admission checks. Mark which existing workloads can keep serving through a control-plane outage and which actions require new scheduling.
3. Admit a node only after identity, time, network, storage plugins and image access pass cold-start probes. Plan upgrades across supported version skew and device-driver compatibility. Drain one node and reserve the capacity required to absorb its work.
4. Protect controller snapshots and the signing or encryption material needed to read them. Restore into an isolated cluster that cannot accidentally claim live node identities or attach production volumes. Compare restored inventory to a known revision.

## Acceptance

Start a representative workload, restrict the management API in a lab, and observe existing service and attempted replacements separately. Restore API access, check convergence and verify there is a single owner for each stateful workload. Retain blocked scheduling reasons, time to replacement and surviving capacity. A healthy quorum alone cannot demonstrate that a workload can start.
