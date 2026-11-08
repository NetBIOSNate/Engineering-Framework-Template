# Map dependency direction and contract ownership

Select one outcome with an end-to-end deadline. Draw edges toward the resources needed to deliver it. Label runtime calls, build dependencies, shared data, control signals and human or supplier dependencies individually. A nightly file feed and an operator-run reconciliation step can form a recovery cycle even when runtime calls are acyclic.

## Specify the edge

Name both endpoint owners, contract and unit conventions, allowed use, authentication or physical access, timeout, retry authority, version policy, failure behavior and exit cost. Identify synchronous edges on the user's critical path. Ask which neighbor can stop a cold start or prevent a restore even if steady operation appears independent.

## Allocate a deadline

A hypothetical interaction has a 2.0 s end-to-end deadline. Reserve 0.3 s for intake and 0.3 s to return a result. Two provider attempts of up to 0.6 s each and one 0.2 s backoff consume the remaining 1.4 s. This leaves zero slack in the proposed allocation. Propagate the remaining deadline, measure overhead and reduce the attempt budget or change the design if the bound cannot be met. Limit retries to operations whose effects can be identified or safely repeated.

If three layers each permit two attempts, one invocation can cause eight terminal calls on a single dependency path. Give one layer responsibility for retries and count actual attempts. A slow attribution provider can leave raw observations pending enrichment if that meets the mission. Define who drains the backlog and which users can see the pending state.

## Break a costly cycle

Mark a dependency cycle and ask whether both ends must deploy or recover simultaneously. Consider a stable contract, a locally recoverable copy with a staleness budget, or asynchronous transfer with reconciliation. Each choice moves work and failure handling to a named owner. Review with a delayed response and a mixed-version change. Measure deadline compliance, compare both endpoint interpretations and check the recovery route. See [compatibility and exit](evolution/compatibility-and-exit.md).

[Architecture field guide](../../framework/README.md)
