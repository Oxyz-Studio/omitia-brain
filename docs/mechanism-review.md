# Mechanism coverage and deployment checks

Design review: 21 October 2026. This map checks that the starter addresses a complete knowledge lifecycle, from first use to recovery. It is a guide to the contracts and the evidence a deployment should seek, not a claim that every optional mechanism is installed.

The review compared the starter with primary documentation, implementation details, and selected read-only operational evidence from an established private company brain. Private records, infrastructure, source material, and business-specific rules are not published here. Documented intent, code behavior, observed operation, and fictional behavioral tests were considered separately.

## Coverage map

| Mechanism | Public contract | Useful acceptance evidence |
| --- | --- | --- |
| Adaptive first use and later contributions | [Start](../START-HERE.md), [direct contributions](../recipes/direct-contributions.md) | A complete brief works immediately; missing answers or connectors do not block unrelated scope; a colleague can resume from saved files. |
| Private workspace and portable agent entry | [Agents](agents.md), [governance](governance.md) | Company data stays separate; a new host loads the actual private instructions; canonical skill links resolve. |
| Authority, permissions, and source trust | [Governance](governance.md) | Existing grants are reused, suggestions stay attributed, and imported commands cannot grant permission. |
| Source access, transport, lifetime, and retention | [Sources](sources.md), [source record](../templates/source.md) | The executing identity can revisit the evidence; permitted captures and recovery limits are known. |
| External references without relocation | [External references](external-references.md) | A document stays at source; reference-only, consultation, and integration grants are distinct; another runtime does not invent access. |
| Source restrictions through derived knowledge | [Access boundaries](governance.md#preserve-access-boundaries-through-derived-knowledge), [access cases](../examples/external-access.md) | Authorized views protect metadata and content before retrieval; mixed-source outputs retain applicable restrictions; revocation reaches managed derivatives with prior-copy limits explicit. |
| Primary ingestion and optional event hooks | [Ingestion design](ingestion-design.md) | A missing hook does not hide activity in an accessible persisted source; ephemeral evidence has a permitted capture route or an explicit limit. |
| Incremental collection and source revisions | [Continuity](continuity.md), [ingest](../missions/ingest.md) | Receipts identify the source identity, actual version, examined range, gaps, and retained proof; identical delivery does not duplicate knowledge. |
| Context reconstruction and interrupted work | [Reconcile](../missions/reconcile.md), [continuity](continuity.md) | Ambiguous fragments stay partial; a later agent can recover their meaning and resume without the original session. |
| Canonical identity and discoverability | [Retrieval](retrieval.md), [note](../templates/note.md) | Names and aliases work through the real lookup path; a variant name does not create a second subject. |
| Claims, evidence, and uncertainty | [Knowledge model](knowledge-model.md) | Mixed assertions have appropriate evidence and scope; a collected source does not automatically become an established fact. |
| Valid time, freshness, and replaced knowledge | [Knowledge model](knowledge-model.md), [revalidate](../missions/revalidate.md) | Import time is separate from validity; overdue review is not falsehood; historical evidence is usable without becoming current policy. |
| Decisions, reasoning, and later results | [Decision](../templates/decision.md) | Alternatives and rationale remain recoverable; execution and results require their own evidence; learned patterns do not silently grant authority. |
| Task routing and bounded context | [Context design](context.md) | The current task selects the subject; links are followed for a reason; reading stops when the answer and limits are supported. |
| Compact runtime memory and pointers | [Context design](context.md#keep-runtime-memory-compact) | Durable orientation stays brief; dated state lives in notes; the pointed canonical destination is opened before reliance. |
| Packs, descriptive domains, procedures, and skills | [Context roles](context.md#give-each-kind-of-context-its-role) | Reading maps, definitions, and execution guidance have clear roles without mandatory extra folders; claimed tool readers are verified. |
| Derived views, links, and optional search indexes | [Knowledge model](knowledge-model.md), [retrieval](retrieval.md) | Summaries reflect changed canon; index scope and age are visible; filtered, unindexed, and forbidden material are distinguished. |
| Checks and actual enforcement | [Reliability](reliability.md) | Agent review, deterministic validation, and an installed gate are distinguished; a claimed gate accepts and rejects representative disposable cases. |
| Rejected candidates and safe changes | [Reliability](reliability.md#reject-a-change-without-damaging-current-knowledge) | Failed new content stays noncanonical; a failed edit leaves existing valid knowledge and concurrent contributions intact. |
| Shared writers and synchronization | [Governance](governance.md), [scheduling](scheduling.md) | Overlap is coordinated; latest versions are inspected; conflicts do not silently drop another contribution. |
| Real invocation, bounded work, and catch-up | [Scheduling](scheduling.md), [mission](../templates/mission.md) | An actual scheduled run uses the intended identity, scope, budget, receipts, and bounded retry behavior. |
| Independent supervision and notification | [Supervise](../missions/supervise.md), [health status](../templates/health-status.md) | Missing expected work and stale observations are detected; verified no-change scans and intentional pauses are treated appropriately; alert delivery has separate evidence. |
| Version history, backup, and restored use | [Reliability](reliability.md#separate-history-backup-and-restored-use), [recover](../missions/recover.md) | Recovery coverage and exclusions are known; an isolated restore passes normal retrieval without reviving obsolete permissions or jobs. |
| Maintenance and open questions | [Maintain](../missions/maintain.md), [consolidate](../missions/consolidate.md) | Important navigation and evidence defects are addressed; resolved questions reach canonical notes; remaining unknowns keep next actions. |
| Evaluation and proportionate evolution | [Validation](validation.md), [retrieval case](../templates/retrieval-case.md) | Positive and negative cases exercise the actual path; a more complex index is justified by measured failures and comparative results. |

## Improvements from this review

The starter already had strong contracts for provenance, temporal meaning, contradictory evidence, durable source coverage, partial ingestion, normal retrieval readback, and replay. Those contracts were retained.

This review made the primary ingestion and optional-hook relationship explicit; separated source location from unattended execution identity; tightened finalization to the source version actually read; added compact-memory and context-selection contracts; and added supervision, write-rejection, and recovery guidance. Optional templates and evaluation cases support those contracts without becoming onboarding requirements.

## Implementation habits deliberately excluded

- Treating an old backlog, an unreadable extract, or a failed transfer as successfully integrated merely to clear pending work.
- Assuming a stable identifier, repeated headers, or a repeated title establishes that content is unchanged.
- Treating a truncated digest as complete evidence or discarding pending material without recording the loss and its effect.
- Reading a fresh status, an old successful run, a source count, or zero error messages as proof of current semantic coverage.
- Treating a versioned protection as installed enforcement, a draft role description as an active agent, or a written domain contract as a working tool integration.
- Treating silence, repeated suggestions, or inferred preferences as authority to change permissions.
- Copying one installation's providers, thresholds, folder hierarchy, approval rules, or scheduler into a universal kit.

## Limits of the review

Coverage of a contract does not establish that every host, connector, model, or deployment implements it. Live integrations, alert routes, access controls, enforcement, and restoration need their own environment-specific evidence. Some mechanisms may remain manual or not configured by choice.

See [validation](validation.md) for the behavioral checks actually performed and their limits. A small useful brain does not need every row implemented on day one; it should state the relevant limits clearly and keep them recoverable as its scope grows.
