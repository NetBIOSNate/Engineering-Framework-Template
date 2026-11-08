# Choose push, pull and emergency reconciliation behavior

## Decision

Pick a delivery mechanism that the target, connectivity and operator model can support. Define who holds the write credential, who chooses desired state, how changes are attributed and how a partial apply converges.

| Model | Useful condition | Failure to rehearse |
| --- | --- | --- |
| Reviewed push to a provider API | Target exposes a transactional or queryable management interface and the runner can reach it. | Runner times out after the provider created an object. |
| Pull-based reconciliation | Local agents can retrieve versioned desired state and observe actual state continuously. | Source becomes unreachable while the cluster continues serving. |
| Signed offline release | Device or site has no persistent upstream path. | Transfer stops midway or local trust data is stale. |
| Controlled appliance change | Device exposes a limited command or configuration interface. | Management access drops after the first part of a route change. |

For a GitOps implementation, the OpenGitOps principles pair declarative intent and immutable version history with automated pull and continuous reconciliation. An appliance workflow can instead retain an intended configuration, review an export and compare with actual state after a bounded apply. [OpenGitOps principles](https://opengitops.dev/)

## Handle exceptions

Give each property one authoritative writer. Define how to pause reconciliation during incident containment, who owns the pause, its expiry and how an emergency configuration becomes reviewed intent. Before resuming, preview the difference so the controller does not undo isolation or recreate a compromised component.

## Prove convergence

Use a fixture with a known ID. Apply the same change twice, interrupt after resource creation once and introduce an out-of-band mutation. Reconcile using live inventory and authorized state. Record which actions retried safely, which required a human decision and how evidence links source revision, target and observed generation.
