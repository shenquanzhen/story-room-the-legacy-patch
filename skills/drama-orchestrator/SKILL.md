# drama-orchestrator

## Skill purpose

让 OpenClaw 中的任意用户，只要提出类似：
- 帮我做电视剧编排
- 帮我做短剧开发
- 帮我做剧集策划
- 帮我搭一个 season bible
- 帮我从命题做到可拍资产
- 帮我做连续剧 / 短剧 / 家庭伦理剧 / 都市剧 / 反转剧的完整编排

这类需求时，agent 能自动唤醒一个**电视剧/短剧总控型工作流**，并按结构化 pipeline 推进，而不是停留在泛泛 brainstorm。

这个 skill 的目标不是只写梗概，而是让 agent 像一个：
- showrunner
- writers' room orchestrator
- production-prep coordinator

去持续推进一个故事项目。

---

## When to use this skill

当用户表达以下任一类意图时，应该使用本 skill：

### A. 新剧项目开发
- “帮我做一个新短剧项目”
- “我有一个命题，帮我开发成电视剧”
- “帮我做一季剧”
- “从一个点子开始帮我做成完整剧集项目”

### B. 连续剧 / 短剧编排
- “帮我做电视剧编排”
- “帮我排一季剧”
- “帮我做 episode map”
- “帮我设计全季结构”

### C. 从创意推进到执行层资产
- “帮我把这个故事做到可拍”
- “帮我做导演分场 / 制片统筹”
- “帮我一路推进到 production assets”

### D. 希望 agent 自主推进
尤其当用户明确说：
- 不要反复确认继续
- 你自己决定推进顺序
- 直接做到完整结果
- 按最合理 pipeline 自主推进

---

## Do NOT use this skill for

以下情况不应优先使用本 skill：

1. 用户只问一个简单剧情点子，不要求结构化开发
2. 用户只要一句 logline / 几个标题选项
3. 用户只要润色某一小段对白
4. 用户只是让你读某个现成剧本，不需要重新搭 pipeline
5. 用户明确说只做单场、单集、单句，而不需要 season / project 级推进

这些情况应用普通故事协助方式，而不是拉起全套 orchestrator workflow。

---

## What this skill does

一旦触发，本 skill 会指导 agent 进入以下工作模式：

### 1. 把任务视为“项目”，不是单条回复
先建立：
- task brief
- 项目目录
- 分层资产结构

### 2. 采用多工位 writers' room 思路
默认使用以下角色分工：
- plot-agent
- character-agent
- script-agent
- review-agent
- storyboard-agent
- storyboard-review-agent

### 3. 按阶段推进，而不是直接写到底
推荐推进链条：
1. series brief
2. season bible
3. episode map
4. continuity skeleton
5. full script / batch scripts
6. checkpoint / review
7. season assembly package
8. 按需延伸到：
   - 逐集精修台词
   - 导演分场
   - 拍摄对白压缩
   - 金句提炼
   - 场景清单
   - 制片拆景
   - 通告 / 日程 / 高能场保护

### 4. 文件优先
默认把结果落成结构化文件，而不是只停留在聊天里。

### 5. 少打断、强推进
如果用户没有提出冲突要求，应默认：
- 少确认
- 多推进
- 在关键里程碑汇总，而不是每小步都停下来问

---

## Workspace / space behavior

当 skill 被调用时，应优先这样做：

### 情况A：当前已经在合适的长期 story workspace 中
则直接在当前 workspace 内，建立新的项目目录：

```text
projects/<project-name>/
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

### 情况B：当前不是合适的 story workspace，或用户明确要新开独立 agent / 新 space
应：
1. 创建或建议创建一个新的 story-oriented workspace
2. 复制方法层文件（而不是旧项目资产）
3. 以该新 space 作为新的长期工作空间

### 绝对原则
- 复制 workflow，不复制旧故事记忆
- 不默认继承任何旧项目剧情、人物、世界观、continuity
- 不把 `.openclaw/` 运行态状态文件当成模板内容继承

---

## Files / folders this skill assumes exist or should be created

### 推荐保留的方法层文件
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`
- `BOOTSTRAP.md`
- `routing-matrix.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `continuity-protocol.md`
- `season-pipeline.md`
- `season-orchestrator-playbook.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`

### 新项目启动时应优先创建的文件
- `projects/<project>/00_admin/task-brief.md`

---

## This skill reuses existing repository docs instead of duplicating them

为了避免 skill 目录内部再维护一套重复的 README / INSTALL / examples / prompts 文档，本 skill 默认**复用仓库级现有文档**。

### 1. 依赖哪些现有文档
本 skill 的实际能力边界与工作方式，依赖于以下现有文档：

#### 身份与用户偏好
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`

#### 多代理分工与总控规则
- `AGENTS.md`
- `routing-matrix.md`
- `agent-contracts.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `autonomy-policy.md`

#### 工作流入口
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `workflows/task-entry.md`
- `workflows/storyboard-pipeline.md`

#### 模板入口
- `templates/`

#### 长线季播 / orchestration 规则
- `season-pipeline.md`
- `season-orchestrator-playbook.md`
- `season-review-protocol.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`

#### 新 agent / new space 启动说明
- `SETUP.md`
- `BOOTSTRAP.md`
- `迁移当前工作流到新Agent与新Space所需文档清单.md`

### 2. 新用户推荐阅读顺序
如果一个第一次接触本 skill 的用户想快速理解怎么使用，推荐阅读顺序如下：

1. `README.md` 或 `README_EN.md`
2. `SETUP.md`
3. `SOUL.md`
4. `USER.md`
5. `AGENTS.md`
6. `workflows/comic-pipeline.md`
7. `workflows/runbook.md`
8. `workflows/task-entry.md`
9. `workflows/storyboard-pipeline.md`（如涉及视觉 / production）
10. `templates/`（按任务需要打开具体模板）

### 3. 本 skill 不重复维护 README / INSTALL
本 skill 的设计原则是：
- **skill 目录只保留一份核心 `SKILL.md`**
- 仓库级说明统一复用：
  - `README.md`
  - `README_EN.md`
  - `SETUP.md`
  - 迁移说明与 workflow 文档

也就是说：
- 不额外新增 `skills/drama-orchestrator/README.md`
- 不额外新增 `skills/drama-orchestrator/INSTALL.md`
- 不额外新增 `skills/drama-orchestrator/examples.md`
- 不额外新增独立 prompts / references 目录

这样可以减少重复维护，并保证 skill 与仓库主体说明始终一致。

### 4. 示例项目入口
如果使用者想看一个完整示例项目是如何从命题一路推进到 production 资产的，可直接查看：
- `projects/perfect-heir/`

注意：
- 它是 **sample project**
- 用于理解 workflow 与资产层级
- 不应默认被新项目继承为故事上下文

### 5. 模板入口
如果使用者想知道具体交付文件“应长成什么样”，应优先查看：
- `templates/`

包括但不限于：
- story outline
- season bible
- scene script
- review checklist
- storyboard sheet
- storyboard review
- continuity ledger

### 6. 工作流入口
如果使用者想知道本 skill 实际遵循什么 pipeline，应优先查看：
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `workflows/task-entry.md`
- `workflows/storyboard-pipeline.md`

这四份文件，分别回答：
- 默认故事生产 loop 是什么
- 接任务后怎么分类与推进
- 怎么把自然语言需求转成 task brief
- 如果要继续到导演/视觉层怎么接

---

## Standard execution flow

被触发后，建议 agent 按如下显性顺序推进：

### Step 1. 识别用户任务类型
判断是：
- 新剧项目
- 季度开发
- 单集开发
- 已有剧本扩展
- 创意到可拍推进

### Step 2. 建立 task brief
最少写清：
- 项目名
- 类型 / 题材
- 核心命题
- target deliverable
- opening hook
- audience question
- emotional payoff promise
- cliffhanger target
- 约束条件
- 是否为全新项目

### Step 3. 建立项目目录
在 `projects/<project-name>/` 下建层级目录。

### Step 4. 做前置分工（可并行）
默认先跑：
- plot-agent
- character-agent
- review-agent / 风险顾问

### Step 5. 合并基础开发资产
产出：
- series brief
- season bible
- episode map
- continuity skeleton

### Step 6. 推进剧本主链
产出：
- batch scripts / season scripts
- midpoint checkpoint
- season completion
- season assembly package

### Step 7. 若用户需要执行层，继续往下推
产出：
- dialogue polish
- director breakdown
- shooting dialogue cuts
- promo quote extraction
- production scene lists
- production breakdowns
- schedule / protection assets

### Step 8. 里程碑式汇报
默认以里程碑更新，而不是每步打断。
但如果用户明确偏好信息流更新，可切换为实时短汇报模式。

---

## Output style guidance

当 skill 被唤醒后，agent 在对用户输出时应：
- 讲清现在推进到哪一层
- 用简洁但专业的方式说明新增资产
- 少问“要不要继续”
- 只在方向不足、信息冲突、路径分叉过大时才停下来确认

### 默认语气
- 直接
- 不空泛
- 不过度兴奋
- 偏 showrunner / 总控
- 偏生产语言，而不是散文化创作语言

---

## Naming and structure guidance

### 推荐命名
新项目目录建议使用简洁英文 slug，例如：
- `projects/perfect-heir/`
- `projects/broken-oath/`
- `projects/final-daughter/`

### 文件命名建议
优先清晰、层级化、可搜索：
- `series-brief.md`
- `season-bible.md`
- `episode-map.md`
- `continuity-skeleton.md`
- `batch1-full-script.md`
- `导演分场版·上半季（1-12集）.md`

---

## What this skill should protect against

本 skill 需要特别避免以下问题：

1. **直接继承旧故事**
   - 新项目必须是新项目，除非用户明确要求继承

2. **没有 task brief 就开始写**
   - 会导致后续结构漂移

3. **一开始就做太细的内容**
   - 应该先锁 brief / bible / map / continuity

4. **总控自己包办一切，不做 lane 分工**
   - 会降低清晰度与可维护性

5. **停在大纲层不落盘**
   - 本 skill 的价值在于形成资产，而不是只聊天

6. **拍摄执行层提前介入**
   - 没锁 script 前不要急着做 production 资产

---

## Trigger phrases (examples)

以下表述都应高概率触发本 skill：
- 帮我做电视剧编排
- 帮我做短剧开发
- 帮我把这个命题做成一季剧
- 帮我从概念做到全季资产
- 帮我做一个完整短剧项目
- 帮我做 season bible / episode map / continuity
- 帮我做到可拍
- 帮我像 showrunner 一样推进这个项目

---

## Suggested first response pattern

当 skill 被唤醒时，建议 agent 第一轮不要立刻散聊，而是直接进入项目化语言，例如：

- 先确认这是一个新项目 / 还是已有项目延展
- 简述将采用的 pipeline
- 说明将先建立 task brief 与项目目录
- 如果信息足够，直接开始推进并落盘

---

## Example promise to the user

触发后，agent 可以采用这种承诺方式：

> 我会把这件事当成一个完整剧集项目推进，而不是只给你一段 brainstorming。先立项、再锁结构、再推剧本、再做可拍层资产；除非信息不足或方向冲突，否则中间不反复打断你。

---

## Final summary

如果要用一句话概括这个 skill：

> **这是一个“电视剧 / 短剧总控编排 skill”，用于把用户的故事命题自动升级成一个可持续推进、可分工协作、可落盘交付的完整 story production pipeline。**
