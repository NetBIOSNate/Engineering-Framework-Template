# Trace hazards to controls and evidence

Begin with the loss someone cares about, the hazardous system state that can lead to it and the operating conditions that make the transition credible. Separate the state, cause, harm and mitigation. A failed link is a possible cause. Continued motion while a person is in the service area is a hazardous state. The distinction helps identify other causes that can lead to the same loss.

## Construct a small assurance argument

| Element | Example for a simulated training rig |
| --- | --- |
| Claim | The rig reaches its defined protective state within the allocated time after the guard opens |
| Context | Agreed operating modes, load, environment, maintenance bypass rules and physical definition of the state |
| Argument | Sensing, decision and actuation together bound response, with identified common-cause dependencies addressed |
| Evidence | Timing analysis, calibrated stimulus-to-physical-state measurements and fault-injection observations |
| Defeater | A common power or sensor failure defeats both nominal control and protection |
| Disposition | Hazard owner determines whether redesign, additional evidence or restricted operation is required |

## Select the analysis technique

A bottom-up failure modes and effects analysis asks what each element's failure does to the system and how it is detected. A top-down fault tree starts at a defined unwanted outcome and identifies combinations that can cause it. A control-oriented analysis asks when issuing, omitting, mistiming or maintaining a control action can be hazardous even if parts function as designed. Choose the lens that matches the uncertainty. Revisit independence assumptions before assigning probabilities to combinations.

Trace each control to an enforcing component, an operational procedure where appropriate, a verification method and a person with authority over residual risk. Include startup, maintenance, bypass, degraded operation and restart. Require evidence of a physical or operational effect when the claim concerns that effect.

A finite test campaign provides observations within its tested envelope. A hard real-time or independence claim can also require analysis, design inspection, environmental evidence and specialist judgment. Project authorities determine the sector-specific obligations and sufficient evidence. Use the [control-system profile](../../profiles/physical-systems/control-and-protection.md) for an illustrative timing allocation.

[Architecture field guide](../../README.md)
