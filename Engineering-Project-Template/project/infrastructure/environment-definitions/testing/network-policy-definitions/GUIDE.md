# Isolated network test cells

## Intended outcome

Fault tests can deliberately break connectivity and observe the result within a known, bounded test domain.

## Policy inputs

Define per-run address scope, allowed routes, DNS suffix, fault injection point, reversal path, telemetry destination and test controller.

## Implementation sequence

1. Build an isolated routing domain for fixtures. Route external dependencies to controlled endpoints when latency, loss or timeout behavior must be reproducible.
2. Record the baseline path with client and destination probes. Apply one bounded fault, such as loss of a resolver or a reduced tunnel MTU, while retaining independent management.
3. Repeat representative connections for both IP families in scope and verify cleanup restores the original route, DNS response and effective MTU.

## Evidence and handoff

Compare cached and uncached queries during resolver loss. Confirm control traffic reached the fixture, isolation prevented access to shared networks, and recovery probes returned to baseline. Preserve the topology revision and injected fault duration with the test result.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
