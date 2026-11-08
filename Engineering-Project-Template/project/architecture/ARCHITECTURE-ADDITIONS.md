# Architecture additions inventory

One-time delivery for `project/architecture`, 7 November 2026. **53 new Markdown documents and 56 new directories** were added. The document count includes this inventory. The original seven topic directories are listed below as starting points. All paths in this inventory are relative to the architecture root.

## Start here

- To apply the framework to a project, open the [architecture field guide](framework/README.md).
- To design and implement a reusable framework, follow the [charter](framework/framework-design/01-charter/purpose-and-design-principles.md), [artifact model](framework/framework-design/02-structure/artifact-model-and-viewpoints.md) and [adoption pilot](framework/framework-design/03-adoption/pilot-and-improvement.md).
- To see a complete decision trace, start with the [field-observation example](framework/examples/field-observations/01-frame/mission-and-options.md).
- For the creation procedure, read the [process record](framework/stewardship/how-this-extension-was-built.md). For the basis of the guidance, read the [primary reference crosswalk](framework/reference/framework-crosswalk.md).

## Delivery by purpose

| Addition | Documents |
| --- | ---: |
| Guidance nested in the seven original areas | 15 |
| Field guide and five-phase architecture method | 8 |
| Designing, structuring and piloting a framework | 3 |
| Cross-cutting architecture concerns | 8 |
| Project-type profiles | 8 |
| Fillable text worksheets | 4 |
| Worked example from framing to evidence | 3 |
| References and glossary | 2 |
| Creation and verification record | 1 |
| This inventory | 1 |
| **Total** | **53** |

## Starting directories

- `capacity-planning/`
- `component-design/`
- `data-flows/`
- `decisions/`
- `dependency-boundaries/`
- `system-context/`
- `trust-boundaries/`

## Added directories

The following 56 paths were created. Parent and leaf directories each have their own entry.

- `capacity-planning/modeling/`
- `capacity-planning/modeling/saturation/`
- `component-design/structure/`
- `component-design/structure/runtime/`
- `data-flows/information/`
- `data-flows/information/exchange/`
- `decisions/records/`
- `decisions/records/evidence/`
- `dependency-boundaries/contracts/`
- `dependency-boundaries/contracts/evolution/`
- `dependency-boundaries/contracts/physical/`
- `framework/`
- `framework/concerns/`
- `framework/concerns/assurance/`
- `framework/concerns/change/`
- `framework/concerns/economics/`
- `framework/concerns/human-factors/`
- `framework/concerns/operations/`
- `framework/concerns/physical-and-deployment/`
- `framework/concerns/resilience/`
- `framework/concerns/sourcing/`
- `framework/examples/`
- `framework/examples/field-observations/`
- `framework/examples/field-observations/01-frame/`
- `framework/examples/field-observations/02-design/`
- `framework/examples/field-observations/03-evaluate/`
- `framework/framework-design/`
- `framework/framework-design/01-charter/`
- `framework/framework-design/02-structure/`
- `framework/framework-design/03-adoption/`
- `framework/method/`
- `framework/method/01-frame/`
- `framework/method/02-design/`
- `framework/method/03-evaluate/`
- `framework/method/04-realize/`
- `framework/method/05-evolve/`
- `framework/profiles/`
- `framework/profiles/business-systems/`
- `framework/profiles/data-products/`
- `framework/profiles/enterprise-systems/`
- `framework/profiles/evolution/`
- `framework/profiles/field-systems/`
- `framework/profiles/physical-systems/`
- `framework/profiles/product-families/`
- `framework/profiles/shared-services/`
- `framework/reference/`
- `framework/stewardship/`
- `framework/worksheets/`
- `framework/worksheets/assurance/`
- `framework/worksheets/decisions/`
- `framework/worksheets/design/`
- `framework/worksheets/framing/`
- `system-context/framing/`
- `system-context/framing/operating-environment/`
- `trust-boundaries/protection/`
- `trust-boundaries/protection/assurance/`

## Added files

### Architecture root

- [ARCHITECTURE-ADDITIONS.md](ARCHITECTURE-ADDITIONS.md) — This inventory, created after the guides and their verification.

### capacity-planning

- [capacity-planning/modeling/saturation/backlog-and-load-shedding.md](capacity-planning/modeling/saturation/backlog-and-load-shedding.md) — Bound backlog and design overload behavior
- [capacity-planning/modeling/workload-and-budgets.md](capacity-planning/modeling/workload-and-budgets.md) — Model workload and allocate capacity

### component-design

- [component-design/structure/responsibility-and-state.md](component-design/structure/responsibility-and-state.md) — Assign responsibilities and authoritative state
- [component-design/structure/runtime/concurrency-and-invariants.md](component-design/structure/runtime/concurrency-and-invariants.md) — Preserve invariants under concurrency

### data-flows

- [data-flows/information/exchange/replay-and-reconciliation.md](data-flows/information/exchange/replay-and-reconciliation.md) — Reconcile attempts, facts and effects
- [data-flows/information/lifecycle-and-ownership.md](data-flows/information/lifecycle-and-ownership.md) — Map information from capture to retirement

### decisions

- [decisions/records/evidence/experiments-and-reversibility.md](decisions/records/evidence/experiments-and-reversibility.md) — Choose evidence proportionate to the decision
- [decisions/records/options-and-consequences.md](decisions/records/options-and-consequences.md) — Record why an architectural choice was made

### dependency-boundaries

- [dependency-boundaries/contracts/direction-and-change.md](dependency-boundaries/contracts/direction-and-change.md) — Map dependency direction and contract ownership
- [dependency-boundaries/contracts/evolution/compatibility-and-exit.md](dependency-boundaries/contracts/evolution/compatibility-and-exit.md) — Design interface evolution and supplier exit
- [dependency-boundaries/contracts/physical/interfaces-and-tolerances.md](dependency-boundaries/contracts/physical/interfaces-and-tolerances.md) — Engineer a physical interface

### Framework / concerns

- [framework/concerns/assurance/hazards-and-evidence.md](framework/concerns/assurance/hazards-and-evidence.md) — Trace hazards to controls and evidence
- [framework/concerns/change/rollout-and-rollback.md](framework/concerns/change/rollout-and-rollback.md) — Plan rollout, rollback and forward recovery
- [framework/concerns/economics/lifecycle-and-resource-cost.md](framework/concerns/economics/lifecycle-and-resource-cost.md) — Compare whole-life cost and constrained resources
- [framework/concerns/human-factors/accessibility-and-control.md](framework/concerns/human-factors/accessibility-and-control.md) — Design human authority, accessibility and handoff
- [framework/concerns/operations/observable-and-operable-design.md](framework/concerns/operations/observable-and-operable-design.md) — Make system state observable and operable
- [framework/concerns/physical-and-deployment/allocation-and-placement.md](framework/concerns/physical-and-deployment/allocation-and-placement.md) — Allocate functions to people, devices and infrastructure
- [framework/concerns/resilience/failure-domains-and-recovery.md](framework/concerns/resilience/failure-domains-and-recovery.md) — Design for failure, recovery and integrity
- [framework/concerns/sourcing/make-buy-and-exit.md](framework/concerns/sourcing/make-buy-and-exit.md) — Decide what to build, buy or depend on

### Framework / examples

- [framework/examples/field-observations/01-frame/mission-and-options.md](framework/examples/field-observations/01-frame/mission-and-options.md) — Field observations, part 1 — mission and options
- [framework/examples/field-observations/02-design/views-and-contracts.md](framework/examples/field-observations/02-design/views-and-contracts.md) — Field observations, part 2 — views and contracts
- [framework/examples/field-observations/03-evaluate/evidence-and-disposition.md](framework/examples/field-observations/03-evaluate/evidence-and-disposition.md) — Field observations, part 3 — evidence and disposition

### Framework / framework-design

- [framework/framework-design/01-charter/purpose-and-design-principles.md](framework/framework-design/01-charter/purpose-and-design-principles.md) — Design a framework for a class of projects
- [framework/framework-design/02-structure/artifact-model-and-viewpoints.md](framework/framework-design/02-structure/artifact-model-and-viewpoints.md) — Define the artifact model and viewpoint catalog
- [framework/framework-design/03-adoption/pilot-and-improvement.md](framework/framework-design/03-adoption/pilot-and-improvement.md) — Pilot, implement and improve the framework

### Framework / method

- [framework/method/01-frame/quality-attribute-scenarios.md](framework/method/01-frame/quality-attribute-scenarios.md) — Turn quality goals into measurable scenarios
- [framework/method/01-frame/tailoring-and-ownership.md](framework/method/01-frame/tailoring-and-ownership.md) — Tailor the work and name the owners
- [framework/method/02-design/views-and-correspondence.md](framework/method/02-design/views-and-correspondence.md) — Select views and check their agreement
- [framework/method/03-evaluate/tradeoff-review.md](framework/method/03-evaluate/tradeoff-review.md) — Run a scenario-based tradeoff review
- [framework/method/04-realize/design-to-implementation.md](framework/method/04-realize/design-to-implementation.md) — Carry the design into implementation
- [framework/method/05-evolve/change-and-retirement.md](framework/method/05-evolve/change-and-retirement.md) — Evolve and retire an architecture
- [framework/method/05-evolve/governance-and-exceptions.md](framework/method/05-evolve/governance-and-exceptions.md) — Set decision rights and handle exceptions

### Framework / profiles

- [framework/profiles/business-systems/modular-transactions.md](framework/profiles/business-systems/modular-transactions.md) — Profile for a modular business system
- [framework/profiles/data-products/analytics-and-ml.md](framework/profiles/data-products/analytics-and-ml.md) — Profile for analytical data and machine learning
- [framework/profiles/enterprise-systems/capabilities-and-transitions.md](framework/profiles/enterprise-systems/capabilities-and-transitions.md) — Profile for enterprise capabilities and federated systems
- [framework/profiles/evolution/legacy-modernization.md](framework/profiles/evolution/legacy-modernization.md) — Profile for modernization and replacement
- [framework/profiles/field-systems/disconnected-edge.md](framework/profiles/field-systems/disconnected-edge.md) — Profile for intermittently connected systems
- [framework/profiles/physical-systems/control-and-protection.md](framework/profiles/physical-systems/control-and-protection.md) — Profile for physical control and protection
- [framework/profiles/product-families/variation-and-configuration.md](framework/profiles/product-families/variation-and-configuration.md) — Profile for product families and engineered variants
- [framework/profiles/shared-services/tenant-isolation.md](framework/profiles/shared-services/tenant-isolation.md) — Profile for shared and distributed services

### Framework / reference

- [framework/reference/field-glossary.md](framework/reference/field-glossary.md) — Field glossary
- [framework/reference/framework-crosswalk.md](framework/reference/framework-crosswalk.md) — Framework crosswalk and primary references

### Framework / stewardship

- [framework/stewardship/how-this-extension-was-built.md](framework/stewardship/how-this-extension-was-built.md) — Creation and verification record

### Framework / worksheets

- [framework/worksheets/assurance/scenario-and-review.md](framework/worksheets/assurance/scenario-and-review.md) — Worksheet for scenario evidence and risk disposition
- [framework/worksheets/decisions/decision-and-experiment.md](framework/worksheets/decisions/decision-and-experiment.md) — Worksheet for a decision and its experiment
- [framework/worksheets/design/view-and-interface.md](framework/worksheets/design/view-and-interface.md) — Worksheet for a view and its interfaces
- [framework/worksheets/framing/architecture-brief.md](framework/worksheets/framing/architecture-brief.md) — Worksheet for a project architecture brief

### Framework entry point

- [framework/README.md](framework/README.md) — Architecture field guide

### system-context

- [system-context/framing/operating-environment/modes-and-authority.md](system-context/framing/operating-environment/modes-and-authority.md) — Analyze operating modes and authority
- [system-context/framing/scope-and-mission.md](system-context/framing/scope-and-mission.md) — Establish scope and mission

### trust-boundaries

- [trust-boundaries/protection/assurance/threats-and-privacy.md](trust-boundaries/protection/assurance/threats-and-privacy.md) — Evaluate abuse, disclosure and privacy
- [trust-boundaries/protection/identity-and-authority.md](trust-boundaries/protection/identity-and-authority.md) — Place identity and authority at trust boundaries

## Verification at delivery

Before writing this inventory, all 52 guide, worksheet, example and process documents matched the authored text on read-back. All 205 internal links resolved and all 52 documents were reachable from the field guide. Seven publisher references appear in the crosswalk. The verified directory set contained the seven original directories and the 56 declared additions.

The worked field example's inputs yield 86,400 observations, 51,840,000 payload bytes and a three-hour ideal drain at ten confirmed observations per second with two new arrivals per second. The minimum rate for exactly four hours is eight per second. The example identifies which further claims require measurements on real equipment.

[Architecture field guide](framework/README.md)
