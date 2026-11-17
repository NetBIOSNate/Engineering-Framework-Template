# Map information from capture to retirement

Select a real unit of information and trace its identity across capture, validation, transformation, publication, correction and disposal. Give each representation a purpose and a custodian. A diagram of the normal route often misses the copies that matter most during audit, restore or correction.

## Record each hop

| Field | Design question |
| --- | --- |
| Source and owner | Which observation is authoritative? Who may correct it and who owns derived results? |
| Meaning | What are the units, reference frame, precision, allowed values and unknown-value semantics? |
| Time | Which clocks report event time, arrival time and commit time? What uncertainty or reset can occur? |
| Lifecycle | What purpose, access, retention, archival and disposal rules apply to this copy? |
| Movement | How are identity, ordering and integrity preserved through retries, exports and manual edits? |
| Repair | How is a late item, correction or deletion carried to derivatives, caches and restore procedures? |

Trace a correction from its original ID to one report, one export and one restored backup. Describe how corrections propagate, whether an already-issued report is restated, who is told and how superseded values can be explained. Agree with the information owner how long retained backups remain accessible and how deletion or restriction is reapplied upon restore.

## Example of clock ambiguity

A disconnected device captures at its local 09:00 and uploads at service time 15:00. Record both clocks, device boot epoch and confidence in local time. An operator seeing an urgent value needs its age and uncertainty. A billing or training dataset may need the time at which the value became available to a decision maker. Never silently reinterpret missing time or units as a valid reading.

Review a synthetic record whose producer restarts, changes units and later corrects a value. Follow how the consumer learns the correction and how a reviewer identifies all affected results. A data steward should be able to explain ownership and disposal at every persistent copy. Use [reconciliation](exchange/replay-and-reconciliation.md) for delivery accounting and [analytical lineage](../../framework/profiles/data-products/analytics-and-ml.md) for decision-time reconstruction.

[Architecture field guide](../../framework/README.md)
