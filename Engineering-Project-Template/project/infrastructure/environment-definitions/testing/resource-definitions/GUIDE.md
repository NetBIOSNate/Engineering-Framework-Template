# Repeatable failure and load fixtures

## Intended outcome

Test resources reproduce a named risk at a known scale, and concurrent test runs cannot alter each other's state.

## Policy inputs

Record fixture version, resource shape, dataset seed, permitted destructive actions, run ID, concurrency, measurement window and teardown owner.

## Implementation sequence

1. Choose the minimum shape that preserves the behavior being measured. Quorum and placement tests need the actual number of independent voting domains relevant to the claim.
2. Namespace resources, data, queues and telemetry by run. Control caches and background jobs and capture starting occupancy before a performance test.
3. Provision and tear down from a clean identity. Interrupt one run mid-create and reconcile live objects against recorded IDs before retrying.

## Evidence and handoff

Run two fixtures concurrently and prove that fault insertion and cleanup in one leave the other's probe and data intact. Record variance across repeated runs. Flag scale assumptions that still need a staging exercise.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
