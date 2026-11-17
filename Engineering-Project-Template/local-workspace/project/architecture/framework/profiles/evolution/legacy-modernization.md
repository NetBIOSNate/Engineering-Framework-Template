# Profile for modernization and replacement

Use this path when replacing an existing capability while users and downstream systems still depend on it. Inventory manual, real-time, batch, support, backup and periodic consumers. Name the authoritative source and the exact meaning of a successful update at each migration stage.

## Example of a staged ownership transfer

| Stage | Write authority | Read and recovery behavior |
| --- | --- | --- |
| Baseline | Legacy system | Capture a consistent snapshot and the change watermark associated with it |
| Catch-up | Legacy system | Apply versioned later changes to the new store and reconcile normalized records |
| Shadow | Legacy system | Compare reads without triggering communications, charging or other real effects |
| Canary cohort | One authority per entity, selected by a stable key | Route requests consistently and verify expected state and rollback feasibility |
| Transfer and retirement | New system | Fence legacy writes, reconcile accepted changes and retain required archive readers |

A preferences store is moving to a new representation. An update arriving during the initial copy can be lost if snapshot and change capture do not share a consistent boundary. Apply monotonic revisions per entity or a verified equivalent. Define legitimate transformations such as normalized spelling before comparing outputs. Include deletes, duplicate changes and late arrivals.

After writes move, routing reads back to the old store is safe only once all accepted new writes are present and representable there. A new field with no old equivalent can change the available recovery route. Pause admission, reconcile, retain a compatible reader or roll forward according to a decision made before cutover.

Test an update during the copy, a reordered change, a schema rename and emergency recovery after a committed write. Expect the latest acknowledged revision to survive, mismatches to have an owner and only the designated writer to act. Obtain retirement evidence from consumer owners across a representative operating cycle. Use [change and retirement](../../method/05-evolve/change-and-retirement.md) and [the rollout guide](../../concerns/change/rollout-and-rollback.md).

[Architecture field guide](../../README.md)
