# Continuity across ingestions

Durable records must carry what was read, its version and meaning, what changed, and what remains. A conversation summary or successful job status cannot supply that continuity.

The [ingestion mission](../missions/ingest.md) applies this contract; [maintenance](../missions/maintain.md) checks it over time.

## Record coverage, not just a last-run date

The [source record](../templates/source.md) holds stable identity and explicit access and retention policy. Each processed unit needs a compact [receipt](../templates/ingestion-log.md) identifying:

- The source identity and observed version, revision, or snapshot.
- The range actually examined, such as message IDs, document sections, pages, records, or a bounded time window with stable item IDs.
- Its processing outcome and any gap or retry requirement.
- Resulting canonical notes, or the reason no notes were created.
- A retrieval readback result for knowledge written or changed.

Use supported granularity: one unit for a tiny document, ranges for a long conversation. Without versioning, record observation time and a suitable fingerprint or permitted snapshot, with its limits. A fingerprint detects change; it does not prove what the source said.

A session title, "processed through Tuesday," or agent memory alone cannot checkpoint overlapping imports, edited messages, or interruptions reliably.

## Keep outcomes distinct

These example outcome labels need no fixed schema or workflow engine. One receipt can cover several versions or ranges if their coverage and outcomes remain unambiguous.

| Outcome | Meaning | Next treatment |
| --- | --- | --- |
| `collected` | The source unit has been located or captured but not fully examined. | Process it within granted permissions. |
| `partial` | Only part was readable, examined, or integrated. | Record exact coverage and retry the uncovered or unresolved part. |
| `blocked` | A named dependency prevents further progress. | Retain the dependency and resume when it changes. |
| `integrated` | Durable knowledge was persisted and successfully read back, with a receipt for the covered unit. | Revisit if the source changes or knowledge needs revalidation. |
| `intentionally-skipped` | A permitted policy or authorized decision excludes this unit. | Record the reason and relevant policy; revisit if that changes. |
| `no-durable-change` | The covered unit was examined and yielded no useful new knowledge or was already represented correctly. | Keep the coverage receipt and reason; reconsider if new context changes its meaning. |

Unreadable material is not "no durable change," and a truncated excerpt cannot complete a full source. Mark the overall unit partial and describe any narrower integrated coverage. A retention or exclusion policy can justify a skip; failure to read cannot.

## Reconstruct context before integrating

Consider this fictional sequence:

> Monday: "We are comparing the Basic offer at €5,000 with Standard at €8,000."
>
> Tuesday: "We chose the second one."

Retrieve the preceding exchange or a canonical note preserving both options. Confirm the referent, decision-maker, and scope before saving a pricing decision. If evidence is unavailable, preserve the gap instead of guessing what "second" means.

Revisit prior coverage, including no-durable-change units, when new evidence depends on it or gives it meaning.

## Complete a unit in recoverable steps

1. **Select and identify.** Read the source version and coverage to process. Check existing receipts and permissions before collecting additional content.
2. **Retrieve context.** Read the current canonical account and the targeted prior evidence needed to interpret this unit.
3. **Reconcile.** Distinguish new facts, changed facts, decisions, conflicts, unknowns, and material that should not become durable knowledge.
4. **Persist.** Save the note changes, source references, and any dependent-view updates that can be completed now. Record remaining refresh work explicitly.
5. **Checkpoint.** Save the coverage receipt with its outcome still partial or pending readback.
6. **Read back.** Use a plausible future question to find and open the canonical knowledge from the brain's entry points or normal search. Verify meaning, evidence links, and relevant dates.
7. **Finalize.** Only then mark that coverage integrated and persist the readback outcome.

Saved knowledge, receipt, and successful retrieval readback are distinct completion evidence for the examined version and range, even in one file. A flag, source ID, or successful run cannot replace them. No-durable-change and intentionally-skipped outcomes need coverage and reasons, not filler notes.

File edits may not be atomic. After an interruption without a receipt, inspect saved notes and source references before reapplying changes. After a pending receipt, resume readback and reconciliation. Deduplicate by stable source identity, version, and range so repeated delivery converges on one canonical assertion.

## Handle changing sources

Completion applies to the observed version. Compare changes and revalidate dependent assertions: appended messages may need only new coverage; edited messages can invalidate conclusions. A rename with preserved identity need not create a new source.

Before finalizing, verify that the receipt identifies what was actually read. If the source changed meanwhile, preserve supported work against that version or permitted snapshot and leave changed ranges and dependent claims for revalidation. A matching source ID cannot acknowledge a newer version. Keep coverage partial if the examined content cannot be identified reliably.

Without reliable change markers, document a periodic comparison strategy and its limits. Overlapping time windows recover late arrivals but cannot detect every edit or deletion.

Missing material may reflect partial results, changed access, expired retention, or deletion. Apply deletion semantics only when the source contract supports them, and review permitted retention of dependent knowledge.

## Preserve the path back to evidence

Keep locators, excerpts, or snapshots under the retention policy. Digests must point to evidence; replacing the only retained evidence with a summary requires applying that policy and recording the verification limit.

Protect confidential locators and dependency records. Review derivative access separately from factual validity; continuity cannot override [revocation and retention](governance.md#handle-revocation-without-promising-recall).

Search the relevant retained archive for context missing from current notes. Historical, superseded, or review-due material may explain a fragment without becoming current knowledge. Follow [retrieval](retrieval.md).

## Make the next run intelligible

A handoff identifies the source unit, exact gap, consequence, next attempt or dependency, and views awaiting refresh. Link compact receipts to evidence; do not use full agent transcripts as ingestion logs.

Maintenance checks uncovered ranges, repeated failures, expired evidence access, overdue reviews, broken links, duplicates, and stale summaries. Surface meaningful gaps under the [autonomy policy](governance.md); already authorized work needs no fresh approval.
