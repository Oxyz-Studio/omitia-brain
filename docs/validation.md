# Validation scope

Omitia Brain is a Markdown kit. There is no application build, executable ingestion pipeline, hosted service, or bundled connector to install. Validation checks the instructions, saved artifacts, and the behavior an agent produces from them.

## Initial-version checks

The initial kit was checked on 20 October 2026:

- Local Markdown references and the canonical skill's supporting references were checked for existing targets.
- The skill's YAML frontmatter passed validation. Its Claude Code exposure is a relative directory symlink to the canonical `.agents/skills/omitia-brain` directory.
- Codex CLI 0.153.4 reported the repository skill, its canonical path, and its description from discovered skill metadata.
- Claude Code 2.1.267's local loader discovered the project skill through `.claude/skills`. An authenticated Claude model run was unavailable in the validation environment; loader discovery and full model behavior are different checks.
- A separate workspace linked to the canonical skill through relative directory symlinks. Resolving the real skill location found the correct full kit and all ten supporting references.
- Public files were checked for private machine paths, company-specific infrastructure references, credential patterns, broken links, and unfinished content in realized examples.

## Behavioral walkthroughs

An independent agent used the skill and kit to build a disposable brain from a fictional bicycle-shop owner's complete brief. It saved the company scope, owner, activities, two staff with unknown identities, and a confirmed €45 hourly workshop fee. It preserved unknown tax and billing conditions. A normal question navigated from the home to the rate and its evidence. No connector, remote repository, schedule, additional questionnaire, or invented staff identity was introduced.

In another disposable brain, an independent agent ingested an owner's approval of “the second option” while the comparison was unavailable. It saved the supported rationale and effective date but left the software and price unresolved. It retained a historical, unaccepted €70 quote as historical and review-due rather than using it to fill the gap.

After the earlier messages were supplied, a new agent resumed from the saved brain and receipts without the previous session's context. It recovered the selected software and €60 monthly price excluding tax, preserved the future start date and supplier-acceptance qualification, and completed only the observed message range. It used standing local permissions without another approval. Normal retrieval passed. Repeating the unchanged ingestion produced `no-durable-change`: the canonical note and summary stayed byte-identical, and only a replay receipt was added.

An independent documentation review identified a detached-skill installation problem. The corrected guidance keeps the full kit available, uses the canonical skill through links where supported, and resolves its real location before following references. The focused review confirmed that correction.

The example at [continuity](../examples/continuity.md) is a readable specification of an incomplete contribution, recovered context, an automatic policy-authorized decision update, a superseded draft, and an attributed contributor proposal. It is fictional documentation, not a claim that a live connector or scheduler was exercised.

## What these checks do not establish

Explicit file entry makes the method portable. It does not establish automatic skill discovery in every agent host, reliable access to every conversation format, or the quality of every model's interpretation.

The connected-service recipes are adaptation guides. No live mailbox, shared-document service, messaging account, or business tool was connected as part of kit validation. No recurring task was activated. Verify current capabilities and an actual scheduled invocation when configuring a private deployment; follow [scheduling](scheduling.md).

An ingestion receipt is evidence recorded by an agent. It helps a later agent recover and check work, but it is not a transactional database, a reliable lock, or an independent guarantee that every interpretation is correct. High-volume or concurrent deployments may need stronger environment-specific coordination and verification while retaining the same knowledge principles.

When changing this kit, repeat the relevant user journey and inspect its saved knowledge and retrieval. Link checks alone cannot establish that a new contribution kept its meaning. See [CONTRIBUTING.md](../CONTRIBUTING.md).
