# Engineer a physical interface

At a physical boundary, list everything that crosses. A detachable instrument may exchange force, power, heat, signals, data and maintenance authority through the same connector. Assign an owner to each side and one person to resolve discrepancies in the interface definition.

## Define the mating conditions

| Aspect | Specify and verify |
| --- | --- |
| Mechanical | Datum, orientation, mounting sequence, tolerance, load, vibration and space for service tools |
| Electrical | Voltage range at the load, current profile, inrush, grounding, protection and powered/unpowered connection behavior |
| Thermal and environment | Allowed temperatures at the interface, heat rejection path, contamination and environmental assumptions |
| Signals and data | Pin assignment, levels, timing, units, version identification, behavior on open or short circuit |
| Maintenance | Keying, identification, isolation, replacement, calibration and restoration to service |

Use dimensioned drawings and an interface control record when a supplier or another discipline builds the mating part. Distinguish guaranteed limits from nominal values. Identify the datum and measurement method on both sides. A tolerance without a reference condition or datum leaves acceptance open to interpretation.

## A simple tolerance allocation

A fictional enclosure has a 50.0 ± 0.3 mm interior gap. An insert is 49.5 ± 0.2 mm wide. At the tightest allowed limits the gap is 49.7 mm and the insert is 49.7 mm. The design guarantees zero clearance. If assembly needs at least 0.2 mm, allocate a new dimension or change the assembly method. Also account for finish thickness, thermal expansion and measurement uncertainty when applicable. Statistical assembly yield needs process distributions and correlation evidence.

Inspect a fitted pair at the limits and review the measurement capability with manufacturing. Ask a technician to replace the part using the actual service envelope. Document who owns a revised interface, how existing stock is identified and which revisions may mate. Link the [physical allocation](../../../framework/concerns/physical-and-deployment/allocation-and-placement.md) and [hazard analysis](../../../framework/concerns/assurance/hazards-and-evidence.md) if a mis-mated assembly can produce harm.

[Architecture field guide](../../../framework/README.md)
