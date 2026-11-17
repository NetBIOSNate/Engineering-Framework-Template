# Profile for physical control and protection

Use this path when timing, the physical environment or an unsafe command can determine the system outcome. Begin with the operating modes and the physical definition of an allowed state. Bring an operator, the control designer, the person responsible for the hazard analysis and someone who maintains the installed equipment.

## Decisions to resolve early

Separate supervisory commands from local control authority. Allocate sensing, filtering, scheduling, communication, decision and actuation delays. Decide where the system can enforce a protective transition when external communication is lost. Map shared power, clock, cabling, sensor and environmental dependencies. Specify who may override, under which conditions, and how the system confirms that maintenance has ended.

## Worked timing allocation

A fictional training rig must reach a defined state within 120 ms of a simulated guard opening. Suppose serial upper-bound allocations are 15 ms sensing, 10 ms filtering, 15 ms scheduling, 5 ms decision, 15 ms communication and 40 ms physical actuation. Their sum is 100 ms, leaving 20 ms for uncertainty or unallocated delay. Verify what each bound includes. Polling phase, interrupt delay, relay travel, aging and temperature can each consume margin. If two terms overlap, justify the overlap with actual scheduling evidence.

Witness time from physical stimulus to observed physical state at representative worst load. Exercise loss of supervision, stuck input, power restoration and an attempted restart during maintenance in an appropriate test setting. A missed deadline, unintended transition or restart without required authority reopens the allocation. A finite run does not establish a hard upper bound. The hazard owner identifies the additional analysis and evidence needed for operation.

**Deliverable.** A mode table, labeled physical interfaces, timing allocation, hazard-to-control trace and verification plan. A junior engineer can trace the longest serial path. A lead should challenge each independence assumption and confirm who accepts the remaining exposure. Use [interface tolerances](../../../dependency-boundaries/contracts/physical/interfaces-and-tolerances.md), [modes](../../../system-context/framing/operating-environment/modes-and-authority.md) and [assurance arguments](../../concerns/assurance/hazards-and-evidence.md).

[Architecture field guide](../../README.md)
