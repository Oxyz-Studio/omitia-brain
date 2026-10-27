# Reproducible metrics

Keep a maintained metric contract when it helps answer a recurring question consistently. A one-off question need not create another artifact. The brain preserves meaning, evidence, and provenance; an existing authorized calculator or query tool performs computation. This guide adds no calculation engine or default execution grant. Follow [governance](governance.md) for authority and access.

## Define what the number means

Use a section in a canonical note or the optional [metric template](../templates/metric.md); prose is sufficient. Record the details that determine the answer:

- **Identity:** stable metric ID, definition version, question answered, maintained owner, and effective period. State who can adopt definition changes.
- **Grain and population:** what one observation represents, stable entity identity and deduplication rule, inclusions, exclusions, and any weighting. Joins must not multiply observations at that grain.
- **Time:** event or date field selecting the population, explicit start-inclusive/end-exclusive bounds, and timezone. Resolve relative dates before execution.
- **Calculation:** exact numerator, denominator, aggregation, unit, and rounding stage and precision. Combine underlying totals and counts; do not average averages unless the contract explicitly calls for that weighting.
- **Unknowns:** treatment of missing or invalid inputs, distinct from zero. An empty denominator returns an unavailable result, never zero.
- **Evidence:** authoritative source and revision or snapshot, usable locators, observation time, freshness requirement, and applicable access dependencies.

Use [domain context](context.md#give-each-kind-of-context-its-role) for shared terms and the [knowledge model](knowledge-model.md) for assertion dates and sources. Do not silently choose between materially different definitions. Continue supported work and clarify the specific missing definition or input.

## Execute and retain the basis

Before reporting a calculated result, check definition, permitted population, freshness, and grain against the actual inputs. Preserve the executed calculator expression or query, its version, parameters and input references with revisions, returned value and unit, execution time, and a receipt or resolvable run reference. A proposed query or model-generated number is not executed evidence.

Retention follows the current action and source grants: a read-only check can report its calculation and evidence in the answer without saving a result or receipt. A metric definition grants neither execution nor retention. Reuse adequate existing execution evidence when applicable; another run is not required merely to repeat a dated result.

Repeated entity IDs with conflicting values require the applicable authority and revision rule; selecting an arbitrary row is not deduplication.

Partial inputs support only an explicitly qualified known subtotal or covered-population result, with coverage and exclusions stated. Do not present it as the complete metric. If completeness is unknown, say so.

When definitions or data change, retain the previous basis and effective scope, identify dependent results and views, then recompute or mark them for review. Use [continuity](continuity.md) for receipts and recovery and [retrieval](retrieval.md) to find and verify the current contract and result; repeating a stored number does not revalidate it.

## Compact fictional check

Metric `repair_elapsed_mean`, definition v1, owned by the fictional workshop coordinator, effective from 2026-04-01: unweighted mean elapsed minutes per completed repair ID. Select completion timestamps in `[2026-04-01T00:00, 2026-05-01T00:00)` in `Europe/Paris`; require valid start and finish, and deduplicate by repair ID before aggregation. Divide summed elapsed minutes by repair count; round only display to one decimal. Missing duration is excluded and reported; no repairs means unavailable.

The complete public fixture, revision 1, contains three April repairs: `R1 = 20`, `R2 = 40`, `R3 = 60` minutes. All timestamps meet the window. A parts join repeats R1 twice: `20, 20, 40, 60`.

Expected result: `(20 + 40 + 60) / 3 = 40.0 minutes`, covering 3/3 repairs. Averaging joined rows gives `35.0`, which fails the grain check. An execution receipt must identify this fixture revision, definition v1, the expression actually run and calculator version, and the returned result. Reproduce both cases with the existing permitted tool before claiming execution.
