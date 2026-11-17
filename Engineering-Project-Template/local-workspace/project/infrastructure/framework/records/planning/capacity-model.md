# Capacity and degraded-state worksheet

## Establish the unit

Consumer operation [ ], demand source and interval [ ], peak sustained rate [ ], burst shape [ ], target latency or deadline [ ], observation date [ ], confidence [ ].

| Input | Measurement and units |
| --- | --- |
| Safe capacity per unit at target | [Benchmark, workload mix, cache state, duration and error rate.] |
| Placement and failure | [Units per domain, largest simultaneous loss, shared bottlenecks.] |
| Working reserve | [Maintenance, surge, growth, rebuild and downstream quotas.] |
| Procurement | [Order or quota-increase lead time, cold start, time to rebalance.] |
| Output | [Surviving usable rate, margin above forecast, limiting resource and next threshold.] |

Compute surviving capacity from a placement map. Subtract unavailable units, apply any documented operating ceiling exactly once and cap the result at the lowest shared dependency capacity. For a queue, drain time equals backlog divided by the positive difference between sustained service rate and continuing arrival rate. When the difference is zero or negative, backlog cannot clear at those rates.

**Worked example.** Three domains tested at 600 requests/s each leave 1,200 requests/s after one loss. A project-selected 80% ceiling gives 960 requests/s. At a 900 requests/s forecast the margin is 60 requests/s, subject to sufficient shared database, network and quota capacity. If the database can handle only 850 requests/s, its capacity limits the whole service and the design misses the forecast.

Assign an owner and test date to the least certain input. Recalculate after a new workload mix, topology, large tenant or procurement delay.
