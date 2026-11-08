# Database infrastructure and writer ownership

## Service goal

Return committed data with a stated consistency guarantee and recover a usable, internally consistent store after the selected failure.

## Contract

Specify writer and reader endpoints, supported isolation and acknowledgement behavior, maximum replication lag, connection budget, recovery point, maintenance window and encryption key custody.

## Build and commission

1. Model read/write mix, hotspots, transaction size, connection counts and growth. Allocate connection limits across clients and retain an operator reserve.
2. Place quorum and durable replicas with awareness of actual site and storage dependencies. Identify whether a successful commit can be lost on promotion. Prevent the former writer from accepting writes after a failover.
3. Protect base backups and transaction history. Record exact database version, extensions, collation and keys required to restore. Rehearse upgrades on a realistic copy and check the reversal point.

## Acceptance exercise

Insert numbered synthetic transactions. Interrupt replication on a test pair and observe lag. Fence the old writer, promote the eligible replica, reconnect a client and compare acknowledged sequence numbers. Separately restore to before a deliberate logical deletion and check constraints and totals.

## Revisit the design

Review high-water marks for connection use, log growth, replica lag and time to replay a day's changes. Verify maintenance will fit the actual recovery window.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
