# Establish scope and mission

Start by asking one user to describe what success looks like at the end of a working day. Name the system of interest so that a reader can tell whether it includes people, equipment, software, procedures or a combination. A context view should remain useful after an implementation change.

## Draw the boundary

1. Write the intended outcome, its beneficiary and an observable end state. A service can deliver a notice even if the recipient never acts on it. Choose the end state for which the project is accountable.
2. Inventory neighboring systems, users, support staff, maintainers, external authorities and operating conditions. Include the people who act only during failure or decommissioning.
3. Label each crossing with a verb, direction, information, material or energy, and the owners on both sides. Show who controls the interface and who bears the consequences of a late response.
4. Walk one normal case, one unavailable neighbor and one shutdown. Write a disputed responsibility next to its crossing and assign an owner to resolve it.

## Field example

A device records observations. An intake service makes them available to a duty operator. A separate authority approves physical intervention. Device capture, service receipt and operator acknowledgment are three different outcomes. If the network disappears, the network provider owns repair and the product team owns how delayed observations are stored and shown. The duty operator needs to distinguish a stale observation from a current hazard report.

For a manual service, follow a paper request from intake to authorized disposition. Mark when custody passes to the next person and what proves that transfer. For a physical product, repeat the walk for installation, maintenance access and stored energy.

## Review challenge

Hand the diagram to someone outside the design team. Give them an old observation and ask who currently owns it, how its age is known and who can act. The diagram and its linked contracts should answer all three. Record any external assumption the team cannot verify and the conditions under which it would change the design. Continue with [operating modes and authority](operating-environment/modes-and-authority.md).

[Architecture field guide](../../framework/README.md)
