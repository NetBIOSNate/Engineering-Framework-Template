# Architecture field guide

Use this guide when a project needs to decide who owns a capability, how its parts interact, or what evidence would justify committing to a design. The deliverable for a project is a set of decisions that people can build, operate and revisit. Choose the smallest set of views that makes those decisions inspectable.

## First hour on a new project

1. Ask an intended user to describe one successful outcome and one costly failure. Ask an operator what happens after hours. Put the answers, the accountable owner and the boundary in the [architecture brief](worksheets/framing/architecture-brief.md).
2. Follow the outcome from the initiating person or device to the visible result. Annotate each handoff with its owner and the meaning of success. Use the [scope guide](../system-context/framing/scope-and-mission.md).
3. Turn the failure into a [measurable scenario](method/01-frame/quality-attribute-scenarios.md). Write down what would cause the team to change its first design.
4. Sketch two credible ways to preserve the outcome. Choose one uncertainty to resolve before committing money, interfaces or a rollout date. Record it in the [decision worksheet](worksheets/decisions/decision-and-experiment.md).

## Choose a reading path

| Reader | Start here | A useful first output |
| --- | --- | --- |
| First-time designer | [Field glossary](reference/field-glossary.md) and [worked example](examples/field-observations/01-frame/mission-and-options.md) | Explain the boundary and one failure in your own words |
| Implementing engineer | [Design views](method/02-design/views-and-correspondence.md), [state ownership](../component-design/structure/responsibility-and-state.md), [implementation handoff](method/04-realize/design-to-implementation.md) | Trace a decision to an interface contract and an acceptance check |
| Project or discipline lead | [Tailoring](method/01-frame/tailoring-and-ownership.md), [tradeoff review](method/03-evaluate/tradeoff-review.md), [recovery](concerns/resilience/failure-domains-and-recovery.md) | Identify one unowned risk and the cheapest evidence that could retire it |
| Principal engineer or reviewer | [Decision rights](method/05-evolve/governance-and-exceptions.md), [whole-life cost](concerns/economics/lifecycle-and-resource-cost.md), [retirement](method/05-evolve/change-and-retirement.md) | Decide where flexibility pays for itself and who accepts the residual exposure |

## Navigate by architectural question

| Question | Working guides |
| --- | --- |
| Where does authority change hands? | [Mission and scope](../system-context/framing/scope-and-mission.md) · [Modes and authority](../system-context/framing/operating-environment/modes-and-authority.md) |
| Who owns a rule under concurrent use? | [Responsibilities](../component-design/structure/responsibility-and-state.md) · [State invariants](../component-design/structure/runtime/concurrency-and-invariants.md) |
| What happens to information after capture? | [Lifecycle](../data-flows/information/lifecycle-and-ownership.md) · [Reconciliation](../data-flows/information/exchange/replay-and-reconciliation.md) |
| How can two things evolve independently? | [Dependency direction](../dependency-boundaries/contracts/direction-and-change.md) · [Compatibility](../dependency-boundaries/contracts/evolution/compatibility-and-exit.md) · [Physical interfaces](../dependency-boundaries/contracts/physical/interfaces-and-tolerances.md) |
| Which principal can make which change? | [Trust boundaries](../trust-boundaries/protection/identity-and-authority.md) · [Threats and privacy](../trust-boundaries/protection/assurance/threats-and-privacy.md) |
| How much work fits during failure and recovery? | [Demand and budgets](../capacity-planning/modeling/workload-and-budgets.md) · [Backpressure](../capacity-planning/modeling/saturation/backlog-and-load-shedding.md) |
| Why commit now and what would change the decision? | [Decision records](../decisions/records/options-and-consequences.md) · [Experiments](../decisions/records/evidence/experiments-and-reversibility.md) |
| Can the design survive placement, rollout and field operation? | [Allocation](concerns/physical-and-deployment/allocation-and-placement.md) · [Rollout](concerns/change/rollout-and-rollback.md) · [Operability](concerns/operations/observable-and-operable-design.md) · [Human factors](concerns/human-factors/accessibility-and-control.md) |
| What deserves specialist or supplier review? | [Hazard assurance](concerns/assurance/hazards-and-evidence.md) · [Sourcing and exit](concerns/sourcing/make-buy-and-exit.md) |

## Adapt the method

Follow the five phases in directory order under `method`. Return to an earlier phase whenever evidence changes a driver. The [framework crosswalk](reference/framework-crosswalk.md) explains which questions each reference helps answer. Worksheets cover the [brief](worksheets/framing/architecture-brief.md), [view and interface](worksheets/design/view-and-interface.md), [decision](worksheets/decisions/decision-and-experiment.md) and [scenario review](worksheets/assurance/scenario-and-review.md). Copy the fields into the project's chosen record system. Keep a link to each authoritative record.

Choose the profile closest to the expensive failure. A field instrument may need both [control and protection](profiles/physical-systems/control-and-protection.md) and [disconnected edge](profiles/field-systems/disconnected-edge.md). A reporting service may need [analytical lineage](profiles/data-products/analytics-and-ml.md), [business transactions](profiles/business-systems/modular-transactions.md) or [tenant isolation](profiles/shared-services/tenant-isolation.md). Use [modernization](profiles/evolution/legacy-modernization.md) when old and new authorities must coexist.

The worked example follows [mission and options](examples/field-observations/01-frame/mission-and-options.md), [views and contracts](examples/field-observations/02-design/views-and-contracts.md) and [evaluation and disposition](examples/field-observations/03-evaluate/evidence-and-disposition.md). Its numerical targets and test outcomes are explicitly labeled. The [creation record](stewardship/how-this-extension-was-built.md) describes how the library was assembled and verified.
