# story-room continuity protocol

This file defines how continuity is tracked and protected across a multi-episode season.

Goal: prevent the system from producing individually strong episodes that break the season as a whole.

---

## 1. Continuity categories

Track continuity in at least these lanes:
- character state
- relationship state
- reveal state
- power hierarchy state
- unresolved thread state
- callback state
- injury / evidence / consequence state

---

## 2. Required continuity artifacts

Create and maintain:
- continuity ledger
- reveal tracker
- callback tracker
- relationship progression grid
- character-state tracker
- episode dependency map

---

## 3. Episode update rule

After every approved episode, update continuity artifacts with:
- what changed permanently
- what was revealed
- what remains hidden
- what new thread was opened
- what old thread was closed
- what next episodes now depend on this change

---

## 4. Continuity review checkpoints

Run continuity review:
- before batch drafting
- after each batch
- after any structural patch
- before final season lock

---

## 5. High-risk continuity failures

Examples:
- a character knows information before learning it
- a relationship flips without progression
- a hidden power reveal is repeated after exposure
- the antagonist loses authority too early
- a promised payoff disappears without closure
- an injury, clue, or legal consequence is forgotten

These are not cosmetic. They affect structural trust.

---

## 6. Continuity severity

### Level 1
Local inconsistency. One episode patch is enough.

### Level 2
Multi-episode dependency break. Patch current batch.

### Level 3
Season-structural contradiction. Patch season map or season spine first.

---

## 7. Continuity patch order

When continuity breaks, patch in this order:
1. season spine if contradiction is structural
2. episode map if dependency path is wrong
3. character / relationship trackers if state is wrong
4. local episode scripts
5. storyboards only after script continuity is stable

---

## 8. Continuity tolerance rule

The system may tolerate minor cosmetic variation.
It must not tolerate continuity errors that break cause-and-effect, reveal order, or emotional progression.

---

## 9. Autonomous protection rule

For autonomous long runs, continuity review is the main brake against blind generation.
If continuity confidence falls below threshold, the system should pause batch advancement and patch the controlling artifact first.
