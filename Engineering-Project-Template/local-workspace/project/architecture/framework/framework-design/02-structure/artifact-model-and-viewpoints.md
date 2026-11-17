# Define the artifact model and viewpoint catalog

Design the relationships between records before deciding where to store them. Stable IDs and links let a spreadsheet, drawing, project record or versioned text file participate in the same framework. Keep one authoritative definition of each fact. A copy used for communication should identify its source and applicable version.

## A minimal architecture record model

| Record | Essential fields | Relationship to check |
| --- | --- | --- |
| System and stakeholder | Scope, environment, stakeholder role, concern | Each priority concern belongs to an identifiable stakeholder |
| Driver or constraint | Stimulus, context, target or limit, authority | A design-driving target has an observation or evidence owner |
| Viewpoint and view | Intended reader, questions, conventions, view scope, version | A view addresses named concerns and identifies the viewpoint applied |
| Element and interface | Responsibility, owner, units, direction, agreement | The endpoints agree on the meaning of success, failure and version |
| Decision | Question, options, rationale, status, owner, revisit trigger | A selected option changes a named element or satisfies a driver |
| Risk and evidence | Exposure, claim, observation, configuration, limits, owner | The decision states which claims remain uncertain and who accepts them |

These relationships support simple integrity queries. Which active decisions lack an owner? Which acceptance claims depend on a retired interface? Which driver has no evidence path? Which sensitivity point has crossed the range tested? Choose the queries a user will actually run and decide how much capture work each is worth.

## Register a viewpoint

Name the intended reader and concern, required model elements, allowed relationships, representation conventions, interpretation rules and a consistency check with another view. For example, a failure-containment viewpoint contains logical functions, placement units and shared dependencies. Its rule is to trace two allegedly independent paths down to common power, identity and administrative control. Its output is a map plus a written claim about which disturbance each surviving path tolerates. Its correspondence check compares that map with the startup and restore sequence.

Define an extension by recording its triggering project condition, added fields or views, reviewer and example. A product family adds configuration identity and binding time. A learning system adds decision-time lineage. Leave the core vocabulary stable and specify how a reader can resolve an unfamiliar extension. See [configuration variation](../../profiles/product-families/variation-and-configuration.md), [analytical products](../../profiles/data-products/analytics-and-ml.md) and [project views](../../method/02-design/views-and-correspondence.md).

[Architecture field guide](../../README.md)
