# Portable agent missions

A mission describes an outcome for an agent. It gives the agent room to choose tools and adapt to the environment while making the result inspectable. It is not a shell script, a scheduler, or permission to use every available tool.

You can run a mission interactively before scheduling it. Starting a brain does not require any recurring jobs.

For a bounded interactive assessment without any saved receipt or repair, use the skill's [`check` action](../docs/commands.md#check-a-bounded-read-only-assessment). It does not execute these missions.

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

Every run leaves a receipt based on [the run-report template](../templates/run-report.md). It identifies the mission, actual source coverage, changes made, items left unresolved, and the next safe continuation. A successful agent invocation does not prove that the source was fully fetched or that useful knowledge was integrated.

Keep collection, processing, and integration distinct. Use the shared outcomes `collected`, `partial`, `blocked`, `integrated`, `no-durable-change`, and `intentionally-skipped` in [ingestion records](../templates/ingestion-log.md). A source item can be fetched but incomplete; fully read but intentionally produce no durable knowledge; or understood but blocked from integration by policy.

Use stable source identifiers and version or time coverage. Do not advance a watermark past an unresolved gap unless the gap is separately recorded with a reliable recovery path. Repeat runs should recognize work already done and avoid duplicating notes. A completed snapshot or range does not mean a changing source is permanently complete.

## Automation is a local choice

The user chooses autonomy per source and action. Once a recurring action is authorized, execute it within that policy without asking for the same permission every run. Escalate only when the policy requires it, the scope changes, or necessary information or access is missing.

See [scheduling](../docs/scheduling.md) for connecting these instructions to an existing agent runtime, and [governance](../docs/governance.md) for permissions and shared contributions.
