# Continuity across ingestions

An agent starts each run with limited context. Durable records must carry the continuity: what was read, which version it came from, what it meant, what changed, and what still needs work. A conversation summary or a successful job status is not enough.

Use this contract in the [ingestion mission](../missions/ingest.md). The [maintenance mission](../missions/maintain.md) checks that it remains true over time.

## Record coverage, not just a last-run date

For each source, maintain a stable identity and an explicit access and retention policy in the [source record](../templates/source.md). For each processed unit, write a small [ingestion receipt](../templates/ingestion-log.md) that identifies:

- The source identity and observed version, revision, or snapshot.
- The range actually examined, such as message IDs, document sections, pages, records, or a bounded time window with stable item IDs.
- Its processing outcome and any gap or retry requirement.
- Resulting canonical notes, or the reason no notes were created.
- A retrieval readback result for knowledge written or changed.

Use the granularity the source supports. A tiny document may be one unit; a long conversation needs ranges. If versioning is unavailable, record the observation time and a suitable fingerprint or retained snapshot where permitted. State the limitation. A source-content fingerprint is a change detector, not evidence of what the source said.

Do not use a session title, a vague "processed through Tuesday," or an agent's memory as the only checkpoint. Overlapping imports, edits to old messages, and interrupted runs make these unreliable.

## Keep outcomes distinct

The labels below are a shared example vocabulary for semantic outcomes. They may be written as short values in the receipt; they do not require a fixed schema or workflow engine. One receipt can describe several versions or ranges if their coverage and outcomes remain unambiguous.

| Outcome | Meaning | Next treatment |
| --- | --- | --- |
| `collected` | The source unit has been located or captured but not fully examined. | Process it within granted permissions. |
| `partial` | Only part was readable, examined, or integrated. | Record exact coverage and retry the uncovered or unresolved part. |
| `blocked` | A named dependency prevents further progress. | Retain the dependency and resume when it changes. |
| `integrated` | Durable knowledge was persisted and successfully read back, with a receipt for the covered unit. | Revisit if the source changes or knowledge needs revalidation. |
| `intentionally-skipped` | A permitted policy or authorized decision excludes this unit. | Record the reason and relevant policy; revisit if that changes. |
| `no-durable-change` | The covered unit was examined and yielded no useful new knowledge or was already represented correctly. | Keep the coverage receipt and reason; reconsider if new context changes its meaning. |

An unreadable attachment is not "no durable change." A truncated excerpt cannot be marked integrated for the full source. If some useful facts were integrated, mark the overall unit partial and describe the narrower completed coverage. An explicit retention or exclusion policy may justify a skip; failure to read does not.

## Reconstruct context before integrating

Consider this fictional sequence:

> Monday: "We are comparing the Basic offer at €5,000 with Standard at €8,000."
>
> Tuesday: "We chose the second one."

Tuesday alone cannot support a durable pricing decision. Retrieve the relevant preceding exchange or a canonical note that preserves both options. Confirm the referent, decision-maker, and scope. If the source cannot be recovered, keep the unresolved statement and its gap; do not guess that "second" means Standard.

New evidence can make an earlier non-actionable fragment meaningful. Revisit the relevant prior coverage, including units previously marked no durable change, when the new material depends on it.

## Complete a unit in recoverable steps

1. **Select and identify.** Read the source version and coverage to process. Check existing receipts and permissions before collecting additional content.
2. **Retrieve context.** Read the current canonical account and the targeted prior evidence needed to interpret this unit.
3. **Reconcile.** Distinguish new facts, changed facts, decisions, conflicts, unknowns, and material that should not become durable knowledge.
4. **Persist.** Save the note changes, source references, and any dependent-view updates that can be completed now. Record remaining refresh work explicitly.
5. **Checkpoint.** Save the coverage receipt with its outcome still partial or pending readback.
6. **Read back.** Use a plausible future question to find and open the canonical knowledge from the brain's entry points or normal search. Verify meaning, evidence links, and relevant dates.
7. **Finalize.** Only then mark that coverage integrated and persist the readback outcome.

The record of an integrated unit must include the saved knowledge, receipt, and successful retrieval readback. These are separate pieces of evidence even when they live in one file. For no-durable-change or intentionally-skipped outcomes, save the examined coverage and reason; do not create filler notes to satisfy a completion rule.

Filesystem edits may not be atomic across files. If a run stops after writing notes but before recording a receipt, the next run must inspect the notes and source references before applying the same change again. If it stops after a pending receipt, resume with readback and reconciliation. Use stable source identity, version, and range to recognize duplicate work. Repeated delivery should converge on one canonical assertion, not repeated copies.

## Handle changing sources

A completed range is complete for the observed version. If that source version changes, compare the affected sections and revalidate dependent assertions. An appended message may need only new coverage; an edited earlier message can invalidate a previous conclusion. A renamed file need not be a new source if its stable identity is preserved.

When the source cannot supply reliable change markers, use a documented periodic comparison strategy and acknowledge its limits. A time-window overlap helps recover late arrivals; it does not by itself detect every edit or deletion.

Missing material is not proof of withdrawal. Confirm whether the connector returned a partial result, access changed, retention expired, or the source deliberately deleted a record. Apply deletion semantics only when the source contract supports them. Review what dependent knowledge may still be retained under the user's policy.

## Preserve the path back to evidence

Keep original source locators, permitted retained excerpts, or snapshots according to the user's retention decision. A digest is useful for navigating a long history but must point to evidence. Do not replace the only retained evidence with a summary without applying the retention policy and marking the resulting verification limit.

If the current notes fail to explain a new fragment, search the relevant retained archive. Historical, superseded, or review-due material can supply context; it must not silently become a current fact. Read the [retrieval rules](retrieval.md) before promoting it.

## Make the next run intelligible

A short handoff should make remaining work actionable: the source unit, exact gap, why it matters, next attempt or dependency, and any dependent views awaiting refresh. Keep receipts compact and link to evidence. Do not accumulate full agent transcripts as ingestion logs.

Maintenance should detect uncovered ranges, repeated failures, expired evidence access, overdue reviews, broken references, duplicate assertions, and summaries that no longer match canonical notes. Surface meaningful gaps under the chosen [autonomy policy](governance.md); do not request a fresh human approval for work already authorized.
