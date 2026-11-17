# Make system state observable and operable

Choose the questions an operator must answer before deciding to continue, stop, retry or recover. Start with user outcomes, then identify the signals that distinguish likely causes. A count of live processes can remain high while the system silently drops accepted work.

| Operator question | Candidate observation | Architectural requirement |
| --- | --- | --- |
| Can users complete the outcome? | Successes and failures by operation and bounded cohort | Define the start, completion and timeout boundaries |
| Is data current? | Age of oldest pending record and time of last valid observation | Identify trusted clocks and uncertainty during disconnection |
| Is the service losing or repeating work? | Reconciliation of stable identities and downstream effects | Share correlation identity across boundaries with appropriate access |
| Can we recover before a limit? | Remaining space, net growth and measured drain rate | Expose capacity, policy and recovery owner |
| Is the evidence itself stale? | Last successful signal collection and monitor health | Provide an independent or local indicator where loss matters |

## Design an operator action

For each severe condition specify what a person sees, which action they are authorized to take, what the action commits and how they can verify the result. Include failed or partial completion and shift handover. Use bounded diagnostic fields with explicit retention and access. High-cardinality identifiers can be useful in restricted traces while creating excessive metric cost or unnecessary disclosure in aggregate systems.

An alert for “queue depth above 5,000” may page during a healthy scheduled batch and miss a small queue whose oldest item is days old. Pair age and drain trend with the user impact, affected population and next safe action. Test the alert with an operator who did not write the design.

Measure operator time from noticing degradation through restoring useful service. Restore monitoring after a simulated signal failure and identify the period of uncertainty. Provide a local cue when the central console or credentials are part of the failure under investigation. Record the selected signals alongside the [recovery sequence](../resilience/failure-domains-and-recovery.md) and [human control design](../human-factors/accessibility-and-control.md).

[Architecture field guide](../../README.md)
