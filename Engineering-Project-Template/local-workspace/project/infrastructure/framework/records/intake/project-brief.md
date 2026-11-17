# Project brief and infrastructure scope

## Fill in at discovery

| Field | Project input |
| --- | --- |
| Service or capability and accountable owner | [Name the operation the consumer needs and who accepts its cost and risk.] |
| Consumers and critical period | [People, systems, sites, operating hours, monthly or seasonal deadlines.] |
| Work unit and demand | [Peak and sustained rates, payload sizes, concurrency, growth, data source and confidence.] |
| Failure consequence | [What stops, who is affected, acceptable degraded mode and deadline to recover.] |
| Information handling | [Data class, allowed locations, custody, retention, recovery copies, deletion owner.] |
| Operator and funding | [Primary and backup responder, staffed hours, recurring budget and procurement lead time.] |
| Existing estate | [Asset IDs, dependency owners, external suppliers, legacy interfaces and exit constraints.] |
| Scope and assumptions | [In-scope boundaries, excluded responsibilities with named owners, unknowns and expiry.] |
| Acceptance | [Consumer-side check, RTO/RPO where applicable, measurement interval and decision owner.] |

## Use it

Interview the consumer and an operator separately. Ask what a bad day looks like and what evidence would convince them recovery is complete. Turn discrepancies into explicit questions, such as whether retrieval by an administrator counts when the intended analyst cannot authenticate. Identify the smallest useful deployment and the recovery path for its durable state.

**Example entry.** “Daily archive for survey operations. By 07:00 an analyst can retrieve the previous export. Restore the active set within four hours after site loss. Support owns recovery, survey operations accepts the recovered manifest, and purchasing needs six weeks to add storage.”

## Exit

Owner confirms the promised operation, accepted loss, availability of the person or budget needed to operate it, and the next decision date. Carry unresolved constraints into the [architecture decision](../design/decision.md).
