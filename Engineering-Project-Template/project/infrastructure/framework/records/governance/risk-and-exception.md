# Time-bounded risk and exception record

## Fill in the decision

| Field | Record |
| --- | --- |
| Scope and baseline | [Asset IDs, environment, affected consumers, expected control and its source.] |
| Gap and mechanism | [Observed condition and how a credible failure or unauthorized action could occur.] |
| Consequence and exposure | [Affected data or service, duration, who can act, dependency on other controls.] |
| Treatment options | [Remove exposure, mitigate, transfer by an explicit agreement, or accept residual risk.] |
| Compensating measure | [Owner, installation revision, limitations and a test that could disprove the claim.] |
| Decision authority | [Named accountable person, decision date, operating restrictions and expiry.] |
| Retirement of exception | [Funded action, due date, expiry behavior, earlier trigger and verification owner.] |

**Example.** A remote gateway cannot obtain short-lived credentials until a supplier firmware update. List the gateway IDs, credential custody, management-source restriction, current exposure after a credential leak and the tested denial from an unapproved source. Set an expiry aligned with the replacement window. Name the person who will isolate the gateway or approve a revised plan if the delivery slips.

## Close

Re-test the original baseline on representative assets, record the result, restore ordinary policy and remove temporary controls or entitlements where appropriate. Keep the original consequence and decision history with the closure so later reviewers can tell how the exposure changed.
