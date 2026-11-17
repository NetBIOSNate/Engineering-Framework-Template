# Power, cooling and physical failure domains

Produce a rack elevation and a dependency drawing that an on-site operator can trace from a service to its power feeds, cooling plant, access switch and cabling. Two sockets can share one upstream breaker. Two carriers can share the same entrance conduit. Get the facilities owner's confirmation for each claimed independent path.

## Design and implement

1. Inventory installed and planned hardware, sustained draw, startup demand, airflow direction, rack units and weight. Record the circuit voltage, phase, power factor assumption and site-approved usable capacity. Have qualified facilities staff establish permitted loading and switching procedures.
2. Trace each dual-supply device through its power distribution units to the upstream feeds. Place critical replicas on different physical dependencies. For single-cord equipment, document the selected transfer mechanism or the interruption expected during maintenance.
3. Calculate surviving-feed load. An illustrative rack drawing 6 kW across A and B may put nearly 6 kW on the surviving feed. Include adjacent racks sharing the same upstream path, growth, cooling loss and battery runtime until generator pickup or controlled shutdown.
4. Label circuits, cross-connects and console ports at both ends. Record spare parts, supplier lead time and the people who can enter the facility outside office hours.

## Acceptance evidence

Obtain a site-approved exercise or equivalent commissioning evidence for the predicted loss. Correlate branch metering, inlet temperature, UPS event timestamps and service probes through the event. Record surviving capacity, shutdown order, restart surge and discrepancies against the drawing. Revisit the model when a rack, feed, carrier or cooling zone changes.
