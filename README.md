# Java 面试与 AI 工程化学习仓库

这个仓库用于在多台电脑之间同步 Java 后端面试复习、AI 工程化学习、项目接管计划和 Codex handoff 文档。

远程仓库：

```text
https://github.com/BQHM/study-tools
```

项目源码来源：

```text
https://github.com/BQHM
```

后续做项目卡片、项目追问和简历话术时，优先读取 GitHub 上的最新项目内容，再结合本地副本和学习笔记。

## 当前目标

1. 恢复 Java 后端基本盘：集合、并发、JVM、Spring、MySQL、Redis、MQ。
2. 把已有项目从“AI 辅助产物”接管成自己能讲清楚的工程资产。
3. 准备一个小而硬的高并发下单/预约项目，逐步掌握限流、库存预热、Redis Lua、MQ、幂等、压测。
4. 学习 AI 工程化能力：LLM 接入、Prompt、结构化输出、RAG、幻觉处理、降级和成本控制。
5. 面向 AI Agent 工程师 JD，强化 Tool Calling、Memory、Planning、RAG、Agent 工作流和技术方案表达。

## 文档索引

| 文件 | 用途 |
| --- | --- |
| `profile.md` | 个人画像主档：学历/工作时间线、真实经历、求职主线、表达边界和待补充事实 |
| `jd-tracking.md` | JD 台账：把看过的 JD 按分隔线记录在一个文件里，保留厂商、岗位、匹配点和简历定制方向 |
| `conversation-log.md` | 对话接续记录：简短记录关键对话、暂停点和下次接续问题，方便换设备继续 |
| `java-backend-interview-plan.md` | Java 后端 6-8 周学习计划：阶段安排、八股顺序、银行 Java 和 AI Agent JD 对齐路线 |
| `knowledge-answer-bank.md` | 高频答案库：沉淀能直接口述的 Java、数据库、Redis、MQ、AI、项目和岗位定位答案 |
| `bank-java-jd-positioning.md` | 银行 Java 岗位专项：银行 JD 匹配、长亮/宁波银行经历包装、开户/存入/支取话术和八股优先级 |
| `ai-agent-jd-study-plan.md` | AI Agent 岗位专项：AI Agent JD 拆解、Tool Calling、Memory、Planning、RAG 和项目改造路线 |
| `interview-assistant-project-card.md` | `interview-assistant` 项目卡：项目定位、核心流程、三档话术、追问清单和接管计划 |
| `java-ai-interview-study-guide.md` | 系统学习资料：Java 后端与 AI 工程化知识讲解，偏教材和长线复习 |
| `study-log.md` | 学习日志：记录每天学了什么、理解了什么、还卡在哪里、下一步做什么 |
| `HANDOFF.md` | 交接文档：跨电脑/跨会话时优先读取，记录当前阶段、已完成、未完成和下一步 |
| `AGENTS.md` | Codex 协作规则：规定学习闭环、项目边界、文档维护方式和回答口径 |
| `.gitignore` | Git 忽略规则：避免提交本地临时文件、密钥和构建产物 |

## 文档唯一职责规则

这个仓库允许同一个主题出现在不同文档中，但每个文档只维护一种形态，避免后续跨电脑同步时出现多个版本互相冲突。

| 文档 | 唯一职责 | 不应该写入的内容 |
| --- | --- | --- |
| `README.md` | 仓库入口，说明仓库目标、文档地图、工作流和更新规则 | 具体学习笔记、每日进度、长篇答案 |
| `AGENTS.md` | Codex 行为规则，固定协作流程、项目边界和回答口径 | 每日学习流水、具体 JD 拆解、临时对话记录 |
| `HANDOFF.md` | 跨电脑、跨 Codex 会话的交接主档，记录当前阶段、未完成事项和下一步 | 完整教材内容、所有历史学习细节 |
| `study-log.md` | 每日学习日志，记录当天学了什么、卡在哪里、下一步做什么 | 长期规则、完整答案卡、项目完整话术 |
| `conversation-log.md` | 对话接续索引，只记录关键暂停点和影响后续学习的对话摘要 | 完整聊天记录、已经归档到主档的详细事实 |
| `profile.md` | 个人画像事实库，维护学历、工作时间线、真实经历和表达边界 | 针对某个 JD 的投递策略、八股答案 |
| `jd-tracking.md` | JD 台账，记录看过的岗位、要求、匹配点和简历定制方向 | 个人完整履历、通用教材内容 |
| `java-backend-interview-plan.md` | 总学习计划，维护阶段顺序、每日节奏和主题优先级 | 具体题目的长篇答案、专项 JD 的全部细节 |
| `java-ai-interview-study-guide.md` | 教材主体，系统讲 Java 后端、AI 工程化和系统设计知识 | 当天进度、交接状态、可直接背诵的短答案 |
| `knowledge-answer-bank.md` | 面试答案库，保存可以直接口述的答案卡 | 长篇教材、完整学习路线、未经验证的项目包装 |
| `interview-assistant-project-card.md` | `interview-assistant` 项目主卡，维护项目定位、流程、话术、追问和接管计划 | 参考项目 `interview-guide` 的成果包装、其他项目卡片 |
| `ai-agent-jd-study-plan.md` | AI Agent 岗位专项学习计划，维护 Agent 方向能力拆解和项目改造路线 | 银行 Java 岗位包装、每日学习流水 |
| `bank-java-jd-positioning.md` | 银行 Java 岗位专项，维护银行业务经历表达、岗位匹配和准备重点 | AI Agent 专项路线、通用 Java 教材 |

更新信息时按下面规则归档：

```text
个人事实 -> profile.md
新 JD -> jd-tracking.md
总计划变化 -> java-backend-interview-plan.md
系统知识讲解 -> java-ai-interview-study-guide.md
可口述答案 -> knowledge-answer-bank.md
项目话术和项目追问 -> 对应项目卡片
当天学习结果 -> study-log.md
换电脑/换会话交接 -> HANDOFF.md
刚聊到哪、下次从哪继续 -> conversation-log.md
Codex 应该如何协作 -> AGENTS.md
```

## 推荐工作流

### 每次开始学习前

```bash
git pull
```

然后阅读：

```text
HANDOFF.md
study-log.md 最近一条记录
```

### 每次结束学习后

1. 更新 `study-log.md`。
2. 更新 `HANDOFF.md` 的当前状态、下一步和阻塞点。
3. 如需暂停或换设备，在 `conversation-log.md` 追加一条关键对话摘要。
4. 提交并推送：

```bash
git status
git add AGENTS.md README.md HANDOFF.md study-log.md conversation-log.md profile.md jd-tracking.md java-backend-interview-plan.md java-ai-interview-study-guide.md knowledge-answer-bank.md ai-agent-jd-study-plan.md bank-java-jd-positioning.md interview-assistant-project-card.md .gitignore
git commit -m "docs: update interview study handoff"
git push
```

### 新电脑拉取

```bash
git clone https://github.com/BQHM/study-tools.git
cd study-tools
```

然后先读：

```text
HANDOFF.md
study-log.md
conversation-log.md
```

## Codex 使用约定

对 Codex 说：

```text
先阅读 HANDOFF.md 和 study-log.md，接着帮我继续今天的 Java 面试复习。
```

或者：

```text
根据 HANDOFF.md，帮我继续接管 interview-assistant 项目，今天只做一个小切片。
```

项目相关任务可以这样说：

```text
请先从 https://github.com/BQHM 获取 interview-assistant 的最新 README 和代码结构，再帮我整理项目卡片。
```

重要原则：

- 不让 AI 一次性生成大项目。
- 每天只推进一个小主题。
- 每个知识点都要落到：概念、Demo、项目、追问。
- 面向 AI Agent JD 时，每个八股还要额外回答：它如何服务 Agent 产品落地？
- 面向银行 Java JD 时，每个八股要额外回答：它如何服务开户、存入、支取、数币等交易系统？
- 每次换电脑前必须更新 handoff。
- 如果刚结束一段关键对话，也要更新 `conversation-log.md`，方便下一台设备快速接上。
- `interview-guide` 是导师项目/参考项目，不写入个人简历项目经历；个人项目只围绕 `interview-assistant` 讲真实实现和接管计划。
