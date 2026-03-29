# story-room execution spec

This file defines how the orchestrator should issue work to child agents in a repeatable way.

Goal: convert architecture into stable execution behavior.

---

## 1. Standard task envelope

Every child-agent task should include these sections in order:
- role
- objective
- owned layer
- current approved inputs
- current working inputs if relevant
- required output format
- must preserve
- must not do
- stop condition

This reduces drift across repeated runs.

---

## 2. Standard child-agent rules

All child agents should follow these rules:
- stay inside owned layer
- flag upstream contradictions instead of silently rewriting them
- preserve approved artifacts unless explicitly told to replace them
- return structured output, not vague commentary
- identify weak points when confidence is low

---

## 3. plot-agent execution spec

### role
plot-agent

### objective
Design or patch the premise spine, beat progression, hook map, and cliffhanger logic.

### owned layer
macro story structure

### required inputs
- approved task brief
- current approved hook board if patching
- current approved outline if patching
- constraints

### required output format
- logline
- premise
- protagonist goal
- antagonist pressure
- episode beat outline
- hook map
- unresolved questions
- risks

### must preserve
- approved character truths unless patch request says otherwise
- approved hook board elements unless explicitly patching them

### must not do
- write full scene dialogue
- silently change motivations owned by character layer

### stop condition
Return one structured proposal or one focused patch only.

---

## 4. character-agent execution spec

### role
character-agent

### objective
Design or patch motivations, relationship tensions, emotional pivots, and voice separation.

### owned layer
character and relationship system

### required inputs
- approved task brief
- premise or outline summary
- current approved hook board if relevant
- current approved character package if patching

### required output format
- main cast sheet
- motivations
- relationship tensions
- voice cues
- contradiction points
- emotional pivots
- character hook points

### must preserve
- approved plot spine unless conflict is flagged

### must not do
- rewrite beat order as if it owns plot structure
- replace scene execution work

### stop condition
Return one structured package or one focused patch only.

---

## 5. script-agent execution spec

### role
script-agent

### objective
Convert approved structure into scenes with conflict escalation, dialogue, reversals, and exit hooks.

### owned layer
scene execution

### required inputs
- approved task brief
- approved hook board
- approved outline
- approved character package
- current script version if patching

### required output format
- numbered scenes
- scene hook
- scene goal
- conflict escalation
- dialogue draft
- turn / reversal
- exit hook
- cliffhanger ending
- known weak points

### must preserve
- approved hook spine
- approved motivations and relationship logic
- non-targeted scenes if request is a local patch

### must not do
- silently replace hook board
- silently invent new character truths that affect upstream logic

### stop condition
Return the requested scope only: full draft, partial patch, or revised scenes.

---

## 6. review-agent execution spec

### role
review-agent

### objective
Diagnose the active layer and route must-fix items to the correct owner.

### owned layer
diagnosis and routing

### required inputs
- approved hook board
- approved outline and character package when relevant
- active draft under review
- task goal

### required output format
- what already works
- hook diagnosis
- logic diagnosis
- payoff diagnosis
- must-fix items by owner
- optional punch-ups
- verdict

### must preserve
- separation between diagnosis and rewriting

### must not do
- perform hidden redrafts instead of review
- give ownerless must-fix notes

### stop condition
Return diagnosis only.

---

## 7. storyboard-agent execution spec

### role
storyboard-agent

### objective
Translate approved script and hook board into visual coverage and visual hook design.

### owned layer
visual planning

### required inputs
- approved script
- approved hook board
- tone / style notes
- production constraints when available
- current storyboard if patching

### required output format
- shot list by scene
- shot purpose
- framing / angle / movement
- covered dialogue or action
- visual hook
- reveal shot
- cliffhanger image
- efficiency notes
- known weak points

### must preserve
- approved script logic unless issue is flagged back upstream

### must not do
- rewrite story structure silently

### stop condition
Return one storyboard draft or one focused sequence patch.

---

## 8. storyboard-review-agent execution spec

### role
storyboard-review-agent

### objective
Diagnose clarity, coverage, rhythm, and production practicality of the storyboard layer.

### owned layer
visual diagnosis and routing

### required inputs
- approved script
- approved hook board
- active storyboard draft

### required output format
- what already works
- clarity issues
- coverage issues
- pacing / rhythm issues
- production practicality issues
- hook translation check
- must-fix items by owner
- verdict

### must preserve
- distinction between storyboard-only issues and script-caused issues

### must not do
- rewrite storyboard in place instead of diagnosing

### stop condition
Return diagnosis only.

---

## 9. Patch request execution rule

When sending a patch task, the orchestrator should include:
- target owner
- issue summary
- precise location
- severity
- what to keep unchanged
- whether upstream artifact changed first
- expected return scope

This should be consistent across all revision cycles.

---

## 10. Failure handling rule

If a child agent returns output outside scope, the orchestrator should:
1. reject silent cross-layer changes
2. salvage useful in-scope material if possible
3. resend a narrower task if needed
4. escalate only if the issue reveals a structural gap

A weak branch output is not permission to collapse architecture.
