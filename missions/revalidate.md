# Mission: revalidate time-sensitive knowledge

## Objective

Check whether selected knowledge is still supported, then make its current reliability visible. A verification deadline is a reason to check; it is not proof that a statement has become false.

## Context and authority

Read current governance, source registrations, applicable freshness rules, relevant reference notes, and the previous run receipt. Select claims because they are due for verification, depend on a changed source, or matter to a current use. Avoid checking every note on every run.

Use only authorized sources and actions. A source becoming inaccessible does not authorize new credentials, a different connector, or an external message.

## Working brief

- Identify the claim, its scope, the evidence previously used, and why it is being checked.
- Prefer an appropriate current source of truth for volatile operational state. A remembered invoice status or inventory quantity cannot substitute for a current authorized lookup when a decision needs live data.
- Retrieve enough evidence to compare like with like. A change in product, region, contract period, or definition can make two statements appear contradictory when they are not.
- When supported, record the verification time, supporting source or source version, and the next check rule if one is useful.
- When replaced, record the new claim and its effective scope, link the earlier version to its replacement, and update affected summaries.
- When unresolved, distinguish overdue verification, unavailable evidence, conflicting evidence, and an unsupported claim. Preserve the last known fact with an appropriate warning instead of inventing a current value.
- Treat source silence carefully. No mention in a partial export is not a deletion event; absence can be evidence only when the source contract and actual coverage justify it.

An authorized agent may mark a claim as stale or superseded without a human gate when policy permits. A policy governing company decisions still applies to claims that would change doctrine or commitments.

## Completion evidence

Leave a receipt identifying the claims checked, evidence used, verification outcome, affected notes and summaries, unresolved dependencies, and the next check or resolution path.

Read the updated reference note through the normal retrieval path. Ensure a future answer can distinguish the current supported claim from historical or unverified material. An updated date without fresh evidence is not successful revalidation.

## Stop and recover

Respect the configured budget and source rate limits. Queue remaining claims with a reason and a useful priority; do not extend a schedule or broaden access to finish the batch.

If a source is temporarily unavailable, record a bounded retry path under the existing policy. Repeated failures should become visible through the reporting mechanism rather than silently renewing a verification date.

See [source management](../docs/sources.md), [retrieval](../docs/retrieval.md), and [the knowledge model](../docs/knowledge-model.md).
