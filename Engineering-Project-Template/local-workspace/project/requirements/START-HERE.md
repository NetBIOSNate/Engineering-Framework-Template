# Requirements planning field guide

Start with the next decision that commits people, money, an interface or permission to operate. Identify who will live with the consequences and what observation could change that decision. Use the guides below to work from the need to an architecture and a defensible acceptance decision.

## Choose a starting point

| If you are working as… | Do this first | Leave with |
| --- | --- | --- |
| A new engineer or student | Reconstruct a failed handoff in the [first planning session](framework/adoption/learning/first-planning-session.txt). | One need, one observable obligation and one way to challenge it. |
| A practitioner | Fill in a [requirement card](framework/worksheets/specification/requirement-card.txt) and take it to both owners of the boundary. | A measure, an allocation and an agreed verification case. |
| A project or discipline lead | Choose the depth of the work using the [tailoring agreement](framework/worksheets/reuse/project-tailoring-record.txt). | A commitment date, accountable people and evidence needed before that date. |
| A principal engineer or reviewer | Examine a disputed decision against its [options and residual exposure](framework/worksheets/decisions/options-and-risk.txt), then apply the [review criteria](framework/adoption/reviews/entry-exit-and-decision-rights.txt). | The conditions to advance, restrict use, investigate or hold. |
| A framework steward | Follow the [charter](framework/design/01-charter/decisions-and-scope.txt), [record model](framework/design/02-information-model/records-and-relationships.txt) and [adoption pilot](framework/design/05-adoption/pilot-and-calibrate.txt). | A reusable framework that two different project teams can apply to real decisions. |

## Run one decision from start to finish

1. Establish who needs the outcome, how the work happens today and where the boundary lies. Capture normal, degraded, service and retirement conditions. [Need and operating envelope](framework/worksheets/intake/need-and-operating-envelope.txt)
2. Identify which obligations could alter the architecture. Allocate them to components, people, suppliers and interfaces. Give cross-cutting obligations an owner for the integrated result. [Trace and coverage register](framework/worksheets/allocation/trace-and-coverage.txt)
3. Compare feasible designs against the same operating conditions. Challenge the assumption that can reverse the choice. Record the consequence and a trigger to revisit it. [Decision workshops](framework/workshops)
4. Sequence the first integration trial around the most consequential uncertainty. Send implementers the agreed limits, interface revision, permitted variation and expected observations. [Integration order](framework/workshops/strategy/integration-order-and-learning.txt) · [Existing template handoffs](framework/adoption/handoffs/existing-template-destinations.txt)
5. Verify the agreed obligations and validate that representative people can complete the intended work. The acceptance authority records the authorized configuration, conditions and remaining exposure. [Evidence worksheet](framework/worksheets/evidence/verification-and-validation.txt)
6. Follow a change backward to the need and forward to affected owners and evidence. Record what can still be credited and what must be repeated. [Change impact worksheet](framework/worksheets/change/impact-and-release.txt)

For a small project, one page can hold this entire chain. Add a deeper record at a point of disagreement, an ownership boundary or an expensive commitment. The [guide catalog](framework/navigation/guide-catalog.md) gives a direct link to each guide and worksheet, including the seven subject areas and all four game-design branches.

## Work through a complete example

A disconnected inspection bench can retain a measurement while its authority to publish remains uncertain. Predict the disposition of a measurement whose capture interval crosses the calibration deadline, then compare your reasoning to the recorded result. The case carries stable IDs across four short chapters.

[1. Need and agreement](framework/examples/inspection-bench/01-frame/need-and-agreement.txt) · [2. Requirements and design](framework/examples/inspection-bench/02-allocate/requirements-and-design.txt) · [3. Failed and passing cases](framework/examples/inspection-bench/03-verify/cases-and-results.txt) · [4. Change and scoped acceptance](framework/examples/inspection-bench/04-accept/change-and-operational-validation.txt)

## Find the basis for a planning decision

The [standards and methods crosswalk](framework/reference/industry/standards-and-methods.txt) points to the publisher pages and identifies the local use of each reference. The [glossary](framework/reference/language/working-glossary.txt) explains terms that often differ between disciplines. Use the adjacent [architecture field guide](../architecture/framework/README.md) to develop the resulting views, contracts and decisions.

The [creation and verification record](framework/stewardship/delivery/creation-and-verification.txt) documents this one-time extension. The complete additions inventory is at the template root, two directories above this guide, in REQUIREMENTS-ADDITIONS.txt.
