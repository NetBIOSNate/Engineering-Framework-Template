# Artifact storage and distribution

## Service goal

A new host can retrieve the exact approved image, package or module required to rebuild an environment even after the primary cache disappears.

## Contract

Publish the repository namespace, immutable digest, provenance policy, read and publish identities, supported architectures, retention and cold-pull throughput. Record who can withdraw a compromised artifact and who owns historical versions.

## Build and commission

1. Separate publication, promotion, consumption and deletion privileges. Resolve mutable aliases to a digest at review and promote the same verified bytes through environments.
2. Place mirrors or caches near slow links. Estimate cold-start bandwidth from concurrent empty hosts, compressed image size and the allowed start interval. Include a burst after a site restart.
3. Protect manifests, signatures, signing trust and repository metadata. Document the order in which clients can trust and use a mirror during bootstrap.

## Acceptance exercise

Evict a disposable node's cache. Pull the released digest, verify its signer and start a probe. Offer a tampered copy and capture rejection. Cut the mirror link and measure time to fetch from the alternate path. Restore an older retained digest from backup.

## Revisit the design

Compare the available retention window with rollback, audit and isolated-site needs before garbage collection. A tag that still exists can point to different bytes.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
