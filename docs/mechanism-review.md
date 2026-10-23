# Mechanism coverage and deployment checks

Design review: 21 October 2026. This map connects the knowledge lifecycle to contracts and deployment acceptance evidence. Optional mechanisms need not all be installed.

The review compared primary documentation, implementation and selected read-only evidence from a private company brain. No private records are published. Documented intent, code behavior, observed operation and fictional tests were assessed separately.

## Coverage map

| Mechanism | Public contract | Useful acceptance evidence |
| --- | --- | --- |
| Adaptive first use and later contributions | [Start](../START-HERE.md), [commands](commands.md), [direct contributions](../recipes/direct-contributions.md) | A complete brief works immediately; missing answers or connectors do not block unrelated scope; a colleague can resume from saved files. |
| Private workspace and portable agent entry | [Agents](agents.md), [governance](governance.md) | Company data stays separate; a new host loads the actual private instructions; canonical skill links resolve; the brain's method reference reaches the pinned kit version; consultation entries expose only approved metadata. |
| Authority, permissions, and source trust | [Governance](governance.md) | Existing grants are reused, suggestions stay attributed, and imported commands cannot grant permission. |
| Source access, transport, lifetime, and retention | [Sources](sources.md), [source record](../templates/source.md) | The executing identity can revisit the evidence; permitted captures and recovery limits are known. |
| External references without relocation | [External references](external-references.md) | A document stays at source; reference-only, consultation, and integration grants are distinct; another runtime does not invent access. |
| Source restrictions through derived knowledge | [Access boundaries](governance.md#preserve-access-boundaries-through-derived-knowledge), [access cases](../examples/external-access.md) | Authorized views protect metadata and content before retrieval; mixed-source outputs retain applicable restrictions; revocation reaches managed derivatives with prior-copy limits explicit. |
| Primary ingestion and optional event hooks | [Ingestion design](ingestion-design.md), [work discovery](work-discovery.md) | A missing hook does not hide activity in an accessible persisted source; ephemeral evidence has a permitted capture route or an explicit limit. |
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

The review preserved provenance, time, contradictions, partial coverage, retrieval readback and replay. It clarified primary discovery versus hooks, execution identity and source-version finalization, and added compact-context, supervision, rejection and recovery guidance. See the [changelog](../CHANGELOG.md) for later changes; optional mechanisms remain optional.

## Implementation habits deliberately excluded

- Clearing backlog or unreadable/truncated input as integrated; assuming stable IDs, titles or headers prove unchanged content.
- Treating counters, recent success, silence or written protections as semantic coverage, installed enforcement or working integration.
- Inferring permissions from suggestions or copying one installation's providers, thresholds, hierarchy and approval rules into the universal kit.

## Limits of the review

Use [validation](validation.md) for evidence actually obtained. Each deployment verifies its own hosts, integrations, alerts, access controls and restoration. A small brain can keep mechanisms manual or unconfigured, with relevant limits and next actions explicit.
