# Analyze operating modes and authority

A system boundary tells you who participates. A mode table tells you whether the same participant is allowed to take the same action under different conditions. Build the table with an operator who has experienced a degraded shift. Distinguish normal, startup, degraded, maintenance, recovery and retirement where the rules actually differ.

| Mode | Entry evidence | Allowed action | Exit guard |
| --- | --- | --- | --- |
| Normal collection | Device commissioned and local record space available | Persist observation and forward when connected | Radio loss or high-water threshold |
| Disconnected | Link health indicates loss of service | Continue local capture within the agreed reserve | Confirm authenticated remote receipt before releasing local copies |
| Suspect identity | Enrollment revoked or continuity cannot be established | Quarantine submitted records and notify reviewer | Designated reviewer resolves identity and disposition |
| Maintenance | Authorized person takes local ownership | Run diagnostics under the maintenance operating envelope | Account for work, remove temporary privilege and verify readiness |

## Find authority gaps

Walk a shift handover while the system is in each mode. Identify who can enter it, who can issue a command, which command wins if two arrive at once, and how a person observes the actual physical or durable state. Treat loss of the operator's console separately from loss of the controlled equipment. A stale display or delayed acknowledgment can make a successful command appear to have failed.

Include transitions often omitted from a design sketch. Consider reset while maintenance is active, restoration of connectivity while an override remains in force, and a replacement operator without the previous person's credentials. Record emergency authority and its expiry where the need exists.

## Produce a reviewable record

Attach a state table to the [view record](../../../framework/worksheets/design/view-and-interface.md). For each forbidden transition identify the enforcing component or procedure and what happens when the request is rejected. Ask the domain owner to trace a realistic degraded transition and identify an observation independent of the command issuer. A reported “stop requested” and a verified stationary actuator are distinct states with different evidence needs.

[Architecture field guide](../../../framework/README.md)
