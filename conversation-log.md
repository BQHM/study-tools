# 对话接续记录

> 作用：记录每次和 Codex 对话的重点、聊天进度、暂停点和下次接续问题，方便学习暂停后在另一台设备或另一个会话继续。
>
> 使用方式：开始学习时先读 `HANDOFF.md` 获取当前大任务，再读本文件接上最近一次聊天进度。
>
> 维护规则：
>
> - 不记录完整聊天全文，只记录会影响后续学习、简历、JD、项目接管的关键信息。
> - 每次准备暂停、换设备、结束一轮学习或形成重要判断时，追加一条简短记录。
> - 事实类信息最终仍要同步到对应主档：个人经历进 `profile.md`，JD 进 `jd-tracking.md`，学习进度进 `study-log.md`，长期交接进 `HANDOFF.md`。
> - 本文件更像“对话索引”，用来快速恢复刚刚聊到哪里；大任务、阶段和长期交接放入 `HANDOFF.md`。

## 记录模板

```text
### YYYY-MM-DD HH:mm｜简短主题

- 对话主题：
- 用户补充：
- 本次判断：
- 已更新：
- 下次接续：
```

## 2026-06-21｜新增对话接续机制

- 对话主题：用户希望新增一个专门记录关键对话的文档，用于当前对话暂停后换设备继续。
- 用户补充：不需要记录太多内容，但可能比较频繁，主要用于学习暂停和跨设备接续。
- 本次判断：新增 `conversation-log.md`，只记录关键对话摘要，不替代 `study-log.md`、`HANDOFF.md`、`profile.md` 和 `jd-tracking.md`。
- 已更新：新增本文件，并准备同步 README、学习日志和 handoff。
- 下次接续：每次阶段性暂停前，优先在本文件追加一条 5 行以内摘要。

## 2026-06-21｜个人经历与 JD 台账沉淀

- 对话主题：整理用户真实工作经历、JD 记录方式和跨设备同步方式。
- 用户补充：本科南京财经大学软件工程，2024 年毕业；2024-04 以实习身份入职长亮科技，2024-07 试用期，2024-11 转正；长亮为存款业务产品研发，做过开户、存入、支取/存取款等交易；参与青海农信 POC、安徽农信 POC、浦发银行新核心驻场约 1 个月、广农商 POC、郑州农商 POC；2026-06 起在宁波银行数币开发组驻场。
- 本次判断：主投递线应优先放在银行 Java / 金融科技 Java，AI Agent 作为成长线；POC 和驻场经历先登记为参与和开发支持，暂不包装成主导交付。
- 已更新：`profile.md`、`jd-tracking.md`、`bank-java-jd-positioning.md`、`README.md`、`study-log.md`、`HANDOFF.md`。
- 下次接续：继续追问各个 POC 的具体职责、浦发新核心参与模块、宁波数币具体业务模块。

## 2026-06-21｜长亮日常工作内容补充

- 对话主题：用复健式提问梳理用户在长亮的日常工作内容。
- 用户补充：主要做存款产品开发和交易后端开发；同时会做参数/配置、SQL 编写或调整；公司提供前端工具，用户会用该工具开发交易相关前端；做过存款产品设计文档，也会进行交易自测。
- 本次判断：用户经历可以表达为“存款产品研发 + 交易后端开发 + 配置/SQL + 前端工具页面/配置 + 设计文档 + 自测”，比单纯“业务开发”更完整。
- 已更新：`profile.md`。
- 下次接续：继续问“你最熟的一类交易是开户、存入还是支取/存取款？”

## 2026-06-21｜存款交易熟悉度边界

- 对话主题：确认开户、存入、支取/存取款中是否有最熟的一类交易。
- 用户补充：都是按需求做，没有明显最熟的一类交易。
- 本次判断：后续简历和面试不硬写“精通某一交易”，更稳妥地表达为“按需求参与多类存款交易开发”，再从具体需求里提炼可讲案例。
- 已更新：`profile.md`。
- 下次接续：继续追问一个具体做过的需求，哪怕只记得大概交易名、改了什么、怎么自测。

## 2026-06-22｜本机项目追问与八股训练补录

- 对话主题：补录公司电脑本机 2026-06-16 到 2026-06-22 的 `interview-assistant` 口述训练和 Java 八股训练。
- 用户补充：已能说出项目两条链路；对内容 hash、文件校验、AI 超时重试降级、Prompt Injection、规则兜底有初步复述；HashMap put 流程曾把 CAS 混入，已纠正。
- 本次判断：需要把“内容 hash 去重不是文件类型检测”“先查是优化、唯一索引是兜底”“AI 输出不可信要校验”“重试不能无限”沉淀到答案库。
- 已更新：`knowledge-answer-bank.md`、`study-log.md`、`HANDOFF.md`。
- 下次接续：继续从 HashMap “为什么容量是 2 的幂”开始，再做一轮 `interview-assistant` 5 题口述。

## 2026-06-22｜明确 handoff 与 conversation 分工

- 对话主题：用户明确跨会话同步流程。
- 用户补充：`HANDOFF.md` 记录当前大任务；`conversation-log.md` 记录每次对话重点。每次学习先看 `HANDOFF.md` 获取大任务，再读 `conversation-log.md` 获取聊天进度。
- 本次判断：这是后续所有 Codex 会话的启动顺序，`study-log.md` 回到学习结果记录，不承担聊天接续入口。
- 已更新：`README.md`、`AGENTS.md`、`HANDOFF.md`、`conversation-log.md`。
- 下次接续：按“先 handoff，后 conversation，再按任务读取计划/教材/答案库”的流程开始。

## 2026-06-22｜明确学习启动协议

- 对话主题：用户补充“准备学习 / 上次学到哪里了”的固定启动方式。
- 用户补充：每次准备学习时，先让 Codex 拉取远程最新代码，再依次读 `HANDOFF.md` 和 `conversation-log.md`；`HANDOFF.md` 定大任务，`conversation-log.md` 定聊天进度，然后直接从最新记录继续。
- 本次判断：后续不能只凭记忆回答“上次学到哪”，必须先同步远程并读取文档；真正的继续点以 `conversation-log.md` 最新记录为准。
- 已更新：`README.md`、`AGENTS.md`、`HANDOFF.md`、`study-log.md`、`conversation-log.md`。
- 下次接续：继续当前暂停题：`HashMap 为什么容量是 2 的幂？`

## 2026-06-22｜暂停学习，先完善 profile 主档

- 对话主题：用户决定暂时把学习放一边，优先完善 `profile.md`。
- 用户补充：当前重点不是继续 HashMap 或项目口述，而是把个人画像主档整理清楚。
- 本次判断：`profile.md` 只登记用户自身实际情况、表达边界和待补充事实；不混入项目资产盘点、JD 专项策略或八股答案。
- 已更新：`profile.md`，重整为一句话画像、基本信息、工作时间线、长亮经历、宁波银行经历、能力状态、表达边界、待补充事实采集清单和下一轮访谈问题。
- 下次接续：从 `profile.md` 第 10 节的 5 个画像访谈问题开始，优先补长亮 V8.7 基板、具体交易需求、浦发驻场模块、宁波数币模块和真实问题排查案例。

## 2026-06-22｜profile 访谈规则纠偏

- 对话主题：用户纠正 `profile.md` 的补充方式。
- 用户补充：`profile.md` 是真实情况登记表，用于后续写简历；不能由 Codex 自行补充，必须通过慢慢访谈、用户回答、事实确认后再写入。
- 本次判断：后续补 `profile.md` 要先问细节、整理“已确认事实 / 待确认事实 / 不能写太满”，用户确认后再更新；不追问无意义的工具类细节，重点记录做过哪些业务和参与程度。
- 已更新：`AGENTS.md` 已加入 profile 补充访谈协议；本轮未继续修改 `profile.md`。
- 下次接续：如继续补 profile，先从“真实业务清单”问起；如继续学习，则接今天的 HashMap 训练。

## 2026-06-22｜HashMap 小白版复健训练

- 对话主题：按学习启动协议恢复学习，从 `HashMap 为什么容量是 2 的幂` 开始。
- 用户补充：希望把自己当小白讲，少用术语；已能答出 HashMap 通过 key 快速定位、哈希冲突、容量 2 的幂与 `(n - 1) & hash` 有关、超过阈值扩容、线程不安全和非原子操作有关。
- 本次判断：用户已掌握 HashMap 的主线直觉，但还需要继续巩固 put 完整流程、链表转红黑树、equals/hashCode、扩容和线程不安全的面试表达。
- 已更新：准备同步 `study-log.md` 和 `HANDOFF.md`。
- 下次接续：继续 HashMap 第二轮 5 题：冲突解决、链表转红黑树、为什么转红黑树、key 为什么重写 `equals/hashCode`、equals 相等但 hashCode 不同会怎样。

## 2026-06-24｜JD 台账提交与今日学习切入

- 对话主题：用户要求先提交推送 JD 台账，再开始今天学习。
- 用户补充：聊天记录也要随时记得登记，不能等很久才补。
- 本次判断：关键对话、JD 分析、学习切换点和暂停点都应及时写入 `conversation-log.md`；今天从集合速通转入更贴银行 Java 主线的 Spring 事务。
- 已更新：`jd-tracking.md` 已本地提交为 `f59a555 docs: add ai tooling jd notes`，但 `git push` 因 GitHub 凭据错误 `SEC_E_NO_CREDENTIALS` 未推送成功；本条记录补入 `conversation-log.md`。
- 下次接续：继续 Spring 事务三问：事务解决什么问题、为什么同类内部调用可能失效、异常被 catch 不抛会怎样。

## 2026-06-30｜Spring 事务三问复述

- 对话主题：继续 Spring 事务学习检查。
- 用户补充：事务解决“一起完成或一起回滚”；同类内部调用会跳过代理，导致事务没有启用；异常被 catch 不抛时，用户初答为“事务不生效”。
- 本次判断：前两题主线正确；第三题需要纠正为“事务本身可能已经开启，但异常被吞掉后 Spring 感知不到失败，可能不会回滚而是提交”。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续讲 Spring 事务回滚规则：`RuntimeException`、检查异常、`rollbackFor`，再练银行交易场景表达。

## 2026-06-30｜Spring 默认回滚规则

- 对话主题：检查 `@Transactional` 默认回滚规则。
- 用户补充：开户交易中外部接口失败抛普通 `Exception`，普通 `@Transactional` 不一定回滚，因为普通 `Exception` 默认不一定触发回滚。
- 本次判断：用户已理解 Spring 默认主要对 `RuntimeException` / `Error` 回滚；下一步要补 `rollbackFor = Exception.class` 的表达和银行交易一致性场景。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：练习回答“银行交易里为什么常配置 `rollbackFor = Exception.class`，以及异常被 catch 后如何处理”。

## 2026-06-30｜支取交易异常吞掉场景

- 对话主题：用支取交易场景练习 Spring 事务和异常处理。
- 用户补充：如果扣减账户余额成功、插入交易流水失败，但代码 catch 异常只打印日志不抛，可能导致余额扣款成功、流水失败、交易还正常结束；应该改成 catch 后报错并抛出异常。
- 本次判断：用户已抓住银行交易一致性风险；需要补充面试表达：异常要继续抛出或转换为运行时异常，必要时配置 `rollbackFor = Exception.class`，避免 Spring 提交事务。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续讲 Spring 事务传播行为中最常见的 `REQUIRED`，再联系开户/支取交易边界。

## 2026-06-30｜Spring 学习入口调整

- 对话主题：用户指出 Spring 整体仍模糊，不应直接专攻事务。
- 用户补充：以前学习过 Servlet 和三层架构。
- 本次判断：后续讲 Spring 应从用户已有的 Servlet / 三层架构认知出发，先建立 Spring MVC、Controller-Service-Mapper、IoC、AOP 的整体地图，再回到事务。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：用 Servlet 三层架构对照 Spring MVC / Spring Boot，讲清 Spring 到底替开发者省掉了什么。

## 2026-06-30｜Spring 短期面试学习策略

- 对话主题：用户询问 Spring 高频知识点、如何在时间少的情况下快速应对面试，以及哪些工作中用得多。
- 用户补充：时间比较少，希望不要大而全学习。
- 本次判断：Spring 后续按“面试高频 + 工作常用 + 能关联银行交易”排序，优先学 Spring MVC 请求流程、IoC/DI、AOP/事务、Bean 生命周期、事务失效、常用注解和异常处理；暂不深挖冷门源码。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：按 3 天速通路线推进 Spring：Day 1 整体地图和请求流程，Day 2 IoC/Bean/AOP/事务，Day 3 事务失效和项目话术。

## 2026-06-30｜Tomcat 与 Spring Boot 启动疑问

- 对话主题：用户询问 Spring 整体地图、MVC 请求流程，以及为什么以前 Servlet 学习要用 Tomcat 启动，现在项目好像不用单独配置 Tomcat。
- 用户补充：以前学习时记得要用 Tomcat 启动。
- 本次判断：需要讲清 Servlet 容器、外部 Tomcat、Spring MVC 的 `DispatcherServlet`、Spring Boot 内嵌 Tomcat 和自动配置之间的关系。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续用“外部 Tomcat 部署 war”对比“Spring Boot 内嵌 Tomcat 跑 jar”，再画一次请求从 Tomcat 到 Controller 的流程。

## 2026-07-02｜DispatcherServlet 职责复述

- 对话主题：检查用户对 `DispatcherServlet` 的理解。
- 用户补充：`DispatcherServlet` 用来接收来自前端的 request。
- 本次判断：方向正确，但需要补充完整：请求先到 Tomcat，再交给 `DispatcherServlet`；`DispatcherServlet` 不只接收请求，还负责分发请求、找 Controller、参数绑定、调用处理链并组织返回。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续 Spring MVC 请求流程：Tomcat -> DispatcherServlet -> HandlerMapping -> Controller -> Service -> Mapper -> DB -> JSON。

## 2026-07-02｜Spring MVC 与 Spring Boot 关系

- 对话主题：检查用户对 Spring / Spring MVC / Spring Boot 三者关系的理解。
- 用户补充：Spring MVC 是 Spring 里面做 Web 的部分；Spring Boot 暂时不知道。
- 本次判断：用户已抓住 Spring MVC 的核心定位；下一步要用“小白版”讲清 Spring Boot 是简化 Spring 项目启动和配置的工具，包含内嵌 Tomcat、自动配置和 starter 依赖。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：让用户复述“Spring 是底座，Spring MVC 管 Web 请求，Spring Boot 负责快速启动和自动配置”。

## 2026-07-02｜Spring Boot 与 Spring MVC 复述通过

- 对话主题：检查用户复述 Spring Boot 和 Spring MVC 的区别。
- 用户补充：Spring Boot 是快速启动 Spring 项目的工具，减少配置、内嵌 Tomcat；Spring MVC 是 Spring 里的 Web 模块，负责接收请求并找到 Controller。
- 本次判断：该表达已经可用于面试初答；后续需要补上 Spring 是底座，以及 Spring Boot 不是替代 Spring MVC，而是把 Spring MVC 等能力更方便地启动起来。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续学习 Controller 常用注解：`@Controller`、`@RestController`、`@RequestMapping`、`@GetMapping`、`@PostMapping`。

## 2026-07-02｜Controller 注解复健

- 对话主题：学习 `@Controller` 和 `@RestController` 的区别。
- 用户补充：`@RestController` 是 `@Controller` + `@Response` 的结合。
- 本次判断：理解方向正确，但注解名需要纠正为 `@ResponseBody`；核心区别是 `@RestController` 默认把方法返回值写入响应体，常用于返回 JSON。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续区分页面跳转场景用 `@Controller`，前后端分离接口返回 JSON 场景用 `@RestController`。

## 2026-07-02｜Mapping 注解待复健

- 对话主题：检查用户对 `@RequestMapping`、`@GetMapping`、`@PostMapping` 的理解。
- 用户补充：暂时不知道这几个注解的作用。
- 本次判断：需要用小白版讲清“URL 和 Controller 方法的绑定关系”，再区分 GET 查询、POST 新增/提交。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：让用户用自己的话解释 `GET /users/1` 和 `POST /users` 分别适合什么场景。

## 2026-07-02｜GET 与 POST 场景判断通过

- 对话主题：检查用户对 GET / POST 使用场景的直觉。
- 用户补充：`GET /account/detail` 是查账户信息，`POST /account/open` 是开户提交。
- 本次判断：用户已建立 GET 偏查询、POST 偏提交/新增的基本判断；后续可继续补 `@RequestParam`、`@PathVariable`、`@RequestBody` 三类参数接收方式。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：学习 Controller 如何接收前端传来的参数。

## 2026-07-02｜Controller 参数注解初步判断

- 对话主题：学习 `@RequestParam`、`@PathVariable`、`@RequestBody` 的使用场景。
- 用户补充：能判断 `/account/detail?accountNo=123` 这种问号后的参数应使用 `@RequestParam`；追问哪种注解用得最多。
- 本次判断：需要按实际开发场景解释：前后端分离业务接口中 `@RequestBody` 很常见；简单查询和少量条件常用 `@RequestParam`；REST 风格资源路径常用 `@PathVariable`。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续用银行开户、账户查询、交易详情三个例子区分三类参数注解。

## 2026-07-02｜RequestBody 场景判断通过

- 对话主题：检查用户对 `@RequestBody` 使用场景的理解。
- 用户补充：能判断 `POST /account/open` 且请求体为姓名、证件号、手机号等 JSON 字段时，应使用 `@RequestBody`。
- 本次判断：用户已能区分简单查询参数和 JSON 请求体；下一步补 `@PathVariable` 的资源路径场景，并形成三类参数注解的口述答案。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：用 `GET /transactions/{tranId}` 检查 `@PathVariable`。

## 2026-07-02｜PathVariable 场景判断通过

- 对话主题：检查用户对 `@PathVariable` 使用场景的理解。
- 用户补充：能判断 `GET /transactions/202507020001` 这种路径中的交易 ID 应使用 `@PathVariable`。
- 本次判断：用户已能区分三类 Controller 参数注解：问号后少量参数用 `@RequestParam`，路径片段用 `@PathVariable`，JSON 请求体用 `@RequestBody`。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：整理 Controller 注解口述答案后，进入 `@Service`、`@Component`、Bean 和 IoC。

## 2026-07-02｜Service 与 Component 初步理解

- 对话主题：学习 Spring 中对象如何交给容器管理。
- 用户补充：`@Service` 表示 Service 层 / 业务层；暂时不知道 `@Component`。
- 本次判断：用户已理解 `@Service` 的分层语义；下一步需要讲清 `@Component` 是通用组件注解，`@Service` 本质上也是一种被 Spring 管理的 Bean，只是语义更明确。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续讲 Bean、IoC，以及为什么加了注解后不用自己到处 `new` 对象。

## 2026-07-02｜Bean 管理与代理概念纠偏

- 对话主题：检查用户对 Spring 中“不用自己 new 对象”的理解。
- 用户补充：不需要自己 `new`，Bean 交由 Spring 代理。
- 本次判断：方向接近，但需要纠正表达：普通 Bean 是交给 Spring 容器创建和管理，不一定都是代理；涉及 AOP、事务等增强时，Spring 才可能创建代理对象。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续讲 IoC / DI：对象创建交给 Spring，依赖对象由 Spring 自动注入。

## 2026-07-02｜IoC DI AOP 概念混淆

- 对话主题：用户反馈 IoC、DI、AOP 容易记混。
- 用户补充：IoC、DI、AOP 三个概念老是混在一起。
- 本次判断：需要用最简单的边界区分：IoC 是对象创建权交给 Spring，DI 是 Spring 把依赖对象塞进来，AOP 是给方法统一加日志、事务、权限等通用逻辑。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：用三个场景题检查区分：不用 new Service、Service 需要 Mapper、方法前后加事务/日志。

## 2026-07-02｜IoC DI AOP 复述通过

- 对话主题：检查用户对 IoC、DI、AOP 英文全称和含义的复述。
- 用户补充：IoC 是控制反转，由 Spring 控制和管理对象；DI 是依赖注入，需要什么依赖由 Spring 帮忙注入；AOP 是面向切面编程，把事务、日志等通用逻辑抽出来统一加。
- 本次判断：用户已能区分三者核心含义；表达上注意 AOP 是“面向切面编程”，DI 用“注入依赖”比“加依赖”更准确。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续用场景题巩固 IoC / DI / AOP，然后回到 Spring 事务为什么依赖 AOP。

## 2026-07-02｜Spring 事务与 AOP 关系待理解

- 对话主题：追问为什么 Spring 事务底层和 AOP 有关系。
- 用户补充：暂时不知道。
- 本次判断：需要从“事务是方法前后统一加的逻辑”讲起：方法执行前开启事务，方法成功后提交，方法异常后回滚；这正符合 AOP 在目标方法前后做增强的思想。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：用开户交易解释 `@Transactional` 背后是代理对象在方法前后做事务控制。

## 2026-07-07｜求职方向偏好变化

- 对话主题：用户表达当前工作状态和下一份工作的偏好。
- 用户补充：不想继续做外包；当前工作枯燥、成长慢、每天加班；希望去自研类岗位，能学到东西，并且加班有加班费。
- 本次判断：这是后续简历定位、JD 筛选和面试准备的重要约束；应优先关注自研团队、产品研发、金融科技自研、银行科技子公司或有明确加班补偿制度的岗位。
- 已更新：本条记录补入 `conversation-log.md`；暂不直接写入 `profile.md`，需要后续访谈确认表达边界。
- 下次接续：确认下一份工作的硬性条件和可接受妥协项，例如是否接受驻场、是否接受外包性质、城市、薪资、加班强度、成长方向。

## 2026-07-07｜下份工作硬性条件

- 对话主题：确认用户对下一份工作的硬性条件。
- 用户补充：如果下份工作仍然加班，最重要的前提是有加班费。
- 本次判断：后续筛选 JD 和面试反问时，需要重点确认加班制度、加班费或调休规则，避免进入无偿高强度加班环境。
- 已更新：本条记录补入 `conversation-log.md`；暂不直接写入 `profile.md`，待后续统一确认求职偏好后再更新。
- 下次接续：继续确认是否完全排斥外包/驻场，以及自研岗位的目标城市、薪资底线和成长方向。

## 2026-07-07｜当前换岗动因补充

- 对话主题：用户进一步说明想离开当前工作的现实原因。
- 用户补充：已工作约两年，但薪资长期没有上涨；当前加班没有加班费，收入回报与工作强度不匹配。
- 本次判断：用户换岗动因不只是追求技术成长，也包括薪资增长和劳动回报不匹配；后续求职策略应同时关注岗位性质、自研程度、薪资涨幅和加班补偿机制。
- 已更新：本条记录补入 `conversation-log.md`；为保护隐私，未记录具体到手金额。
- 下次接续：确认目标薪资区间、最低可接受底线、是否接受阶段性加班以及哪些岗位坚决不投。

## 2026-07-09｜事务异常吞掉复述通过

- 对话主题：检查用户对 `@Transactional` 异常回滚条件的理解。
- 用户补充：异常要抛出来才能回滚，不能直接 catch 后不抛。
- 本次判断：用户已抓住核心：异常被吞掉后，事务代理可能认为方法正常结束并提交；面试表达需要补充“抛到事务代理外面”和“默认回滚规则”。
- 已更新：本条记录补入 `conversation-log.md`。
- 下次接续：继续讲普通 `Exception` 默认不一定回滚，以及为什么银行交易常用 `rollbackFor = Exception.class`。

## 2026-07-16｜离职求职冲刺阶段切换

- 对话主题：用户说明当前公司补贴下降，准备从宁波出差状态直接离职，并在月底前后回无锡找工作。
- 用户补充：当前是 7 月中旬，计划提离职；这段时间需要抓紧补充知识面和相关项目，目标是尽快具备投递和面试能力。
- 本次判断：后续学习节奏应切换为“求职冲刺模式”，优先补简历项目表达、银行 Java 高频知识、Spring/MyBatis/MySQL/Redis/MQ、离职原因话术和 JD 筛选，不再按 6-8 周慢计划推进。
- 已更新：本条记录补入 `conversation-log.md`；准备同步 `HANDOFF.md` 的当前阶段。
- 下次接续：制定 2026-07-16 到月底的两周冲刺安排，并先从简历主线、项目话术和高频八股清单开始。

## 2026-07-16｜宁波驻场时间线确认

- 对话主题：补充宁波驻场的准确起始时间。
- 用户补充：从 2026-06-01 来宁波到现在一直在宁波驻场。
- 本次判断：后续简历和面试口径应将宁波经历表述为“2026-06-01 起参与宁波银行数币相关驻场工作”，但具体模块、职责和产出仍需继续访谈确认，暂不写太满。
- 已更新：本条记录补入 `conversation-log.md`，并同步 `HANDOFF.md` 中的驻场时间线。
- 下次接续：继续确认宁波数币驻场具体做的模块、接口/交易范围、联调对象和可讲问题排查案例。

## 2026-07-16｜interview-assistant 当前完成度补充

- 对话主题：用户补充 `interview-assistant` 项目的当前状态。
- 用户补充：`interview-assistant` 目前大体完成了后端 + 前端，其中有不少 AI 辅助开发内容，但现在已经有一个大体上的 MVC 流程。
- 本次判断：后续不能再只按“后端 MVP/待接管”理解该项目；更稳妥的定位是“AI 辅助完成的前后端项目，用户需要梳理并掌握 MVC 主链路、核心模块和自己能讲清/能修改的部分”。写入简历前必须先读取 GitHub 最新代码和本地项目核验。
- 已更新：本条记录补入 `conversation-log.md`；准备同步 `HANDOFF.md` 的项目状态提示。
- 下次接续：读取 `interview-assistant` 最新代码，梳理前端页面 -> Controller -> Service -> Mapper/Repository -> DB/AI 的 MVC 主流程，并确认哪些部分用户能独立讲清。

## 2026-07-16｜新增 Java + AI Agent 离线题库

- 对话主题：用户要求整理近年高频 Java 和 AI Agent 面试题，包含题目、答案、优先级、星级和来源标签，方便后续无法使用 AI 时离线学习。
- 用户补充：需要尽量全面，覆盖 Java 与 AI Agent 等方向，按优先级整理，并标注类似“哪家公司面试问过”的来源信息。
- 本次判断：新增独立题库文件比塞进 `knowledge-answer-bank.md` 更合适；公司标签采用公开面经常见归纳，答案用官方文档和主流工程资料校准，避免把未经核实的公司题库当官方事实。
- 已更新：新增 `java-ai-agent-interview-question-bank-2026.md`，并同步 `HANDOFF.md`。
- 下次接续：从题库 P0 题开始做口述训练，优先顺序为 Spring/事务 -> MySQL -> Redis/幂等 -> Java 集合/线程池 -> AI Agent/RAG。

## 2026-07-16｜题目和答案拆分

- 对话主题：用户希望题目和答案分离，方便自检。
- 用户补充：不希望打开题库时题目和答案混在一起，后续可能无法使用 AI，需要靠文件自测。
- 本次判断：将原题库改成入口文件，新增题目册和答案册；题目册只保留 ID、星级、题目、公司/来源标签和自检要求，答案册保留完整答案和追问。
- 已更新：`java-ai-agent-interview-question-bank-2026.md`、`java-ai-agent-interview-questions-2026.md`、`java-ai-agent-interview-answers-2026.md`，并同步 `HANDOFF.md`。
- 下次接续：使用题目册从 ★★★★★ 开始口述训练，答完再按 ID 打开答案册核对。

## 2026-07-19｜interview-assistant 每日回顾机制

- 对话主题：用户希望每天由 Codex 带着回顾 `interview-assistant`，避免长期项目和早期模块遗忘。
- 用户补充：`interview-assistant` 项目周期比较长，虽然现在大体有 MVC 流程，但早期项目内容容易忘。
- 本次判断：后续学习和求职冲刺前应先进行 5-10 分钟项目唤醒，重点回顾项目定位、MVC 主链路、一个早期模块、失败场景和 AI 辅助边界。
- 已更新：新增 `interview-assistant-daily-review.md`，并同步 `AGENTS.md`、`HANDOFF.md`、`README.md`、`study-log.md`。
- 下次接续：每天开场先问“你先用一句话说，interview-assistant 是做什么的？”，再按清单抽一个模块复盘。
## 2026-07-28｜interview-assistant 真实技术面试式复盘

- 用户要求项目复盘改为真实技术面试官追问，规则已写入 `AGENTS.md`：基于真实源码，一次一题，逐层追问异常、并发、一致性、边界和取舍。
- 已复盘简历上传：前端 `FormData(file)` -> `ResumeController` -> `ResumeUploadService`；类型/大小校验、hash 去重、Tika 文本解析、对象存储、数据库保存、AI 分析和规则兜底。
- 已重新检查本地 `interview-assistant`：AI 出题、AI 单题评估及规则兜底已实现；会话详情、历史详情、报告均从独立答案表与题目快照聚合，不再是待完成项。
- 远程同步失败：Git 代理 `127.0.0.1:7890` 不可连接，因此本轮结论基于本地源码，GitHub 最新性未确认。
- 用户当前回答进度：能说明 Controller/Service 分层、Tika 作用、原始文件放对象存储、AI 失败不阻塞上传；曾把 hash 与文件类型校验混淆，已纠正。
- 下次接续问题：`ResumeUploadService` 为什么先计算内容 hash 并查重，再执行 Tika 解析、对象存储上传和 AI 分析？如果把查重放到最后，会有什么问题？
