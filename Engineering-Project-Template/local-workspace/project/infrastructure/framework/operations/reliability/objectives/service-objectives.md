# Service objectives and alerting

**Goal.** Translate infrastructure behavior into a promise a consumer can measure. Start with one dependency, one user journey and one owner who can decide how much service risk to accept.

1. Define what counts as an eligible event, a good event and the rolling measurement window. For a resolver, a good lookup returns the expected response within an agreed latency. Include valid negative responses according to the contract. Record how timed-out attempts enter the denominator. Keep synthetic and production traffic distinguishable.
2. Calculate the budget. At a 99.9% target across 2,000,000 eligible lookups, 2,000 bad events consume the budget. A 1% observed bad fraction burns it at ten times the sustainable rate. Set paging windows around the time the team needs to intervene and the amount of budget it can spend. Document which slower conditions create work during staffed hours.
3. Replay a short spike, a sustained outage and a quiet interval. Verify the fast and slow rules fire as designed, the page reaches someone with authority to act, and the alert clears after recovery. Add an independent probe for low-traffic paths and detect missing telemetry explicitly.

**Review evidence.** Keep the event query, denominator exclusions, traffic sample size, paging test and error-budget response together. Revisit the objective when consumers, traffic mix or failure consequences change. [Google SRE Workbook](https://sre.google/workbook/alerting-on-slos/)
