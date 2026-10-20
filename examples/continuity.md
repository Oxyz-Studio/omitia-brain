# Continuity: “the second one”

A processed source and an understood claim are different things. This fictional example shows how to preserve that difference across runs.

## 1. First run: context missing

On 13 October, the agent can read only M03:

> For bookings, let's take the second one. We will stay weekday-only for the launch.

The earlier options are absent from the available export. The weekday statement stands alone, so the agent integrates it. It cannot identify “the second one” and records C01 as `partial`, with M03 retained and M01 listed as the missing dependency. It does not write a provider decision or mark the entire source integrated.

This is the state recorded in [R01](studio-brain/receipts/2026-10-13.md). The system can answer “weekday-only” while saying the provider is not yet resolved.

## 2. Next run: rehydrate before interpreting

On 14 October, a recovered export supplies M01:

| Position | Option | Source details |
| --- | --- | --- |
| First | Shared calendar | €0 per month, manual confirmations. |
| Second | BookLane | €20 per month, customer self-booking and reminders. |

The agent retrieves the earlier C01 gap, reads the original comparison, and combines M01 with M03. Policy v1 already authorizes automatic owner-decision integration, so it records **BookLane** without another approval. It preserves the alternatives to make future references recoverable. The run saves notes and a partial receipt, then asks ordinary booking, price, and opening-scope questions through README navigation. Only after successful readback does it finalize changed items as integrated. See the [decision](studio-brain/decisions/booking-platform.md) and [R02](studio-brain/receipts/2026-10-14.md).

A rerun recognizes the same stable message IDs and does not create a second decision. If M01 had remained unavailable, C01 would remain partial with its retry condition; absence would not turn a guess into knowledge.

## 3. A stale draft is useful history

M02 contains a €40 price draft with a review deadline of 13 October. After that deadline it is stale for current-price retrieval, even before a replacement is known. M04 then confirms €45 and explicitly replaces the draft.

The agent updates the [current launch note](studio-brain/notes/repair-launch.md) and preserves the [draft's history](studio-brain/notes/pricing-draft-history.md). It can now explain the change without answering a current-price question with the stale draft. Merely failing to see the €40 draft in a new export would not have been evidence to delete or retract it.

## 4. A contribution is not automatically a company decision

Luca suggests Saturday opening because of his personal scheduling preference. The source supports an attributed proposal, not a change to the owner's weekday-only decision. The agent records the [proposal](studio-brain/notes/weekend-proposal.md) automatically within its grant. A repetition the next day produces `no-durable-change`, not a second note or a new policy.

This illustrates one configured policy, not a universal approval hierarchy. Another business can grant different people different authority and automatic actions while keeping the same evidence and continuity principles.

## What the next run needs

The [log](studio-brain/INGESTION_LOG.md) preserves source versions/ranges, stable claim IDs, item outcomes, destinations, and retry conditions. The source files preserve enough original context to reconstruct meaning. Summaries link to canonical decisions. The agent must retrieve those records; keeping them on disk alone does not guarantee they will be read.

A source may be unavailable, an export may be truncated, or retention rules may prohibit storing originals. Record the resulting recovery limits. Do not call inaccessible material integrated merely to advance a cursor. Unrelated useful work can still continue.
