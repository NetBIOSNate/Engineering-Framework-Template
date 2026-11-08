# Terms used in infrastructure reviews

| Term | Working meaning | Question for the design |
| --- | --- | --- |
| Control plane | Services that configure or coordinate infrastructure. | Can existing traffic continue if this plane disappears? |
| Data plane | Path serving consumer traffic or moving stored data. | Which probe crosses the consumer's path? |
| Failure domain | Components vulnerable to one shared cause. | Which rack feed, account, release or operator do they share? |
| Blast radius | Consumers or resources one fault or change can affect. | Where is the boundary enforced? |
| Idempotence | Repeating an operation has the same intended effect as applying it once. | What happens after a timeout following a successful create? |
| Convergence and drift | Convergence brings observed state toward intent. Drift is a difference between the two. | Which writer owns the field? |
| SLI / SLO | A service level indicator measures a user-relevant outcome. Its objective sets a target over a window. | Which events enter the denominator? |
| RTO / RPO | Recovery time objective limits interruption. Recovery point objective limits tolerable age of recovered data relative to disruption. | Which timestamps define interruption and loss? |
| Fencing | Enforced exclusion of an old writer during transfer. | What prevents a partitioned primary from accepting writes? |
| Quorum | Members required for a particular agreement rule. | Can survivors communicate and meet that rule? |
| Backpressure | A signal or limit that slows admission when downstream work accumulates. | Does backlog age stabilize under continued traffic? |
| Out-of-band management | Independent management and recovery path. | Does it share power, network or identity with the failed system? |
| IaC and state | Infrastructure as code describes intent. Some tools track mappings from declarations to live resource IDs. | Can operators recover the mappings and serialize writes? |
| TTL and MTU | Time to live bounds cache or packet behavior in its protocol. Maximum transmission unit bounds packet size on a link. | Are real clients and the complete path tested? |
| Attestation | Verifiable statement about an artifact, build or other subject. | Who made it and does it bind the exact item in use? |
