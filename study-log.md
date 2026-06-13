# 学习日志

> 每次学习结束后更新。重点写“学会了什么、还不会什么、下一步做什么”，不用写长篇流水账。

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
