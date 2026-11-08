# Model workload and allocate capacity

Start with useful output, its unit, the demand window and the service objective. “Requests per second” can hide large variation in record size, expensive operations, connection setup and unsuccessful work. Define separate workload classes when mixing them changes the bottleneck.

## Build a capacity budget

| Input | Questions and units |
| --- | --- |
| Demand | Peak and sustained arrivals per second, burst duration, concurrent sources, item-size distribution |
| Resource demand per unit | CPU-seconds, bytes stored, network bytes, joules, machine-minutes or operator-minutes |
| Available service | Successful units per second at the required latency and error envelope |
| Reserve | Capacity unavailable during maintenance, failure, throttling, seasonal variation or wear |
| Limit and observation | First saturated resource, queue age, missed outcome and how overload is signaled |

Compute the demand on each constrained resource. A unit requiring 0.020 CPU-seconds at 100 units/s needs two CPU-seconds of work per elapsed second before overhead. Check serial stages, skew and coordination before assuming that two cores suffice. At stable average flow, Little's law relates average units in the system to throughput times average time in the system. Keep the same population and boundaries on both sides. Tail latency requires its own evidence.

## Fleet model

For 1,200 devices producing one observation per minute, normal arrivals average 20/s. A simultaneous six-hour outage creates 432,000 observations. At 2 KiB per observation the payload per device is 720 KiB. Add indexes, allocation overhead and reserve based on the candidate medium. A reconnect storm may exhaust authentication or network capacity before ingestion saturates.

At 60 successful observations/s sustained during recovery and 20/s ongoing arrivals, drain time is 432,000 / (60 − 20) = 10,800 seconds, or three hours. Finishing in at most four hours requires at least 50/s total under these ideal assumptions. Provide margin for restart and variability. A shared daily average cannot establish a recovery guarantee.

Review the model against a ranked demand trace or calibrated measurements at the intended service target. Vary one influential assumption at a time, then test combinations that arise together in the field. Carry the result to [backpressure and overload](saturation/backlog-and-load-shedding.md).

[Architecture field guide](../../framework/README.md)
