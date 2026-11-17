# Choose topology against a failure model

Pick the failure you promise to survive. Identify correlated risks such as a bad policy release, expired certificate and replicated logical deletion.

| Option | When to consider it | Evidence to request |
| --- | --- | --- |
| Single site with independent recovery copies | A measured rebuild fits the downtime allowance. | Recovery from clean access with consumer validation. |
| Multiple zones | Service must continue through localized power or host loss. | Surviving capacity, zone-aware quorum, route convergence and working keys. |
| Active site plus standby | Location loss matters and promotion fits the interruption budget. | Reserved capacity, data lag, fencing and measured failback. |
| Multiple active sites | Users require local service or very short interruption. | Conflict semantics, partition behavior and tested loss of intersite coordination. |

For a three-voter consensus group, two voters must communicate to form a majority. Placing two in the same rack lets a single rack failure stop progress. A witness at a third site may help quorum while adding a WAN dependency. A witness may hold no recoverable copy of the data. Verify voting and persistence rules separately.

Draw a line through a site and forbid all calls into it, including control-plane calls. Estimate demand and quotas on survivors, trace a new write, and show how the old writer is fenced. Repeat for a global credential compromise. Document which scenario the topology covers, which needs a restore, recurring cost and the condition that justifies changing topology. Capture the result in a [decision record](../../../records/design/decision.md).
