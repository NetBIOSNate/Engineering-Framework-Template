# Design segmented connectivity and address allocation

Start with a flow inventory. Give each environment, tenant and management plane an owner. For every permitted path, identify initiating workload identity, source segment, destination service, name resolution path, protocol, port, address family and reason. Include backup, update and certificate renewal traffic alongside user requests.

## Implement the plan

1. Check the IP address management (IPAM) register for overlap with existing sites, partners and expected acquisitions. Allocate contiguous growth space by routing boundary. Reserve addresses needed for load balancers, managed interfaces, replacement nodes and disaster recovery. Record owner, purpose, permitted advertisement, lifecycle and reclaim date for each prefix.
2. Place traffic that requires distinct trust or failure boundaries into separate routing or policy domains. Choose firewall enforcement points with an identifiable return path. Specify the behavior of established sessions during failover and which workloads may initiate outbound sessions.
3. Reserve independent capacity for emergency management. Establish policy parity for IPv4 and IPv6 where both are enabled. Capture rule counters and flow evidence at the points that decide access.

## Demonstrate isolation

Use representative clients in each segment. Prove each approved path reaches the expected authenticated endpoint, then prove an unapproved tenant or destination is denied by the intended control. Validate DNS resolution separately so a missing record cannot masquerade as successful isolation. Repeat in both address families and during gateway failover. A full subnet can stop replacement nodes during a rollout. Compare free addresses with maximum surge, evacuation demand and growth before signing off. Attach the prefix ledger, flow matrix and test timestamps to the change.
