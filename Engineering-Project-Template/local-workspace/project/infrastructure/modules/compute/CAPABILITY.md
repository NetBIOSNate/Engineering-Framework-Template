# Compute pools and failure placement

## Service goal

Deliver measured work at an agreed tail latency or completion deadline through routine replacement and the chosen domain loss.

## Contract

Define architecture, image, identity, device and kernel needs, persistence, placement, quotas, health signal, drain timeout, startup and sustained capacity per unit.

## Build and commission

1. Benchmark representative work per unit at the objective. A safe rate of 100 requests/s and a 1,200/s peak require twelve surviving units. Across three equal domains, six per domain yield twelve after one loss, before additional headroom.
2. Distribute units across verified failure domains. Budget for replacement overlap, provider quota, subnets, downstream limits and the time to warm a cold host.
3. Use distinct readiness and liveness checks. Stop admitting work before draining. For stateful work, transfer or fence ownership before letting a replacement serve writes.

## Acceptance exercise

Replace one healthy instance at representative load, then test loss of the largest modeled domain in an authorized test boundary. Record consumer errors, tail latency, peak queue and time until full redundancy returns.

## Revisit the design

Rebenchmark when payload shape, host type, memory pressure or runtime changes. Peak CPU alone cannot predict downstream saturation.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
