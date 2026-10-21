# Mission: {name}

## Outcome

{The useful state this mission should produce, and how to verify it. This is an agent instruction, not an executable script.}

## Scope and authority

- Working folder / entry point: {explicit private brain path; no assumed current folder}.
- Sources and permitted ranges: {source records}.
- Applicable policy: {policy reference and actual permissions}.
- Requester / execution access identity / output audience: {distinguish the human or job principal, actual credentials' scope without secrets, and permitted recipients; model identity is not access authority}.
- Permitted changes: {notes, receipts, summaries, or other explicitly authorized destinations}.
- Exclusions: {out-of-scope data and actions}.

## Method

Read the entry point and relevant policy. Retrieve current notes and enough source history to understand each new claim. Integrate within the configured rules, preserve provenance, update affected summaries, and record incomplete items without inventing context. Reuse prior receipts to avoid duplicate work and to retry gaps. Preserve other contributors' edits.

{Add task-specific instructions, for example freshness checks, retention, batch limits, or how an authorized automatic conflict rule applies.}

## Runtime and completion

- Cadence / trigger and timezone: not configured.
- Existing scheduler / agent environment: not configured.
- Runtime or model identity and allowed fallback, when material to cost or reproducibility: not configured.
- Limits, retry, and overlap handling: not configured.
- Report destination and notification conditions: not configured.
- Evidence that scheduling is active: not configured.
- Scheduling identifier / management reference and pause or removal method: not configured.
- How a missing expected receipt is noticed, if unattended continuity is needed: not configured.

Persist changed knowledge and a partial coverage receipt. Use an ordinary retrieval question from the brain entry point or configured search to verify that a later run can find the canonical knowledge and its limits. Record readback evidence before finalizing a changed unit as `integrated`; retain partial coverage if retrieval fails.

Produce a run report with source coverage, actual useful changes, evidence, unresolved items, and next action. Distinguish a finished attempt from the last useful success. If required access or a runtime choice is missing, record it and finish independent work; do not claim the mission is active or complete without evidence.
