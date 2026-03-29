# story-room merge protocol

This file defines how outputs from different branches are combined into trusted working or approved artifacts.

Goal: merging should be explicit, traceable, and architecture-safe.

---

## 1. Merge philosophy

A merge is a control action, not a copy-paste action.

Every merge should answer:
- what inputs are being combined
- which artifact becomes authoritative
- what conflicts were resolved
- what downstream artifacts may now be stale

---

## 2. Merge preconditions

Before any merge, verify:
- input artifacts are identified by version or clear reference
- ownership boundaries are respected
- conflicts are surfaced, not hidden
- merge target is defined

If these are not clear, do not merge yet.

---

## 3. Merge types

## 3.1 Hook merge
### Purpose
Combine plot-layer and character-layer outputs into one hook board.

### Inputs
- latest plot output
- latest character output
- approved task brief

### Output
- working or approved hook board

### Checks
- hook spine is internally consistent
- character motivations support hook promises
- no silent contradiction with approved brief

---

## 3.2 Script readiness merge
### Purpose
Prepare the controlled brief for script-agent.

### Inputs
- approved or working hook board
- outline
- character package

### Output
- script-agent input package

### Checks
- non-negotiable beats are explicit
- reveal timing constraints are explicit
- scene-level responsibilities are clear

---

## 3.3 Patch merge
### Purpose
Integrate a patch into the active working artifact.

### Inputs
- active artifact under revision
- returned patch
- review routing summary

### Output
- revised working artifact

### Checks
- named issue is actually solved
- unchanged scope remains stable
- upstream authority is not accidentally overwritten
- stale downstream artifacts are marked if needed

---

## 3.4 Delivery merge
### Purpose
Assemble final user-facing package.

### Inputs
Depend on request type, but should prefer approved artifacts.

### Output
- delivery package

### Checks
- coherent order
- no contradictory sections
- no raw branch dump without curation

---

## 4. Conflict resolution order

When merge inputs conflict, resolve in this order:
1. approved task brief
2. approved hook board
3. approved outline / character package
4. active draft layer
5. review suggestions
6. optional punch-up notes

If a lower-priority input contradicts a higher-priority one, do not merge it blindly.

---

## 5. Merge outcomes

A merge should end in exactly one of these outcomes:
- approved artifact created
- working artifact created
- merge blocked pending clarification
- merge rejected because of contradiction

Do not leave merge status ambiguous.

---

## 6. Post-merge actions

After every meaningful merge:
1. assign or update artifact version
2. record merge in run ledger
3. mark stale downstream artifacts if any
4. decide whether artifact is working or approved
5. update current state index if used

---

## 7. Anti-drift rule

Never treat a merged artifact as approved just because it looks better.
Approval requires review passage, user approval, or explicit orchestrator promotion under defined rules.
