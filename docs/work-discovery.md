# Discover work and refine the brain

During initial setup or a requested expansion, offer the capabilities below explicitly. Do not wait for the user to know their names. Explain the useful result, show the proposed scope, and reuse choices already recorded. An offer is not an installed skill, a source grant, or an active job. Record accepted, deferred, declined, and unavailable options, with a revisit date or condition for deferrals, in the home's readiness record so later sessions resume rather than repeat onboarding. The session-start [`status` orientation](commands.md#status-orient-at-the-start-of-a-session) reads that record to surface what remains to do in each host.

Use the authorized material already supplied to produce useful knowledge while these choices remain open. Discovery, content reading, retaining sources, updating notes, installing a consultation entry, and running unattended jobs are distinct actions. Apply the existing policy to each; resolve only missing choices that affect the next action.

The interactive [`discover` action](commands.md#discover-preview-available-work-sources) uses these inventory criteria for a read-only preview: return findings and choices in the conversation without persisting them. Save an inventory only when explicitly requested and permitted; the setup/ingestion handover records below do not override that default.

## Offer consultation across agents

Offer a brain query skill shared by the agents the user uses, so work outside the brain can retrieve its knowledge. Keep one canonical brain-specific skill and expose it through supported links or short entry bridges; verify discovery separately in each intended host. The [agent guidance](agents.md#reach-the-brain-from-other-work) defines installation, metadata, audience, and read-only consultation. Do not silently edit personal configurations or promise that every host supports skills.

## Inventory agents and histories on authorized machines

Propose an inventory of **all locally used work agents on each machine the user authorizes**, not just the agent running this setup. Start with the user's known machines and tools and the host's permitted application or configuration inventory. Inventory access is not permission to read every conversation or inspect unrelated personal folders. An unlisted or unreachable machine remains outside observed coverage; remote access must already be authorized or separately chosen.

For each authorized machine/agent pair, record the agent identity, work scope, actual history location or native interface, available date range, session discovery method, reading and retention grants, and whether the intended unattended runtime can access it. Distinguish accessible, unavailable, excluded, and not yet checked. Do not store credentials or sensitive titles in a broadly visible inventory. A user recollection or detected installation is not proof that its sessions were read.

Offer two complementary operations:

- **Historical catch-up:** consider all accessible work sessions in the agreed machine/agent/project/date scope, including completed and still-open sessions, with explicit exclusions and bounded batches.
- **Continuing ingestion:** discover new sessions and changed versions, retry gaps, and periodically check the authorized agent inventory for newly used agents or moved histories. Use the [conversation recipe](../recipes/agent-conversations.md) and [ingestion design](ingestion-design.md), independent of end-of-session hooks.

Show the proposed scope before content collection: machines, agents, projects or session selection, dates, excluded personal material and secrets, retention, destination audience, budget, and cadence if requested. Ask only for missing choices. An authorization for all work sessions does not authorize personal sessions, secret retention, another machine, or arbitrary future source types. Record whether the grant includes newly discovered work agents within the approved boundary; otherwise propose adding them before reading their content.

Make coverage inspectable per machine and agent: discovery time and bounds, sessions/versions enumerated, reviewed ranges, integrated changes, reviewed no-change items, explicit exclusions, open gaps, and pending work. State the denominator and its limits. “12 of 12 enumerated work sessions reviewed in this source range” is useful; “all sessions ingested” is unsupported if another agent or machine is unchecked. A count alone does not prove complete message or semantic coverage. Keep only the identifiers the audience may discover, using the [source record](../templates/source.md) and [ingestion log](../templates/ingestion-log.md).

## Offer a bounded work-folder inventory

Propose inventorying the user's work folders, then scanning the folders they choose. Preview candidate roots and exclusions from supplied paths or authorized discovery before opening file contents. A selected file does not authorize siblings or parent folders. Listing filenames can itself reveal private metadata; establish the permitted discovery boundary first.

A whole-computer inventory or scan is a separate explicit choice, never the fallback for an unknown project path. Even with that choice, preview the roots, inaccessible areas, excluded personal locations, secret stores, credential files, and other agreed limits. Do not follow directory links, mounted volumes, cloud shortcuts, or nested repositories beyond the approved boundary without checking whether the grant covers their targets. Secret-bearing files are not material to collect merely because a broad scan was chosen.

Use the [local-document recipe](../recipes/local-documents.md) for the actual selected scan. Record supported formats, skipped or unreadable files and next actions; do not equate a directory listing with ingestion. Documents may stay at source rather than being copied into the brain.

## Distil projects, then ask useful questions

Considering every eligible source session is different from promoting every statement into company memory. Apply [selective distillation](principles.md#distil-selectively): retain reusable facts, decisions, reasons, constraints, relationships and methods with provenance. Keep collection, semantic review and canonical integration separate. A session can contribute to several subjects, or none; retaining an entire transcript is not required and must follow its retention grant.

Search existing project names, aliases, stakeholders and evidence before creating a project account. Create or enrich projects progressively when the sources establish a coherent identity and purpose, not one project per session, folder or agent. Link a project's observations to their actual source ranges; keep uncertain identity matches separate until resolved. Record goals, scope, decisions, dependencies and last verified state only as supported. A historical plan or confident agent statement does not establish that work is still active or that an action succeeded.

After reading a bounded batch, offer a short grouped set of targeted questions about material ambiguities, contradictory evidence, project identity or scope, and the present state of dated work. Attach the relevant source references and explain what an answer would settle. Do not ask the user to restate facts already supported by the sources or turn questions into a prerequisite for saving independent facts.

Save supported findings now, keep the affected conclusions partial or disputed, and record deferred questions with a resume point. A later user answer is new attributed evidence: reconcile it with the existing account, refresh affected views, and verify ordinary retrieval. Use [reconciliation](../missions/reconcile.md) for unresolved contextual dependencies.

## Offer concrete continuing work

Once the inventory makes scope visible, offer historical catch-up, continuing ingestion, and proportionate maintenance as separate choices. Describe what each would read, update, check and report. Prepare concrete mission proposals using the [scheduling contract](scheduling.md#record-the-scheduling-contract); activate only when scope, source/action permissions, runtime, cadence and limits are established. Reuse standing grants. If no unattended runtime is available, offer manual batches and record that continuing coverage is not configured.

The handover records the offers and user choices, actual observed coverage, useful project notes, open questions, consultation entries verified per host, and which jobs are merely proposed versus configured and observed. Test this route with the [work-discovery scenarios](../examples/work-discovery-checks.md).
