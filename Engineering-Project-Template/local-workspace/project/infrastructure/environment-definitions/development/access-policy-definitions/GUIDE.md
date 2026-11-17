# Development access and developer autonomy

## Intended outcome

Engineers can build and dispose of their own fixtures without acquiring authority over shared or production resources.

## Policy inputs

Define sandbox owner, developer group, delegated actions, test-data classification, expiration and rotation of automation access.

## Implementation sequence

1. Give contributors scoped self-service within named development spaces. Assign a separate workload identity per fixture that needs network or data access.
2. Use synthetic or explicitly approved development data. Keep production issuers, high-privilege roles and production secret stores outside normal sandbox grants.
3. Tie teardown and grant review to the sandbox lifecycle. Preserve ownership on shared dependencies so an expired experiment cannot remove a teammate's resource.

## Evidence and handoff

Using a developer identity, create a harmless fixture, inspect it, then attempt to list a neighboring sandbox and access production secrets. Capture the actual authorization decision. Record the sandbox owner, expiry and who can recover abandoned fixtures.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
