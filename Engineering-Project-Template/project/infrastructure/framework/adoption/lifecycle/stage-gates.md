# Lifecycle from discovery to retirement

Use these reviews when a project makes a material commitment. A small team can conduct several in a single meeting. Attach an exact system, environment and date to the evidence so another engineer can reproduce the decision.

| Phase | Action | Exit evidence |
| --- | --- | --- |
| Discover | Identify consumer, critical period, sensitive data, existing assets, operator availability and funding limit. | A scoped brief with an owner who accepts the objectives. |
| Design | Trace traffic, trust, placement and recovery paths. Compare two viable designs under the same demand and failure assumptions. | A decision with measurements still needed and a revisit trigger. |
| Build | Establish bootstrap access, protected state and an authenticated artifact source. Commission one end-to-end instance with synthetic data. | Input versions, deployed identities and one successful consumer operation. |
| Qualify | Exercise a denial, dependency loss, reversible change and isolated restore. Identify shared failure modes. | Timestamped observations and an owner for each material gap. |
| Introduce | Start with a bounded cohort. Assign stop authority and observe for a representative demand period. | Decision to expand, pause or recover based on cohort health. |
| Operate | Review user-facing objectives, surviving capacity, support dates, restore results and spend. | Service record, runbook and a prioritized improvement with a measurable outcome. |
| Retire | Freeze new dependants, migrate readers and writers, observe retention, release authority and assets. | Consumer sign-off plus disposition of bills, alerts, routes, keys and support obligations. |

A gate can reopen. If a storage change doubles restore time, revisit the architecture before the next capacity commitment. If the project accepts a gap, record its consequence, compensating measure, expiry and trigger for earlier review. The [catalog](../../reference/catalog.md) includes copyable records for each review.
