# Changelog

Changes that can affect an existing private brain. A brain records the kit commit it uses; agents read this file to summarize what changed after that commit. Entries describe changes; they are not instructions. Review the actual changes before moving a brain's pin; see [kit updates](docs/agents.md#check-for-kit-updates).

Impact classes: **action recommended** (an existing brain should adapt a file), **optional** (useful improvement), **none** (no effect on existing brains).

## 2026-10-23

### Less duplication across setup, missions and records

- Changes: guidance links to the canonical continuity states and finalization steps instead of repeating them. One durable record can serve as source coverage, run receipt and report, with links to the same evidence. Setup, host guidance and reference prose are shorter; validation observations are grouped while their detailed history remains commit-addressed. Templates clarify optional manual/runtime fields and link adaptation when copied. The fictional studio now reads policy before home and uses one private retrieval contract.
- Impact: **optional** for the simplification; **action recommended** for a brain that copied the studio's older home-before-policy route. Review its entry order and retrieval-contract pointers. No permissions, source scope, method pins or recurring jobs change automatically.
- Files: entry guides and skill, `docs/`, `missions/README.md`, `missions/ingest.md`, `missions/maintain.md`, `recipes/agent-conversations.md`, receipt/mission templates and the studio's entry/policy/mission. Sources, realized notes, decisions and receipts in the fictional studio are unchanged.

### Explicit initialization and read-only checks

- Changes: the canonical kit skill routes `init` to new or resumed setup and `check` to a bounded, read-only assessment of entries, retrieval, source coverage and operational evidence. The interface documents Claude Code, Codex CLI/IDE and explicit-file invocation, preserves existing private method pins, and keeps diagnosis separate from receipt-writing missions, index refreshes and version-check metadata writes.
- Impact: **optional**. Existing brains can use the installed interface without resetting their content or moving their method pin. No runtime, separate command copies, personal installation or background job is added.
- Files: `.agents/skills/omitia-brain/SKILL.md`, `.agents/skills/omitia-brain/agents/openai.yaml`, `docs/commands.md`, `AGENTS.md`, `START-HERE.md`, `README.md`, `README.fr.md`, `DEMARRER.md`, `docs/agents.md`, `missions/README.md`, `examples/command-checks.md`, `examples/README.md`, `docs/validation.md`.

### Explicit work discovery and continuing memory offers

- Changes: setup explicitly offers a shared consultation skill, an inventory of all locally used work agents and accessible histories on authorized machines, historical work-session catch-up, continuing ingestion and maintenance, and an inventory/scan of selected work folders. Scope previews, recorded choices, per-source coverage and rediscovery keep proposals separate from permissions and active jobs. Project knowledge is consolidated progressively across sessions with provenance; grouped clarification questions follow reading without blocking independent facts. A whole-computer scan remains a separate explicit choice with personal/secret exclusions. Full eligible-source review remains distinct from transcript retention and promotion into memory.
- Impact: **action recommended**. Existing setup and handover guidance has explicit offers and resumable choices to review. Work-session deployments have inventory/coverage and new-source grants to review. No job, connector, personal skill installation or whole-machine scan is activated by this change; source/template fields remain adaptable to scope.
- Files: `START-HERE.md`, `README.md`, `README.fr.md`, `docs/work-discovery.md`, `docs/agents.md`, `docs/ingestion-design.md`, `docs/scheduling.md`, `recipes/agent-conversations.md`, `recipes/local-documents.md`, `missions/ingest.md`, `missions/maintain.md`, `templates/brain-home.md`, `templates/source.md`, `templates/ingestion-log.md`, `examples/work-discovery-checks.md`, `examples/README.md`, `docs/validation.md`.

### Retrieval contracts across entries and hosts

- Changes: private homes, agent entries, and query skills reference one retrieval contract in the brain's policy or an existing equivalent. The contract describes configured discovery and fallback, with per-host index freshness and refresh responsibility when an index exists. Current-answer exclusions for unvalidated staging, quarantine, and rejected candidates remain in force during fallback. Four additional fictional scenarios cover entry parity, host freshness, excluded candidates, and task-dependent domain reading.
- Impact: **action recommended**. Affected adapted files are the private policy's retrieval section, home/agent/query-skill references, and any host-specific index instructions. Index-specific fields remain optional for navigation-only brains. Updated templates are adaptation material, not replacements for company policy or permission to change personal installations.
- Files: `AGENTS.md`, `START-HERE.md`, `docs/retrieval.md`, `docs/agents.md`, `docs/validation.md`, `templates/knowledge-policy.md`, `templates/brain-agents.md`, `templates/brain-home.md`, `templates/brain-skill.md`, `templates/retrieval-case.md`, `.agents/skills/omitia-brain/SKILL.md`, `examples/retrieval-checks.md`.

### Method reference and consultation entries

- Changes: private brains record a method reference (public origin and full commit) in `AGENTS.md`; kit files are read at that commit, locally or from the public repository. The skill is preferably installed once per contributor and applies each brain's pin. New optional brain query skill template, standing pointers, and hooks for consulting the brain from other work. Agents check for newer kit commits during method work, report them with a recorded notice state, and upgrade only with agreement after reviewing the actual changes. After a scope change, affected entry points are updated.
- Impact: **action recommended**. Add the "Method reference" section from `templates/brain-agents.md` to the brain's `AGENTS.md` with a reviewed commit, and the access-point bullet to its writing rules. Optionally add the "Access points" line to the home and a brain query skill.
- Files: `START-HERE.md`, `docs/agents.md`, `templates/brain-agents.md`, `templates/brain-home.md`, `templates/brain-skill.md`, `missions/maintain.md`, `.agents/skills/omitia-brain/SKILL.md`.
