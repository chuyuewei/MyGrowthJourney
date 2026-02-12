```
ServerScriptService/
└── CommandX/
    ├── Init.server.lua              -- 系统入口，启动引导脚本
    │
    ├── Config.lua                   -- 全局配置（前缀、GroupId、速率限制参数）
    │
    ├── Core/
    │   ├── Parser.lua               -- 消息解析器（前缀检测、命令名/参数拆分）
    │   ├── Registry.lua             -- 命令注册表（注册、查找、遍历）
    │   ├── Dispatcher.lua           -- 命令调度器（权限校验 → 节流检查 → pcall 执行）
    │   ├── Permissions.lua          -- 权限系统（UserId/GroupRank → Level 映射与验证）
    │   └── RateLimiter.lua          -- 节流限制器（per-player 令牌桶/滑动窗口）
    │
    ├── Commands/
    │   ├── Moderation.lua           -- 管理类命令（kick、ban、mute、unmute）
    │   ├── Utility.lua              -- 工具类命令（speed、jumppower、respawn、tp）
    │   ├── Server.lua               -- 服务器类命令（shutdown、lock、announce）
    │   └── Fun.lua                  -- 娱乐类命令（explode、fire、sparkles）
    │
    └── Util/
        ├── PlayerResolver.lua       -- 目标玩家解析（me、all、others、模糊匹配）
        └── Logger.lua               -- 轻量日志工具（warn/error 输出，可选 webhook）
```
