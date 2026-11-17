# Operational readiness and release decision

## Identify the candidate

Service [ ], environment [ ], cohort [ ], exact source revision and artifact digest [ ], change owner [ ], stop authority [ ], reversal or forward-repair point [ ], observation window [ ].

| Review question | Evidence ID and outcome |
| --- | --- |
| Can the consumer complete the promised operation from an ordinary client? | [Probe, denominator, data shape, result.] |
| Can the team replace capacity during the modeled failure? | [Surviving throughput, quotas, cold start and downstream measurements.] |
| Can the intended operators reach and authorize recovery? | [Independence of route, identity, keys and instructions.] |
| Can retained data be restored and interpreted? | [Clean restore point, version/key dependencies, integrity and consumer read.] |
| Are isolation and denial observable? | [Test identity, source, target, deciding control and audit event.] |
| Can the operator detect and reverse a bad change? | [Independent signal, abort condition, last safe rollback point and exercise.] |
| Who supports the steady service? | [On-call contact, supplier terms, cost owner and next maintenance deadline.] |

## Record the decision

For each check use **observed**, **modeled**, **failed** or **inapplicable with reason**. Include test date and actual environment. Capture “unknown” when the team lacks either measurement or a defensible model. A staging result may support the production decision if differences and their consequences are explicit.

Decision [expand / hold / stop / accept stated gap]. Reason [ ]. Residual exposure [ ]. Compensating action [ ]. Accountable owner [ ]. Expiry or earlier revisit trigger [ ]. Confirm the first production cohort's result and record any change to the plan before expansion.
