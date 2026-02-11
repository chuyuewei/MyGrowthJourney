第一步：发送“系统设定”指令（Project Initialization）
目的：让 Claude 理解整个架构，确立编码风格（高性能、模块化），并记住文件结构。不要让它立刻写代码，而是先“握手”。
复制以下内容发送给 Claude：
```
我需要你作为一个资深的 Roblox Luau 系统架构师，协助我开发一个名为 CommandX 的下一代 Admin 系统。
核心设计目标：
极度模块化 (Modular)：所有组件解耦，通过 Registry 进行交互。
高可用性 (High Availability)：必须包含熔断机制 (Circuit Breaker)、自动重试队列和看门狗 (Watchdog) 保护。
高性能 (High Performance)：最小化内存占用，优化网络带宽（字节级压缩），使用 Luau 的 --!strict 类型检查。
这是项目的文件结构（请以此为蓝本）：
[这里粘贴你上面提供的那个树状结构图]
请注意：
由于代码量巨大，请不要一次性生成所有代码。
首先，请你分析这个架构，确认你理解了 High Availability (HA) 层在这个 Admin 系统中的作用，并告诉我你准备如何处理 Init.server.lua 与 Core 模块的加载顺序。
确认无误后，我会分模块让你编写代码。
```
第二步：核心基础层（Core Infrastructure）
目的：搭建地基。没有这些，其他模块无法运行。
复制发送：
```
很好。现在我们开始第一阶段开发：基础设施层 (Infrastructure Layer)。
请为我编写以下核心文件的代码。请务必使用 --!strict 类型检查，并确保 Registry 可以被其他模块 require。
Shared/Constants.lua：定义所有 Remote 事件名、权限等级常量、颜色配置。
Shared/Types.lua：定义 PlayerData, CommandDefinition, Context 等核心 Type 导出。
Core/Config.lua：系统默认配置表。
Core/Registry.lua：这是一个核心服务定位器（Service Locator），用于存储和获取其他模块（CommandManager, DataStoreManager 等），解决循环依赖问题。
```
第三步：高可用性层（HA Layer - 重点）
目的：这是你架构中最亮眼的部分，需要重点实现。
复制发送：
```
现在进入第二阶段：高可用性层 (HA Layer)。这是 CommandX 与普通 Admin 系统的最大区别。
请编写以下模块，确保它们能保护系统不崩溃：
HA/CircuitBreaker.lua：当某个指令或 DataStore 连续失败超过阈值时，暂时熔断该功能，防止服务器卡死。
HA/RetryQueue.lua：处理失败的 DataStore 请求，使用指数退避算法 (Exponential Backoff) 进行重试。
HA/HealthMonitor.lua：监控 Server Script 的心跳和内存使用率，异常时发出警报。
Core/Logger.lua：集成 HA 层的日志记录器，支持 Info/Warn/Error/Debug 级别。
```
第三步：数据与权限层（Data & Core Logic）
目的：实现核心业务逻辑。
复制发送：
```
第三阶段：核心逻辑与数据层 (Core Logic & Data)。
请实现以下模块：
Core/PermissionManager.lua：处理玩家权限，支持 UserId 和 GroupRank 映射。
Core/Parser.lua：解析聊天信息（例如 :kick player reason），支持参数自动推导。
Core/Dispatcher.lua：接收解析后的指令，检查权限，检查 Cooldown，然后分发给 Executor。
Init.server.lua：这是入口文件。请写出如何遍历文件夹、require 模块、初始化 HA 层、并注册 RemoteEvents 的逻辑。
```
第四步：指令实现（Commands - 举例）
目的：指令文件太多了，建议先让它写一个“模板”或“基类”，然后你再根据需要让它补充。
复制发送：
```
第四阶段：指令系统 (Command System)。
我们不需要一次性写完所有指令。请先为我建立指令的标准模板和加载机制。
请展示 Core/Executor.lua：如何执行具体的指令函数。
请编写 Commands/ModerationCommands.lua 作为示例。我需要里面包含 :kick 和 :ban 指令。
要求：指令必须包含 Name, Alias, Description, Args (类型定义), PermissionLevel。
要求：Kick 指令必须经过 HA/CircuitBreaker 保护（防止恶意刷指令导致 API 限制）。
```
第五步：客户端（Client Side）
目的：UI 和交互。
复制发送：
```
最后阶段：客户端 (Client Side)。
请编写 StarterPlayerScripts/CommandXClient.client.lua。
需求：
监听 CommandXRemotes/Notification 事件，制作一个简单的 UI 通知（使用代码创建 UI，不要 Instance.new 太多，尽量复用）。
监听 CommandXRemotes/CommandOutput，在 F9 控制台或自定义 UI 中显示指令返回结果。
客户端需要对 RemoteEvent 进行防抖动 (Debounce) 处理，防止被垃圾信息刷屏。
```
💡 针对“高可用”和“高性能”的提示技巧
在与 Claude 对话过程中，如果它生成的代码看起来比较普通，你可以用以下话术进行修正：
关于性能： “Claude，请优化 Parser.lua 的字符串处理。不要使用大量的 string.split，尝试使用 string.gmatch 迭代器来减少内存分配。”
关于HA： “在 Data/BanDataStore.lua 中，请务必使用 pcall 包裹所有 GetAsync/SetAsync 请求，并将失败的请求发送给 HA/RetryQueue 处理，而不是直接报错。”
关于模块化： “请确保 ModerationCommands 不直接依赖 PermissionManager，而是通过 context 或 Registry 获取，保持指令模块的纯净。”
```
game
│
├── ServerScriptService/
│   └── CommandX/
│       │
│       ├── Init.server.lua                            ✅ Script
│       │
│       ├── Core/
|       |   ├── AdminConfig.lua                        📦 ModuleScript
│       │   ├── Config.lua                             📦 ModuleScript
│       │   ├── Registry.lua                           📦 ModuleScript
│       │   ├── Parser.lua                             📦 ModuleScript
│       │   ├── Executor.lua                           📦 ModuleScript
│       │   ├── Dispatcher.lua                         📦 ModuleScript
│       │   ├── PermissionManager.lua                  📦 ModuleScript
│       │   ├── CooldownManager.lua                    📦 ModuleScript
│       │   ├── Output.lua                             📦 ModuleScript
│       │   ├── Logger.lua                             📦 ModuleScript
│       │   ├── HelpRequestManager.lua                 📦 ModuleScript
│       │   ├── MuteManager.lua                        📦 ModuleScript
│       │   ├── ServerLockManager.lua                  📦 ModuleScript
│       │   └── UndoManager.lua                        📦 ModuleScript
│       │
│       ├── HA/
│       │   ├── CircuitBreaker.lua                     📦 ModuleScript
│       │   ├── HealthMonitor.lua                      📦 ModuleScript
│       │   ├── RetryQueue.lua                         📦 ModuleScript
│       │   └── Watchdog.lua                           📦 ModuleScript
│       │
│       ├── Data/
│       │   ├── BanDataStore.lua                       📦 ModuleScript
│       │   ├── PermissionDataStore.lua                📦 ModuleScript
│       │   ├── WarningDataStore.lua                   📦 ModuleScript
│       │   ├── WaypointDataStore.lua                  📦 ModuleScript
│       │   └── PlayerNoteDataStore.lua                📦 ModuleScript
│       │
│       ├── Commands/
│       │   ├── HelpRequestCommands.lua                📦 ModuleScript
│       │   ├── PlayerCommands.lua                     📦 ModuleScript
│       │   ├── TeleportCommands.lua                   📦 ModuleScript
│       │   ├── ModerationCommands.lua                 📦 ModuleScript
│       │   ├── CharacterCommands.lua                  📦 ModuleScript
│       │   ├── ServerCommands.lua                     📦 ModuleScript
│       │   ├── EnvironmentCommands.lua                📦 ModuleScript
│       │   ├── ItemCommands.lua                       📦 ModuleScript
│       │   ├── FunCommands.lua                        📦 ModuleScript
│       │   ├── TeamCommands.lua                       📦 ModuleScript
│       │   ├── EconomyCommands.lua                    📦 ModuleScript
│       │   ├── BuildCommands.lua                      📦 ModuleScript
│       │   ├── DebugCommands.lua                      📦 ModuleScript
│       │   ├── UtilityCommands.lua                    📦 ModuleScript
│       │   ├── PermissionCommands.lua                 📦 ModuleScript
│       │   └── SystemCommands.lua                     📦 ModuleScript
│       │
│       ├── Shared/
│       │   ├── Types.lua                              📦 ModuleScript
│       │   └── Constants.lua                          📦 ModuleScript
│       │
│       └── Extensions/
│           ├── PluginLoader.lua                       📦 ModuleScript
│           └── Hooks.lua                              📦 ModuleScript
│
├── StarterPlayer/
│   └── StarterPlayerScripts/
│       └── CommandXClient.client.lua                  🖥️ LocalScript
│
└── ReplicatedStorage/
└── CommandXRemotes/                               📁 Folder (自动创建)
├── CommandOutput                              RemoteEvent
└── Notification                               RemoteEvent
```
