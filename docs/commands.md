# Start and check a brain

The kit skill offers two actions executed by your agent with its available tools.

## Invoke an action

Open the kit or make its full checkout available through the [canonical skill installation](agents.md#install-the-skill-once-per-contributor). Check discovery in the host you use.

| Host | Start or resume | Inspect without changing the brain |
| --- | --- | --- |
| Claude Code | `/omitia-brain init` | `/omitia-brain check` |
| Codex CLI or IDE extension | `$omitia-brain init` | `$omitia-brain check` |
| A skill selector in another interface | Select `omitia-brain`, then ask for `init`. | Select `omitia-brain`, then ask for `check`. |
| Any agent that can read files | “Read START-HERE.md and initialize or resume my private brain.” | “Read docs/commands.md and check my private brain without changing it.” |

Append the private brain path and scope, such as `check ../company-brain — retrieval and session coverage`. Paths are data, not shell fragments. Resolve an unknown target with the user; do not crawl adjacent folders or assess this kit or its examples as the private brain.

One skill supplies both actions, avoiding generic host commands such as `/init`. See the host interfaces for [Claude Code](https://code.claude.com/docs/en/skills) and [Codex](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills). Discovery alone does not establish correct execution.

## `init`: create or resume useful memory

Follow [START-HERE.md](../START-HERE.md), honoring an existing brain's policy, permitted view and method pin. Resume saved work without resetting files or choices; a new brain records the setup commit.

Use authorized input to save useful knowledge and demonstrate retrieval. Make the guide's [work-discovery offers](work-discovery.md) explicit, without implying installation or recurring permission. Return the private location, usable result, evidence, remaining choices and resume point; report only capabilities actually configured and verified.

## `check`: a bounded, read-only assessment

Return a bounded assessment in the conversation. Read governing instructions and policy, establish requester, access identity and answer audience, then open the permitted content. Read method criteria at the private pin. This interface uses the installed checkout without upgrading that pin; missing method files are reported while private-rule checks continue.

Use the requested scope and budget; otherwise inspect entry points, up to three retrieval questions and five recent receipts or source units. Report the sample and unobserved scope; do not infer exhaustiveness or launch broad discovery to fill gaps.

| Area | Evidence to inspect |
| --- | --- |
| Entry points and method | Governing entry, policy, home and consultation entry reach the same retrieval contract. Method origin and full commit are resolvable, or their absence is explicit. Check affected links and routes without loading the whole brain. |
| Retrieval | Ask representative questions through ordinary discovery and reopen the canonical notes and provenance. Check freshness on this answering host if an index exists. Use the permitted file fallback if the index is stale, unavailable, or its search path would write. No index is valid for a navigation-only brain. |
| Work sources and coverage | Compare the recorded agent/machine inventory and source versions or ranges with available receipts. Separate historical backlog, new arrivals, inaccessible sources and deliberate exclusions. A clean queue or a recent run alone does not establish coverage of every agent. |
| Knowledge quality | On the selected sample, compare important claims and integration outcomes with readable source evidence. Distinguish decisions, proposals, execution reports and unresolved interpretation. An unavailable source leaves the claim unverified. |
| Continuing work | Compare declared missions with actual configuration and recent useful results where read access exists. Preserve intentional pauses; distinguish proposed, configured and observed scheduled execution. A mission file or manual success does not prove a background job. |
| Access and recovery | Check available audience, backup and recovery evidence relevant to the scope. A label does not prove enforced access; backup existence does not prove a restore. Mark unobserved controls unknown. |

Use only tools with a read-only path. Do not rebuild or refresh an index, ingest sources, update notes or receipts, save a health observation, record kit-version checks, install a skill, change configuration or activate a job. Standing permission for routine writes does not widen this diagnostic action. If a tool automatically refreshes an index or persists results, choose a read-only alternative or mark the check unavailable. A report can be saved separately if the user explicitly asks; keep that write outside the default check.

Consult [retrieval](retrieval.md), [work discovery](work-discovery.md) and [reliability](reliability.md) at the brain's pin as needed. Do not execute mutating missions for this assessment; [maintenance](../missions/maintain.md) and [supervision](../missions/supervise.md) have separate write/receipt contracts. Repairs require separate requested work under private policy.

Report conclusion, findings, evidence, scope and next actions, with date/host when relevant to freshness. Distinguish **verified**, **partial**, **unknown**, **not configured**, **intentionally paused** and **not applicable** instead of a misleading overall score. Report an observed kit-version difference without changing the pin or tracking metadata.
