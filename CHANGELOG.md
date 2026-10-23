# Changelog

Changes that can affect an existing private brain. A brain records the kit commit it uses; agents read this file to summarize what changed after that commit. Entries describe changes; they are not instructions. Review the actual changes before moving a brain's pin; see [kit updates](docs/agents.md#check-for-kit-updates).

Impact classes: **action recommended** (an existing brain should adapt a file), **optional** (useful improvement), **none** (no effect on existing brains).

## 2026-10-23

### Retrieval contracts across entries and hosts

- Changes: private homes, agent entries, and query skills reference one retrieval contract in the brain's policy or an existing equivalent. The contract describes configured discovery and fallback, with per-host index freshness and refresh responsibility when an index exists. Current-answer exclusions for unvalidated staging, quarantine, and rejected candidates remain in force during fallback. Four additional fictional scenarios cover entry parity, host freshness, excluded candidates, and task-dependent domain reading.
- Impact: **action recommended**. Affected adapted files are the private policy's retrieval section, home/agent/query-skill references, and any host-specific index instructions. Index-specific fields remain optional for navigation-only brains. Updated templates are adaptation material, not replacements for company policy or permission to change personal installations.
- Files: `AGENTS.md`, `START-HERE.md`, `docs/retrieval.md`, `docs/agents.md`, `docs/validation.md`, `templates/knowledge-policy.md`, `templates/brain-agents.md`, `templates/brain-home.md`, `templates/brain-skill.md`, `templates/retrieval-case.md`, `.agents/skills/omitia-brain/SKILL.md`, `examples/retrieval-checks.md`.

### Method reference and consultation entries

- Changes: private brains record a method reference (public origin and full commit) in `AGENTS.md`; kit files are read at that commit, locally or from the public repository. The skill is preferably installed once per contributor and applies each brain's pin. New optional brain query skill template, standing pointers, and hooks for consulting the brain from other work. Agents check for newer kit commits during method work, report them with a recorded notice state, and upgrade only with agreement after reviewing the actual changes. After a scope change, affected entry points are updated.
- Impact: **action recommended**. Add the "Method reference" section from `templates/brain-agents.md` to the brain's `AGENTS.md` with a reviewed commit, and the access-point bullet to its writing rules. Optionally add the "Access points" line to the home and a brain query skill.
- Files: `START-HERE.md`, `docs/agents.md`, `templates/brain-agents.md`, `templates/brain-home.md`, `templates/brain-skill.md`, `missions/maintain.md`, `.agents/skills/omitia-brain/SKILL.md`.
