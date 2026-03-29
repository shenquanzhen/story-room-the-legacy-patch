# story-room orchestrator playbook

This file is the practical operating guide for running the system end to end.

Use it when executing real jobs, not just designing policy.

---

## 1. First move on every request

When a new request arrives, do these in order:
1. classify the request type
2. normalize the task brief
3. check existing approved artifacts
4. identify missing dependencies
5. choose the smallest valid branch set

Do not spawn branches before dependency check.

---

## 2. Startup checklist

Before starting a run, confirm:
- current request type
- current target deliverable
- approved hook board exists or not
- approved outline exists or not
- approved character package exists or not
- approved script exists or not
- approved storyboard exists or not
- active working revision exists or not
- stale artifacts exist or not

If stale artifacts exist, decide whether to patch or regenerate before continuing.

---

## 3. Request handling by type

## 3.1 concept-package
### Steps
1. build normalized brief
2. spawn plot-agent
3. spawn character-agent
4. merge into hook board
5. run review-agent
6. if revise -> patch smallest broken layer
7. promote approved concept artifacts
8. assemble delivery

### Promote on success
- brief
- hook board
- outline
- character package
- review summary

---

## 3.2 pilot-package
### Steps
1. build normalized brief
2. spawn plot-agent
3. spawn character-agent
4. merge hook board
5. prepare script brief from hook board + outline + characters
6. spawn script-agent
7. run review-agent
8. if revise -> patch smallest broken layer
9. if approved -> promote script package
10. assemble delivery

### If visual planning requested
11. check script + hook board approved
12. spawn storyboard-agent
13. run storyboard-review-agent
14. if revise -> patch storyboard or upstream as needed
15. promote storyboard artifacts
16. update delivery package

---

## 3.3 rewrite-package
### Steps
1. collect current approved draft and latest review context
2. if no review exists, run review-agent first
3. classify issue type and owner
4. decide patch depth
5. patch hook board first if structural
6. patch target layer
7. re-check touched scope only
8. promote revised artifact if successful
9. assemble rewrite delivery

---

## 3.4 storyboard-package
### Steps
1. confirm approved script + hook board
2. spawn storyboard-agent
3. run storyboard-review-agent
4. patch smallest broken visual layer
5. promote storyboard if approved
6. assemble delivery

---

## 3.5 storyboard-rewrite-package
### Steps
1. collect storyboard + script + hook board
2. run storyboard-review-agent first
3. classify storyboard-only vs script-caused
4. if script-caused -> patch script first
5. regenerate affected shots only where possible
6. re-check touched scope
7. promote revised storyboard
8. assemble delivery

---

## 4. Merge procedure

### Merge A - hook board merge
Use when plot and character outputs are both available.

Inputs:
- plot output
- character output

Produce:
- approved or working hook board
- notes on unresolved conflict if any

### Merge B - script readiness merge
Use before script drafting.

Inputs:
- hook board
- outline
- character package

Produce:
- script-agent brief
- list of non-negotiable beats
- reveal timing constraints

### Merge C - patch merge
Use after patch returns.

Inputs:
- active artifact
- patch result
- review routing note

Produce:
- revised working artifact
- stale downstream list if applicable

### Merge D - final delivery merge
Use after approved artifacts are ready.

Produce a coherent user package, not a branch dump.

---

## 5. Promotion procedure

Promote to approved only after one of these:
- review verdict is ship
- must-fix items for that layer are resolved
- user explicitly accepts tradeoff and approves

When promoting:
1. archive previous approved version
2. mark new version approved
3. record downstream stale impact if any
4. update latest artifact references

---

## 6. Patch order rule

If multiple owners are involved, patch in this order:
1. plot layer if hook spine is broken
2. character layer if motivation support is broken
3. script layer for scene execution
4. storyboard layer for visual translation

Do not patch downstream first when upstream control logic is clearly broken.

---

## 7. Stop rule in real operation

Stop the run when:
- active layer is usable
- must-fix items are closed
- remaining issues are cosmetic
- additional iteration has poor ROI

Escalate to restart only if structural contradiction blocks stable patching.

---

## 8. What to do if the room drifts

If a branch drifts outside scope:
1. isolate what is still usable
2. reject silent cross-layer changes
3. resend a narrower scoped task
4. patch controlling artifact first if needed

Do not reward drift by adopting it automatically.

---

## 9. Minimal run closeout

At the end of every meaningful run, ensure all of these are true:
- final delivery assembled
- at least one artifact promoted or deliberately retained
- stale artifacts identified
- latest approved state is clear
- next run can start without reconstructing context from memory only
