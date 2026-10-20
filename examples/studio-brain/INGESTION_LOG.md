# Ingestion log

## Run R01 — 13 October 2026, 17:00 Europe/Paris

Policy v1. Observed owner-launch export v1, M03 only. M01–M02 were unavailable in the export.

| Item | Evidence | Outcome | Destination / reason | Follow-up |
| --- | --- | --- | --- | --- |
| C01: selected booking provider | owner-launch v1 M03 | partial | “The second one” lacks its options. No provider decision was written. | Retry when M01 is available. |
| C02: weekday-only launch | owner-launch v1 M03 | integrated | Initial launch summary. This statement is self-contained. | None. |

Readback: after saving notes and a partial receipt, the ordinary question “Which days are planned for the repair launch?” followed the README to the saved weekday-only statement. C02 was finalized only after that readback. C01 remained unresolved.

Observed through M03; completed integration has an explicit C01 gap. Retained M03 and its stable ID; do not discard it or pretend the source is fully integrated. [Receipt R01](receipts/2026-10-13.md).

## Run R02 — 14 October 2026, 15:00 Europe/Paris

Policy v1. Observed owner-launch v2 M01–M04, plus workshop-input v1 L01. Retrieved the prior C01 gap before interpreting M03.

| Item | Evidence | Outcome | Destination / reason | Follow-up |
| --- | --- | --- | --- | --- |
| C01: selected booking provider | owner-launch v2 M01 + M03 | integrated | [Booking decision](decisions/booking-platform.md): second option is BookLane. | Verify live supplier details before purchase. |
| C02: weekday-only launch | owner-launch v2 M03 | no-durable-change | Already integrated; summary retained. | None. |
| C03: draft and confirmed service prices | owner-launch v2 M02 + M04 | integrated | [Current €45 price](notes/repair-launch.md); [€40 historical draft](notes/pricing-draft-history.md). | Recheck on owner change or before live quotation. |
| C04: Luca's Saturday suggestion | workshop-input v1 L01 | integrated | [Attributed proposal](notes/weekend-proposal.md); company decision unchanged. | No action unless relevant to future planning. |

Readback: notes and a partial receipt were saved first. Normal questions about the selected provider, launch price/history, and Saturday opening followed README links to the canonical answers with their limits. See the detailed readback in R02. Only then were changed items finalized as integrated.

Completed integration: owner-launch v2 M01–M04, workshop-input v1 L01. C01 is resolved. Source evidence is retained in the local fictional transcripts. No open integration gaps remain. [Receipt R02](receipts/2026-10-14.md).

## Run R03 — 15 October 2026, 12:00 Europe/Paris

Policy v1. Observed workshop-input v2 L02; recovered L01 and the existing proposal to compare meaning.

| Item | Evidence | Outcome | Destination / reason | Follow-up |
| --- | --- | --- | --- | --- |
| C05: repeated Saturday preference | workshop-input v2 L02 | no-durable-change | Repeats C04 without new evidence or decision authority. Source coverage and the proposal's last-check date were updated. | None. |

Completed review: workshop-input v2 L01–L02. No new domain knowledge was created; a reviewed repeat is not a failure. Last useful domain change remains R02. [Receipt R03](receipts/2026-10-15.md).
