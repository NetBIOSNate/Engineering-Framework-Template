# Profile for analytical data and machine learning

Use this path when downstream decisions depend on a derived dataset, forecast or model. State what action depends on the output, who can contest or correct it, and whether the decision can be reproduced with the information that was actually available at the time.

## Draw the time-aware lineage

Trace source event, observation availability, transformation, feature computation, prediction or report, label arrival and downstream action. Version contracts, transformations, model or rule definitions and the input snapshot or reconstruction procedure. Record feature ownership, missingness, units and the treatment of late or corrected data. State when a backfill can republish results and which operational effects it may trigger.

A prediction is issued at 09:10. A sensor event stamped 09:00 first arrives at 09:12. A historical join on event time alone leaks future knowledge into replay of the 09:10 decision. Store a decision-time snapshot or availability history and use both event and availability rules. If replay also depends on randomness, capture the version, configuration and tolerances needed to compare outputs meaningfully.

## Promotion and recovery

Fix the evaluation cohort, baseline, thresholds, representative subgroups and uncertainty treatment with the decision owner before comparing releases. Distinguish data quality from downstream outcome quality. A shift in an input distribution can trigger investigation while delayed labels leave final outcome quality unresolved. Define what users receive when inputs are out of contract or the model is unavailable.

Add the late record to a fixture, change a schema version and replay the fixed cohort. Check which observations were eligible, compare output within agreed tolerance and ensure a shadow run cannot issue an operational action. Revoke or roll back a release and identify which prior decisions need notice or remediation. Retain evidence of provenance and permissions for the lifetime required by the project. Use [information lifecycle](../../../data-flows/information/lifecycle-and-ownership.md), [rollout](../../concerns/change/rollout-and-rollback.md) and [privacy](../../../trust-boundaries/protection/assurance/threats-and-privacy.md).

[Architecture field guide](../../README.md)
