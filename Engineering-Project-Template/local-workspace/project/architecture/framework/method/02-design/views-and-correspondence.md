# Select views and check their agreement

A viewpoint describes how to answer a kind of question. A view applies those conventions to a particular design. Begin with the reader's question, choose a representation and explain its vocabulary. A table can answer ownership or timing questions more precisely than a diagram.

| Question | View to construct | Consistency check |
| --- | --- | --- |
| Who relies on the outcome? | Context and external interfaces | Every crossing has a direction, purpose and accountable party |
| Who may change state? | Logical responsibilities and information ownership | Each mutable fact has a writer or an explicit coordination rule |
| What happens during interruption? | Runtime sequence, including timeout and repair | The step that acknowledges work agrees with the durable-state view |
| What can fail together? | Deployment, physical allocation and shared resources | Redundant roles are mapped to actual power, identity, network and operator dependencies |
| Who can authorize a change? | Trust zones and authority transitions | Maintenance routes appear in both trust and runtime views |
| What holds during transition? | Current, intermediate and target configurations | Every supported mixed state can read and recover its own records |

## Construct and review a view

Pick a scenario and the decision it informs. Use stable names for elements, label arrows with a verb and specify units or payload where ambiguity matters. State the scope, abstraction level, assumptions, version and date. If one box expands into several parts in a lower-level view, identify its parent and preserve its external promises. Distinguish a process boundary, a team boundary and a physical barrier using a short legend.

Review with someone from the other side of an interface. Ask them to walk a request and a failure with a finger. If a line can mean either “reads a copy” or “may write the source,” redraw it or add a contract. When views disagree, identify the decision whose outcome changes and assign an owner. A network link labeled optional on a placement view cannot be required by the only startup sequence.

Use the [view and interface worksheet](../../worksheets/design/view-and-interface.md) for small systems. A larger software system may use C4 levels for structure and a sequence for time. Use a mode table or physical interface drawing for equipment where that better explains the concern. See the [reference crosswalk](../../reference/framework-crosswalk.md).

[Architecture field guide](../../README.md)
