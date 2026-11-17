# Choose acknowledgement and fencing under a partition

## Set the contract

Specify what a consumer may infer after a successful write, a timeout and a read from a replica. If the primary receives a write and its acknowledgement is lost, a client cannot infer that the write failed. Use an operation identifier or a reconciliation path whenever a repeated write could cause a second effect.

1. Draw the path from request to durable media and acknowledgement. Identify synchronous and asynchronous boundaries, write caches, quorum rules and lag visibility. Count durable data copies independently from voting members. Confirm behavior from the chosen product's actual configuration.
2. Decide whether a minority partition may accept writes. For a single-writer service, establish an enforceable fence using the platform's supported mechanism. DNS movement and loss of heartbeat alone cannot prove the old writer stopped accepting work. If exclusivity cannot be established, decide who can pause writes.
3. For an intentionally multi-writer service, specify which operations commute, how conflicting updates are ordered or surfaced and who resolves irreconcilable records. State the effect of clock skew or two sites editing the same logical object. Name the application interface owner who accepts those semantics.
4. Specify a recovery point for a group of dependent stores. Restoring a database and an object index to individually valid but different points can create dangling references. Publish a manifest, checkpoint or reconciliation procedure that verifies a usable grouped state.

## Drill

Write numbered records from both sides of a partition in a disposable environment within the promised access rules. Preserve responses as seen by clients, restore connectivity, and compare acknowledged operations with durable final state. Check old-writer rejection, duplicate handling, read freshness and time to restore redundancy. Retain observed loss or conflicts and the release version tested.
