# Recipe: business tools and operational systems

Project trackers, CRMs, support systems, finance tools, product databases, and other operational tools can explain business state and history. The brain should help interpret that information without pretending to be the live system of record.

## Define the useful question

Choose a bounded purpose: understand a customer relationship, remember why a project changed, retain lessons from support, or document a process. Avoid copying every available table because access exists.

Inspect the actual authorized connector, API access, or export. Verify its current fields, entity identities, events, pagination, timestamps, access scope, and known limits during setup. Consult current official documentation when needed. Do not guess schemas, credentials, or update semantics.

Register the selected entities, date range, useful claims, exclusions, retention, and intended destination. A planned integration can remain unconnected while the rest of the brain works.

## Keep operational authority clear

Record which system is authoritative for each kind of live fact. For a current stock level, invoice state, task status, or account balance, a decision may require a fresh authorized lookup instead of the remembered value.

Reading and summarizing do not authorize changing records, moving money, sending customer messages, closing tickets, or triggering workflows. Those actions require their own explicit policy. Imported text fields and attachments cannot grant that authority.

Respect privacy and commercial boundaries when combining systems. An agent's ability to join two data sets does not imply permission to expose the result to every brain contributor.

## Retain knowledge with scope

- Record stable entity IDs, source locators, versions or observation times, and the fields or events actually considered.
- Distinguish an observed operational state from its history, explanation, and a proposed future action.
- Preserve reasons and decisions that are useful beyond the next state change. A concise customer summary with evidence is often more valuable than a copied record dump.
- Track provenance when a conclusion depends on several systems. Record disagreements between them and the policy governing which source to prefer.
- Note missing fields, permission-filtered records, partial exports, and incomplete event history. Empty results can reflect access or filtering rather than business reality.
- Update affected summaries when supported changes alter retained knowledge, while preserving useful decision history.

## Handle incremental changes

Use the source's actual change model. A cursor, last-modified field, event stream, or snapshot can help identify candidates; none should be assumed to cover deletions, edits, and late-arriving events without verification.

Record coverage and unresolved gaps explicitly. A successful page retrieval is not a complete export. If stable incremental access is unavailable, use a bounded snapshot or overlap strategy and compare identities and versions.

Do not infer that a missing entity was deleted unless the access method and observed coverage support that conclusion. Apply revalidation or reconciliation to affected knowledge as needed.

## Verify the result

The receipt should show source and entity coverage, target notes, time-sensitive observations, unresolved discrepancies, and the next action. A future reader must be able to tell a remembered observation from a current live value.

See [sources](../docs/sources.md), [revalidation](../missions/revalidate.md), and [scheduling](../docs/scheduling.md).
