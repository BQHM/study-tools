# Codex Handoff

> 作用：在公司电脑、家里电脑以及不同 Codex 会话之间同步上下文。每次结束学习或开发前都更新这里。

## 当前日期

2026-06-12

## 当前阶段

阶段：Java 后端面试复健 + AI 工程化学习资料整理。

当前重点：

- 先恢复已有知识和项目表达，不急着开新大项目。
- 使用 `java-ai-interview-study-guide.md` 作为主复习资料。
- 后续优先接管 `interview-assistant`，因为它比 `FixLedger` 小，更适合真正吃透。
- 远程同步仓库使用 `https://github.com/BQHM/study-tools`。

## 已完成

- 整理了父目录项目现状：
  - `FixLedger`：AI 开发的完整业务项目，可作为后续代码审查、重构、测试补充对象。
  - `interview-assistant`：在 AI 辅助下参考 `interview-guide` 开发，适合作为主接管项目。
  - `java-core-lab`：AI 辅助学习实验仓，适合复习 Java 集合、并发、JVM 排查。
  - `truckfarm`：旧项目和现代化重构设想，目前不适合作为主简历项目。
- 创建了 `java-ai-interview-study-guide.md`：
  - Java 基础、集合、并发、JVM。
  - Spring / MySQL / Redis / MQ。
  - 高并发项目追问。
  - AI 工程化、RAG、Embedding、Prompt、结构化输出。
  - 两个月学习路线和每日复习模板。
- 明确了学习原则：
  - 不让 AI 直接生成完整项目。
  - 用 AI 解释、Review、追问、辅助复盘。
  - 每个知识点都要能讲“问题、原理、项目、坑、排查”。

## 当前未完成

- 当前目录还没有初始化 Git 仓库。
- 还没有推送到远程仓库。
- 还没有开始逐日学习记录。
- 还没有正式接管 `interview-assistant` 的新功能。

## 下一步建议

### 第一步：初始化同步仓库

在当前目录执行：

```bash
git init
git add README.md HANDOFF.md study-log.md java-ai-interview-study-guide.md .gitignore
git commit -m "docs: initialize java interview study repo"
git branch -M main
git remote add origin https://github.com/BQHM/study-tools.git
git push -u origin main
```

如果远程仓库已经有 README，先 `git pull --rebase origin main` 再 push。

### 第二步：开始第 1 周复习

从 `java-ai-interview-study-guide.md` 的这些章节开始：

```text
1. Java 基础高频题
2. 集合框架高频题
3. Java 并发高频题
```

每天只选一个主题，例如：

```text
Day 1：HashMap
Day 2：ConcurrentHashMap
Day 3：volatile + synchronized
Day 4：ThreadLocal
Day 5：线程池
Day 6：AQS
Day 7：复盘和模拟面试
```

### 第三步：用 java-core-lab 做实验

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
请先阅读 HANDOFF.md 和 study-log.md，然后根据 java-ai-interview-study-guide.md 带我复习 HashMap，并结合 java-core-lab 里的 Demo 做讲解和追问。
```

或者：

```text
请根据 HANDOFF.md，帮我开始接管 interview-assistant，今天只做异步简历分析任务的设计文档，不直接生成代码。
```

## 注意事项

- 简历中不要把 AI 生成项目包装成完全独立开发。
- 更合适的说法是：AI 辅助开发后，自己进行代码审查、测试补充、模块接管和重构。
- 真正能写进简历的内容，必须满足：
  - 自己能画流程图。
  - 自己能讲核心代码。
  - 自己能回答失败场景。
  - 自己能做一个小改动。
