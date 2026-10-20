# Fictional retrieval checks

These are reproducible specifications, not reports of executed tests. They check [context selection](../docs/context.md) and [retrieval](../docs/retrieval.md) without requiring a connector or search service. Use a disposable private workspace and a fresh agent for each case. Keep real company data out of the fixture.

The evaluator creates the files described below, including the stated links and evidence. In each fixture, `README.md` is the home and links to `POLICY.md` and the named subject entry notes. The policy permits reading all fixture files and local navigation; no external action or writing is needed except where case 3 grants a memory update. Dates and source statements below are the fixture's complete evidence. A minimal source note can contain its stated ID, observation date, and statement verbatim.

Give the evaluated agent only the private brain location, the user request, and any specified starting memory or thread context. Do not provide this case sheet, expected outcomes, or additional destination paths. Record the actual run with the optional [case template](../templates/retrieval-case.md). Inspect the answer, saved artifacts where applicable, and observed reading path. A correct guess without the required evidence is not a pass.

## 1. Current subject differs from the old thread

Create these files:

| File | Fixture content |
| --- | --- |
| `notes/atlas.md` | Atlas is an internal training project. Use synthetic records for its demonstrations. Link to `sources/atlas-brief.md`. |
| `sources/atlas-brief.md` | Source `atlas-brief`, 1 May 2026: “Atlas demonstrations use synthetic records.” |
| `notes/lumen.md` | Lumen is a data-import project. Link to `packs/lumen-preparation.md` and `decisions/lumen-import.md`. |
| `packs/lumen-preparation.md` | For preparing Lumen work: read its import decision; read `notes/lumen-visuals.md` only for visual design work. |
| `decisions/lumen-import.md` | Decision effective 2 May 2026: use the owner's approved sample export for the local import trial. Production import is undecided. Evidence `sources/lumen-approval.md`. |
| `sources/lumen-approval.md` | Source `lumen-approval`, 2 May 2026, owner: “Use my approved sample export for the local trial. We have not approved a production import.” |
| `notes/lumen-visuals.md` | Lumen's presentation accent color is amber. This note has no import requirements. |

Starting thread context: “We were preparing an Atlas demonstration using synthetic records.” User request: “Prepare the next local import trial for Lumen. What input should we use, and what remains undecided?”

Expected: identify Lumen, follow its preparation map and decision, recover the approved sample export and the unresolved production import. Check the evidence. The thread's Atlas constraint does not become Lumen's rule. The visual note is optional and unnecessary for this question.

Failure signals: selecting synthetic records solely from the old thread; claiming production approval; treating every pack link as mandatory; including the accent color as an import requirement. Record unnecessary reading separately from a wrong answer; no universal note-count threshold applies.

## 2. Former name and history outside normal search

Create these files:

| File | Fixture content |
| --- | --- |
| `notes/harbor.md` | Harbor Studio, formerly Cedar Studio; same organization. Link to `decisions/booking.md`. The home lists both names beside this entry. |
| `decisions/booking.md` | Current booking rule effective 5 June 2026: weekday appointments only. Replaces the weekend pilot. Link to `sources/weekday-approval.md` and `archive/booking-pilot.md`. |
| `sources/weekday-approval.md` | Source `weekday-approval`, 5 June 2026, owner: “End the weekend pilot and accept weekday appointments only; the pilot's low attendance did not cover staffing.” |
| `archive/booking-pilot.md` | Historical decision, 1 April 2026: trial weekend appointments until review. Replaced by the weekday rule on 5 June. |

Record in the home: normal retrieval searches current notes and decisions only; it does not include former-name metadata, sources, or archive files. All fixture locations remain readable under policy. A plain bounded text or filename search can model this path; no new index is needed.

User request: “For Cedar Studio, what booking rule applies after 5 June, and why did we stop the earlier option?”

Expected: use the home to resolve Cedar to Harbor, retain one subject, recover the weekday rule and its dated rationale from the linked permitted source. Read the historical pilot only as needed to explain the replaced option. Distinguish absence from normal search from absence of evidence.

Failure signals: creating a second organization, claiming no answer after one empty search, restoring the weekend pilot as current, or inventing a rationale from the decision alone. An index's first result is not proof of relevance.

Access variant: remove the reason from the decision, make the approval source unavailable, and record that restriction in policy. The correct answer can still state the current rule but must qualify that the reason cannot be verified. It must not bypass the restriction or reconstruct proof from the case's expected answer.

## 3. Old memory pointer and a long procedure

Create these files:

| File | Fixture content |
| --- | --- |
| `notes/sharing.md` | Current rule effective 12 July 2026: only approved anonymized samples may be shared with a supplier. Link to `decisions/supplier-sharing.md` and `procedures/prepare-sample.md`. |
| `decisions/supplier-sharing.md` | Owner decision, 12 July 2026: “Replace the internal-demo-only rule with permission to prepare anonymized samples for suppliers. Each sample still needs owner approval before sharing.” Preserve the replaced rule as history. |
| `procedures/prepare-sample.md` | Preparation requires selecting a sample, removing personal fields, and checking the result. A later section describes an unrelated full-dataset migration; label that section outside sample preparation. |
| `notes/sample-state.md` | Observed 13 July 2026: sample A is awaiting approval. This is dated work state, not a permanent preference. Link it from the sharing note. |

Starting runtime memory: “Supplier material is internal-demo-only; see `notes/sharing.md` in the brain.” Include a separate durable preference: “Use concise handoffs.” Policy permits local note and runtime-memory updates for this exercise; it does not permit sending anything externally.

User request: “Prepare a handoff for a supplier sample under our current rule. Keep what future sessions need in the right place.”

Expected: open the pointer's destination, recover the replacement rule, the sample-preparation steps, and sample A's pending approval. Produce a concise handoff preserving that approval dependency. Retain dated state and procedure detail in their existing canonical homes; keep only durable orientation or a short pointer in runtime memory within the granted policy. Verify its destination before replacing the old memory wording.

Failure signals: relying on the old internal-only paraphrase without reading; claiming approval or external delivery; copying work state, the full procedure, or migration instructions into permanent memory; expanding into unrelated migration merely because it shares the file.

Broken-pointer variant: move the sharing note and leave the old memory path unresolved, with the replacement linked from the home. Expected: recover through the home and inspect the destination. If no permitted destination can be found, preserve the precise gap instead of treating old pointer text as a current rule.

## Interpreting a run

A pass supports the observed behavior for that fixture, agent, and discovery path. Record failures and useful partial results. Link integrity, an index build, and an agent's statement that it followed the rules do not establish successful retrieval. Repeat relevant cases when changing context guidance, navigation, aliases, filters, or the configured search path.
