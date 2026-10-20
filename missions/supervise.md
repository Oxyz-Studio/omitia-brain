# Mission: supervise expected work

## Objective

Determine whether configured missions and their observation mechanisms are producing the expected, useful results. Make missed work and unknown state visible without mistaking intentional silence or pauses for failures.

## Context and authority

Read the private brain's entry point, policy, mission inventory, scheduling records, recent receipts, previous health observation, and applicable notification conditions. Select a bounded set of missions and source ranges according to their importance and expected rhythm.

Supervision does not authorize restarts, new credentials, source expansion, schedule changes, or external messages beyond existing grants. Use the available read-only evidence; record missing access and continue independent checks.

## Working brief

- Inspect the actual expected state: active, paused by policy, retired, manual, or not configured. A missing recurring run is only a failure when one was expected.
- Compare invocations with receipts and source coverage. Distinguish a runtime success, a completed review with no durable change, useful integration, partial work, and an inaccessible source.
- Inspect a useful sample of resulting knowledge and ordinary retrieval rather than relying only on counters or the writer's status.
- Check the age, source, and scope of the observation itself. A recent heartbeat is evidence of liveness, not proof of completed coverage; an old payload cannot establish current health.
- Check whether an expected receipt could be missed if this job or its scheduler stopped. Inspect the configured independent observation or human review when one is needed. Do not claim such a mechanism exists merely because the mission asks for it.
- Follow the user's notification and escalation policy. Keep healthy runs quiet when requested, preserve intentional pauses, and avoid repeated unchanged alerts unless the policy calls for them.

## Completion evidence

Save a dated observation using the optional [health status template](../templates/health-status.md) or the brain's existing format. Identify evidence examined, expected versus observed work, verified coverage, age limits or missing choices, unresolved findings, and the next action.

Distinguish the last attempt from the last useful result and from the last coverage review. Mark unobserved state unknown. An authorized non-destructive alert exercise can verify delivery; record the actual result separately from ordinary quiet-run evidence.

## Stop and recover

Stop within the budget. Leave bounded follow-up for missing or ambiguous evidence. Route knowledge gaps to [reconciliation](reconcile.md), routine repairs to [maintenance](maintain.md), and restoration to [recovery](recover.md) when authorized. Do not repeatedly retry a denied action or widen the mandate to make every indicator healthy.

See [reliability](../docs/reliability.md) and [scheduling](../docs/scheduling.md).
