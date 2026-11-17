# Place identity and authority at trust boundaries

A trust boundary occurs wherever a design starts relying on a different identity, administrator, physical environment or source of evidence. Trace the ordinary path and the paths used for enrollment, service, backup, emergency access and decommissioning. Name the asset and the action that requires authority at each crossing.

## Build an authority table

| Subject | Resource and action | Trusted basis | Enforcement and evidence |
| --- | --- | --- | --- |
| Field device | Submit observation for its assigned site | Enrollment binding between device identity and site | Intake checks binding and records disposition |
| Maintainer | Rotate the credential of an assigned device | Authenticated role and maintenance scope | Enrollment owner records old and new credential references |
| Duty operator | Review a quarantined observation | Operator assignment to the affected site | Review record names the observation and rationale |
| Intervention authority | Authorize a physical action | Operating procedure and current authority | Action owner verifies permission and observes the result |

Untrusted input can name a site, customer or role. The resource owner checks that assertion against the trusted assignment. Record what happens when identity services are unavailable, when a credential is valid but privileges changed, and when access must be revoked across cached or disconnected components. Specify the exposure window and who accepts it.

## Delayed data after revocation

A revoked device may hold hours of offline observations. Its local timestamps can be forged or reset. One policy is to quarantine uploads arriving after revocation and let a reviewer decide their disposition, subject to the system's record-handling requirements. If authentication rejects the device at the transport boundary, provide a separately authorized recovery route if retaining the records is required. Make the chosen route and evidence explicit.

Try a valid identity from site A with a payload naming site B. Check the cross-site effect is denied. Test a maintainer attempting an intervention and a revoked device after the promised propagation window. Inspect audit entries for sufficient attribution and absence of credential material. See [threats and privacy](assurance/threats-and-privacy.md) and [tenant isolation](../../framework/profiles/shared-services/tenant-isolation.md).

[Architecture field guide](../../framework/README.md)
