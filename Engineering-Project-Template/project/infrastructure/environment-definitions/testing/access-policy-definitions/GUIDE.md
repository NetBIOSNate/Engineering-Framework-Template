# Test identities and evidence custody

## Intended outcome

A test can exercise authorization boundaries reproducibly without inheriting the operator's existing access.

## Policy inputs

Record test suite, issuer, test tenant, expected roles, allowed fixtures, token lifetime and destination for redacted evidence.

## Implementation sequence

1. Create distinct fixture principals for normal consumer, unauthorized neighbor, administrator and expired credential. Keep the test harness identity separate from the identity under test.
2. Seed fixtures with deterministic ownership. Run positive and negative probes with newly acquired sessions so cached administrator access cannot mask failures.
3. Constrain test runners to the selected environment. Remove transient grants when the run ends and keep enough metadata to reproduce a failing decision.

## Evidence and handoff

Replay a cross-tenant read using both a list operation and a direct object identifier. Verify the failure came from the intended policy and that logs contain the correlation ID without credentials. Assign triage to the owner of the deciding control.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
