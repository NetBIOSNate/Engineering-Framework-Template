# Specify a reusable infrastructure module

## Design an interface someone else can own

Keep resource lifecycle, authority and failure behavior together. A storage module can own a bucket, its access boundary and its lifecycle policy. An environment selects the region, tenant, retention class and recovery objective. A central identity module can supply a principal reference without granting the storage module authority to reset that principal.

| Contract element | Example for an archive store |
| --- | --- |
| Required inputs | Scope ID, environment, data class, owner, allowed location, writer and reader references. |
| Validated options | Retention class, protection against accidental deletion, size estimate, recovery copy placement. |
| Outputs | Stable store reference, endpoint, access policy reference, recovery catalog identifier. |
| Invariants | An acknowledged upload has an immutable version ID. A reader cannot delete retained versions. |
| Replacement semantics | Changing the physical location requires a migrated target and a cutover. |
| Ownership | Storage owns the store and its access policy. Identity owns principal lifecycle. |
| External assumptions | Working DNS, identity issuance, recovery keys and funded copy capacity. |

## Implement a version

Validate required inputs, permitted combinations, globally unique names and tenant scope before allocation. Build using stable resource keys. Expose only outputs consumers need. A change to an internal naming rule becomes a breaking change when it changes a live identity that consumers depend on.

Document compatibility by behavior. An added optional setting can still change existing deployments if its default changes the acknowledgement, routing or retention contract. Provide an upgrade path with handling for older state and external consumers.

## Qualification matrix

Build a fresh fixture, adopt a pre-existing fixture with an unchanged ID, repeat the plan, interrupt after creation and upgrade from the last supported version. Verify desired outputs, denial of an unauthorized action and recovery after a failed change. During teardown, account separately for shared dependencies and retained data. Use the [state guide](../../../controls/delivery/state/module-state-and-drift.txt) to settle ownership and concurrency.
