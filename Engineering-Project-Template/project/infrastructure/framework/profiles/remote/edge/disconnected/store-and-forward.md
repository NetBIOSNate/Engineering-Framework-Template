# Edge sites with intermittent connections

## When to use this profile

A branch, vessel or field station must continue a defined local operation while its WAN link is unavailable. Determine which work can pause, which must proceed locally and who resolves conflicts when connectivity returns. Record the maximum disconnection the project funds.

## Design the disconnected interval

1. Inventory local dependencies for boot, login, name resolution, clock, certificates and storage. Restart a fresh node with the WAN disabled. A warm process can mask an external dependency for hours.
2. Size durable spooling for peak production and the outage duration. At 150 KiB/s for 12 h, raw input is about 6.18 GiB. A 25% overhead allowance gives 7.73 GiB before filesystem reserve, write amplification and any separate alarm queue. Measure the allowance with the actual encoding.
3. Choose what happens at each occupancy threshold. Preserve acknowledged records according to contract, reserve space for alarms, and bound low-priority admission. A disconnected site needs a local signal when operator intervention is required.
4. Give events stable identifiers and per-source sequence numbers. Define acceptance of duplicates, out-of-order records and simultaneous edits. Rate-limit replay so reconnecting sites cannot overload the central collector. Drain capacity must exceed live ingress.

## Prove the profile

Introduce a controlled WAN loss on a bench. Reboot, advance through a credential renewal interval, fill the spool to the warning threshold, and reconnect through a flapping link. Verify local service, ordering assumptions, duplicate suppression, alarm delivery and time to empty the backlog. Identify the site owner, replacement lead time and the locally accessible recovery method.
