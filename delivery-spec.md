# story-room delivery spec

This file defines how final packages are assembled so outputs remain stable across repeated runs.

Principle: final delivery is a curated package, not a raw concatenation of agent outputs.

---

## 1. General assembly rules

Every package should preserve this order when applicable:
1. title / label
2. hook spine or hook board summary
3. premise / logline
4. cast or role notes
5. outline or beat structure
6. active draft layer
7. review summary
8. remaining risks / next-step notes

The orchestrator may compress sections for shorter requests, but should not scramble the hierarchy.

---

## 2. concept-package delivery

### Required sections
- Title options
- Hook board summary
- Logline
- Premise
- Core conflict
- Main cast
- Episode outline
- Risks / open questions
- Review summary

### Goal
The user should be able to approve the concept spine without needing a full script.

---

## 3. pilot-package delivery

### Required sections
- Title
- Hook board summary
- Episode synopsis
- Cast essentials
- Scene script
- Ending cliffhanger
- Review summary
- Remaining risks

### Optional sections
- Change log if revised
- Visual planning note if storyboard follows next

---

## 4. rewrite-package delivery

### Required sections
- Revised scope summary
- What changed
- Revised scenes or revised layer output
- Why the patch was made
- Remaining risks

### Rule
Do not re-dump unchanged material unless the user asked for a full clean version.

---

## 5. expansion-package delivery

### Required sections
- Expansion goal
- Updated hook spine / board summary
- Updated outline or episode map
- New scenes or new episode material
- Continuity notes
- Review summary

---

## 6. storyboard-package delivery

### Required sections
- Script reference
- Hook translation summary
- Shot list by scene
- Key reversal image
- Cliffhanger image
- Production efficiency notes
- Storyboard review summary

---

## 7. storyboard-rewrite-package delivery

### Required sections
- Rewrite scope
- What was wrong
- Updated shots only or updated sequence
- Whether script layer was patched too
- Remaining production risks

---

## 8. Stable run rule

For the workflow to keep running over time, the orchestrator should be able to identify at least one approved artifact after every completed delivery:
- approved concept spine
- approved hook board
- approved character package
- approved script
- approved storyboard

If final delivery does not leave behind a reusable approved artifact, the run is structurally weak.
