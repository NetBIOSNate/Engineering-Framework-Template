# Worksheet for a view and its interfaces

Create a view for one stakeholder question. A sketch, sequence, table or dimensioned drawing belongs here if a reader can use it to answer that question. Use stable identifiers and link the authoritative drawing when it is maintained elsewhere.

## View header

| Field | Project entry |
| --- | --- |
| View ID, revision, date and owner | [Identity and person responsible for accuracy] |
| Viewpoint and readers | [Conventions used, audience and decision this view supports] |
| Scope and environment | [System boundary, modes, configuration and assumptions] |
| Legend and units | [Box and arrow meanings, reference direction, physical units, timebase] |
| Authoritative representation | [Insert the drawing/table or link to its maintained location] |
| Related drivers and decisions | [IDs and links] |

## Element and edge records

| Element ID | Responsibility and state owned | Placement or allocation | Loss or failure effect |
| --- | --- | --- | --- |
| [EL-…] | [Rule, fact or authority] | [Person, process, equipment, site] | [Who notices and what remains possible] |

| Interface ID and endpoints | Meaning, units and identity | Success, delay, refusal and uncertainty | Version, trust and owners |
| --- | --- | --- | --- |
| [IF-… from A to B] | [Information, material, energy or command] | [When custody transfers and how to reconcile] | [Supported revisions, authorization and responsible parties] |

## Walkthrough

1. Select one successful case, one interrupted case and one mixed or degraded configuration. Trace each numbered step or edge. Capture a missing step or state as an owned issue.
2. Compare this view with one other representation. A trust boundary in the interface table should agree with placement and with the sequence in which authority is checked.
3. Identify the interface whose description would be most expensive to misinterpret. Ask both endpoint owners to paraphrase the success condition independently.

Record the reviewer, disagreement, disposition and revision that resolves it. See [the completed field-system walkthrough](../../examples/field-observations/02-design/views-and-contracts.md) and [the viewpoint catalog method](../../framework-design/02-structure/artifact-model-and-viewpoints.md).

[Architecture field guide](../../README.md)
