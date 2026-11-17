# Infrastructure signals and independent monitoring

## Service goal

An on-call engineer can distinguish a failed service from a failed monitoring pipeline and locate the implicated dependency.

## Contract

Specify consumer probes, signal fields and units, inventory labels, allowed dimensions, sampling, retention, access and a destination outside the failure being observed.

## Build and commission

1. Collect demand, errors, latency and saturation at boundaries a consumer uses. Keep raw counts for objectives. Track timeouts and refused work in the denominator.
2. Separate security audit retention from sampled diagnostics. Scope log access and redact tokens and sensitive payloads before forwarding. Budget high-cardinality identifiers to prevent uncontrolled series growth.
3. Bound buffers and decide overflow behavior. Measure oldest event, drops, exporter errors and time skew. Provide independent heartbeat delivery for lost telemetry.

## Acceptance exercise

Send a uniquely identified synthetic event from source to query and page. Disconnect a test exporter, confirm independent detection, reconnect it and observe replay and buffer drainage. Reconstruct a request timeline using both source and ingestion timestamps.

## Revisit the design

Review probe coverage after topology changes. A green dashboard whose last observation is stale must expose its age.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
