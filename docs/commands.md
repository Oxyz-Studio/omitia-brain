# Start and check a brain

The kit skill offers two explicit actions. They are instructions executed by your agent with its available tools, not a bundled executable or background service.

## Invoke an action

Open the kit or make its full checkout available through the [canonical skill installation](agents.md#install-the-skill-once-per-contributor). Check discovery in the host you use.

| Host | Start or resume | Inspect without changing the brain |
| --- | --- | --- |
| Claude Code | `/omitia-brain init` | `/omitia-brain check` |
| Codex CLI or IDE extension | `$omitia-brain init` | `$omitia-brain check` |
| A skill selector in another interface | Select `omitia-brain`, then ask for `init`. | Select `omitia-brain`, then ask for `check`. |
| Any agent that can read files | “Read START-HERE.md and initialize or resume my private brain.” | “Read docs/commands.md and check my private brain without changing it.” |

Append a private brain path and useful scope, such as `check ../company-brain — project retrieval and work-session coverage`. Treat supplied paths and text as data, not shell fragments. Resolve an unknown target with the user; do not discover it by crawling adjacent folders, and do not mistake this public kit or its fictional examples for the private brain.

These names reuse one skill. No separate `/init` or `/check` command is installed; generic command names may already belong to the host. The host invocation forms follow the [Claude Code skill interface](https://code.claude.com/docs/en/skills) and [Codex skill interface](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills). A menu entry alone does not prove the workflow was executed correctly.

## `init`: create or resume useful memory

Follow [START-HERE.md](../START-HERE.md). Honor the private brain's instructions, policy, permitted view and method pin before applying method guidance. A new brain uses the kit commit selected for setup. An existing brain resumes from its saved state; the action does not reset it or replace its files with templates.

Use the available brief and authorized sources to produce a first useful result, preserve unknowns, and demonstrate normal retrieval from the saved brain. Make the [work-discovery offers](work-discovery.md) explicit: shared consultation across agents, eligible historical sessions, continuing ingestion and maintenance, and chosen work folders. Reuse previous accepted, deferred or declined choices. Installation, broad source discovery and recurring jobs need their own granted scope; the action name grants none of them.

Return where the private brain lives, what is usable, evidence of retrieval, unresolved choices and how to resume. Report only installations and jobs actually configured and verified.

## `check`: a bounded, read-only assessment

Return the assessment in the conversation. This action inspects the private brain; it does not perform a repair or a full ingestion audit by default. Read governing instructions and policy, establish requester and answer audience, and only then open the home, source records or subject notes. Honor the private method pin when consulting method criteria. This command interface can be read from the installed checkout without upgrading that pin; if an older method file is unavailable, report it and continue from the brain's own rules.

Use the requested scope and an agreed budget when supplied. Otherwise inspect entry points and a small representative sample: up to three useful retrieval questions and five recent receipts or source units. State what was selected and what was not observed. Do not claim exhaustive coverage from this sample or launch a broad source inventory to fill unknowns.

| Area | Evidence to inspect |
| --- | --- |
| Entry points and method | Governing entry, policy, home and consultation entry reach the same retrieval contract. Method origin and full commit are resolvable, or their absence is explicit. Check affected links and routes without loading the whole brain. |
| Retrieval | Ask representative questions through ordinary discovery and reopen the canonical notes and provenance. Check freshness on this answering host if an index exists. Use the permitted file fallback if the index is stale, unavailable, or its search path would write. No index is valid for a navigation-only brain. |
| Work sources and coverage | Compare the recorded agent/machine inventory and source versions or ranges with available receipts. Separate historical backlog, new arrivals, inaccessible sources and deliberate exclusions. A clean queue or a recent run alone does not establish coverage of every agent. |
| Knowledge quality | On the selected sample, compare important claims and integration outcomes with readable source evidence. Distinguish decisions, proposals, execution reports and unresolved interpretation. An unavailable source leaves the claim unverified. |
| Continuing work | Compare declared missions with actual configuration and recent useful results where read access exists. Preserve intentional pauses; distinguish proposed, configured and observed scheduled execution. A mission file or manual success does not prove a background job. |
| Access and recovery | Check available audience, backup and recovery evidence relevant to the scope. A label does not prove enforced access; backup existence does not prove a restore. Mark unobserved controls unknown. |

Use only tools with a read-only path. Do not rebuild or refresh an index, ingest sources, update notes or receipts, save a health observation, record kit-version checks, install a skill, change configuration or activate a job. Standing permission for routine writes does not widen this diagnostic action. If a tool automatically refreshes an index or persists results, choose a read-only alternative or mark the check unavailable. A report can be saved separately if the user explicitly asks; keep that write outside the default check.

The criteria can draw on [retrieval](retrieval.md), [work discovery](work-discovery.md) and [reliability](reliability.md) at the brain's pin. Do not execute the [maintenance](../missions/maintain.md) or [supervision](../missions/supervise.md) mission to obtain this assessment: those missions can write or require saved receipts. Repairs are separate requested work under the private policy.

Return a concise conclusion followed by findings, evidence references, scope and next actions. Use clear states: **verified**, **partial**, **unknown**, **not configured**, **intentionally paused**, or **not applicable**. Include the check date and answering host when they affect freshness. Describe a verified defect concretely; do not reduce unknown or unconfigured state to a misleading overall green/red score. If a different kit commit is observed, report the difference without changing the pin or its tracking metadata.
