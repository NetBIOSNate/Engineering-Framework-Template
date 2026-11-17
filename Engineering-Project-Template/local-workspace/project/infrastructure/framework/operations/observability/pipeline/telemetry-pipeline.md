# Observability and telemetry delivery

**Goal.** Preserve enough independent evidence to explain an outage even if the affected platform also hosts its usual monitoring. Draw the path from emitter through collector, buffer, transport and storage to alert router and operator.

1. For each critical path, select a consumer probe, duration histogram, traffic count, failure count and relevant saturation measurement. Put detailed object identifiers in access-controlled logs or traces. Bound metric dimensions using stable fields such as site and service class. Estimate an upper bound on the number of time series for each metric by multiplying the distinct values of its proposed dimensions.
2. Give queues a byte limit, retention duration and explicit overflow policy. For 2 MiB/s sustained input, 30 minutes without egress needs about 3.52 GiB before indexing, replication or burst allowance. Track oldest unshipped event, dropped records, exporter errors and clock offset. Separate event time from arrival time so delayed data can be identified.
3. Send a recognizable test event end to end. Then disconnect the test exporter for a bounded interval. Confirm the independent heartbeat detects loss, operators can retrieve an event across tiers, buffers recover within their storage limits and replay stays within the service network budget.

**Review evidence.** Record expected and observed delivery delay, retained fields, access scope, disk use and missing-data behavior. Match security audit record retention and integrity controls to the audit requirement independently of diagnostic sampling.
