# Brain skill actions

Five actions route requests to the existing setup guide, source-discovery criteria and missions. Your agent executes them with its available tools.

## Invoke an action

Open the kit or make its full checkout available through the [canonical skill installation](agents.md#install-the-skill-once-per-contributor). Check discovery in the host you use.

| Action | Claude Code | Codex CLI / IDE |
| --- | --- | --- |
| Create or resume | `/omitia-brain init` | `$omitia-brain init` |
| Assess without changing the brain | `/omitia-brain check` | `$omitia-brain check` |
| Integrate selected input | `/omitia-brain ingest` | `$omitia-brain ingest` |
| Preview authorized source metadata | `/omitia-brain discover` | `$omitia-brain discover` |
| Repair within existing policy | `/omitia-brain maintain` | `$omitia-brain maintain` |

In another interface, select `omitia-brain` and request the action. Any file-capable agent can instead be asked to read `.agents/skills/omitia-brain/SKILL.md` and execute the named action; `init` also has the direct [START-HERE.md](../START-HERE.md) entry.

Add inputs and scope in ordinary text: `ingest ../exports/session.md — brain ../company-brain`, `discover ../work — filenames and history metadata only`, or `maintain ../company-brain — links in project notes`. Paths are data, not shell fragments or permission to scan adjacent folders.

Reuse a known private target and policy. Resolve a missing brain destination before ingestion or repairs, and a missing discovery scope/audience before enumeration; do not search sibling/home folders for them. Discovery may preview an explicitly permitted scope before brain setup, without creating a workspace. For an existing brain, establish its policy and permitted view before discovering subject or source metadata.

The action interface uses the installed checkout; missions and method criteria stay at the private pin. Report missing pinned files and continue only where private rules and available evidence suffice, without substituting current methods or moving the pin. None of these actions installs a skill, connects a new source or activates recurring work merely from its name.

One skill supplies these actions, avoiding generic host commands such as `/init`. See the host interfaces for [Claude Code](https://code.claude.com/docs/en/skills) and [Codex](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills). Discovery alone does not establish correct execution.

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

## `ingest`: integrate selected source material

Use the private brain's [ingestion mission](../missions/ingest.md) and the relevant [source recipe](sources.md). The request selects a contribution, document, conversation or bounded registered source set. Reuse its grants and receipts; register new material only within the requested source/action scope. A link authorized only for reference or live consultation cannot be distilled by this action.

Read enough context, find the existing subject, select durable knowledge and preserve evidence, uncertainty and relevant dates. Save coverage and perform normal retrieval readback before finalizing, following [continuity](continuity.md); a reviewed no-change result needs a receipt, not a filler note. Source revisions and interrupted work resume through that same contract, without duplicate knowledge.

Historical catch-up is this action with explicit machines, agents, projects/date range, exclusions and a batch budget. If source discovery or access is unresolved, propose the missing bounded scope instead of launching a machine-wide search. Distinguish historical backlog from current coverage and carry gaps forward. Recurrence is separate [scheduling](scheduling.md) work.

Return what was integrated or left partial, exact examined versions/ranges, evidence and retrieval results, and the next continuation. Counts describe observed coverage, not every history on every machine.

## `discover`: preview available work sources

Use [work discovery](work-discovery.md) at the brain's pin, where applicable, to inventory authorized agents/history locations or selected work-folder metadata. Reuse recorded exclusions and choices. Permission to enumerate metadata is distinct from reading bodies: source names, paths, dates and counts can themselves be restricted. If the available tool would return source bodies or follow a target outside the grant, do not invoke it for this metadata-only preview; report the limit.

By default, return the bounded inventory in the conversation: what was checked, accessible, excluded, unavailable or unknown, the observed denominator, and proposed ingestion batches or missing choices. An installed agent or discovered session is not proof that its content was read. Do not open documents/transcripts, follow links or mounts beyond scope, ingest, install, configure jobs, or write notes, receipts, choices, inventories or kit-update tracking metadata.

If the user explicitly asks to save the inventory, first establish the private destination and write permission, then use its existing source records. That request authorizes only the selected inventory write, not content collection, installation, scheduling or update-tracking writes. The setup guide's persistent handover requirements do not override this action's default preview mode.

## `maintain`: repair a bounded part of the brain

Run the private brain's [maintenance mission](../missions/maintain.md). Reuse the requested scope, recorded mission budget and existing repair grants. Without a specific pass, state a small scope based on recent changes or check findings; do not silently turn routine upkeep into a full source/history scan.

Diagnose, repair routine issues within policy, verify the saved result through ordinary retrieval and leave a durable receipt identifying changes, evidence, unresolved issues and continuation. Consolidation, revalidation or reconciliation can use their existing contracts when the scope and permissions cover them. A configured index can be refreshed only with the actual recorded procedure and permission; otherwise retain the permitted fallback and report the limitation.

Unlike `check`, this action can write authorized repairs. It cannot broaden ingestion, connect services, alter source/retention/access policy, edit personal configuration, move the method pin or create/change jobs to finish the pass. Missing authority blocks only the affected action; continue independent permitted work. Report what was actually repaired and tested rather than declaring every control healthy.
