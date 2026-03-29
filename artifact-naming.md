# story-room artifact naming

This file defines naming and version conventions for durable system artifacts.

Goal: names should reveal artifact type, version, and state clearly enough to support long-term operation.

---

## 1. Naming formula

Recommended pattern:
<artifact-type>-v<version>[-working][-scope]

Examples:
- brief-v1
- hook-board-v2
- hook-board-v3-working
- script-v4
- storyboard-v2-working
- delivery-v1-pilot

Scope suffix is optional but useful when multiple episode scopes exist.

---

## 2. Canonical artifact names

Use these base names where possible:
- brief
- hook-board
- outline
- characters
- script
- storyboard
- review-routing
- delivery

Avoid inventing many near-duplicate labels for the same layer.

---

## 3. State suffix rule

### approved
No suffix required beyond version.
Example:
- script-v3

### working
Use `-working` suffix.
Example:
- script-v4-working

### archived
Preserve original name and move to archive, or append archival timestamp if needed.
Example:
- script-v2
- script-v2-archived-2026-03-28

---

## 4. Version rule

Use simple increasing integers.
Do not skip to semantic versioning unless system complexity truly requires it.

Examples:
- hook-board-v1
- hook-board-v2
- hook-board-v3-working

A new approved replacement increments version.
A working patch before approval uses the next intended version with `-working`.

---

## 5. Promotion examples

### Example A
- approved current: script-v2
- new patch draft: script-v3-working
- after approval: script-v3
- old approved moved to archive: script-v2

### Example B
- approved current: hook-board-v1
- structural patch draft: hook-board-v2-working
- after approval: hook-board-v2
- downstream script may become stale

---

## 6. Scope naming

If multiple episodes or branches exist, append a concise scope suffix.

Examples:
- script-v2-ep01
- hook-board-v1-pilot
- storyboard-v3-ep02-working

Keep scope short and stable.

---

## 7. File hygiene rules

- do not overwrite approved artifacts without archiving previous approved version
- do not store unnamed drafts as final references
- do not create ambiguous labels like `new-script-final-final2`
- do not change naming style mid-project without migration plan

---

## 8. Operational rule

The orchestrator should be able to infer from the filename:
- artifact type
- version order
- whether it is working or approved
- optional scope

If a filename does not make these obvious, rename it.
