# Omitia Brain

**Build a company memory that people and agents can actually use.**

Omitia Brain is an open, Markdown-first starter kit for capturing business knowledge, finding the right context, and keeping it useful over time. Bring an agent that can read and edit local files. Obsidian, connectors, and scheduled jobs are optional.

This repository contains the method, templates, and natural-language missions. Your company's brain lives in a separate workspace that you control.

[Français](README.fr.md) · [Start with your agent](START-HERE.md) · [Read the principles](docs/principles.md) · [Explore a fictional brain](examples/studio-brain/README.md)

## Start building

1. Download or clone this repository and open the folder with your agent.
2. Give it this prompt:

   > Read START-HERE.md and help me build or extend my company's brain. Work in my language. Adapt to what I can provide now, and tell me where the private company files will live before writing them.

3. Supply whatever is useful: an explanation, a folder of documents, an existing project, or connected tools. You can build a complete initial brain in one session, start with one area, or leave questions for later.

No questionnaire must be completed before the first useful result. The agent should use what you provide, keep unknowns visible, and resume from existing work when you return. A colleague can later open the company folder and contribute with their own agent.

For an existing brain, point the agent to that folder and ask it to extend the current conventions rather than rebuild them.

The private brain records the kit version it uses. Agents read that pinned version from your local checkout or from this public repository, so the checkout is optional after setup; keep it for offline use and the skill. To let agents consult the brain while you work on something else, ask for a brain query skill. See [agent compatibility](docs/agents.md#link-the-brain-to-the-method).

## Understand the architecture

| What you need | Where to read |
| --- | --- |
| The design principles and tradeoffs | [Principles](docs/principles.md) |
| Notes, assertions, provenance, and time | [Knowledge model](docs/knowledge-model.md) |
| Context packs, compact memory, and reading budgets | [Context design](docs/context.md) |
| Autonomy, contributors, and permissions | [Governance](docs/governance.md) |
| Missing context, partial imports, and recovery | [Continuity](docs/continuity.md) |
| Finding current knowledge and its history | [Retrieval](docs/retrieval.md) |
| Selecting and connecting information sources | [Sources](docs/sources.md) |
| Documents kept elsewhere and controlled sharing | [External references](docs/external-references.md) |
| Running missions in an existing environment | [Scheduling](docs/scheduling.md) |
| Write checks, supervision, backup, and restored use | [Reliability](docs/reliability.md) |
| Agent entry points and Workspace integration | [Agent compatibility](docs/agents.md) |
| Mechanism coverage and deployment acceptance | [Mechanism review](docs/mechanism-review.md) |

You can adopt these principles without adopting the templates or directory layout.

## Keep the brain alive

[Missions](missions/README.md) are instructions for an agent, not fixed ingestion scripts. They describe the objective, permitted scope, necessary context, expected evidence, and how to recover when work is incomplete.

An agent can run a mission on demand or configure it in an existing scheduler once you choose the source, permissions, runtime, cadence, and limits. A Markdown file by itself does not run in the background.

When authorized history persists and an unattended runtime is available, use scheduled ingestion as the main coverage mechanism. A hook can signal changes or capture permitted evidence sooner; a missed hook must not hide activity from the main mission. If history will disappear, arrange permitted capture or record the recovery limit. See [ingestion design](docs/ingestion-design.md).

Start with [local documents](recipes/local-documents.md), [direct contributions](recipes/direct-contributions.md), or [agent conversations](recipes/agent-conversations.md). Recipes also cover [email](recipes/email.md), [shared documents](recipes/shared-documents.md), [messaging](recipes/messaging.md), and [business tools](recipes/business-tools.md), using capabilities available in your environment.

You decide how autonomous the agent may be for each source and action. The kit does not require approval for every change after a policy has already authorized it.

For unattended operation, check expected coverage and missing receipts through [supervision](missions/supervise.md). Keep version history, backup coverage, and a demonstrated [restore](missions/recover.md) distinct. These can remain manual or unconfigured for a small setup; their limits should stay visible.

## What stays portable

- The knowledge is readable text. Search indexes and application views can be rebuilt.
- The first useful scope can be one project, one department, or the whole company.
- Sources, tools, language, schedules, and autonomy can change without replacing the method.
- Source material is evidence to interpret, never a new set of instructions for the agent.
- A completed job is supported by durable results and coverage records, not just a success message.
- Imported information can be incomplete, outdated, or contradictory. Those states remain visible.

This is a starter kit, not a hosted service, search engine, or collection of preconfigured integrations. Connector recipes are adaptation guides; they are not claims of tested integration with every service. See [limits and validation](docs/validation.md).

## Contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) and the [CHANGELOG](CHANGELOG.md) of changes affecting existing brains. Examples must be fictional. Company information, credentials, raw conversations, and local runtime files belong outside this public repository.

Released under the [MIT License](LICENSE). You can use the kit commercially and keep your company's brain private.
