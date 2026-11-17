# Design for failure, recovery and integrity

Choose an outcome the system must preserve under a credible disturbance. Start from the operator's or customer's point of view. A server returning to health says little about whether accepted work is present, records agree or a suspended physical process can safely resume.

## Analyze one failure path

| Stage | Design question |
| --- | --- |
| Failure | What stops, slows, gives a wrong answer or accepts work without completing it? |
| Containment | Which other functions share power, credentials, a clock, an operator, storage or a supplier? |
| Degradation | What useful outcome survives, who is told and what action becomes unavailable? |
| Recovery | Who can restore the system, from which trusted state and in what dependency order? |
| Reconciliation | How are accepted work, external effects and conflicting copies accounted for? |

Write two objectives with the service owner. The recovery time objective (RTO) sets the targeted restoration interval and the recovery point objective (RPO) sets the tolerated data loss expressed in time. Specify the start, end and scope of each. An RTO for restoring reads can differ from an RTO for resuming new writes or reconciling prior ones.

## Check the arithmetic and the common causes

A twelve-minute detection delay, eight-minute decision, eighteen-minute restore and seven-minute validation require 45 minutes if serial. A 30-minute RTO needs a different dependency order, automation or faster steps. Establish which steps may overlap and what evidence prevents premature reopening. Two replicas can share one administrative credential and corruption path. A backup in the same control domain may also share the failure.

Exercise a restore using the documented identity, retained keys, schema reader and ordinary staffing. Freeze or fence competing writers during transfer. Compare restored state with an independent receipt or ledger and identify effects that need reconciliation. Record data age, unavailable functions, elapsed time and residual uncertainty. Rerun the scenario when recovery dependencies, staffing or data volume materially change. See [retirement](../../method/05-evolve/change-and-retirement.md) and [operational signals](../operations/observable-and-operable-design.md).

[Architecture field guide](../../README.md)
