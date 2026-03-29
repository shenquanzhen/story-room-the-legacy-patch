# SETUP.md

# 如何新建一个 Agent 与 New Space

这份文档面向第一次拿到本仓库的人，目标是回答两个问题：

1. **如何基于这个仓库新建一个 agent**
2. **如何基于这个 agent 新开一个不继承旧故事内容的新 space / 新项目空间**

> 核心原则：
> **复制工作流，不复制旧项目剧情。**

---

## 一、先理解三件事

### 1. 这个仓库里有什么
这个仓库主要有两类内容：

#### A. 方法层（可复用）
包括：
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`
- 各类 protocol / playbook / spec 文档

这些决定的是：
- agent 是谁
- 如何工作
- 如何拆任务
- 如何交付

#### B. 项目层（不要默认继承）
包括：
- `projects/perfect-heir/`
- 当前具体故事的 bible / script / production / assembly 资产

这些是案例项目，不应自动成为新 agent 的默认故事记忆。

---

### 2. 什么叫“新建 agent”
这里的“新建 agent”，本质上是：
- 新建一个有自己名字、人格、职责边界的长期工作体
- 它可以复用当前仓库的方法层文件
- 但不应该自动继承旧故事项目上下文

---

### 3. 什么叫“new space”
这里的“new space”，本质上是：
- 一个新的工作目录 / 新项目目录 / 新任务空间
- 用于承载一个新故事项目或新长期任务
- 它应当拥有自己的项目文件夹和 task brief

---

## 二、最推荐的启动方式

推荐采用：

## 方案A：新建一个干净 space，然后复制方法层文件
这是最推荐的方法。

### 适合谁
- 你想要干净模板
- 你不想混入旧故事
- 你准备长期复用这套工作流

### 你要复制进去的内容
#### 必须复制
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`

#### 强烈建议复制
- `autonomy-policy.md`
- `continuity-protocol.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `routing-matrix.md`
- `season-pipeline.md`
- `orchestrator-playbook.md`
- `season-orchestrator-playbook.md`
- `season-review-protocol.md`
- `delivery-spec.md`
- `execution-spec.md`
- `artifact-naming.md`
- `agent-contracts.md`
- `next-run-briefing-template.md`
- `BOOTSTRAP.md`

#### 可选复制
- `references/`（需确认不是旧项目专属参考）
- `agents/`
- `HEARTBEAT.md`
- `TOOLS.md`

#### 不要复制
- `.openclaw/`
- `projects/perfect-heir/`
- 任何旧项目脚本 / 分场 / 制片 / 宣发资产
- 带项目性内容的 MEMORY

---

## 三、如何给新 agent 起步

### 第一步：确定 agent 的身份
至少修改或确认以下文件：

#### 1. `IDENTITY.md`
建议调整：
- 名称
- vibe
- emoji / avatar（如果需要）

#### 2. `SOUL.md`
建议确认：
- 这个 agent 的核心身份
- 默认服务的内容类型
- 工作语气
- 边界

#### 3. `USER.md`
建议保留：
- 用户工作偏好
- 用户喜欢的交付方式
- 用户喜欢少确认、多推进的节奏（如果仍然成立）

### 第二步：重建 MEMORY
如果你需要长期记忆，建议：
- 建一个新的 `MEMORY.md`
- 只保留方法性、偏好性记忆
- 不带入旧故事项目记忆

例如只保留：
- 这个 agent 擅长 orchestrated story development
- 用户偏好结构化、多代理、少打断

不要保留：
- 《完美继承人》的人物、剧情、进度、项目判断

---

## 四、如何新建一个 new space

### 推荐目录结构
在新 space 中，建议先建立：

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

### 为什么这么建
因为这和当前工作流完全一致，后面：
- brief
- bible
- map
- script
- director
- production
就都能自然往下接。

---

## 五、new space 的第一份文件应该是什么

建议第一份文件一定是：

`projects/<your-project>/00_admin/task-brief.md`

### 这份 brief 至少要写清楚
- 项目名
- 类型 / format
- 核心冲突
- 目标交付链条
- 特别约束
- opening hook
- suspense question
- emotional payoff promise
- cliffhanger target
- 是否是全新项目
- 是否继承旧项目内容

如果这一步没做，后面很容易边写边漂。

---

## 六、推荐的新项目启动顺序

在新 agent + new space 里，建议按下面顺序工作：

1. 建立 `task-brief.md`
2. 产出 `series-brief.md`
3. 产出 `season-bible.md`
4. 产出 `episode-map.md`
5. 产出 `continuity-skeleton.md`
6. 产出 `batch1 / batch2 full-script`
7. 做 `checkpoint`
8. 做 `season assembly package`
9. 再扩展到：
   - 逐集精修台词
   - 导演分场
   - 拍摄对白压缩
   - 宣发金句
   - 场景清单
   - 制片拆景
   - 通告 / 日程 / 高能保护

这是当前仓库已经验证过的一条顺序。

---

## 七、哪些文件必须让新 agent 启动时先读

推荐 startup 顺序：
1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md`（如果你需要视觉/执行层）

如果你还保留了更多方法文档，再按需读：
- `autonomy-policy.md`
- `delivery-spec.md`
- `execution-spec.md`
- `merge-protocol.md`
- `revision-protocol.md`

---

## 八、GitHub 模板使用建议

如果你是从 GitHub 克隆这个仓库来开新 agent / new space，建议这样做：

### 模板仓库使用法
1. clone 仓库
2. 保留方法层文件
3. 删除或移走旧项目目录（如 `projects/perfect-heir/`），或者只把它当 sample 参考
4. 新建自己的 `projects/<your-project>/`
5. 从 `task-brief.md` 开始

### 如果你想保留旧项目作为示例
建议把旧项目放在：

```text
examples/perfect-heir/
```

而不是让它继续占据默认 `projects/` 入口。

---

## 九、最容易犯的错误

### 错误1：把旧项目 assets 一起带入新项目
结果：
- continuity 被污染
- agent 默认沿用旧故事习惯
- 新 space 不再真正“新”

### 错误2：不写 task brief，直接开写
结果：
- 结构漂移
- 中段返工
- 难以并行分工

### 错误3：只复制 README，不复制 workflows / templates
结果：
- 看起来知道怎么做
- 实际 agent 运行时没有可执行骨架

### 错误4：把 `.openclaw/` 一起带走
结果：
- 把运行态、本地状态和缓存污染进新 space
- 对复用没有帮助，反而制造混乱

---

## 十、给使用者的一句话指南

如果你只想记住一句话：

> **新建 agent 时，复制人格与工作流；新建 space 时，重建 task brief 与项目目录；不要把旧项目剧情资产和运行态文件一起继承。**

---

## 十一、推荐最小清单（真正懒人版）

如果你现在就要最快新开一个可工作的 agent + space，最小保留：

### 文件
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/`
- `templates/`
- `BOOTSTRAP.md`

### 新建
- `projects/<your-project>/00_admin/task-brief.md`

### 不带
- `.openclaw/`
- 旧项目目录
- 旧项目记忆

这样就能开工。
