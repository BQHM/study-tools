# 学习日志

> 每次学习结束后更新。重点写“学会了什么、还不会什么、下一步做什么”，不用写长篇流水账。

## 2026-06-21

### 今日主题

第一阶段 Day 1：整理 `interview-assistant` 项目卡片和面试话术。

### 已完成

- 从 GitHub 拉取并阅读 `BQHM/interview-assistant` 最新源码和文档。
- 阅读项目 README、`AGENTS.md`、`docs/implementation-plan.md`、`docs/learning-roadmap.md`、ADR 和完成度审计文档。
- 阅读核心后端文件：`ResumeController`、`InterviewController`、`ResumeUploadService`、`ResumeGradingService`、`InterviewSessionService`、`ResumeEntity`、`ResumeAnalysisEntity`、`InterviewSessionEntity`、`InterviewAnswerEntity`。
- 新增 `interview-assistant-project-card.md`，沉淀项目定位、核心流程、30 秒 / 1 分钟 / 3 分钟话术、必会追问和接管计划。
- 更新 `knowledge-answer-bank.md`，新增 `interview-assistant` 项目深挖答案卡。

### 今日理解

- `interview-assistant` 当前最适合讲两条主链路：简历上传分析链路和文字模拟面试链路。
- 简历模块的亮点不是“调 AI”，而是文件校验、内容 hash 去重、Tika 解析、对象存储、PostgreSQL 落库、Spring AI 结构化分析和规则兜底。
- 面试模块的关键语义是：`currentQuestionIndex` 表示下一道待答题索引；暂存答案不推进，提交答案才推进；完成后禁止继续作答。
- 最新代码里已经有 `InterviewAnswerEntity`、历史列表、详情和删除接口，说明 README / 早期审计文档有部分过期描述，后续要以最新源码为准。
- 下一步很适合亲手接管一个小切片：检查报告和历史详情是否真正从独立答案表聚合答案，并补核心流程测试。

### 还不清楚

- 当前本机是否已经有可运行的 `interview-assistant` 正式工作区，而不仅是临时 clone。
- PostgreSQL、RustFS / S3 和 AI Key 是否已经在本机配置好，能否直接启动项目做接口验证。
- 报告生成和历史详情在最新代码中是否已经完全适配 `InterviewAnswerEntity`，需要进入项目工作区后跑测试或手工验证。

### 下一步

- 先让用户按 30 秒和 1 分钟话术复述 `interview-assistant`。
- Codex 扮演面试官，围绕项目追问 5 个问题，答不上来的补入答案库。
- 如果进入开发接管，则优先做一个小切片：修正报告 / 历史详情从答案表聚合，并为 `InterviewSessionService` 补最小测试。

### 补充：AI Agent JD 对齐

- 阅读用户提供的 AI Agent 工程师 JD 截图，确认该岗位不是纯算法岗，也不是传统 Java CRUD 岗，而是偏“Java 后端 + LLM 应用工程 + Agent 产品落地”。
- 新增 `ai-agent-jd-study-plan.md`，把 JD 拆成需求拆解、方案评审、原型上线、工具调用、记忆增强、自主规划、多模态交互和大模型生态。
- 更新 `java-backend-interview-plan.md`，增加 AI Agent 工程师 JD 对齐路线。
- 更新 `knowledge-answer-bank.md`，新增 AI Agent 岗位定位和 Agent vs ChatBot 答案卡。
- 后续八股学习要额外回答：这个知识点如何服务 `interview-assistant` 的 Agent 化改造？

### JD 对齐后的下一步

- 下一主题优先学“线程池 + AI 异步任务”，同时覆盖 Java 并发八股和 Agent 产品落地。
- 继续保留 HashMap、ConcurrentHashMap、ThreadLocal 等基础题，但讲解时要绑定工具注册表、用户上下文和多线程状态安全。

### 补充：银行 Java JD 与真实经历

- 用户补充真实工作经历：2024 年毕业，2024 年 4 月入职长亮科技，担任存款组 Java 开发工程师；2026 年 6 月开始在宁波银行驻场外包，与同事参与数币业务开发。
- 用户在长亮主要做业务开发，包括长亮 V8.7 基板的开户、存入、支取等交易。
- 新增 `bank-java-jd-positioning.md`，沉淀银行 Java 岗位匹配、工作经历表达、开户/存入/支取业务话术和八股优先级。
- 更新 `java-backend-interview-plan.md`，增加银行 Java JD 对齐路线。
- 更新 `knowledge-answer-bank.md`，新增银行 Java 岗位定位和开户/存入/支取业务答案卡。

### 银行 JD 对齐后的下一步

- 面向银行 Java 岗，下一主题优先学“Spring 事务 + 银行交易一致性”。
- 后续每个八股都要额外回答：它如何服务开户、存入、支取、数币这类交易系统？

### 补充：JD 台账

- 新增 `jd-tracking.md`，用于长期记录用户发过的 JD、对应厂商/用工方、岗位要求、匹配点和简历定制方向。
- 当前已记录：
  - JD-001：益海嘉里丰益信息 AI Agent 工程师。
  - JD-002：无锡锡商银行 Java 开发工程师。
- 后续每次用户发 JD，都要追加到 `jd-tracking.md`，避免截图和聊天信息散落。

### 补充：个人画像主档

- 新增 `profile.md`，用于长期维护用户自身情况，包括毕业时间、工作时间线、长亮科技存款组经历、宁波银行数币驻场经历、求职主线、表达边界和待补充事实。
- 更新 `README.md` 文档索引，为每个 Markdown 文档补充明确作用。
- 后续用户补充自身情况时，优先更新 `profile.md`；用户补充 JD 时，优先更新 `jd-tracking.md`。
- 补充用户基本信息：本科南京财经大学，软件工程专业；2024 年 4 月以实习身份入职长亮科技，2024 年 7 月开始试用期，2024 年 11 月转正，一直工作至今。
- 补充长亮科技工作性质：用户在长亮做的是产品研发，负责存款业务开发，主要围绕开户、存入、支取/存取款等交易。
- 补充客户 / POC / 驻场经历：青海农信 POC、安徽农信 POC、浦发银行新核心驻场约 1 个月、广农商 POC、郑州农商 POC，以及 2026 年 6 月开始的宁波银行数币开发组驻场。
- 更新 `profile.md` 和 `bank-java-jd-positioning.md`，把“产品研发 + 多客户 POC + 新核心驻场 + 数币开发”纳入银行 Java 主线表达。
- 当前这些 POC / 驻场经历只先登记为事实线索，后续需要继续追问具体职责、交易范围、开发内容、联调问题和可讲案例，暂不包装成“主导项目交付”。

### 补充：对话接续记录

- 新增 `conversation-log.md`，用于记录关键对话摘要、暂停点和下次接续问题。
- 该文件不记录完整聊天内容，只作为跨设备继续学习的轻量索引。
- README 已补充该文档的用途，并在结束学习流程中加入“必要时更新 conversation-log.md”。

## 2026-06-22

### 今日主题

补录本机口述训练成果：`interview-assistant` 简历上传链路、AI 工程化追问和 Java 高频八股。

### 已完成

- 先拉取远程 `study-tools` 最新内容，合并 2026-06-21 在其他设备新增的项目卡片、JD 台账、个人画像和答案库。
- 补充 `knowledge-answer-bank.md` 的 Java 基础与集合答案卡：
  - HashMap put 流程。
  - HashMap 为什么容量是 2 的幂。
  - ArrayList 和 LinkedList 区别。
  - `==` 和 `equals` 区别。
  - String、StringBuilder、StringBuffer 区别。
- 补充 `interview-assistant` 项目深挖答案卡：
  - 为什么用内容 hash 去重，而不是文件名。
  - 两个请求同时上传同一份简历如何避免重复数据。
  - 为什么上传简历要先做文件类型和大小校验。
  - 为什么不能只根据文件后缀判断文件类型。
  - Tika 解析失败或解析出噪音怎么处理。
- 补充 AI 工程化答案卡：
  - 超时、重试、降级分别解决什么问题。
  - 哪些错误适合重试，哪些不适合。
  - Prompt Injection 是什么，怎么防。
  - 为什么不能直接信任 AI 返回结果。
- 更新 `conversation-log.md`，记录本机训练暂停点和下次接续题。

### 今日理解

- 内容 hash 解决的是“重复文件识别”，不是“真实文件类型识别”；真实文件类型要靠 Tika/MIME 内容探测。
- 并发上传同一份简历时，业务层先查只是优化，数据库唯一索引才是最终兜底；更完整做法是捕获唯一约束异常后回查旧记录。
- AI 是外部依赖，不能无限等待和无限重试；失败时要通过规则版分析兜底，避免外部服务拖垮主流程。
- AI 输出要当成不可信输入，必须做结构化解析、字段、范围、枚举和业务规则校验。
- HashMap put 流程不能混入 CAS；CAS 是 ConcurrentHashMap 等并发结构常见手段。

### 下一步

- 继续八股训练题：`HashMap 为什么容量是 2 的幂？`
- 再做一轮 `interview-assistant` 项目 5 题口述，重点检查是否还能讲清 hash 去重、AI 兜底和 Prompt Injection。
- 后续择机把 `interview-assistant` 的“并发重复上传捕获唯一约束异常后回查旧记录”做成一个小接管任务。

### 补充：README 文档职责治理

- 检查当前仓库 Markdown 文档后，在 `README.md` 新增“文档唯一职责规则”。
- 明确每个文档的唯一职责和不应该写入的内容，避免 `profile.md`、`jd-tracking.md`、`knowledge-answer-bank.md`、`HANDOFF.md` 等文件后续互相重复。
- 当前策略是先保留现有文档结构，通过 README 约束归档规则；暂不删除、不移动、不合并文件。

### 补充：profile 职责纠偏

- 用户指出 `profile.md` 只应登记用户自身实际情况和档案状态，不应混入项目资产盘点、项目学习优先级或项目简历建议。
- 已修正 `profile.md`：删除项目资产与简历使用建议，保留个人基本情况、工作时间线、求职主线、当前能力状态、简历表达边界和档案登记状态。
- 后续项目资产、项目边界和项目学习优先级应放在项目卡、学习计划或 `HANDOFF.md`，不要再写入 `profile.md`。

### 补充：handoff 与 conversation 分工

- 明确启动流程：先读 `HANDOFF.md` 获取当前大任务，再读 `conversation-log.md` 获取最近对话重点和聊天进度。
- 更新 `README.md`、`AGENTS.md`、`HANDOFF.md` 和 `conversation-log.md`，固化该分工。
- `study-log.md` 回到每日学习结果记录，不作为聊天接续主入口。

### 补充：学习启动协议

- 用户明确：每次准备学习或询问“上次学到哪里了”时，Codex 要先 `git pull`，确保公司电脑和家里电脑的文档同步。
- 启动顺序固定为：先读 `HANDOFF.md` 获取当前大任务，再读 `conversation-log.md` 获取最新聊天暂停点，再按需要读 `study-log.md` 和 `java-backend-interview-plan.md`。
- 后续继续学习时，直接从 `conversation-log.md` 最新记录的“下次接续”开始；当前接续点仍是 `HashMap 为什么容量是 2 的幂？`

## 2026-06-13

### 今日主题

纠正 `interview-assistant` 和 `interview-guide` 的项目归属边界。

### 已完成

- 明确 `interview-guide` 不是用户项目，而是导师项目/参考项目。
- 明确简历和面试项目经历中只讲 `interview-assistant`，不能把 `interview-guide` 包装成个人成果。
- 更新 `AGENTS.md`，加入 `interview-guide` 边界规则，后续 Codex 必须按该口径回答。
- 更新 `HANDOFF.md` 和 `java-backend-interview-plan.md`，把 Day 1 项目话术收敛到 `interview-assistant` 本身。
- 更新 `knowledge-answer-bank.md`，把 RAG 的项目关联改成“参考项目只能作为学习和功能规划参考”。

### 今日理解

- 面试里可以说自己参考过成熟系统或导师项目的功能拆分思路，但不能把参考项目讲成自己的项目。
- `interview-assistant` 的正确定位是：用户正在接管和开发的后端 MVP，当前重点是简历解析分析、面试会话、答题推进和报告生成。
- 简历表达要围绕真实实现、自己能讲清的模块、后续接管计划，而不是围绕参考项目。

### 下一步

- 继续 Day 1：整理 `interview-assistant` 项目卡片。
- 重新写 `interview-assistant` 的 30 秒、1 分钟、3 分钟项目话术，确保不把 `interview-guide` 写成个人经历。
- 把项目必会题补入 `knowledge-answer-bank.md`。

## 2026-06-12

### 今日主题

整理 Java 后端与 AI 工程化面试学习资料，建立跨电脑同步学习仓库结构。

### 已完成

- 创建 `AGENTS.md`，固化用户与 Codex 的学习协作流程。
- 更新 `AGENTS.md`，规定项目相关提问优先从 `https://github.com/BQHM` 获取最新上下文。
- 创建 `java-ai-interview-study-guide.md`。
- 创建 `knowledge-answer-bank.md`，用于沉淀可直接讲的知识点答案。
- 阅读知识星球文章《Java 后端面试通关全阶指南（涵盖后端通用体系）》的核心结构。
- 创建 `java-backend-interview-plan.md`，按文章阶段顺序改造成个人 6-8 周学习计划。
- 创建 `README.md`。
- 创建 `HANDOFF.md`。
- 创建 `study-log.md`。
- 明确后续路线：先复健 Java 后端基本盘，再接管 `interview-assistant`，最后做高并发下单小项目。

### 今日理解

- 现阶段不是继续堆 AI 生成项目，而是把已有项目接管成自己能讲清楚的资产。
- 面试资料不能只背题，要做到：概念、Demo、项目、追问。
- 以后每学一个知识点，都要同步补充到 `knowledge-answer-bank.md`。
- 学习顺序改为先项目与简历深挖，再 Java/MySQL/Redis，不直接从八股开刷。
- 之后 Codex 必须按“预习计划 -> 教材讲解 -> 八股回答 -> 项目关联 -> 追问训练 -> 答案沉淀 -> 日志和 handoff”的闭环推进。
- 项目相关问题不能只凭记忆回答，要优先读取 GitHub 上的最新 README、目录结构和关键源码。
- 跨电脑同步时，Git 负责同步文件，`HANDOFF.md` 负责同步上下文。

### 还不清楚

- 是否需要为每个项目单独维护项目卡片文档，还是先统一放在本仓库。
- 是否把其他项目也统一纳入一个学习总仓库，还是保持项目各自独立。

### 下一步

- 按 `java-backend-interview-plan.md` 第一阶段 Day 1，先从 GitHub 获取 `interview-assistant` 最新内容，再整理项目卡片。
- 写 `interview-assistant` 的 30 秒、1 分钟、3 分钟话术。
- 从项目中反推必会题，再补充到 `knowledge-answer-bank.md`。
