# Field observations, part 1 — mission and options

This fictional case follows one decision from user need through design and evaluation. All targets are illustrative. The calculations are design estimates. Device and system tests described in this case are planned.

## Mission and drivers

A field inspector uses an instrument to collect observations even when the radio link is unavailable. The duty operator needs a traceable history and an indication of stale data. The equipment authority retains control of physical intervention. The observation service has no authority to move equipment.

| ID | Concern | Decision-driving condition |
| --- | --- | --- |
| DRV-01 | A field inspector can continue collecting | One commissioned unit loses connectivity for 12 hours while generating 2 observations/s at 600 payload bytes each |
| QS-01 | Acceptance means custody survived a local restart | An observation acknowledged locally can be retrieved after a power cycle under the specified storage failure model |
| QS-02 | The duty operator can trust eventual completeness | After reconnect, reconcile accepted IDs and drain the backlog in less than four hours while new work continues |
| QS-03 | The duty operator can distinguish stale information | The display supplies observation age or its uncertainty, including after a device clock reset |

## ADR-01 — where to take custody

| Option | Benefit | Decisive limitation |
| --- | --- | --- |
| Accept only after remote commit | One central record with straightforward remote lookup | The inspector cannot complete local capture during a partition |
| Persist at the site gateway | Shared medium with easier maintenance | Loss of the device-to-gateway hop leaves accepted capture unsupported |
| Persist at the device | Covers loss of either hop and allows immediate local receipt | Storage wear, reliable identity, format evolution and power-loss recovery move into the device |

Provisionally select durable device capture. The field-product lead owns the local receipt meaning, the platform lead owns deduplication and committed remote receipts, and the service owner decides whether measured catch-up meets the mission. Physical destruction of the only offline copy remains a residual risk for the sponsor to evaluate. Procurement is the last responsible decision point for storage capacity and endurance.

The device's observed time may be uncertain. Decide to preserve both the local time and its quality, plus a distinct service receipt time. Final acceptance of ADR-01 depends on a power-cut exercise and a representative storage and replay measurement. Continue to [part 2, views and contracts](../02-design/views-and-contracts.md).

[Architecture field guide](../../../README.md)
