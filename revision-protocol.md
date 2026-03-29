# story-room revision protocol

This file defines how revisions are requested, routed, merged, and stopped.

Goal: revisions must improve the active draft without turning the room into endless full rewrites.

---

## 1. Revision philosophy

A revision is not a fresh generation pass.
A revision is a controlled repair process.

Default order:
1. diagnose
2. assign owner
3. patch smallest broken layer
4. merge patch
5. re-check only what changed
6. stop when usable

---

## 2. Revision entry conditions

A revision cycle begins only when at least one of these is true:
- review-agent verdict is revise
- storyboard-review-agent verdict is revise
- user requests targeted changes
- orchestrator detects contradiction against approved artifacts

A revision should not begin from vague dissatisfaction alone. Convert dissatisfaction into named issues first.

---

## 3. Issue classification

Every issue must be classified before patching.

### 3.1 Hook issue
Examples:
- opening does not grab fast enough
- first reversal lands too late
- cliffhanger is weak

Default owner:
- plot-agent or script-agent

### 3.2 Logic issue
Examples:
- motivation unclear
- reveal order breaks credibility
- cause-and-effect chain is broken

Default owner:
- plot-agent, character-agent, or script-agent depending on layer

### 3.3 Payoff issue
Examples:
- humiliation is not sharp enough
- slap-back is too soft
- emotional turn does not land

Default owner:
- script-agent first unless premise spine is the cause

### 3.4 Visual issue
Examples:
- coverage unclear
- reversal image weak
- cliffhanger shot lacks force

Default owner:
- storyboard-agent

---

## 4. Patch depth rules

### Level 1 - Local patch
Use when the problem is contained to one scene, one motivation link, or one visual sequence.

Examples:
- strengthen scene exit hook
- clarify one character turn
- replace a weak final shot

### Level 2 - Layer patch
Use when a whole layer is wrong but upstream structure is still valid.

Examples:
- several scenes drag even though hook board is fine
- character voice is flat across the episode
- storyboard coverage is weak across all scenes

### Level 3 - Structural patch
Use when the hook board or premise spine is broken.

Examples:
- opening hook does not align with payoff
- comeback fantasy is unclear
- cliffhanger contradicts the episode arc

### Level 4 - Full restart
Rare. Use only when patching would create more contradiction than rewriting.

Requires explicit reason.

---

## 5. Mandatory patch request structure

Every patch request sent to a branch should include:
- target layer owner
- issue summary
- exact location
- why it matters
- what must remain unchanged
- whether hook board patch has already happened
- expected output format

### Patch request template
- Owner:
- Severity:
- Issue:
- Location:
- Why this breaks retention / logic / payoff:
- Keep unchanged:
- Patch hook board first?: yes / no
- Return:

---

## 6. Hook board patch rule

If a revision changes any of the following, patch the hook board before or alongside scene revision:
- opening hook
- protagonist pressure point
- audience suspense question
- first reversal
- emotional payoff beat
- episode-end cliffhanger

Script patches should not quietly replace these on their own.

---

## 7. Routing rules

### Send to plot-agent when
- premise is muddy
- beat order is weak
- reversal placement is wrong
- cliffhanger structure is weak

### Send to character-agent when
- motive is unclear
- emotional pivot lacks basis
- relationship tension is weak
- voice separation is poor

### Send to script-agent when
- scenes drag
- conflict lacks escalation
- dialogue carries too much exposition
- payoff execution is soft
- exit hooks are weak

### Send to storyboard-agent when
- visual emphasis is unclear
- reveal shot is weak
- shot order hurts rhythm
- production logic is clumsy

---

## 8. Merge after patch

After a patch returns, the orchestrator must merge the result back into the active approved state.

Merge checklist:
- Does the patch solve the named issue?
- Does it break any approved hook spine element?
- Does it create new contradictions?
- Does it change any downstream dependency?

If yes, update the controlling artifact before continuing.

---

## 9. Re-review rules

Re-review only the affected scope unless the patch is structural.

### Local patch
Re-check the touched scene or sequence.

### Layer patch
Re-check the active layer.

### Structural patch
Re-check downstream layers affected by the hook board or premise change.

Do not restart full review by default.

---

## 10. Stop rules

Stop revision when one of these is true:
- must-fix items are resolved
- remaining issues are cosmetic
- additional iteration has low ROI
- user prefers speed over polish

Default cap:
- one focused revision round
- one final polish only if clearly justified

---

## 11. Anti-loop rules

To keep revisions sustainable over repeated runs:
- do not mix diagnosis and redrafting in the same instruction unless scope is tiny
- do not send the same vague note back twice
- do not reopen approved upstream layers without explicit reason
- do not let optional polish become hidden must-fix work
- do not let one weak branch force a whole-room reset automatically

If the same issue survives two passes, escalate one level up in patch depth or stop and surface the tradeoff.
