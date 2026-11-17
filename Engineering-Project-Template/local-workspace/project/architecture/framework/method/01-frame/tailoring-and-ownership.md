# Tailor the work and name the owners

Start by identifying the next expensive commitment. Tooling, procurement, a shared protocol, a public promise or a field installation can all narrow future options. The architecture work before that commitment should reduce the uncertainty that could make it a mistake.

## Size the decision

| Signal | Smallest useful treatment | When to expand |
| --- | --- | --- |
| One team, reversible change, familiar operating envelope | One-page brief, context sketch, critical scenario, decision entry | Another owner starts relying on an undocumented behavior |
| Multiple teams, stored data, independent releases | Contract, state owner, mixed-version scenario, recovery test | Changing a field or stopping a writer requires synchronized cutover |
| Irreversible physical action, sensitive records or scarce replacement parts | Trace from loss to controls, independence assumptions, specialist review and lifecycle budget | A common cause can defeat the claimed protection |
| Several products or organizational units | Baseline, target and transition states with capability and funding owners | Local optimization transfers cost or risk to another unit |
| Prototype with unknown feasibility | A bounded research question, experiment, stop condition and handoff criteria | A real user, operational duty or long-lived record depends on it |

## Allocate decision rights

Give one person or named role responsibility for deciding. Identify the owners of each affected interface and the people authorized to accept the remaining exposure. Where ownership crosses organizations, name the mechanism for agreeing to change, the notice window and a way to operate when the parties disagree. A partner can own a radio network while the product team owns handling late data.

Ask an implementer to estimate the work to reverse the choice. Ask an operator to estimate recovery time at night with the staff actually available. Ask the sponsor how long a wrong choice can be tolerated. Record any disagreement as an assumption to test. A fixed deadline with a negotiable feature is a different constraint from a mandatory physical limit.

## Exit from framing

Complete the [brief](../../worksheets/framing/architecture-brief.md) with the first decision, accountable role and next evidence. Mark a deferred concern with a reason and a trigger. An internal utility with local-only storage might defer multi-region placement until distribution becomes a requirement. Revisit that entry when the boundary moves. See [decision rights and exceptions](../05-evolve/governance-and-exceptions.md) for commitments affecting others.

[Architecture field guide](../../README.md)
