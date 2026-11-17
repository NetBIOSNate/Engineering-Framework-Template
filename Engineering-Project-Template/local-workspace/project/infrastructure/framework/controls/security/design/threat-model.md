# Threat-model an infrastructure change

## Start at the control that could cause the most harm

Choose a durable asset, privileged action or availability boundary. Draw the source of the request, identity issuer, policy decision, target, data store, audit destination and recovery authority. Mark where ownership or trust changes. Ask an operator how each box can be bypassed, misconfigured or made unavailable.

| Scenario | Prevent or contain | Detect and recover |
| --- | --- | --- |
| A compromised build job changes production routes | Bind untrusted previews to a separate pool and scope deployment rights to an approved target. | Alert on route changes from an unexpected identity. Use independent console access to restore an approved route. |
| A backup administrator deletes both live and retained data | Separate recovery custody and verify the retention boundary under the modeled administrator compromise. | Detect attempted deletion outside normal policy, restore through independent access and verify content. |
| A noisy tenant exhausts a shared endpoint | Enforce tenant-aware concurrency limits before work consumes the scarce resource. | Observe admitted and rejected work by tenant and verify another tenant's consumer probe during a burst. |
| A stale trust anchor blocks site bootstrap | Define trust-bundle replacement, a verified offline copy and a custodian who can install it. | Reboot a spare with empty caches, validate the recovered identity and inspect the audit trail. |

## Turn the model into work

For each scenario, identify the preconditions, reachable assets, consequence and observable evidence. Prioritize paths one actor or one release can use to cross several failure boundaries. Assign both a control owner and a person who will independently run the negative test. Preserve the remaining exposure and revisit the model when a credential authority, network boundary, supplier or recovery dependency changes. See the [exception record](../../../records/governance/risk-and-exception.md) for unresolved findings.
