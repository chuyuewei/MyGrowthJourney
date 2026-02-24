```
game
├── ServerScriptService
│   └── OptimizationX
│       ├── Init.server.lua          ← 唯一入口，引导 CoreX
│       ├── CoreX
│       │   ├── Config.lua
│       │   ├── Logger.lua
│       │   ├── EventBus.lua
│       │   └── ModuleLoader.lua
│       ├── DataX
│       │   ├── DataManager.lua       ← 外观门面
│       │   ├── Cache.lua             ← LRU + TTL 缓存
│       │   ├── Queue.lua             ← DS 请求节流队列
│       │   ├── DeltaSaver.lua        ← 增量保存
│       │   ├── SessionLock.lua       ← 防冲突
│       │   ├── Retry.lua             ← 指数退避
│       │   └── SchemaValidator.lua   ← 数据校验 + 迁移
│       ├── NetworkX
│       │   ├── NetworkManager.lua
│       │   ├── RateLimiter.lua       ← Token Bucket
│       │   ├── Batcher.lua           ← 事件批处理
│       │   ├── Compressor.lua        ← 字典压缩
│       │   ├── PriorityQueue.lua
│       │   └── RemoteRegistry.lua    ← Remote 注册中心
│       ├── PerformanceX
│       │   ├── PerformanceManager.lua
│       │   ├── HeartbeatScheduler.lua ← 统一调度
│       │   ├── MemoryWatcher.lua
│       │   ├── InstanceTracker.lua
│       │   ├── WorkSplitter.lua      ← 分帧处理
│       │   ├── CoroutinePool.lua
│       │   └── PhysicsOptimizer.lua
│       ├── ScriptX
│       │   ├── ObjectPool.lua
│       │   ├── ConnectionManager.lua
│       │   ├── Memoize.lua
│       │   ├── Signal.lua            ← 轻量事件
│       │   ├── LazyLoader.lua
│       │   └── Utilities.lua         ← debounce/throttle/deepCopy
│       ├── AssetX
│       │   ├── AssetManager.lua
│       │   ├── PreloadQueue.lua
│       │   ├── MemoryBudget.lua
│       │   ├── DuplicateDetector.lua
│       │   └── AnimationCache.lua
│       └── MonitorX
│           ├── MonitorManager.lua
│           ├── ServerSampler.lua
│           ├── DiagnosticsReport.lua
│           └── AlertRules.lua
│
├── ReplicatedStorage
│   └── OptimizationX_Shared
│       ├── SharedConfig.lua          ← 客户端可读配置
│       ├── SharedTypes.lua           ← 类型定义 / 接口约定
│       ├── RemoteDefinitions.lua     ← Remote 名称 + 签名
│       └── Remotes (Folder)          ← 运行时由 NetworkX 创建
│
├── StarterPlayer
│   └── StarterPlayerScripts
│       └── OptimizationX_Client
│           ├── ClientBoot.client.lua ← 客户端入口
│           ├── RenderX
│           │   ├── RenderManager.lua
│           │   ├── DeviceTier.lua    ← 设备检测 (GPU/内存/平台)
│           │   ├── QualityAdapter.lua← FPS 自适应
│           │   ├── StreamingTuner.lua
│           │   ├── LODController.lua ← Mesh/Texture/Shadow/Particle
│           │   ├── OcclusionAssist.lua
│           │   ├── DrawCallReducer.lua
│           │   ├── TerrainOptimizer.lua
│           │   └── LightOptimizer.lua
│           ├── ClientNetworkX
│           │   ├── OutboundThrottle.lua
│           │   └── EventCoalescer.lua
│           └── ClientMonitorX
│               ├── FPSCounter.lua
│               ├── PingMeasure.lua
│               └── DeviceProfile.lua
│
└── ServerStorage
    └── OptimizationX_Config
        └── ProductionConfig.lua      ← 可热替换的生产配置
```
