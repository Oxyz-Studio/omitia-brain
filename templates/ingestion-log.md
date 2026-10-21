# Ingestion log

Record source coverage and claim outcomes, not merely that a file was opened. Use a small receipt per batch or a growing table, whichever stays readable.

Keep the receipt and its search metadata within the applicable audience. Source identities, titles, and the fact that an item was processed can be confidential; a broadly readable run report must not expose a restricted receipt.

## Run: {stable run ID}

- Mission and time: {mission reference and actual run time}.
- Policy used: {policy version or dated section}.
- Source observations: {source IDs, versions, and exact ranges inspected}.

| Claim or item | Evidence / source range | Outcome | Destination or reason | Follow-up |
| --- | --- | --- | --- | --- |
| {stable item ID and meaning} | {version + range} | {collected / partial / blocked / integrated / no-durable-change / intentionally-skipped} | {canonical note or concrete reason} | {retry condition / none} |

## Retrieval readback

For changed knowledge, save the note and this coverage receipt while the outcome is still `partial`. Then test an ordinary later-use question through the brain entry point or configured search, not solely by opening the destination path supplied by the writer.

- Question: {the normal question used}.
- Path followed / result: {how the canonical knowledge and its limits were found, or what failed}.
- Receipt and note persisted before readback: {evidence}.
- Finalization: {mark the covered unit integrated only after successful readback; otherwise retain partial and a recovery step}.

A `no-durable-change` or `intentionally-skipped` item needs examined coverage and a reason; it does not require a filler note.

## Coverage checkpoint

- Observed through: {ranges actually inspected}.
- Fully integrated through: {ranges fully reconciled, with gaps explicitly listed}.
- Open items carried forward: {stable IDs and missing context}.
- Evidence retained / recovery location: {resolvable references within permitted retention}.

Do not mark an unreadable or context-dependent item as integrated. Use `collected` for input acquired but not evaluated, `partial` for an incomplete integration, and `blocked` when an item cannot currently be processed. Use `no-durable-change` when the reviewed material contributes no new durable knowledge; use `intentionally-skipped` when an explicit scope or retention rule excludes it. A replay should add missing evidence or confirm prior integration without creating duplicate notes.
