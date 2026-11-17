# Field glossary

Use these meanings when reading the worksheets. On a live project, add the domain terms that cause disagreement between people, such as “received,” “available,” “safe” or “customer.” Put a concrete counterexample beside any term whose meaning changes across a boundary.

| Term | Working meaning | Example or question |
| --- | --- | --- |
| Capability | An outcome the organization or system can deliver | Can a field team retain observations through loss of a link? |
| Constraint | A limit an option must respect | A replacement part must fit an existing enclosure |
| Driver | A concern that changes the design choice | Local capture during a partition rules out remote-only persistence |
| Assumption | A premise used before it is established | The installed medium can tolerate a certain write pattern |
| Invariant | A rule that must hold within a declared scope | One accepted reservation consumes exactly one available unit |
| Viewpoint | Conventions for answering a class of architectural questions | What fails together, how to draw it and what to check |
| View | A representation of a particular architecture using such conventions | A placement map of a specific site and shared power supply |
| Contract | Agreed observable behavior at a boundary | Meaning of acknowledgment, units, timing, failure and owner |
| Sensitivity point | Parameter whose variation materially affects a quality response | Arrival rate changes backlog drain time nonlinearly near saturation |
| Tradeoff point | Choice or parameter affecting multiple qualities differently | Longer replay history aids repair while increasing storage and exposure |
| Failure domain | Elements vulnerable to a particular shared failure | Two independent hosts on one power feed |
| Backpressure | A signal or mechanism that limits upstream admission | A full receiver refuses work before accepting custody |
| Idempotency | A repeated logical operation has the specified single effect | Repeating a reservation key returns the original result |
| Watermark | A named position through which processing or copying is known complete | A snapshot includes all committed changes through revision 42 |
| SLO | Service level objective with a defined population and window | Fraction of valid uploads durably acknowledged in time |
| RTO and RPO | Target time to recover and maximum tolerated data loss measured in time | Define which function has recovered and which writes may be missing |
| Verification | Evidence that specified requirements were met | A measured actuator response meets an allocated timing limit |
| Validation | Evidence the system serves its intended use in context | An operator can recognize stale state and make the intended decision |
| Residual risk | Exposure remaining after the chosen treatment | Loss of an unuploaded record if the whole device is physically destroyed |
| Superseded | A past decision has a named successor | Earlier reasoning remains available for interpreting older installations |

If two owners use one term differently, record both definitions and the conversion or ownership rule at their interface. Follow a term into the [worked contracts](../examples/field-observations/02-design/views-and-contracts.md) or use it when defining a [quality scenario](../method/01-frame/quality-attribute-scenarios.md).

[Architecture field guide](../README.md)
