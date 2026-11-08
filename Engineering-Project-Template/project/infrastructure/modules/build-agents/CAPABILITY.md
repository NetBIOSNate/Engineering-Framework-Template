# Build agents and privileged execution

## Service goal

An infrastructure change runs on a known worker, with narrowly bounded credentials, and leaves an auditable relationship between input and output.

## Contract

Specify runner image and digest, supported job types, queue policy, maximum job duration, network reach, identity scope, cache isolation and teardown behavior.

## Build and commission

1. Give untrusted change previews a pool without production deployment rights. Use a distinct short-lived identity for approved apply jobs and bind it to the intended environment.
2. Recreate workers from a versioned image. Separate writable workspaces, caches and signing functions by trust level. Scope secret issuance to the job and resource.
3. Budget disk, parallel slots and egress for simultaneous cold builds. Drain a worker before host maintenance and document the fate of interrupted work and partial artifacts.

## Acceptance exercise

Submit a harmless fixture to both pools. Confirm the preview cannot use the production credential. Cancel a job during publication and verify incomplete artifacts are invisible to consumers. On the replacement worker, prove the preceding job's credentials and workspace are inaccessible.

## Revisit the design

Watch oldest queued job and time to obtain a worker. Increase capacity only after ruling out a failing dependency that causes retries.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
