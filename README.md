# OpenClaw 全季（多集）剧本自动化生成

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
- [如何新建一个 agent / workspace](#如何新建一个-agent--workspace)
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
- [当前仓库状态说明（含 GitHub 推送 / Passkey）](#当前仓库状态说明)
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

# 如何新建一个 agent / workspace

如果你的目标不是继续当前项目，而是：
- 新建一个新 agent
- 新开一个不继承旧故事内容的 workspace / space

推荐这样做：

## 1. 保留方法层文件
必须保留：
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`

## 2. 不要继承旧项目资产
不要默认继承：
- `projects/perfect-heir/`
- 旧项目剧情
- 旧角色与 continuity
- 旧 production 资产

## 3. 新建自己的项目目录
直接创建：

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

## 4. 第一份文件一定先写 `task-brief.md`
这是整个 pipeline 的起点。

## 5. 更详细说明
请直接看：
- `SETUP.md`
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
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `MEMORY.md`

## 多代理与运行规则层
- `AGENTS.md`
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
位于 `agents/`

## 工作流
位于 `workflows/`

## 模板
位于 `templates/`

## 参考样例
位于 `references/`

---

# 核心工作流（简版）

1. 任务入口标准化
2. series brief
3. season bible
4. episode map
5. continuity skeleton
6. batch scripts
7. review / checkpoint
8. season assembly package
9. 逐集精修台词
10. 导演分场
11. 拍摄对白压缩
12. 宣发金句提炼
13. 场景清单
14. 制片拆景与拍摄统筹
15. 高能场保护与执行辅助资产

---

# 多代理角色设计

默认 child roles：
- plot-agent
- character-agent
- script-agent
- review-agent
- storyboard-agent
- storyboard-review-agent

---

# 如何在新项目中使用

建议新项目启动时至少先读：
- `SOUL.md`
- `USER.md`
- `AGENTS.md`
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `workflows/task-entry.md`
- `workflows/storyboard-pipeline.md`

---

# 示例项目说明

当前仓库中已经包含一个完整项目案例：
- `projects/perfect-heir/`

该项目展示了如何把一个新命题从：
- brief
- bible
- episode map
- continuity
- script
- dialogue
- director breakdown
- production planning
一路推进到可交接的多层资产包。

### 注意
它是 sample，不是默认继承内容。

---

# 如果你要复制这套工作流，而不是复制当前项目

推荐迁移：
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`
- 各类 protocol / playbook / spec

不要直接迁移：
- 具体项目资产目录
- 旧 story bible / script / production 文件
- `.openclaw/`

---

# 推荐阅读顺序

按角色可参考：
- 编剧 / 创作者
- 总控 / orchestration
- 导演 / 制片 / 执行

（详见仓库其他说明文件）

---

# 仓库特色

- 不停留在“写梗概”
- 不是单人创作，而是可持续 orchestration
- 输出默认文件化
- 适合 production handoff

---

# 注意事项

- 不要把旧项目记忆直接混入新项目
- MEMORY 只建议保留方法性长期记忆
- 分工越清楚，review 越好做
- 先锁结构，再做精修

---

# 当前仓库状态说明
当前仓库同时包含：
- 可复用方法层
- 一个完整 sample project

如果对外发布，建议明确区分二者角色。

## 推送到 GitHub（Passkey / 浏览器登录）

命令行里的 `git` 不能直接扫 Passkey。推荐用 **GitHub CLI（`gh`）** 打开浏览器登录（网页可用 Passkey），由 `gh` 配置 HTTPS 凭据后再 `git push`。

**环境：** 本地 **WSL**，目录 `/root/.openclaw/story-room-the-legacy-patch`（按实际 home 调整）。

```bash
sudo apt update && sudo apt install -y gh   # 若未安装
cd /root/.openclaw/story-room-the-legacy-patch
gh auth login    # 选 GitHub.com、HTTPS、浏览器登录

git add -A && git status
git commit -m "chore: sync"    # 有变更时再提交
git branch -M main
git remote add origin https://github.com/<用户>/<仓库>.git   # 首次
git push -u origin main
```

**成功：** 显示 Writing objects 100%，远端能看到文件。**失败：** `Authentication failed` → 重跑 `gh auth login`；`remote origin already exists` → `git remote remove origin` 后重加。勿把 Token 写进 remote URL。

---

# 适合谁

- 长期运行故事 agent 的使用者
- 想把 AI 从“会写”推进到“会做项目”的人
- 中文短剧 / 连续剧开发团队
- 需要创作与 production handoff 连通的人

---

# License / 使用建议
如果你要公开发布到 GitHub，建议补充：
- `LICENSE`
- `CONTRIBUTING.md`
- `CHANGELOG.md`

---

# 最后一段

> 它不是“一个会写故事的 agent 配置”，而是一套让 agent 以 showrunner / orchestration / production handoff 方式持续工作的故事生产系统。
