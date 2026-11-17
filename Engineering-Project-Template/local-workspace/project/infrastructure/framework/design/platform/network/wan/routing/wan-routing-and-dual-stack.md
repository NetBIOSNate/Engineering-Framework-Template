# WAN routing and dual-stack diagnosis

Document which organization owns each wide-area network circuit, autonomous system, advertised prefix, filtering policy and escalation route. Draw physical path and provider dependencies. A second circuit adds limited resilience when both routes depend on the same conduit, upstream device or change authority.

## Prepare routing changes

1. For Border Gateway Protocol (BGP) peering, agree with the peer on prefixes, address families, maximum route counts and permitted default routes. Install inbound and outbound prefix policy, set a preservation or withdrawal policy for each origin, and record which route should win under ordinary and degraded conditions.
2. Establish a read-only baseline at both ends. Capture adjacency state, received and advertised prefixes, next hop, forwarding table, interface errors and measured latency from a real source segment. Plan a bounded withdrawal test and a specific way to restore the prior routing policy.
3. Exercise one address family and one peer at a time in an approved test boundary. Check convergence time against tolerated interruption. Record path symmetry if a stateful middlebox depends on it.

## Find a partial outage

A dual-stack client may silently fall back to IPv4. Resolve A and AAAA records, force each address family separately and test the same endpoint with the same payload size. If a small connection succeeds but bulk transfer stalls, inspect path maximum transmission unit (MTU) and ICMPv6 Packet Too Big delivery. When a routing session is healthy but data fails, inspect actual forwarding, neighbor resolution, return routing and security policy. Preserve timestamps and affected prefixes for the carrier. [RFC 4890 on ICMPv6 filtering](https://www.rfc-editor.org/info/rfc4890/)
