``` text
game (DataModel)
│
│ ══════════════════════════════════════════════════════════════════
│  🌍 WORKSPACE — 设施 3D 世界 (六大扇区 + 全新阵营出生点)
│ ══════════════════════════════════════════════════════════════════
│
├── Workspace/
│   │
│   ├── _Runtime/                                    # 运行时动态物体
│   │   ├── ActiveAnomalies/                         # 当前活跃异常实体 (原SCP)
│   │   ├── SpawnedNPCs/                             
│   │   ├── DroppedItems/                            
│   │   ├── Projectiles/                             
│   │   ├── BreachEffects/                           
│   │   ├── Corpses/                                 
│   │   └── TempDebris/                              
│   │
│   ├── Facility/                                    # ====== 设施主体结构 ======
│   │   │
│   │   ├── SectorA_ControlAndRiot/                  # 🟢 扇区 A: 管控与暴动区 (D级 & 安保)
│   │   │   ├── ClassD_Block/                        # D级人员营房
│   │   │   │   ├── CellBlock_Main                   # 大型上下铺集中区(防卡顿)
│   │   │   │   ├── ClassD_Yard                      # 放风庭院/篮球场
│   │   │   │   ├── ClassD_Showers                   # 淋浴间(经典暴动点)
│   │   │   │   └── ContrabandStashes/               # 违禁品藏匿点(暗格)
│   │   │   │
│   │   │   ├── SecurityHQ/                          # 安保部指挥所
│   │   │   │   ├── GuardSpawnArea                   # 安保出生点
│   │   │   │   ├── Armory_Light                     # 轻型武器库(手枪/电击枪)
│   │   │   │   ├── SectorA_CCTV                     # A区专属监控台
│   │   │   │   └── InterrogationRooms/              # 审讯室(双面镜设计)
│   │   │   │
│   │   │   ├── EscortCorridors/                     # 押送走廊(超宽设计)
│   │   │   │   ├── Checkpoint_A_to_E                # 通往测试区(E区)的重兵把守大门
│   │   │   │   └── Checkpoint_A_to_D                # 通往中央枢纽(D区)的通道
│   │   │   │
│   │   │   └── HiddenVents/                         # 通风管道暗道(D级越狱用)
│   │   │
│   │   ├── SectorB_RescueAndResearch/               # 🟣 扇区 B: 救援与研究区 (科研 & 医疗)
│   │   │   ├── MedicalBay/                          # 核心医疗部
│   │   │   │   ├── Med_SpawnArea                    # 医生出生点
│   │   │   │   ├── EmergencyTriage                  # 紧急分诊大厅(大空间容纳伤员)
│   │   │   │   ├── VirusQuarantineWards/            # 病毒隔离病房(玻璃墙)
│   │   │   │   └── SurgeryRooms/                    # 手术室
│   │   │   │
│   │   │   ├── ResearchLabs/                        # 科研部
│   │   │   │   ├── Sci_SpawnArea                    # 科学家出生点
│   │   │   │   ├── Lab_Biology                      # 生物/病毒化验室
│   │   │   │   ├── Lab_Chemistry                    # 化学合成室
│   │   │   │   ├── DataArchive                      # 资料档案库
│   │   │   │   └── Storage/                # 安全级物品保管库(如万能药)
│   │   │   │
│   │   │   └── Corridors/                           # 走廊
│   │   │       └── Checkpoint_B_to_D                # 必须经过消毒程序的通道
│   │   │
│   │   ├── SectorC_TacticalResponse/                # 🔵 扇区 C: 重装镇压区 (武装力量/MTF)
│   │   │   ├── TacticalHQ/                          # 战术大本营(易守难攻)
│   │   │   │   ├── Armed_SpawnArea                  # 武装人员出生点
│   │   │   │   ├── Armory_Heavy                     # 重武器库(步枪/护甲/重火力)
│   │   │   │   ├── BriefingRoom                     # 战术简报室(带全息地图)
│   │   │   │   └── FiringRange                      # 室内射击训练场
│   │   │   │
│   │   │   └── RapidDeployment/                     # 快速响应通道
│   │   │       ├── Catwalk_Overwatch                # 俯瞰A区和E区的高空步道
│   │   │       ├── Elevator_To_SectorA              # 直达A区镇压暴动的电梯
│   │   │       └── Elevator_To_SectorE              # 直达E区处理收容失效的电梯
│   │   │
│   │   ├── SectorD_FacilityHeart/                   # 🟢 扇区 D: 设施心脏与枢纽 (文职/后勤)
│   │   │   ├── CentralAtrium                        # 🏛️ 中央十字大厅 (百人服缓冲极宽阔区域)
│   │   │   ├── CivilianOffices/                     # 文职出生与办公区
│   │   │   │   ├── Civ_SpawnArea                    # 文职人员出生点
│   │   │   │   ├── AdminOffices                     # 行政办公室
│   │   │   │   └── MainCafeteria                    # 主餐厅(全图最大中立RP聚集点)
│   │   │   │
│   │   │   ├── LogisticsAndPower/                   # 后勤与动力区
│   │   │   │   ├── ReactorCore/                     # 主反应堆/发电机房(可被破坏导致停电)
│   │   │   │   ├── WaterTreatment                   # 水循环处理室
│   │   │   │   ├── MaintenanceTunnels               # 维修通道(文职工程师专属路线)
│   │   │   │   └── JanitorClosets                   # 全图分布的清洁工具间
│   │   │   │
│   │   │   └── SiteCommand/                         # 高管区域
│   │   │       ├── SiteDirectorOffice               # 站点主管办公室
│   │   │       └── PA_SystemRoom                    # 全图广播控制室
│   │   │
│   │   ├── SectorE_HazardAndTesting/                # 🔴 扇区 E: 危险源与实验场 (病毒/SCP测试)
│   │   │   ├── TestingChambers/                     # 测试区域
│   │   │   │   ├── TestChamber_01/                  # 双层结构测试室
│   │   │   │   │   ├── ObservationDeck              # 上层防弹观察室(科研/安保站立)
│   │   │   │   │   └── ContainmentCell              # 下层收容隔间(D级人员进入)
│   │   │   │   ├── TestChamber_02/
│   │   │   │   └── GasChamber                       # 毒气测试室
│   │   │   │
│   │   │   ├── ContainmentZone/                     # 收容/感染区 (极度危险)
│   │   │   │   ├── VirusGroundZero                  # 病毒泄露源头(感染者/怪物出生点)
│   │   │   │   ├── SCP_Chambers/                    # 危险SCP收容室
│   │   │   │   │   ├── Chamber_KeterClass
│   │   │   │   │   └── Chamber_EuclidClass
│   │   │   │   └── DarkCorridors                    # 闪烁红光、长满生物组织的黑暗走廊
│   │   │   │
│   │   │   └── WarheadSilo/                         # 净化核弹井 (终极销毁手段)
│   │   │       ├── WarheadDevice
│   │   │       └── ActivationPanel
│   │   │
│   │   │── SectorF_SurfaceExtraction/               # 🟠 扇区 F: 通往地表 (终极逃生区)
│   │   │   ├── BlastDoors/                          # 防爆大门
│   │   │   │   ├── Gate_A_Structure
│   │   │   │   └── Gate_B_Structure
│   │   │   ├── HeavyElevators/                      # 货运级超大电梯
│   │   │   │   └── Elevator_Surface
│   │   │   ├── SurfaceOutpost/                      # 地面哨所
│   │   │   │   ├── Helipad                          # 逃生直升机停机坪
│   │   │   │   ├── EvacTents                        # 临时撤离帐篷
│   │   │   │   └── SniperTowers                     # 狙击塔
│   │   │   └── PerimeterForest                  # 周边禁区森林
│   │   └── Doors/                                   
│   │       ├── StandardDoors/
│   │       ├── KeycardDoors/
│   │       ├── BlastDoors/
│   │       ├── AirlockDoors/                        # 扇区交界处的双重气闸门
│   │       └── ContainmentDoors/
│   │
│   ├── FacilityInfrastructure/                      # ====== 设施基础设施 (逻辑组件库) ======
│   │   │                                            # (保留了你极其优秀的原设计，仅重命名配合扇区)
│   │   │
│   │   ├── Cameras/                                 
│   │   │   ├── Cameras_SectorA
│   │   │   ├── Cameras_SectorB
│   │   │   ├── Cameras_SectorC
│   │   │   ├── Cameras_SectorD
│   │   │   ├── Cameras_SectorE
│   │   │   └── Cameras_SectorF
│   │   │
│   │   ├── Speakers/                                # 广播喇叭
│   │   ├── EmergencyLights/                         # 紧急照明(红光/停电时亮起)
│   │   ├── Terminals/                               # 电脑终端
│   │   ├── InteractableProps/                       # 掩体/储物箱/电脑椅等(分担性能)
│   │   └── Signs/                                   # 墙面标识牌(极大帮助玩家在六大扇区寻路)
│   │
│   ├── Zones/                                       # ====== 区域触发器 (不可见Part) ======
│   │   ├── ZoneTrigger_SectorA_Control
│   │   ├── ZoneTrigger_SectorB_Medical
│   │   ├── ZoneTrigger_SectorC_Tactical
│   │   ├── ZoneTrigger_SectorD_Hub
│   │   ├── ZoneTrigger_SectorE_Hazard
│   │   ├── ZoneTrigger_SectorF_Surface
│   │   ├── SafeZones/                               # 绝对安全区(如出生点无敌判定)
│   │   └── RestrictedZones/                         # 限制区域(越权进入触发警报)
│   │
│   ├── SpawnLocations/                              # ====== 扇区化出生点 ======
│   │   │
│   │   ├── SectorA_Spawns/                          # 🟢 扇区 A: 管控与暴动区
│   │   │   ├── Spawn_ExposureSubject                # 暴露对象 (ES)
│   │   │   ├── Spawn_SecurityDept                   # 安保部 (SD)
│   │   │   └── Spawn_ProtocolEnforcers              # 协议执行者 (PE)
│   │   │
│   │   ├── SectorB_Spawns/                          # 🟣 扇区 B: 救援与研究区
│   │   │   ├── Spawn_ScientificDivision             # 科学部 (ScD)
│   │   │   ├── Spawn_VirologyResearch               # 病毒研究部 (VRD)
│   │   │   ├── Spawn_MedicalDivision                # 医疗部门 (MedDiv)
│   │   │   └── Spawn_PsychologicalDept              # 心理学部 (PsyD)
│   │   │
│   │   ├── SectorC_Spawns/                          # 🔵 扇区 C: 重装镇压区
│   │   │   ├── Spawn_CBRN_IS                        # CBRN内部安全 (CBRN-IS)
│   │   │   ├── Spawn_RapidContainmentForce          # 快速收容部队 (RCF)
│   │   │   ├── Spawn_PurgeTaskForce                 # "净化"特遣队 (PTF)
│   │   │   └── Spawn_ScorchedEarth                  # "焦土"响应单位 (SERU)
│   │   │
│   │   ├── SectorD_Spawns/                          # 🟢 扇区 D: 设施心脏与枢纽
│   │   │   ├── Spawn_SiteAdministration             # 设施管理层 (SA)
│   │   │   ├── Spawn_EthicsCommittee                # 伦理委员会 (EC)
│   │   │   ├── Spawn_InternalAffairs                # 内务调查部 (IA)
│   │   │   ├── Spawn_InternalSecurityDept           # 内部安全部 (ISD)
│   │   │   ├── Spawn_ExternalAffairs                # 对外事务部 (DEA)
│   │   │   ├── Spawn_LogisticsArmory                # 后勤与军械部 (LAD)
│   │   │   └── Spawn_DeconEngineering               # 净化与工程部 (D&E)
│   │   │
│   │   ├── SectorE_Spawns/                          # 🔴 扇区 E: 危险源与实验场
│   │   │   ├── Spawn_ContainmentSurveillance        # 收容监控部 (CSD)
│   │   │   ├── Spawn_Anomaly                        # 异常实体 (Anomaly)
│   │   │   └── Spawn_Infected                       # 感染体 (Communion等)
│   │   │
│   │   ├── SectorF_Spawns/                          # 🟠 扇区 F: 通往地表
│   │   │   ├── Spawn_SurfaceDefenseCorps            # 地表防卫军 (SDC)
│   │   │   └── Spawn_HostileFaction                 # 敌对阵营入侵出生点 (Sigma/RogueCell/BlackTide)
│   │   │
│   │   └── Spawn_Spectator                          # 旁观者出生点
│   │
│   └── Interactables/                               # 通用可交互物体
│       ├── KeycardReaders/                          
│       ├── Buttons/                                 
│       ├── Pickups/                                 
│       └── Workstations/                            
│
│
│ ══════════════════════════════════════════════════════════════════
│  🖥️ SERVER SCRIPT SERVICE — 服务端脚本 (部门重构版)
│ ══════════════════════════════════════════════════════════════════
│
├── ServerScriptService/
│   │
│   ├── Core/                                        
│   │   ├── ServerBootstrap.server.lua               
│   │   ├── PlayerJoinHandler.server.lua             
│   │   └── ServerHeartbeat.server.lua               
│   │
│   ├── Services/                                    
│   │   │
│   │   │ ── 📦 数据 & 基础 & 设施 ──
│   │   ├── DataService.lua                          
│   │   ├── ClearanceService.lua                     # 0-5级/Omni权限系统
│   │   ├── DoorService.lua                          
│   │   ├── PowerService.lua                         
│   │   ├── LockdownService.lua                      # 封锁系统 (IRON GATE等协议)
│   │   ├── WarheadService.lua                       # Alpha弹头系统
│   │   │
│   │   │ ── 👥 团队 & 部门核心 ──
│   │   ├── TeamService.lua                          # 团队/阵营管理核心
│   │   ├── RankService.lua                          # 职位等级管理
│   │   ├── DepartmentService.lua                    # 部门系统核心
│   │   │
│   │   ├── Departments/                             # ====== 各部门专属逻辑 ======
│   │   │   │
│   │   │   │ ── 📋 指挥与监督 (Command & Oversight) ──
│   │   │   ├── SiteAdministrationService.lua        # 设施状态码 · Alpha弹头授权 · 跨部门覆权
│   │   │   ├── EthicsCommitteeService.lua           # 实验否决权 · 伦理冻结 · GLASS CEILING协议
│   │   │   ├── InternalAffairsService.lua           # 内鬼调查 · 反间谍 · 审讯
│   │   │   ├── InternalSecurityDeptService.lua      # 武装逮捕 · 拘留执行 (IA的武装分支)
│   │   │   ├── ExternalAffairsService.lua           # 掩护故事 · 外部通信管制
│   │   │   │
│   │   │   │ ── 🔬 研究与医疗 (Research & Medical) ──
│   │   │   ├── ScientificDivisionService.lua        # 异常理论 · 收容设计
│   │   │   ├── VirologyResearchService.lua          # 病原体研究 · BSL-4实验室 · Bio-Risk分级
│   │   │   ├── MedicalDivisionService.lua           # 创伤救治 · 隔离护理
│   │   │   ├── PsychologicalDeptService.lua         # CFC认证 · 心理冻结 · Weight Protocol
│   │   │   │
│   │   │   │ ── 🛡️ 安全与武装 (Security & Armed Forces) ──
│   │   │   ├── SecurityDeptService.lua              # 常规巡逻 · 门禁管理 · 暴露对象押送
│   │   │   ├── CBRNInternalSecurityService.lua      # 生化核威胁响应 · 隔离区安全覆权
│   │   │   ├── ProtocolEnforcersService.lua         # 合规执法 · 违规处理
│   │   │   ├── ContainmentSurveillanceService.lua   # 实时监控 · 收容状态核实
│   │   │   ├── RapidContainmentForceService.lua     # 失效首批响应 · 重新收容
│   │   │   ├── PurgeTaskForceService.lua            # 区域清除行动
│   │   │   ├── ScorchedEarthService.lua             # 毁灭协议 · 终极方案
│   │   │   ├── SurfaceDefenseCorpsService.lua       # 地表防御 · 防空 · 撤离通道
│   │   │   │
│   │   │   │ ── 🔧 后勤与支援 (Decontamination & Support) ──
│   │   │   ├── DeconEngineeringService.lua          # 设施维修 · 消毒 · 结构完整性
│   │   │   ├── LogisticsArmoryService.lua           # 物资分配 · 武器发放
│   │   │   └── CommunicationsDivisionService.lua    # 广播系统 · 频道管控
│   │   │
│   │   │ ── 🧑‍🤝‍🧑 角色系统 ──
│   │   ├── CharacterService.lua                     
│   │   ├── ExposureSubjectService.lua               # 暴露对象管理 (原ClassD)
│   │   ├── ExposureSubjectEscapeService.lua         
│   │   ├── ExposureSubjectTerminationService.lua    
│   │   │
│   │   │ ── 👾 异常实体 (Anomaly) ──
│   │   ├── AnomalyService.lua                       # 核心管理 (原SCPService)
│   │   ├── AnomalyContainmentService.lua            
│   │   ├── AnomalyBreachService.lua                 
│   │   ├── AnomalyBehaviors/                        # 具体异常行为库
│   │   │
│   │   │ ── 🕵️ 敌对阵营 (Hostile Factions) ──
│   │   ├── HostileFactionService.lua                # 核心阵营管理
│   │   ├── SigmaService.lua                         # 准军事袭击逻辑
│   │   ├── CommunionService.lua                     # 感染/邪教仪式逻辑
│   │   ├── RogueCellService.lua                     # 泄密/渗透逻辑
│   │   └── BlackTideService.lua                     # 走私/破坏逻辑
│   │   │
│   │   │ ── 🔫 战斗 & 装备 ──
│   │   ├── CombatService.lua                        
│   │   ├── WeaponService.lua                        
│   │   ├── EquipmentService.lua                     
│   │   │
│   │   │ ── 📻 通信系统 ──
│   │   ├── RadioService.lua                         
│   │   ├── RadioChannels/                           # 电台频道定义
│   │   │   ├── CommandChannel.lua                   # 指挥 (SA / EC / Admin Liaison)
│   │   │   ├── OversightChannel.lua                 # 监督 (EC / IA / ISD)
│   │   │   ├── SecurityChannel.lua                  # 安保 (SD / PE)
│   │   │   ├── TacticalChannel.lua                  # 战术 (RCF / PTF / SERU)
│   │   │   ├── CBRNChannel.lua                      # 化生放核 (CBRN-IS)
│   │   │   ├── SurfaceDefenseChannel.lua            # 地表防卫 (SDC)
│   │   │   ├── ContainmentChannel.lua               # 收容 (CSD / RCF)
│   │   │   ├── ResearchChannel.lua                  # 研究 (ScD / VRD)
│   │   │   ├── MedicalChannel.lua                   # 医疗 (MedDiv / PsyD)
│   │   │   ├── LogisticsChannel.lua                 # 后勤 (LAD / D&E)
│   │   │   ├── CommunicationsChannel.lua            # 通讯 (ComDiv)
│   │   │   ├── InternalAffairsChannel.lua           # IA加密专用
│   │   │   ├── ExternalAffairsChannel.lua           # DEA加密专用
│   │   │   ├── EmergencyChannel.lua                 # 紧急全员
│   │   │   ├── SigmaChannel.lua                     
│   │   │   ├── CommunionChannel.lua                 
│   │   │   └── BlackTideChannel.lua                 
│   │   │
│   │   └── (...其余组件/配置...)
│
│
│ ══════════════════════════════════════════════════════════════════
│  📡 REPLICATED STORAGE — 共享资源 (枚举与数据重构)
│ ══════════════════════════════════════════════════════════════════
│
├── ReplicatedStorage/
│   │
│   ├── Shared/
│   │   │
│   │   ├── Enums/                                   # 枚举值
│   │   │   ├── FactionEnum.lua                      # Facility / Hostile / Anomalous / System
│   │   │   ├── DepartmentCategoryEnum.lua           # CommandAndOversight / ResearchAndMedical...
│   │   │   ├── ClearanceEnum.lua                    # Level 0-5, Omni
│   │   │   ├── TeamEnum.lua                         # 27个子团队枚举(SiteAdministration, Sigma等)
│   │   │   ├── ThreatClassEnum.lua                  # Stable / Volatile / Critical / Terminal
│   │   │   ├── BioRiskTierEnum.lua                  # Tier I / II / III / IV / X
│   │   │   ├── ZoneEnum.lua                         # SectorA_Control... 到 SectorF_Surface
│   │   │   ├── AlertLevelEnum.lua                   # Green / Yellow / Orange / Red / RedBio / Black
│   │   │   ├── FacilityStateEnum.lua                # Normal / IronGate / CleanHouse / DeadAir...
│   │   │   ├── AnomalyStateEnum.lua                 # Contained / Breached / Recontained / Terminated
│   │   │   └── RadioChannelEnum.lua                 
│   │   │
│   │   └── Formulas/
│   │
│   ├── Network/                                     # 网络通信层
│   │   └── Remotes/
│   │       ├── Events/
│   │       │   ├── Team/                            # 加入/晋升/调岗/CFC认证
│   │       │   ├── ExposureSubject/                 # ES逃跑/处决/测试/移交
│   │       │   ├── Command/                         # 指挥层特权(声明警报/授权净化/签署逮捕令/否决实验)
│   │       │   ├── HostileFaction/                  # Sigma袭击/Communion感染/BlackTide走私
│   │       │   ├── Anomaly/                         # 异常能力交互/重新收容
│   │       │   └── Functions/                       # 获取数据(GetAnomalyStatus, GetChainOfCommand等)
│   │       └── (...其余如Combat, Equipment, CCTV不变...)
│   │
│   ├── Data/                                        # ====== 数据定义 ======
│   │   │
│   │   ├── Teams/                                   # 团队数据
│   │   │   ├── TeamDefinitions.lua                  # 团队颜色/简称/所属阵营
│   │   │   ├── TeamSpawns.lua                       # 映射到 Workspace/..._Spawns
│   │   │   ├── TeamLoadouts.lua                     # 27个团队的精细初始装备
│   │   │   └── TeamPermissions.lua                  # 极度硬核的扇区访问控制矩阵
│   │   │
│   │   ├── Ranks/                                   # 职位等级数据
│   │   │   ├── SiteAdminRanks.lua
│   │   │   ├── EthicsCommitteeRanks.lua
│   │   │   ├── InternalAffairsRanks.lua
│   │   │   ├── InternalSecurityDeptRanks.lua
│   │   │   ├── ExternalAffairsRanks.lua
│   │   │   ├── ScientificDivisionRanks.lua
│   │   │   ├── VirologyResearchRanks.lua
│   │   │   ├── MedicalDivisionRanks.lua
│   │   │   ├── PsychologicalDeptRanks.lua
│   │   │   ├── SecurityDeptRanks.lua
│   │   │   ├── CBRNRanks.lua
│   │   │   ├── ProtocolEnforcerRanks.lua
│   │   │   ├── ContainmentSurveillanceRanks.lua
│   │   │   ├── RCFRanks.lua
│   │   │   ├── PTFRanks.lua
│   │   │   ├── SERURanks.lua
│   │   │   ├── SurfaceDefenseRanks.lua
│   │   │   ├── DeconEngineeringRanks.lua
│   │   │   ├── LogisticsArmoryRanks.lua
│   │   │   └── CommunicationsDivisionRanks.lua
│   │   │
│   │   └── Anomalies/                               # 异常实体数据 (替代SCPs)
│   │       └── _AnomalyRegistry.lua
│   │
│   └── Assets/                                      # 共享资产
│       ├── Uniforms/                                # ====== 全新制服体系 ======
│       │   ├── Uniform_SA_SiteDirector
│       │   ├── Uniform_SA_AdminLiaison
│       │   ├── Uniform_EC
│       │   ├── Uniform_IA
│       │   ├── Uniform_ISD
│       │   ├── Uniform_ScD
│       │   ├── Uniform_VRD_BSL4
│       │   ├── Uniform_PsyD_CRP
│       │   ├── Uniform_RCF_Heavy
│       │   ├── Uniform_SERU
│       │   ├── Uniform_ExposureSubject
│       │   ├── Uniform_Sigma
│       │   └── Uniform_Communion
│       │
│       ├── Decals/                                  # 贴图
│       │   ├── Facility_Logo                        
│       │   ├── TheAdministration_Seal               
│       │   └── Department_Logos/                    # 21+个部门专属Logo
│       │       ├── Logo_SA, Logo_EC, Logo_IA...
│       │       └── Logo_Sigma, Logo_Communion...
│       │
│       └── (Models, Effects, Sounds 保持原架构)
│
│
│ ══════════════════════════════════════════════════════════════════
│  🏷️ TEAMS & CHAT
│ ══════════════════════════════════════════════════════════════════
│
├── Teams/                                           # Roblox 团队实例
│   │
│   │ ── ═══ FACILITY FACTION ═══ ──
│   │ ── Command & Oversight
│   ├── SiteAdministration                           
│   ├── EthicsCommittee                              
│   ├── InternalAffairs                              
│   ├── InternalSecurityDept                         
│   ├── ExternalAffairs                              
│   │ ── Research & Medical
│   ├── ScientificDivision                           
│   ├── VirologyResearch                             
│   ├── MedicalDivision                              
│   ├── PsychologicalDept                            
│   │ ── Security & Armed Forces
│   ├── SecurityDept                                 
│   ├── CBRN_InternalSecurity                        
│   ├── ProtocolEnforcers                            
│   ├── ContainmentSurveillance                      
│   ├── RapidContainmentForce                        
│   ├── PurgeTaskForce                               
│   ├── ScorchedEarth                                
│   ├── SurfaceDefenseCorps                          
│   │ ── Decontamination & Support
│   ├── DeconEngineering                             
│   ├── LogisticsArmory                              
│   ├── CommunicationsDivision                       
│   │ ── Other
│   ├── ExposureSubject                              
│   │
│   │ ── ═══ HOSTILE FACTIONS ═══ ──
│   ├── Sigma                                        
│   ├── Communion                                    
│   ├── RogueCell                                    
│   ├── BlackTide                                    
│   │
│   │ ── ═══ ANOMALOUS & SYSTEM ═══ ──
│   ├── Anomaly                                      
│   └── Spectator                                    
│
├── Chat/
│   └── ChatModules/
│       ├── RPNameTag.lua                            # e.g., [SA] Site Director ████
│       ├── ProximityChat.lua                        
│       ├── RadioChatIntegration.lua                 
│       ├── TeamChat.lua                             
│       ├── FactionChat.lua                          # 阵营频道 (Facility / Hostile)
│       ├── SecureChannel.lua                        # 高级加密 (IA/DEA/SA)
│       └── CustomCommands.lua                       
│
│
│ ══════════════════════════════════════════════════════════════════
│  🧑 STARTER PLAYER — 客户端脚本
│ ══════════════════════════════════════════════════════════════════
│
├── StarterPlayer/
│   ├── StarterPlayerScripts/
│   │   ├── Controllers/
│   │   │   ├── TeamSelectController.lua             # 团队选择大UI
│   │   │   ├── DepartmentHUDController.lua          # 动态注入各部门专属面板
│   │   │   ├── ChainOfCommandController.lua         # 指挥链预览
│   │   │   ├── OathDisplayController.lua            # 团队誓言视觉效果
│   │   │   ├── (Camera, Weapon, Movement等控制器不变)
│   │   │
│   │   └── Components/
│   │
│   └── StarterCharacterScripts/
│
│
│ ══════════════════════════════════════════════════════════════════
│  🎨 STARTER GUI — 用户界面
│ ══════════════════════════════════════════════════════════════════
│
├── StarterGui/
│   │
│   ├── HUD/                                         # ===== 游戏HUD =====
│   │   ├── InfoPanel/                               
│   │   │   ├── FactionDisplay                       # 阵营
│   │   │   ├── DepartmentDisplay                    # 部门全称
│   │   │   ├── DepartmentAbbr                       # 简称徽章
│   │   │   ├── RankDisplay                          
│   │   │   ├── ClearanceDisplay                     
│   │   │   └── ZoneDisplay                          
│   │   │
│   │   ├── FacilityStatus/                          
│   │   │   ├── AlertLevel                           
│   │   │   ├── AnomalyBreachIndicators              
│   │   │   ├── BioRiskIndicator                     # 生物风险指示器
│   │   │   ├── ActiveProtocol                       # IRON GATE等
│   │   │   ├── PowerStatus                          
│   │   │   ├── WarheadStatus                        
│   │   │   └── LockdownStatus                       
│   │   │
│   │   ├── DepartmentHUD/                           # ===== 部门专属面板 =====
│   │   │   └── DeptSpecificPanel                    # 根据DepartmentHUDController注入
│   │   │
│   │   └── (WeaponHUD, Health, Radio等保持不变)
│   │
│   ├── Menus/                                       # ===== 菜单 =====
│   │   ├── MainMenu/                                
│   │   │   ├── TeamSelection/                       # ===== 重构版阵营选单 =====
│   │   │   │   ├── FacilityFaction/                 # 设施类选项卡
│   │   │   │   │   ├── CommandOversight_Header
│   │   │   │   │   │   └── SA_Card, EC_Card...
│   │   │   │   │   ├── ResearchMedical_Header
│   │   │   │   │   │   └── ScD_Card, VRD_Card...
│   │   │   │   │   ├── SecurityArmed_Header
│   │   │   │   │   │   └── SD_Card, PTF_Card...
│   │   │   │   │   └── DeconSupport_Header
│   │   │   │   │       └── DE_Card, ES_Card...
│   │   │   │   ├── HostileFactions/                 # 敌对类选项卡
│   │   │   │   │   └── Sigma_Card, Communion_Card...
│   │   │   │   ├── AnomalySelection/                # 异常类选项卡
│   │   │   │   │
│   │   │   │   ├── TeamInfo/                        # 信息预览区
│   │   │   │   │   ├── TeamName & TeamOath          
│   │   │   │   │   ├── ChainOfCommand               
│   │   │   │   │   ├── SpawnZone & Loadout          
│   │   │   │   │   └── Difficulty & Relationships   
│   │   │   │   └── ConfirmButton
│   │   │   └── SettingsButton
│   │   │
│   │   └── (Inventory, CCTV, Terminal等保持不变)
│   │
│   └── Popups/ & Overlays/                          # (弹窗与屏幕效果保持不变)
│
└── TestService/                                     # 测试模块
    └── Integration/
        ├── FacilityProtocolFlowTest.lua             # 设施协议(IRON GATE等)测试
        ├── ChainOfCommandTest.lua                   # 指挥链覆权测试
        └── BioRiskProgressionTest.lua               # 感染爆发层级测试
    ```
