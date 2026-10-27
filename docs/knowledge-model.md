# Knowledge model

Use the smallest structure that lets a reader understand, verify, and update a statement without losing meaning. No database, prescribed folder tree, or large metadata schema is required.

## The core objects

| Object | Purpose |
| --- | --- |
| Canonical note | The maintained account of one subject, such as an offer, project, customer, or procedure. |
| Assertion | A fact, hypothesis, observation, decision, or unknown within that note. |
| Source record | Where the evidence lives, how to access it, and the permitted retention policy. |
| Ingestion receipt | The durable record of which source version and range was examined, the outcome, and resulting notes. |
| Derived view | A context pack, overview, index, or other synthesis built from canonical knowledge. |

Start with the [note](../templates/note.md), [source](../templates/source.md), and [ingestion log](../templates/ingestion-log.md) templates. Add metadata only when needed.

For context packs, domain descriptions, and procedures, use the [context roles](context.md#give-each-kind-of-context-its-role). They can be sections rather than separate files.

## Assertions need a clear meaning

Distinguish in prose or short labels:

- **Fact:** supported by identified evidence.
- **Observation:** what a person or source reported, with its scope preserved.
- **Hypothesis:** a proposed explanation or assumption to test.
- **Decision:** an authorized choice, including scope, effective date, and reason where available.
- **Unknown:** missing or insufficient information, with the consequence when useful.

"A customer asked for weekly exports" describes that customer's request, not a universal need or company commitment. Repetition is neither authority nor proof.

Retain conflicting claims and evidence until [governance](governance.md) resolves them. Do not invent a compromise or let the latest import win by default.

## Evidence belongs at the right level

A reference identifies the source and a usable locator: section, message or thread ID, record ID, or retained excerpt. Include a version or observation time for changeable content; link the source record for access and retention details.

A note-level reference can suffice when all assertions share a source, timing, and scope. Otherwise attach references to individual assertions so readers can identify what supports a price or decision.

Prefer stable source IDs where available so renames and moves preserve the trail. Digests and model summaries can locate evidence but cannot prove what a source said.

If retention is prohibited, keep a permitted locator and its access dependency. If access or retention expires, mark affected claims as no longer independently verifiable from the brain; a dead link is not proof. See [sources](sources.md).

## Relationships express a specific claim

When a relationship affects an answer, name its meaning and direction: a project **depends on** an asset, an offer **replaces** another, or a person **approves** a delivery within a stated role. A generic link can support navigation without establishing any of these claims. Use the existing canonical subjects and identifiers; a similar name or related topic is not identity.

Keep the relation's endpoints, scope, evidence, applicable time and relevant conditions together in prose or a small table. Distinguish recorded facts from inferred or proposed relationships. Follow [domain definitions](context.md#define-terms-that-affect-the-task) and [information authority](governance.md#authority-is-specific); no fixed vocabulary, graph database or extra note per edge is required.

For example, “Birch launch depends on approved photographs from Studio Vale” needs the applicable launch, which photographs, their required date and the source establishing the dependency. If those photographs are already accepted, a later supplier delay need not affect this launch. If acceptance is unknown, report a possible impact and the missing check rather than a confirmed delay.

For a conclusion across several links, inspect every material step, its conditions and current evidence within the permitted view. A path alone does not prove causation, delay or permission. Cite its premises and label the inference; inaccessible or missing evidence keeps that conclusion bounded. Changes to an endpoint, relationship or satisfied condition can require review of the dependent conclusion under [changes preserve meaning](#changes-preserve-meaning).

## Three different dates

Use these names for structured dates, or express the distinctions in prose.

| Name | Meaning | Example |
| --- | --- | --- |
| `valid_at` | When the assertion applied or was explicitly confirmed. Use an interval when the evidence supports one. | A price becomes effective on 1 April. |
| `recorded_at` | When this assertion was added to or changed in the brain. | The April price list is imported on 18 March. |
| `review_after` | When the assertion should next be checked, according to its volatility and use. | Verify before quoting after 1 July. |

An import date does not make content valid that day. If no effective date is supported, mark it unknown and record the source's observation time.

Date volatile assertions individually where practical. A file's modification time does not verify every assertion.

## Freshness and truth are separate

An overdue review means **review due**, not **false**. A replaced decision can remain historically accurate. Missing confirmation is uncertainty, not contradiction.

Use a small number of explicit states only when needed:

| State | Treatment |
| --- | --- |
| Current | Supported for its stated scope and time; still subject to the evidence's limits. |
| Review due | Revalidation is needed before relying on it for the relevant use. |
| Disputed | Conflicting evidence remains unresolved. |
| Superseded | A specified later assertion or decision replaces it for a stated scope. |
| Historical | Retained to explain the past; not a current operating instruction. |

Apply states to the affected assertion or section; one changed price need not supersede a whole note. Check dates and evidence when reading: a label cannot guarantee freshness. See [retrieval](retrieval.md).

## Changes preserve meaning

When replacing an assertion:

1. Identify the evidence and authority for the change.
2. State what changed, its effective scope and time, and why when known.
3. Link the replacement from the old assertion or retain a concise change history.
4. Update the current account without erasing important prior reasoning.
5. Find derived views and dependent conclusions that must be refreshed.

Derived views should link to canonical notes and limit duplication. When an offer changes, refresh a sales brief repeating its price or mark it for refresh. An index rebuild does not repair stale prose.

Do not infer cancellation from absence unless a complete authoritative snapshot and its deletion semantics support that conclusion. Otherwise record the discrepancy and seek evidence.

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

Match detail to consequence and complexity. A stable glossary entry may need only a definition and source link.
