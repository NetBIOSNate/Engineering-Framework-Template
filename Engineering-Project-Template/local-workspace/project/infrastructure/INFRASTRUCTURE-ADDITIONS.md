# Infrastructure framework additions

Installation record for 8 November 2026. The working root is the project's existing infrastructure directory. Start with the [field guide](framework/START-HERE.md), browse the [complete catalog](framework/reference/catalog.md), or review [how the library was assembled](framework/adoption/authoring/installation-record.md).

## Delivered footprint

| Item | Count |
| --- | ---: |
| Original directories checked against the starting inventory | 32 |
| Original files present at the start | 0 |
| New directories | 115 |
| New guidance, navigation and record documents | 93 |
| This root inventory | 1 |
| Total new files including this inventory | 94 |

The ten existing module folders each gained a capability contract. Each of the fifteen access, network and resource policy folders across the five existing environments gained an environment-specific guide. The other 68 documents form the shared framework. The deepest guides sit under six directory levels below this root.

The shared library covers requirements, architecture decisions, module composition, physical and logical platforms, security and supply-chain controls, deployment, observability, incident response, continuity, capacity, cost, sustainability and retirement. Seven deployment profiles, two complete worked designs and nine reusable records support project adoption. The [framework crosswalk](framework/reference/framework-crosswalk.md) identifies the primary sources and the evidence each can help a project produce.

All workspace additions were made with native Windows PowerShell. Before this final file was created, the original directory paths, creation times and attributes were checked, all 93 documents were read, local references were evaluated, and SHA-256 digests were collected. Example infrastructure targets and drills are guidance for future projects. This installation created documentation.

## New directories

Paths below are relative to the infrastructure root. Existing parent directories are excluded from this directory list.

~~~text
framework/
framework/adoption/
framework/adoption/authoring/
framework/adoption/environments/
framework/adoption/learning/
framework/adoption/learning/windows/
framework/adoption/lifecycle/
framework/controls/
framework/controls/cryptography/
framework/controls/cryptography/rotation/
framework/controls/delivery/
framework/controls/delivery/automation/
framework/controls/delivery/promotion/
framework/controls/delivery/state/
framework/controls/governance/
framework/controls/governance/exceptions/
framework/controls/governance/suppliers/
framework/controls/identity/
framework/controls/identity/tenancy/
framework/controls/lifecycle/
framework/controls/lifecycle/retirement/
framework/controls/security/
framework/controls/security/design/
framework/controls/security/hardening/
framework/controls/supply-chain/
framework/controls/supply-chain/verification/
framework/design/
framework/design/boundaries/
framework/design/boundaries/ownership/
framework/design/composition/
framework/design/composition/bindings/
framework/design/composition/contracts/
framework/design/decisions/
framework/design/decisions/topology/
framework/design/platform/
framework/design/platform/compute/
framework/design/platform/compute/bootstrap/
framework/design/platform/compute/placement/
framework/design/platform/compute/scheduling/
framework/design/platform/data/
framework/design/platform/data/cache/
framework/design/platform/data/replication/
framework/design/platform/facilities/
framework/design/platform/facilities/power/
framework/design/platform/network/
framework/design/platform/network/addressing/
framework/design/platform/network/naming/
framework/design/platform/network/naming/trust/
framework/design/platform/network/traffic/
framework/design/platform/network/wan/
framework/design/platform/network/wan/routing/
framework/design/platform/storage/
framework/design/platform/storage/durability/
framework/design/platform/tenancy/
framework/design/platform/tenancy/hybrid/
framework/design/requirements/
framework/design/requirements/quality/
framework/design/transition/
framework/design/transition/brownfield/
framework/examples/
framework/examples/archive-service/
framework/examples/field-station/
framework/operations/
framework/operations/assurance/
framework/operations/assurance/exercises/
framework/operations/continuity/
framework/operations/continuity/backup/
framework/operations/continuity/backup/integrity/
framework/operations/continuity/recovery/
framework/operations/continuity/recovery/failback/
framework/operations/economics/
framework/operations/economics/allocation/
framework/operations/economics/sustainability/
framework/operations/inventory/
framework/operations/inventory/discovery/
framework/operations/observability/
framework/operations/observability/pipeline/
framework/operations/planning/
framework/operations/planning/capacity/
framework/operations/planning/quotas/
framework/operations/reliability/
framework/operations/reliability/objectives/
framework/operations/response/
framework/operations/response/on-call/
framework/operations/service-management/
framework/operations/service-management/catalog/
framework/profiles/
framework/profiles/compute/
framework/profiles/compute/hpc/
framework/profiles/compute/hpc/accelerators/
framework/profiles/industrial/
framework/profiles/industrial/ot/
framework/profiles/regulated/
framework/profiles/regulated/residency/
framework/profiles/remote/
framework/profiles/remote/edge/
framework/profiles/remote/edge/disconnected/
framework/profiles/restricted/
framework/profiles/restricted/air-gap/
framework/profiles/restricted/air-gap/transfer/
framework/profiles/shared/
framework/profiles/shared/multitenant/
framework/profiles/small-project/
framework/profiles/small-project/single-site/
framework/records/
framework/records/assurance/
framework/records/assurance/exercises/
framework/records/delivery/
framework/records/design/
framework/records/design/interfaces/
framework/records/governance/
framework/records/intake/
framework/records/operations/
framework/records/planning/
framework/reference/
~~~

## New files

Each link is relative to this root. SHA-256 covers the exact bytes written to disk, including line endings. The inventory lists itself without a digest to avoid a circular hash.

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| [environment-definitions/development/access-policy-definitions/GUIDE.md](environment-definitions/development/access-policy-definitions/GUIDE.md) | 1290 | 557354E2CDE9CC986E942A11225752D43C4D230EDEE53B3CF574820C10645784 |
| [environment-definitions/development/network-policy-definitions/GUIDE.md](environment-definitions/development/network-policy-definitions/GUIDE.md) | 1299 | 32CAC053844D1491B61BDDE98271B9D28AA249E05CF18583BB76FA44A85BAB98 |
| [environment-definitions/development/resource-definitions/GUIDE.md](environment-definitions/development/resource-definitions/GUIDE.md) | 1276 | ED7618A9243F289CAC31C95AA06AE33927F57791C5C2C7DAFF46AF5BDB0EE7D9 |
| [environment-definitions/disaster-recovery/access-policy-definitions/GUIDE.md](environment-definitions/disaster-recovery/access-policy-definitions/GUIDE.md) | 1389 | 031428D3C5B9D7721A25C321187C33B1953B9EF1A435D363FCBCA9DC6B590436 |
| [environment-definitions/disaster-recovery/network-policy-definitions/GUIDE.md](environment-definitions/disaster-recovery/network-policy-definitions/GUIDE.md) | 1335 | 3E82A9C05BEED962274BD836D1068782856E1CAF74161E27E4284AADD7EA3089 |
| [environment-definitions/disaster-recovery/resource-definitions/GUIDE.md](environment-definitions/disaster-recovery/resource-definitions/GUIDE.md) | 1374 | BB2E0827779638675D4C4CA1E7177B90373325EF3CC08D08E9F15564A3C8D0EA |
| [environment-definitions/production/access-policy-definitions/GUIDE.md](environment-definitions/production/access-policy-definitions/GUIDE.md) | 1395 | 0C79506775F212A6C586E5E11A2F3FE57C615E828556049EFBE01D5419183E1B |
| [environment-definitions/production/network-policy-definitions/GUIDE.md](environment-definitions/production/network-policy-definitions/GUIDE.md) | 1323 | 6CEC2B05F91741B23CA8B20B3226ABB4D85455F7363D5D52F33C02082B0CB436 |
| [environment-definitions/production/resource-definitions/GUIDE.md](environment-definitions/production/resource-definitions/GUIDE.md) | 1339 | 7C6FADE806210FB5C3F10EBC213E2E13984D08D4A6E9C91F28FA36141D0A66EF |
| [environment-definitions/staging/access-policy-definitions/GUIDE.md](environment-definitions/staging/access-policy-definitions/GUIDE.md) | 1337 | CDE0C9A348C58D77F66542F8D2237772E250198D4C6DCE6A5498E927EDC3A6CF |
| [environment-definitions/staging/network-policy-definitions/GUIDE.md](environment-definitions/staging/network-policy-definitions/GUIDE.md) | 1257 | A25400E1C2D67EA4919FAB52F9252F308AB47F589E77A0EFA793FF1747BBD30A |
| [environment-definitions/staging/resource-definitions/GUIDE.md](environment-definitions/staging/resource-definitions/GUIDE.md) | 1272 | 9AAFCCD806D63548162B71FE03BEE5019DB5F9613E1C5E0ED2346FBE828D32F5 |
| [environment-definitions/testing/access-policy-definitions/GUIDE.md](environment-definitions/testing/access-policy-definitions/GUIDE.md) | 1289 | 4DD8C0A37549C17DE0CE4A7DE020610215C5777010838199B79B56CEA1BB14BD |
| [environment-definitions/testing/network-policy-definitions/GUIDE.md](environment-definitions/testing/network-policy-definitions/GUIDE.md) | 1297 | C6BC3E315BE72FF1DEE1BFD3ACA5ED561DC446F7DC1A62E51193DC01838C3F1E |
| [environment-definitions/testing/resource-definitions/GUIDE.md](environment-definitions/testing/resource-definitions/GUIDE.md) | 1243 | 162C723946FDA4923E67AC8B5C863E97607BF6494158E03B80E6DFE08A1C4109 |
| [framework/adoption/authoring/installation-record.md](framework/adoption/authoring/installation-record.md) | 3447 | D34949FB2A9E3689DB6DE2017C22B890B9A1B8BF733A3EC68252317F7A4E2FB2 |
| [framework/adoption/environments/promotion-matrix.md](framework/adoption/environments/promotion-matrix.md) | 2645 | FAFB8B544121C6FC845B86EF2C4AD5B51B6AEA3BB942878BD94F75935104182B |
| [framework/adoption/learning/first-walkthrough.md](framework/adoption/learning/first-walkthrough.md) | 1745 | 3F084CAB3D20833264226325CB5AA3052A560AD0B8AA31F6B12CB839EEDBFBF2 |
| [framework/adoption/learning/windows/read-only-path-check.md](framework/adoption/learning/windows/read-only-path-check.md) | 2130 | 4C093D0A91E20EABD43CFE123F7BBFE5982F514569449BE6DC586D8AA0F6ADE1 |
| [framework/adoption/lifecycle/stage-gates.md](framework/adoption/lifecycle/stage-gates.md) | 2038 | A17D1A25064F41B02B1DD59367F340A62AC16FC6C8866CA54954107AD549D0B0 |
| [framework/controls/cryptography/rotation/keys-and-secrets.txt](framework/controls/cryptography/rotation/keys-and-secrets.txt) | 1983 | 4BD1E63147CABF7CFD4DD6BAEA05B3F885DA630150269C7E0B6295905AECFB84 |
| [framework/controls/delivery/automation/reconciliation.md](framework/controls/delivery/automation/reconciliation.md) | 2095 | 80EB47E95F9E04899BB61CC0BBEFD90BE6354AAD9D5FEA3EFD0E4ECA069D20AC |
| [framework/controls/delivery/promotion/canary-and-recovery.txt](framework/controls/delivery/promotion/canary-and-recovery.txt) | 1928 | 0951056CE37AD49D4DD829ECBB233C176D2CC6B9912BC615572E45A0A6E0C31E |
| [framework/controls/delivery/state/module-state-and-drift.txt](framework/controls/delivery/state/module-state-and-drift.txt) | 2066 | 8E8F1FD4C50711BCACAD0B8052E1DEAB8D5CD6B201293F1708853C0626DE5337 |
| [framework/controls/governance/exceptions/risk-and-evidence.txt](framework/controls/governance/exceptions/risk-and-evidence.txt) | 1955 | DA383DF048984DA0468FEAA17738BFE8D8A99937E0B7957C4C9DE3634D96867B |
| [framework/controls/governance/suppliers/exit-and-support.md](framework/controls/governance/suppliers/exit-and-support.md) | 1817 | 01FD44FC07F91AF0561A2CF8188D0F4641910B68DF41466FCB3420AB72E5751F |
| [framework/controls/identity/tenancy/access-boundaries.txt](framework/controls/identity/tenancy/access-boundaries.txt) | 1884 | A2C80E754D176386A9C15D7769860098C3E440AAC5CE6E98738F2B1AE244B816 |
| [framework/controls/lifecycle/retirement/sanitization-and-closure.txt](framework/controls/lifecycle/retirement/sanitization-and-closure.txt) | 2022 | 839B0B347E757CADC38E29843A071B5D79E23B3E21E2739820EA4CFE0836E3D5 |
| [framework/controls/security/design/threat-model.md](framework/controls/security/design/threat-model.md) | 2071 | 53A26352065E1E66D849D9AE7A520F533A546A15BE351F0EF66A6E5E033AF1DD |
| [framework/controls/security/hardening/patch-lifecycle.md](framework/controls/security/hardening/patch-lifecycle.md) | 1829 | 3B15961B9CC9CFC95E3181B380B11F2185AF1AAE199060F85692E152CC55D39D |
| [framework/controls/supply-chain/verification/artifact-provenance.txt](framework/controls/supply-chain/verification/artifact-provenance.txt) | 2047 | ADA03F789DBA179CA7AE2EBD37452A6151787DBB100B7DE8B6A6A9D7B4616683 |
| [framework/design/boundaries/ownership/service-map.md](framework/design/boundaries/ownership/service-map.md) | 1718 | 4910FACEBB933C68D16C51680F74736FC13DA9B5C13844F2B4B2C5B169DBD0CE |
| [framework/design/composition/bindings/environment-assembly.md](framework/design/composition/bindings/environment-assembly.md) | 2406 | E2D5D7586D21F3225BCCC7061A8539F4EFACEB1BCA38B255FE5A7A30EBF5C210 |
| [framework/design/composition/contracts/module-interface.md](framework/design/composition/contracts/module-interface.md) | 2340 | A06F87BC332C817B8E35B3FB166EB7B8E5CA1310F3CFC871311E0AAD1617BCE3 |
| [framework/design/decisions/topology/failure-domains.md](framework/design/decisions/topology/failure-domains.md) | 1696 | B9321841723FEED13F44B7301FBEB458A186992D7AB9E19FFEBE835547B8DE2F |
| [framework/design/platform/compute/bootstrap/bare-metal-bootstrap.md](framework/design/platform/compute/bootstrap/bare-metal-bootstrap.md) | 1833 | F2743B49905CBCE37967AF88B26799921A40E8FB66ACD625626415095F71891E |
| [framework/design/platform/compute/placement/compute-placement.md](framework/design/platform/compute/placement/compute-placement.md) | 1855 | 879F12D686543A8DF39598A5EE9F0C703B61CED5E0A6AC6F378434C01BCB9DFC |
| [framework/design/platform/compute/scheduling/control-plane.md](framework/design/platform/compute/scheduling/control-plane.md) | 1792 | DAA88AE7D5274EB980FAF94A48B067CBB8AC6D322B3BDFA97616EFD1FDA2620F |
| [framework/design/platform/data/cache/invalidation.md](framework/design/platform/data/cache/invalidation.md) | 1745 | 1CF112B6EC16C5CBA22EAE173B7B887D390144AC2495642C161C5A37CBAF3292 |
| [framework/design/platform/data/replication/partition-and-fencing.md](framework/design/platform/data/replication/partition-and-fencing.md) | 2015 | 82754DFB7E565232066CDF5595C1F5014C5356467D18F2CC4595EC8858F35C63 |
| [framework/design/platform/facilities/power/facility-power-and-cooling.md](framework/design/platform/facilities/power/facility-power-and-cooling.md) | 1801 | 23BCEA1DE5A06D46B9FADC43A3020E4538BAED584E453A740E3078DE4D08D1E1 |
| [framework/design/platform/network/addressing/segmented-connectivity-and-ipam.md](framework/design/platform/network/addressing/segmented-connectivity-and-ipam.md) | 1885 | 008454DB929C1FDEA74328A4390992E2332011358E6F9CDD15EA81A493E2C144 |
| [framework/design/platform/network/naming/trust/dns-time-and-pki.md](framework/design/platform/network/naming/trust/dns-time-and-pki.md) | 1866 | C23BCF224381FFD0E23772BC7EF9D2D493E2211F79D41F1761BC3E6817741C15 |
| [framework/design/platform/network/traffic/ingress-egress.md](framework/design/platform/network/traffic/ingress-egress.md) | 1741 | EBC72B560E46AB7E668B450A36CAC68A34FCD611298368F5D7AEBFC640630F02 |
| [framework/design/platform/network/wan/routing/wan-routing-and-dual-stack.md](framework/design/platform/network/wan/routing/wan-routing-and-dual-stack.md) | 1794 | 47059812538C2702B8910B73805901298648B61598DFB4A7EFCA599AF876CC88 |
| [framework/design/platform/storage/durability/storage-durability-and-rebuild.md](framework/design/platform/storage/durability/storage-durability-and-rebuild.md) | 1845 | A7AB53A4C8577E13372F2D735C98EA7D6653AFEF1CA3E101982F4929F86896FC |
| [framework/design/platform/tenancy/hybrid/hybrid-tenancy-and-landing-zones.md](framework/design/platform/tenancy/hybrid/hybrid-tenancy-and-landing-zones.md) | 1893 | 8847F3CB0E1C87B738D7C785118BB052FAAABED5320EB7A7E336684F8665FC33 |
| [framework/design/requirements/quality/targets.md](framework/design/requirements/quality/targets.md) | 1723 | 649C50FDFD6B94AB5732C8A6C4D1A2CC421ACEA21FFEE988B03807A1C560C162 |
| [framework/design/transition/brownfield/coexistence.md](framework/design/transition/brownfield/coexistence.md) | 1731 | 4091BCCAE1090B1B0676C96DD55B9FD702B66462EDB1BF625E67C8E0E2CC7EC5 |
| [framework/examples/archive-service/from-request-to-handover.md](framework/examples/archive-service/from-request-to-handover.md) | 3971 | 785A4221BEF463CFC24777900F899F2554E5AA145D56FC5BFAB7E34898D5418C |
| [framework/examples/field-station/design-to-commissioning.md](framework/examples/field-station/design-to-commissioning.md) | 2877 | B5A34D443B4E803B3D15BFC337F202ABEF9A0680C6E756C0B33A8B85744791F9 |
| [framework/operations/assurance/exercises/failure-exercises.md](framework/operations/assurance/exercises/failure-exercises.md) | 1519 | 614793995FB2F30DAAC8A3946DF780A28C3C2FB178886EBCD6479F671B617329 |
| [framework/operations/continuity/backup/integrity/backup-integrity.md](framework/operations/continuity/backup/integrity/backup-integrity.md) | 1737 | 6329795CC3FAC6EA027E766E335AB4703ACA251B431EFB4A97E8C62F51F22F5E |
| [framework/operations/continuity/recovery/failback/recovery-and-failback.md](framework/operations/continuity/recovery/failback/recovery-and-failback.md) | 1659 | EC3FA76EE70A0A4649C3402F5F8B19D75A03209F444BAA68CDAC406C4A66E90E |
| [framework/operations/economics/allocation/unit-cost.md](framework/operations/economics/allocation/unit-cost.md) | 1810 | 23B87083DA2759714929D7E72977974902827460545EE74819A0C830BF98F114 |
| [framework/operations/economics/sustainability/energy-and-utilization.md](framework/operations/economics/sustainability/energy-and-utilization.md) | 1828 | 47C679B0A9E088E6FCDF25D1E95ADEF8CCF6D759252BB861A2535F19D140F3A2 |
| [framework/operations/inventory/discovery/asset-reconciliation.md](framework/operations/inventory/discovery/asset-reconciliation.md) | 1964 | E8ABCBD6884A7BA76A4D53A7B74F8410B3EA5FD7BA6E4E89CAF4ECC7D5C7A70A |
| [framework/operations/observability/pipeline/telemetry-pipeline.md](framework/operations/observability/pipeline/telemetry-pipeline.md) | 1611 | 8E613C8C230E98FA284DBBB2C1A8C1031799C3746AC7203235F06408BB55930B |
| [framework/operations/planning/capacity/capacity-performance-and-cost.md](framework/operations/planning/capacity/capacity-performance-and-cost.md) | 1846 | 70607E11F2313F26AE4F4F6FD671993220C49632DBE735325E70CBEAC30D5037 |
| [framework/operations/planning/quotas/exhaustion.md](framework/operations/planning/quotas/exhaustion.md) | 1716 | 67D86AAFDC9D841B7C63A5D332210E089D51FCECE3E9B448D9ABB7E4B1AA7680 |
| [framework/operations/reliability/objectives/service-objectives.md](framework/operations/reliability/objectives/service-objectives.md) | 1512 | FE03FE2DA4B16EE8148DA0F9629EE26FBE3BDD93F46C0DE836823F2BD42C2371 |
| [framework/operations/response/on-call/incident-command.md](framework/operations/response/on-call/incident-command.md) | 1643 | 5A5CD857453CAB57532DF37B2858276EEAC264E439C30F7A6628AA8D0B3D417F |
| [framework/operations/service-management/catalog/operating-model.md](framework/operations/service-management/catalog/operating-model.md) | 2029 | 9BAD8218DD06958EF63AE235B0A1B63967B1D3CEC49FEA417A12ECA5DB929252 |
| [framework/profiles/compute/hpc/accelerators/gpu-cluster.md](framework/profiles/compute/hpc/accelerators/gpu-cluster.md) | 1831 | 0BC33E798F1259F0340F1412BE70AD8B1CF01F1B3DF6B28A6B89E9F33F6B7E85 |
| [framework/profiles/industrial/ot/site-maintenance.md](framework/profiles/industrial/ot/site-maintenance.md) | 1929 | 4A8EB6ADC78BE900D9BFCD4ED6E34555B175FCB244D2EAB8ED6B5768CC0DD6FC |
| [framework/profiles/regulated/residency/data-paths.md](framework/profiles/regulated/residency/data-paths.md) | 1796 | 939C9DE856A2BF3FA6AB9C87EBD4A0449CCFC8C779DDAF8566C4189C0AE01643 |
| [framework/profiles/remote/edge/disconnected/store-and-forward.md](framework/profiles/remote/edge/disconnected/store-and-forward.md) | 1806 | 701C35AEB68DE591BE699CE41E59DD79D6BCD454F31E5E193D602F32ACB22680 |
| [framework/profiles/restricted/air-gap/transfer/trust-bundle.md](framework/profiles/restricted/air-gap/transfer/trust-bundle.md) | 1853 | 4E42191B65CE254270A30DB0BDCC30A8441B28BF9B01519FFDD495D9310326FB |
| [framework/profiles/shared/multitenant/noisy-neighbor.md](framework/profiles/shared/multitenant/noisy-neighbor.md) | 1733 | F105D000095E51783B086934D9E4AD19F364F36E64870647EA85E642337C1D5C |
| [framework/profiles/small-project/single-site/minimum-footprint.md](framework/profiles/small-project/single-site/minimum-footprint.md) | 1680 | 32FCBB1922FFAA3B27AD1022FF5545677B78ED56FBC12264F732AC9879598D03 |
| [framework/records/assurance/exercises/recovery-trial.md](framework/records/assurance/exercises/recovery-trial.md) | 1835 | 55D635C33FD4FD79EC5E120358A87A2F0F624175B471992371F1849D62CCA13E |
| [framework/records/assurance/readiness.md](framework/records/assurance/readiness.md) | 1833 | 9B0656F9E5AADFF71FA305BA294D15BAE0719BC0E255D89EC6010A1F526426F6 |
| [framework/records/delivery/change-packet.md](framework/records/delivery/change-packet.md) | 1808 | BF7D7058E80ABC878220D0891749C55151157B61295725142FFD33D456E03840 |
| [framework/records/design/decision.md](framework/records/design/decision.md) | 1874 | 354D940EC6FA3C925E6AFF05DF6A390EA338F875B73CDA3296762AEAAF7BDB32 |
| [framework/records/design/interfaces/dependency-register.md](framework/records/design/interfaces/dependency-register.md) | 1706 | F7DC9835E721A9A2F78E071F125A4EEC3B5AAC586EE2B3986E2C490D91274D35 |
| [framework/records/governance/risk-and-exception.md](framework/records/governance/risk-and-exception.md) | 1594 | C4D74A7080C9A76A309E050237E8B3162B275BB3EAB42BA718F0044AB3F0C550 |
| [framework/records/intake/project-brief.md](framework/records/intake/project-brief.md) | 2076 | D8AAC51CFF4DB2C1647BF053C0E142AA4B950EB21E6C96CBC0E19F926C9762DB |
| [framework/records/operations/service-record.md](framework/records/operations/service-record.md) | 1869 | 93342E040D7EB38B014C194FB2B6150319BBD437717556C5F2A74D843E99EDD9 |
| [framework/records/planning/capacity-model.md](framework/records/planning/capacity-model.md) | 1716 | FBD4EAA3A677EA22E5C7CAC8BDE9C5AAC962E48E06F314FB3DBD78A18E4EA49D |
| [framework/reference/catalog.md](framework/reference/catalog.md) | 11167 | D4FB7BF23B86882ACF1AE93F995C3D924A6B7433EB39C5B95EFCC260402967B8 |
| [framework/reference/framework-crosswalk.md](framework/reference/framework-crosswalk.md) | 4270 | D2DC1A6817B6867805269E75B822E29080A46484C041B58174B991F8D255FC77 |
| [framework/reference/terms.md](framework/reference/terms.md) | 2297 | 3EE430627CF981CFB883AE23724C3C239743FFB740A09F4EB406D697BB6A2EC8 |
| [framework/START-HERE.md](framework/START-HERE.md) | 2295 | D393ACE32E1255616F43277E0528191DF12F5BF2C9C4CA3D7B8666885C93DCE6 |
| [modules/artifact-storage/CAPABILITY.md](modules/artifact-storage/CAPABILITY.md) | 1702 | 5F9F88B209D0EC2DDA3BF1C2686623C9769CF994EF5E82D3A03D1A2177980D55 |
| [modules/build-agents/CAPABILITY.md](modules/build-agents/CAPABILITY.md) | 1623 | 8D19BA3B90F9895264660ACB05E433C2784D779A07ACB10D20CC1ACE7916F696 |
| [modules/compute/CAPABILITY.md](modules/compute/CAPABILITY.md) | 1590 | 6A3EBB270A0ACDF1E94C6F051A4F166ACB89850C0964A1C7285F2C388F9CED9B |
| [modules/databases/CAPABILITY.md](modules/databases/CAPABILITY.md) | 1748 | 7EA349C7BE9F9CCC6C34EA96F11275124715196B2ED3F460AA0D21EACB554DC2 |
| [modules/identity/CAPABILITY.md](modules/identity/CAPABILITY.md) | 1656 | 65560C58BFCAA8E30E8D1A3A3E4C569EA820012CC7D0C860B24F93B2F4EC95BE |
| [modules/messaging/CAPABILITY.md](modules/messaging/CAPABILITY.md) | 1641 | 30DC3E5F128A268E64C5CBE9C68852737A8B76E7A7EA2DB4209095D134EDC641 |
| [modules/networking/CAPABILITY.md](modules/networking/CAPABILITY.md) | 1621 | DEC8EA94D3AE2BDCDFED4CF854AD1238AA9B31301D56E61207DF4E64A9D2A63F |
| [modules/observability/CAPABILITY.md](modules/observability/CAPABILITY.md) | 1602 | 4487595EC28B488BCED0FC0AFA95AD635EBD7C452ABE33E648F8506295C936D8 |
| [modules/recovery/CAPABILITY.md](modules/recovery/CAPABILITY.md) | 1728 | D01521D2DA6A289657FC32277120D96BC14670D00657AF9D163A81EFFEF29004 |
| [modules/storage/CAPABILITY.md](modules/storage/CAPABILITY.md) | 1686 | A5B5CF3080DFEC5934DB1D3469271506E6D0D5A886E7560FC2CC13BB3DA52656 |
| [INFRASTRUCTURE-ADDITIONS.md](INFRASTRUCTURE-ADDITIONS.md) | Self | Self |
