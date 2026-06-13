# Codex Handoff

> 作用：在公司电脑、家里电脑以及不同 Codex 会话之间同步上下文。每次结束学习或开发前都更新这里。

## 当前日期

2026-06-13

## 当前阶段

阶段：Java 后端面试复健 + AI 工程化学习资料整理。

当前重点：

- 先恢复已有知识和项目表达，不急着开新大项目。
- 已将用户与 Codex 的固定协作流程写入 `AGENTS.md`。
- 使用 `java-ai-interview-study-guide.md` 作为主复习资料。
- 使用 `java-backend-interview-plan.md` 作为 6-8 周执行计划。
- 使用 `knowledge-answer-bank.md` 沉淀面试问题答案。
- 后续优先接管 `interview-assistant`，因为它比 `FixLedger` 小，更适合真正吃透。
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
- 明确了学习原则：
  - 不让 AI 直接生成完整项目。
  - 用 AI 解释、Review、追问、辅助复盘。
  - 每个知识点都要能讲“问题、原理、项目、坑、排查”。

## 当前未完成

- 还没有正式进入第一阶段 Day 1：整理 `interview-assistant` 项目卡片。
- 还没有开始项目话术录音和模拟追问。
- 还没有正式接管 `interview-assistant` 的新功能。
- 还需要把 `interview-assistant` 的项目话术统一改成“不出现 guide 项目经历，只讲 assistant 的真实实现和接管计划”。

## 下一步建议

### 第一步：开始第 1 周复习

从 `java-backend-interview-plan.md` 的第一阶段开始，不要直接跳到八股：

```text
第一阶段：项目与简历深挖
Day 1：interview-assistant 项目卡片
Day 2：FixLedger 项目卡片
Day 3：java-core-lab 学习实验卡片
```

完成第一阶段后，再进入 Java/MySQL/Redis：

```text
HashMap -> ConcurrentHashMap -> volatile -> ThreadLocal -> 线程池 -> MySQL 索引 -> Redis 缓存
```

### 第二步：用 java-core-lab 做实验

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
请先阅读 HANDOFF.md、study-log.md 和 java-backend-interview-plan.md，然后从 https://github.com/BQHM 获取 interview-assistant 的最新项目内容，按第一阶段 Day 1 帮我整理项目卡片。
```

或者：

```text
请根据 java-backend-interview-plan.md，今天只推进一个学习主题，并把答案沉淀到 knowledge-answer-bank.md。
```

## 注意事项

- 简历中不要把 AI 生成项目包装成完全独立开发。
- 更合适的说法是：AI 辅助开发后，自己进行代码审查、测试补充、模块接管和重构。
- 真正能写进简历的内容，必须满足：
  - 自己能画流程图。
  - 自己能讲核心代码。
  - 自己能回答失败场景。
  - 自己能做一个小改动。
