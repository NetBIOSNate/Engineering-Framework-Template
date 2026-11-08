# Run a scenario-based tradeoff review

Convene a review when plausible approaches exist and a consequential choice is still open. Bring the sponsor or delegate, design owner, someone who will implement or maintain the system and someone who experiences failure. Share the mission, constraints, views, competing options and ranked quality scenarios before the discussion.

## Work the decision

1. Restate the decision and identify constraints that disqualify an option. Separate negotiated targets from physical or contractual limits.
2. Walk the highest-impact scenario through each option. Stop at the first unsupported assumption. Record the specific dependency, failure mechanism and consequence.
3. Find sensitivity points, where a small parameter change matters. A buffer's time coverage halves if its input rate doubles. Find tradeoff points, where improving one concern changes another. Longer deduplication retention covers delayed retries while increasing storage and exposure.
4. Seek an adversarial example. Ask for a late acknowledgment, a restart while state is being moved, maintenance during peak load, or withdrawal of a supplier service.
5. Disposition each finding. Choose an option, bound a reversible trial, request evidence by a decision date, or take the risk to someone with authority to accept it.

| Review entry | Illustrative result |
| --- | --- |
| Decision | Buffer at each field device or one site gateway |
| Sensitivity | Device write endurance under the actual commit pattern |
| Tradeoff | Local buffering covers loss of the first radio hop and adds device lifecycle cost |
| Unknown | Usable capacity after formatting, journal overhead and wear reserve |
| Follow-up | Device lead measures formatted headroom and power-cut recovery on the candidate medium before procurement |

Document the strongest rejected alternative and what evidence would make it win. A numerical score is useful only if its scales and weights reflect stakeholder preferences. Do not average away an unmet release constraint. If probabilities are speculative, compare break-even values and show the range in which the decision holds.

Close with owners, dates, residual risk and linked [decision records](../../../decisions/records/options-and-consequences.md). The [review worksheet](../../worksheets/assurance/scenario-and-review.md) distinguishes predictions from observations. This session draws on QAW and ATAM concepts. A project commissioning a formal evaluation should specify the evaluation method and participants independently.

[Architecture field guide](../../README.md)
