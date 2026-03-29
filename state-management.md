# story-room state management

This file defines how the system stores, promotes, and reuses working artifacts across repeated runs.

Goal: the room should keep running over time without losing track of approved state, active revisions, or branch outputs.

---

## 1. State model

Every important artifact should live in one of three states:
- working
- approved
- archived

### working
Current editable version under active development.

### approved
Current trusted version that downstream branches may rely on.

### archived
Older versions kept for traceability, rollback, or comparison.

The orchestrator should never confuse working with approved.

---

## 2. Canonical artifact types

The system should recognize these artifacts as first-class state:
- task brief
- hook board
- outline
- character package
- script draft
- storyboard draft
- review routing summary
- final delivery package

Not every run will create all artifact types, but every meaningful run should update at least one.

---

## 3. Promotion rules

### working -> approved
Promote an artifact from working to approved only when:
- it has passed the required review checkpoint for its layer
or
- the user explicitly approves it
or
- the orchestrator marks it as approved baseline for constrained iteration

### approved -> archived
When a newer approved artifact replaces an older one, archive the older one instead of deleting it.

### working -> archived
Archive abandoned working artifacts if they are superseded or structurally invalid.

---

## 4. Single source of truth rule

For each artifact type, there should be one current approved source of truth.

Examples:
- one approved hook board for the active episode scope
- one approved script for the active draft version
- one approved storyboard for the current visual plan

If multiple candidate artifacts exist, the orchestrator must resolve which is authoritative before new work continues.

---

## 5. Run startup rule

At the start of a new run, the orchestrator should determine:
- latest approved task brief
- latest approved hook board
- latest approved outline
- latest approved character package
- latest approved script
- latest approved storyboard
- any active working revision

If an approved artifact exists, reuse it instead of rebuilding from memory.

---

## 6. Versioning rule

Use simple monotonic versions for stability.

Recommended pattern by artifact type:
- brief-v1
- hook-board-v1
- outline-v1
- characters-v1
- script-v1
- storyboard-v1
- review-routing-v1
- delivery-v1

When revised and approved:
- hook-board-v2
- script-v2
etc.

If a working patch exists before approval, use a working suffix such as:
- script-v2-working
- storyboard-v3-working

---

## 7. Dependency integrity rule

Downstream work should always reference the approved upstream artifact version it depends on.

Examples:
- script-v2-working depends on hook-board-v2 + characters-v1
- storyboard-v1-working depends on script-v2 + hook-board-v2

If upstream changes invalidate downstream outputs, downstream state must be marked stale until patched or regenerated.

---

## 8. Staleness rule

An artifact becomes stale when a controlling upstream artifact changes in a way that affects it.

Examples:
- changing the hook board can stale the script
- changing character motivation can stale scenes and storyboard
- changing script structure can stale storyboard coverage

Stale artifacts should not be treated as approved for new dependent work.

---

## 9. Session continuity rule

The orchestrator should preserve enough state so a future run can answer:
- what is approved right now
- what is being revised right now
- what changed last
- what downstream artifacts may now be stale

If the system cannot answer these four questions, state hygiene is weak.

---

## 10. Recommended directory logic

Use a stable structure such as:
- state/brief/
- state/hook-board/
- state/outline/
- state/characters/
- state/script/
- state/storyboard/
- state/review/
- state/delivery/
- state/archive/

This document does not force immediate migration, but future architecture should align to a predictable state tree.

---

## 11. Merge logging rule

After every meaningful merge, record:
- source artifacts used
- new artifact created
- whether it is working or approved
- which downstream artifacts may be stale

This can later become a run log or merge ledger.

---

## 12. Safety against drift

To keep repeated runs stable:
- do not overwrite approved artifacts silently
- do not create downstream drafts from unapproved upstream changes unless explicitly exploratory
- do not let memory-only summaries replace approved artifacts
- do not delete older approved versions without archiving

---

## 13. Minimum persistence rule

A completed run should leave behind at least:
- one approved artifact
- one identifiable latest version
- enough metadata to know what depends on what

If not, the run is not durable enough for long-term system use.
