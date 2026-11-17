# Backup chains and restored integrity

**Goal.** Demonstrate that a recoverable copy includes the data, metadata and keys required to reconstitute a usable system. Define owners, consistency boundaries, retention periods and the expected time to retrieve archived copies.

1. Catalog persistent volumes, database state, configuration, object versions, permissions and dependencies on key versions. For each dataset, document whether the backup is crash-consistent or application-consistent and how to obtain an internally consistent recovery point across stores. Map the complete chain from baseline to increments or transaction logs.
2. Protect at least one recovery copy against the failure being designed for. A separate storage account that shares destructive administrator credentials can fail with the original. Scope deletion authority, record recovery access and rehearse retrieval of historical keys under the chosen policy.
3. Select an older recovery point and restore it in an isolated namespace using the recovery identity. Validate checksums, object counts, permissions and referential or sequence invariants. Read through the consumption interface and reconcile a known transaction marker. Measure retrieval, transfer and replay time separately.

**Worked test.** Delete a synthetic parent row in a lab and let replication propagate the deletion. Recover to the point immediately preceding the deletion and confirm the parent, child relationships and expected totals. Record the restored timestamp, evidence of a clean read and any missing interval.

**Exit evidence.** Keep a restore transcript, coverage gaps, owner and next exercise. Test expiry on a designated fixture under its approved retention policy.
