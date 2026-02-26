```
Types → Signal → Promise → Result / Option → Mutex / Semaphore → ObjectPool → Buffer → Timer / Clock → Config → DI Container → Lifecycle → ModuleLoader → Bootstrap → Logger / Profiler
```

```
game/
├── ReplicatedStorage/
│   └── FrameworkX/
│       ├── Kernel/
│       │   ├── Bootstrap.luau
│       │   ├── Container.luau           -- DI 容器
│       │   ├── Lifecycle.luau           -- 生命周期管理器
│       │   ├── Config.luau              -- 配置系统
│       │   ├── ModuleLoader.luau        -- 模块加载器
│       │   └── Types.luau               -- 全局类型定义
│       │
│       ├── Primitives/
│       │   ├── Signal.luau
│       │   ├── Promise.luau
│       │   ├── Observable.luau          -- Value/Computed/ObservableList/Map
│       │   ├── Mutex.luau
│       │   ├── RWLock.luau
│       │   ├── Semaphore.luau
│       │   ├── RateLimiter.luau
│       │   ├── ObjectPool.luau
│       │   ├── Result.luau
│       │   ├── Option.luau
│       │   ├── BufferUtils.luau         -- BufferWriter/Reader
│       │   ├── Timer.luau
│       │   ├── Clock.luau
│       │   ├── Throttle.luau
│       │   └── Maid.luau               -- 清理器（自动管理析构）
│       │
│       ├── Core/
│       │   ├── Network/
│       │   │   ├── PacketRegistry.luau
│       │   │   ├── Serializer.luau
│       │   │   ├── Middleware.luau
│       │   │   ├── Batcher.luau
│       │   │   ├── NetServer.luau
│       │   │   ├── NetClient.luau
│       │   │   └── Types.luau
│       │   │
│       │   ├── Data/
│       │   │   ├── DataService.luau
│       │   │   ├── PlayerProfile.luau
│       │   │   ├── Schema.luau
│       │   │   ├── Migration.luau
│       │   │   ├── SessionLock.luau
│       │   │   ├── Cache.luau
│       │   │   ├── Transaction.luau
│       │   │   ├── RetryPolicy.luau
│       │   │   ├── CircuitBreaker.luau
│       │   │   ├── Adapters/
│       │   │   │   ├── DataStoreAdapter.luau
│       │   │   │   ├── OrderedDataStoreAdapter.luau
│       │   │   │   ├── MemoryStoreAdapter.luau
│       │   │   │   └── MockAdapter.luau
│       │   │   └── Types.luau
│       │   │
│       │   ├── State/
│       │   │   ├── Store.luau
│       │   │   ├── Reducer.luau
│       │   │   ├── Selector.luau
│       │   │   ├── Middleware.luau
│       │   │   ├── Replicator.luau
│       │   │   ├── DeltaDiff.luau
│       │   │   └── Types.luau
│       │   │
│       │   ├── ECS/
│       │   │   ├── World.luau
│       │   │   ├── Entity.luau
│       │   │   ├── Component.luau
│       │   │   ├── System.luau
│       │   │   ├── Query.luau
│       │   │   ├── Archetype.luau
│       │   │   ├── CommandBuffer.luau
│       │   │   ├── Observer.luau
│       │   │   └── Types.luau
│       │   │
│       │   ├── Event/
│       │   │   ├── EventBus.luau
│       │   │   ├── EventChannel.luau
│       │   │   └── Types.luau
│       │   │
│       │   ├── Scheduler/
│       │   │   ├── TaskScheduler.luau
│       │   │   ├── TimerWheel.luau
│       │   │   ├── JobQueue.luau
│       │   │   └── Types.luau
│       │   │
│       │   └── Logger/
│       │       ├── Logger.luau
│       │       ├── Profiler.luau
│       │       ├── Metrics.luau
│       │       ├── HealthCheck.luau
│       │       ├── Sinks/
│       │       │   ├── ConsoleSink.luau
│       │       │   ├── MemoryRingSink.luau
│       │       │   └── RemoteSink.luau
│       │       └── Types.luau
│       │
│       ├── Services/
│       │   ├── PlayerService.luau
│       │   ├── SecurityService.luau
│       │   ├── AssetService.luau
│       │   ├── AnalyticsService.luau
│       │   └── LocalizationService.luau
│       │
│       ├── Shared/
│       │   ├── Constants.luau
│       │   ├── Enums.luau
│       │   ├── Errors.luau
│       │   └── Utils.luau
│       │
│       └── init.luau                    -- 框架入口 (FrameworkX)
│
├── ServerScriptService/
│   └── Server/
│       ├── init.server.luau             -- 服务端启动脚本
│       ├── Services/                    -- 游戏业务 Service
│       │   ├── CombatService.luau
│       │   ├── InventoryService.luau
│       │   └── ...
│       └── Systems/                     -- ECS Systems
│           ├── DamageSystem.luau
│           └── ...
│
├── StarterPlayer/
│   └── StarterPlayerScripts/
│       └── Client/
│           ├── init.client.luau         -- 客户端启动脚本
│           ├── Services/
│           │   ├── InputService.luau    -- (覆盖/扩展内置)
│           │   ├── UIService.luau
│           │   └── ...
│           ├── Controllers/             -- UI Controllers
│           │   ├── HUDController.luau
│           │   └── ...
│           └── Systems/                 -- Client ECS Systems
│               ├── RenderSystem.luau
│               └── ...
│
└── ReplicatedStorage/
    └── Shared/                          -- 业务共享代码
        ├── Packets.luau                 -- 网络包定义
        ├── Schemas.luau                 -- 数据 Schema 定义
        ├── Actions.luau                 -- State Actions 定义
        ├── Components.luau              -- ECS Component 定义
        └── Config.luau                  -- 业务配置
```
