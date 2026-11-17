# Disaster recovery and failback

**Goal.** Restore a named infrastructure service within its recovery time objective (RTO) and recovery point objective (RPO). Agree with consumers on the minimum usable service, acceptable data loss and clock start and stop events.

1. Draw restoration dependencies for emergency identity, DNS, time, network, keys, backup catalog, data and consumer routing. Keep instructions and recovery access available outside the failed domain. Choose restore, standby or active replication according to the interruption the service can tolerate.
2. Rehearse loss of the primary in an isolated environment. Fence the old writer before allowing the secondary to accept writes. Verify identity and key access, restore a consistent recovery point, run integrity checks and route a test consumer. If fencing is uncertain, pause promotion of a single-writer service until exclusivity is established.
3. Use a timestamped canary. With impact beginning at 13:00, a last consistent canary at 12:52 and successful validation at 13:42, observed outage is 42 minutes and the canary indicates an eight-minute recovery-point gap. Record canary spacing and cross-store consistency. Compare measurements with both objectives.
4. For failback, reseed the former primary, measure catch-up, define the final write fence and route transition, then reconcile writes and repeat probes. Reopen normal operations after standby coverage has been re-established.

**Review evidence.** Preserve the timeline, promotion authority, integrity results and residual recovery gaps. [NIST SP 800-34 Rev. 1](https://csrc.nist.gov/pubs/sp/800/34/r1/upd1/final)
