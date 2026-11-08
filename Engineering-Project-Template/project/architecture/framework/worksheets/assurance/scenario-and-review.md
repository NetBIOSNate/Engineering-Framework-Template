# Worksheet for scenario evidence and risk disposition

Use a row for each claim that matters to a decision. Record planned evidence separately from an actual observation. Verification compares the system with a specified requirement. Validation checks whether the outcome serves the intended user in their operating conditions.

## Scenario and observation

| Field | Project entry |
| --- | --- |
| Scenario ID, driver and owner | [Traceable identity, affected beneficiary, accountable person] |
| Source, stimulus and affected element | [Who or what acts, event and target] |
| Environment and expected response | [Mode, configuration, workload, disturbance, response] |
| Threshold and population | [Units, start/end boundaries, time window and allowable errors] |
| Evidence method | [Analysis, inspection, demonstration, test or intended-use observation] |
| Measurement and limits | [Instrument, data source, uncertainty and conditions excluded] |
| Evidence state | [Proposed, calculated or observed, with date and evidence location] |
| Result and disposition | [Observed value if available, pass/fail/inconclusive, next decision and owner] |

## Risks and evidence actions

| Risk ID and exposure | Current treatment | Residual risk and authority | Next action and trigger |
| --- | --- | --- | --- |
| [RSK-… and consequence] | [Mitigation, transfer, avoidance or acceptance with rationale] | [What remains, who can accept it, approval status] | [Owner, due event and reopen condition] |

## Review handoff

Record the accepted design scope, any exception expiry, which records must change and who receives the outcome. If the result fails, identify which requirement, design assumption or allocation needs a new decision. A team may discover that the user outcome was mis-specified even when a component passes its own test.

Ask an independent reader to find the evidence for the claim and distinguish it from the predicted result. If a measure is a percentile, include sample population, count, observation window and treatment of failures. If a claim concerns physical state, specify how that state was independently observed. See [review facilitation](../../method/03-evaluate/tradeoff-review.md) and [a populated evidence table](../../examples/field-observations/03-evaluate/evidence-and-disposition.md).

[Architecture field guide](../../README.md)
