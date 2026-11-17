# Choose an execution environment

Write down what a work unit needs from the substrate. Include lifetime, startup deadline, memory ceiling, persistent state, CPU architecture, devices, network attachment, kernel privileges and licensing. Record who can patch the operating system and how long they need. These inputs often settle the choice before a benchmark does.

## Evaluate the candidates

- Managed execution fits bounded work when its duration, concurrency, network and startup limits fit the workload. Measure cold starts and the service's response to quota exhaustion. Establish which recovery actions the provider exposes.
- Containers suit repeatable packaging and shared capacity. Decide who owns the node image, scheduler, networking and upgrades. Identify workloads requiring a stronger isolation boundary. Test node eviction, registry unavailability and placement across failure domains.
- Virtual machines offer a separate guest kernel and accommodate long-lived processes and specialized agents. Price their idle capacity and patching effort. Build an image that can replace the guest without losing persistent volumes or host identity records.
- Bare metal can serve specialized devices or measured performance constraints. Include spare capacity, lead times, firmware compatibility and the scheduling impact of a failed host.

## Make the choice observable

Run identical representative work on the viable candidates. Record sustained throughput at the latency objective, time from zero to ready, recovery with one unit unavailable, operator effort per upgrade and total cost per completed work unit. For long-running work, interrupt a unit mid-job and verify ownership and checkpoint recovery. Record the selected environment, owner, rejected constraint and the demand level or product limitation that should trigger another review.
