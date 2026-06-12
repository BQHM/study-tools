# Java 面试与 AI 工程化学习仓库

这个仓库用于在多台电脑之间同步 Java 后端面试复习、AI 工程化学习、项目接管计划和 Codex handoff 文档。

远程仓库：

```text
https://github.com/BQHM/study-tools
```

## 当前目标

1. 恢复 Java 后端基本盘：集合、并发、JVM、Spring、MySQL、Redis、MQ。
2. 把已有项目从“AI 辅助产物”接管成自己能讲清楚的工程资产。
3. 准备一个小而硬的高并发下单/预约项目，逐步掌握限流、库存预热、Redis Lua、MQ、幂等、压测。
4. 学习 AI 工程化能力：LLM 接入、Prompt、结构化输出、RAG、幻觉处理、降级和成本控制。

## 文档索引

| 文件 | 用途 |
| --- | --- |
| `java-ai-interview-study-guide.md` | Java 后端与 AI 工程化面试学习资料 |
| `HANDOFF.md` | 两台电脑 / 两个 Codex 之间交接当前进度 |
| `study-log.md` | 每日学习记录和复盘 |
| `.gitignore` | 避免提交本地临时文件、密钥和构建产物 |

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
3. 提交并推送：

```bash
git status
git add README.md HANDOFF.md study-log.md java-ai-interview-study-guide.md .gitignore
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

重要原则：

- 不让 AI 一次性生成大项目。
- 每天只推进一个小主题。
- 每个知识点都要落到：概念、Demo、项目、追问。
- 每次换电脑前必须更新 handoff。
