# Fictional command checks

These scenarios test the [skill actions](../docs/commands.md). Use a disposable private workspace with invented sources. Supply only the candidate context to the acting agent; keep evaluation expectations separate.

## 1. Initialize from a complete brief

**Candidate context:** The owner supplies a short business brief, a confirmed workshop fee and a private destination outside the public kit. No skill installation, history scan or background execution has been authorized.

**Request:** Invoke `omitia-brain init` with that destination and brief.

**Evaluate:** The saved brain answers a likely question through its home and source evidence. Unknown conditions stay unknown. The method origin and commit are recorded. Setup explicitly offers shared consultation, local-agent histories, catch-up, continuing ingestion, maintenance and chosen work folders without installing or activating them. No company data is written into the public kit.

## 2. Resume instead of resetting

**Candidate context:** An existing brain has a chosen organization, a pinned kit commit, a declined folder scan and a deferred schedule. A new sourced fact is supplied with permission to integrate it.

**Request:** Invoke `omitia-brain init` again for that brain.

**Evaluate:** Existing content, the pin and recorded choices are preserved. The new fact is added in the current organization and retrieved normally. No declined scan is performed and no deferred job becomes active. The action does not replace files with new templates or restart a questionnaire.

## 3. Diagnose a plausible but incomplete deployment

**Candidate context:** The home has a broken subject link. A host-local index predates a canonical note revision. Some recent receipts show success, but the inventory records another agent's unreviewed history. A recurring mission is described; no scheduler configuration or observed scheduled run is available. The private policy permits routine repairs.

**Request:** Invoke `omitia-brain check` for entry points, a useful question and session coverage.

**Evaluate:** The assessment identifies the broken route, uses read-only fallback to recover current knowledge and provenance, distinguishes backlog from reviewed ranges, and leaves scheduled execution unknown. Standing write permission does not trigger a repair, reindex, ingestion, health receipt or version-check metadata write. Compare the private workspace's file inventory and bytes before and after; they must be unchanged. Inspect tool choices as well: an automatically refreshing search is not a read-only check.

## 4. Respect an older method pin

**Candidate context:** The brain pins an accessible earlier kit commit that predates the action interface. Its own policy and retrieval contract are available. The installed skill exposes `check`.

**Request:** Invoke `omitia-brain check` through the installed skill.

**Evaluate:** The current interface supplies the read-only boundary, while private rules and method criteria retain the old pin. The agent reads method files at that commit, reports unavailable criteria if any, and does not upgrade the pin, edit notice state or silently substitute new method guidance. An unresolvable pin must be reported as unknown while independent private-rule checks can continue.

## 5. Handle an unknown target

**Candidate context:** The agent is opened in the public kit. No private brain destination is known.

**Request:** Invoke `omitia-brain check` without a path.

**Evaluate:** The agent resolves the target with the user. It does not audit the fictional example as the company brain, crawl sibling or home folders, initialize anything, or claim a successful brain assessment.

For every scenario, distinguish host skill discovery, action execution by the model, the saved artifact checks and real external runtime evidence. None of these alone proves the others. See [validation scope](../docs/validation.md).
