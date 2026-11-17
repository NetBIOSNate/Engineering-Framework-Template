# A supportable single-site project

## Use when

The project has one operator or a small shared team, modest demand, and an owner willing to accept measured rebuild downtime. Start with one deployable unit and a simple data path. Tie each new component to a failure or workload it measurably improves.

## Implement the minimum

1. Record the service consumer, operating hours, expected bytes and transactions, tolerated outage, loss limit, operator contact and funding source. Identify the host, persistent state, inputs required to rebuild and how another person gains authorized access.
2. Version the configuration and an image or installation manifest. Export an independently recoverable copy of required data, keys and metadata to a location appropriate to the failure model. Use separate deletion authority if operator error or compromised administration is in scope.
3. Monitor the user-visible operation, free storage, certificate expiry, backup freshness and independent reachability. Set alert delivery to match staffed hours and the actual promise to the consumer.
4. Run one cold rebuild from an empty replacement target, with the original site treated as unavailable. Recover data and read a known item as the consumer. Record elapsed time, newest recovered item, operator time and dependencies discovered.

## Growth trigger

If the data doubles, estimate transfer time again and test the assumption. If restore time or single-person access falls outside the accepted limit, compare a cached recovery copy, an additional custodian, warm capacity and a more resilient topology. Preserve the input and measurement that justify the added complexity.
