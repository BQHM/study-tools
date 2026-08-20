# AI Agent 工程师 JD 对齐学习计划

> 生成日期：2026-06-21
>
> 最近更新：2026-08-20（补充 MCP / A2A 基础认知，并明确尚未在个人项目中落地）
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
+ MCP / A2A 协议接入
+ B 端产品落地协作
+ 技术方案表达
```

所以学习重点要从“只刷八股”调整成：

```text
八股知识点 -> Agent 项目中的工程问题 -> 能讲方案、风险和取舍
```

补充：MCP（Model Context Protocol）用于标准化 Agent 与工具/数据的连接，A2A（Agent-to-Agent）用于 Agent 之间的互操作，两者关注的连接层级不同。当前先掌握概念、边界和安全问题；具体版本、生态支持和 SDK 状态在面试前以官方最新资料为准。

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
| 协议接入 | 用标准协议连接工具与 Agent | MCP（agent→tool）、A2A（agent→agent） | 工具以 MCP Server 暴露、多 Agent 协作 |
| 大模型生态 | 了解主流框架和实践 | Spring AI 2.x、LangChain、LangGraph、Dify、Coze | Java 后端优先用 Spring AI |

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
-> MCP / A2A 协议
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

- `07_面试答案库.md` 新增 AI 结构化输出和失败兜底答案卡。
- `interview-assistant` 简历分析链路图。

### 第 2 周：Tool Calling 和工具编排

目标：

让 Agent 能调用后端工具，而不是只聊天。

学习内容：

- Function Calling / Tool Calling。
- 工具入参、出参、异常处理。
- 工具选择和权限控制。
- 工具调用日志。
- MCP 基础：用 Spring AI 2.x MCP Server Starter 把工具暴露成标准服务。

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
- 有能力时，把其中 1 个工具用 Spring AI MCP Server Starter 暴露，验证客户端能发现并调用，体验 MCP 的“工具即服务”。

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

- 把 `07_面试答案库.md` 作为第一版知识库来源。
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
- 能用第 8 节模板讲清 MCP / A2A 在项目里的位置。

## 8. MCP 与 A2A 速通（2026 必备）

> 更新于 2026-08-20。当前目标是建立直觉和表达边界，不把“了解协议”说成“已经完成项目落地”。具体版本和厂商支持情况在使用前以官方文档为准。

### 8.1 MCP（Model Context Protocol）

一句话答案：

```text
MCP 是把“AI 应用连接外部工具、数据、系统”这件事标准化的开放协议，相当于 AI 世界的 USB-C 接口。
```

展开要点：

- 解决什么问题：每个 AI 应用接数据库、文件、搜索、业务系统时都要自己写一套工具接入逻辑，MCP 用统一协议替代，一次接入、到处复用。
- 组成：MCP Client 和 MCP Server。Server 暴露工具/资源/提示，Client（AI 应用）发现并调用。
- 传输：支持 STDIO、SSE、Streamable-HTTP 等。
- Java 落地方向：Spring AI 2.x 提供 MCP Client/Server 相关能力，可以作为后续实验方向；`interview-assistant` 当前还没有接入 MCP。
- 与 Tool Calling 的关系：Tool Calling 是模型能力（模型决定调用哪个函数）；MCP 是工具接入协议（怎么把工具暴露给 AI 应用）。二者互补：先用 MCP 把工具接进来，再靠 Tool Calling 让模型调用。
- 常见追问：MCP 里怎么保证安全？（权限、作用域、Server 只暴露最小工具集）；工具返回失败 Agent 怎么办？（错误结构 + 重试/降级）。

### 8.2 A2A（Agent-to-Agent）

一句话答案：

```text
A2A 是让不同框架、不同团队开发的 Agent 之间能够发现能力、委托任务并交换结果的开放协议。
```

展开要点：

- 与 MCP 的关系：**MCP 管 Agent 到工具的连接，A2A 管 Agent 到 Agent 的连接**，官方明确两者互补、不是竞争。
- 解决的问题：Agent 由不同团队用 LangGraph、CrewAI、自定义框架开发，互相之间无法协作；A2A 提供统一通信语言（发现、任务委托、结果共享）。
- 定位边界：它不是 Agent 开发框架，不是子 Agent/工具调用协议，也不替代 MCP。
- 生态和 SDK 状态变化较快，实际选型前需要查官方文档，当前不把某个版本或 Java SDK 作为已经掌握的项目经验。
- 面试表达：先能说清“MCP 连接工具，A2A 连接 Agent”，再说明自己尚未完成 A2A 落地。

### 8.3 面试一口回答模板

```text
AI Agent 工程化里，我关注两层连接：工具层可以用 MCP 标准化 Agent 对后端能力、数据库和知识库的访问，Agent 之间的协作可以用 A2A。MCP 偏工具和数据接入，A2A 偏 Agent 互操作。我目前先完成了 Spring AI 的模型调用、结构化输出和规则兜底，MCP/A2A 仍处于学习和后续实验阶段。
```

## 9. interview-assistant 改造方向

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

## 10. 八股和 Agent 项目的绑定

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

## 11. 面试定位话术

30 秒版本：

我现在的方向是 Java 后端加 AI 应用工程化。我不做模型训练，重点学习把大模型能力接入业务系统，例如 Prompt 模板、结构化输出、工具调用、RAG、用户记忆、异步任务、降级和成本控制。`interview-assistant` 当前已经完成模型调用、Skill 出题和规则兜底，MCP、Memory、RAG 和完整 Agent 工作流仍是后续计划。

1 分钟版本：

我主要走 Java 后端和 AI 应用工程方向。传统后端能力上，我重点复习 Spring Boot、数据库、Redis、线程池、MQ 和 JVM 排查；AI 工程化上，我正在学习 LLM 接入、结构化输出、Tool Calling、RAG、Memory 和 Agent 工作流，也了解 MCP 与 A2A 分别解决工具接入和 Agent 协作问题。`interview-assistant` 当前能读取简历、生成 Skill 定向题目、评估答案并生成报告；结合 JD 分析、知识库、长期记忆和 MCP/A2A 还没有完成，属于后续演进计划。

## 12. 单次学习闭环

每次只推进一个主题：

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
