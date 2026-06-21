# AI Agent 工程师 JD 对齐学习计划

> 生成日期：2026-06-21
>
> 来源：用户提供的 AI Agent 工程师 JD 截图。
>
> 目标：把现有 Java 后端面试复习，调整为更贴近“AI Agent 工程化落地”的学习路线。

## 1. JD 关键信息

岗位：

AI Agent 工程师。

岗位属性：

- 地点：无锡。
- 年限：1-3 年。
- 学历：本科。
- 方向：机器学习类 AI，B 端产品。

岗位职责拆解：

1. 参与需求拆解、技术方案评审与项目排期，推动 AI Agent 产品从原型到上线的全流程落地。
2. 跟踪并调研 Agent 领域前沿技术，例如多模态交互、工具调用、记忆增强、自主规划，并探索落地优化方案。
3. 持续关注大模型与 AI Agent 生态，把行业实践和创新思路融入日常开发，为产品迭代和技术突破提供支持。

任职要求拆解：

1. 本科及以上，计算机、软件工程、人工智能、数据科学、数学统计等相关专业。
2. 具备良好的沟通表达和跨团队协作能力，能清晰传达技术方案与风险，高效推进项目。

## 2. 岗位本质判断

这个岗位不是纯算法岗，也不是传统 Java CRUD 岗，而是：

```text
Java 后端基本盘
+ LLM 应用开发
+ Agent 工作流编排
+ B 端产品落地协作
+ 技术方案表达
```

所以学习重点要从“只刷八股”调整成：

```text
八股知识点 -> Agent 项目中的工程问题 -> 能讲方案、风险和取舍
```

## 3. 能力模型

| JD 能力 | 具体含义 | 对应学习内容 | 项目落点 |
| --- | --- | --- | --- |
| 需求拆解 | 把业务目标拆成可开发任务 | 需求分析、接口设计、任务排期 | `interview-assistant` 功能切片 |
| 方案评审 | 讲清方案、风险、取舍 | 技术方案文档、异常场景、降级 | AI 分析、面试评估、RAG 方案 |
| Agent 原型上线 | 从 Demo 到可用后端服务 | Controller、Service、DB、状态、日志 | 面试准备 Agent |
| 工具调用 | Agent 调用后端能力 | Function Calling / Tool Calling | 简历分析工具、出题工具、评分工具 |
| 记忆增强 | 保存用户历史和偏好 | 短期会话、长期记忆、画像表 | 薄弱知识点记忆 |
| 自主规划 | 拆解多步骤任务并执行 | Plan-and-Execute、状态机 | 生成学习计划并追踪进度 |
| 多模态交互 | 文件、图片、语音等输入 | 文件解析、OCR/ASR 基本认知 | 简历文件、后续语音面试 |
| 大模型生态 | 了解主流框架和实践 | Spring AI、LangChain、LangGraph、Dify、Coze | Java 后端优先用 Spring AI |

## 4. 当前优势和短板

当前优势：

- 有 Java 后端学习计划和答案库。
- 已经有 `interview-assistant` 作为 AI 应用项目载体。
- 项目里已有 Spring AI、Prompt 模板、结构化输出、AI 失败兜底。
- 有跨电脑 handoff 和学习日志，适合长期迭代。

当前短板：

- Agent 概念还没有形成系统表达。
- Tool Calling、Memory、Planning、RAG 还没有落到项目代码或方案里。
- 八股和 AI Agent 项目的关联还不够强。
- 技术方案评审、风险表达和排期能力需要补文档化训练。

## 5. 学习主线调整

原主线：

```text
项目深挖 -> Java/MySQL/Redis 八股 -> Spring -> 系统设计 -> 高并发 -> JVM
```

JD 对齐后的主线：

```text
interview-assistant 项目
-> Java 后端八股
-> LLM 工程化
-> Tool Calling
-> RAG 和 Memory
-> Agent 工作流
-> 技术方案和项目表达
```

注意：不是放弃八股，而是让每个八股都服务 Agent 项目。

## 6. 八股优先级调整

为了适配这个 JD，八股学习优先级调整为：

1. Spring Boot、REST 接口、参数校验、统一响应、异常处理。
2. MySQL 表设计、索引、事务、唯一约束。
3. Redis 缓存、限流、会话状态、分布式锁。
4. 线程池、异步任务、MQ。
5. HashMap、ConcurrentHashMap、ThreadLocal。
6. JVM 排查基础。

原因：

- Agent 产品落地首先要有稳定后端服务。
- LLM 调用需要异步、限流、重试、降级和日志。
- Memory、RAG、答题记录都离不开数据库设计。
- Tool Calling 需要接口设计、权限控制和异常处理。

## 7. 4 周 JD 适配计划

### 第 1 周：LLM 应用工程基础

目标：

把“调用大模型”从 Demo 变成稳定后端能力。

学习内容：

- 大模型 API 调用。
- Prompt 模板。
- 结构化输出 JSON。
- 超时、重试、降级。
- Token 成本和日志。

项目落地：

- 复盘 `ResumeGradingService`。
- 写清 AI 简历分析成功路径和失败路径。
- 准备回答：AI 输出不稳定怎么办？

产出：

- `knowledge-answer-bank.md` 新增 AI 结构化输出和失败兜底答案卡。
- `interview-assistant` 简历分析链路图。

### 第 2 周：Tool Calling 和工具编排

目标：

让 Agent 能调用后端工具，而不是只聊天。

学习内容：

- Function Calling / Tool Calling。
- 工具入参、出参、异常处理。
- 工具选择和权限控制。
- 工具调用日志。

项目工具设计：

```text
parseResumeTool
analyzeResumeTool
generateQuestionTool
evaluateAnswerTool
searchKnowledgeTool
makeStudyPlanTool
```

项目落地：

- 先不急着全实现，先写工具清单和接口草图。
- 选择 1 个工具做最小闭环，例如 `generateQuestionTool`。

### 第 3 周：RAG 和 Memory

目标：

让 Agent 能基于资料回答，并记住用户薄弱点。

学习内容：

- 文档切分。
- Embedding。
- 向量检索。
- TopK 和相似度阈值。
- 短期记忆和长期记忆。
- 用户画像和薄弱点记录。

项目落地：

- 把 `knowledge-answer-bank.md` 作为第一版知识库来源。
- 设计 `user_weakness_memory` 表或等价实体。
- 用户答错后，把知识点、错误原因、下次复习时间写入记忆。

### 第 4 周：Agent 工作流和产品化

目标：

把单点能力串成可解释的 Agent 流程。

学习内容：

- ReAct 基本思想。
- Plan-and-Execute。
- 状态机。
- 多步骤任务编排。
- 失败回退和人工确认。

项目流程：

```text
上传简历
-> Agent 分析岗位匹配度
-> 生成学习计划
-> 调用知识库出题
-> 用户回答
-> Agent 评分
-> 更新薄弱点记忆
-> 生成下一轮训练计划
```

产出：

- 一页技术方案。
- 一张流程图。
- 一版 1 分钟项目话术。
- 5 个项目追问答案。

## 8. interview-assistant 改造方向

项目新定位：

```text
AI 面试准备 Agent
```

核心能力：

1. 读取简历并分析岗位匹配度。
2. 根据 JD 和简历生成学习计划。
3. 调用知识库生成八股题和项目追问。
4. 根据用户回答做评分和反馈。
5. 记录用户薄弱点作为长期记忆。
6. 下次训练优先追问薄弱知识点。

不要一开始做的内容：

- 不先做完整前端。
- 不先做语音面试。
- 不先做复杂多 Agent。
- 不先追求完整 RAG 平台。

最小切片顺序：

1. AI 分析结果结构化和兜底讲清楚。
2. 面试题生成工具化。
3. 答案评估工具化。
4. 用户薄弱点记忆表。
5. 基于答案库的简化 RAG。
6. Agent 生成下一轮学习计划。

## 9. 八股和 Agent 项目的绑定

| 八股主题 | Agent 项目中的对应问题 |
| --- | --- |
| HashMap | 工具注册表、临时上下文、分类聚合怎么存？ |
| ConcurrentHashMap | 多线程工具执行状态怎么保证安全？ |
| ThreadLocal | 当前用户上下文如何传递和清理？ |
| 线程池 | AI 分析和评估如何异步执行？ |
| MySQL 索引 | 用户记忆、答题记录、会话列表怎么查得快？ |
| 事务 | 答案保存和薄弱点更新如何保证一致？ |
| Redis | 会话缓存、限流、热点知识点缓存怎么做？ |
| MQ | AI 任务失败重试和削峰怎么做？ |
| Spring AOP | 限流、日志、权限校验如何统一处理？ |
| JVM 排查 | AI 服务调用堆积导致线程和内存问题怎么定位？ |

## 10. 面试定位话术

30 秒版本：

我现在的方向是 Java 后端加 AI Agent 工程化。我不做模型训练，重点是把大模型能力落到业务系统里，比如 Prompt 模板、结构化输出、工具调用、RAG、用户记忆、异步任务、降级和成本控制。我正在把 `interview-assistant` 改造成 AI 面试准备 Agent，用它练习从需求拆解、后端实现到项目表达的完整流程。

1 分钟版本：

我主要走 Java 后端和 AI 应用工程方向。传统后端能力上，我重点复习 Spring Boot、MySQL、Redis、线程池、MQ 和 JVM 排查；AI 工程化上，我关注 LLM 接入、结构化输出、Tool Calling、RAG、Memory 和 Agent 工作流。我的项目 `interview-assistant` 原来是一个智能面试助手 MVP，现在我准备把它改造成 AI 面试准备 Agent：它能读取简历，结合 JD 分析薄弱点，生成学习计划，调用知识库出题，评估用户答案，并记录长期薄弱点。这个项目能比较好地对应 AI Agent 岗位里“从原型到上线落地”的要求。

## 11. 每日学习闭环

每天只推进一个主题：

```text
1. 学一个八股或 Agent 工程主题。
2. 写一句“它解决什么问题”。
3. 讲清原理。
4. 绑定到 interview-assistant。
5. 写一张答案卡。
6. 做 3 个追问。
7. 更新日志和 handoff。
```

下一次建议主题：

```text
线程池 + AI 异步任务
```

原因：这个主题比单独从 HashMap 继续刷更贴近 JD，可以同时覆盖 Java 并发八股和 AI Agent 产品落地。
