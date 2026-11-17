# Ingress, egress and overload at the service boundary

## Design the path

Trace client discovery, edge routing, transport or TLS termination, upstream selection, response path and timeout. Draw separate paths for operator access and health checking. Name who can change certificates, DNS records, route preferences and load balancer membership.

1. Define which health signal may take a backend out of service. A dependency shared by every backend can cause all targets to be ejected simultaneously. Decide whether to serve a degraded response, reject work, or retain carefully bounded traffic when all checks fail.
2. Set an end-to-end deadline and allocate budgets across hops. Bound connection pools, queues, retry attempts and payloads. When multiple layers retry independently, a single client operation can amplify traffic to an already saturated backend. Select the layer that owns retries and define when retry is safe.
3. Size public and private egress for new-connection rate, ephemeral ports and destination skew. Exercise idle connection timeouts, long-lived streams, certificate replacement, client-IP preservation and return routing at stateful devices.
4. Keep overload observable. Count attempted, admitted, rejected and completed work alongside queue age. Record where a caller sees rejection, the retry hint if any and the cost of the rejected request.

## Acceptance

In staging, withdraw one healthy backend and observe active streams and new requests. Introduce a slow dependency and verify the admission policy bounds backlog at the agreed maximum. Compare during-fault client latency, rejection rate and post-recovery drain time against the [quality targets](../../../requirements/quality/targets.md).
