# Industrial infrastructure and maintenance windows

## Decision boundary

Loss of connectivity in a plant can interrupt visibility or physical control. Ask the responsible site engineer to identify safe operating states, process timing, interlocks, permissible diagnostic methods and local recovery authority. Preserve the distinction between the industrial control network, supervisory services and enterprise reporting.

## Apply the framework

1. Inventory controllers, operator stations, engineering workstations, firmware, spare hardware and support agreements using site-approved methods. Record which device clocks, network flows and environmental conditions the process requires. Capture known-good controller configuration and the tool versions needed to restore it.
2. Define zones and conduits for supervisory, control, vendor support and telemetry traffic. Time-bound vendor sessions and give on-site staff the means to terminate them. Keep the management path available through a failed enterprise uplink.
3. Rehearse network loss, logging backpressure and host restart on a simulator or representative spare. Agree on a stop authority, physical rollback procedure, last safe decision time and operator communication before scheduling field work.
4. For a field change, confirm the actual equipment revision and local process state. Check that the operator can see physical status independently of the software being changed. Restore or isolate a component according to the site's established procedure if the observation disagrees.

## Evidence

Retain the bench result, site-approved window, safe-state verification, tested spare image and the named custodian. An IT patch deadline, recovery objective or generic scanning procedure requires review against the process safety and availability constraints of that installation. [NIST SP 800-82 Rev. 3](https://csrc.nist.gov/pubs/sp/800/82/r3/final)
