# Profile for product families and engineered variants

Use this path when several products share an architecture but differ by market, equipment, capacity or operating environment. Identify the common mission and the outcomes each variant must preserve. Specify variation points at a boundary the team can test and support.

## Model what may vary

| Variation point | Binding time | Constraint or consequence |
| --- | --- | --- |
| Sensor module | Assembly or field replacement | Compatible connector, calibration source and input range |
| Offline retention | Provisioning | Advertised capacity must fit actual storage and endurance budget |
| Analysis rule set | Release or configuration | Preserve meaning of prior records and identify rule version in reports |
| User authority | Enrollment and operation | Physical or administrative permissions remain enforced across variants |

For each variation point name the owner, valid choices, prohibited combinations, evidence inherited from the common design and evidence specific to the variant. An option fixed at manufacture has different verification, support and recovery costs from one changed at run time. Keep the supported configurations in a versioned manifest with hardware, firmware, schema and calibration identity.

Suppose three selectable sensor heads, two power packs and two radio options produce twelve nominal combinations. A high-current head with the low-capacity pack may violate an operating constraint under transmit load. Express the exclusion in the configuration model and at the point of assembly or provisioning. Exercise the worst credible concurrent load on allowed boundary combinations. Pairwise tests cover pairs while a three-way interaction may still determine the outcome.

Review how support staff identify an installed configuration after replacement and how records retain the calibration applicable at capture time. A new variant should explain which claims it inherits, which assumptions changed and who owns its service life. See [physical interfaces](../../../dependency-boundaries/contracts/physical/interfaces-and-tolerances.md), [capacity budgets](../../../capacity-planning/modeling/workload-and-budgets.md) and [evidence selection](../../../decisions/records/evidence/experiments-and-reversibility.md).

[Architecture field guide](../../README.md)
