# Recovery identity during primary control-plane loss

## Intended outcome

Authorized responders can access clean recovery assets while compromised or unavailable primary credentials cannot erase recovery copies.

## Policy inputs

Identify incident authority, recovery issuer or custody arrangement, independent audit path, minimum restore permissions, historical key access and handback procedure.

## Implementation sequence

1. Trace all login dependencies including DNS, time, network, devices and second factors. Remove circular dependencies on systems that responders must restore.
2. Limit standby credentials between events and protect access to backup deletion and historical key destruction. Agree who can declare recovery and who can fence an old writer.
3. Activate recovery access in an isolated exercise. Preserve a bounded evidence trail, rotate exercised emergency material as applicable, and revoke temporary roles after handback.

## Evidence and handoff

Prevent use of the normal operator identity during the drill. Recover an encrypted fixture with a retained key and verify a primary-only principal cannot delete the recovery copy. Record time to access, custody actions, failed paths and the next owner.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
