# Carry the design into implementation

Translate each important architectural promise into a responsibility, a boundary and an observable check. Start with a thin end-to-end slice that crosses the riskiest real interface. Choose a representative storage medium, external contract or physical interface when its behavior is the uncertainty.

## Build an allocation table

| Design promise | Realization owner | Evidence before expanding scope |
| --- | --- | --- |
| A receipt survives loss of connectivity | Producer owns the durable write and publicly defined receipt boundary | Cut power after receipt, restart and recover the same stable identifier |
| Work remains isolated by customer | Resource owner authorizes each scoped operation | Exercise a valid identity with another customer's object key through direct, cached and restored reads |
| Recovery finishes within a window | Intake owner reserves catch-up capacity | Measure successful drain while new work continues and the slowest consumer is present |
| Service remains diagnosable in degraded mode | Operator-facing component exposes state age and pending work | Fresh operator distinguishes stale, rejected and pending without privileged database access |

## Sequence the work

Implement the boundary contract and a conformance example first. Exercise an ordinary case, then a case where the result is ambiguous to the caller. Identify the one transition that may commit before the caller learns the outcome. Make retry, deduplication or reconciliation behavior explicit there. Record the version of the contract and the configuration under which the check ran.

At integration, compare the built system with the [views](../02-design/views-and-correspondence.md). Read actual call paths, physical wiring or commissioning records. A direct reporting query into another team's write schema creates a dependency, even when the intended diagram omits it. Either remove the coupling or record its owner, implications and compatibility commitment.

## Hand off evidence

Provide implementers the accepted decision, contracts and allowed variation. Give operations the degradation states, capacity envelope and recovery authority. Give test owners the scenario, acceptance measure and an observation point independent of the component being checked. Place project records with the relevant project teams and link them back to the architecture decision. Escalate a new constraint when it changes a shared interface, the risk owner or the evidence needed for acceptance.

[Architecture field guide](../../README.md)
