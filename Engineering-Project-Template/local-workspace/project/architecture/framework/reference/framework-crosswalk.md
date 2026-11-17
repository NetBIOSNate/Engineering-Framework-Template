# Framework crosswalk and primary references

Use each reference for the question it helps answer. This library combines selected concepts with original project guidance and examples. Its five-phase method, worksheet fields and numerical examples are local design choices. Formal conformance or a sector-specific assurance determination requires its own scope and evidence.

| Need | Reference and application in this library | Local artifact |
| --- | --- | --- |
| Describe an architecture across disciplines | ISO/IEC/IEEE 42010:2022 gives concepts and requirements for architecture descriptions and frameworks. Use concerns, viewpoints, views and consistency relationships to organize what readers need | [Artifact and viewpoint model](../framework-design/02-structure/artifact-model-and-viewpoints.md) |
| Discover meaningful quality requirements | SEI's Quality Attribute Workshop (QAW) informs early stakeholder scenarios, even while the architecture is conceptual | [Quality scenarios](../method/01-frame/quality-attribute-scenarios.md) |
| Evaluate a proposed design | SEI's Architecture Tradeoff Analysis Method (ATAM) examines architectural approaches against quality concerns and exposes risks, sensitivity points and tradeoffs | [Scenario-based review](../method/03-evaluate/tradeoff-review.md) |
| Explain software structure | C4 offers context, container, component and code views, with dynamic and deployment views where useful. Select depth according to the reader's question | [View selection](../method/02-design/views-and-correspondence.md) |
| Check coverage of software documentation | arc42 organizes architecture documentation into twelve tailorable sections. Use its topics to spot absent decisions, quality goals, risks or runtime behavior | [Field guide](../README.md) |
| Coordinate enterprise change | The TOGAF Standard, 10th Edition, includes the Architecture Development Method and guidance for tailoring practice. For a multi-product change, connect capability, baseline, target, transition and governance | [Enterprise profile](../profiles/enterprise-systems/capabilities-and-transitions.md) |
| Connect allocation, verification and validation | NASA's Systems Engineering Handbook provides systems-engineering examples and supporting material. Verify specified requirements and validate intended use with representative users and conditions | [Assurance evidence](../concerns/assurance/hazards-and-evidence.md) |
| Build security into system design | NIST SP 800-160 Vol. 1 Rev. 1 addresses systems security engineering across the lifecycle. Translate protection needs into authority boundaries, design decisions and supporting evidence | [Authority at crossings](../../trust-boundaries/protection/identity-and-authority.md) |

## Applying the combination

When designing a reusable framework, start with its [charter](../framework-design/01-charter/purpose-and-design-principles.md), define the [artifact relationships](../framework-design/02-structure/artifact-model-and-viewpoints.md), then [pilot the method](../framework-design/03-adoption/pilot-and-improvement.md). When applying an existing framework to one system, begin with the [architecture brief](../worksheets/framing/architecture-brief.md). A solo project may use a scope sketch and one decision. Enterprise or physical projects can add views without imposing new software terminology on the rest of the team.

## Publisher pages consulted on 7 November 2026

- Description and scope of the architecture-description standard. [ISO/IEC/IEEE 42010:2022](https://www.iso.org/standard/74393.html)
- Relationship between QAW and ATAM and the stage at which each helps. [CMU Software Engineering Institute](https://www.sei.cmu.edu/library/sei-architecture-analysis-techniques-and-when-to-use-them/)
- Levels of structural detail and supporting views. [C4 diagram guidance](https://c4model.com/diagrams)
- The twelve documentation sections and their purposes. [arc42 template overview](https://arc42.org/overview/)
- Scope, structure and tailoring of the tenth edition. [The Open Group overview](https://help.opengroup.org/hc/en-us/articles/32726995273362-Understanding-the-TOGAF-Standard)
- Systems engineering guidance and reference appendices. [NASA Systems Engineering Handbook appendices](https://www.nasa.gov/reference/system-engineering-handbook-appendix/)
- Lifecycle systems security engineering. [NIST SP 800-160 Vol. 1 Rev. 1](https://csrc.nist.gov/pubs/sp/800/160/v1/r1/final)

[Architecture field guide](../README.md)
