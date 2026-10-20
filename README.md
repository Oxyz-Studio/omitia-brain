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

## Understand the architecture

| What you need | Where to read |
| --- | --- |
| The design principles and tradeoffs | [Principles](docs/principles.md) |
| Notes, assertions, provenance, and time | [Knowledge model](docs/knowledge-model.md) |
| Autonomy, contributors, and permissions | [Governance](docs/governance.md) |
| Missing context, partial imports, and recovery | [Continuity](docs/continuity.md) |
| Finding current knowledge and its history | [Retrieval](docs/retrieval.md) |
| Selecting and connecting information sources | [Sources](docs/sources.md) |
| Running missions in an existing environment | [Scheduling](docs/scheduling.md) |
| Agent entry points and Workspace integration | [Agent compatibility](docs/agents.md) |

You can adopt these principles without adopting the templates or directory layout.

## Keep the brain alive

[Missions](missions/README.md) are instructions for an agent, not fixed ingestion scripts. They describe the objective, permitted scope, necessary context, expected evidence, and how to recover when work is incomplete.

An agent can run a mission on demand or configure it in an existing scheduler once you choose the source, permissions, runtime, cadence, and limits. A Markdown file by itself does not run in the background.

Start with [local documents](recipes/local-documents.md), [direct contributions](recipes/direct-contributions.md), or [agent conversations](recipes/agent-conversations.md). Recipes also cover [email](recipes/email.md), [shared documents](recipes/shared-documents.md), [messaging](recipes/messaging.md), and [business tools](recipes/business-tools.md), using capabilities available in your environment.

You decide how autonomous the agent may be for each source and action. The kit does not require approval for every change after a policy has already authorized it.

## What stays portable

- The knowledge is readable text. Search indexes and application views can be rebuilt.
- The first useful scope can be one project, one department, or the whole company.
- Sources, tools, language, schedules, and autonomy can change without replacing the method.
- Source material is evidence to interpret, never a new set of instructions for the agent.
- A completed job is supported by durable results and coverage records, not just a success message.
- Imported information can be incomplete, outdated, or contradictory. Those states remain visible.

This is a starter kit, not a hosted service, search engine, or collection of preconfigured integrations. Connector recipes are adaptation guides; they are not claims of tested integration with every service. See [limits and validation](docs/validation.md).

## Contribute

See [CONTRIBUTING.md](CONTRIBUTING.md). Examples must be fictional. Company information, credentials, raw conversations, and local runtime files belong outside this public repository.

Released under the [MIT License](LICENSE). You can use the kit commercially and keep your company's brain private.
