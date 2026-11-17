# Find capacity limits before the resource runs out

## Goal

Keep enough time and spare capacity to grow, replace a failed unit and perform maintenance. Throughput, count limits and procurement lead time can bind independently.

1. Inventory quotas at tenant, account, region, subnet, cluster, license and provider levels. Record current use, hard limit, allowed burst duration, whether an increase is guaranteed and the time to obtain it. Include small pools such as usable addresses, NAT ports, disk attachment slots and hardware spares.
2. Size concurrent events. During a rollout, old and new units may overlap while evacuated units from a failed domain start elsewhere. A design with adequate steady-state capacity can still fail at replacement because the address pool is full.
3. Estimate runway using peak-adjusted headroom divided by sustained growth. For a 20 TiB usable pool with 13 TiB occupied, a 3 TiB protected repair reserve and 0.5 TiB weekly net growth, spendable space is 4 TiB and runway is eight weeks. A six-week procurement lead time leaves two weeks of margin. Recompute with the higher growth case.
4. Instrument current use, rate of change, failed allocations and oldest queued work. Forecast multiple horizons. Include outstanding reservations and allocations awaiting eventual release.

## Exercise

In a disposable scope set a small quota, trigger a replacement while the limit is reached, and examine the consumer symptom, provider error and recovery path. Verify cleanup releases the quota and subsequent reconciliation succeeds without duplicating resources. Set an intervention threshold that allows procurement or escalation before the protected reserve is consumed.
