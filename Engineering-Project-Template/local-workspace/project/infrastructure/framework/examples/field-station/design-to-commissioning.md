# Worked commissioning review for a field station

## Operating assumption

A field station captures 150 KiB/s of sensor records. The WAN may be unavailable for 12 hours. Locally acknowledged records must survive an ordinary restart and be delivered once to the central record of observations after the link returns. A site technician is available during working hours. This example uses a bench fixture and illustrative rates.

## Select the minimum architecture

Assign an event ID at capture and acknowledge only after durable local append. Store a source sequence and checksum. The central consumer records each processed event identity atomically with the durable result or uses an equivalent idempotent write. Keep the local item until central durable acknowledgement. Duplicate delivery is expected after loss of an acknowledgement. Define how a replaced station retains or changes source identity to avoid colliding with old sequence numbers.

A 12-hour outage produces about 6.18 GiB of raw records. At 25% measured encoding overhead, that becomes about 7.73 GiB. Reserve additional capacity for filesystem operation, alarms, growth and an interrupted compaction. Document behavior when capacity is exhausted. Finite storage cannot promise unbounded retention during an indefinite outage.

## Reconnect and drain

If central delivery can sustain 450 KiB/s of raw payload equivalent while new records continue at 150 KiB/s, a 12-hour raw backlog drains in six hours. Observe actual acknowledgements over the intended link. Include retransmission, payload expansion, rate limits and contention with other sites when measuring usable throughput. Limit concurrent site replay to protect the shared ingest service.

## Bench sequence and acceptance

1. Run a known sequence, disconnect the WAN, and restart the node with its upstream identity provider and DNS unavailable. Confirm the agreed capture mode continues and a local operator sees the disconnection.
2. Cut the link immediately after a central commit and before the station receives its acknowledgement. On replay, compare the central event IDs, counts and checksums with the fixture. Verify any duplicate delivery produced one durable effect.
3. Restore connectivity, observe live capture and measure backlog drainage. Exercise the low-space threshold and prove the defined admission and alarm behavior before actual disk exhaustion.
4. Hand a second technician the replacement kit. Time a cold bootstrap and recovery with the approved local trust bundle. Record which retained records survive complete device loss separately from restart survival.

Use the [edge profile](../../profiles/remote/edge/disconnected/store-and-forward.md), [messaging contract](../../../modules/messaging/CAPABILITY.md) and [capacity worksheet](../../records/planning/capacity-model.md) to adapt this design.
