# Design a framework for a class of projects

An architecture framework gives people a repeatable way to describe a system, decide among alternatives and carry the chosen design into use. Define its intended users and the decisions it should improve before choosing document names or review gates. A framework for choosing capital equipment can share concepts with one for software while using different views and verification evidence.

## Write the framework charter

| Charter field | Question for its sponsor |
| --- | --- |
| Scope | Which kinds of system, decision and lifecycle stage will the framework support? |
| Users | Who creates records, who uses them to act and who can accept the resulting obligations? |
| Promised outcome | Which recurring failure in design or handoff should become less frequent? |
| Core concepts | What minimum language must travel across every project using this framework? |
| Local discretion | Which representations, profiles, review depth and tools may a project choose? |
| Stewardship | Who may change the framework and how will users recognize a new edition? |

## Identify the common core

Review a small project, a project that crosses teams and one with an expensive physical or operational failure. For each, take an actual consequential decision and trace it from mission to evidence. Keep a common field when it helps a downstream reader act. For example, the term “owner” needs a precise scope because the owner of a radio link may differ from the owner of delayed records. A universally required deployment diagram would provide less value to a manual service with no deployable software.

Express a design principle as a default choice, its rationale and the condition that can justify a different choice. Example: assign each mutable fact one authoritative writer to simplify recovery. A disconnected multi-writer design can qualify when it specifies merge semantics, user-visible conflicts and reconciliation ownership. An exception has a technical cost a team can discuss.

## Deliver the first edition

Publish the charter, vocabulary, minimum relationships, viewpoint catalog, project profiles, worksheets and one small completed trace. State how projects contribute improvements, how old records retain their meaning and what evidence would warrant adding a new required field. Use [the artifact model](../02-structure/artifact-model-and-viewpoints.md) to define those relationships and [the pilot](../03-adoption/pilot-and-improvement.md) to test whether they earn their cost. The [crosswalk](../../reference/framework-crosswalk.md) identifies the public methods this library draws from.

[Architecture field guide](../../README.md)
