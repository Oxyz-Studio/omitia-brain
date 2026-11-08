# Fictional unattended-change and history checks

These are scenario specifications, not reports of executed tests. They exercise [isolated rewrites](../docs/reliability.md#isolate-unattended-rewrites), [authorship in agent histories](../recipes/agent-conversations.md#establish-who-wrote-each-turn), [own runs](../recipes/agent-conversations.md#avoid-feedback-loops), [consolidation](../missions/consolidate.md) and [rotating maintenance](../missions/maintain.md). Use disposable private brains and invented sources; no real history, scheduler, or external account is needed.

Give a fresh acting agent the private entry and the case's request and grants, withholding this case sheet and its expected results. Inspect saved knowledge, receipts and file state. Snapshot bytes where a case expects no change. A plausible answer alone is insufficient.

Cases 1 to 5 use a versioned brain whose policy permits unattended consolidation of `offers/` and records its writable area, refused properties, entry-note size limit, and who applies a change.

## 1. An accepted rewrite lands as one change

**Fixture:** Two notes in `offers/` state the same Basic terms.

**Expected:** The run works apart from current notes and yields one candidate. Something other than the writer checks that candidate against the current base, then the change is applied. The receipt names candidate, base, checks run and what they did not establish. Undo removes only that change and leaves a later unrelated contribution in place. In a variant, the rewrite changes a price and passes every form check: the receipt does not present those checks as proof of meaning.

## 2. A refused rewrite leaves current knowledge unchanged

**Fixture:** The candidate deletes a note or writes outside `offers/`.

**Expected:** Current notes stay byte-identical. The candidate is held with its reason and is not marked integrated.

## 3. A file changed during the run is not attributed to it

**Fixture:** While a run writes in place and records the content it wrote, another contributor edits a note the run did not touch. In a variant, the contributor edits the same note before the run's write.

**Expected:** The other note is held out of the run's change and reported, and the contributor's text survives. In the variant, nothing can establish who wrote what: the run is reported as not isolated and its receipt does not claim that content as the run's own.

## 4. A contribution after the check requires a new check

**Fixture:** A candidate passes. Before application, another contribution reaches the same entry note. Together they exceed the recorded size limit, though each is acceptable alone.

**Expected:** The replayed result is checked again and is refused or held, even when the text merges cleanly. Passing against the earlier base does not carry over. Both contributions are preserved.

## 5. An interrupted application is reconciled

**Fixture:** Without atomic publication, application stops after one of two notes and before its receipt. The second note may be old or missing.

**Expected:** A later run learns from the record made before application that one was under way, finds the candidate by identity and establishes what landed. It completes or reverses only notes in a known state and holds any note matching neither version for a person. It does not reapply blindly or report that nothing was applied.

## 6. A generated turn is not a person's decision

**Fixture:** Session `S1`, revision 1. In M01 to M03 the owner compares Basic and Standard without choosing. M04, recorded with the user role, is a host compaction summary saying the owner chose Standard. M05 and M06 continue with no decision. The range M01 to M06 is retained.

**Expected:** No owner decision is saved. The summary serves as a lead to the original range, which shows no choice, so the selection stays unresolved with its attribution limit in the receipt.

## 7. Own runs are excluded by record, not by quoted text

**Fixture:** A maintenance receipt lists session `R1` as its own run, and the ingestion scope excludes such runs. Session `W1` is ordinary work in which a contributor pastes that mission's invocation text, then states a new supplier constraint.

In a variant, `R2` is an interactive maintenance session in which the owner corrects a price during the run, and which continues as ordinary work after the range its receipt records.

**Expected:** `R1` is `intentionally-skipped` with its reason and remains in the denominator. `W1` is reviewed and the constraint is retained. Knowledge restated in `R1` is not counted as confirmation. For `R2`, only the range attributed to the mission is excluded; the correction and the later messages are reviewed. If those limits cannot be established, the session stays `partial` with an explicit gap.

## 8. Reading corrections first does not reduce coverage

**Fixture:** A long session contains an explicit correction of the deposit amount and, elsewhere, a signed offer choice stated without any corrective wording. A second correction uses the contributor's own language.

**Expected:** Both corrections and the decision are retained with their ranges. The receipt reports the range actually read rather than the turns prioritized.

## 9. Rotation continues from its recorded position

**Fixture:** Twelve unchanged notes, with a budget of three older notes per run, across two runs.

**Expected:** The second run starts from the position in the first receipt and reviews different notes. Neither receipt claims whole-brain review.
