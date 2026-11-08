# Turn quality goals into measurable scenarios

“Fast,” “secure” and “easy to maintain” cannot distinguish two candidate designs. Choose an event that matters to somebody. Describe the state the system must preserve, and agree where and how someone could measure success.

## Build the scenario

1. Name the source of the stimulus, such as an operator, an adjacent subsystem, the environment, a maintainer or an attacker.
2. State the stimulus and the system element it affects. Separate an action from its observed consequence.
3. Specify the operating environment, including peak load, outage, maintenance, degraded staffing or a mixed-version rollout.
4. Describe the observable response. Include what a person can learn when completion is uncertain.
5. Give the response measure a unit, population, measurement points and time window. Separate allowable loss, timeliness and recovery. Name the person authorized to negotiate the threshold.

| Quality concern | Example scenario | What to check |
| --- | --- | --- |
| Modifiability | A second supplier changes measurement units mid-product-life | Adapter and contract fixtures absorb the change. Count every other module or procedure touched |
| Availability | A worker stops immediately after a durable receipt | Reissue the request. Check the caller can discover the outcome and the action occurs once |
| Usability | An operator taking over mid-incident encounters an old reading | Observe whether they can identify its age and choose the documented response without coaching |
| Performance | A contracted cohort submits at peak for 15 minutes | Measure successful end-to-end duration from submission to durable acknowledgment. Report failures and timeouts separately |

## Select the design drivers

Ask stakeholders to rank business impact and implementation uncertainty separately. Plot the scenarios in those two dimensions and start with high impact and high uncertainty. A hard physical constraint removes an option regardless of the rest of its score. Keep one scenario that challenges the preferred design and one involving a user who is usually missing from design reviews.

Attach a baseline measurement or explicitly label an estimate. Record what would invalidate the evidence, such as smaller test records, missing encryption overhead or different ambient temperature. End with an owner for every unresolved threshold and carry the selected scenarios into the [tradeoff review](../03-evaluate/tradeoff-review.md).

[Architecture field guide](../../README.md)
