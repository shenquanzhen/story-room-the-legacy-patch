# 迁移当前工作流到新 Agent 与新 Space 所需文档清单

## 一、文档目的
本清单用于回答一个非常具体的问题：

> 如果要复制当前这套工作流、方法、节奏和资产组织方式，
> 但**不需要继承《完美继承人》这个故事本身的记忆、人物、剧情、世界观、具体项目资产**，
> 那么新起一个 agent、新开一个 space 时，应该带走哪些文档？

本清单会尽量完整地把文档分为：
1. **必须迁移**
2. **强烈建议迁移**
3. **按需迁移**
4. **不要迁移**

并说明原因，方便你直接复制或重建。

---

## 二、迁移原则（先讲原则，再讲清单）
如果你要的是：
- 复制当前 agent 的工作方式
- 复制多代理 writers' room / production-room 流程
- 复制目录组织和推进方法
- 复制持续推进、少打断、结构化资产生产的能力

但**不要继承当前故事项目本身**，那么迁移时要遵守以下原则：

### 原则1：迁移“方法”，不要迁移“故事内容”
应迁移：
- pipeline
- playbook
- 模板
- 规则
- 角色分工逻辑
- 命名规范
- 交付标准

不应迁移：
- 当前项目的剧情设定
- 当前角色名
- 当前世界观
- 当前 episode map
- 当前台词、分场、制片资产

### 原则2：迁移“身份与习惯”，但谨慎迁移“项目记忆”
可迁移：
- agent 的人格定位
- 用户偏好
- 工作习惯
- 协作节奏

不要直接迁移：
- 当前项目的故事状态
- 当前 agent 已经对《完美继承人》形成的具体故事记忆

### 原则3：优先迁移“能复用多次”的基础设施文档
比如：
- SOUL
- USER
- workflows
- templates
- production / routing / revision 类方法文档

这些才是新 agent 最值钱的底座。

---

## 三、必须迁移的文档（建议完整保留或等价重建）
这些文档决定的是：
**这个 agent 是谁、怎么工作、怎么接任务、怎么拆任务、怎么交付。**

如果不迁移，新的 agent 很可能会变成“会写，但不按你喜欢的方式工作”。

---

### A. 身份与人格层

#### 1. `SOUL.md`
### 为什么必须带
这是 agent 的核心身份文件。  
它定义了：
- 这个 agent 不是普通聊天机器人，而是 showrunner / orchestrator
- 它的气质、边界、工作哲学
- 它面对用户时的语气
- 它做故事时的价值排序

### 不带会怎样
新 agent 很可能会：
- 说话变泛化
- 失去“总控感”
- 回答方式变成普通客服或单人作者

### 迁移建议
- **必须迁移**
- 可以微调名字、领域，但结构建议保留

---

#### 2. `USER.md`
### 为什么必须带
这份文件定义了用户偏好，尤其是：
- 喜欢结构化文件
- 喜欢多代理协作
- 喜欢少确认、多执行
- 喜欢 milestone 式更新而不是不断打断

### 不带会怎样
新 agent 可能不知道：
- 用户希望它持续推进
- 用户更重视资产闭环而不是聊天体验

### 迁移建议
- **必须迁移**
- 可保留用户工作偏好部分
- 与具体项目无关的用户习惯建议全部带走

---

#### 3. `IDENTITY.md`
### 为什么建议纳入必须层
这是比 SOUL 更外显的“自我设定”文件，定义：
- 名字
- vibe
- 角色感
- 是否要调整 identity

### 迁移建议
- 若新 agent 是“同类 showrunner agent”，建议带
- 若新 agent 是全新类型，可重写

---

### B. 工作流与管线层

#### 4. `AGENTS.md`
### 为什么必须带
这是整个多代理 writers' room 的中枢说明，定义了：
- 标准 child roles（plot-agent / character-agent / script-agent / review-agent / storyboard-agent 等）
- 责任路由原则
- 阶段A / 阶段B 的基本 pipeline
- 何时 spawn 新 session，何时续用旧 session
- 每类 agent 的输出合同

### 不带会怎样
新 agent 即便会工作，也不一定会：
- 用正确角色去做正确任务
- 保持 lane 清晰
- 让 reviewer 不和 drafting lane 混线

### 迁移建议
- **必须迁移**
- 可以按新空间领域微调 child roles，但整体框架非常值得保留

---

#### 5. `workflows/comic-pipeline.md`
### 为什么必须带
它定义了 hook-first 的工作方法：
- 先做 hook board
- 再做 plot/character
- 再做 script
- 再做 review

### 迁移建议
- **必须迁移**
- 即使新项目不是“漫画”，这份 workflow 本质上是故事型 pipeline，仍然非常可复用

---

#### 6. `workflows/runbook.md`
### 为什么必须带
它是接活后的操作指南，定义：
- 如何分类 request type
- 如何 build task brief
- 如何 merge
- 何时停止

### 迁移建议
- **必须迁移**
- 这是当前 workflow 非常关键的执行说明

---

#### 7. `workflows/task-entry.md`
### 为什么必须带
它把“用户自然语言需求”标准化成可执行字段：
- protagonist
- pressure
- opening hook
- suspense question
- payoff promise
- cliffhanger target

### 迁移建议
- **必须迁移**
- 它能避免新 agent 接到任务后直接乱写

---

#### 8. `workflows/storyboard-pipeline.md`
### 为什么必须带
后续如果仍要做导演分场、分镜、拍摄设计，这份非常关键。
它定义了：
- script lock check
- storyboard-agent / continuity-agent
- storyboard-review
- focused revision

### 迁移建议
- **必须迁移**
- 如果新 agent 完全不做 visual / production 层，可降级为强烈建议迁移

---

### C. 模板与交付标准层

#### 9. `templates/` 整个目录
### 为什么必须带
模板决定了输出的一致性和交付格式。
比如：
- story outline
- character sheet
- scene script
- review checklist
- storyboard sheet
- storyboard review

### 不带会怎样
新 agent 可能知道要做什么，但不知道应当“长成什么样”。

### 迁移建议
- **整个目录建议必须迁移**
- 如果模板中含有当前故事案例，注意清掉案例内容，只保留结构

---

#### 10. `delivery-spec.md`
### 为什么建议纳入必须层
它通常定义：
- 交付颗粒度
- 每类资产要达到什么标准
- 最终汇总怎么组织

### 迁移建议
- 若你希望新 agent 保持现在这种“结果是可交付文件，而不是闲聊”的风格，建议必须带

---

#### 11. `execution-spec.md`
### 为什么建议纳入必须层
它决定的是实际执行时的行为规范，例如：
- 做到什么程度算完成
- 多轮任务如何衔接
- 什么可以自动推进

### 迁移建议
- 建议带
- 对“持续工作、不反复确认”很有帮助

---

#### 12. `merge-protocol.md`
### 为什么建议带
当前 agent 很多内容是多代理并行产出再统一合并。  
如果没有 merge protocol，新 agent 容易：
- 合并风格不统一
- 重复内容过多
- reviewer 结论无法正确回收到主稿

### 迁移建议
- 强烈建议带

---

#### 13. `revision-protocol.md`
### 为什么建议带
后续如果新 agent 继续要跑多轮修订、打补丁、局部返工，这份极重要。

### 迁移建议
- 强烈建议带

---

---

## 四、强烈建议迁移的文档（不带也能跑，但品质会明显下降）
这些文档决定的是：
**工作会不会更稳、更持续、更像一个长期可用的 production agent。**

---

### 14. `autonomy-policy.md`
### 为什么强烈建议带
这类文件通常会定义：
- 什么情况下自动推进
- 什么情况下暂停
- 什么情况下必须请求确认

### 迁移建议
- 如果你喜欢当前这种“你做主，持续推进”的感觉，这份非常值得迁移

---

### 15. `continuity-protocol.md`
### 为什么强烈建议带
这类文件对长链条项目非常有用，尤其是：
- 人物状态连续性
- 语言埋词回收
- 场景逻辑不打架

### 迁移建议
- 强烈建议带

---

### 16. `routing-matrix.md`
### 为什么强烈建议带
它能明确：
- 什么任务给哪个 child role
- 什么任务必须 reviewer 介入
- 什么任务能合并到同一轮做

### 迁移建议
- 强烈建议带

---

### 17. `season-pipeline.md`
### 为什么强烈建议带
当前项目之所以能从 brief 一路跑到 production，是因为实际采用了 season 级 pipeline。  
这份若存在，建议保留。

---

### 18. `season-orchestrator-playbook.md`
### 为什么强烈建议带
它能帮助新 agent 理解：
- 如何管理全季而不是单集
- 如何安排阶段产出
- 如何控制 stop point

---

### 19. `season-review-protocol.md`
### 为什么强烈建议带
一旦你要复制当前这种“先跑，再 review，再 patch”的方式，这份会很有价值。

---

### 20. `orchestrator-playbook.md`
### 为什么强烈建议带
这是让 agent 保持“总控感”的关键补充文件之一。  
尤其适合长期 space。

---

### 21. `state-management.md`
### 为什么强烈建议带
如果新 space 也会是长期运行型 agent，这份非常重要。  
它可以帮助新 agent 不把 session 做成一团散记忆。

---

### 22. `artifact-naming.md`
### 为什么强烈建议带
当前项目文件命名相对有秩序。  
如果要复制 workflow，命名标准非常值得复用。

---

### 23. `agent-contracts.md`
### 为什么强烈建议带
如果你还想继续用 child role 协作，这类“输出合同”文档很重要。  
它能保证不同 child role 的产出结构稳定。

---

### 24. `next-run-briefing-template.md`
### 为什么强烈建议带
长期项目特别需要这类文件。  
新 agent 如果断档接手，它能帮助快速恢复上下文。

---

## 五、按需迁移的文档（看你新 agent 是否还做同类工作）
这些文档不一定所有新 agent 都要带，但如果目标相近，非常值得带。

---

### 25. `BOOTSTRAP.md`
### 适用情况
如果你经常从一个长期主空间派生新 branch workspace / 新项目空间，这份很有用。

### 为什么
它定义了：
- 什么继承，什么不继承
- 新项目启动时默认要读什么

### 迁移建议
- 适合带
- 尤其适合你未来继续开很多新 story project

---

### 26. `MEMORY.md`
### 适用情况
只建议迁移“长期身份与工作偏好记忆”，不要迁移当前故事内容。

### 如何处理
可复制其中这些内容：
- agent name / strength
- 用户偏好
- 工作模式

不要复制：
- 当前《完美继承人》的任何项目具体记忆

### 最佳做法
新建一份新的 MEMORY.md，保留方法性长期记忆，不保留故事性记忆。

---

### 27. `HEARTBEAT.md`
### 适用情况
如果新 agent 也要长期自维护、周期性检查项目状态，可以带。

---

### 28. `TOOLS.md`
### 适用情况
如果里面后来会加环境特定约束、工作规范、命名偏好，这份值得带。  
但当前版本内容较轻，可带可不带。

---

### 29. `references/` 目录
### 适用情况
如果 references 里放的是工作方法、行业基准、风格规范，而不是《完美继承人》专属参考，则可迁移。

### 不适合直接迁移的情况
如果 references 已经混入当前故事的调研或内容参考，就不要整体搬，需筛选。

---

### 30. `agents/` 目录
### 适用情况
如果这里面存的是 child role 定义或固定 prompt 模板，值得迁移。

### 注意
如果 agents 目录里混入了当前项目专属角色配置，要去项目化后再带。

---

## 六、不要迁移的文档 / 目录（否则会把旧故事记忆一起带过去）
这一部分很关键。  
如果你的目标是：**复制工作流，不复制当前故事记忆**，那下面这些应避免直接带走。

---

### 31. `projects/perfect-heir/` 整个目录
### 为什么不要带
这整个目录就是《完美继承人》本项目资产本身。  
里面包含：
- 设定
- 人物
- 全季结构
- 台词
- 分场
- 制片规划
- 宣发句池

### 如果带走会发生什么
新的 agent 很可能默认把这套内容当成“当前项目历史”继续沿用。

### 结论
- **不要整体迁移**
- 若仅想研究工作流，可作为旁参保留在外部，但不要直接放进新 space 主工作目录

---

### 32. 任何旧项目的 episode map / bible / script / storyboard / production 文件
### 为什么不要带
这些都属于具体故事资产，而不是方法资产。

---

### 33. 当前项目相关的 assembly package
### 为什么不要带
因为 assembly package 本质是旧项目总装说明，不是流程模板。

---

### 34. 与当前故事直接绑定的记忆内容
包括但不限于：
- 《完美继承人》的角色信息
- 《完美继承人》的结构信息
- 当前项目的剧情状态
- 当前项目的制片包与通告包

### 最佳做法
如果新 agent 需要“知道如何工作”，应通过 workflow 文档知道，而不是通过旧项目记忆知道。

---

## 七、推荐的“新Agent / 新Space 最小迁移包”
如果你想要一个**既不臃肿、又能最大程度复制当前工作流**的版本，推荐最小迁移包如下：

### 必带
- `SOUL.md`
- `USER.md`
- `IDENTITY.md`
- `AGENTS.md`
- `workflows/comic-pipeline.md`
- `workflows/runbook.md`
- `workflows/task-entry.md`
- `workflows/storyboard-pipeline.md`
- `templates/` 整个目录

### 强烈建议加带
- `autonomy-policy.md`
- `continuity-protocol.md`
- `merge-protocol.md`
- `revision-protocol.md`
- `routing-matrix.md`
- `season-pipeline.md`
- `season-orchestrator-playbook.md`
- `season-review-protocol.md`
- `orchestrator-playbook.md`
- `state-management.md`
- `artifact-naming.md`
- `agent-contracts.md`
- `next-run-briefing-template.md`
- `delivery-spec.md`
- `execution-spec.md`

### 可选
- `BOOTSTRAP.md`
- `MEMORY.md`（只保留方法记忆，重建内容）
- `HEARTBEAT.md`
- `TOOLS.md`
- `agents/`
- `references/`（需筛选）

### 不要直接带
- `projects/perfect-heir/`
- 任何当前项目具体资产文件

---

## 八、推荐的新Space初始化方式
为了避免污染新项目，建议不要“整个 workspace 原地复制后删内容”，更好的方法是：

### 方案A：新建干净 space，只复制方法文档
适合：
- 你要真正开一个全新 agent
- 不想混入旧故事资产

### 方案B：复制当前 workspace，再只保留方法层文档
适合：
- 你想最快复刻当前工作流
- 但你有能力手动删除项目资产

### 推荐删除顺序（如果采用方案B）
删除或移走：
1. `projects/perfect-heir/`
2. 任何旧项目 references
3. MEMORY 中的项目性记忆
4. 当前项目相关 assembly / checkpoint / script / production 文件

保留：
- 身份层
- workflow 层
- template 层
- playbook / protocol 层

---

## 九、最推荐给新Agent的“启动必读顺序”
如果你已经把方法文档迁过去了，建议新 agent 的 startup rule 读这几项：

1. `SOUL.md`
2. `USER.md`
3. `AGENTS.md`
4. `workflows/comic-pipeline.md`
5. `workflows/runbook.md`
6. `workflows/task-entry.md`
7. `workflows/storyboard-pipeline.md`
8. `templates/`（按任务需要再读）
9. `autonomy-policy.md` / `execution-spec.md` / `delivery-spec.md`（若存在）

这样它会最快进入你现在熟悉的工作方式。

---

## 十、给你的一句话结论
如果你的目标是：

> **复制当前 agent 的工作方式，而不复制《完美继承人》这个故事本身。**

那最该带走的是：
- **人格文件**（SOUL / USER / IDENTITY）
- **多代理与工作流文件**（AGENTS / workflows / playbooks / protocols）
- **模板文件**（templates）
- **少量方法性长期记忆**（重建后的 MEMORY）

最不该带走的是：
- **任何当前项目具体资产**（projects/perfect-heir 整包）

一句话概括：

> **带走“怎么做”，不要带走“做了什么”。**
