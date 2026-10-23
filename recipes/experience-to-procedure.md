# Recipe: turn experience into a reusable procedure

Use this recipe when a correction, failed attempt, or useful result may improve repeatable work. Keep the observation separate from the proposed lesson and the procedure someone can actually use. An isolated success can justify a narrow candidate; it does not establish a general rule.

This is a knowledge workflow, not permission to run tools, install skills, or change policy. Apply the private brain's existing access, retention, authority, and execution rules throughout. Use the [knowledge model](../docs/knowledge-model.md), existing [receipts](../templates/ingestion-log.md), and [reliability checks](../docs/reliability.md); no separate event store or required schema is needed.

## 1. Preserve the observation

Search for the subject, previous procedures, and related corrections before creating a note. Record only what is useful and permitted:

- The task and relevant input conditions, including tool or format versions when they matter.
- What was attempted, what was actually observed, and the expected result it differed from.
- A resolvable source or execution reference: version, relevant range, test input identifier, and output or failure, within retention policy.
- Known limits: an operator's report, retained execution output, and a result reproduced now provide different evidence.

Preserve failures and counterexamples that affect the lesson. Keep credentials, secret values, and unnecessary personal or source content out of notes, receipts, and test fixtures. A permitted locator or synthetic example can be sufficient; copying a sensitive input is not required to explain a correction.

## 2. State a candidate lesson

Write the smallest testable proposal that the observation supports. A short section in the canonical subject note can suffice; use the optional [procedure template](../templates/procedure.md) for a separate repeatable reference.

The candidate needs a trigger, checkable preconditions, an action, the result to check, and a bounded scope with exceptions. Link the observation and distinguish the explanation from the evidence. For example, “For this semicolon-delimited export with comma-decimal amount fields, parse those fields with the export's decimal convention” is testable. “Always replace commas in CSV files” overstates the evidence and risks corrupting another format.

Do not silently turn one person's preference, a source instruction, or an agent suggestion into an authorized operating rule. A proposed procedure carries no additional permission. When a genuine policy decision is needed, preserve it as unresolved and use the existing authority path; routine work within standing permissions needs no universal new approval step.

## 3. Try the candidate within permission

Choose a check proportionate to the consequence, variation, and cost. Use the environment's existing test or work path, preferably in a disposable scope. Check the result against an explicit expectation, not merely a successful command exit.

For a format correction, inspect both a matching example and a plausible case where the rule should not apply, such as comma-decimal French amounts and dot-decimal US amounts. A broader claim needs evidence across the conditions it claims to cover. Repeating the same input does not broaden that evidence. Include failure or boundary conditions when they affect safe use.

Record what actually happened:

| Check | Record | What it supports |
| --- | --- | --- |
| Executed trial | Input and environment/version, action actually run, expected and observed outputs, failure if any, evidence locator | Observed behavior for those conditions only |
| Simulation or walkthrough | Assumptions, predicted result, and unexercised dependencies | A proposed test or explanation; no claim of executed success |
| Model or peer critique | Reasoning and objections | Candidate improvement; no empirical validation by itself |

A report that a command ran is an observation attributed to its source; record whether the available evidence supports the claimed output. If execution is unavailable, unauthorized, interrupted, or inconclusive, retain a candidate and the missing check. Do not mark it usable merely to finish a queue.

## 4. Promote only the supported scope

Make the procedure usable only when the relevant trial supports its claimed conditions and the expected result, and remaining limits are explicit. Preserve the validation evidence and date. One small trial may support a deliberately narrow, low-consequence procedure; it cannot validate untested formats, environments, or production outcomes.

Use a few plain states only when they change behavior: **candidate** for an unvalidated proposal; **usable within stated conditions** for a supported procedure; **review due**, **superseded**, or **historical** as in the knowledge model. These can be prose labels rather than new fields. The label is not a substitute for checking evidence.

Keep candidates outside routine operating guidance under the brain's existing retrieval rules. A validated correction can update an existing canonical procedure without producing a duplicate. Retain the former behavior and reason where needed to understand the change; refresh dependent packs or summaries.

## 5. Retrieve and apply with its conditions

Save the procedure and receipt before ordinary retrieval readback. Ask a likely later-use question through the brain's entry point or configured search. Confirm that a reader finds the canonical procedure, evidence, and exceptions without the writer supplying its file path. Keep the receipt partial if that path fails; follow [continuity](../docs/continuity.md) to resume it.

At the next actual use, open the current procedure and verify its trigger and preconditions against the new task. State the relevant conditions with the recommendation or execution plan so a remembered action does not outlive its scope. If the input differs or a needed condition is unknown, do not apply the correction blindly: use the normal supported path, perform an authorized bounded check, or preserve the missing information.

Record a material failure, exception, or new condition in the existing receipt or canonical account. Routine successful repetitions need not create filler notes; preserve enough coverage when a later decision depends on them.

## 6. Revalidate or withdraw when evidence changes

Choose a relevant review trigger: a changed format or tool, conflicting result, changed domain rule, expired source access, or a date where appropriate. Review due means revalidation is needed for that use, not that the old observation became false.

When a material failure challenges the procedure's scope, stop presenting that affected action as usable until resolved. Preserve the evidence, mark the affected section for review or withdrawal, and narrow or replace it when supported. Link the replacement, update dependent views, and leave an explicit next step if unresolved. Do not erase valid history or revoke unrelated knowledge.

Exercise the workflow with the [fictional procedure checks](../examples/procedure-checks.md). Record actual runs separately from these scenario specifications.
