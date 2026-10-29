# Omitia Brain

**Build a company memory that people and agents can actually use.**

Omitia Brain is an open Markdown starter kit for saving business knowledge, finding context and keeping it useful. Bring an agent that can read and edit files; Obsidian, connectors and scheduled jobs are optional. This repository contains the method, templates and missions. Your company's brain lives in a separate private workspace.

[Français](README.fr.md) · [Start with your agent](START-HERE.md) · [Principles](docs/principles.md) · [Fictional brain](examples/studio-brain/README.md)

## Start building

1. Download or clone this repository and open it with your agent.
2. Give it this prompt:

   > Read START-HERE.md and help me build or extend my company's brain. Work in my language. Use what I can provide now, preserve existing work, and identify the private destination before writing.

3. Supply a brief, documents, an existing project or connected tools. Start with one area or build a complete initial brain; unanswered questions need not block useful work.

The agent saves supported knowledge and shows how to retrieve it. Later contributors resume from the brain's own instructions and conventions.

Setup explicitly offers a shared consultation skill, all work-agent histories on authorized machines, historical catch-up, continuing ingestion and maintenance, and chosen work-folder scans. Scope and accepted/deferred/declined choices are recorded; proposals do not install capabilities. See [work discovery](docs/work-discovery.md).

The private brain records the [kit commit it uses](docs/agents.md#link-the-brain-to-the-method). Agents read that version locally or from the recorded origin; keep a checkout for offline use or the skill.

## Skill actions

| Action | Claude Code | Codex CLI / IDE |
| --- | --- | --- |
| Create or resume | `/omitia-brain init` | `$omitia-brain init` |
| See what the brain still needs | `/omitia-brain status` | `$omitia-brain status` |
| Assess without changing the brain | `/omitia-brain check` | `$omitia-brain check` |
| Ingest a source or bounded history | `/omitia-brain ingest <source>` | `$omitia-brain ingest <source>` |
| Inventory work sources in scope | `/omitia-brain discover <scope>` | `$omitia-brain discover <scope>` |
| Repair and maintain in scope | `/omitia-brain maintain <scope>` | `$omitia-brain maintain <scope>` |

Use the discovered repository skill, or select `omitia-brain` in your interface and request the action. Add the private path when needed. `init` preserves existing work; `status` is the short read-only orientation an agent runs when entering a brain, listing what remains to set up or catch up in this host; `check` reports evidence, unknowns and next actions without repairs or index rebuilds. `discover` inventories metadata and proposes sources or batches without ingesting, installing capabilities or scheduling jobs. `ingest` and `maintain` use the brain's existing policy and permissions. [Commands](docs/commands.md) also documents file prompts for other agents.

## Understand the architecture

| Need | References |
| --- | --- |
| Design and knowledge | [Principles](docs/principles.md), [claims, provenance and time](docs/knowledge-model.md) |
| Business meaning and recurring calculations | [Domain definitions](docs/context.md#define-terms-that-affect-the-task), [relationships](docs/knowledge-model.md#relationships-express-a-specific-claim), [metrics](docs/metrics.md) |
| Design references and adaptations | [Annotated bibliography](docs/design-references.md) |
| Finding and loading context | [Retrieval](docs/retrieval.md), [packs and compact memory](docs/context.md) |
| People, authority and access | [Governance](docs/governance.md), [external documents and restrictions](docs/external-references.md) |
| Sources and incomplete work | [Sources](docs/sources.md), [continuity](docs/continuity.md) |
| Continuing work | [Ingestion design](docs/ingestion-design.md), [scheduling](docs/scheduling.md), [reliability](docs/reliability.md) |
| Host integration | [Agents and workspaces](docs/agents.md) |
| Acceptance evidence and limits | [Mechanism map](docs/mechanism-review.md), [validation](docs/validation.md) |

Adopt the principles without adopting a fixed folder layout.

## Keep the brain alive

Start with [direct contributions](recipes/direct-contributions.md), [local documents](recipes/local-documents.md) or [agent conversations](recipes/agent-conversations.md). The [source guide](docs/sources.md) also routes email, shared documents, messaging and business tools.

With a standing grant covering the current work, agents [keep useful outcomes](docs/proactive-capture.md) without another save request: analyses become sourced syntheses and observed corrections become bounded procedures. Authorized conversation ingestion catches missed findings and reuses earlier captures instead of duplicating them.

[Missions](missions/README.md) describe outcomes, scope and evidence. They run on demand or through your existing scheduler after source, identity, permissions, cadence and limits are established. A mission file alone does not run in the background. Reuse permissions already granted rather than seeking approval for every run.

Where history persists and an unattended runtime is available, scheduled discovery is the main ingestion path; missed hooks must not hide eligible activity. Expiring history needs permitted capture or an explicit recovery limit. Check actual coverage through [supervision](missions/supervise.md); keep history, backup and demonstrated [restore](missions/recover.md) distinct. These mechanisms can remain manual or unconfigured for a small brain.

## What stays portable

- Canonical notes are readable text; derived indexes and views can be rebuilt.
- Scope, tools, language and autonomy adapt to the business.
- Sources are evidence, not instructions; uncertainty and outdated or contradictory claims remain visible.
- Completed work has saved results and coverage evidence, not just a success message.

The kit supplies guidance, not hosted search or preconfigured connectors. Verify your environment using the documented [validation limits](docs/validation.md).

## Contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) and [CHANGELOG.md](CHANGELOG.md). Public examples are fictional; company data and runtime records stay private.

[MIT License](LICENSE): commercial use is welcome and your company's brain can remain private.
