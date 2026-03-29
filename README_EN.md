# story-room-the-legacy-patch

A multi-agent writing and production workflow repository for **long-form serialized story development**.

This repository is not just about “writing a story.” It is designed to carry a new story project all the way from **concept → structure → scripts → dialogue polish → director breakdown → production planning → promo support assets**.

> While the current workspace originally focused on Chinese short drama / urban family ethics / high-hook serialized storytelling, the real value of this repository is not tied to one genre.
> Its value is in the workflow: **how to move a new story project from idea to a reusable, handoff-ready asset system.**

---

# What this repository is

This repository is best understood as:

- a **story orchestrator** workspace
- a **multi-agent writers' room** operating system
- a structured pipeline for serialized story production
- a file-first, handoff-friendly creative environment

It is meant to answer not only:
- what to write

but also:
- what to do first
- what to do next
- which specialist role should do what
- when to stop
- how to preserve outputs as reusable assets

---

# Best use cases

## Good fit
- launching a brand-new story project from scratch
- developing a concept into season-level assets
- coordinating parallel lanes such as plot / character / script / review / storyboard
- continuing from story development into director and production support layers
- keeping results in files rather than buried in chat logs

## Not ideal for
- casual one-off brainstorming only
- tiny standalone answers with no asset trail
- projects that do not need structure, review loops, or reusable files

---

# Core philosophy

This repository is built around a few strong defaults:

1. **structure before flourish**
2. **hook and conflict before scene expansion**
3. **the orchestrator decides and merges; specialists handle lanes**
4. **less idle discussion, more written assets**
5. **stop at useful completion rather than polishing forever**
6. **every output layer should feed the next one**

This is not an inspiration scrapbook.
It is a **story production system**.

---

# Repository overview

## Identity and personality layer
- `SOUL.md` — core personality, boundaries, tone, working philosophy
- `USER.md` — user preferences and collaboration style
- `IDENTITY.md` — name, vibe, self-definition
- `MEMORY.md` — long-term method memory (project-specific memory should be handled carefully)

## Multi-agent / operating rules
- `AGENTS.md` — orchestrator model, child roles, routing, output contracts
- `agent-contracts.md`
- `routing-matrix.md`
- `autonomy-policy.md`
- `state-management.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `continuity-protocol.md`

## Season / long-run playbooks
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `season-pipeline.md`
- `season-review-protocol.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`
- `next-run-briefing-template.md`

## Child role definitions
Located in `agents/`:
- `plot-agent.md`
- `character-agent.md`
- `script-agent.md`
- `review-agent.md`
- `storyboard-agent.md`
- `storyboard-review-agent.md`

## Workflows
Located in `workflows/`:
- `comic-pipeline.md`
- `runbook.md`
- `task-entry.md`
- `storyboard-pipeline.md`

## Templates
Located in `templates/`:
- story outline
- season bible
- scene script
- review checklist
- storyboard sheet
- continuity ledger
- orchestrator prompt
- and more

## Reference examples
Located in `references/`:
- sample season assembly
- sample storyboard package
- sample shot deck package
- etc.

---

# Core workflow (short version)

A typical pipeline in this repository looks like this:

1. **normalize the incoming task**
2. **series brief**
3. **season bible**
4. **episode map**
5. **continuity skeleton**
6. **batch scripts**
7. **review / checkpoint**
8. **season assembly package**
9. **episode-level dialogue polish**
10. **director scene breakdown**
11. **shooting dialogue compression**
12. **promo quote extraction**
13. **scene lists**
14. **production breakdowns / schedule-ready assets**
15. **high-intensity scene protection / execution aids**

You can stop earlier if your task ends sooner, but the system is designed so that each layer naturally feeds the next one.

---

# Child roles

Default specialist lanes include:

- **plot-agent** — concept, structure, reversals, beats, hook map
- **character-agent** — cast package, relationship map, voice, contradiction points
- **script-agent** — scene writing, dialogue, pacing, dramatic flow
- **review-agent** — logic review, pacing review, hook diagnosis, revision direction
- **storyboard-agent** — director-facing scene and visual breakdown
- **storyboard-review-agent** — execution review of storyboard / director breakdown material

The value is not “more agents,” but **clear responsibility separation**.

---

# How to use this repo for a new project

## Minimum startup reading
For a fresh project, start with:

1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md` (if visual / directing layers matter)

Then:
- create a fresh project directory
- write a `task-brief.md`
- push the project forward layer by layer

## Suggested project folder structure
A practical structure looks like this:

```text
projects/<your-project>/
  00_admin/
  01_brief/
  02_bible/
  03_structure/
  04_continuity/
  05_scripts/
  06_storyboard/
  06_production/
  07_checkpoint/
  08_scripts/season_complete/
  09_assembly/
```

You may adapt this, but the key principle is: **clear layers, reusable files, clean handoff points**.

---

# If you want the workflow, not the current story project

If your goal is:
- to reuse the workflow,
- but **not** inherit the current story's plot, characters, or project memory,

then migrate:

## Must keep
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`

## Strongly recommended
- `autonomy-policy.md`
- `continuity-protocol.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `routing-matrix.md`
- `season-pipeline.md`
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`

## Do NOT directly carry over
- any concrete project directory such as `projects/perfect-heir/`
- story-specific bibles, scripts, assembly packages, production assets

Short version:

> **Carry over how the work is done, not what was produced.**

There is also a dedicated Chinese reference file in this repo:
- `迁移当前工作流到新Agent与新Space所需文档清单.md`

---

# Suggested reading paths by role

## If you are a writer / story creator
Start with:
- `SOUL.md`
- `AGENTS.md`
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `templates/story-outline.md`
- `templates/scene-script.md`
- `templates/season-bible.md`

## If you are using this as an orchestrator system
Start with:
- `AGENTS.md`
- `routing-matrix.md`
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `merge-protocol.md`
- `revision-protocol.md`

## If you also care about directing / production handoff
Also read:
- `workflows/storyboard-pipeline.md`
- `templates/storyboard-sheet.md`
- `templates/storyboard-review.md`
- `continuity-protocol.md`
- `delivery-spec.md`

---

# What makes this repo different

## 1. It does not stop at premise or outline
Many writing setups stop at logline / premise / outline.
This one is designed to continue into:
- scripts
- polished dialogue
- director-facing breakdowns
- production planning assets

## 2. It is built for orchestration, not solo drafting only
This repository assumes a room, not a lone writer.
The orchestrator does not need to write every lane directly.
It assigns, merges, reviews, and decides.

## 3. It is file-first
The outputs are meant to live as:
- folders
- assets
- checkpoints
- reusable handoff documents

not just chat output.

## 4. It supports production handoff
If you want material that can move from writing into directing / producing / scheduling layers, this setup is especially useful.

---

# Important cautions

## 1. Do not leak old project memory into a new project by default
Especially avoid carrying forward:
- plot state
- character state
- continuity state
- production planning tied to a previous story

## 2. Keep MEMORY method-oriented if reused
Long-term memory should preserve:
- style
- workflow habits
- collaboration preferences

But story-specific memory should not automatically become the next project's default context.

## 3. Structure first, polish second
This repo works best if you resist the urge to over-polish too early.
Do not:
- over-polish scenes before the season structure is locked
- start director breakdowns before key scenes stabilize
- start production planning before the scene system is coherent

---

# Current repo status

This repository currently contains one full example project path in practice, but that should not automatically be treated as default inherited material for future projects.

If you publish this repo publicly on GitHub, consider clearly separating:
- **method layer** files (reusable)
- **project layer** files (example / sample only)

You may even move sample projects into:
- `examples/`
- or a separate showcase repository

---

# Who this is for

This repository is especially useful for:
- users building long-lived story agents
- people who want AI to do more than “write text”
- teams developing serialized drama / short drama pipelines
- creators who need writing + directing + production handoff continuity

---

# License / publishing suggestions

If you publish this on GitHub, consider adding:
- `LICENSE`
- `CONTRIBUTING.md`
- `CHANGELOG.md`

At the moment, the repo functions more like a **custom story-room operating system** than a generic lightweight template.

---

# One-line summary

If you only remember one sentence about this repository:

> This is not just an agent setup that can write stories — it is a story production system designed to let an agent work like a showrunner, orchestrator, and production handoff layer across a full serialized pipeline.
