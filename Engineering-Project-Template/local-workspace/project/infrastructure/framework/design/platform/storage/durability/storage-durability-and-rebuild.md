# Choose storage tiers and prove recovery

Define a tier by what the consumer can measure. Record access model (block, file or object), write size, sustained bandwidth, operations per second, tail latency, acknowledgement semantics, retention, restore deadline and tolerated loss of acknowledged data. Include the software or key needed to interpret a restored object. Distinguish temporary scratch space from data that must survive loss of its writer.

## Place and size copies

1. Draw the path from write acknowledgement to durable copies. Identify caches, replication mode and hardware failure domains. Place replicas or erasure-coded fragments so that the modeled failure leaves enough usable copies. Include power, rack, controller and site dependencies in that model.
2. Reserve capacity and bandwidth for rebuilding while serving normal load. Estimate the time at risk as bytes to reconstruct divided by sustained rebuild throughput. Rebalancing, foreground contention and small random writes can lengthen the measured interval. Define when new writes should slow or stop during capacity exhaustion.
3. Keep a separately recoverable version where accidental deletion, corruption or compromised administrative access is a concern. Record restore credentials, key custody, minimum retained versions and the latest point that can be reconstructed.

## Verify the contract

Use a disposable data set with known checksums and a sequence of acknowledged writes. Exercise a permitted component loss, observe degraded throughput and verify repair completes. Restore a separate copy from the selected recovery point and compare its contents. For illustration, reading 2 TiB at a measured 200 MiB/s consumes about 2.91 hours before provisioning, replay and validation. Compare the complete elapsed restoration time with the consumer's objective.
