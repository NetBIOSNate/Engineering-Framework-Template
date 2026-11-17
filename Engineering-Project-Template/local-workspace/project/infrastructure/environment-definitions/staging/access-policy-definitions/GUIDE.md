# Rehearse production authority in staging

## Intended outcome

A production-bound change exercises the same identity relationships while using distinct staging principals and keys.

## Policy inputs

Record issuer and audience, claim shape, role mapping, operator and automation identities, key references, and expected parity or explicit differences.

## Implementation sequence

1. Replicate the authorization structure including approval, deny rules, expiration and break-glass logging. Bind grants to staging resource identifiers.
2. Run promotion under the delivery identity and operate the probe under the ordinary consumer identity. Confirm neither relies on an engineer's cached credentials.
3. Rehearse rotation with an overlapping trust window, new sessions and an explicit old-key rejection. Record deviations that prevent production extrapolation.

## Evidence and handoff

Use a wrong-environment token against the staging endpoint and a staging identity against a designated denial probe at the production boundary. Confirm denial without returning sensitive data. Attach policy revision, principal claims used and redacted test evidence to the release review.

Compare the [environment contracts](../../../framework/adoption/environments/promotion-matrix.md) before reusing this decision elsewhere.
