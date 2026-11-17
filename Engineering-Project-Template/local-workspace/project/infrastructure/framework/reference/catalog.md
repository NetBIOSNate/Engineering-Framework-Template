# Infrastructure guide catalog

Browse by the decision you need to make. Begin with the [field guide](../START-HERE.md) for a role-based reading path. The [delivery inventory](../../INFRASTRUCTURE-ADDITIONS.md) gives exact paths and integrity digests.

## Orient and adopt

Start here for reader routes, lifecycle reviews, a native Windows exercise and the environment handoffs.

- [Infrastructure framework field guide](../START-HERE.md)
- [How this infrastructure library was assembled and verified](../adoption/authoring/installation-record.md)
- [Environment contracts and promotion evidence](../adoption/environments/promotion-matrix.md)
- [A first infrastructure design in an afternoon](../adoption/learning/first-walkthrough.md)
- [Trace a Windows client connection from name to service](../adoption/learning/windows/read-only-path-check.md)
- [Lifecycle from discovery to retirement](../adoption/lifecycle/stage-gates.md)

## Design the system

Define outcomes, architecture boundaries, ownership, module contracts and transition choices.

- [Map ownership and shared dependencies](../design/boundaries/ownership/service-map.md)
- [Assemble modules into an environment](../design/composition/bindings/environment-assembly.md)
- [Specify a reusable infrastructure module](../design/composition/contracts/module-interface.md)
- [Choose topology against a failure model](../design/decisions/topology/failure-domains.md)
- [Turn constraints into testable targets](../design/requirements/quality/targets.md)
- [Adopt infrastructure that already serves consumers](../design/transition/brownfield/coexistence.md)

## Design the platform

Follow a dependency down to its physical or logical implementation and acceptance test.

- [Bare-metal bootstrap and out-of-band recovery](../design/platform/compute/bootstrap/bare-metal-bootstrap.md)
- [Choose an execution environment](../design/platform/compute/placement/compute-placement.md)
- [Cluster scheduling and control-plane continuity](../design/platform/compute/scheduling/control-plane.md)
- [Cache correctness, refill and failure amplification](../design/platform/data/cache/invalidation.md)
- [Choose acknowledgement and fencing under a partition](../design/platform/data/replication/partition-and-fencing.md)
- [Power, cooling and physical failure domains](../design/platform/facilities/power/facility-power-and-cooling.md)
- [Design segmented connectivity and address allocation](../design/platform/network/addressing/segmented-connectivity-and-ipam.md)
- [Bootstrap DNS, time and certificates](../design/platform/network/naming/trust/dns-time-and-pki.md)
- [Ingress, egress and overload at the service boundary](../design/platform/network/traffic/ingress-egress.md)
- [WAN routing and dual-stack diagnosis](../design/platform/network/wan/routing/wan-routing-and-dual-stack.md)
- [Choose storage tiers and prove recovery](../design/platform/storage/durability/storage-durability-and-rebuild.md)
- [Establish a landing zone across ownership boundaries](../design/platform/tenancy/hybrid/hybrid-tenancy-and-landing-zones.md)

## Reusable module contracts

Open the existing module that owns the capability. Each contract identifies inputs, behavior, commissioning and a failure exercise.

- [Artifact storage and distribution](../../modules/artifact-storage/CAPABILITY.md)
- [Build agents and privileged execution](../../modules/build-agents/CAPABILITY.md)
- [Compute pools and failure placement](../../modules/compute/CAPABILITY.md)
- [Database infrastructure and writer ownership](../../modules/databases/CAPABILITY.md)
- [Identity federation and recovery access](../../modules/identity/CAPABILITY.md)
- [Queues, replay and overload](../../modules/messaging/CAPABILITY.md)
- [Network reachability and isolation](../../modules/networking/CAPABILITY.md)
- [Infrastructure signals and independent monitoring](../../modules/observability/CAPABILITY.md)
- [Independent recovery capability](../../modules/recovery/CAPABILITY.md)
- [Storage services and retained data](../../modules/storage/CAPABILITY.md)

## Environment policy guides

Each row covers one environment. Read across it when assembling a deployment.

| Environment | Access | Network | Resources |
| --- | --- | --- | --- |
| development | [Development access and developer autonomy](../../environment-definitions/development/access-policy-definitions/GUIDE.md) | [Development network boundaries](../../environment-definitions/development/network-policy-definitions/GUIDE.md) | [Disposable development capacity](../../environment-definitions/development/resource-definitions/GUIDE.md) |
| testing | [Test identities and evidence custody](../../environment-definitions/testing/access-policy-definitions/GUIDE.md) | [Isolated network test cells](../../environment-definitions/testing/network-policy-definitions/GUIDE.md) | [Repeatable failure and load fixtures](../../environment-definitions/testing/resource-definitions/GUIDE.md) |
| staging | [Rehearse production authority in staging](../../environment-definitions/staging/access-policy-definitions/GUIDE.md) | [Stage representative traffic and cutovers](../../environment-definitions/staging/network-policy-definitions/GUIDE.md) | [Qualify resource definitions for promotion](../../environment-definitions/staging/resource-definitions/GUIDE.md) |
| production | [Production administration and emergency custody](../../environment-definitions/production/access-policy-definitions/GUIDE.md) | [Production ingress, egress and management](../../environment-definitions/production/network-policy-definitions/GUIDE.md) | [Production capacity and ownership](../../environment-definitions/production/resource-definitions/GUIDE.md) |
| disaster-recovery | [Recovery identity during primary control-plane loss](../../environment-definitions/disaster-recovery/access-policy-definitions/GUIDE.md) | [Recovery routing and controlled failover](../../environment-definitions/disaster-recovery/network-policy-definitions/GUIDE.md) | [Recovery footprint, clean rebuild and failback](../../environment-definitions/disaster-recovery/resource-definitions/GUIDE.md) |

## Controls and delivery

Choose evidence for administration, supply chain, promotion, remediation and exit.

- [Keys, secrets and certificate rotation](../controls/cryptography/rotation/keys-and-secrets.txt)
- [Choose push, pull and emergency reconciliation behavior](../controls/delivery/automation/reconciliation.md)
- [Promotion, canaries and recovery from change](../controls/delivery/promotion/canary-and-recovery.txt)
- [Infrastructure-as-code module contracts, state and drift](../controls/delivery/state/module-state-and-drift.txt)
- [Risk exceptions, evidence and decision rights](../controls/governance/exceptions/risk-and-evidence.txt)
- [Supplier support, concentration and exit](../controls/governance/suppliers/exit-and-support.md)
- [Access boundaries and tenant isolation](../controls/identity/tenancy/access-boundaries.txt)
- [Infrastructure retirement and media sanitization](../controls/lifecycle/retirement/sanitization-and-closure.txt)
- [Threat-model an infrastructure change](../controls/security/design/threat-model.md)
- [Host hardening, vulnerability response and firmware support](../controls/security/hardening/patch-lifecycle.md)
- [Infrastructure artifact provenance and supplier trust](../controls/supply-chain/verification/artifact-provenance.txt)

## Operate and recover

Use these guides during readiness, incident response, capacity reviews and recovery trials.

- [Failure exercises and game days](../operations/assurance/exercises/failure-exercises.md)
- [Backup chains and restored integrity](../operations/continuity/backup/integrity/backup-integrity.md)
- [Disaster recovery and failback](../operations/continuity/recovery/failback/recovery-and-failback.md)
- [Allocate cost and decide when to change capacity](../operations/economics/allocation/unit-cost.md)
- [Energy and hardware lifecycle at a useful-work boundary](../operations/economics/sustainability/energy-and-utilization.md)
- [Reconcile intended resources with the estate that actually runs](../operations/inventory/discovery/asset-reconciliation.md)
- [Observability and telemetry delivery](../operations/observability/pipeline/telemetry-pipeline.md)
- [Capacity, performance and unit cost](../operations/planning/capacity/capacity-performance-and-cost.md)
- [Find capacity limits before the resource runs out](../operations/planning/quotas/exhaustion.md)
- [Service objectives and alerting](../operations/reliability/objectives/service-objectives.md)
- [On-call and incident command](../operations/response/on-call/incident-command.md)
- [Define the service and the team that can operate it](../operations/service-management/catalog/operating-model.md)

## Adapt to a deployment profile

Select the constraint that most changes the ordinary design and exercise its failure mode.

- [Accelerator clusters and tightly coupled batch work](../profiles/compute/hpc/accelerators/gpu-cluster.md)
- [Industrial infrastructure and maintenance windows](../profiles/industrial/ot/site-maintenance.md)
- [Regional placement and custodial boundaries](../profiles/regulated/residency/data-paths.md)
- [Edge sites with intermittent connections](../profiles/remote/edge/disconnected/store-and-forward.md)
- [Maintain and recover an air-gapped installation](../profiles/restricted/air-gap/transfer/trust-bundle.md)
- [Multi-tenant isolation and noisy neighbors](../profiles/shared/multitenant/noisy-neighbor.md)
- [A supportable single-site project](../profiles/small-project/single-site/minimum-footprint.md)

## Worked examples

Follow each example from operating assumptions to a decision the team can test.

- [Worked design review for a recoverable archive](../examples/archive-service/from-request-to-handover.md)
- [Worked commissioning review for a field station](../examples/field-station/design-to-commissioning.md)

## Reusable project records

Use the field prompts and worked fragments to record a project decision or observation.

- [Recovery trial evidence sheet](../records/assurance/exercises/recovery-trial.md)
- [Operational readiness and release decision](../records/assurance/readiness.md)
- [Infrastructure change and reversal packet](../records/delivery/change-packet.md)
- [Architecture decision record](../records/design/decision.md)
- [Dependency and flow register](../records/design/interfaces/dependency-register.md)
- [Time-bounded risk and exception record](../records/governance/risk-and-exception.md)
- [Project brief and infrastructure scope](../records/intake/project-brief.md)
- [Service record and operator handoff](../records/operations/service-record.md)
- [Capacity and degraded-state worksheet](../records/planning/capacity-model.md)

## Reference

Consult terminology and primary-source mappings when setting project criteria.

- [Industry frameworks and the evidence to produce](../reference/framework-crosswalk.md)
- [Terms used in infrastructure reviews](../reference/terms.md)
