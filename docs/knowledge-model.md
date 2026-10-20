# Knowledge model

Use the smallest structure that lets a person or agent understand a statement, verify it, and update it without losing its meaning. These concepts are portable; they do not require a database, a particular folder tree, or a large frontmatter schema.

## The core objects

| Object | Purpose |
| --- | --- |
| Canonical note | The maintained account of one subject, such as an offer, project, customer, or procedure. |
| Assertion | A fact, hypothesis, observation, decision, or unknown within that note. |
| Source record | Where the evidence lives, how to access it, and the permitted retention policy. |
| Ingestion receipt | The durable record of which source version and range was examined, the outcome, and resulting notes. |
| Derived view | A context pack, overview, index, or other synthesis built from canonical knowledge. |

Begin with the [note template](../templates/note.md), [source template](../templates/source.md), and [ingestion log](../templates/ingestion-log.md). Keep optional metadata out until it resolves an actual need.

## Assertions need a clear meaning

Distinguish these kinds in ordinary prose or a short label:

- **Fact:** supported by identified evidence.
- **Observation:** what a person or source reported, with its scope preserved.
- **Hypothesis:** a proposed explanation or assumption to test.
- **Decision:** an authorized choice, including scope, effective date, and reason where available.
- **Unknown:** missing or insufficient information, with the consequence when useful.

"A customer asked for weekly exports" is an observation about that customer. It does not establish that all customers need exports or that the company has committed to building them. Frequency of repetition is not authority or proof.

When two sources disagree, retain the competing assertions and their evidence until the conflict can be resolved under the chosen [governance](governance.md). Do not manufacture a compromise value or silently let the most recently imported statement win.

## Evidence belongs at the right level

A source reference should identify the source and a usable locator: a file section, message or thread ID, document section, record ID, or retained excerpt. Include its version or observation time when the content can change. Link to the source record for access and retention details.

One note-level evidence reference can be enough for a short note whose assertions share the same source, timing, and scope. For a note mixing claims from several sources or periods, attach references to the relevant assertions. A reader should not have to guess which of five sources supports a price or a decision.

Prefer stable source IDs over filenames as identity where available. File moves and renamed subjects should not break the trail. A digest or model-generated summary can help find evidence; it cannot prove the source said something.

If retaining a source is prohibited, keep the permitted locator and describe the access dependency. If access or retention later expires, mark affected claims as no longer independently verifiable from the brain. Do not pretend a dead link is usable proof. See [sources](sources.md).

## Three different dates

Use these names when structured dates are useful; the same distinctions can be written in prose.

| Name | Meaning | Example |
| --- | --- | --- |
| `valid_at` | When the assertion applied or was explicitly confirmed. Use an interval when the evidence supports one. | A price becomes effective on 1 April. |
| `recorded_at` | When this assertion was added to or changed in the brain. | The April price list is imported on 18 March. |
| `review_after` | When the assertion should next be checked, according to its volatility and use. | Verify before quoting after 1 July. |

These dates are not interchangeable. Importing a document today does not make its contents valid today. Do not invent an effective date when the source provides none; say that it is unknown and record when the source was observed.

For mixed notes, date the volatile assertions individually when practical. A note's last-modified time says that the file changed, not that every assertion was verified.

## Freshness and truth are separate

An overdue review means **review due**, not **false**. A historical decision can remain accurately recorded after its policy is replaced. A missing confirmation is uncertainty, not a contradiction.

Use a small number of explicit states only when needed:

| State | Treatment |
| --- | --- |
| Current | Supported for its stated scope and time; still subject to the evidence's limits. |
| Review due | Revalidation is needed before relying on it for the relevant use. |
| Disputed | Conflicting evidence remains unresolved. |
| Superseded | A specified later assertion or decision replaces it for a stated scope. |
| Historical | Retained to explain the past; not a current operating instruction. |

States can apply to a section or assertion. Avoid marking a whole note superseded when only one price, owner, or condition changed. The agent must check dates and evidence when reading; a maintenance label alone cannot guarantee freshness. See [retrieval](retrieval.md).

## Changes preserve meaning

When replacing an assertion:

1. Identify the evidence and authority for the change.
2. State what changed, its effective scope and time, and why when known.
3. Link the replacement from the old assertion or retain a concise change history.
4. Update the current account without erasing important prior reasoning.
5. Find derived views and dependent conclusions that must be refreshed.

A context pack is a maintained summary of canonical notes. It should link to those notes and avoid unnecessary duplicated detail. When an offer changes, an old sales brief that repeats its price must be updated or visibly marked for refresh. An index rebuild alone does not repair stale prose.

Do not infer cancellation from absence in a later import. Absence is meaningful only if the source is known to be a complete authoritative snapshot with understood deletion semantics. Otherwise record the discrepancy and seek evidence.

## A compact fictional example

```markdown
# Harbor project

## Current scope

- Decision: use the Standard offer at €8,000 for phase one.
  Valid at: 2026-04-08. Recorded at: 2026-04-09.
  Evidence: source `harbor-planning`, revision 3, messages 41–46.
  Authority: project owner, within the agreed project budget.
  Replaces: the tentative comparison in revision 2, messages 20–27.

## Open questions

- The launch date has not been confirmed. Do not infer it from the offer.

## Related views

- Project brief: refreshed after the scope decision.
```

This level of detail is useful for a consequential decision. A stable glossary definition may need only a short definition and one source link. Match the record to the risk and complexity of the claim.
