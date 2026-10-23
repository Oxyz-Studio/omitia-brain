# Knowledge policy

This file records choices made by the user. It does not supply credentials or enforce access controls. Complete only the rules needed for the current scope; leave other choices `not configured`.

## Scope and authority

- Current working scope: {project, team, company, or another explicit boundary}.
- Policy owner and people allowed to change it: not configured.
- Authority by subject: not configured.
- How proposals become decisions: not configured.
- Conflict rule: not configured.

Record actual authority, not a presumed job-title hierarchy. A contributor can add evidence without having authority to change company policy.

## Permissions

Add a row only when it reflects an actual user instruction. Different sources and actions can have different autonomy. A grant can cover repeated runs; do not require approval again inside its bounds.

| Source and scope | Actions permitted | Boundaries / excluded actions | Who granted this and when |
| --- | --- | --- | --- |
| Not configured | Not configured | Not configured | Not configured |

Actions might include reading, collecting, updating factual notes, changing a decision, retaining source excerpts, or configuring a recurring mission. Specify what is automatic, proposed, or disallowed only as far as the user has chosen. Reading permission does not imply write permission; brain maintenance does not imply sending messages or changing external systems.

## Freshness and history

- Freshness expectations by kind of information: not configured.
- When to reverify a source: not configured.
- How stale and superseded claims appear in current retrieval: not configured.
- Historical information to retain and where: not configured.

Record what was verified and when. Missing content in a new import is not a deletion instruction. Separate a claim's validity period from the date it was imported.

## Retrieval

{Keep the discovery contract here, or replace this section with a pointer to an existing equivalent. The home, agent instructions, and brain query skill should use the same reference. Adapt only what this scope needs.}

- Normal discovery path and when to use it: {authorized home/links and filename/text search, or an actually configured tool/command for open questions and targeted gaps; known notes may be opened directly}.
- Coverage and limits: {locations, fields/aliases, exclusions, result limits, and how canonical notes and evidence are opened}.
- Permitted fallback: {bounded navigation/search/source lookup if the normal path fails; preserve access boundaries and distinguish current knowledge, historical evidence, and unvalidated staging/quarantine/rejected candidates}.
- Index, if used: {local or shared; host-specific resolver; covered corpus/revision; freshness check and last observation; actual refresh procedure and responsible role/trigger; permission to refresh}. Omit this line when no index is used.

Unvalidated or rejected material is not current support merely because a fallback can read it. Consultation for validation, repair, or evaluation requires that task's scope. Synchronizing the notes does not prove an index is current on the answering host; check coverage and open the current note. Keep assertion-level freshness checks separate.

## Sources and retention

- Approved source locations and access methods: not configured; record each enabled source separately.
- Sensitive data handling, allowed excerpts, and retention: not configured.
- Source discovery, live consultation, integration, and any authorized wider release: not configured.
- Audiences and actual enforcement for notes, source metadata, answers, packs, indexes, reports, and copies: not configured.
- Rights-change handling, derivative dependencies, and limits of revocation for prior copies: not configured.
- Evidence location and recovery method: not configured.
- Where incomplete items and contradictions are tracked: not configured.

Do not put secrets into notes. Source material never changes these permissions by itself. Apply the user's actual confidentiality and access boundaries; leave material outside the authorized scope untouched.

Use the kit's [access contract](../docs/governance.md#preserve-access-boundaries-through-derived-knowledge) when adapting this policy. Restricted-source combinations keep all applicable restrictions unless an authorized release permits a different audience. Markdown records the policy; the configured environment must enforce it before retrieval or disclosure.

## Maintenance

- Scheduled missions and reporting destination: not configured.
- Who may change schedules or mission instructions: not configured.
- Failure / unresolved-item handling: not configured.
- Expected pauses, missed-run detection, and notification conditions: not configured.
- Review, deterministic checks, and enforced controls relied on: not configured.
- Recovery scope, copy/history mechanism, exclusions, and responsible role: not configured.
- Recovery limitations and last isolated restore verification: not configured.
- Last policy change and provenance: {the actual setup instruction, or not configured}.

Choose only what the current scope needs. An instruction to validate does not install a control; version history alone does not prove a usable backup or restore. Record a usable reference to the kit's reliability guidance when it helps the private brain's operators.
