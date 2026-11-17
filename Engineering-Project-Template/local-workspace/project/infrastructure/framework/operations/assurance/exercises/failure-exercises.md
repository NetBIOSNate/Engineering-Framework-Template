# Failure exercises and game days

**Goal.** Establish what an infrastructure component does under a specified fault. Begin with a tabletop for authority and sequencing, then use a representative isolated environment to measure behavior.

1. Write a falsifiable hypothesis, the exact component and scope, baseline probe, injection method and observation period. Assign a controller, an observer and an operator with the ability to reverse the fault. Define an abort threshold and an independent way for the operator to see it. For physical control systems, use a simulator or approved bench with the site safety lead.
2. Exercise one mechanism at a time. To check resolver redundancy, isolate one test resolver and make both cached and previously unseen queries. To test monitoring blindness, stop the test exporter and verify an external heartbeat pages. To test loss of administrative identity, make the usual operator account unavailable in the lab and time the audited recovery route.
3. Record actual fault start, first symptom, alarm, corrective action and verified recovery. Stop on the agreed threshold or an unexplained integrity failure. Remove the injection, verify traffic and state, drain pending work and confirm redundancy is available again.

**Review evidence.** Keep probe data, reversal time, unexpected dependencies and residual uncertainty. Assign an owner and a replay date for each failed hypothesis. A passing single-node test leaves site-wide dependency loss as a separate experiment.
