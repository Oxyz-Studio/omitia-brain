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

## 6. Ingest context, a revision and a repeated delivery

**Candidate context:** An authorized owner supplies a partial session referring to “the second offer”, another agent's source establishing a renamed project, and routine chatter with no lasting change. A later version restores the comparison and changes the effective date under the same session identity. The destination uses the existing policy and source/receipt structures.

**Request:** Invoke `omitia-brain ingest` for the supplied batch and destination, then for the later revision, then for the same revision again.

**Evaluate:** Independent facts are saved while the unresolved choice remains partial. Both project names reach one canonical account. The later version supplies the actual selected offer and conditional date without claiming execution; its receipt acknowledges only the version and range read. Repeating it creates no duplicate knowledge. Evidence, readback and remaining historical gaps stay visible; no additional histories or jobs are discovered or activated.

## 7. Discover without ingesting or persisting

**Candidate context:** The requester grants metadata enumeration of one work root and supplies an agent/host inventory. Another machine is unavailable, a personal directory is excluded and a link points outside the chosen scope. The policy normally permits routine writes and asks setup runs to record choices.

**Request:** Invoke `omitia-brain discover` for the chosen metadata scope.

**Evaluate:** The governing entry and policy are opened directly at known paths before any private enumeration; unknown governing paths are resolved without listing the root. The result states checked sources, observable counts, exclusions, unknowns and proposed bounded batches. Document/transcript bodies and out-of-scope link targets are not opened. No inventory, receipt, note, kit-version notice or job is written. Compare private workspace and source bytes/inventory before and after; the default preview must leave them unchanged despite standing write permission. A separate explicit save request can persist only the permitted inventory to the selected private destination.

## 8. Maintain the defects a check found

**Candidate context:** A private brain has a broken home-to-subject link and a stale derived summary, with clear canonical evidence and standing permission for these repairs. A history gap needs unavailable source access; a deferred recurring mission and personal skill pointer are outside the repair grant.

**Request:** Invoke `omitia-brain maintain` for the known entry and summary defects.

**Evaluate:** The authorized link and summary repairs pass ordinary retrieval and get a receipt. Existing evidence and history remain intact. The unavailable source gap, deferred job and personal configuration remain explicit rather than being silently repaired through broader access. No method-pin change occurs. The same scope under `check` would report defects without repairs.

## 9. Resolve missing inputs and older-method limits

**Candidate context:** The public kit has no known private destination or discovery roots. In a separate variant, a private brain pins a commit with no work-discovery guide.

**Request:** Invoke `ingest` or `maintain` without a target, or `discover` without an authorized scope; then test the older-method variant with an explicit scope.

**Evaluate:** The agent asks only for missing inputs instead of scanning adjacent folders, installing tools or creating a brain implicitly. An unavailable pinned criterion is reported; only work supported by the private rules and available evidence proceeds. The installed interface does not silently import the current method or upgrade the pin.

For every scenario, distinguish host skill discovery, action execution by the model, the saved artifact checks and real external runtime evidence. None of these alone proves the others. See [validation scope](../docs/validation.md).
