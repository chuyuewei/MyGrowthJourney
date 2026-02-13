```
On-Site: Roleplay
│
├── ServerScriptService
│   └── CommandX/                                    -- 🔒 根节点 (Folder)
│       │
│       ├── Bootstrap.server.lua                     -- 唯一入口 (Script) — 引导内核启动
│       │
│       ├── Config/                                  -- ⚙️ 配置层 (Folder)
│       │   ├── Settings.lua                         -- 全局静态配置 (ModuleScript)
│       │   ├── Permissions.lua                      -- 权限声明表 (ModuleScript)
│       │   └── Flags.lua                            -- 功能开关 / Feature Flags (ModuleScript)
│       │
│       ├── Kernel/                                  -- 🧠 内核层 (Folder) — 零业务逻辑
│       │   ├── Lifecycle.lua                        -- 生命周期管理器 (ModuleScript)
│       │   ├── ServiceLocator.lua                   -- IoC 服务定位器 (ModuleScript)
│       │   ├── EventBus.lua                         -- 发布/订阅事件总线 (ModuleScript)
│       │   └── ErrorBoundary.lua                    -- 全局异常边界 (ModuleScript)
│       │
│       ├── Services/                                -- 🔧 服务层 (Folder) — 单例有状态服务
│       │   ├── InputService.lua                     -- 聊天输入监听适配器 (ModuleScript)
│       │   ├── AuthService.lua                      -- 鉴权与权限裁决 (ModuleScript)
│       │   ├── RateLimitService.lua                 -- 令牌桶限流 (ModuleScript)
│       │   ├── SessionService.lua                   -- 玩家会话生命周期 (ModuleScript)
│       │   ├── LogService.lua                       -- 结构化日志 (ModuleScript)
│       │   └── SanctionService.lua                  -- 处罚执行 (ban/mute 持久化) (ModuleScript)
│       │
│       ├── Pipeline/                                -- 🔀 管道层 (Folder) — 命令处理流水线
│       │   ├── Parser.lua                           -- 词法解析器 (ModuleScript)
│       │   ├── Validator.lua                        -- 参数类型校验 (ModuleScript)
│       │   ├── Resolver.lua                         -- 目标玩家解析 (ModuleScript)
│       │   ├── Dispatcher.lua                       -- 命令分发执行器 (ModuleScript)
│       │   └── Middleware/                           -- 中间件链 (Folder)
│       │       ├── AuthMiddleware.lua               -- 权限检查中间件 (ModuleScript)
│       │       ├── RateLimitMiddleware.lua           -- 限流中间件 (ModuleScript)
│       │       ├── CooldownMiddleware.lua            -- 命令冷却中间件 (ModuleScript)
│       │       └── AuditMiddleware.lua              -- 审计日志中间件 (ModuleScript)
│       │
│       ├── Registry/                                -- 📦 注册层 (Folder)
│       │   ├── CommandRegistry.lua                  -- 命令注册表 (ModuleScript)
│       │   ├── AliasRegistry.lua                    -- 别名映射表 (ModuleScript)
│       │   └── PluginRegistry.lua                   -- 插件注册表 (ModuleScript)
│       │
│       ├── Commands/                                -- 📋 内置命令集 (Folder)
│       │   ├── _Loader.lua                          -- 批量自动加载器 (ModuleScript)
│       │   ├── Moderation/                          -- 管理域 (Folder)
│       │   │   ├── Kick.lua                         -- (ModuleScript)
│       │   │   ├── Ban.lua                          -- (ModuleScript)
│       │   │   ├── Mute.lua                         -- (ModuleScript)
│       │   │   └── Warn.lua                         -- (ModuleScript)
│       │   ├── Movement/                            -- 传送域 (Folder)
│       │   │   ├── Teleport.lua                     -- (ModuleScript)
│       │   │   ├── Bring.lua                        -- (ModuleScript)
│       │   │   └── To.lua                           -- (ModuleScript)
│       │   ├── Character/                           -- 角色域 (Folder)
│       │   │   ├── Kill.lua                         -- (ModuleScript)
│       │   │   ├── Heal.lua                         -- (ModuleScript)
│       │   │   ├── Speed.lua                        -- (ModuleScript)
│       │   │   ├── Jump.lua                         -- (ModuleScript)
│       │   │   └── ForceField.lua                   -- (ModuleScript)
│       │   ├── Server/                              -- 服务器域 (Folder)
│       │   │   ├── Shutdown.lua                     -- (ModuleScript)
│       │   │   ├── ServerLock.lua                   -- (ModuleScript)
│       │   │   └── Announce.lua                     -- (ModuleScript)
│       │   └── Utility/                             -- 工具域 (Folder)
│       │       ├── Help.lua                         -- (ModuleScript)
│       │       ├── Commands.lua                     -- (ModuleScript)
│       │       └── Info.lua                         -- (ModuleScript)
│       │
│       ├── Plugins/                                 -- 🔌 插件层 (Folder) — 热扩展区
│       │   ├── _PluginLoader.lua                    -- 插件引导加载器 (ModuleScript)
│       │   ├── _PluginAPI.lua                       -- 沙箱化插件接口 (ModuleScript)
│       │   ├── _PluginTemplate.lua                  -- 插件开发模板 (ModuleScript)
│       │   └── ExamplePlugin/                       -- 示例插件 (Folder)
│       │       ├── Manifest.lua                     -- 插件元数据声明 (ModuleScript)
│       │       └── Init.lua                         -- 插件入口 (ModuleScript)
│       │
│       └── Shared/                                  -- 📐 共享层 (Folder) — 纯函数/零状态
│           ├── Types.lua                            -- 全局类型定义 (ModuleScript)
│           ├── Constants.lua                        -- 枚举与常量 (ModuleScript)
│           ├── StringUtil.lua                       -- 字符串工具 (ModuleScript)
│           ├── TableUtil.lua                        -- 表操作工具 (ModuleScript)
│           └── Guard.lua                            -- 类型守卫/断言 (ModuleScript)
│
└── ReplicatedStorage
    └── CommandX/                                    -- 📡 客户端共享 (Folder)
        ├── Types.lua                                -- 公开类型镜像 (ModuleScript)
        └── Remotes/                                 -- 远程通信 (Folder)
            └── Notify.lua                           -- 通知通道定义 (ModuleScript)
```
