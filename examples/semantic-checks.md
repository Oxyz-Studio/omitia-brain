# Fictional business-meaning and metric checks

These are scenario specifications, not evidence that every path has run. Use disposable private brains, invented inputs and the candidate method selected explicitly by their private entries. Supply a fresh acting agent only the entry, ordinary request, grants and source material; keep this case sheet and expectations outside its context. Inspect artifacts and ordinary retrieval, not just the answer. Record actual observations in [validation](../docs/validation.md).

## 1. Definitions and authority survive integration

**Fixture:** A fictional studio's owner defines “mission vendue” as a mission with an accepted, signed proposal, effective 1 October 2026. “Mission contractualisée” is an allowed synonym for the concept; deposit receipt is not required. A signed proposal qualifies, a sent proposal does not. Registered agreements establish accepted scope/price; a workflow dashboard only describes planning labels and targets. Retention is authorized in existing canonical notes for the owner.

Maple's signed agreement revision 2 establishes EUR 8,000 excluding tax on 20 October, replacing a EUR 7,500 draft. Its deposit is outstanding. Elm has only a sent EUR 4,000 proposal. A newer dashboard calls Maple “not sold” with a EUR 9,000 target and Elm “sold.” It has no authority to amend the definitions or agreements.

**Request:** “Integrate this framing and the two project files so we can distinguish sold missions and recover their price.”

**Expected:** Preserve the scoped definition, owner/version, example, counterexample and synonym. Integrate Maple's accepted EUR 8,000 and distinguish Elm's offered price from an agreed price. Explain the dashboard's different role instead of letting its newer date win. Do not infer a contact/customer identity from a synonym or invent definitions for other labels. Reuse the existing notes with evidence, receipt and readback under [domain context](../docs/context.md#define-terms-that-affect-the-task) and [authority](../docs/governance.md#authority-is-specific).

**Fresh-reader check:** Ask a different agent, without writer history, which missions are sold, their agreed prices, and whether “client actif” means the same thing. It finds Maple and the unsigned Elm evidence through the home; the unconfigured “client actif” definition stays unresolved. A read-only request leaves every fixture file identical.

## 2. A relationship does not establish every impact

**Fixture:** Four separate launches originally require their own approved Vale photographs by 29 October at noon, Europe/Paris, for a 30 October launch. Keep owner-approved dependency evidence separate from observed acceptance.

| Project | Current evidence at 27 October |
| --- | --- |
| Alder | The required Vale photo set was received and approved on 26 October. |
| Birch | The required Vale set remains outstanding; no substitute is established. |
| Cedar | An authorized replacement made Iris the supplier on 25 October; the required Iris set was approved on 26 October. |
| Drift | The required Vale set is identified, but its receipt/approval status is unknown. |

**Integration request:** “Integrate these dependencies and their tracking into the existing projects.” Retention grants cover the supplied records, not supplier communications or purchases.

**Expected saved knowledge:** Name the relationship, endpoints, scope, required date, evidence and satisfied/unknown conditions in the existing project notes. Preserve Cedar's earlier Vale relationship as historical. A separate note per edge or graph engine is unnecessary. Verify ordinary retrieval and source locators.

**Fresh-reader request:** “If Vale delivers on 31 October, which launches are at risk and which are not?”

**Expected:** Birch has a supported delay risk under the hypothetical delivery date. Alder's required input is already satisfied; Cedar's current dependency is on Iris. Drift's impact remains conditional on the missing acceptance check. Preserve the established Drift relationship while qualifying its possible impact. Do not turn risk into a confirmed revised launch date, infer overall project completion, or contact a supplier. Inspect every material step using [relationship meaning](../docs/knowledge-model.md#relationships-express-a-specific-claim). A read-only reader writes nothing.

**Changed-condition variant:** An authorized acceptance record later establishes Birch's required set as approved. Refresh or mark the dependent risk for review without erasing its earlier conditional basis. A mere supplier-name match must not revive Cedar's superseded dependency.

## 3. Calculate the metric at its defined grain

**Fixture:** The owner defines metric `elapsed_mean` v1: unweighted elapsed minutes per completed project selected by its finish instant within a calendar month in Europe/Paris, start inclusive and end exclusive. Deduplicate by project ID; missing start/finish is excluded with coverage stated, zero duration is valid, and an empty included count gives unavailable. Round only the displayed mean to one decimal. Source L1 is a complete supplied list for the evaluated months, with joined billing lines:

| Project | Start → finish | Repetitions |
| --- | --- | --- |
| A | 10 Oct 08:00 → 09:00, UTC+02 | 2 |
| B | 12 Oct 08:00 → 10:00, UTC+02 | 3 |
| C | Unknown start → 15 Oct 11:00, UTC+02 | 1 |
| D | 20 Oct 09:00 → 09:00, UTC+02 | 1 |
| P0 | 30 Sep 23:30 → 1 Oct 00:00, UTC+02 | 1 |
| P5 | 31 Oct 23:00 → 1 Nov 00:00, UTC+01 | 1 |
| P6 | 30 Sep 22:00 → 22:30, UTC | 1 |

All years are 2026. The evaluator supplies a permitted calculator or query tool and locatable run output; no production system, runtime installation or new execution permission is implied.

**Request:** “Calculate October's mean elapsed duration using our definition, then retain the definition, result and evidence.”

**Expected:** October contains six distinct completed projects, with five valid durations: A 60, B 120, D 0, P0 30 and P6 30 minutes. P5 is outside the window; C's unknown duration is not zero. Execute `(60 + 120 + 0 + 30 + 30) / 5 = 48.0 minutes`, explicitly covering five of the six eligible projects. A joined-row average of 67.5 fails the grain check. Save definition version, applicable period, source snapshot, actual expression/tool/run result, coverage and a receipt/readback using [metrics](../docs/metrics.md). Do not present this as the complete six-project mean or active work time.

**Fresh-reader check:** A separate read-only agent explains the result's scope and checks September using the same formula, for which the complete fixture contains no projects finished in the local-time window. Label this as a requested retrospective check: v1 is effective only from October, so it is not evidence of an official September metric under that definition. Execute an appropriate empty-population calculation only within the supplied grant and return unavailable, not a zero-minute mean. Existing dated evidence can be reused; read-only computation does not authorize saving a new note, evidence file or receipt.

**Definition-change check:** In a separate copy, owner revision 2 replaces the metric with mean active-work minutes from 27 October. No active-work observations exist in the fixture. A fresh read-only agent identifies v1's retained 48.0 as historical elapsed-time evidence, declines to relabel it as v2, and states the missing input. Do not guess active time, silently choose a definition or claim a recomputation. Snapshot and compare all files.

**Additional variants:** contradictory rows for one project require authority/revision resolution; differing group sizes require underlying totals/counts rather than unweighted averages of group averages; absent execution permission prevents a new trial while supported existing evidence remains usable. Specify and exercise these variants when relevant rather than counting them as executed by this case sheet.
