# Assign responsibilities and authoritative state

Begin with one rule that must remain true after a crash, interruption or shift change. Allocate that rule to a component or accountable role that can decide and observe the result. A component is a unit of responsibility. Its placement in a process, device or organization is a separate design decision.

## Design a boundary

| Element | What to write |
| --- | --- |
| Purpose | A verb and object the component owns, such as “accept observations” |
| Authority | Facts it may change, rules it must enforce and dependencies it reads |
| Public promise | Input, response, meaning of success and behavior when the caller sees a timeout |
| Failure and repair | Persistent state after interruption, recovery owner and visible diagnostic state |
| Change pressure | The change likely to affect it and who must coordinate that change |

Trace one change through two possible decompositions. A parser for vendor measurements could sit inside intake or behind a versioned adapter. Test which choice keeps a units change from forcing the operator display or persistence format to change. Choose a separate deployment only when consequences such as independent scaling, fault containment or independent release justify operating another boundary.

## Durable intake example

Intake owns the canonical observation. It records the observation and its pending publication together before issuing a receipt. A publisher may crash after sending and before marking the publication complete. The downstream consumer atomically records the observation identity and corresponding business effect. A reused identity with a different payload enters conflict handling. Stable producer identities and a defined deduplication horizon are prerequisites.

Ask the maintainer what survives if power disappears before commit, after commit but before receipt, or after publication but before marking completion. Recover and repeat the operation from each point. The caller should be able to discover the result. Each accepted observation should converge to the promised effect with conflicts visible. For a physical component, substitute sensing, command and observed actuation for the persistence steps. See [concurrency and invariants](runtime/concurrency-and-invariants.md).

[Architecture field guide](../../framework/README.md)
