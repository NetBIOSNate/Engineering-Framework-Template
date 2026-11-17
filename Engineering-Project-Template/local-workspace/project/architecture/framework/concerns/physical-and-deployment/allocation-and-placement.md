# Allocate functions to people, devices and infrastructure

Start with a logical responsibility map, then assign each function and store to a person, location, device or execution environment. Compare deployment candidates against latency, physical access, energy, isolation, jurisdictional constraints agreed by the project, cost and recovery. A local placement can preserve operation through a partition and increase field maintenance obligations.

## Make the allocation visible

| Logical function | Candidate placement | Decision-driving evidence |
| --- | --- | --- |
| Capture and first durable receipt | Field unit | Offline duration, local medium endurance, startup and safe removal |
| Normalize and aggregate | Gateway or central processor | Upstream bandwidth, schema change rate, power and repair access |
| Emergency intervention | Authorized local role or controller | Hazard analysis, response bound, independence and authority |
| Historical analysis | Central store with a defined export contract | Retention purpose, completeness, access and read-back fidelity |

Show the allocation in at least two operating states if startup, maintenance or recovery uses different dependencies. Trace power, data, control, timing and administrative authority along each critical path. Mark shared items that defeat independence, including enclosure cooling, a common ground, shared clock source, sign-in authority and the same technician on call for both sites.

A field design proposing a spare computer in the same cabinet may tolerate processor failure and still fail when the cabinet overheats. Describe the protected event and the surviving path. Calculate power and thermal budgets using credible concurrent peaks and environmental conditions. A duty-cycle average can hide a startup surge or thermal limit.

Trace replacement from fault detection to a verified return to service. Include lifting clearance, remote access during a network outage, credential provisioning and compatibility of spare parts with stored data. Review the placement with a maintainer and operator as well as the designer. Capture any constraints the implementation must preserve in the [allocation and interface record](../../worksheets/design/view-and-interface.md).

[Architecture field guide](../../README.md)
