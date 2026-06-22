# Codex Handoff

> 作用：在公司电脑、家里电脑以及不同 Codex 会话之间同步上下文。每次结束学习或开发前都更新这里。

## 当前日期

2026-06-22

## 当前阶段

阶段：银行 Java 岗位定位 + AI Agent 工程师 JD 对齐。

当前重点：

- 先恢复已有知识和项目表达，不急着开新大项目。
- 已将用户与 Codex 的固定协作流程写入 `AGENTS.md`。
- 使用 `java-ai-interview-study-guide.md` 作为主复习资料。
- 使用 `java-backend-interview-plan.md` 作为 6-8 周执行计划。
- 使用 `knowledge-answer-bank.md` 沉淀面试问题答案。
- 后续优先接管 `interview-assistant`，因为它比 `FixLedger` 小，更适合真正吃透。
- 2026-06-21 已从 GitHub 拉取 `BQHM/interview-assistant` 最新源码并完成第一版项目卡片。
- 2026-06-21 已根据用户提供的 AI Agent 工程师 JD，新增岗位适配学习路线。
- 2026-06-21 用户补充真实工作经历：2024-04 入职长亮科技存款组做 Java 开发，2026-06 起在宁波银行驻场参与数币业务。
- 2026-06-21 用户进一步补充：长亮工作性质是产品研发，负责存款业务开发，参与过青海农信 POC、安徽农信 POC、浦发银行新核心驻场约 1 个月、广农商 POC、郑州农商 POC，以及宁波银行数币开发组驻场。
- 2026-06-22 已把本机这几天的项目口述训练和八股训练补充进答案库，重点包括简历 hash 去重、文件校验、Tika 解析、AI 超时/重试/降级、Prompt Injection、AI 输出校验、HashMap put 和 String 系列。
- 2026-06-22 已在 `README.md` 新增“文档唯一职责规则”，明确每个文档的归档边界，后续先按职责治理重复内容，暂不删除、不移动、不合并文件。
- 2026-06-22 已补充 `profile.md` 的项目资产与简历使用建议，明确 `interview-assistant`、`FixLedger`、`java-core-lab`、`truckfarm`、未来高并发项目和 `interview-guide` 的使用边界，并拆分“已确认可表达 / 正在补强 / 暂不建议主动写成强项”的技术能力口径。
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
- 已完成银行 Java JD 对齐：
  - 新增 `bank-java-jd-positioning.md`。
  - 明确用户主线是“银行核心业务 Java 开发 + 存款/账户/交易链路 + 数币业务开发”。
  - 更新 `java-backend-interview-plan.md`，加入银行 Java JD 对齐路线。
  - 更新 `knowledge-answer-bank.md`，加入银行 Java 岗位定位和开户/存入/支取业务答案卡。
  - 明确银行 Java 岗八股优先级：事务、索引、MyBatis、Redis 幂等、MQ、Spring Cloud、Linux、并发、JVM。
- 已新增 JD 台账：
  - `jd-tracking.md` 记录用户发过的 JD、厂商/用工方、匹配点和简历定制方向。
  - 已记录 JD-001：益海嘉里丰益信息 AI Agent 工程师。
  - 已记录 JD-002：无锡锡商银行 Java 开发工程师。
- 已新增个人画像主档：
  - `profile.md` 记录用户毕业时间、工作时间线、长亮科技存款组经历、宁波银行数币驻场经历、求职主线、表达边界和待补充事实。
  - 后续用户补充自身情况时优先更新 `profile.md`。
  - README 已补充每个 Markdown 文档的作用。
- 已新增对话接续记录：
  - `conversation-log.md` 用于简短记录关键对话、暂停点和下次接续问题。
  - 它不替代 `study-log.md` 和 `HANDOFF.md`，只作为换设备时快速恢复“刚才聊到哪”的轻量索引。
- 已补录 2026-06-16 到 2026-06-22 的本机学习成果：
  - `knowledge-answer-bank.md` 新增 Java 基础与集合、AI 工程化、`interview-assistant` 项目深挖答案卡。
  - `conversation-log.md` 新增“本机项目追问与八股训练补录”。
  - `study-log.md` 新增 2026-06-22 学习记录。
- 已将用户最新经历补入 `profile.md` 和 `bank-java-jd-positioning.md`：
  - 长亮科技岗位性质：产品研发，负责存款业务开发。
  - 主要业务：开户、存入、支取/存取款等交易。
  - 客户 / POC / 驻场：青海农信 POC、安徽农信 POC、浦发银行新核心驻场、广农商 POC、郑州农商 POC、宁波银行数币开发组。
  - 当前表达边界：这些经历先登记为“参与 POC / 驻场 / 开发支持”，暂不包装成“主导项目交付”。
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
- 还没有把长亮科技 / 宁波银行经历整理成正式简历条目。
- 还没有补银行交易一致性、幂等、流水、冲正/补偿等高频答案卡。
- JD-001 还需要补充是否要求 Java、Python、LangChain、Dify、Coze 或其他特定框架。
- `profile.md` 中仍有大量待补充事实：专业、长亮技术栈、具体接口、数币模块、真实排查案例、可量化结果。
- 多个 POC / 驻场经历还需要继续细化，尤其要确认每个项目中用户具体做了什么：交易开发、参数配置、联调排查、演示支持、问题修复、文档沉淀、设计参与范围等。
- 需要继续完成本机暂停的八股追问：`HashMap 为什么容量是 2 的幂？`

## 下一步建议

### 第一步：明确两条投递主线

当前有两条可投递主线：

```text
1. 银行 Java / 金融科技 Java：主线，基于长亮科技存款组和宁波银行数币经历。
2. AI Agent 工程师：成长线，基于 interview-assistant Agent 化改造。
```

银行 Java 岗更贴真实工作经历，优先准备：

```text
profile.md
jd-tracking.md
bank-java-jd-positioning.md
Spring 事务 + 银行交易一致性
MySQL/Oracle 索引和慢 SQL
Redis 幂等和防重复提交
MQ 可靠消息和补偿
```

如果继续整理个人经历，优先追问：

```text
1. 长亮 V8.7 基板到底是什么：标准产品、客户项目基础版，还是内部产品基线？
2. 开户、存入、支取/存取款中，分别写过哪些交易、字段校验、规则、接口或联调内容？
3. 青海农信、安徽农信、广农商、郑州农商 POC 中，主要做交易开发、配置、联调、演示支持、问题修复还是文档？
4. 浦发银行新核心驻场 1 个月，参与了哪些设计和开发模块？
5. 宁波银行数币开发组现在具体做哪个模块：接口、交易、对账、回调、状态流转还是别的？
```

### 第二步：按 AI Agent JD 调整学习重心

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

### 第三步：完成 Day 1 口述训练

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

当前本机训练暂停点：

```text
已完成：interview-assistant 30 秒介绍、内容 hash 去重、并发重复上传、文件校验、Tika 解析、AI 失败兜底、Prompt Injection、AI 输出校验、HashMap put 流程、String 系列纠错。
下一题：HashMap 为什么容量是 2 的幂？
```

### 第四步：继续第 1 周复习

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

### 第五步：用 java-core-lab 做实验

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
请先阅读 HANDOFF.md、study-log.md 和 conversation-log.md，然后继续上次暂停的学习任务。
```

或者：

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

或者：

```text
请根据 bank-java-jd-positioning.md，从 Spring 事务 + 银行交易一致性开始，帮我用八股 + 工作经历话术的方式学习。
```

## 注意事项

- 简历中不要把 AI 生成项目包装成完全独立开发。
- 更合适的说法是：AI 辅助开发后，自己进行代码审查、测试补充、模块接管和重构。
- 真正能写进简历的内容，必须满足：
  - 自己能画流程图。
  - 自己能讲核心代码。
  - 自己能回答失败场景。
  - 自己能做一个小改动。
