# Cache correctness, refill and failure amplification

## Choose a contract

State the authoritative data source, maximum tolerable staleness, cache key, invalidation owner and response when authority is unreachable. Cache usefulness depends on the correctness of a hit and the cost of a miss. Include the tenant, version and authorization scope in key design when values differ across those boundaries.

1. Observe hit ratio and latency by key class. A high aggregate hit rate can hide one hot key or an origin dependency that fails only on cold start. Record enough cardinality to diagnose skew while protecting sensitive identifiers.
2. Define time to live, invalidation and any bounded stale-serving behavior. Distinguish successful lookups from negative results. Revoked authorization or deleted sensitive data may need a tighter bound than ordinary content. Test bypass paths and independent invalidation.
3. Size the origin for a realistic miss burst after cache loss. Limit concurrent refills and coalesce work for identical keys where supported. Stagger expirations where compatible with freshness. Bound wait time and decide which callers can accept a degraded response.
4. During rollout, support compatible keys and value formats or isolate versions. Document how operator purges are scoped and who can cause a full cold start.

## Acceptance

Prime two tenant fixtures with distinct values for the same logical name. Verify separation, change the authoritative value and measure time to correct reads on independent clients. Evict a test partition under load and track origin QPS, waiting requests, consumer errors and recovery time. Verify a cache outage cannot silently change the durability of acknowledged writes.
