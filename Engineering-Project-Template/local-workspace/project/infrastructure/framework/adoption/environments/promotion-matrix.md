# Environment contracts and promotion evidence

## Hold the contract steady

Promote a reviewed definition and exact artifact identity. Vary the bindings that give an environment its authority, location and capacity. Record expected differences so a green staging result can be interpreted accurately.

| Environment | Access evidence | Network evidence | Resource evidence |
| --- | --- | --- | --- |
| [Development](../../../environment-definitions/development/access-policy-definitions/GUIDE.md) | Engineers can create owned fixtures and remove stale grants. | A preview has a named owner and bounded ingress and egress. | A fixture expires without deleting retained data. |
| [Testing](../../../environment-definitions/testing/access-policy-definitions/GUIDE.md) | Deterministic identities reproduce positive and negative probes. | Fault injection is isolated per run. | Two parallel runs preserve each other's state. |
| [Staging](../../../environment-definitions/staging/access-policy-definitions/GUIDE.md) | Production-like role shape with separate credentials. | Route, cache and TLS behavior are representative. | Canary, upgrade and recovery measured with explicit scale differences. |
| [Production](../../../environment-definitions/production/access-policy-definitions/GUIDE.md) | Bounded privileged actions have independent evidence. | Service, management and emergency paths have owners. | Consumer signal, surviving capacity and recoverability accepted. |
| [Disaster recovery](../../../environment-definitions/disaster-recovery/access-policy-definitions/GUIDE.md) | Recovery works through loss of primary access. | Isolated rehearsal, activation and failback paths tested. | Clean restore timed with available historical keys. |

## Assemble a release

1. List immutable inputs common to all environments. Put resource IDs, quotas, principals, prefixes and retention in an environment binding. Keep secret values in the designated custodian.
2. For each difference that affects a test, write its expected effect and who accepts the residual uncertainty. A staging database one hundredth the size of production cannot establish full-volume restore time.
3. Preserve evidence from the earlier environment and rerun probes whose conditions change. Record release digest, target, operator and stop condition for the next cohort.
4. Treat disaster recovery as a parallel operating contract. Update it when production dependencies change, then demonstrate that a previously supported recovery point can still be read.

The [catalog](../../reference/catalog.md) links all three policy guides for each environment.
