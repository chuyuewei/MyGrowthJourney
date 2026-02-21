```
ServerScriptService/
└── DAWX/
    │
    ├── Init.server.luau                 ★ 唯一的 Script
    │                                      职责: 部署 + 启动服务端
    │
    ├── Server/                          ── 服务端模块 (不会被部署) ──
    │   │
    │   ├── Core/
    │   │   ├── TimeEngine.luau              时间引擎
    │   │   ├── WeatherEngine.luau           天气状态机
    │   │   ├── Scheduler.luau               自动调度器
    │   │   └── BloodMoonController.luau     血月控制器
    │   │
    │   ├── Network/
    │   │   ├── NetworkBootstrap.luau        创建所有 Remote 实例
    │   │   └── StateReplicator.luau         差量状态广播
    │   │
    │   └── API/
    │       └── DAWX_API.luau            ★ 对外公开接口 (BAE2.0)
    │
    ├── Client/                          ── 运行时部署到客户端 ──
    │   │
    │   ├── ClientBoot.luau              ★ 部署时自动包装为 LocalScript 的入口
    │   │
    │   ├── Core/
    │   │   ├── StateReceiver.luau           接收服务端状态
    │   │   └── TransitionOrchestrator.luau  视觉过渡编排
    │   │
    │   ├── Renderers/
    │   │   ├── LightingRenderer.luau        Lighting 属性
    │   │   ├── AtmosphereRenderer.luau      Atmosphere
    │   │   ├── SkyRenderer.luau             天空盒
    │   │   ├── ParticleRenderer.luau        雨/雪/闪电粒子
    │   │   ├── SoundRenderer.luau           环境音/雷声
    │   │   ├── PostFXRenderer.luau          后处理特效
    │   │   └── MoonRenderer.luau            月相/血月
    │   │
    │   └── Util/
    │       └── ObjectPool.luau              粒子对象池
    │
    └── Shared/                          ── 运行时部署到 ReplicatedStorage ──
        │
        ├── Types.luau                       类型定义
        ├── Constants.luau                   枚举/常量
        ├── TimePhases.luau                  时段边界表
        ├── EventBridge.luau                 Remote 引用获取工具
        │
        └── WeatherDefinitions/
            ├── Sunny.luau
            ├── Cloudy.luau
            ├── Rainy.luau
            ├── HeavyRain.luau
            ├── Thunderstorm.luau
            ├── Snowy.luau
            ├── Haze.luau
            └── BloodMoon.luau
```
