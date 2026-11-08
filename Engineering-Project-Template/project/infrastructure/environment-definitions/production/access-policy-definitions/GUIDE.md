# Production administration and emergency custody

## Intended outcome

Every privileged production action has a bounded identity, a recoverable authorization path and evidence attributable to an operator or automation job.

## Policy inputs

Define separation of duties proportional to impact, role owner, temporary privilege lifetime, emergency access custodian, evidence destination and revocation target.

## Implementation sequence

1. Remove routine dependence on shared administrator credentials. Bind deploy identities to approved sources, target environment and specific operations.
2. Make exceptional access time-bound and independently logged. Protect recovery instructions and custody factors from the identity failure they must handle.
3. Reconcile departing people and suppliers, inherited groups and active sessions. Document which rights the service provider retains and how emergency support is audited.

## Evidence and handoff

Exercise a low-risk privileged task, expiry, revoked access and the recovery path under supervision. Compare issuance, action and revocation timestamps in an independently controlled audit destination. Retain the evidence location and accountable owner in the production service record.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
