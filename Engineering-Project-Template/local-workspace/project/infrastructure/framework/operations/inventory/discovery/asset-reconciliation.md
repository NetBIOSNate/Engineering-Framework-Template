# Reconcile intended resources with the estate that actually runs

## Goal

Maintain an inventory good enough to answer three operational questions. Who owns this asset, what breaks if it disappears, and can the team replace or retire it?

1. Select stable identifiers for each asset class. A chassis serial, cloud resource ID, certificate issuer and serial pair, or storage volume ID usually survives more changes than a display name. Track logical service identity separately from the replaceable physical instance.
2. Collect declared configuration, provider or device readback, network and identity observations, purchasing records and backup coverage with timestamps. Mark each source's authority and blind spots. A device absent from the current scan could be offline, access-restricted, retired or genuinely missing.
3. Reconcile in both directions. A declared asset missing from reality may indicate failed provisioning or a stale mapping. A running asset absent from declarations may be an emergency fix, inherited service or orphan. Assign an owner to investigate before remediation.
4. Track location, tenant, lifecycle state, ownership, software or firmware version, management route, dependency references, cost allocation, support deadline and evidence freshness. Minimize collection of secrets and sensitive topology. Define retention and access for the register.
5. Sample for accuracy. Pick assets from a supplier bill and find their owners. Pick owners from the register and trace to live management IDs, backup policies and alerts. Measure unmatched items, duplicate IDs and time from provisioning to discovery.

## Close the loop

For a replaced host, transfer its logical role, verify existing monitors now follow the new ID, quarantine the old asset until its data disposition is known, and reconcile its support and billing records. An inventory entry reaches retirement when its remaining obligations have an explicit owner.
