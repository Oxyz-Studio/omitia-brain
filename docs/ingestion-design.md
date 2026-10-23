# Ingestion design

Ingestion is agent work: discover authorized source changes, recover their context, compare them with existing knowledge, and leave useful notes and coverage receipts. A capture or successful transfer supplies material; it does not establish that the material was understood or integrated.

## One mission, several triggers

Use the same [ingestion mission](../missions/ingest.md) for manual requests, scheduled runs, and authorized event triggers. Keep one set of source registrations, permissions, receipts, and recovery rules. A new trigger should not create a second independent pipeline that races to update the same knowledge. Coordinate overlapping work using the existing environment's mechanism; see [scheduling](scheduling.md).

When recurrence is authorized, sources persist, and a suitable agent runtime can revisit them, scheduled ingestion is the main mechanism for maintaining coverage. Each run examines the registered sources within its budget, recognizes new or changed units, and carries incomplete work forward. Its discovery must work without an end-of-session hook. Manual ingestion remains valid when recurrence is unnecessary or unavailable.

During setup, explicitly offer historical work-session catch-up and continuing ingestion after an authorized [machine/agent inventory](work-discovery.md#inventory-agents-and-histories-on-authorized-machines). Initial catch-up and live coverage have separate observed checkpoints. Continuing work rechecks the permitted inventory for new agents and history locations as well as sessions; inclusion of new sources follows the existing grant or requires a missing scope choice. Full eligible-source review is not full transcript retention or automatic promotion of every claim into the brain.

## Select useful knowledge without a repeated save request

Use [proactive capture](proactive-capture.md) when the existing grant permits retention. Authorized ingestion selects reusable synthesis and resolution lessons from covered evidence even when no message explicitly asks to save them. The canonical reference routes those outcomes to the existing synthesis and procedure recipes and preserves read-only, consultation, evidence, and retention limits.

When configured, historical and continuing ingestion remain the main coverage mechanism. Inline capture can save useful knowledge sooner during ordinary work; it complements source discovery and historical review. Recognize its saved notes and receipts when the same source arrives later, completing only missing work under the shared contract. Neither inline capture, a hook, nor a skill guarantees that every source or conversation is covered.

## Hooks and captures are optional inputs

A hook may signal that a conversation changed or capture permitted evidence for later reading. It can reduce delay, but a missing hook event does not prove there was no source activity. The main mission checks source coverage through the available authorized history or change interface.

Source lifetime changes that design. If history will be unavailable when ingestion runs, a permitted export, supplied transcript, or capture before expiry is needed to preserve the relevant evidence. Choose retention and capture explicitly, or record that later recovery will be limited. A visible conversation does not establish unattended history access, and this kit does not install or verify a hook, connector, capture process, or scheduler.

## Collection and integration have different outcomes

Keep the evidence's source identity, version, and locator separate from the capture, transfer, and agent run that delivered it. The same source version can arrive through several routes. Recognize that overlap without creating duplicate assertions; inspect changed versions rather than treating every repeated source ID as already complete.

A capture, export, or connector can record what it made available and where collection stopped. The agent then interprets that material, retrieves necessary context, reconciles claims, and verifies the saved knowledge. Collection success must not finalize semantic integration. Use the outcomes and version-bound checkpoints in [continuity](continuity.md), with [quality and coverage checks](reliability.md).

## Keep operation verifiable

Record which source host or service holds the evidence and which runtime and access identity perform the mission. Apply the configured audience and retention rules to every retained copy and report; moving evidence between environments does not broaden permission. See [sources](sources.md).

Verify actual capabilities during private setup and distinguish a successful manual run, an enabled schedule, and an observed scheduled run. Use [supervision](../missions/supervise.md) when recurring work needs its coverage and recovery checked. No trigger or technical success removes the need for a durable receipt, supported knowledge, and a successful retrieval readback before integration is complete.
