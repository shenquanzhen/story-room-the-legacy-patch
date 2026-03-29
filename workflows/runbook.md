# runbook.md

## story-room runbook

Use this file as the operating guide for real jobs.

## Step 1 - Classify request
Classify incoming requests into one of:
- concept-package
- pilot-package
- rewrite-package
- expansion-package
- storyboard-package
- storyboard-rewrite-package

## Step 2 - Build task brief
Create a short structured brief with:
- target type
- genre flavor
- protagonist identity
- pressure / humiliation setup
- payoff fantasy
- audience question
- first slap-back promise
- episode cliffhanger target
- episode scope
- special constraints

## Step 3 - Build hook board inputs first
Before scene drafting, identify the core hook stack:
- opening hook
- protagonist pressure point
- audience suspense question
- first reversal
- emotional payoff beat
- episode-end cliffhanger

These inputs should be explicit, not implied.

## Step 4 - Spawn branches
### For concept-package
Spawn:
- plot-agent
- character-agent
Then merge a hook board
Then spawn:
- review-agent

### For pilot-package
Spawn in parallel:
- plot-agent
- character-agent
Then merge a hook board
Then spawn:
- script-agent
Then spawn:
- review-agent
If script is approved and the user wants visual planning, continue with:
- storyboard-agent
- storyboard-review-agent

### For rewrite-package
Spawn:
- review-agent first
Have review-agent identify whether the break is mainly in:
- hook
- logic
- payoff
Then send focused changes to:
- plot-agent or character-agent or script-agent
Patch the hook board if the episode spine changed

### For storyboard-package
Require a usable script first.
Also require a clear hook board or equivalent script spine.
Spawn:
- storyboard-agent
Then spawn:
- storyboard-review-agent

### For storyboard-rewrite-package
Spawn:
- storyboard-review-agent first
Then send focused changes to:
- storyboard-agent
If the storyboard problem comes from the script, patch script first, then regenerate the affected shots only

## Step 5 - Merge
Merge outputs into one package with sections as needed:
- title options
- hook board
- logline
- premise
- cast
- outline
- script
- script revision notes
- storyboard shot list
- storyboard revision notes
- production / continuity notes

## Step 6 - Stop condition
Stop after:
- first useful draft + one revision pass
or
- first useful draft + one revision + one polish if clearly justified

Do not endlessly recurse.
