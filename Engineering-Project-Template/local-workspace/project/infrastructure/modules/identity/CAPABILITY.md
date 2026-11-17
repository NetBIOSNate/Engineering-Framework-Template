# Identity federation and recovery access

## Service goal

People and machines receive the least authority needed to perform a named action for a bounded period, with recoverable access through issuer outages.

## Contract

Define issuer, audience, subject, tenant, role, credential lifetime, claim validation, revocation path, required audit fields and owner of emergency authority.

## Build and commission

1. Separate human, workload, deployment and recovery roles. Map permissions to resource and action. Restrict federation subjects and intended audience so a token for one environment cannot authorize another.
2. Decide the fate of existing sessions and new logins during issuer unavailability. Map dependencies on DNS, certificates and time before designing emergency access.
3. Provide independently reachable recovery credentials and audited custody. Design removal of departing staff or suppliers, including group inheritance and active sessions.

## Acceptance exercise

Exercise a permitted action and its cross-tenant counterpart. Try a valid token minted for another audience. Revoke a fixture user's access and measure when existing sessions stop working. Time a recovery login with the usual provider unavailable and review the custody event.

## Revisit the design

Check grants after organizational changes and service transfers. Record the interval between revocation and the last usable cached authorization.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
