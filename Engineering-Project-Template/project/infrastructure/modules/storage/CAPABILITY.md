# Storage services and retained data

## Service goal

Provide the required block, file or object interface with measurable performance, durability, access and recovery behavior.

## Contract

Specify durability at acknowledgement, availability domain, capacity, IOPS, throughput, latency distribution, access classes, key custody, consistency and deletion semantics.

## Build and commission

1. Measure read/write ratios, request size and randomness. Size usable capacity separately from raw media, accounting for protection, snapshots, rebuild reserve and temporary restore space.
2. Map copies through controller, rack, site, account and key dependencies. Decide who can delete data and retained versions. Consider the dependency between retention locks and legitimate disposal obligations.
3. Set thresholds for growth and rebuild exposure. Include rate limits, retrieval delay and egress for archive tiers. Document expected behavior when a volume or quota fills.

## Acceptance exercise

Write known bytes, record checksums and acknowledgement order, then exercise a permitted failure. Observe foreground latency during repair. Recover an older independent version into a new target and read it with the recovery identity. Record fees, elapsed time, permissions and verified checksum.

## Revisit the design

Re-test with representative file counts and object sizes. A fast sequential benchmark can hide metadata bottlenecks on millions of small objects.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
