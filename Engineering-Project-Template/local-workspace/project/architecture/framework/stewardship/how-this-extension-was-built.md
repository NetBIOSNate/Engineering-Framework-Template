# Creation and verification record

This record documents the one-time extension of the engineering project's architecture workspace on 7 November 2026. The starting directory contained seven empty directories named `capacity-planning`, `component-design`, `data-flows`, `decisions`, `dependency-boundaries`, `system-context` and `trust-boundaries`. The delivery boundary is the `project/architecture` directory. Sibling project disciplines keep their own implementation, operational and governance records.

## How the material was organized

1. Inventory the existing paths, including hidden entries, and check for local project instructions. Treat the seven existing directory names as stable entry points.
2. Give each existing area a general design guide and a deeper decision or verification topic. Add physical interface guidance alongside software contracts. Choose examples with an observable outcome and a failure boundary.
3. Add a common `framework` branch for designing the framework, applying it through the project lifecycle, cross-cutting concerns, project profiles, worksheets, a worked trace, reference material and stewardship.
4. Distinguish the questions the selected public frameworks answer. The [reference crosswalk](../reference/framework-crosswalk.md) gives publisher links for follow-up. The project-specific guidance, selection rules and examples are original to this library.
5. Walk one example from a stakeholder goal through alternative architectures, custody, capacity, failure and proposed evidence. Label illustrative inputs and calculations so future projects can substitute measured values.
6. Place a final inventory in the architecture root. It distinguishes the original directories from additions and enumerates the new paths, including the inventory itself.

## Native Windows creation procedure

PowerShell was used for every directory and file creation. Each write batch checked the intended root, rejected an occupied destination and checked existing ancestors for unexpected file types or reparse points. Missing directories were created one path component at a time. New documents were created with `New-Item -ItemType File -Value`, read back with `Get-Content -Raw -Encoding utf8` and compared with the authored text. Commands operated on explicit paths. No setup script or package is needed to use the library.

The authors used relative Markdown links so a project can move the architecture tree as a unit. Source references are ordinary publisher links. Each core guide joins a decision to a way of checking it. The framework's general policy belongs in the shared method. Project-profile instructions describe what changes under a particular condition.

## Acceptance procedure

- Enumerate all descendants with native PowerShell. Compare the file and directory sets with the starting layout plus the declared additions. Check that all original folders remain directories.
- Verify every expected document is readable, has a top-level title, and matches its authored text. Resolve relative Markdown links from each source file and check that every internal target exists inside the architecture root.
- Check navigability from the field guide, directly or via linked guides. Check the worked example's buffer and drain arithmetic against its stated units and time window.
- Generate the root inventory from the verified tree, listing new directories and files. Create it last with exclusive creation semantics and read it back. Perform final read-only verification after adding it.

## Reusing the material

Start a new project with the [brief](../worksheets/framing/architecture-brief.md), a single consequential decision and one applicable profile. Keep project measurements and approvals in the project's records. Use the [framework charter](../framework-design/01-charter/purpose-and-design-principles.md) when adapting the method for a class of projects and the [pilot guide](../framework-design/03-adoption/pilot-and-improvement.md) to evaluate an adaptation. The inventory is a record of this delivery. Later editions can maintain their own change history.

[Architecture field guide](../README.md)
