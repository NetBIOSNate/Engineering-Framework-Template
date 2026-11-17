# Disposable development capacity

## Intended outcome

Make ordinary experiments inexpensive to create, repeat and clean up while preserving data explicitly marked for retention.

## Policy inputs

Supply owner, purpose, resource class, lifetime, cost allocation, quota and data disposition at creation. Keep persistent shared fixtures in a separate ownership boundary.

## Implementation sequence

1. Choose small defaults with a documented override for jobs that reproduce production limits. Apply limits to both resource count and expensive classes.
2. Generate fixtures from a versioned definition with sample data. Test repeated creation and cleanup after a partially successful build.
3. Mark expiration on ephemeral compute, disks, addresses and snapshots. Identify orphaned dependants before reclaiming a sandbox with retained results.

## Evidence and handoff

Run a full create-use-expire cycle on a fixture. Verify its DNS entry, unattached volume and allocated address are released and prove an explicitly retained sample can be recovered. Publish typical startup time and observed cost per active day.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
