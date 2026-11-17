# Assemble modules into an environment

## Goal

Compose independently versioned capabilities into a deployment that can be understood and rebuilt from its inputs. This example records a provider-neutral contract. Map field names and resource types to the implementation selected by the project.

```text
environment             staging
owner                   survey-operations
network.scope           survey-stage
identity.writer.output  archive-producer-role-ref
storage.module          archive-store / release 2.1.0 / approved digest
storage.writer_ref      identity.writer.output
storage.location        approved-site-b
storage.retention_days  35
recovery.copy_scope     independently administered archive-vault
probe                   retrieve and verify yesterday's published manifest
```

## Resolve the assembly

1. Resolve a reviewed release set and environment binding into an effective configuration. Define the order of defaults, organization constraints, project settings and environment choices. Reject contradictory locked constraints. Require explicit values for fields whose default could expose data or destroy retained state.
2. Construct the dependency order from explicit outputs and inputs. The storage module waits for the writer reference, and the validation probe waits for both the store endpoint and reader access. Handle identity-policy cycles with staged enrollment or a separate binding after both resources exist.
3. Bind a separately authenticated execution identity and scope. Validate referenced objects belong to the intended environment and tenant. Require an explicit contract for a deliberately shared service. Record all external ownership so teardown can preserve shared assets.
4. Preview the effective changes, store the state generation and apply within that ownership boundary. After a partial run, read the live IDs before retrying. Publish effective input revision, resolved digests, exposed outputs, observed resource IDs and evidence location.

## Acceptance

Rebuild a disposable assembly from an empty environment and run the consumer probe. Re-render the same inputs and explain every remaining difference. Try binding a production-only role into the staging fixture and verify the validation or authorization boundary rejects it. Compare the [five environment contracts](../../../adoption/environments/promotion-matrix.md).
