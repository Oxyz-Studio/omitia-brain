# Contributing

Contributions should improve a portable method that both a business user and a technical reader can use. Open an issue for a problem or submit a focused pull request with the observed behavior and the proposed improvement.

## Keep the boundary clear

- Public kit: principles, entry points, templates, natural-language missions, recipes, and fictional examples.
- Private brain: company notes, actual source records, contributor identities, ingestion receipts, logs, and runtime configuration. Keep them outside this repository.
- Existing tools: source access, authentication, execution, search, and scheduling. Do not add a new runtime or fixed ingestion scripts as an incidental documentation change.

Generalize from a concrete experience; do not copy a company's private policy or assume every company shares its structure, tools, approval preferences, or source authority.

## Canonical locations

Reference documentation is maintained in English under `docs/`. `README.fr.md` and `DEMARRER.md` provide the French entry. Agents work in the user's language, and company notes need not be English.

Keep each substantive rule in one reference and link to it from entry points or missions. Templates should support the rule without repeating an entire manual. Add a field only when it affects a real decision or a recoverable outcome.

The repository skill has one canonical directory at `.agents/skills/omitia-brain`. Expose that directory to Claude Code with the relative symlink `.claude/skills/omitia-brain`. Validate YAML frontmatter, relative references, and symlink discovery in both hosts when changing the skill; document a host limitation rather than claiming universal automatic discovery.

## Review before proposing changes

- Read changed material from the perspective of an unfamiliar user and a new agent.
- Check relative links and make sure no real local paths, credentials, source exports, or company details entered the patch.
- Walk through a relevant scenario in a disposable private workspace. Assess saved knowledge and retrieval, not just instruction compliance.
- For ingestion changes, exercise missing context, a changed source version, and interruption recovery where applicable.
- For scheduling guidance, distinguish a manual run from a naturally scheduled run and identify unverified parts.
- Run `git diff --check` and the skill frontmatter validator available in your agent environment when relevant. No build or package installation is required for the Markdown kit.

Describe the scenario and limitations in your contribution. Do not claim that a recipe was verified against a service merely because its Markdown was reviewed.

Contributions are provided under the repository's [MIT License](LICENSE).
