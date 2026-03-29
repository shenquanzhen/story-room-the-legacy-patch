# story-room autonomy policy

This file defines when the system may continue automatically and when it must slow down, patch, or escalate.

Goal: support near-uninterrupted production without allowing blind structural failure.

---

## 1. Continue automatically when

The system may keep running when:
- dependencies are satisfied
- current layer review is within tolerance
- continuity checks pass
- no unresolved critical contradiction exists
- required artifacts are promoted clearly

---

## 2. Slow down and patch when

The system should patch before advancing when:
- a hook issue weakens retention materially
- a continuity issue affects later episodes
- a reveal order issue creates confusion
- an antagonist or protagonist arc is drifting off plan

---

## 3. Pause and escalate when

The system should pause autonomous advancement when:
- season spine is contradictory
- multiple batches become stale at once
- final payoff no longer exceeds early payoff
- the protagonist arc becomes incoherent
- patch cost exceeds safe autonomous scope

---

## 4. Human intervention threshold

In the target future mode, human intervention should be rare, not absent by default.
The system should request intervention only when:
- core creative intent is ambiguous
- two valid structural directions conflict materially
- season-scale regeneration would be expensive and preference-dependent

---

## 5. Anti-blindness rule

Autonomy does not mean "keep generating no matter what."
Autonomy means:
- detect risk
- patch locally when possible
- pause only at real structural uncertainty
- preserve approved state while deciding next move

---

## 6. Target behavior for 20-episode runs

The desired autonomous mode is:
- long uninterrupted stretches of drafting and review
- bounded self-repair loops
- continuity-aware gating
- rare but meaningful escalation only when required
