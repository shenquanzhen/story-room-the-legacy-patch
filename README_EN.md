[**中文**](./README.md) | [**English**](./README_EN.md)

# story-room-the-legacy-patch

![Status](https://img.shields.io/badge/status-active-success)
![Language](https://img.shields.io/badge/language-Chinese%20%2F%20English-blue)
![Workflow](https://img.shields.io/badge/workflow-multi--agent-orange)
![Focus](https://img.shields.io/badge/focus-story%20production-purple)

A multi-agent writing and production workflow repository for **long-form serialized story development**.

This repository is not just about “writing a story.” It is designed to carry a new story project all the way from **concept → structure → scripts → dialogue polish → director breakdown → production planning → promo support assets**.

> While the current workspace originally focused on Chinese short drama / urban family ethics / high-hook serialized storytelling, the real value of this repository is not tied to one genre.
> Its value is in the workflow: **how to move a new story project from idea to a reusable, handoff-ready asset system.**

---

# Table of Contents
- [What this repository is](#what-this-repository-is)
- [Quick Start](#quick-start)
- [How to create a new agent / workspace](#how-to-create-a-new-agent--workspace)
- [Best use cases](#best-use-cases)
- [Core philosophy](#core-philosophy)
- [Repository overview](#repository-overview)
- [Core workflow (short version)](#core-workflow-short-version)
- [Child roles](#child-roles)
- [How to use this repo for a new project](#how-to-use-this-repo-for-a-new-project)
- [Example project](#example-project)
- [If you want the workflow, not the current story project](#if-you-want-the-workflow-not-the-current-story-project)
- [Suggested reading paths by role](#suggested-reading-paths-by-role)
- [What makes this repo different](#what-makes-this-repo-different)
- [Important cautions](#important-cautions)
- [Current repo status](#current-repo-status)
- [Who this is for](#who-this-is-for)
- [License / publishing suggestions](#license--publishing-suggestions)

---

# What this repository is

This repository is best understood as:
- a story orchestrator workspace
- a multi-agent writers' room operating system
- a structured pipeline for serialized story production
- a file-first, handoff-friendly creative environment

---

# Quick Start

## 1. Read the core files first
At minimum, read:
1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md` (if you also care about directing / production layers)

## 2. Create a fresh project folder
Suggested structure:

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

## 3. Start with a task brief
Create:
- `00_admin/task-brief.md`

## 4. Move down the pipeline
Recommended order:
1. series brief
2. season bible
3. episode map
4. continuity skeleton
5. batch scripts
6. review / checkpoint
7. season assembly package
8. dialogue / storyboard / production extensions

## 5. If you only want the workflow
See:
- `SETUP.md`
- `迁移当前工作流到新Agent与新Space所需文档清单.md`

---

# How to create a new agent / workspace

If your goal is not to continue the current sample project, but instead:
- create a new agent
- open a new workspace / space without inheriting the old story

then use this rule:

## Keep the method layer
Must keep:
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`

## Do not inherit old project assets by default
Do not automatically inherit:
- `projects/perfect-heir/`
- old plot / characters / continuity
- old production assets
- `.openclaw/`

## Create a fresh project directory
Use:

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

## Start with `task-brief.md`
That should always be the first file.

## For a fuller explanation
Read:
- `SETUP.md`

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

1. structure before flourish
2. hook and conflict before scene expansion
3. the orchestrator decides and merges; specialists handle lanes
4. less idle discussion, more written assets
5. stop at useful completion rather than polishing forever
6. every output layer should feed the next one

---

# Repository overview

## Identity and personality layer
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `MEMORY.md`

## Multi-agent / operating rules
- `AGENTS.md`
- `agent-contracts.md`
- `routing-matrix.md`
- `autonomy-policy.md`
- `state-management.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `continuity-protocol.md`

## Playbooks / specs
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `season-pipeline.md`
- `season-review-protocol.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`
- `next-run-briefing-template.md`

## Child role definitions
In `agents/`

## Workflows
In `workflows/`

## Templates
In `templates/`

## Reference examples
In `references/`

---

# Core workflow (short version)

1. normalize the incoming task
2. series brief
3. season bible
4. episode map
5. continuity skeleton
6. batch scripts
7. review / checkpoint
8. season assembly package
9. episode-level dialogue polish
10. director scene breakdown
11. shooting dialogue compression
12. promo quote extraction
13. scene lists
14. production breakdowns / schedule-ready assets
15. high-intensity scene protection / execution aids

---

# Child roles

Default specialist lanes include:
- plot-agent
- character-agent
- script-agent
- review-agent
- storyboard-agent
- storyboard-review-agent

---

# How to use this repo for a new project

Start by reading the core method files, then create a fresh project directory and begin with a task brief.

---

# Example project

This repository currently contains one full sample project:
- `projects/perfect-heir/`

It exists to demonstrate how the workflow can run end to end.
It should not be treated as default inherited story context for new projects.

---

# If you want the workflow, not the current story project

Carry over:
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`
- method-layer protocols and playbooks

Do not directly carry over:
- project-specific assets
- old scripts
- old continuity
- `.openclaw/`

---

# Suggested reading paths by role

Different readers can enter through:
- writing / creative layer
- orchestrator / system layer
- directing / production handoff layer

---

# What makes this repo different

- it does not stop at premise or outline
- it is built for orchestration, not solo drafting only
- it is file-first
- it supports production handoff

---

# Important cautions

- do not leak old project memory into a new project by default
- keep MEMORY method-oriented if reused
- structure first, polish second

---

# Current repo status

This repo currently contains both:
- reusable method-layer files
- one sample project path

If you publish it publicly, make that distinction explicit.

---

# Who this is for

This repository is useful for:
- long-lived story agents
- serialized drama pipelines
- creators who want writing + directing + production continuity

---

# License / publishing suggestions

If you publish this repo on GitHub, consider adding:
- `LICENSE`
- `CONTRIBUTING.md`
- `CHANGELOG.md`

---

# One-line summary

> This is not just an agent setup that can write stories — it is a story production system designed to let an agent work like a showrunner, orchestrator, and production handoff layer across a full serialized pipeline.
