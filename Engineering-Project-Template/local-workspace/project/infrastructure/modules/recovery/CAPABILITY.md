# Independent recovery capability

## Service goal

Restore the minimum usable service within its agreed interruption and loss limits using people, credentials and data that survive the modeled failure.

## Contract

List recovery scope, ordered dependencies, required key versions, alternate access, protected copies, capacity, RTO/RPO, promotion authority and the conditions for returning to normal service.

## Build and commission

1. Trace a recovery from a blank target through identity, network, time, keys, backup catalog, clean artifacts and data. Break bootstrap cycles before documenting the procedure.
2. Choose restore, warm standby or active replicas using measured rebuild time and data lag. Maintain at least one usable version beyond correlated deletion or corruption where that threat matters.
3. Preserve versioned, independently accessible instructions. Give a second operator the location of evidence and a method to reach recovery contacts during primary-site loss.

## Acceptance exercise

Disable access to the primary in a drill. Recover a timestamped sequence, validate consumer reads and a new write, and measure the recovery point and elapsed outage. Before failback, prove there is a unique writer, reconcile divergence and restore protection at the alternate site.

## Revisit the design

Recalculate recovery feasibility when data volume grows or access practices change. A successful backup job measures capture, while an isolated verified restore demonstrates usability.

Use the [project brief](../../framework/records/intake/project-brief.md) to record demand and the [service record](../../framework/records/operations/service-record.md) to hand the capability over.
