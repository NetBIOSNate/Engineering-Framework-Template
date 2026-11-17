# Profile for shared and distributed services

Use this path when several customers, teams or workloads share infrastructure and one tenant's behavior can affect another's outcome. Agree the isolation promise for data, compute, queue capacity, control actions, diagnostics and restoration. Name any shared resource that remains a common failure domain.

## Walk a request across the tenancy boundary

Trace identity at ingress, authorization at the resource, cache keys, message ownership, durable write, backup and support export. Define which tenant identity comes from a trusted assignment. For cross-region flows specify where a write becomes authoritative, how readers recognize stale data, who can take over after partition and how a former writer is fenced out.

Two nested layers each permit three total attempts. One incoming operation can cause nine terminal attempts on this one-call path. Assign retries to one owner, cap attempts at two in the example and propagate the remaining deadline. Agree which clients can safely retry on refusal and how they learn the outcome of an uncertain write.

## Test the proposed isolation

Let tenant A exceed its agreed allowance while tenant B sends the reference load. Block the downstream service, observe admission and restore it with a backlog. An illustrative criterion for B is p95 completion within 250 ms over a specified ten-minute window. Report the number of admitted operations, success fraction, failures and timeouts alongside successful latency. Narrow the claim to the workload and shared resources exercised.

Check tenant A receives the documented throttle response, terminal attempts per admitted operation stay within the cap, and the test corpus yields zero cross-tenant reads including cache hits. Restore a single tenant into an isolated environment and verify scoped access to restored records. Preserve the tenancy and recovery views, per-hop budgets, workload definition and any explicitly accepted shared-risk budget. See [authority](../../../trust-boundaries/protection/identity-and-authority.md), [dependency budgets](../../../dependency-boundaries/contracts/direction-and-change.md) and [recovery](../../concerns/resilience/failure-domains-and-recovery.md).

[Architecture field guide](../../README.md)
