# Accelerator clusters and tightly coupled batch work

## Goal

Deliver completed jobs per allocation with a predictable restart path after node loss. Capture model or solver memory, number and type of devices, placement constraints, dataset size, checkpoint interval, acceptable queue time and billed or metered energy per completed job.

1. Start with one representative job. Compare device utilization with host-to-device bandwidth, host memory, NUMA placement, local scratch and shared storage throughput. A starved accelerator can have a high acquisition cost and a low useful-work rate.
2. For multi-node jobs, benchmark collectives across the exact network and node geometry requested. Record topology, oversubscription, link error counters, driver/runtime combination and job placement. Specify whether the scheduler must allocate the entire group together.
3. Reserve temporary space and aggregate write throughput for simultaneous checkpoints. Use a completion marker and integrity check so a resumed job can reject a partial checkpoint. Budget retention for at least the versions needed during a failed write or incompatible driver rollout.
4. Model downtime due to maintenance and unavailable devices. A full chassis may wait idle for a single matching replacement. Evaluate smaller job sizes, supported spare models or checkpoint portability against the project's completion deadline.

## Prove the contract

Run a representative multi-node job and interrupt a worker during a checkpoint in a test allocation. Restore the last complete checkpoint on supported replacement hardware. Record lost compute time, queue wait, data reload, collective throughput and final result tolerance. Compare total cost per successful job across the candidate placements. Report benchmark conditions along with all rates.
