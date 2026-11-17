# Bound backlog and design overload behavior

A queue turns a shortage of service into delay and storage demand. It cannot turn a sustained shortage into throughput. Define the maximum useful age of an item as well as the maximum backlog. An old warning displayed as current can be worse than an explicitly stale reading.

## Work out the bounds

For a single bottleneck with constant arrivals λ and successful drain capacity μ in the same units per second, the ideal catch-up time for backlog B is B / (μ − λ) when μ exceeds λ. If μ is equal to or below λ, select another service mode, increase capacity or reduce admitted work. Account for fan-out, retries, variable item sizes and setup work before interpreting the result as a system estimate.

| Condition | Candidate response | Architectural price |
| --- | --- | --- |
| Temporary burst with time to clear it | Buffer within an age and space bound | Durable storage, recovery logic and an owner for stale items |
| One tenant monopolizes admission | Per-tenant limits and fair scheduling | Tracking cost and a policy for unused capacity |
| Lossless work at full capacity | Backpressure or controlled stop before accepting work | Producer must understand refusal and own the item |
| Low-value telemetry tolerates loss | Sample or coalesce by an explicit rule | Report drops and preserve the semantics of aggregates |
| High-priority work competes with replay | Reserve service or schedule classes | Bound starvation and state whether live work can overtake older items |

At a proposed high-water mark calculate time to exhaustion at peak net growth. A 200 MB reserve with net growth of 2 MB/min buys 100 minutes under that load. Compare that with detection, escalation and intervention time. Allow for slower response at night. Specify behavior at hard exhaustion separately.

Exercise sustained overload through the first limiting resource, then remove the disturbance while preserving live arrivals. Measure oldest age, committed throughput, loss, duplicates, live-service latency and restoration time. Check the policy with the party whose work is shed. A device or human who sees a success response reasonably expects the design to honor its documented meaning. See [operational signals](../../../framework/concerns/operations/observable-and-operable-design.md).

[Architecture field guide](../../../framework/README.md)
