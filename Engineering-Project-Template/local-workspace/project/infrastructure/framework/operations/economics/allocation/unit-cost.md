# Allocate cost and decide when to change capacity

## Goal

Connect a recurring infrastructure cost to useful work while preserving service and recovery objectives. Pick a unit that someone actually values, such as a completed batch, a verified restore or a tenant-month within its service objective.

1. Define the accounting boundary and period. Include directly billed compute and storage, network transfer, software, support, amortized equipment, facilities and shared operations where applicable. Keep currency, discounts and tax treatment consistent with the finance owner's ledger.
2. Assign direct costs first. Split shared costs with an agreed driver such as reserved capacity, metered bytes or peak contribution. Keep unallocated cost visible. A reconciliation passes when direct, shared and unallocated amounts sum to the original total within the documented rounding tolerance.
3. Compare units delivered over the same interval. An illustrative $12,000 monthly cost for 4,000 verified restores yields $3 per restore. Track failed attempts separately. A declining unit cost can coincide with rising total spend if demand grows.
4. Decompose a budget variance into rate, volume and mix. Check whether a cheaper tier changes egress, restore delay, minimum retention or operator workload. Evaluate commitments under low, base and high demand with exit costs and expiry dates.

## Review decision

Record current and proposed unit cost, quality targets, capacity after the modeled failure and one measurable change. Assign an owner and repeat the calculation after a full billing cycle. For on-premises growth, compare procurement lead time with remaining runway, including equipment space, power and maintenance capacity. [FinOps Foundation Framework](https://www.finops.org/framework/)
