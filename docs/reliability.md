# Reliability and recovery

A usable brain needs evidence that its knowledge can be found, its unfinished work remains visible, and meaningful changes can be recovered. Choose controls according to the brain's value, workload, and available environment. A small brain can use manual checks and recoverable copies; unattended operation may need stronger coordination and supervision.

## Know what a check establishes

Three kinds of assurance serve different purposes:

| Check | What it can establish | Limit |
| --- | --- | --- |
| Agent review | Meaning, authority, source context, and whether a summary preserves important qualifications. | A plausible interpretation can still be wrong. |
| Deterministic check | A specific property such as a resolvable local link, a required field, or a configured sensitive-data pattern. | Passing does not prove meaning, complete evidence, or confidentiality against every possible disclosure. |
| Enforced gate | A configured environment prevents an operation when a selected check fails. | A supplied script or written instruction does not prove that the gate is installed, active, or applied to this operation. |

Use the checks already appropriate to the environment. Do not introduce a fixed schema or new service merely to complete a checklist. Record the scope examined, exclusions, check version when relevant, and actual result. A missing or failed validator is different from rejected content; neither is a passing check.

When relying on a gate, inspect its effective configuration and exercise a representative accepted and rejected operation in a disposable scope. Repeat the relevant assurance after moving to another environment or changing the gate. Agent instructions, installed controls, and observed enforcement are separate evidence.

## Reject a change without damaging current knowledge

Prepare consequential changes in a recoverable form and compare with the latest saved version before applying them. Follow the [collaboration rules](governance.md) when another contributor may edit the same subject.

If a new candidate fails the selected checks, keep it outside the current canonical account until corrected or explicitly excluded. A draft or restricted staging area can serve this purpose. Preserve its permitted source reference, failure reason, and next action; do not mark it integrated to clear a queue.

If a proposed update fails, preserve the existing valid note and isolate or discard only the rejected change under the user's policy. Do not move an established canonical note into quarantine, replace a whole folder from an old snapshot, or undo another contributor's work. Inspect versions and reconcile when targeted recovery would overlap their changes.

Staging and quarantine do not make sensitive content safe to collect or retain. Apply the same access and retention rules there. Keep error reports free of secret values and unnecessary source content. Record enough to distinguish an invalid candidate, a validator failure, and an unresolved policy question.

After a valid update, save its provenance and receipt, refresh affected views, and perform normal retrieval readback. A successful format check alone does not complete ingestion. See [continuity](continuity.md).

## Observe useful work and missing work

Track the signals needed to explain the actual state:

- Last expected invocation and last attempt completed, when recurrence is configured.
- Last verified source coverage and any uncovered ranges or inaccessible sources.
- Last useful result and the receipt that supports it.
- Age and scope of the health observation itself.
- Open failures, incomplete items, and their next action or dependency.
- Whether the mission is expected to run, deliberately paused, retired, or not configured.

No new input and `no-durable-change` can be healthy outcomes. A long time since the last note edit does not prove inactivity: inspect recent reviewed coverage. Conversely, a fresh heartbeat or successful invocation does not establish that the expected source ranges were read or their meaning preserved.

An unavailable source, missing expected receipt, or old health observation must remain visible as an uncertainty or failure under the chosen policy. Do not display a reassuring state merely because no error was reported. Include the observation time and scope so a reader can assess the result.

For unattended work that needs timely failure detection, choose a way to notice silence that does not depend solely on the same job and scheduler being healthy. An existing independent monitor or a planned human review may be enough. Record who or what checks, what evidence it expects, and how a missing signal becomes visible. This kit does not install that mechanism.

Exercise an authorized, non-destructive failure case and verify the configured reporting path. A successful quiet run and a delivered failure alert are different proofs. Respect the user's notification conditions and audience, including quiet healthy runs and intentional pauses. Repeated observations of the same unresolved issue need not generate repeated messages unless the chosen escalation policy calls for them.

Use the [supervision mission](../missions/supervise.md) and optional [health status template](../templates/health-status.md). The [scheduling guide](scheduling.md) covers invocation, overlap, retries, and the first natural scheduled run.

## Separate history, backup, and restored use

Version history makes changes reviewable and can help undo mistakes. A backup provides a recoverable copy under a chosen failure scenario. A successful restore demonstrates that the needed material can actually be recovered and used. These are different claims. A Git remote can be part of a backup strategy; its presence alone does not establish coverage of ignored files, separately retained evidence, or operational configuration.

Choose what needs recovery according to the user's scope and retention policy: canonical notes, policy, source references and permitted evidence, receipts and unresolved items, and the information needed to inspect or rebind missions. Derived indexes can usually be rebuilt. Credentials belong in an appropriate access mechanism, not in notes to make a backup appear complete.

Record the chosen copy or history mechanism, covered material, exclusions, access dependencies, retention, responsible role, and acceptable recovery limitations. Independence from the original storage, frequency, and tolerated loss depend on the user's needs; do not assume an existing remote copy satisfies them.

Test restoration into an isolated destination when authorized. Confirm that recovered notes, policy, receipts, and evidence agree, then use an ordinary question to retrieve the knowledge and its limits. Reading an archive listing or checking its checksum is useful evidence of a narrower property; it does not prove a usable restoration.

Record what was restored, from which version, what was tested, and what remains untested. A never-tested or old recovery path should be described that way. Restore under the current access and retention policy: do not recreate material that must remain deleted, silently revive removed permissions, or reactivate retired jobs.

Use the [recovery mission](../missions/recover.md) for a restore rehearsal or an actual incident. A rehearsal does not authorize changes to live storage or services.

## Keep maintenance proportional

Useful structural signals include broken evidence links, important notes unreachable from entry points, duplicated claims, oversized notes that obscure current answers, and unresolved items that have lost their next action. Qualify these findings by impact and inspected scope. A long historical note or an intentionally isolated source is not automatically defective.

When a question is resolved, place the supported answer in its canonical account, refresh affected views, and link the pending item to its resolution using the brain's chosen history mechanism. Preserve only the remaining unknown when the answer is partial. Do not treat a queue's shrinking count as proof that knowledge improved.

Keep an index's covered corpus and build age distinguishable from source coverage and claim validity. Before adding a more complex search or graph system, identify observed retrieval failures and compare a candidate with the existing path on representative questions. Include qualifications, evidence resolution, historical versus current answers, and appropriate uncertainty when evidence is missing. Assess cost and latency where they matter. A working process or a small smoke test does not establish better knowledge quality.
