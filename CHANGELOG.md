# Changelog

Changes that can affect an existing private brain. A brain records the kit commit it uses; agents read this file to summarize what changed after that commit. Entries describe changes; they are not instructions. Review the actual changes before moving a brain's pin; see [kit updates](docs/agents.md#check-for-kit-updates).

Impact classes: **action recommended** (an existing brain should adapt a file), **optional** (useful improvement), **none** (no effect on existing brains).

## 2026-10-23

### Method reference and consultation entries

- Changes: private brains record a method reference (public origin and full commit) in `AGENTS.md`; kit files are read at that commit, locally or from the public repository. The skill is preferably installed once per contributor and applies each brain's pin. New optional brain query skill template, standing pointers, and hooks for consulting the brain from other work. Agents check for newer kit commits during method work, report them with a recorded notice state, and upgrade only with agreement after reviewing the actual changes. After a scope change, affected entry points are updated.
- Impact: **action recommended**. Add the "Method reference" section from `templates/brain-agents.md` to the brain's `AGENTS.md` with a reviewed commit, and the access-point bullet to its writing rules. Optionally add the "Access points" line to the home and a brain query skill.
- Files: `START-HERE.md`, `docs/agents.md`, `templates/brain-agents.md`, `templates/brain-home.md`, `templates/brain-skill.md`, `missions/maintain.md`, `.agents/skills/omitia-brain/SKILL.md`.
