# Service record and operator handoff

## Service identity

| Field | Fill in |
| --- | --- |
| Capability, consumer and owner | [What outcome matters, to whom, and who can change the promise?] |
| Operational contacts | [Primary, backup, supplier, facilities, security and escalation path outside the service.] |
| Boundary | [Inventory IDs, locations, tenant, data classes, dependencies and shared failure domains.] |
| Objective and signals | [User-path probe, objective window, measurement gaps, page route and initial action.] |
| Known-good release | [Immutable input, deployed version, control state mapping and recovery instructions.] |
| Maintenance | [Window, recent exercise, spare capacity, support expiry and contract renewal date.] |
| Recovery | [RTO/RPO, latest verified marker, restore location, emergency custody and contact.] |
| Cost and lifecycle | [Funding owner, unit of value, typical and peak cost, retention and exit dependencies.] |

## Handoff exercise

Give a second operator the service identifier and a simulated degradation. Ask them to find the consumer signal, distinguish service failure from monitoring failure, locate the correct owner, and recover a clean fixture. Observe where undocumented knowledge is required. Add an evidence reference and review date for every correction.

**Example.** A file service can report healthy storage while the analyst's credential no longer grants read access. The handoff should show the check run as the analyst, the issuer owner, the fallback contact and how to confirm that the actual consumer can retrieve the file after repair.

## Review triggers

Update the record when the team, supplier, trust root, critical path or capacity assumption changes. Keep credentials and sensitive topology in the access-controlled system of record and link to their custodian here.
