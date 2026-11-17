# Set decision rights and handle exceptions

Reserve architecture review for decisions that change shared promises, allocation of risk, system boundaries or costly commitments. Delegate local implementation choices to the people who can reverse them. Write down who decides, who must be consulted and whose authority covers any remaining exposure.

## Pick the decision level

| Scope of consequence | Suitable owner | Example |
| --- | --- | --- |
| Local and reversible within one component | Component owner | Internal representation that preserves its public contract |
| Crosses an interface or changes a recovery promise | System design owner with both endpoint owners | Change in acknowledgment meaning or replacement tolerance |
| Transfers costs or risk across products | Portfolio or capability owner with affected operators | Shared identity dependency or retirement of a common service |
| Changes a protection claim or operating envelope | Accountable domain authority | Wider temperature range or different authority to override a stop |

## Resolve disagreements

Write the disagreement as a prediction. “The gateway approach cannot preserve readings across loss of the local radio hop” can be exercised. “The gateway is simpler” needs a unit, such as deployable count, field support hours or power consumption. Let the owners choose an experiment or a decision date. Preserve a minority view when it identifies a consequence worth watching.

## Time-bound exceptions

An exception record names the rule or promise at issue, affected scope, reason, temporary behavior, owner, exposure, mitigation, expiry or trigger, and what happens at expiry. Example: a legacy reader may consume one old schema during the first migration cohort. Its owner observes usage and reports remaining installations. Removing the reader's access follows confirmation of migration or a documented service decision.

At review, sample a real boundary, a recent change and an outstanding exception. Trace each to a current owner and evidence. Track decisions waiting for evidence, the age of unresolved exceptions and repeat failures caused by the same assumption. Use the findings to change the method or retire a rule that no longer earns its coordination cost. See [experiments](../../../decisions/records/evidence/experiments-and-reversibility.md) and [change triggers](change-and-retirement.md).

[Architecture field guide](../../README.md)
