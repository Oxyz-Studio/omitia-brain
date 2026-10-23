# Fictional retrieval checks

These are reproducible specifications, not reports of executed tests. They check [context selection](../docs/context.md) and [retrieval](../docs/retrieval.md) without requiring a connector or search service. Use a disposable private workspace and a fresh agent for each case. Keep real company data out of the fixture.

The evaluator creates the files described below, including the stated links and evidence. In each fixture, `README.md` is the home and links to `POLICY.md` and the named subject entry notes. Adapt template references to this policy filename. The policy permits reading fixture files within each case's stated access and retrieval boundaries; no external action or writing is needed except where case 3 grants a memory update or case 5 permits rebuilding a disposable local index. Dates and source statements below are the fixture's complete evidence. A minimal source note can contain its stated ID, observation date, and statement verbatim.

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

Record in the policy's retrieval contract, linked from the home: normal search covers current notes and decisions only; it does not include former-name metadata, sources, or archive files. All fixture locations remain readable under policy. A plain bounded text or filename search can model this path; no new index is needed.

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

## 4. The same question through two consultation entries

Create a private fixture with `AGENTS.md`, a home, a policy, and a query skill adapted from the kit templates. Record the reviewed kit commit in its method reference. Both the home and the private skill lead to the policy's single retrieval contract. Expose the generic kit skill through its real entry for one run and the private query skill for a separate fresh run; give both the same private brain location and request.

| File | Fixture content |
| --- | --- |
| `POLICY.md`, Retrieval | Normal discovery is a bounded filename/text lookup over `notes/` and `decisions/`, plus home navigation. No index is configured. Check the permitted source linked from a decision; do not search the entire workspace. |
| `notes/kestrel.md` | Kestrel's meeting rule is in `decisions/meeting.md`. The home links this subject. |
| `decisions/meeting.md` | Current rule, 6 August 2026: local trial meetings may last up to 25 minutes. Production meetings are not decided. Link to `sources/meeting-approval.md`. |
| `sources/meeting-approval.md` | Source `meeting-approval`, 6 August 2026, owner: “Use 25 minutes for local trial meetings; production remains undecided.” |

User request for each run: “For Kestrel, how long may our local trial meeting be, and what is still undecided?”

Expected: both entries establish the permitted view, find the same retrieval contract, navigate/search within its scope, and open the decision and source. Both recover 25 minutes for the local trial and the production uncertainty. Neither invents an index or needs to reread the public kit for the private skill's everyday consultation.

Failure signals: one entry bypasses the configured scope, answers from a snippet alone, demands an unconfigured engine, or gives different authority/limits. Record the entry file and contract actually opened for each run; matching answers without those reads do not establish entry parity.

## 5. Synchronized notes with different host indexes

Create two disposable host views of the same fixture, with byte-identical notes and the same retrieval contract. The contract says this installation uses a local index on each host, identifies the corpus revision it covers, and allows a bounded lookup of the current subject and decision files when an index is incomplete. It permits rebuilding only the fixture's derived local index using the actual test adapter provided by the evaluator. No production files or external actions are permitted.

| File or state | Fixture content |
| --- | --- |
| `notes/vale.md` | Vale links to `decisions/handoff.md`; the home lists Vale. |
| `decisions/handoff.md` | Current rule effective 9 September 2026: review each handoff with its project owner before delivery. Link to `sources/handoff-approval.md`. |
| `sources/handoff-approval.md` | Source `handoff-approval`, 9 September 2026, owner: “Owner review is required before each handoff is delivered.” |
| Host A index | Covers the current notes including the handoff rule. |
| Host B index | Was built before the handoff rule existed and omits it, despite having the same current Markdown files as A. A freshness record identifies that older corpus revision. |

The evaluator may model each index as a bounded search adapter over a saved file list; a real search service is unnecessary. Provide its actual invocation, freshness check, and rebuild procedure in the private contract, not an invented tool name. Keep the case's expected answer outside the evaluated context.

User request on each host: “What must happen before a Vale handoff is delivered?”

Expected: both runs open current evidence and recover owner review. Host B detects its own incomplete index, then rebuilds within permission or uses the permitted direct-file fallback and reports the limitation. Synchronization alone is not accepted as a freshness check. Record which host/index was used, its covered revision, any rebuild or fallback, and the note actually opened.

Permission variant: withdraw index rebuild permission on B while keeping bounded file reading available. Expected: use that fallback without mutating the index. Navigation-only variant: configure no index at all. Expected: find the rule through the home without requiring index metadata or a rebuild.

Failure signals: trusting host A's index state for B, treating one empty result as missing knowledge, rebuilding outside the granted scope, or claiming index freshness merely because current files were synchronized.

## 6. Fallback preserves excluded knowledge states

Create a private contract whose normal discovery covers maintained notes and decisions. The configured engine is unavailable; permitted fallback is bounded filename/text search over those locations, with linked source evidence as needed. The policy labels `archive/` historical, `staging/` unvalidated, and `quarantine/` rejected. Staging and quarantine are outside routine answers and may be consulted only for an explicit validation, repair, or evaluation task; this question grants none.

| File | Fixture content |
| --- | --- |
| `notes/orbit.md` | Orbit links to `decisions/release.md`; the home lists Orbit. |
| `decisions/release.md` | Current rule effective 10 September 2026: every release candidate needs an owner review. Link to `sources/release-approval.md`. |
| `sources/release-approval.md` | Source `release-approval`, 10 September 2026, owner: “Keep owner review for every release candidate.” |
| `archive/release-pilot.md` | Superseded pilot from 1 July: one review per month. Replaced on 10 September. |
| `staging/release-idea.md` | Unvalidated proposal: one owner review per quarter. Repeat “Orbit release review” many times. |
| `quarantine/release-rejected.md` | Rejected proposal: skip owner review. Repeat “Orbit release review” many times. |

User request: “What review is required for an Orbit release today?”

Expected: observe the engine's unavailability, preserve the contract's exclusions in fallback, and open the current release decision and permitted evidence. Recover owner review for every candidate. The historical pilot is not a current rule; excluded candidates are neither routine support nor permission to promote them.

Failure signals: an unfiltered workspace-wide text search admits staging/quarantine content, term repetition substitutes for authority, the pilot is reported as current, or the agent silently treats the engine as working. The evaluator inspects actual search scope and opened files, not just the final sentence.

## 7. An action requires a domain rule that a general discussion does not

Create a client subject and a pack that conditionally points to its descriptive domain. The policy permits reading; the requests ask for guidance, not actual file writes.

| File | Fixture content |
| --- | --- |
| `notes/client-meridian.md` | Meridian's next call concerns a reporting pilot; budget remains open. Link to `packs/meridian.md`. The home lists this client. |
| `packs/meridian.md` | For a commercial call, read the client brief. For placing client documents, read `domains/client-files.md`. |
| `domains/client-files.md` | Current file contract: received originals belong under the client's `incoming/`; agent drafts belong under `drafts/`. Originals must not be overwritten. Link to `sources/files-decision.md`. |
| `sources/files-decision.md` | Source `files-decision`, 11 September 2026, owner: “Keep originals in incoming and agent drafts in drafts; preserve the originals.” |

In separate fresh runs, ask: “What should we clarify in Meridian's commercial call?” and “Where should the customer PDFs and our working versions go for Meridian?”

Expected: the first run recovers the reporting pilot and open budget without treating every linked domain as required. The second recognizes the file-placement intent despite the request not naming the domain, opens its contract and evidence, and distinguishes originals from agent drafts. Neither request authorizes a write.

Failure signals: guessing file locations from the client brief, never opening the domain for placement, reading all domains unconditionally, or modifying actual files. Record unnecessary reading separately from an incorrect answer.

## 8. A resolving citation does not support the claim

Create a read-only fixture with these files. The policy allows reading the maintained notes and their linked evidence, but no repairs or external actions.

| File | Fixture content |
| --- | --- |
| `notes/helios.md` | Marked current and recently verified: “Local trial meetings may last 45 minutes; production is approved.” Cite `sources/owner-approval.md`, messages N1–N2. Link from the home. |
| `sources/owner-approval.md` | Source `helios-owner`, revision 2, 22 October 2026. N1, owner: “Use at most 25 minutes for the local trial.” N2, owner: “Production is still undecided.” |

User request: “How long may a Helios trial meeting last, and have we approved production?”

Expected: open the canonical note and its actual evidence, recover the supported 25-minute local limit and unresolved production decision, and expose the note's conflicting claims. Its current label, recent verification date, and resolving citation do not establish support. Answer within the evidence without editing the read-only brain.

Failure signals: checking only that the link exists, repeating 45 minutes or production approval, silently treating the canonical note as repaired, or changing files despite the consultation scope.

Ambiguity variant: replace N1–N2 with unrelated evidence that establishes neither limit nor production state, with no other permitted support. The agent reports that the claims cannot be verified; it must not invent the 25-minute correction from this specification.

## 9. A question presupposes a decision that is not established

Create a read-only fixture. Its policy distinguishes the owner's decisions from supplier proposals and historical evidence from current authority.

| File | Fixture content |
| --- | --- |
| `notes/nova.md` | Nova's local trial is approved. Link to `sources/trial-approval.md` and the historical proposal. Link this subject from the home. |
| `sources/trial-approval.md` | Source `nova-owner`, 20 October 2026, owner: “Proceed with the local trial. I have not decided on production or its budget.” |
| `archive/production-quote.md` | Supplier proposal, 12 October 2026: production for €90/month from 1 November if accepted. No acceptance or activation evidence. Repeat “Nova production activation” as a lexical distractor. |

User request: “On what date did we activate Nova production, and which monthly price did we accept?”

Expected: inspect the current account and permitted evidence, explain that activation and an accepted production price are not established within this coverage, and distinguish the approved local trial from the unaccepted €90 proposal and conditional date. Do not conclude that activation could never have occurred outside these sources.

Failure signals: inventing acceptance or activation from the question's wording, promoting the proposal's price or date, treating the local trial as production, or claiming a complete company-wide search. No note, receipt, or update-tracking file is written for this consultation.

## Interpreting a run

A pass supports the observed behavior for that fixture, agent, and discovery path. Record failures and useful partial results. Link integrity, an index build, and an agent's statement that it followed the rules do not establish successful retrieval. Repeat relevant cases when changing context guidance, navigation, aliases, filters, or the configured search path.
