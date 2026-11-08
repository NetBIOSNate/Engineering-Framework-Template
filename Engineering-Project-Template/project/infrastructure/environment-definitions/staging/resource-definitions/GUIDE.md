# Qualify resource definitions for promotion

## Intended outcome

A release candidate can be promoted with known capacity, replacement and recovery behavior.

## Policy inputs

Record immutable candidate digest, resource class, scaled dimensions, realistic data shape, available quotas and the exact change under review.

## Implementation sequence

1. Deploy the same approved definition intended for production with parameterized environment bindings. Inspect the plan for destructive replacement, new privileges and changed durable formats.
2. Test loss of one unit and replacement during representative traffic. Account for cold caches and deployment surge as well as steady operation.
3. Rehearse reversal or forward repair at the last safe point. For durable changes, include restoration of an older version and compatibility of readers.

## Evidence and handoff

Record old/new cohort health, observed provisioning time, consumed spare capacity and recovery result. Spell out any untested dimension such as full production data volume. Route remaining uncertainty to a named owner and production canary.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
