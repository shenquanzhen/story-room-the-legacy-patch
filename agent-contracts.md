# story-room agent contracts

This file defines stable interfaces for specialist child agents.

Principle: each agent owns a narrow layer of the pipeline. No agent should silently absorb another layer's responsibilities.

---

## 1. plot-agent contract

### Owns
- premise clarity
- conflict spine
- episode beat progression
- macro hook design
- reversal placement
- cliffhanger design

### Inputs
- task brief
- genre flavor
- episode scope
- protagonist setup
- pressure / humiliation setup
- comeback fantasy
- constraints

### Must output
- logline
- premise
- protagonist goal
- antagonist pressure
- episode beat outline
- hook map
  - opening hook
  - suspense question
  - first reversal
  - payoff turn
  - cliffhanger
- unresolved questions
- risks

### Must not own
- full scene dialogue
- detailed relationship psychology beyond story function
- shot-by-shot visual planning

---

## 2. character-agent contract

### Owns
- cast readability
- desire / fear / contradiction design
- relationship tension
- motivation clarity
- emotional pivot design
- voice differentiation

### Inputs
- task brief
- plot summary or premise
- protagonist pressure setup
- comeback fantasy
- relationship context

### Must output
- main cast sheet
- motivations
- relationship tensions
- voice cues
- contradiction points
- emotional pivots
- character hook points
  - sympathy trigger
  - anger trigger
  - desire trigger
  - vulnerability point

### Must not own
- beat outline authority
- final scene structure
- camera language

---

## 3. script-agent contract

### Owns
- scene construction
- conflict execution
- dialogue rhythm
- reveal timing inside scenes
- scene exits and forward pull

### Required inputs
- approved task brief
- current outline
- current character package
- episode hook board

Script-agent should not draft without a hook board unless explicitly instructed.

### Must output
- numbered scenes
- scene goal
- conflict in each scene
- dialogue draft
- turn / reversal in each scene
- exit hook in each scene
- cliffhanger ending
- known weak points

### Per-scene structure
For every scene, include:
- scene hook
- scene goal
- conflict escalation
- turn / reversal
- exit hook

### Must not own
- replacing the hook spine on its own
- changing core motivations without flagging it
- inventing storyboard coverage as a substitute for scene writing

---

## 4. review-agent contract

### Owns
- diagnosis
- weakness detection
- routing of must-fix items
- ship / revise judgment

### Inputs
- hook board
- outline
- character package
- script draft or storyboard draft
- current task goal

### Must output
- what already works
- hook diagnosis
- logic diagnosis
- payoff diagnosis
- must-fix items by owner
- optional punch-ups
- verdict: ship / revise

### Routing rule
Review-agent should route issues to the smallest responsible owner:
- premise / beat / cliffhanger problem -> plot-agent
- motive / relationship / voice problem -> character-agent
- scene execution / dialogue / pacing problem -> script-agent
- visual clarity / coverage / production practicality problem -> storyboard-agent

### Must not own
- silently rewriting the script in place instead of diagnosing
- broad aesthetic notes without location or owner

---

## 5. storyboard-agent contract

### Owns
- visual hook translation
- shot-by-shot coverage
- framing / movement choices
- reveal image design
- cliffhanger final image
- production efficiency at shot level

### Required inputs
- approved script
- hook board
- tone / style notes
- production constraints when available

### Must output
- shot list by scene
- shot purpose
- framing / angle / movement
- covered action or dialogue
- visual hook
- reveal shot
- cliffhanger image
- production efficiency notes
- known weak points

### Must not own
- rewriting major story logic without flagging back to script layer
- inventing emotional beats unsupported by the script

---

## 6. storyboard-review-agent contract

### Owns
- visual clarity review
- coverage review
- pacing / rhythm review
- production practicality review
- ship / revise judgment for storyboard layer

### Inputs
- approved script
- hook board
- storyboard draft
- production constraints when available

### Must output
- what already works
- clarity issues
- coverage issues
- pacing / rhythm issues
- production practicality issues
- must-fix items
- optional punch-ups
- verdict: ship / revise

### Must not own
- rewriting the script unless the root cause is explicitly identified

---

## 7. orchestrator rules

The orchestrator owns:
- request classification
- task brief quality
- hook board merge
- branch spawning
- review routing enforcement
- stop conditions
- final package assembly

### Core rule
No full drafting branch should begin before the orchestrator can state the episode hook spine clearly.

### Merge rule
The orchestrator should merge plot-agent + character-agent outputs into a hook board before script drafting.

### Revision rule
Patch the smallest broken layer first.
Do not restart the whole room unless the premise or hook spine is broken.

### Stop rule
Default maximum:
- first draft
- one focused revision round
- one final polish round only if justified
