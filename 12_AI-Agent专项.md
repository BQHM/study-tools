# AI Agent 工程师专项

> 最近更新：2026-08-25。
>
> 用途：维护 AI Agent 岗位能力模型、技术边界、项目演进和面试表达。具体执行顺序以 `05_总学习计划.md` 为准。
>
> 官方核验：Spring AI 当前参考文档为 2.0.1；MCP 最新规范页面显示版本 `2026-07-28`。版本变化快，开发前必须再次核验。

## 1. 岗位本质

AI Agent 工程师通常不是纯模型训练岗，也不是“会写 Prompt”就够，而是：

```text
后端工程能力
+ 可靠 LLM 调用
+ 工具和任务编排
+ 状态与数据管理
+ 评估、可观测性和安全
+ 产品落地与技术方案表达
```

当前求职定位：

```text
Java 后端背景的 AI 应用工程候选人，
主攻 Java + Spring AI 的可靠 AI 应用和 Agent 工程化。
```

不能包装成：

- 模型训练或算法专家。
- 已上线完整 Agent 平台。
- 已完成 RAG、Memory、MCP、A2A 或多 Agent 项目落地。
- 独立从零完成全部 AI 辅助代码。

## 2. ChatBot、Workflow 与 Agent

### ChatBot

主要根据用户输入生成回复，可以有多轮上下文，但通常不负责完成复杂任务。

### Workflow

步骤主要由程序预先定义，模型在指定节点执行分析、分类或生成。它更可控、可测试，也更适合多数业务系统的第一版。

### Agent

模型围绕目标，根据当前状态和观察动态决定下一步，可能调用工具、更新状态、请求人工确认并继续执行。

工程原则：

```text
能用普通代码解决，就不用模型。
能用固定 Workflow 解决，就不急着上动态 Agent。
单 Agent 能解决，就不急着上多 Agent。
```

`interview-assistant` 当前属于：

```text
AI 应用 + 固定业务 Workflow
```

它已有简历解析、AI 分析、Skill 定向出题、答案评估和报告生成，但尚未具备通用的动态工具选择、任务规划、Agent 运行状态、暂停恢复和人工审批闭环。

## 3. 能力优先级

### P0：求职和项目必须掌握

1. ChatBot、Workflow、Agent 的边界和选型。
2. Prompt、结构化输出、Schema 和业务校验。
3. 超时、有限重试、降级、Token/成本和上下文管理。
4. Tool Calling：工具 Schema、权限、参数、幂等和错误处理。
5. Workflow 状态机、异步任务、暂停恢复和失败补偿。
6. Tracing、Metrics、Prompt/模型版本和 Agent Evals。
7. Guardrails、Prompt Injection、数据隔离、工具安全和人工审批。

### P1：形成完整 AI 应用能力

1. RAG：切分、元数据、召回、过滤、重排、引用和评估。
2. Memory：会话上下文、业务长期记忆、生命周期和隐私。
3. Java 后端可靠性：Spring、MySQL、Redis、线程池、MQ、测试和 JVM。

### P2：有需求再落地

1. MCP Client/Server 小实验。
2. 多模态输入。
3. 更复杂的模型路由和长任务执行。

### P3：当前只了解

1. A2A。
2. 多 Agent 协作。
3. 同时深入多个 Agent 框架。

## 4. 可靠 LLM 调用

结构化输出不是“模型返回 JSON 就结束”。必须经过：

```text
Provider 原生结构化输出（可用时）
-> JSON Schema / DTO 转换
-> 格式校验
-> 字段、类型、枚举校验
-> 业务规则校验
-> 有限重试或规则兜底
-> 持久化
```

三层校验：

- 格式：JSON 是否可解析。
- 结构：字段、类型、枚举、必填项是否合法。
- 业务：分数范围、题量、Skill 配额、数据归属和内容是否有效。

重试原则：

- 网络抖动、限流、临时服务错误可以有限重试，并使用退避和抖动。
- 参数错误、权限错误、确定性的业务校验失败不应盲目重试。
- 重试必须有次数、总耗时和成本上限。

## 5. Tool Calling

Tool Calling 的边界：

```text
模型负责选择工具和生成候选参数；
程序负责校验、授权、真实执行、审计和错误处理。
```

完整链路：

```text
用户目标
-> 模型请求工具
-> 校验工具白名单、参数和用户权限
-> 执行真实函数/API
-> 返回结构化结果或错误
-> 模型继续生成
-> 记录 Trace 和审计日志
```

必须考虑：

- 最小权限和数据范围。
- 输入 Schema 与业务校验。
- 超时、幂等、并发和重试边界。
- SSRF、任意文件访问和命令执行风险。
- 删除、转账、发布等高风险动作的人工审批。

`interview-assistant` 第一版建议做只读工具，例如 `getResumeSummary`，不要先做删除或修改类工具。

## 6. 状态与可靠性

Agent/Workflow 不是一个长方法调用。需要显式任务状态：

```text
CREATED -> RUNNING -> WAITING_APPROVAL -> COMPLETED
                    -> FAILED / CANCELED
```

需要设计：

- 状态迁移和合法性校验。
- 幂等键、唯一约束、乐观锁。
- 暂停、恢复、取消和超时。
- 外部模型调用与数据库事务边界。
- 失败重试、死信、补偿和人工处理入口。

`interview-assistant` 当前的面试会话状态可以作为第一张状态机练习图。

## 7. 评估与可观测性

这是 P0。AI 功能不能只用“接口返回 200”验收。

### 可观测性

至少记录：

```text
traceId、业务类型、模型、Prompt 版本、工具调用、
Token、延迟、重试、错误类型、兜底结果、脱敏后的输入输出摘要。
```

### 评估

- 离线：Golden Set、结构正确率、相关性、评分一致性、引用正确率、拒答率。
- 线上：成功率、P95/P99 延迟、Token/费用、兜底率、人工反馈和失败分类。
- LLM-as-judge：可以辅助，但不能作为唯一评委；需要规则和人工抽检校准。

项目最小产出：

- 10-20 条脱敏测试样本。
- AI 简历分析、出题和答案评估的质量标准。
- Prompt/模型版本和失败分类记录。

## 8. 安全与人工审批

重点风险：

- 直接和间接 Prompt Injection。
- 跨用户数据泄露、RAG 权限绕过。
- 工具越权、参数注入、SSRF、任意 URL/文件访问。
- 敏感信息进入模型、日志或 Trace。
- 模型触发不可逆操作。

安全链路：

```text
指令与数据隔离
-> 工具白名单和最小权限
-> 参数、身份和数据范围校验
-> 输出校验
-> 高风险操作人工审批
-> 审计、告警和撤销/补偿
```

## 9. RAG 与 Memory

### RAG

```text
加载和清洗
-> 切分
-> 元数据与权限标签
-> Embedding 和入库
-> 召回与过滤
-> 重排
-> 引用
-> 生成与校验
-> 评估
```

必须回答：

- 如何选择 chunk 大小和重叠？
- 如何按用户、租户和数据权限过滤？
- 简历删除后，向量数据如何同步删除？
- 检索错误或没有可靠来源时是否拒答？
- 如何分别评估检索和最终答案？

### Memory

- 短期记忆：当前会话完成任务所需的上下文。
- 长期记忆：经过确认的用户偏好、薄弱点和历史结果。
- 知识库：外部事实资料，不等于用户记忆。

长期记忆需要来源、置信度、修改、过期、删除和隐私授权机制。

## 10. MCP 与 A2A

### MCP：P2

MCP 标准化 AI 应用与外部工具、资源和提示之间的连接。它不负责 Agent 规划，也不会自动解决业务权限、幂等和工具安全。

当前项目先掌握 Tool Calling，后续再用 Spring AI MCP Client/Server 做一个只读工具实验。

### A2A：P3

A2A 用于独立 Agent 之间的能力发现、任务委托、状态和结果协作。当前单体项目没有明确跨 Agent 协作需求，不应优先投入。

## 11. 框架策略

主线：

```text
Java + Spring AI 2.x
```

了解但不同时深入：

- LangChain / LangGraph：Python/JS 生态中的 Agent 与图编排。
- OpenAI Agents SDK：Agent、工具、Guardrails、Handoffs、Sessions、Tracing。
- Google ADK：多语言 Agent 开发工具包。
- Dify / Coze：低代码 AI 应用平台。

选框架前先问：项目是否真的需要它，它解决了什么复杂度，又引入了什么锁定和调试成本。

## 12. interview-assistant 演进边界

当前已实现：

- 简历文件解析、内容 hash 去重和对象存储。
- Spring AI 调用、结构化结果和规则兜底。
- Skill 定向出题、答案评估、会话状态和报告聚合。

当前正在接管：

- 事务和并发边界。
- 前后端接口契约。
- 真实测试和失败场景。

后续规划：

1. 结构化输出三层校验和测试。
2. AI 调用 Trace、Prompt/模型版本和质量评估。
3. 一个只读 Tool Calling 闭环。
4. 可暂停恢复的学习计划 Workflow。
5. 简化 RAG 和用户薄弱点长期记忆。
6. 有实际需求后再做 MCP；A2A 和多 Agent 暂不安排。

## 13. 面试话术

30 秒版本：

```text
我主要走 Java 后端和 AI 应用工程化方向，重点不是模型训练，而是把大模型能力做成可靠业务系统。我正在接管 interview-assistant，它目前是具有固定工作流的 AI 面试应用，已经完成简历分析、Skill 出题、答案评估和规则兜底。我接下来重点补结构化校验、调用追踪、评估和 Tool Calling，不会把尚未完成的 RAG、Memory 或完整 Agent 能力写成已有成果。
```

## 14. 当前下一步

1. 回答 ChatBot、Workflow、Agent 的区别，并判断当前项目定位。
2. 学习结构化输出的格式、结构和业务三层校验。
3. 复盘 `ResumeGradingService` 的真实成功和失败路径。
4. 设计第一个只读 Tool Calling 闭环。

## 15. 官方资料

- Spring AI 2.0.1：<https://docs.spring.io/spring-ai/reference/>
- Spring AI Structured Output：<https://docs.spring.io/spring-ai/reference/api/structured-output.html>
- Spring AI Tool Calling：<https://docs.spring.io/spring-ai/reference/api/tools.html>
- Spring AI Observability：<https://docs.spring.io/spring-ai/reference/observability/index.html>
- Spring AI MCP：<https://docs.spring.io/spring-ai/reference/api/mcp/mcp-overview.html>
- MCP 最新规范：<https://modelcontextprotocol.io/specification/latest>
- A2A 最新规范：<https://a2a-protocol.org/latest/specification/>
- OpenAI Agents 指南：<https://platform.openai.com/docs/guides/agents.md>
- Anthropic Building Effective AI Agents：<https://www.anthropic.com/research/building-effective-agents>
