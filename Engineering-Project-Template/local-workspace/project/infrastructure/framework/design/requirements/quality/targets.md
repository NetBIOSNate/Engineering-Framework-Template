# Turn constraints into testable targets

Translate words such as “fast” and “highly available” into a stimulus, operating conditions, observable response, measurement point and owner. Define the population that matters. Storage latency at an idle disk and time until a consumer can read a committed file answer different questions.

| Concern | Illustrative project target | Verification |
| --- | --- | --- |
| Latency | At 800 eligible lookups/s with a cold secondary, 99% complete within 200 ms at the client. | Replay the agreed key distribution and include timeouts. |
| Restore | Recover the latest consistent export in 2 h with at most 15 min of acknowledged data loss. | Seed timestamped records, remove primary access, restore in isolation, compare sequence and clock. |
| Isolation | A test operator cannot read production keys or route traffic into its management subnet. | Use a test identity for both denials and capture deciding audit events. |
| Operability | A second operator can bootstrap a clean worker with the primary image cache unavailable. | Time from blank host to passing a consumer probe using recovery instructions. |

Ask which failure carries the greatest consequence during the busiest operating period. Capture limits on staffing, procurement time, geographic placement, physical access and recurring spend. Assign an owner who can trade latency for consistency or cost for recovery speed when targets conflict. Label assumptions with an expiry or trigger and record who can measure them.

Attach the source of the target, baseline measurement, test interval and acceptance decision. Derive project thresholds from observed demand and the consequence of missing them.
