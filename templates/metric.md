# {Metric name}

Use only when a recurring question benefits from a maintained definition. Adapt these prompts into prose or existing notes; no fixed schema is required. See [reproducible metrics](../docs/metrics.md).

## Definition

- ID / definition version / question: {stable identity, version, intended use}.
- Owner / authority / effective period: {maintainer, who adopts changes, when this definition applies}.
- Grain / population: {one observation, entity ID and deduplication, inclusion/exclusion and weighting}.
- Time: {selection field, start-inclusive/end-exclusive bounds, timezone}.
- Formula / unit / rounding: {numerator, denominator and aggregation, output unit, rounding stage and precision}.
- Missing or invalid inputs / empty denominator: {treatment distinct from zero; unavailable when denominator is empty}.
- Source / freshness / access: {authoritative source, revision or snapshot and locator, observed time, freshness requirement, policy dependencies}.

## Result and evidence

{Definition version; actual executed expression or query and its version; parameters and input locators with revisions; calculator or query tool version; returned value and unit; execution time and receipt/run reference. If unexecuted, label it as such. State coverage, exclusions and whether the result is partial or unavailable.}

## Changes and dependencies

{Previous definition or input basis, effective scope of the change, dependent results/views, and recomputation or review needed. Omit when unnecessary.}
