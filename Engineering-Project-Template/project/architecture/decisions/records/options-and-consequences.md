# Record why an architectural choice was made

Write an architecture decision record (ADR) when a choice changes a shared promise, binds multiple owners, or is expensive to reverse. Begin with the question while alternatives are still credible. A completed record should let a successor reconstruct the reasoning with the evidence available at the time.

## Write the decision

1. State the question, scope, decision owner and date by which further delay has a cost. Name the actors who inherit the consequences.
2. Separate mission, hard constraints, quality goals and assumptions. Attach a measurement or evidence owner to influential assumptions.
3. Compare at least two credible approaches where alternatives exist. Include keeping the current design if it can satisfy the mission. Explain infeasible options through the constraint they violate.
4. State the choice, rationale, accepted cost, dissent, confidence and dependencies. Give reversal a sequence, estimated effort and last safe point.
5. Assign the experiment or acceptance check, its owner and an observable condition that would reopen the decision. Record status and link superseding decisions while preserving historical context.

## Example of an option boundary

For a six-hour radio outage, buffering at a site gateway can protect an upstream backhaul failure while the device-to-gateway hop remains available. A device buffer covers either hop and adds local storage, recovery and wear obligations. Rejecting capture during an outage can be an honest option when the mission permits gaps. Ask which link can fail, how a user knows a reading was accepted, and what a replacement device does with its predecessor's state.

A decision may be proposed pending endurance data. Acceptance authorizes the selected direction within specified conditions. A passing test applies to the tested configuration and workload. Give the person accepting residual risk the actual observation and the conditions still untested.

A newcomer can use the [decision worksheet](../../framework/worksheets/decisions/decision-and-experiment.md) to write the question and alternatives. A principal reviewer should try to identify plausible evidence that would reverse the choice. If none exists, determine whether the team has an actual constraint or an unexamined preference.

[Architecture field guide](../../framework/README.md)
