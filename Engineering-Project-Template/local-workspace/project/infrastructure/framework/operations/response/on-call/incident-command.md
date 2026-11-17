# On-call and incident command

**Goal.** Give the first responder authority to stabilize infrastructure and a way to hand over incomplete work. Each paged service needs a primary responder, backup contact, reachability test and concise first-action runbook.

1. Qualify the page using a consumer-path probe and establish affected services, sites, tenants and start time. Open a UTC incident log. Assign incident command, hands-on operations, communications and timeline recording. In a small team, one responder may hold several roles. Name the person authorized to halt changes or invoke recovery.
2. Record each hypothesis with an observation that could disprove it. For each change, record the operator, expected effect, stop condition and reversal. Prefer a reversible isolation step while impact is growing. Preserve relevant audit records and route suspected security compromise to the designated security contact using an independent channel when necessary.
3. At handoff, read back the current impact, last change, active hypothesis, next checkpoint and remaining hazards. Validate recovery by replaying an affected journey and checking the backlog or data reconciliation. Record separately when impact began, detection occurred, mitigation worked and complete recovery was verified.

**Review evidence.** Compare the timeline with paging and change records. Give corrective actions owners and acceptance checks tied to the failure. A runbook revision is complete when a second operator can follow it during a rehearsal. [NIST SP 800-61 Rev. 3, cybersecurity incident response](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
