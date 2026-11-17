# Bootstrap DNS, time and certificates

List what an empty host needs to find a service and trust its certificate. Name resolution, accurate time and a trust anchor often depend on systems that themselves need authenticated network access. Draw arrows for each startup dependency and circle any cycle. Assign an owner to each source of initial trust.

## Build a cold-start path

1. Provide network configuration and an approved path to a Domain Name System (DNS) resolver. Record how the resolver reaches its upstream servers after a reboot, including the authoritative service for internal zones. Protect zone changes, delegation and transfer permissions. Document who can recover the domain or private namespace.
2. Establish an initial time source consistent with the threat model and hardware capability. Define tolerable skew, independent observations and operator response when clocks disagree. Document how a host with an invalid clock obtains trustworthy time before certificate-based authentication becomes viable.
3. Provision a validated trust bundle and identity enrollment method. Inventory issuers, deployed certificates, renewal owners, expiry thresholds and revocation behavior during disconnection. Stage new and old trust roots together where supported, renew dependents, verify adoption, then retire the old root at the agreed boundary.

## Exercise startup and transition

Boot an isolated test host with empty caches. Resolve a private service name, synchronize its clock, enroll identity and authenticate a real request. Repeat with an upstream resolver unavailable and with a controlled skew in a disposable guest. Observe cached DNS results over the cutover and verify the failure mode for an untrusted certificate. Retain timestamps, error signals, issuer identifiers and recovery time. Store secret keys in the designated custody system.
