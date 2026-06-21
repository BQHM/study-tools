# Codex Handoff

> 作用：在公司电脑、家里电脑以及不同 Codex 会话之间同步上下文。每次结束学习或开发前都更新这里。

## 当前日期

2026-06-21

## 当前阶段

阶段：AI Agent 工程师 JD 对齐 + `interview-assistant` Agent 化学习路线调整。

当前重点：

- 先恢复已有知识和项目表达，不急着开新大项目。
- 已将用户与 Codex 的固定协作流程写入 `AGENTS.md`。
- 使用 `java-ai-interview-study-guide.md` 作为主复习资料。
- 使用 `java-backend-interview-plan.md` 作为 6-8 周执行计划。
- 使用 `knowledge-answer-bank.md` 沉淀面试问题答案。
- 后续优先接管 `interview-assistant`，因为它比 `FixLedger` 小，更适合真正吃透。
- 2026-06-21 已从 GitHub 拉取 `BQHM/interview-assistant` 最新源码并完成第一版项目卡片。
- 2026-06-21 已根据用户提供的 AI Agent 工程师 JD，新增岗位适配学习路线。
- 远程同步仓库使用 `https://github.com/BQHM/study-tools`。
- 项目源码统一以 `https://github.com/BQHM` 为最新事实来源；项目提问前优先读取 GitHub 最新 README、目录结构和关键源码。
- 重要项目边界：`interview-guide` 不是用户项目，而是导师项目/参考项目；简历和面试项目经历只讲 `interview-assistant`，不能把 `interview-guide` 包装成个人项目。

## 已完成

- 整理了父目录项目现状：
  - `FixLedger`：AI 开发的完整业务项目，可作为后续代码审查、重构、测试补充对象。
  - `interview-assistant`：用户开发中的主接管项目，在 AI 辅助下参考导师项目 `interview-guide` 的功能形态和设计思路逐步实现。
  - `java-core-lab`：AI 辅助学习实验仓，适合复习 Java 集合、并发、JVM 排查。
  - `truckfarm`：旧项目和现代化重构设想，目前不适合作为主简历项目。
- 创建了 `java-ai-interview-study-guide.md`：
  - Java 基础、集合、并发、JVM。
  - Spring / MySQL / Redis / MQ。
  - 高并发项目追问。
  - AI 工程化、RAG、Embedding、Prompt、结构化输出。
  - 两个月学习路线和每日复习模板。
- 创建了 `knowledge-answer-bank.md`：
  - 用固定答案卡模板存储高频面试题答案。
  - 已覆盖 HashMap、ConcurrentHashMap、volatile、ThreadLocal、线程池、事务失效、JWT、MySQL 索引、MVCC、Redis 缓存、Redis Lua、MQ、RAG、AI 幻觉和高并发下单。
- 根据知识星球文章《Java 后端面试通关全阶指南（涵盖后端通用体系）》创建了 `java-backend-interview-plan.md`：
  - 采用“项目与简历深挖 -> Java/MySQL/Redis -> 框架与系统设计 -> 计算机基础 -> 分布式高并发 -> JVM -> 面试冲刺”的顺序。
  - 按个人情况强化了项目接管、AI 辅助开发的诚实表达和跨电脑 handoff。
- 创建 `AGENTS.md`：
  - 固化“预习计划 -> 教材讲解 -> 高频八股 -> 项目关联 -> 追问训练 -> 答案沉淀 -> 学习记录 -> handoff 同步”的协作流程。
  - 明确 Codex 要同时扮演架构师、工程师和老师。
  - 规定项目相关问题优先从 `https://github.com/BQHM` 获取最新上下文。
  - 规定默认下一步是整理 `interview-assistant` 项目卡片。
  - 补充规则：`interview-guide` 是导师项目/参考项目，不属于用户简历项目经历。
- 已初始化本地 Git 仓库并推送到 `https://github.com/BQHM/study-tools`。
- 已完成 `interview-assistant` Day 1 文档产出：
  - 新增 `interview-assistant-project-card.md`。
  - 写出 30 秒、1 分钟、3 分钟项目话术。
  - 梳理简历上传分析链路、文字模拟面试链路、真实接管点和后续小切片。
  - 更新 `knowledge-answer-bank.md`，新增项目深挖答案卡。
- 已确认 `interview-assistant` 最新代码中的事实：
  - 后端已有简历上传、Tika 解析、内容 hash 去重、对象存储、AI 分析 + 规则兜底。
  - 后端已有文字模拟面试创建、未完成会话复用、当前题查询、暂存答案、提交答案、提前交卷、历史列表、历史详情、删除和报告接口。
  - 最新代码里已经有 `InterviewAnswerEntity`，部分旧文档关于“独立答案表未完成”的描述可能过期。
- 已完成 AI Agent JD 对齐：
  - 新增 `ai-agent-jd-study-plan.md`。
  - 更新 `java-backend-interview-plan.md`，加入 JD 对齐路线。
  - 更新 `knowledge-answer-bank.md`，加入 AI Agent 岗位定位和 Agent vs ChatBot 答案卡。
  - 明确后续八股学习要绑定 Agent 工程问题，例如线程池对应 AI 异步任务，Redis 对应会话缓存和限流，MySQL 对应用户记忆和答题记录。
- 明确了学习原则：
  - 不让 AI 直接生成完整项目。
  - 用 AI 解释、Review、追问、辅助复盘。
  - 每个知识点都要能讲“问题、原理、项目、坑、排查”。

## 当前未完成

- 还没有进行 `interview-assistant` 项目话术口述训练和模拟追问。
- 还没有正式接管 `interview-assistant` 的新功能。
- 还没有在正式工作区验证 `interview-assistant` 是否能启动、构建和跑接口。
- 还需要检查报告生成和历史详情是否已经完全从 `InterviewAnswerEntity` 聚合答案。
- 还没有开始 Tool Calling、Memory、Planning 的项目化落地。

## 下一步建议

### 第一步：按 AI Agent JD 调整学习重心

先阅读：

```text
ai-agent-jd-study-plan.md
interview-assistant-project-card.md
knowledge-answer-bank.md 中的 AI Agent 岗位定位
```

后续八股学习必须额外回答：

```text
这个知识点如何服务 AI Agent 产品落地？
它在 interview-assistant Agent 化改造中对应哪个工程问题？
```

### 第二步：完成 Day 1 口述训练

围绕 `interview-assistant-project-card.md` 进行口述：

```text
1. 30 秒介绍。
2. 1 分钟介绍。
3. 5 个项目追问。
```

优先追问：

```text
AI 简历分析失败怎么办？
为什么用内容 hash 去重？
currentQuestionIndex 为什么表示下一道待答题？
为什么答案要拆成独立答案表？
下一步你准备亲手接管哪个小切片？
```

### 第三步：继续第 1 周复习

从 `java-backend-interview-plan.md` 的第一阶段开始，不要直接跳到八股：

```text
第一阶段：项目与简历深挖
Day 1：interview-assistant 项目卡片（文档已完成，待口述训练）
Day 2：FixLedger 项目卡片
Day 3：java-core-lab 学习实验卡片
```

完成第一阶段后，再进入 Java/MySQL/Redis：

```text
HashMap -> ConcurrentHashMap -> volatile -> ThreadLocal -> 线程池 -> MySQL 索引 -> Redis 缓存
```

### 第四步：用 java-core-lab 做实验

每学一个主题，到本机的 `java-core-lab` 项目目录跑对应 Demo。

当前公司电脑参考路径：

```text
D:\work\work_space\Project\java-core-lab
```

家里电脑以实际 clone 路径为准。

目标不是看完，而是能写出：

```text
这个 Demo 验证了什么？
如果面试官追问，我怎么解释？
这个知识点能和哪个项目关联？
```

## 下次打开 Codex 时可以这样说

```text
请先阅读 HANDOFF.md、study-log.md 和 interview-assistant-project-card.md，然后围绕 interview-assistant 扮演面试官追问我 5 个问题。
```

或者：

```text
请根据 java-backend-interview-plan.md，今天只推进一个学习主题，并把答案沉淀到 knowledge-answer-bank.md。
```

或者：

```text
请根据 ai-agent-jd-study-plan.md，从线程池 + AI 异步任务开始，帮我用八股 + 项目落地的方式学习。
```

## 注意事项

- 简历中不要把 AI 生成项目包装成完全独立开发。
- 更合适的说法是：AI 辅助开发后，自己进行代码审查、测试补充、模块接管和重构。
- 真正能写进简历的内容，必须满足：
  - 自己能画流程图。
  - 自己能讲核心代码。
  - 自己能回答失败场景。
  - 自己能做一个小改动。
