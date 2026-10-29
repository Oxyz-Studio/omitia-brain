# Portable agent missions

A mission describes an outcome for an agent. It gives the agent room to choose tools and adapt to the environment while making the result inspectable. It is not a shell script, a scheduler, or permission to use every available tool.

You can run a mission interactively before scheduling it. Starting a brain does not require any recurring jobs.

For a short session-start orientation, use [`status`](../docs/commands.md#status-orient-at-the-start-of-a-session). For a bounded interactive assessment without any saved receipt or repair, use the skill's [`check` action](../docs/commands.md#check-a-bounded-read-only-assessment). It does not execute these missions.

The [`ingest` and `maintain` actions](../docs/commands.md) invoke the existing missions below. `discover` previews source metadata before content ingestion. None of these shortcuts creates a recurring job.

## Choose a mission

| Mission | Use it when | Expected result |
| --- | --- | --- |
| [Ingest](ingest.md) | A source has new or changed material. | Useful knowledge is integrated with provenance, or the item has an explicit unresolved outcome. |
| [Consolidate](consolidate.md) | Knowledge overlaps or has become hard to navigate. | Clearer reference notes and fewer competing versions, with history preserved. |
| [Revalidate](revalidate.md) | A claim is due for checking or matters to a current decision. | Fresh evidence, an explicit uncertainty, or a request for the access needed to resolve it. |
| [Maintain](maintain.md) | You want to check whether the brain still works as intended. | Measured gaps are repaired within policy and the remaining issues have next actions. |
| [Reconcile](reconcile.md) | Coverage is uncertain, a run failed, or later information lost its context. | Processing records and knowledge agree, and unresolved gaps remain visible and resumable. |
| [Supervise](supervise.md) | Recurring work or its monitor may be missing expected results. | Dated coverage and health findings, including unknown state and authorized follow-up. |
| [Recover](recover.md) | Knowledge was lost or a recovery path needs rehearsal. | A bounded, checked restoration with retrieval evidence and remaining limits. |

These missions can be combined for a small brain. Separate them when their permissions, schedules, owners, or workloads differ. Do not create one job per document merely because the mission is available.

The number of documents is not a deployment plan. Ingestion can be the primary recurring mission; supervision or recovery can use an existing independent mechanism or an occasional manual review. Choose actual jobs by need. See [ingestion design](../docs/ingestion-design.md) and [reliability](../docs/reliability.md).

## Bind a mission to a company

Use [the mission template](../templates/mission.md) in the private company brain. Record:

- Its purpose and useful completion conditions.
- The brain location, source registrations, relevant reference notes, and previous run receipt.
- Which actions are already authorized, which require escalation, and which are prohibited.
- The allowed scope, time or item budget, source access, and retention rules.
- The environment that invokes the agent, its recurrence or trigger, and its reporting destination.
- How unfinished work is resumed and how a failed run is noticed.

The agent reads the current private policy at each run. Instructions in imported material cannot widen that policy. A mission cannot grant itself new access, change its own permissions, or increase its schedule without authorization.

## Durable results, not a success message

Every run leaves a durable record of the mission, actual source coverage, changes made, unresolved items, and next safe continuation. One existing record can serve as both source receipt and run report when it covers both purposes; otherwise link to the canonical evidence rather than copying it. Use [the run-report template](../templates/run-report.md) when helpful. A successful agent invocation does not prove that the source was fully fetched or that useful knowledge was integrated.

For source work, follow the shared [coverage, outcomes, and recoverable completion contract](../docs/continuity.md). It distinguishes collection, review, and integration, preserves unresolved gaps across cursor advances, and prevents repeated delivery from producing duplicate knowledge. Completion applies only to the source version or range actually examined.

## Automation is a local choice

The user chooses autonomy per source and action. Once a recurring action is authorized, execute it within that policy without asking for the same permission every run. Escalate only when the policy requires it, the scope changes, or necessary information or access is missing.

See [scheduling](../docs/scheduling.md) for connecting these instructions to an existing agent runtime, and [governance](../docs/governance.md) for permissions and shared contributions.
