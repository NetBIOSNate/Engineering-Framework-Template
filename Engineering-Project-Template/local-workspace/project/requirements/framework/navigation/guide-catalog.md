# Requirements guide catalog

Choose the question your team needs to answer and follow the linked guide. All guides open as local text. The numbered lifecycle and framework-design folders can also be read in sequence.

[Start here](../../START-HERE.md) · [First planning session](../adoption/learning/first-planning-session.txt) · [Reusable requirement card](../worksheets/specification/requirement-card.txt)

## Business outcomes

Define who benefits, what counts as improvement and who can resolve competing stakeholder interests. Put a baseline and a guardrail next to the target.

- [Mission measures and the decision to invest](../../business/outcomes/value/mission-measures.txt)
- [Resolve competing needs at the system boundary](../../business/stakeholders/authority/conflicting-needs.txt)

## Functional behavior

Describe the externally visible responses, modes, unexpected inputs and obligations that a design must preserve at each boundary.

- [Specify behavior across modes and interruptions](../../functional/behavior/modes/state-transitions.txt)
- [Allocate obligations across an interface](../../functional/interfaces/contracts/boundary-obligations.txt)

## Quality attributes

Choose the operating population and measurement boundary, then allocate a system limit and reserve enough margin to integrate the contributions.

- [Allocate budgets and preserve engineering margin](../../quality-attributes/allocation/budgets/end-to-end-margin.txt)
- [Set a quality target that will survive measurement](../../quality-attributes/scenarios/measurement/response-envelope.txt)

## Accessibility

Trace a complete task across interaction channels and interruptions. Identify where a person loses information or control and how they can finish independently.

- [Plan an accessible end-to-end task](../../accessibility/journeys/interaction/equivalent-actions.txt)
- [Preserve access during mode changes](../../accessibility/operations/degraded/multimodal-feedback.txt)

## Privacy

Trace personal information from its purpose through collection, derived copies, retention, restoration and disposal. Identify who can decide a change of use.

- [Plan disposition across copies and recovery](../../privacy/lifecycle/disposition/deletion-and-restoration.txt)
- [Derive data needs from decisions](../../privacy/lifecycle/purpose/minimum-data.txt)

## Game design

Connect intent about player experience to observable rules, the progression state, narrative continuity and balancing evidence. Select the branches that own the affected decisions.

- [Bound feedback loops in a resource economy](../../game-design/balancing/economy/feedback-and-exploits.txt)
- [Define rule authority and reproducible outcomes](../../game-design/mechanics/rules/authority-and-replay.txt)
- [Specify continuity across branching stories](../../game-design/narrative/branches/continuity-and-variants.txt)
- [Preserve earned progress across interruption and change](../../game-design/progression/persistence/checkpoints-and-migration.txt)

## Acceptance criteria

Define how to recognize conformance and fitness for use, who can make the decision and how uncertainty affects the verdict.

- [Design evidence before the architecture is fixed](../../acceptance-criteria/evidence/design/verification-cases.txt)
- [Validate fitness for an operating situation](../../acceptance-criteria/validation/operations/fitness-for-use.txt)

## Designing the framework

Follow the numbered branches to define its charter, information model, viewpoints, tailoring, pilot and governance. Use this route when the product is the reusable engineering framework itself.

- [Charter a reusable requirements framework](../design/01-charter/decisions-and-scope.txt)
- [Design the information model](../design/02-information-model/records-and-relationships.txt)
- [Select viewpoints from decisions](../design/03-viewpoints/choosing-and-checking-views.txt)
- [Tailor the depth of the evidence](../design/04-tailoring/risk-and-project-scale.txt)
- [Implement the framework on a real decision](../design/05-adoption/pilot-and-calibrate.txt)
- [Govern a baseline without freezing discovery](../design/06-governance/baselines-and-exceptions.txt)

## Applying the requirements lifecycle

Follow one real requirement through the stages. Revisit an earlier decision when a derived constraint, field observation or failed test invalidates an assumption.

- [The operating concept](../lifecycle/01-frame/mission/operating-concept.txt)
- [Elicit needs when stakeholders disagree](../lifecycle/01-frame/stakeholders/needs-and-conflicts.txt)
- [Select requirements that can change the architecture](../lifecycle/02-specify/drivers/priority-and-uncertainty.txt)
- [Turn a need into a verifiable obligation](../lifecycle/02-specify/statements/measurable-obligations.txt)
- [Specify an interface both parties can accept](../lifecycle/03-allocate/boundaries/interface-obligations.txt)
- [Divide a system budget among owners](../lifecycle/03-allocate/system/budgets-and-margins.txt)
- [Hand architectural obligations to delivery teams](../lifecycle/04-decide/handoff/design-and-realization.txt)
- [Choose among feasible architectures](../lifecycle/04-decide/options/sensitivity-and-tradeoffs.txt)
- [Validate the intended outcome](../lifecycle/05-assure/validation/operational-acceptance.txt)
- [Choose sufficient verification evidence](../lifecycle/05-assure/verification/evidence-design.txt)
- [Keep a baseline intelligible as the system changes](../lifecycle/06-steward/baselines/change-impact.txt)
- [Learn from service and close obligations](../lifecycle/06-steward/service/feedback-and-retirement.txt)

## Architectural decision workshops

Select the question that can change the design. Bring the people who own the two sides of the trade and leave with a decision, an explicit uncertainty or a planned experiment.

- [Budget restoration from the customer's clock](../workshops/continuity/restoration-and-backlog.txt)
- [Compare options over the period the owner must support](../workshops/economics/whole-life-options-and-sensitivity.txt)
- [Plan a change across independently governed systems](../workshops/enterprise/independent-authorities-and-transitions.txt)
- [Derive requirements from loss of control](../workshops/hazards/independence-and-control.txt)
- [Bring the factory, maintainer and end-of-life owner into the boundary](../workshops/physical-realization/manufacture-service-and-disposal.txt)
- [Translate a protection need into boundary requirements](../workshops/protection/authority-and-misuse.txt)
- [Turn a resource constraint into a whole-mission budget](../workshops/resources/duty-cycle-and-environment.txt)
- [Define what a supplier must deliver and what a project must retain](../workshops/sourcing/acquisition-and-exit.txt)
- [Sequence architecture work around the first expensive commitment](../workshops/strategy/integration-order-and-learning.txt)
- [Reuse a claim across a family of products](../workshops/variants/configurations-and-evidence-credit.txt)

## Profiles for specific operating conditions

Choose by failure consequence and operating envelope. Combine profiles when a system crosses domains and revisit the chosen numerical limits with the project owner.

- [Preserve business meaning across a cutover](../profiles/data-exchange/brownfield-cutover/identity-and-reconciliation.txt)
- [Keep observations attributable through a disconnection](../profiles/field-instruments/disconnected-operation/custody-and-replay.txt)
- [Transfer control without losing open work](../profiles/human-operated-systems/shift-handover/authority-and-open-work.txt)
- [Separate local feedback from shared outcomes](../profiles/interactive-systems/networked-play/latency-and-authority.txt)
- [Keep replacement parts interchangeable in the field](../profiles/manufactured-products/service-interchange/fit-across-variants.txt)
- [Safe state across a power interruption](../profiles/physical-control/stored-energy/power-loss-and-restart.txt)
- [Keep referred cases within human review capacity](../profiles/predictive-systems/population-shift/referral-and-model-release.txt)
- [Budget energy across a low-supply interval](../profiles/resource-constrained-systems/seasonal-energy/mode-and-reserve-budget.txt)
- [Define the decision at the measurement boundary](../profiles/scientific-measurement/calibration-drift/uncertainty-and-disposition.txt)
- [Bound interference between tenants](../profiles/shared-services/tenant-contention/admission-and-fairness.txt)

## Reusable records

Copy only the fields a project needs into its chosen record system. Record actual observations and acceptance authority separately from what a designer expects to happen.

- [Worksheet — Trace and coverage register](../worksheets/allocation/trace-and-coverage.txt)
- [Worksheet — Change impact and scope of approval](../worksheets/change/impact-and-release.txt)
- [Worksheet — Decision, options and residual exposure](../worksheets/decisions/options-and-risk.txt)
- [Worksheet — Evidence and acceptance decision](../worksheets/evidence/verification-and-validation.txt)
- [Worksheet — Need and operating envelope](../worksheets/intake/need-and-operating-envelope.txt)
- [Worksheet — Project tailoring agreement](../worksheets/reuse/project-tailoring-record.txt)
- [Worksheet — Requirement card](../worksheets/specification/requirement-card.txt)

## Worked inspection-bench example

Read in directory order to see one need cross a physical and information boundary, fail a verification case and reach a restricted operating decision. All results are illustrative.

- [Inspection bench — Decide which results may be released](../examples/inspection-bench/01-frame/need-and-agreement.txt)
- [Inspection bench — Allocate the release decision](../examples/inspection-bench/02-allocate/requirements-and-design.txt)
- [Inspection bench — Plan the oracle and inspect the evidence](../examples/inspection-bench/03-verify/cases-and-results.txt)
- [Inspection bench — Change the design and authorize a bounded use](../examples/inspection-bench/04-accept/change-and-operational-validation.txt)

## Learning, review and handoff

Match the record to the next commitment and put it in the hands of the discipline that owns the result.

- [Where requirements hand off to the existing template](../adoption/handoffs/existing-template-destinations.txt)
- [A first planning session](../adoption/learning/first-planning-session.txt)
- [Decide what the next commitment authorizes](../adoption/reviews/entry-exit-and-decision-rights.txt)

## Reference and vocabulary

Use the terminology across disciplines and consult publisher sources when choosing a project-specific standard or method.

- [How published frameworks inform this guide](../reference/industry/standards-and-methods.txt)
- [A glossary for cross-discipline reviews](../reference/language/working-glossary.txt)

## Creation and verification

Use the delivery record to understand the starting tree, the Windows authoring method and the checks used for the one-time extension.

- [How this extension was designed, installed and checked](../stewardship/delivery/creation-and-verification.txt)
- [Read the delivery inventory with Windows PowerShell](../stewardship/delivery/read-only-inventory-check.txt)
