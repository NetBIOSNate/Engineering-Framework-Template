# Host hardening, vulnerability response and firmware support

## Goal

Run supported infrastructure with a known baseline and a rehearsed response when an exposed component cannot be fixed immediately.

1. Inventory hardware or service model, firmware, OS image, installed roles, exposed interfaces, packages, origin, patch owner and support end date. Record which baseline applies to each role and which exceptions an appliance vendor requires. Disable or restrict unused management services and establish an independent management route.
2. Correlate supplier advisories and inventory. Prioritize according to exposed path, privileges, exploitability, operational consequence and compensating controls. Track assets the scanner cannot see, including intermittently connected hosts and powered-off spares.
3. Build a candidate image or update bundle. Verify origin, test cold boot, management access, workload health, backup readability and rollback compatibility. For firmware, verify that downgrade is supported or have tested rescue media and a compatible spare.
4. Apply to a representative cohort, observe through the relevant maintenance cycle, and expand within disruption tolerance. If a patch breaks a critical dependency, restrict exposure, identify the approving risk owner and set a dated alternative treatment.
5. Reconcile actual versions and configuration after deployment. Reimage or repair stragglers, including hosts that were offline during the rollout.

## Evidence

Compare inventory coverage against known assets. Retain the tested baseline revision, failed probe, remediation owner, due date, rollback outcome and date the exception ends. A passing scan of reachable assets cannot establish the condition of an offline spare. [NIST SP 800-193](https://csrc.nist.gov/pubs/sp/800/193/final)
