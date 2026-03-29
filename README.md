# story-room-the-legacy-patch

![Status](https://img.shields.io/badge/status-active-success)
![Language](https://img.shields.io/badge/language-Chinese%20%2F%20English-blue)
![Workflow](https://img.shields.io/badge/workflow-multi--agent-orange)
![Focus](https://img.shields.io/badge/focus-story%20production-purple)

一个面向**长线序列化故事开发**的多代理写作与生产工作流仓库。  
它不是单纯的“写一个故事”，而是把**故事开发、剧本精修、导演分场、制片统筹、宣发辅助**整合进一套可复用的 pipeline 中。

> 当前仓库最初用于中文短剧/都市家庭伦理/强钩子叙事方向，但其核心价值不在单一题材，而在于：
> **如何把一个新故事项目，从概念一路推进到可拍、可统筹、可交接的多层资产包。**

---

# 目录导航
- [仓库定位](#仓库定位)
- [快速开始](#快速开始)
- [适合什么场景](#适合什么场景)
- [核心理念](#核心理念)
- [仓库结构总览](#仓库结构总览)
- [核心工作流（简版）](#核心工作流简版)
- [多代理角色设计](#多代理角色设计)
- [如何在新项目中使用](#如何在新项目中使用)
- [示例项目说明](#示例项目说明)
- [如果你要复制这套工作流，而不是复制当前项目](#如果你要复制这套工作流而不是复制当前项目)
- [推荐阅读顺序](#推荐阅读顺序)
- [仓库特色](#仓库特色)
- [注意事项](#注意事项)
- [当前仓库状态说明](#当前仓库状态说明)
- [适合谁](#适合谁)
- [License--使用建议](#license--使用建议)

---

# 仓库定位

这个仓库的核心定位是：

- 一个 **story orchestrator（故事总控）** 的工作底座
- 一个 **multi-agent writers' room（多代理编剧室）** 的操作框架
- 一个从 **brief → bible → episode map → script → review → storyboard → production assets** 的连续生产系统

它适合：
- 短剧 / 连续剧 / 轻季播项目开发
- 需要多角色并行协作的内容团队
- 想把“故事创作”做成结构化生产的人
- 需要长期运行、可持续迭代、可交接的 agent space

它不只是回答“写什么”，更回答：
- 先做什么
- 后做什么
- 谁做什么
- 什么时候停
- 如何把结果留下来

---

# 快速开始

如果你想把这个仓库当成一个**新项目工作流模板**来用，推荐按下面步骤开始。

## 1. 先阅读核心文件
建议至少先看：
1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md`（如果你也要做导演/分场/拍摄层）

## 2. 新建项目目录
建议按如下结构创建：

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

## 3. 先写任务入口
在新项目里先建立：
- `00_admin/task-brief.md`

把以下信息写清楚：
- 项目名
- 类型
- 核心命题
- 目标交付链条
- 约束条件
- opening hook
- audience question
- payoff promise
- cliffhanger target

## 4. 按 pipeline 往下推
推荐顺序：
1. series brief
2. season bible
3. episode map
4. continuity skeleton
5. batch scripts
6. review / checkpoint
7. season assembly package
8. dialogue / storyboard / production 扩展资产

## 5. 如果你只想复制工作流
请看仓库内这份说明：
- `迁移当前工作流到新Agent与新Space所需文档清单.md`

---

# 适合什么场景

## 适合
- 新故事项目从零启动
- 已有概念，需要拆成 season 级资产
- 需要多代理并行做：plot / character / script / review / storyboard
- 需要继续往拍摄执行层推进
- 需要把结果沉淀成文件，而不是散落在聊天记录中

## 不适合
- 只想随便 brainstorm 两句
- 只做一次性短回答
- 完全不需要结构化文件沉淀
- 不需要角色分工、review loop、生产交付链条的项目

---

# 核心理念

这个仓库默认遵循以下原则：

1. **先结构，后文采**
2. **先锁 hook 和 conflict，再扩正文**
3. **总控只负责决策与合并，专项任务交给子角色**
4. **少空聊，多落盘**
5. **不要无限打磨，优先形成可用资产**
6. **每一层产出都要为下一层服务**

换句话说，这不是“灵感仓库”，而是“故事生产仓库”。

---

# 仓库结构总览

## 身份与人格层
- `SOUL.md`：agent 核心人格、边界、语气、工作哲学
- `USER.md`：用户偏好与协作方式
- `IDENTITY.md`：名称、气质、自我识别
- `MEMORY.md`：长期方法性记忆（建议谨慎保留项目性内容）

## 多代理与运行规则层
- `AGENTS.md`：总控模型、子角色分工、责任路由、输出合同
- `agent-contracts.md`
- `routing-matrix.md`
- `autonomy-policy.md`
- `state-management.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `continuity-protocol.md`

## 季播 / 长线开发 playbook
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `season-pipeline.md`
- `season-review-protocol.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`
- `next-run-briefing-template.md`

## 子代理定义
位于 `agents/`：
- `plot-agent.md`
- `character-agent.md`
- `script-agent.md`
- `review-agent.md`
- `storyboard-agent.md`
- `storyboard-review-agent.md`

## 工作流
位于 `workflows/`：
- `comic-pipeline.md`
- `runbook.md`
- `task-entry.md`
- `storyboard-pipeline.md`

## 模板
位于 `templates/`：
- story outline
- season bible
- scene script
- review checklist
- storyboard sheet
- continuity ledger
- orchestrator prompt 等

## 参考样例
位于 `references/`：
- sample season assembly
- sample storyboard package
- sample shot deck package 等

---

# 核心工作流（简版）

这套仓库推荐的典型推进顺序是：

1. **任务入口标准化**
2. **series brief**
3. **season bible**
4. **episode map**
5. **continuity skeleton**
6. **batch scripts**
7. **review / checkpoint**
8. **season assembly package**
9. **逐集精修台词**
10. **导演分场**
11. **拍摄对白压缩**
12. **宣发金句提炼**
13. **场景清单**
14. **制片拆景与拍摄统筹**
15. **高能场保护与执行辅助资产**

你可以在项目里按需停在任一层，但推荐保持“上一层为下一层服务”的顺序。

---

# 多代理角色设计

默认 child roles：

- **plot-agent**：概念、结构、反转、beat、hook map
- **character-agent**：角色包、关系图、voice、矛盾点
- **script-agent**：逐场剧本、对白、节奏、场次推进
- **review-agent**：逻辑审查、节奏审查、hook 诊断、修订建议
- **storyboard-agent**：导演分场、镜头方向、场次视觉化
- **storyboard-review-agent**：导演分场 / storyboard 的执行审查

这个设计的关键不是“多”，而是**每个人只负责自己该负责的那一块**。

---

# 如何在新项目中使用

## 最小启动步骤
建议新项目启动时至少先读：

1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md`

然后：
- 新建项目目录
- 先写 `task-brief.md`
- 再按 pipeline 往下推

## 推荐启动方式
新建一个全新的 `projects/<your-project>/` 目录，按类似层级组织。

---

# 示例项目说明

当前仓库中已经包含一个完整项目案例：
- `projects/perfect-heir/`

该项目展示了如何把一个新命题从以下阶段一路推进：
- brief
- bible
- episode map
- continuity
- full scripts
- dialogue polish
- director breakdown
- shooting dialogue cuts
- promo quotes
- production scene lists
- production breakdowns
- schedule-ready planning assets

## 注意
这个案例项目的作用是：
- **示范 workflow 怎么跑通**
- **示范文件应该长成什么样**

它**不应该**被新项目直接继承为默认故事上下文。

如果你要把这个仓库当模板使用，建议：
- 保留 `projects/perfect-heir/` 作为 sample
- 或者未来把它迁到 `examples/` 目录

---

# 如果你要复制这套工作流，而不是复制当前项目

如果你的目标是：
- 复制当前工作方式
- 但不继承当前具体故事内容

推荐迁移这些文件：

## 必带
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`

## 强烈建议带
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

## 不要直接带
- 任何具体项目目录（如 `projects/perfect-heir/`）
- 任何已有 story bible / script / assembly / production 项目资产

一句话：

> **带走“怎么做”，不要带走“做了什么”。**

仓库中也附了一份独立说明：
- `迁移当前工作流到新Agent与新Space所需文档清单.md`

---

# 推荐阅读顺序

## 如果你是内容创作者 / 编剧
建议先读：
- `SOUL.md`
- `AGENTS.md`
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `templates/story-outline.md`
- `templates/scene-script.md`
- `templates/season-bible.md`

## 如果你是总控 / orchestration 使用者
建议先读：
- `AGENTS.md`
- `routing-matrix.md`
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `merge-protocol.md`
- `revision-protocol.md`

## 如果你也做导演 / 制片层延伸
建议再读：
- `workflows/storyboard-pipeline.md`
- `templates/storyboard-sheet.md`
- `templates/storyboard-review.md`
- `continuity-protocol.md`
- `delivery-spec.md`

---

# 仓库特色

## 1. 不停留在“写梗概”
很多写作型 agent 只会停在 logline / premise / outline。  
这套仓库的特色是：**可以继续往下走到执行层资产。**

## 2. 不是单人创作，而是可持续 orchestration
这里默认是一个 room，而不是一个单枪匹马的 writer。  
总控不必什么都亲写，而是让每条 lane 做自己最擅长的事。

## 3. 输出默认文件化
这个仓库更偏向：
- 文件资产
- 目录结构
- 版本节点
- 可交接

而不是把所有成果留在聊天里。

## 4. 既适合创作，也适合 production handoff
如果你要把故事进一步交给导演、制片、执行层，这套架构特别有用。

---

# 注意事项

## 1. 不要把旧项目记忆直接混入新项目
特别是：
- 人物
- 世界观
- continuity
- scene assets
- production package

## 2. MEMORY 只建议保留方法性长期记忆
项目性记忆建议按项目单独放，不要默认长期继承。

## 3. 分工越清楚，review 越好做
不要让同一子角色同时负责：
- 写初稿
- 给自己评审
- 再自己改自己

## 4. 先锁结构，再做精修
这套仓库最怕的不是“写得不够美”，而是：
- 结构没锁就开始精修
- 台词没稳就开始分场
- 剧本没稳就开始制片拆景

---

# 当前仓库状态说明
这个仓库里已经包含一个完整示范项目开发过程，但它不应该被自动视为新项目默认继承内容。  
如果你想把这里作为模板仓库发布到 GitHub，推荐明确区分：

- **方法层文件**：可复用
- **项目层文件**：仅示范 / 仅案例

如果未来你要公开发布，建议：
- 可以保留项目案例作为 sample
- 也可以把 sample 项目移到 `examples/` 或单独仓库

---

# 适合谁

这个仓库最适合：
- 需要长期运行的故事 agent 使用者
- 想把 AI 从“会写”推进到“会做项目”的人
- 做中文短剧 / 连续剧 / 内容开发 pipeline 的团队
- 想把创作与 production handoff 连起来的人

---

# License / 使用建议
如果你要公开发布到 GitHub，建议补充：
- `LICENSE`
- `CONTRIBUTING.md`
- `CHANGELOG.md`

目前本仓库更像是一个**高度定制化的 story-room operating system**。

---

# 最后一段
如果你只想用一句话理解这个仓库：

> 它不是“一个会写故事的 agent 配置”，而是一套让 agent 以 showrunner / orchestration / production handoff 方式持续工作的故事生产系统。
