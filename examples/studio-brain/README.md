# Northstar Bike Studio brain

This is a fully fictional brain for a two-person bicycle repair studio. It covers only the launch of a weekday repair service. It was initialized by Mira Chen; Luca Moreau can contribute workshop observations through his own agent.

## Start here

Read [agent instructions](AGENTS.md), the [knowledge policy](KNOWLEDGE_POLICY.md), and the [source registry](SOURCES.md). Use the minimum relevant notes for the task.

- [Current repair launch](notes/repair-launch.md): weekday appointments and the current service price.
- [Booking decision](decisions/booking-platform.md): BookLane was selected; earlier alternatives remain available.
- [Weekend proposal](notes/weekend-proposal.md): Luca's suggestion, not a company decision.
- [Pricing draft history](notes/pricing-draft-history.md): stale material retained to explain the earlier discussion.
- [Ingestion log](INGESTION_LOG.md): source coverage, retryable gaps, and integration results.

## Setup state

Setup is complete for this small launch scope. The team has not attempted to document its entire business. A second contributor can add relevant evidence within the policy without restarting onboarding.

The brain has local fictional conversation sources. No mailbox, live booking system, or external connector is connected. Source connectors and retention outside this example are not configured. The [weekly review mission](missions/weekly-review.md) is written but has no active schedule. This brain is already usable for launch preparation.

The latest reviewed input is 15 October 2026. The last useful change was on 14 October: the agent recovered the missing options, recorded the owner's booking decision, and integrated the confirmed €45 service price. See the [latest receipt](receipts/2026-10-15.md). The dates describe this example's snapshot; they are not a claim of present-day freshness.

The reusable kit is available [two levels above this folder](../../README.md). Real company content belongs in a separate private location chosen during setup.
