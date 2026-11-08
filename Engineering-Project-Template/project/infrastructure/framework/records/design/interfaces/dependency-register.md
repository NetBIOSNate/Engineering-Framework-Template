# Dependency and flow register

## Enter one row for each interface

| Field | Record |
| --- | --- |
| Consumer and provider | [Stable service identifiers, business hours, primary and secondary owners.] |
| Function and phase | [What is consumed during normal operation, startup, upgrade, incident or restore?] |
| Request path | [Initiator, zone, identity, destination, port/protocol, DNS and trust anchor.] |
| Guarantees | [Availability window, sustained and burst limits, timeout, acknowledgement and consistency.] |
| Failure and fallback | [Consumer symptom, local behavior, duration tolerated, backpressure and operator action.] |
| Correlation | [Common control plane, power, network, operator, key custody or supplier.] |
| Probes | [One positive and one negative or degraded test, last result, sample and evidence ID.] |
| Change and exit | [Notification period, compatibility window, replacement path and data handback.] |

**Example.** A new compute node requires an image registry at startup. Existing nodes with that exact image cached may keep serving during a registry outage. A cold standby may be unable to launch. Record cache policy, signed mirror digest, secondary DNS and mirror ownership. Test this dependency with an empty node during a representative network restriction.

## Use the register

Trace a consumer request and a blank-site recovery. Add a row whenever a different owner, failure domain, custody boundary or operational phase appears. Ask each provider owner to acknowledge the row and identify any dependency you cannot directly test. When an incident crosses teams, use the dated probe and the named contact to decide where to investigate first.
