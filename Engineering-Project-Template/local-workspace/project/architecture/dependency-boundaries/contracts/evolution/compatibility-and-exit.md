# Design interface evolution and supplier exit

Write a compatibility promise in terms of supported producers and consumers, the duration of coexistence and the behaviors that must survive. A field added to a message can still break a consumer with strict parsing. Keeping the schema readable can still break a user if the meaning of a unit or success response changes.

| Producer | Consumer | Example question |
| --- | --- | --- |
| Old | Old | Is the baseline reproducible with representative records? |
| Old | New | Does a missing field have the same meaning as the previous release? |
| New | Old | Can an old reader interpret unknown values without silent corruption? |
| New | New | Can the target support the new behavior and the promised recovery route? |

## Plan a change

Start with examples contributed by actual consumers, including offline readers and older field equipment. Separate syntax, semantics, timing, ordering, error meaning and performance commitments. Add or negotiate capability with an observable fallback. During transition, keep write ownership explicit. Instrument usage by version, then set removal conditions with the owner of the slowest legitimate consumer.

A producer migrating temperature from whole degrees Celsius to millidegrees must identify the unit and precision explicitly. Reusing the same unqualified integer field can produce a plausible but incorrect observation. Preserve old meaning through a versioned representation, range checks and fixtures at boundary values. Include negative values and unknown readings.

## Exit rehearsal

List everything needed to leave a supplier, including canonical identifiers, complete history, attachment export, key access, audit trail, calibration records and support for interpreting old versions. Rehearse with a sample containing rare states. Have an independent consumer reconstruct the original meaning. Estimate time and staff to transfer the full estate, then compare against contract notice and spare-part lead time.

Finish when both endpoint owners accept the coexistence window and a genuine old consumer has exercised the proposed contract. See [sourcing and exit economics](../../../framework/concerns/sourcing/make-buy-and-exit.md) and [phased rollout](../../../framework/concerns/change/rollout-and-rollback.md).

[Architecture field guide](../../../framework/README.md)
