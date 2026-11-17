# Infrastructure framework field guide

Start with one capability and follow it from a consumer's request to a verified recovery. For a nightly survey export, the capability is “an analyst can retrieve yesterday's complete file by 07:00.” That statement gives you a design target, an acceptance test and a person who can say whether the service works.

| Your role today | First action | What to bring back |
| --- | --- | --- |
| Learning infrastructure | Follow the [first walkthrough](adoption/learning/first-walkthrough.md) with a pencil and a sample workload. | A dependency sketch and the results you predict during an overwrite. |
| Building a project | Fill in the [project brief](records/intake/project-brief.md), select the relevant [module and environment guides](reference/catalog.md), and rehearse a restore. | A reviewed design, repeatable build and observed results. |
| Accountable for the design | Use the [decision record](records/design/decision.md) and [readiness review](records/assurance/readiness.md) to settle expensive choices. | The largest credible loss, evidence behind the recovery promise, and who owns the residual exposure. |
| Operating an existing installation | Start with the [service record](records/operations/service-record.md) and trace a recent incident through the [lifecycle](adoption/lifecycle/stage-gates.md). | A working recovery contact, usable probe and tested next action. |

## Use the tree

`modules/` describes reusable capabilities and their interfaces. `environment-definitions/` describes where each capability runs and how authority, connectivity and resource policy vary. `framework/` holds decisions that cross those boundaries. The [catalog](reference/catalog.md) links every guide. The [terms guide](reference/terms.md) defines vocabulary used in reviews.

A small project may need a single host, a known image and an independent backup. A fleet may also need staged promotion, quota reservations and a recovery identity per region. Select the smallest design that can demonstrate the agreed outcome. Record a reason and owner for deferred capabilities. The [worked example](examples/archive-service/from-request-to-handover.md) shows how restore arithmetic changes a design before the project commits to hardware.
