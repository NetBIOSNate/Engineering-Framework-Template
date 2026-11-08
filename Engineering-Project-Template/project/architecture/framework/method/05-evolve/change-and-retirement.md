# Evolve and retire an architecture

A working system accumulates consumers whose dependency is often invisible in the original design. Start an evolution decision by naming the promise to preserve and the observation that suggests the present architecture has reached a limit. Record the baseline with a date and a way to detect stale evidence.

## Plan the intermediate states

| State | Questions for the design owner |
| --- | --- |
| Baseline | Who can write today? Which batch, support, manual, offline and recovery paths read that state? |
| Coexistence | Can old and new versions decode and authorize one another's work? Who owns reconciliation and its deadline? |
| Transfer | What watermark proves the new owner is current? How are late writes fenced off or handed over? |
| Recovery | Can all newly acknowledged work be represented in the former system? If not, define a forward repair |
| Retirement | Which readers, credentials, backup restore paths, physical spares and contractual duties survive shutdown? |

Use evidence from consumer inventories, access logs over a representative cycle, field inspections and owner confirmation. Silence during a short observation period gives little information about a quarterly reconciliation job. Keep one authoritative writer per fact or document the conflict-resolution protocol and compensation that permit concurrent ownership.

## Decide when to reopen

Reopen a choice when an input crosses the range for which the option was justified. Examples include a new type of sensitive data, a supplier end-of-life notice, a growing queue despite steady demand, or a requirement to operate without a central identity service. Revisit the affected scenario, links and owners. Preserve the earlier decision as history and record the successor.

At retirement, recover a representative archive with its retained reader and keys. Account for outstanding work, release maintenance authority and record where obligations pass to the successor. For physical products, address field stock, decommissioning constraints and remaining support arrangements. A completed move has a named owner for each surviving obligation and an observation demonstrating the obsolete path can be withdrawn. See the [modernization profile](../../profiles/evolution/legacy-modernization.md) and [cutover guide](../../concerns/change/rollout-and-rollback.md).

[Architecture field guide](../../README.md)
