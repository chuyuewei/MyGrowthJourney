``` text
game (DataModel)
│
│
│ ══════════════════════════════════════════════════════════════════
│  🌍 WORKSPACE — 设施 3D 世界
│ ══════════════════════════════════════════════════════════════════
│
├── Workspace/
│   │
│   ├── _Runtime/                                    # 运行时动态物体
│   │   ├── ActiveSCPs/                              # 当前活跃SCP实体
│   │   ├── SpawnedNPCs/                             # 生成的NPC
│   │   ├── DroppedItems/                            # 掉落物品
│   │   ├── Projectiles/                             # 投射物
│   │   ├── BreachEffects/                           # 收容失效特效
│   │   ├── Corpses/                                 # 尸体(临时)
│   │   └── TempDebris/                              # 临时碎片/破坏
│   │
│   ├── Facility/                                    # ====== 设施主体 ======
│   │   │
│   │   ├── Exterior/                                # 设施外部
│   │   │   ├── MainGate/                            # 主大门
│   │   │   │   ├── GateStructure
│   │   │   │   ├── GuardBooth
│   │   │   │   ├── Barriers/
│   │   │   │   ├── SecurityCheckpoint
│   │   │   │   └── GateDoors/                       # 大门(可开关)
│   │   │   ├── Perimeter/                           # 外围
│   │   │   │   ├── Fencing/
│   │   │   │   ├── WatchTowers/
│   │   │   │   │   ├── WatchTower_N
│   │   │   │   │   ├── WatchTower_S
│   │   │   │   │   ├── WatchTower_E
│   │   │   │   │   └── WatchTower_W
│   │   │   │   ├── Searchlights/
│   │   │   │   └── Minefield_Signs
│   │   │   ├── Helipad/                             # 直升机停机坪
│   │   │   ├── ParkingLot/                          # 停车场
│   │   │   │   ├── MTF_Vehicles/
│   │   │   │   └── Staff_Parking/
│   │   │   ├── OutdoorRange/                        # 室外射击训练场
│   │   │   ├── Forest/                              # 周围森林
│   │   │   │   ├── Trees/
│   │   │   │   ├── Paths/
│   │   │   │   └── HiddenBunker                     # 隐藏掩体
│   │   │   └── Roads/                               # 通往设施的道路
│   │   │       ├── MainRoad
│   │   │       └── EmergencyRoute
│   │   │
│   │   ├── EntranceZone/                            # ===== 入口区(EZ) =====
│   │   │   ├── MainLobby/                           # 主大厅
│   │   │   │   ├── ReceptionDesk
│   │   │   │   ├── WaitingArea
│   │   │   │   ├── SecurityScreening                # 安检
│   │   │   │   ├── VisitorBadgeStation
│   │   │   │   └── DirectoryBoard                   # 设施导览板
│   │   │   │
│   │   │   ├── AdministrationWing/                  # 行政区
│   │   │   │   ├── SiteDirectorOffice/              # 设施主管办公室
│   │   │   │   │   ├── Desk
│   │   │   │   │   ├── FileCabinets
│   │   │   │   │   ├── SecureTerminal               # 安全终端
│   │   │   │   │   └── EmergencyPanel               # 紧急控制面板
│   │   │   │   ├── O5CouncilRoom/                   # O5议会室
│   │   │   │   │   ├── ConferenceTable
│   │   │   │   │   ├── HolographicDisplay
│   │   │   │   │   └── SecureVault                  # 高安全保险库
│   │   │   │   ├── EthicsCommitteeRoom/             # 伦理委员会室
│   │   │   │   ├── MeetingRooms/                    # 会议室
│   │   │   │   │   ├── MeetingRoom_A
│   │   │   │   │   ├── MeetingRoom_B
│   │   │   │   │   └── BriefingRoom                 # 任务简报室
│   │   │   │   ├── HROffice/                        # 人事办公室
│   │   │   │   └── RecordsArchive/                  # 档案室
│   │   │   │
│   │   │   ├── SecurityOffice/                      # 安保办公室
│   │   │   │   ├── SecurityDesk
│   │   │   │   ├── WeaponLocker                     # 武器柜
│   │   │   │   ├── CCTVMonitorRoom/                 # 监控室
│   │   │   │   │   ├── MonitorWall                  # 监控墙
│   │   │   │   │   ├── ControlConsole               # 控制台
│   │   │   │   │   └── RecordingEquipment           # 录像设备
│   │   │   │   ├── DetentionCells/                  # 拘留室
│   │   │   │   │   ├── Cell_01
│   │   │   │   │   ├── Cell_02
│   │   │   │   │   └── Cell_03
│   │   │   │   └── InterrogationRoom/               # 审讯室
│   │   │   │
│   │   │   ├── StaffAreas/                          # 员工区域
│   │   │   │   ├── Cafeteria/                       # 食堂
│   │   │   │   │   ├── ServingLine
│   │   │   │   │   ├── SeatingArea
│   │   │   │   │   └── Kitchen
│   │   │   │   ├── StaffLounge/                     # 休息室
│   │   │   │   │   ├── Sofas
│   │   │   │   │   ├── VendingMachines
│   │   │   │   │   ├── TVArea
│   │   │   │   │   └── CoffeeMachine
│   │   │   │   ├── StaffDormitories/                # 员工宿舍
│   │   │   │   │   ├── Dorm_01
│   │   │   │   │   ├── Dorm_02
│   │   │   │   │   ├── Dorm_03
│   │   │   │   │   └── Dorm_04
│   │   │   │   └── Lockers/                         # 更衣柜
│   │   │   │
│   │   │   ├── MedicalBay/                          # 医疗区
│   │   │   │   ├── ReceptionArea
│   │   │   │   ├── ExamRooms/
│   │   │   │   │   ├── ExamRoom_01
│   │   │   │   │   └── ExamRoom_02
│   │   │   │   ├── OperatingRoom/                   # 手术室
│   │   │   │   ├── RecoveryWard/                    # 康复病房
│   │   │   │   │   ├── Bed_01
│   │   │   │   │   ├── Bed_02
│   │   │   │   │   └── Bed_03
│   │   │   │   ├── Pharmacy/                        # 药房
│   │   │   │   ├── PsychologicalEvalRoom/           # 心理评估室
│   │   │   │   ├── Morgue/                          # 太平间
│   │   │   │   └── QuarantineRoom/                  # 隔离室
│   │   │   │
│   │   │   ├── Armory/                              # 军械库
│   │   │   │   ├── WeaponRacks/
│   │   │   │   ├── AmmunitionStorage/
│   │   │   │   ├── EquipmentLockers/
│   │   │   │   ├── GearUpStation/                   # 装备站
│   │   │   │   └── ArmoryDesk                       # 军械管理台
│   │   │   │
│   │   │   ├── Checkpoints/                         # 检查站(EZ→LCZ)
│   │   │   │   ├── Checkpoint_EZ_A/
│   │   │   │   │   ├── ScannerGate                  # 扫描门
│   │   │   │   │   ├── GuardStation
│   │   │   │   │   └── BlastDoor                    # 防爆门
│   │   │   │   └── Checkpoint_EZ_B/
│   │   │   │
│   │   │   ├── Elevators/                           # 电梯
│   │   │   │   ├── Elevator_Main
│   │   │   │   ├── Elevator_Staff
│   │   │   │   └── Elevator_Emergency
│   │   │   │
│   │   │   └── Corridors/                           # 走廊
│   │   │       ├── Hallway_EZ_Main
│   │   │       ├── Hallway_EZ_Admin
│   │   │       └── Hallway_EZ_Medical
│   │   │
│   │   ├── LightContainmentZone/                    # ===== 轻型收容区(LCZ) =====
│   │   │   │
│   │   │   ├── SCPChambers_Safe/                    # Safe级SCP收容室
│   │   │   │   ├── SCP_500_Chamber/                 # SCP-500 万能药
│   │   │   │   │   ├── ContainmentCell
│   │   │   │   │   ├── ObservationWindow
│   │   │   │   │   ├── AccessTerminal
│   │   │   │   │   └── StatusDisplay
│   │   │   │   ├── SCP_999_Chamber/                 # SCP-999 痒痒怪
│   │   │   │   │   ├── PlayRoom
│   │   │   │   │   ├── FeedingStation
│   │   │   │   │   └── ObservationDeck
│   │   │   │   ├── SCP_131_Chamber/                 # SCP-131 眼泪滴
│   │   │   │   ├── SCP_529_Chamber/                 # SCP-529 半猫
│   │   │   │   └── SCP_914_Chamber/                 # SCP-914 万能转换机
│   │   │   │       ├── InputBooth
│   │   │   │       ├── OutputBooth
│   │   │   │       ├── ControlPanel                 # 精细/粗糙/1:1等
│   │   │   │       └── ObservationRoom
│   │   │   │
│   │   │   ├── SCPChambers_Euclid_Light/            # 部分Euclid级
│   │   │   │   ├── SCP_173_Chamber/                 # SCP-173 花生
│   │   │   │   │   ├── ContainmentCell
│   │   │   │   │   │   ├── SteelDoor
│   │   │   │   │   │   └── FloodLights
│   │   │   │   │   ├── CleaningSupplyRoom
│   │   │   │   │   └── ObservationWindow
│   │   │   │   ├── SCP_714_Chamber/                 # SCP-714 翡翠戒指
│   │   │   │   └── SCP_330_Chamber/                 # SCP-330 糖果碗
│   │   │   │
│   │   │   ├── ClassD_Block/                        # D级人员区
│   │   │   │   ├── ClassD_Cells/                    # D级牢房
│   │   │   │   │   ├── Cell_D01
│   │   │   │   │   ├── Cell_D02
│   │   │   │   │   ├── Cell_D03
│   │   │   │   │   ├── Cell_D04
│   │   │   │   │   ├── Cell_D05
│   │   │   │   │   ├── Cell_D06
│   │   │   │   │   ├── Cell_D07
│   │   │   │   │   └── Cell_D08
│   │   │   │   ├── ClassD_Showers/                  # 淋浴间
│   │   │   │   ├── ClassD_Yard/                     # 放风院
│   │   │   │   ├── ClassD_Cafeteria/                # D级食堂
│   │   │   │   └── ClassD_GuardStation              # 看守站
│   │   │   │
│   │   │   ├── TestingRooms/                        # 测试室
│   │   │   │   ├── TestingRoom_A/                   # 标准测试室
│   │   │   │   │   ├── ObservationBooth
│   │   │   │   │   ├── TestingArea
│   │   │   │   │   ├── RecordingEquipment
│   │   │   │   │   └── EmergencyButton
│   │   │   │   ├── TestingRoom_B/                   # 大型测试室
│   │   │   │   ├── TestingRoom_C/                   # 生物测试室
│   │   │   │   └── TestingRoom_Hazardous/           # 危险品测试室
│   │   │   │
│   │   │   ├── ResearchLabs/                        # 研究实验室
│   │   │   │   ├── Lab_Biology/                     # 生物实验室
│   │   │   │   ├── Lab_Chemistry/                   # 化学实验室
│   │   │   │   ├── Lab_Physics/                     # 物理实验室
│   │   │   │   ├── Lab_Anomalous/                   # 异常物品研究室
│   │   │   │   └── Lab_DataAnalysis/                # 数据分析室
│   │   │   │
│   │   │   ├── StorageRooms/                        # 存储室
│   │   │   │   ├── AnomalousItemStorage/            # 异常物品存储
│   │   │   │   ├── SampleStorage/                   # 样本存储
│   │   │   │   ├── EquipmentStorage/                # 设备存储
│   │   │   │   └── JanitorCloset/                   # 清洁工具间
│   │   │   │
│   │   │   ├── Checkpoints/
│   │   │   │   ├── Checkpoint_LCZ_HCZ/              # LCZ→HCZ检查站
│   │   │   │   │   ├── HeavyBlastDoor_A
│   │   │   │   │   ├── HeavyBlastDoor_B
│   │   │   │   │   ├── DecontaminationChamber       # 消毒室
│   │   │   │   │   └── ScannerGate
│   │   │   │   └── Checkpoint_LCZ_ClassD/           # 进入D级区域检查站
│   │   │   │
│   │   │   └── Corridors/
│   │   │       ├── Hallway_LCZ_Main
│   │   │       ├── Hallway_LCZ_Cells
│   │   │       ├── Hallway_LCZ_Labs
│   │   │       ├── TCrossing_LCZ_01
│   │   │       └── Corner_LCZ_01
│   │   │
│   │   ├── HeavyContainmentZone/                    # ===== 重型收容区(HCZ) =====
│   │   │   │
│   │   │   ├── SCPChambers_Euclid/                  # Euclid级SCP收容室
│   │   │   │   ├── SCP_049_Chamber/                 # SCP-049 瘟疫医生
│   │   │   │   │   ├── ContainmentCell
│   │   │   │   │   │   ├── ReinforcedDoor
│   │   │   │   │   │   ├── Desk
│   │   │   │   │   │   └── Bookshelf
│   │   │   │   │   ├── ObservationRoom
│   │   │   │   │   ├── InterviewRoom
│   │   │   │   │   └── BodyStorageRoom              # 049-2 存放室
│   │   │   │   │
│   │   │   │   ├── SCP_096_Chamber/                 # SCP-096 害羞的家伙
│   │   │   │   │   ├── SteelReinforcedCell
│   │   │   │   │   │   ├── NoWindows                # 无窗户
│   │   │   │   │   │   └── AudioSensors
│   │   │   │   │   ├── Camera_NoVisual              # 无视觉摄像头(仅音频)
│   │   │   │   │   └── EmergencyLockdown
│   │   │   │   │
│   │   │   │   ├── SCP_939_Chamber/                 # SCP-939 众多声音
│   │   │   │   │   ├── SoundproofCell
│   │   │   │   │   ├── FeedingChute
│   │   │   │   │   └── PressureSensors
│   │   │   │   │
│   │   │   │   ├── SCP_066_Chamber/                 # SCP-066
│   │   │   │   └── SCP_457_Chamber/                 # SCP-457 燃烧人
│   │   │   │       ├── FireproofCell
│   │   │   │       ├── SprinklerSystem
│   │   │   │       └── TemperatureSensors
│   │   │   │
│   │   │   ├── SCPChambers_Keter/                   # Keter级SCP收容室
│   │   │   │   ├── SCP_682_Chamber/                 # SCP-682 不灭孽蜥
│   │   │   │   │   ├── AcidTank                     # 酸液槽
│   │   │   │   │   ├── ReinforcedContainment
│   │   │   │   │   │   ├── TitaniumWalls
│   │   │   │   │   │   ├── ElectricGrid
│   │   │   │   │   │   └── BackupContainment
│   │   │   │   │   ├── ObservationDeck
│   │   │   │   │   ├── DrainageSystem
│   │   │   │   │   └── EmergencyPurge
│   │   │   │   │
│   │   │   │   ├── SCP_106_Chamber/                 # SCP-106 恐怖老人
│   │   │   │   │   ├── LeadLinedCell
│   │   │   │   │   ├── FemurBreaker/                # 断股装置
│   │   │   │   │   │   ├── ControlPanel
│   │   │   │   │   │   ├── LureCell
│   │   │   │   │   │   └── ActivationButton
│   │   │   │   │   ├── CorrosionSensors
│   │   │   │   │   └── ContainmentGrid
│   │   │   │   │
│   │   │   │   └── SCP_035_Chamber/                 # SCP-035 恶魔面具
│   │   │   │       ├── SealedGlassCase
│   │   │   │       ├── CorrosionDrains
│   │   │   │       └── PsychicShielding
│   │   │   │
│   │   │   ├── ServerRoom/                          # 服务器机房
│   │   │   │   ├── ServerRacks/
│   │   │   │   ├── CoolingSystem
│   │   │   │   ├── MainTerminal                     # 主终端
│   │   │   │   └── BackupGenerator
│   │   │   │
│   │   │   ├── NuclearWarheadSilo/                  # 核弹头发射井
│   │   │   │   ├── WarheadRoom
│   │   │   │   │   ├── WarheadDevice
│   │   │   │   │   ├── ActivationPanel              # 启动面板
│   │   │   │   │   │   ├── KeySlot_A
│   │   │   │   │   │   ├── KeySlot_B
│   │   │   │   │   │   └── DetonateButton
│   │   │   │   │   ├── CountdownDisplay             # 倒计时显示
│   │   │   │   │   └── CancelButton                 # 取消按钮
│   │   │   │   ├── WarheadArmory
│   │   │   │   └── BlastShelter                     # 防爆掩体
│   │   │   │
│   │   │   ├── GeneratorRooms/                      # 发电机房
│   │   │   │   ├── Generator_01
│   │   │   │   ├── Generator_02
│   │   │   │   ├── Generator_03
│   │   │   │   ├── MainPowerSwitch
│   │   │   │   └── BackupPowerSwitch
│   │   │   │
│   │   │   ├── MTF_Quarters/                        # MTF 驻地
│   │   │   │   ├── ReadyRoom/                       # 待命室
│   │   │   │   ├── Barracks/                        # 营房
│   │   │   │   ├── TrainingRoom/                    # 训练室
│   │   │   │   ├── Briefing/                        # 简报室
│   │   │   │   ├── HeavyArmory/                     # 重型军械库
│   │   │   │   └── VehicleBay/                      # 载具库
│   │   │   │
│   │   │   ├── TunnelSystem/                        # 地下隧道系统
│   │   │   │   ├── MainTunnel
│   │   │   │   ├── ServiceTunnel_A
│   │   │   │   ├── ServiceTunnel_B
│   │   │   │   ├── VentilationShafts/               # 通风管道
│   │   │   │   │   ├── Vent_Main
│   │   │   │   │   ├── Vent_LCZ
│   │   │   │   │   └── Vent_HCZ
│   │   │   │   └── EmergencyTunnel                  # 紧急逃生通道
│   │   │   │
│   │   │   ├── Checkpoints/
│   │   │   │   └── Checkpoint_HCZ_Exit/
│   │   │   │       ├── GateA/                       # A门
│   │   │   │       │   ├── BlastDoor_Final
│   │   │   │       │   ├── GuardStation
│   │   │   │       │   └── Elevator_Surface
│   │   │   │       └── GateB/                       # B门
│   │   │   │           ├── BlastDoor_Final
│   │   │   │           ├── GuardStation
│   │   │   │           └── EscapeRoute
│   │   │   │
│   │   │   └── Corridors/
│   │   │       ├── Hallway_HCZ_Main
│   │   │       ├── Hallway_HCZ_SCP
│   │   │       ├── Hallway_HCZ_Warhead
│   │   │       └── Catwalk_HCZ
│   │   │
│   │   └── PocketDimension/                         # SCP-106 口袋维度
│   │       ├── DistortedHallways/
│   │       ├── TrapRooms/
│   │       │   ├── TrapRoom_Pit
│   │       │   ├── TrapRoom_Coffins
│   │       │   └── TrapRoom_Throne
│   │       └── ExitPortal
│   │
│   ├── FacilityInfrastructure/                      # ====== 设施基础设施 ======
│   │   │
│   │   ├── Doors/                                   # 所有门(按类型分组)
│   │   │   ├── StandardDoors/                       # 标准门
│   │   │   ├── KeycardDoors/                        # 钥匙卡门
│   │   │   │   ├── Level1Doors/                     # 1级权限门
│   │   │   │   ├── Level2Doors/                     # 2级权限门
│   │   │   │   ├── Level3Doors/                     # 3级权限门
│   │   │   │   ├── Level4Doors/                     # 4级权限门
│   │   │   │   └── Level5Doors/                     # 5级(O5)权限门
│   │   │   ├── BlastDoors/                          # 防爆门
│   │   │   ├── AirlockDoors/                        # 气闸门
│   │   │   └── ContainmentDoors/                    # 收容门
│   │   │
│   │   ├── Cameras/                                 # 监控摄像头
│   │   │   ├── Camera_EZ_Lobby
│   │   │   ├── Camera_EZ_Admin
│   │   │   ├── Camera_EZ_Medical
│   │   │   ├── Camera_LCZ_Hall_01
│   │   │   ├── Camera_LCZ_ClassD
│   │   │   ├── Camera_LCZ_914
│   │   │   ├── Camera_HCZ_Hall_01
│   │   │   ├── Camera_HCZ_049
│   │   │   ├── Camera_HCZ_682
│   │   │   ├── Camera_HCZ_Warhead
│   │   │   ├── Camera_GateA
│   │   │   ├── Camera_GateB
│   │   │   └── Camera_Exterior_Gate
│   │   │
│   │   ├── Speakers/                                # 广播喇叭
│   │   │   ├── Speaker_EZ_01
│   │   │   ├── Speaker_LCZ_01
│   │   │   ├── Speaker_HCZ_01
│   │   │   └── Speaker_Exterior
│   │   │
│   │   ├── EmergencyLights/                         # 紧急照明
│   │   │   ├── RedLights_EZ/
│   │   │   ├── RedLights_LCZ/
│   │   │   └── RedLights_HCZ/
│   │   │
│   │   ├── Terminals/                               # 电脑终端
│   │   │   ├── Terminal_Reception
│   │   │   ├── Terminal_Security
│   │   │   ├── Terminal_Research_01
│   │   │   ├── Terminal_Research_02
│   │   │   ├── Terminal_Medical
│   │   │   ├── Terminal_SiteDirector
│   │   │   └── Terminal_ServerRoom
│   │   │
│   │   ├── SCP914/                                  # SCP-914 交互结构
│   │   │   ├── Machine
│   │   │   ├── InputChute
│   │   │   ├── OutputChute
│   │   │   └── SettingKnob                          # Rough/Coarse/1:1/Fine/VeryFine
│   │   │
│   │   └── Signs/                                   # 标识牌
│   │       ├── ZoneSigns/                           # 区域标识
│   │       ├── DirectionSigns/                      # 方向指引
│   │       ├── WarningSigns/                        # 警告标识
│   │       ├── SCPContainmentSigns/                 # SCP编号标牌
│   │       └── ClearanceSigns/                      # 权限等级标识
│   │
│   ├── Zones/                                       # 区域触发器(不可见Part)
│   │   ├── ZoneTrigger_EntranceZone
│   │   ├── ZoneTrigger_LightContainment
│   │   ├── ZoneTrigger_HeavyContainment
│   │   ├── ZoneTrigger_Surface
│   │   ├── ZoneTrigger_PocketDimension
│   │   ├── ZoneTrigger_ClassD_Block
│   │   ├── ZoneTrigger_MedicalBay
│   │   ├── ZoneTrigger_WarheadSilo
│   │   ├── SafeZones/                               # 安全区域
│   │   └── RestrictedZones/                         # 限制区域(越权警报)
│   │
│   ├── SpawnLocations/                              # 出生点
│   │   ├── Spawn_ClassD                             # D级人员出生
│   │   ├── Spawn_Security                           # 安保出生
│   │   ├── Spawn_Research                           # 研究员出生
│   │   ├── Spawn_Medical                            # 医疗出生
│   │   ├── Spawn_MTF                                # MTF出生
│   │   ├── Spawn_CI                                 # 混沌分裂者出生(地面)
│   │   ├── Spawn_SiteDirector                       # 设施主管出生
│   │   └── Spawn_Spectator                          # 旁观者
│   │
│   └── Interactables/                               # 通用可交互物体
│       ├── KeycardReaders/                          # 钥匙卡读取器
│       ├── Buttons/                                 # 按钮
│       │   ├── DoorButtons/
│       │   ├── ElevatorButtons/
│       │   ├── LockdownButtons/
│       │   └── IntercomButtons/
│       ├── MedicalSupplies/                         # 医疗物资
│       │   ├── FirstAidKit
│       │   ├── MedKit
│       │   └── SCP500Pill
│       ├── Workstations/                            # 工作台
│       │   ├── ResearchDesk
│       │   ├── MedicalStation
│       │   └── RepairStation
│       └── Misc/
│           ├── WaterFountain
│           ├── VendingMachine
│           └── Payphone
│
│
│ ══════════════════════════════════════════════════════════════════
│  🖥️ SERVER SCRIPT SERVICE — 服务端脚本
│ ══════════════════════════════════════════════════════════════════
│
├── ServerScriptService/
│   │
│   ├── Core/                                        # 核心启动
│   │   ├── ServerBootstrap.server.lua               # 🔥 服务端主入口
│   │   ├── PlayerJoinHandler.server.lua             # 玩家加入/离开处理
│   │   └── ServerHeartbeat.server.lua               # 服务端主循环
│   │
│   ├── Services/                                    # ====== 全部服务 ======
│   │   │
│   │   │ ── 📦 数据 & 基础 ──
│   │   ├── DataService.lua                          # 玩家数据存储/加载/自动保存
│   │   ├── SessionService.lua                       # 会话锁防数据冲突
│   │   ├── BackupService.lua                        # 数据备份/回档
│   │   ├── LogService.lua                           # 操作日志(审计追踪)
│   │   ├── AnalyticsService.lua                     # 数据统计分析
│   │   │
│   │   │ ── 🔐 权限 & 安全 ──
│   │   ├── ClearanceService.lua                     # 安全等级权限系统(0-5/O5)
│   │   ├── KeycardService.lua                       # 钥匙卡管理(发放/升级/收回)
│   │   ├── AuthorizationService.lua                 # 操作授权验证
│   │   ├── AntiCheatService.lua                     # 反作弊
│   │   ├── AntiExploitService.lua                   # 反外挂
│   │   │
│   │   │ ── 🏢 设施系统 ──
│   │   ├── DoorService.lua                          # 门控系统(开/关/锁/权限)
│   │   ├── ElevatorService.lua                      # 电梯系统
│   │   ├── PowerService.lua                         # 电力系统(发电机/停电)
│   │   ├── LightingSystemService.lua                # 设施灯光系统(正常/紧急/停电)
│   │   ├── CCTVService.lua                          # 监控摄像系统
│   │   ├── IntercomService.lua                      # 广播/对讲系统
│   │   ├── LockdownService.lua                      # 封锁系统(区域/全站封锁)
│   │   ├── WarheadService.lua                       # 核弹头系统
│   │   ├── DecontaminationService.lua               # LCZ消毒协议
│   │   ├── VentilationService.lua                   # 通风系统(毒气/氧气)
│   │   ├── FacilityAlarmService.lua                 # 警报系统
│   │   ├── TerminalService.lua                      # 电脑终端交互
│   │   ├── GeneratorService.lua                     # 发电机交互
│   │   │
│   │   │ ── 👾 SCP 系统 ──
│   │   ├── SCPService.lua                           # SCP实体核心管理
│   │   ├── SCPContainmentService.lua                # 收容状态管理
│   │   ├── SCPBreachService.lua                     # 收容失效(Breach)管理
│   │   ├── SCPBehaviors/                            # 各SCP专属行为逻辑
│   │   │   ├── SCP049Behavior.lua                   # 瘟疫医生行为
│   │   │   ├── SCP096Behavior.lua                   # 害羞的家伙行为
│   │   │   ├── SCP106Behavior.lua                   # 恐怖老人行为
│   │   │   ├── SCP173Behavior.lua                   # 花生行为
│   │   │   ├── SCP682Behavior.lua                   # 不灭孽蜥行为
│   │   │   ├── SCP939Behavior.lua                   # 众多声音行为
│   │   │   ├── SCP457Behavior.lua                   # 燃烧人行为
│   │   │   ├── SCP035Behavior.lua                   # 恶魔面具行为
│   │   │   ├── SCP999Behavior.lua                   # 痒痒怪行为(友善)
│   │   │   ├── SCP914Behavior.lua                   # 万能转换机逻辑
│   │   │   ├── SCP500Behavior.lua                   # 万能药逻辑
│   │   │   └── SCP131Behavior.lua                   # 眼泪滴行为
│   │   ├── SCPSpawnService.lua                      # SCP生成/分配(玩家扮演)
│   │   ├── PocketDimensionService.lua               # 106口袋维度逻辑
│   │   │
│   │   │ ── 🧪 研究 & 测试 ──
│   │   ├── ResearchService.lua                      # 研究系统
│   │   ├── TestingService.lua                       # SCP测试流程
│   │   ├── ExperimentLogService.lua                 # 实验日志记录
│   │   ├── SCP914ProcessService.lua                 # SCP-914 物品转换逻辑
│   │   ├── DocumentService.lua                      # SCP文档/报告系统
│   │   │
│   │   │ ── 👥 团队 & 部门 ──
│   │   ├── TeamService.lua                          # 团队/部门管理
│   │   ├── RankService.lua                          # 职位等级管理
│   │   ├── DepartmentService.lua                    # 部门系统
│   │   ├── Departments/                             # 各部门专属逻辑
│   │   │   ├── SecurityDeptService.lua              # 安保部
│   │   │   ├── ResearchDeptService.lua              # 研究部
│   │   │   ├── MedicalDeptService.lua               # 医疗部
│   │   │   ├── MTFDeptService.lua                   # 机动特遣队
│   │   │   ├── EngineeringDeptService.lua           # 工程部
│   │   │   ├── InternalAffairsService.lua           # 内部事务部
│   │   │   ├── EthicsCommitteeService.lua           # 伦理委员会
│   │   │   └── O5CouncilService.lua                 # O5议会
│   │   │
│   │   │ ── 🧑‍🤝‍🧑 角色 ──
│   │   ├── CharacterService.lua                     # 角色外观/制服/模型
│   │   ├── ClassDService.lua                        # D级人员管理
│   │   ├── ClassDEscapeService.lua                  # D级逃跑系统
│   │   ├── ClassDTerminationService.lua             # D级处决系统
│   │   │
│   │   │ ── 🔫 战斗 & 装备 ──
│   │   ├── CombatService.lua                        # 战斗系统核心
│   │   ├── WeaponService.lua                        # 武器管理
│   │   ├── DamageService.lua                        # 伤害计算
│   │   ├── HealthService.lua                        # 生命值/死亡/重生
│   │   ├── EquipmentService.lua                     # 装备管理(防弹衣/头盔等)
│   │   ├── InventoryService.lua                     # 背包系统
│   │   ├── AmmoService.lua                          # 弹药系统
│   │   │
│   │   │ ── 🚨 事件系统 ──
│   │   ├── BreachEventService.lua                   # 收容失效事件管理
│   │   ├── RaidEventService.lua                     # 混沌分裂者袭击事件
│   │   ├── EventSchedulerService.lua                # 事件调度器
│   │   ├── RoundService.lua                         # 回合/轮次管理(可选)
│   │   │
│   │   │ ── 🕵️ GOI (关注组织) ──
│   │   ├── GOIService.lua                           # 关注组织管理
│   │   ├── ChaosInsurgencyService.lua               # 混沌分裂者逻辑
│   │   ├── SerpentsHandService.lua                  # 蛇之手(可选)
│   │   ├── UIUService.lua                           # 不寻常事件调查科(可选)
│   │   │
│   │   │ ── 📻 通信系统 ──
│   │   ├── RadioService.lua                         # 无线电通信
│   │   ├── RadioChannels/                           # 电台频道定义
│   │   │   ├── SecurityChannel.lua                  # 安保频道
│   │   │   ├── MTFChannel.lua                       # MTF频道
│   │   │   ├── ResearchChannel.lua                  # 研究频道
│   │   │   ├── MedicalChannel.lua                   # 医疗频道
│   │   │   ├── CommandChannel.lua                   # 指挥频道
│   │   │   ├── CIChannel.lua                        # CI频道
│   │   │   └── EmergencyChannel.lua                 # 紧急频道
│   │   │
│   │   │ ── 🩺 医疗系统 ──
│   │   ├── MedicalService.lua                       # 医疗/治疗/手术
│   │   ├── StatusEffectService.lua                   # 状态效果(中毒/流血/感染/SCP效果)
│   │   ├── PsychologicalService.lua                 # 心理状态(恐惧/理智)
│   │   │
│   │   │ ── 🏗️ NPC系统 ──
│   │   ├── NPCService.lua                           # NPC管理
│   │   ├── NPCAIService.lua                         # NPC AI行为
│   │   ├── SCPEntityAI.lua                          # SCP实体AI(非玩家控制时)
│   │   ├── GuardNPCService.lua                      # NPC守卫AI
│   │   │
│   │   │ ── 🛡️ 管理系统 ──
│   │   ├── AdminService.lua                         # 管理员系统
│   │   ├── ModerationService.lua                    # 审核/举报
│   │   ├── BanService.lua                           # 封禁系统
│   │   ├── VotekickService.lua                      # 投票踢人
│   │   │
│   │   │ ── 💎 氪金 & 奖励 ──
│   │   ├── GamepassService.lua                      # Gamepass
│   │   ├── DevProductService.lua                    # Developer Products
│   │   ├── DailyRewardService.lua                   # 每日奖励
│   │   ├── PointsService.lua                        # 游戏积分系统
│   │   │
│   │   │ ── 📊 进度系统 ──
│   │   ├── PromotionService.lua                     # 晋升系统
│   │   ├── TrainingService.lua                      # 培训系统
│   │   ├── AchievementService.lua                   # 成就系统
│   │   └── StatisticsService.lua                    # 统计系统
│   │
│   ├── Components/                                  # 服务端ECS组件
│   │   ├── KeycardDoor.lua                          # 钥匙卡门组件
│   │   ├── ContainmentCell.lua                      # 收容室组件
│   │   ├── SecurityCamera.lua                       # 摄像头组件
│   │   ├── Generator.lua                            # 发电机组件
│   │   ├── Interactable.lua                         # 通用交互组件
│   │   ├── Breakable.lua                            # 可破坏组件
│   │   ├── Healable.lua                             # 可治疗组件
│   │   ├── Lockable.lua                             # 可锁定组件
│   │   ├── Alarm.lua                                # 警报器组件
│   │   ├── Speaker.lua                              # 广播喇叭组件
│   │   ├── Terminal.lua                             # 终端组件
│   │   ├── ElevatorNode.lua                         # 电梯节点组件
│   │   └── ZoneTrigger.lua                          # 区域触发器组件
│   │
│   └── Config/                                      # 服务端配置
│       ├── SecretConfig.lua                         # 密钥
│       ├── ServerSettings.lua                       # 服务器参数
│       ├── RateLimits.lua                           # 频率限制
│       ├── ClearancePermissions.lua                 # 各等级权限详表
│       └── BreachConfig.lua                         # 收容失效配置
│
│
│ ══════════════════════════════════════════════════════════════════
│  📡 REPLICATED STORAGE — 共享资源
│ ══════════════════════════════════════════════════════════════════
│
├── ReplicatedStorage/
│   │
│   ├── Shared/                                      # 共享基础模块
│   │   ├── Constants.lua                            # 全局常量
│   │   ├── GameConfig.lua                           # 游戏公共配置
│   │   ├── Types.lua                                # Luau类型定义
│   │   │
│   │   ├── Enums/                                   # 枚举值
│   │   │   ├── ClearanceEnum.lua                    # 权限等级枚举
│   │   │   │   -- Level0 = 0  (D级/访客)
│   │   │   │   -- Level1 = 1  (初级员工)
│   │   │   │   -- Level2 = 2  (研究员/保安)
│   │   │   │   -- Level3 = 3  (高级研究员/安保主管)
│   │   │   │   -- Level4 = 4  (设施主管/MTF指挥官)
│   │   │   │   -- Level5 = 5  (O5议会)
│   │   │   │   -- Omni  = 99  (万能卡)
│   │   │   │
│   │   │   ├── TeamEnum.lua                         # 团队枚举
│   │   │   │   -- ClassD
│   │   │   │   -- Security
│   │   │   │   -- Research
│   │   │   │   -- Medical
│   │   │   │   -- MTF
│   │   │   │   -- Engineering
│   │   │   │   -- InternalAffairs
│   │   │   │   -- EthicsCommittee
│   │   │   │   -- O5Council
│   │   │   │   -- SiteDirector
│   │   │   │   -- ChaosInsurgency
│   │   │   │   -- SerpentsHand
│   │   │   │   -- SCP
│   │   │   │   -- Spectator
│   │   │   │
│   │   │   ├── SCPClassEnum.lua                     # SCP分类枚举
│   │   │   │   -- Safe / Euclid / Keter / Thaumiel / Apollyon
│   │   │   │
│   │   │   ├── ZoneEnum.lua                         # 区域枚举
│   │   │   │   -- Surface / EntranceZone / LightContainment
│   │   │   │   -- HeavyContainment / PocketDimension
│   │   │   │
│   │   │   ├── DoorStateEnum.lua                    # 门状态枚举
│   │   │   │   -- Open / Closed / Locked / Destroyed / Lockdown
│   │   │   │
│   │   │   ├── AlertLevelEnum.lua                   # 警报等级枚举
│   │   │   │   -- Normal / Elevated / High / Critical / BreachContainment
│   │   │   │
│   │   │   ├── StatusEffectEnum.lua                 # 状态效果枚举
│   │   │   │   -- Bleeding / Poisoned / Infected / Burning
│   │   │   │   -- SCP049Touch / SCP096Rage / SCP106Corrode
│   │   │   │   -- Irradiated / Deafened / Blinded / Insane
│   │   │   │
│   │   │   ├── WeaponEnum.lua                       # 武器枚举
│   │   │   ├── ItemEnum.lua                         # 物品枚举
│   │   │   ├── RadioChannelEnum.lua                 # 电台频道枚举
│   │   │   ├── RankEnum.lua                         # 职位等级枚举
│   │   │   ├── SCPStateEnum.lua                     # SCP状态枚举
│   │   │   │   -- Contained / Breached / Recontained / Terminated
│   │   │   │
│   │   │   └── FacilityStateEnum.lua                # 设施状态枚举
│   │   │       -- Normal / PartialLockdown / FullLockdown
│   │   │       -- BreachProtocol / EvacuationProtocol
│   │   │       -- NuclearDetonation / AllClear
│   │   │
│   │   └── Formulas/                                # 共享计算公式
│   │       ├── DamageFormulas.lua                   # 伤害计算
│   │       ├── ClearanceFormulas.lua                # 权限判断公式
│   │       └── SCPBehaviorFormulas.lua              # SCP行为参数
│   │
│   ├── Libs/                                        # 工具库
│   │   ├── Promise.lua
│   │   ├── Signal.lua
│   │   ├── Trove.lua
│   │   ├── Component.lua
│   │   ├── Timer.lua
│   │   ├── Spring.lua
│   │   ├── TableUtil.lua
│   │   ├── StringUtil.lua
│   │   ├── MathUtil.lua
│   │   ├── CFrameUtil.lua
│   │   ├── RaycastUtil.lua
│   │   ├── FormatUtil.lua
│   │   ├── PathfindingUtil.lua                      # 寻路工具
│   │   ├── LineOfSightUtil.lua                      # 视线检测工具
│   │   ├── Serializer.lua
│   │   └── BitBuffer.lua                            # 位缓冲(网络优化)
│   │
│   ├── Network/                                     # 网络通信层
│   │   ├── NetworkConfig.lua
│   │   ├── ClientNetwork.lua
│   │   ├── ServerNetwork.lua
│   │   │
│   │   ├── Remotes/
│   │   │   ├── Events/
│   │   │   │   ├── Facility/
│   │   │   │   │   ├── DoorInteract                 # 门交互
│   │   │   │   │   ├── ElevatorCall                 # 呼叫电梯
│   │   │   │   │   ├── TerminalUse                  # 使用终端
│   │   │   │   │   ├── GeneratorInteract            # 发电机交互
│   │   │   │   │   ├── ButtonPress                  # 按钮按下
│   │   │   │   │   ├── ActivateWarhead              # 启动核弹
│   │   │   │   │   ├── CancelWarhead                # 取消核弹
│   │   │   │   │   └── TriggerLockdown              # 触发封锁
│   │   │   │   │
│   │   │   │   ├── SCP/
│   │   │   │   │   ├── SCPAbility                   # SCP使用能力
│   │   │   │   │   ├── SCPInteract                  # 与SCP交互
│   │   │   │   │   ├── ContainSCP                   # 重新收容
│   │   │   │   │   ├── SCP914Input                  # 914放入物品
│   │   │   │   │   └── SCP914Activate               # 914启动
│   │   │   │   │
│   │   │   │   ├── Combat/
│   │   │   │   │   ├── FireWeapon                   # 开火
│   │   │   │   │   ├── ReloadWeapon                 # 装弹
│   │   │   │   │   ├── MeleeAttack                  # 近战
│   │   │   │   │   ├── ThrowGrenade                 # 投掷手雷
│   │   │   │   │   └── TakeDamage                   # 受伤(服务端→客户端)
│   │   │   │   │
│   │   │   │   ├── Equipment/
│   │   │   │   │   ├── EquipItem                    # 装备物品
│   │   │   │   │   ├── UnequipItem                  # 卸下物品
│   │   │   │   │   ├── DropItem                     # 丢弃
│   │   │   │   │   ├── PickupItem                   # 拾取
│   │   │   │   │   └── UseItem                      # 使用(医疗包等)
│   │   │   │   │
│   │   │   │   ├── Radio/
│   │   │   │   │   ├── RadioTransmit                # 无线电发送
│   │   │   │   │   ├── ChangeChannel                # 切换频道
│   │   │   │   │   └── IntercomBroadcast            # 广播
│   │   │   │   │
│   │   │   │   ├── Team/
│   │   │   │   │   ├── RequestTeam                  # 请求加入团队
│   │   │   │   │   ├── LeaveTeam                    # 离开团队
│   │   │   │   │   └── PromotePlayer                # 晋升玩家
│   │   │   │   │
│   │   │   │   ├── ClassD/
│   │   │   │   │   ├── ClassDEscape                 # D级逃跑
│   │   │   │   │   ├── ClassDTerminate              # D级处决
│   │   │   │   │   └── ClassDTest                   # 带D级测试
│   │   │   │   │
│   │   │   │   ├── CCTV/
│   │   │   │   │   ├── ViewCamera                   # 切换摄像头
│   │   │   │   │   ├── NextCamera                   # 下一个
│   │   │   │   │   └── ExitCCTV                     # 退出监控
│   │   │   │   │
│   │   │   │   ├── Research/
│   │   │   │   │   ├── StartTest                    # 开始测试
│   │   │   │   │   ├── EndTest                      # 结束测试
│   │   │   │   │   ├── SubmitReport                 # 提交报告
│   │   │   │   │   └── RequestClassD                # 请求D级人员
│   │   │   │   │
│   │   │   │   ├── Medical/
│   │   │   │   │   ├── HealPlayer                   # 治疗
│   │   │   │   │   ├── RevivePlayer                 # 复活
│   │   │   │   │   ├── Diagnose                     # 诊断
│   │   │   │   │   └── AdministerDrug               # 给药
│   │   │   │   │
│   │   │   │   ├── GOI/
│   │   │   │   │   ├── CIRaid                       # CI发起袭击
│   │   │   │   │   ├── CIExtract                    # CI撤离
│   │   │   │   │   └── CIObjective                  # CI目标
│   │   │   │   │
│   │   │   │   ├── Admin/
│   │   │   │   │   ├── AdminCommand                 # 管理员命令
│   │   │   │   │   ├── Announce                     # 管理公告
│   │   │   │   │   └── ForceTeam                    # 强制切换团队
│   │   │   │   │
│   │   │   │   └── UI/
│   │   │   │       ├── UpdateHUD                    # 更新HUD
│   │   │   │       ├── ShowNotification             # 显示通知
│   │   │   │       ├── ShowObjective                # 显示目标
│   │   │   │       └── TriggerScreenEffect          # 触发屏幕效果
│   │   │   │
│   │   │   └── Functions/
│   │   │       ├── GetPlayerData
│   │   │       ├── GetSCPStatus                     # 获取SCP状态
│   │   │       ├── GetFacilityStatus                # 获取设施状态
│   │   │       ├── GetTeamRoster                    # 获取队伍名单
│   │   │       ├── GetDoorStatus                    # 获取门状态
│   │   │       ├── GetAvailableTeams                # 获取可加入团队
│   │   │       ├── GetInventory                     # 获取背包
│   │   │       └── GetLeaderboard                   # 获取排行榜
│   │   │
│   │   └── Middleware/
│   │       ├── RateLimiter.lua
│   │       ├── Validator.lua
│   │       ├── ClearanceChecker.lua                 # 权限等级检查中间件
│   │       └── Sanitizer.lua
│   │
│   ├── Data/                                        # ====== 数据定义 ======
│   │   │
│   │   ├── SCPs/                                    # SCP数据定义
│   │   │   ├── SCP049Data.lua
│   │   │   │   --[[
│   │   │   │       Name = "SCP-049",
│   │   │   │       Alias = "The Plague Doctor",
│   │   │   │       ObjectClass = "Euclid",
│   │   │   │       Zone = "HeavyContainment",
│   │   │   │       Health = 8000,
│   │   │   │       WalkSpeed = 14,
│   │   │   │       Abilities = {
│   │   │   │           KillingTouch = { Cooldown=3, Range=5 },
│   │   │   │           Resurrect = { Cooldown=30, Range=10 },
│   │   │   │       },
│   │   │   │       ContainmentRequirements = {
│   │   │   │           DoorLevel = 3,
│   │   │   │           SpecialConditions = {...},
│   │   │   │       },
│   │   │   │   ]]
│   │   │   ├── SCP096Data.lua
│   │   │   ├── SCP106Data.lua
│   │   │   ├── SCP173Data.lua
│   │   │   ├── SCP682Data.lua
│   │   │   ├── SCP939Data.lua
│   │   │   ├── SCP457Data.lua
│   │   │   ├── SCP035Data.lua
│   │   │   ├── SCP999Data.lua
│   │   │   ├── SCP914Data.lua
│   │   │   ├── SCP500Data.lua
│   │   │   ├── SCP131Data.lua
│   │   │   └── _SCPRegistry.lua                     # SCP总注册表
│   │   │
│   │   ├── Teams/                                   # 团队数据
│   │   │   ├── TeamDefinitions.lua                  # 团队定义(颜色/描述)
│   │   │   ├── TeamSpawns.lua                       # 团队出生点
│   │   │   ├── TeamLoadouts.lua                     # 团队初始装备
│   │   │   │   --[[
│   │   │   │       Security = {
│   │   │   │           Keycard = "Level2",
│   │   │   │           PrimaryWeapon = "P90",
│   │   │   │           SecondaryWeapon = "Glock17",
│   │   │   │           Equipment = {"Radio", "Handcuffs", "Flashlight"},
│   │   │   │           Armor = "LightArmor",
│   │   │   │       },
│   │   │   │   ]]
│   │   │   └── TeamPermissions.lua                  # 团队权限
│   │   │
│   │   ├── Ranks/                                   # 职位等级数据
│   │   │   ├── SecurityRanks.lua
│   │   │   │   -- Cadet → Guard → Corporal → Sergeant → Lieutenant → Captain → Commander
│   │   │   ├── ResearchRanks.lua
│   │   │   │   -- Intern → JuniorResearcher → Researcher → SeniorResearcher → Supervisor → Director
│   │   │   ├── MedicalRanks.lua
│   │   │   │   -- Trainee → Nurse → Doctor → Surgeon → ChiefMedicalOfficer
│   │   │   ├── MTFRanks.lua
│   │   │   │   -- Recruit → Operative → Specialist → Agent → TeamLeader → Commander
│   │   │   └── AdminRanks.lua
│   │   │       -- SiteDirector → O5Member
│   │   │
│   │   ├── Items/                                   # 物品数据
│   │   │   ├── Weapons/
│   │   │   │   ├── PistolData.lua                   # 手枪类
│   │   │   │   │   -- Glock17, M1911, DesertEagle, P250
│   │   │   │   ├── SMGData.lua                      # 冲锋枪类
│   │   │   │   │   -- P90, MP5, UMP45
│   │   │   │   ├── RifleData.lua                    # 步枪类
│   │   │   │   │   -- M4A1, AK47, SCAR
│   │   │   │   ├── ShotgunData.lua                  # 霰弹枪类
│   │   │   │   │   -- Remington870, SPAS12
│   │   │   │   ├── SniperData.lua                   # 狙击枪类
│   │   │   │   │   -- AWP, M14
│   │   │   │   ├── MeleeData.lua                    # 近战武器
│   │   │   │   │   -- Baton, Knife, Crowbar
│   │   │   │   └── SpecialData.lua                  # 特殊武器
│   │   │   │       -- MicroHID, Taser, FlamethrowerTank
│   │   │   │
│   │   │   ├── Keycards/
│   │   │   │   └── KeycardData.lua                  # 钥匙卡数据
│   │   │   │       -- KeycardLevel1...5, OmniCard, ContainmentEngineerCard
│   │   │   │
│   │   │   ├── Medical/
│   │   │   │   └── MedicalItemData.lua              # 医疗物品
│   │   │   │       -- FirstAidKit, Medkit, Painkillers, Adrenaline
│   │   │   │       -- SCP500Pill, Antidote, Bandage
│   │   │   │
│   │   │   ├── Equipment/
│   │   │   │   └── EquipmentData.lua                # 装备数据
│   │   │   │       -- Radio, Flashlight, NightVisionGoggles, GasMask
│   │   │   │       -- Handcuffs, DisarmDevice, BallisticShield
│   │   │   │       -- HazmatSuit, BombDefuseKit, S-NAV
│   │   │   │
│   │   │   ├── Armor/
│   │   │   │   └── ArmorData.lua                    # 护甲数据
│   │   │   │       -- LightArmor, MediumArmor, HeavyArmor, JuggernautArmor
│   │   │   │
│   │   │   ├── Throwables/
│   │   │   │   └── ThrowableData.lua                # 投掷物数据
│   │   │   │       -- FragGrenade, Flashbang, SmokeGrenade, GasGrenade
│   │   │   │
│   │   │   ├── SCPItems/
│   │   │   │   └── SCPItemData.lua                  # SCP相关物品
│   │   │   │       -- SCP500Pill, SCP714Ring, SCP330Candy
│   │   │   │       -- ContainmentBeacon, SCPTracker
│   │   │   │
│   │   │   └── _ItemRegistry.lua                    # 物品总注册表
│   │   │
│   │   ├── Facility/                                # 设施数据
│   │   │   ├── DoorDefinitions.lua                  # 所有门定义(位置/权限/类型)
│   │   │   ├── CameraDefinitions.lua                # 摄像头定义
│   │   │   ├── ZoneDefinitions.lua                  # 区域定义
│   │   │   ├── ElevatorDefinitions.lua              # 电梯定义
│   │   │   ├── TerminalDefinitions.lua              # 终端定义
│   │   │   ├── AlarmDefinitions.lua                 # 警报定义
│   │   │   ├── GeneratorDefinitions.lua             # 发电机定义
│   │   │   └── IntercomDefinitions.lua              # 广播点定义
│   │   │
│   │   ├── SCP914Recipes.lua                        # SCP-914 转换配方表
│   │   │   --[[
│   │   │       ["KeycardLevel1"] = {
│   │   │           Rough   = "ScrapMetal",
│   │   │           Coarse  = "BrokenKeycard",
│   │   │           OneToOne = "KeycardLevel1",   -- 随机另一张L1
│   │   │           Fine    = "KeycardLevel2",
│   │   │           VeryFine = "KeycardLevel3",   -- 小概率失败
│   │   │       },
│   │   │   ]]
│   │   │
│   │   ├── BreachScenarios.lua                      # 收容失效场景定义
│   │   │   -- 哪些SCP会失效、顺序、触发条件
│   │   │
│   │   ├── Protocols.lua                            # 基金会协议定义
│   │   │   -- Code Green / Code Yellow / Code Orange / Code Red / Code Black
│   │   │   -- Alpha Warhead Protocol / Omega Protocol
│   │   │
│   │   ├── Dialogues/                               # NPC对话
│   │   │   ├── SCP049Dialogue.lua
│   │   │   ├── SCP999Dialogue.lua
│   │   │   └── NPCGuardDialogue.lua
│   │   │
│   │   ├── Achievements/
│   │   │   └── AchievementDefinitions.lua
│   │   │
│   │   └── PlayerTemplate.lua                       # 新玩家数据模板
│   │
│   ├── Classes/                                     # OOP类定义
│   │   ├── BaseClass.lua
│   │   ├── SCPEntity.lua                            # SCP实体类
│   │   ├── DoorObject.lua                           # 门对象类
│   │   ├── WeaponObject.lua                         # 武器对象类
│   │   ├── KeycardObject.lua                        # 钥匙卡类
│   │   ├── EquipmentObject.lua                      # 装备类
│   │   ├── CameraObject.lua                         # 摄像头类
│   │   ├── InventoryObject.lua                      # 背包类
│   │   ├── StatusEffect.lua                         # 状态效果类
│   │   ├── RadioObject.lua                          # 无线电类
│   │   ├── TestSession.lua                          # 测试会话类
│   │   └── BreachEvent.lua                          # 收容失效事件类
│   │
│   ├── Assets/                                      # 共享资产
│   │   │
│   │   ├── SCPModels/                               # SCP模型
│   │   │   ├── SCP049_Model                         # 瘟疫医生
│   │   │   ├── SCP049_2_Model                       # 049-2 丧尸
│   │   │   ├── SCP096_Model                         # 害羞的家伙
│   │   │   ├── SCP096_Enraged_Model                 # 096暴怒状态
│   │   │   ├── SCP106_Model                         # 恐怖老人
│   │   │   ├── SCP173_Model                         # 花生
│   │   │   ├── SCP682_Model                         # 不灭孽蜥
│   │   │   ├── SCP939_Model                         # 众多声音
│   │   │   ├── SCP457_Model                         # 燃烧人
│   │   │   ├── SCP035_Model                         # 恶魔面具(戴在宿主上)
│   │   │   ├── SCP999_Model                         # 痒痒怪
│   │   │   ├── SCP131_Model                         # 眼泪滴
│   │   │   └── SCP529_Model                         # 半猫
│   │   │
│   │   ├── Weapons/                                 # 武器模型
│   │   │   ├── Pistols/
│   │   │   │   ├── Glock17_Model
│   │   │   │   ├── M1911_Model
│   │   │   │   └── DesertEagle_Model
│   │   │   ├── SMGs/
│   │   │   │   ├── P90_Model
│   │   │   │   ├── MP5_Model
│   │   │   │   └── UMP45_Model
│   │   │   ├── Rifles/
│   │   │   │   ├── M4A1_Model
│   │   │   │   ├── AK47_Model
│   │   │   │   └── SCAR_Model
│   │   │   ├── Shotguns/
│   │   │   │   ├── Remington870_Model
│   │   │   │   └── SPAS12_Model
│   │   │   ├── Snipers/
│   │   │   │   └── AWP_Model
│   │   │   ├── Melee/
│   │   │   │   ├── Baton_Model
│   │   │   │   ├── Knife_Model
│   │   │   │   └── Crowbar_Model
│   │   │   └── Special/
│   │   │       ├── MicroHID_Model                   # 微型HID炮
│   │   │       ├── Taser_Model
│   │   │       └── FemurBreaker_Model
│   │   │
│   │   ├── Equipment/                               # 装备模型
│   │   │   ├── Radio_Model
│   │   │   ├── Flashlight_Model
│   │   │   ├── NightVision_Model
│   │   │   ├── GasMask_Model
│   │   │   ├── Handcuffs_Model
│   │   │   ├── BallisticShield_Model
│   │   │   ├── HazmatSuit_Model
│   │   │   └── SNAV_Model                          # S-NAV 导航器
│   │   │
│   │   ├── Items/                                   # 物品模型
│   │   │   ├── Keycards/
│   │   │   │   ├── Keycard_Level1
│   │   │   │   ├── Keycard_Level2
│   │   │   │   ├── Keycard_Level3
│   │   │   │   ├── Keycard_Level4
│   │   │   │   ├── Keycard_Level5
│   │   │   │   ├── Keycard_Omni
│   │   │   │   └── Keycard_Containment
│   │   │   ├── Medical/
│   │   │   │   ├── FirstAidKit_Model
│   │   │   │   ├── Medkit_Model
│   │   │   │   ├── Painkillers_Model
│   │   │   │   ├── Adrenaline_Model
│   │   │   │   └── SCP500Pill_Model
│   │   │   ├── Throwables/
│   │   │   │   ├── FragGrenade_Model
│   │   │   │   ├── Flashbang_Model
│   │   │   │   ├── SmokeGrenade_Model
│   │   │   │   └── GasGrenade_Model
│   │   │   └── Misc/
│   │   │       ├── IDCard_Model
│   │   │       ├── Clipboard_Model                  # 研究用剪贴板
│   │   │       ├── BodyBag_Model
│   │   │       └── ContainmentDevice_Model
│   │   │
│   │   ├── Uniforms/                                # 制服
│   │   │   ├── Uniform_ClassD                       # D级橙色囚服
│   │   │   ├── Uniform_Security                     # 安保制服
│   │   │   ├── Uniform_Research                     # 研究员白袍
│   │   │   ├── Uniform_Medical                      # 医疗白衣
│   │   │   ├── Uniform_MTF                          # MTF战术装
│   │   │   ├── Uniform_MTF_Heavy                    # MTF重型装
│   │   │   ├── Uniform_Engineering                  # 工程制服
│   │   │   ├── Uniform_SiteDirector                 # 设施主管西装
│   │   │   ├── Uniform_O5                           # O5正装
│   │   │   ├── Uniform_CI                           # CI制服
│   │   │   ├── Uniform_CI_Heavy                     # CI重型装
│   │   │   └── Uniform_Janitor                      # 清洁工制服
│   │   │
│   │   ├── Effects/                                 # 视觉效果
│   │   │   ├── BloodSplatter                        # 血迹飞溅
│   │   │   ├── BulletHole                           # 弹孔
│   │   │   ├── MuzzleFlash                          # 枪口火焰
│   │   │   ├── Explosion                            # 爆炸
│   │   │   ├── SmokeCloud                           # 烟雾
│   │   │   ├── GasCloud                             # 毒气
│   │   │   ├── SCP106Portal                         # 106传送门特效
│   │   │   ├── SCP106Corrosion                      # 106腐蚀特效
│   │   │   ├── SCP096RageAura                       # 096暴怒光环
│   │   │   ├── SCP457FireTrail                      # 457火焰轨迹
│   │   │   ├── SCP999Glow                           # 999发光效果
│   │   │   ├── SCP049TouchEffect                    # 049触碰效果
│   │   │   ├── SCP173BlinkEffect                    # 173眨眼时闪屏
│   │   │   ├── TaserArc                             # 泰瑟电弧
│   │   │   ├── MicroHIDBeam                         # MicroHID光束
│   │   │   ├── DecontaminationGas                   # 消毒气体
│   │   │   ├── NuclearFlash                         # 核爆闪光
│   │   │   ├── AlarmFlash_Red                       # 红色警报闪光
│   │   │   ├── AlarmFlash_Yellow                    # 黄色警报闪光
│   │   │   ├── SparkEffect                          # 电火花
│   │   │   ├── HealingEffect                        # 治疗效果
│   │   │   └── PowerDownEffect                      # 停电效果
│   │   │
│   │   ├── UI/                                      # UI预制件
│   │   │   ├── ItemSlotTemplate
│   │   │   ├── TeamCard
│   │   │   ├── SCPStatusCard
│   │   │   ├── PlayerCard
│   │   │   ├── NotificationToast
│   │   │   ├── RadioMessage
│   │   │   ├── ObjectiveCard
│   │   │   ├── KeycardIcon
│   │   │   ├── WeaponHUDTemplate
│   │   │   ├── CCTVFeedFrame
│   │   │   ├── DoorStatusIndicator
│   │   │   ├── ExperimentLogEntry
│   │   │   ├── RankBadge
│   │   │   └── AchievementCard
│   │   │
│   │   └── Decals/                                  # 贴图
│   │       ├── SCP_Foundation_Logo
│   │       ├── SCP_Warning_Signs/
│   │       ├── Blood_Decals/
│   │       ├── Corrosion_Decals/
│   │       ├── Department_Logos/
│   │       │   ├── Logo_Security
│   │       │   ├── Logo_Research
│   │       │   ├── Logo_Medical
│   │       │   ├── Logo_MTF
│   │       │   └── Logo_Engineering
│   │       └── Zone_Markers/
│   │
│   └── Animations/                                  # 动画
│       ├── Character/
│       │   ├── Crouch                               # 蹲下
│       │   ├── CrouchWalk                           # 蹲走
│       │   ├── Sprint                               # 冲刺
│       │   ├── Prone                                # 趴下
│       │   ├── Surrender                            # 投降
│       │   ├── Handcuffed                           # 被铐住
│       │   ├── Carry                                # 搬运
│       │   └── Salute                               # 敬礼
│       │
│       ├── Weapons/
│       │   ├── Pistol_Idle
│       │   ├── Pistol_Fire
│       │   ├── Pistol_Reload
│       │   ├── Rifle_Idle
│       │   ├── Rifle_Fire
│       │   ├── Rifle_Reload
│       │   ├── Shotgun_Idle
│       │   ├── Shotgun_Fire
│       │   ├── Shotgun_Reload
│       │   ├── Melee_Swing
│       │   ├── Taser_Fire
│       │   ├── Shield_Hold
│       │   ├── Grenade_Throw
│       │   └── MicroHID_Fire
│       │
│       ├── Equipment/
│       │   ├── Flashlight_Hold
│       │   ├── Radio_Use
│       │   ├── Keycard_Swipe
│       │   ├── Medkit_Use
│       │   ├── Handcuff_Apply
│       │   └── Terminal_Type
│       │
│       ├── SCP/
│       │   ├── SCP049_Walk
│       │   ├── SCP049_Touch
│       │   ├── SCP049_Resurrect
│       │   ├── SCP096_Idle_Crying
│       │   ├── SCP096_Enrage
│       │   ├── SCP096_Chase
│       │   ├── SCP096_Attack
│       │   ├── SCP106_Walk
│       │   ├── SCP106_Emerge
│       │   ├── SCP106_Submerge
│       │   ├── SCP106_Grab
│       │   ├── SCP173_Idle
│       │   ├── SCP173_SnapNeck
│       │   ├── SCP682_Walk
│       │   ├── SCP682_Attack
│       │   ├── SCP682_Roar
│       │   ├── SCP939_Walk
│       │   ├── SCP939_Attack
│       │   ├── SCP939_Mimic
│       │   ├── SCP457_Walk
│       │   ├── SCP457_Ignite
│       │   ├── SCP999_Bounce
│       │   └── SCP999_Hug
│       │
│       └── Interactions/
│           ├── DoorOpen
│           ├── ButtonPress
│           ├── PickupItem
│           ├── SitChair
│           ├── UseComputer
│           └── Eating
│
│
│ ══════════════════════════════════════════════════════════════════
│  🧑 STARTER PLAYER — 客户端脚本
│ ══════════════════════════════════════════════════════════════════
│
├── StarterPlayer/
│   │
│   ├── StarterPlayerScripts/
│   │   │
│   │   ├── Core/
│   │   │   ├── ClientBootstrap.client.lua           # 🔥 唯一客户端入口
│   │   │   └── InputManager.lua                     # 输入管理
│   │   │
│   │   ├── Controllers/
│   │   │   │
│   │   │   │ ── 🎥 渲染 & 相机 ──
│   │   │   ├── CameraController.lua                 # 相机(第一/第三人称)
│   │   │   ├── CCTVCameraController.lua             # 监控摄像视角
│   │   │   ├── SpectatorCameraController.lua        # 旁观者相机
│   │   │   ├── PostProcessController.lua            # 后期效果(恐怖氛围)
│   │   │   ├── CinematicController.lua              # 过场动画
│   │   │   │
│   │   │   │ ── 🖼️ UI ──
│   │   │   ├── UIController.lua                     # UI总管理器
│   │   │   ├── HUDController.lua                    # HUD控制
│   │   │   ├── MenuController.lua                   # 菜单控制
│   │   │   ├── NotificationController.lua           # 通知控制
│   │   │   ├── ObjectiveController.lua              # 目标指示控制
│   │   │   ├── TooltipController.lua                # 工具提示
│   │   │   ├── ScoreboardController.lua             # 计分板/玩家列表
│   │   │   │
│   │   │   │ ── 👤 角色 ──
│   │   │   ├── CharacterController.lua              # 角色控制
│   │   │   ├── MovementController.lua               # 移动(跑/蹲/趴)
│   │   │   ├── StaminaController.lua                # 耐力系统
│   │   │   │
│   │   │   │ ── 🔫 战斗 & 武器 ──
│   │   │   ├── WeaponController.lua                 # 武器客户端控制
│   │   │   ├── AimController.lua                    # 瞄准/ADS
│   │   │   ├── RecoilController.lua                 # 后坐力
│   │   │   ├── CrosshairController.lua              # 准星
│   │   │   ├── HitmarkerController.lua              # 命中标记
│   │   │   ├── BulletHoleController.lua             # 弹孔贴花
│   │   │   │
│   │   │   │ ── 🎒 装备 & 物品 ──
│   │   │   ├── InventoryController.lua              # 背包UI
│   │   │   ├── EquipmentController.lua              # 装备切换
│   │   │   ├── FlashlightController.lua             # 手电筒(客户端灯光)
│   │   │   ├── NightVisionController.lua            # 夜视仪效果
│   │   │   ├── GasMaskController.lua                # 防毒面具效果
│   │   │   │
│   │   │   │ ── 📻 通信 ──
│   │   │   ├── RadioController.lua                  # 无线电UI/音效
│   │   │   ├── IntercomController.lua               # 广播UI
│   │   │   │
│   │   │   │ ── 🏢 设施交互 ──
│   │   │   ├── DoorController.lua                   # 门交互提示
│   │   │   ├── ElevatorController.lua               # 电梯UI
│   │   │   ├── TerminalController.lua               # 终端UI
│   │   │   ├── CCTVController.lua                   # 监控界面UI
│   │   │   ├── KeycardController.lua                # 刷卡UI效果
│   │   │   │
│   │   │   │ ── 👾 SCP 相关 ──
│   │   │   ├── SCPPlayController.lua                # 扮演SCP时的控制器
│   │   │   ├── SCPAbilityController.lua             # SCP能力UI/冷却
│   │   │   ├── SCP096ViewController.lua             # 096视线检测(客户端辅助)
│   │   │   ├── SCP173BlinkController.lua            # 173眨眼机制(客户端)
│   │   │   ├── SCP106PortalController.lua           # 106传送门视觉
│   │   │   ├── PocketDimensionController.lua        # 口袋维度视觉
│   │   │   │
│   │   │   │ ── 🌫️ 恐怖氛围 ──
│   │   │   ├── HorrorAtmosphereController.lua       # 恐怖氛围管理
│   │   │   ├── ScreenEffectController.lua           # 屏幕效果(受伤/死亡/恐惧)
│   │   │   ├── JumpscareController.lua              # 跳吓效果
│   │   │   ├── AmbientSoundController.lua           # 环境音效控制
│   │   │   │
│   │   │   │ ── 🔊 音频 ──
│   │   │   ├── SoundController.lua                  # 音效总控
│   │   │   ├── MusicController.lua                  # 音乐/氛围音乐
│   │   │   ├── FootstepController.lua               # 脚步声(材质区分)
│   │   │   │
│   │   │   │ ── ⚙️ 其他 ──
│   │   │   ├── TeamSelectController.lua             # 团队选择UI
│   │   │   ├── SettingsController.lua               # 设置
│   │   │   ├── TutorialController.lua               # 新手教程
│   │   │   └── DeathController.lua                  # 死亡界面/旁观
│   │   │
│   │   ├── Components/                              # 客户端组件
│   │   │   ├── Nameplate.lua                        # 头顶名牌(名字/部门/职级)
│   │   │   ├── DoorIndicator.lua                    # 门状态指示灯
│   │   │   ├── InteractPrompt.lua                   # 交互提示[E]
│   │   │   ├── KeycardLight.lua                     # 钥匙卡读取器灯光
│   │   │   ├── AlarmLight.lua                       # 警报灯闪烁
│   │   │   ├── CameraRotation.lua                   # 摄像头旋转
│   │   │   ├── GeneratorHum.lua                     # 发电机嗡嗡声
│   │   │   ├── FlickeringLight.lua                  # 闪烁灯光(恐怖氛围)
│   │   │   ├── BloodPool.lua                        # 血池效果
│   │   │   ├── SCPPresenceEffect.lua                # SCP存在感知效果
│   │   │   ├── CorrosionSpread.lua                  # 腐蚀扩散视觉(106)
│   │   │   └── EmergencyStrobe.lua                  # 紧急闪光灯
│   │   │
│   │   └── Systems/                                 # 客户端系统
│   │       ├── BlinkSystem.lua                      # 眨眼系统(SCP-173交互)
│   │       ├── LineOfSightSystem.lua                # 视线系统(SCP-096)
│   │       ├── ProximityVoiceSystem.lua             # 近距离语音(可选)
│   │       ├── StreamingManager.lua                 # 流式加载
│   │       ├── ObjectPoolManager.lua                # 对象池
│   │       └── PerformanceMonitor.lua               # 性能监控
│   │
│   └── StarterCharacterScripts/
│       ├── Animate.client.lua                       # 动画脚本
│       ├── CharacterEffects.client.lua              # 受伤/状态视觉
│       └── Footsteps.client.lua                     # 脚步声系统
│
│
│ ══════════════════════════════════════════════════════════════════
│  🎨 STARTER GUI — 用户界面
│ ══════════════════════════════════════════════════════════════════
│
├── StarterGui/
│   │
│   ├── HUD/                                         # ===== 游戏HUD =====
│   │   │
│   │   ├── HealthDisplay/                           # 生命值
│   │   │   ├── HealthBar
│   │   │   ├── ArmorBar
│   │   │   └── StaminaBar
│   │   │
│   │   ├── WeaponHUD/                               # 武器HUD
│   │   │   ├── AmmoCount                            # 弹药: 30/120
│   │   │   ├── WeaponName                           # 武器名
│   │   │   ├── FireMode                             # 射击模式(单发/连发)
│   │   │   └── Crosshair                            # 准星
│   │   │
│   │   ├── InventoryBar/                            # 快捷栏
│   │   │   ├── Slot_1 through Slot_8                # 物品槽1-8
│   │   │   └── ActiveSlotHighlight
│   │   │
│   │   ├── InfoPanel/                               # 信息面板
│   │   │   ├── TeamDisplay                          # 当前团队
│   │   │   ├── RankDisplay                          # 当前职级
│   │   │   ├── ZoneDisplay                          # 当前区域
│   │   │   ├── ClearanceDisplay                     # 权限等级
│   │   │   └── TimeDisplay                          # 游戏内时间
│   │   │
│   │   ├── RadioHUD/                                # 无线电HUD
│   │   │   ├── ChannelIndicator                     # 当前频道
│   │   │   ├── TransmitIndicator                    # 正在发送
│   │   │   └── IncomingMessages                     # 收到的消息
│   │   │
│   │   ├── FacilityStatus/                          # 设施状态HUD
│   │   │   ├── AlertLevel                           # 当前警报等级
│   │   │   ├── SCPBreachIndicators                  # SCP失效指示
│   │   │   ├── PowerStatus                          # 电力状态
│   │   │   ├── WarheadStatus                        # 核弹状态/倒计时
│   │   │   └── LockdownStatus                       # 封锁状态
│   │   │
│   │   ├── ObjectiveTracker/                        # 目标追踪
│   │   │   ├── CurrentObjective                     # 当前目标
│   │   │   ├── ObjectiveProgress                    # 目标进度
│   │   │   └── ObjectiveWaypoint                    # 目标路径指示
│   │   │
│   │   ├── StatusEffects/                           # 状态效果图标
│   │   │   ├── BleedingIcon
│   │   │   ├── PoisonedIcon
│   │   │   ├── InfectedIcon
│   │   │   ├── BurningIcon
│   │   │   ├── DeafenedIcon
│   │   │   ├── BlindedIcon
│   │   │   └── InsaneIcon
│   │   │
│   │   ├── InteractionPrompt/                       # 交互提示
│   │   │   ├── PromptText                           # [E] Open Door
│   │   │   ├── RequiredClearance                    # Requires: Level 3
│   │   │   └── ProgressRing                         # 长按进度环
│   │   │
│   │   ├── Compass/                                 # 指南针(可选)
│   │   │   ├── DirectionIndicator
│   │   │   └── POIMarkers
│   │   │
│   │   ├── SCPAbilityHUD/                           # SCP能力HUD(扮演SCP时)
│   │   │   ├── AbilitySlots/
│   │   │   │   ├── Ability_1
│   │   │   │   ├── Ability_2
│   │   │   │   └── Ability_3
│   │   │   ├── CooldownDisplay
│   │   │   └── SCPHealthBar
│   │   │
│   │   └── Hitmarker/                               # 命中标记
│   │       ├── NormalHit
│   │       ├── HeadshotHit
│   │       └── KillConfirm
│   │
│   ├── Menus/                                       # ===== 菜单 =====
│   │   │
│   │   ├── MainMenu/                                # 主菜单
│   │   │   ├── PlayButton
│   │   │   ├── TeamSelection/                       # 团队选择界面
│   │   │   │   ├── FoundationTeams/
│   │   │   │   │   ├── ClassD_Card
│   │   │   │   │   ├── Security_Card
│   │   │   │   │   ├── Research_Card
│   │   │   │   │   ├── Medical_Card
│   │   │   │   │   ├── MTF_Card
│   │   │   │   │   ├── Engineering_Card
│   │   │   │   │   ├── InternalAffairs_Card
│   │   │   │   │   ├── EthicsCommittee_Card
│   │   │   │   │   └── O5Council_Card
│   │   │   │   ├── GOI_Teams/
│   │   │   │   │   ├── ChaosInsurgency_Card
│   │   │   │   │   └── SerpentsHand_Card
│   │   │   │   ├── SCP_Selection/                   # SCP选择
│   │   │   │   │   ├── SCP049_Card
│   │   │   │   │   ├── SCP096_Card
│   │   │   │   │   ├── SCP106_Card
│   │   │   │   │   ├── SCP173_Card
│   │   │   │   │   ├── SCP682_Card
│   │   │   │   │   ├── SCP939_Card
│   │   │   │   │   └── SCP999_Card
│   │   │   │   ├── TeamInfo/                        # 团队信息面板
│   │   │   │   │   ├── Description
│   │   │   │   │   ├── Loadout
│   │   │   │   │   ├── Objectives
│   │   │   │   │   └── PlayerCount
│   │   │   │   └── ConfirmButton
│   │   │   ├── SettingsButton
│   │   │   └── CreditsButton
│   │   │
│   │   ├── PauseMenu/                               # ESC菜单
│   │   │   ├── ResumeButton
│   │   │   ├── SettingsButton
│   │   │   ├── RulesButton
│   │   │   ├── ReportButton
│   │   │   └── LeaveButton
│   │   │
│   │   ├── InventoryMenu/                           # 背包菜单
│   │   │   ├── ItemGrid
│   │   │   ├── ItemDetail
│   │   │   ├── EquipButton
│   │   │   ├── DropButton
│   │   │   └── UseButton
│   │   │
│   │   ├── CCTVMenu/                                # 监控界面
│   │   │   ├── CameraFeed/                          # 摄像头画面
│   │   │   │   ├── MainFeed
│   │   │   │   ├── StaticOverlay                    # 静态噪点
│   │   │   │   ├── Timestamp                        # 时间戳
│   │   │   │   └── CameraLabel                      # 摄像头名称
│   │   │   ├── CameraList/                          # 摄像头列表
│   │   │   │   ├── EZ_Cameras
│   │   │   │   ├── LCZ_Cameras
│   │   │   │   ├── HCZ_Cameras
│   │   │   │   └── Exterior_Cameras
│   │   │   ├── Controls/
│   │   │   │   ├── NextCamera
│   │   │   │   ├── PreviousCamera
│   │   │   │   ├── ZoomIn
│   │   │   │   ├── ZoomOut
│   │   │   │   └── ExitButton
│   │   │   └── DoorControls/                        # 远程门控制
│   │   │       ├── OpenDoor
│   │   │       ├── CloseDoor
│   │   │       └── LockDoor
│   │   │
│   │   ├── TerminalMenu/                            # 电脑终端界面
│   │   │   ├── TerminalScreen/
│   │   │   │   ├── LoginPrompt                      # 登录界面
│   │   │   │   ├── Desktop/                         # 桌面
│   │   │   │   │   ├── SCPDatabaseApp               # SCP数据库
│   │   │   │   │   ├── FacilityMapApp               # 设施地图
│   │   │   │   │   ├── PersonnelApp                 # 人员系统
│   │   │   │   │   ├── DoorControlApp               # 门控制
│   │   │   │   │   ├── CCTVApp                      # 监控
│   │   │   │   │   ├── IntercomApp                  # 广播
│   │   │   │   │   ├── WarheadControlApp            # 核弹控制(Level 5)
│   │   │   │   │   ├── LockdownControlApp           # 封锁控制
│   │   │   │   │   ├── ResearchLogApp               # 研究日志
│   │   │   │   │   └── LogoutButton
│   │   │   │   └── Scanlines                        # CRT扫描线效果
│   │   │   └── ExitTerminalButton
│   │   │
│   │   ├── RadioMenu/                               # 无线电菜单
│   │   │   ├── ChannelSelector                      # 频道选择
│   │   │   ├── TransmitButton                       # 发送按钮(PTT)
│   │   │   ├── VolumeSlider                         # 音量
│   │   │   └── MessageLog                           # 消息记录
│   │   │
│   │   ├── SCPDatabaseMenu/                         # SCP数据库界面
│   │   │   ├── SearchBar
│   │   │   ├── SCPList
│   │   │   ├── SCPDetailView/
│   │   │   │   ├── SCPImage
│   │   │   │   ├── Classification
│   │   │   │   ├── ContainmentProcedures
│   │   │   │   ├── Description
│   │   │   │   └── TestLogs
│   │   │   └── [REDACTED] Overlay                   # 权限不足时的遮挡
│   │   │
│   │   ├── ResearchMenu/                            # 研究界面
│   │   │   ├── ExperimentSetup/                     # 实验设置
│   │   │   │   ├── SCPSelector                      # 选择SCP
│   │   │   │   ├── SubjectSelector                  # 选择实验对象(D级)
│   │   │   │   ├── ProcedureNotes                   # 实验步骤记录
│   │   │   │   └── StartExperiment
│   │   │   ├── ExperimentLog/                       # 实验日志
│   │   │   │   ├── LogEntry
│   │   │   │   ├── ObservationNotes
│   │   │   │   └── ResultSummary
│   │   │   └── SubmitReport                         # 提交报告
│   │   │
│   │   ├── ScoreboardMenu/                          # 计分板/玩家列表
│   │   │   ├── PlayerList
│   │   │   │   ├── PlayerName
│   │   │   │   ├── PlayerTeam
│   │   │   │   ├── PlayerRank
│   │   │   │   └── PlayerPing
│   │   │   └── ServerInfo
│   │   │
│   │   ├── SettingsMenu/                            # 设置
│   │   │   ├── GraphicsSettings/
│   │   │   │   ├── RenderQuality
│   │   │   │   ├── ShadowQuality
│   │   │   │   └── ParticleEffects
│   │   │   ├── AudioSettings/
│   │   │   │   ├── MasterVolume
│   │   │   │   ├── MusicVolume
│   │   │   │   ├── SFXVolume
│   │   │   │   ├── AmbientVolume
│   │   │   │   └── RadioVolume
│   │   │   ├── GameplaySettings/
│   │   │   │   ├── Sensitivity
│   │   │   │   ├── FOV
│   │   │   │   ├── CrosshairStyle
│   │   │   │   ├── ToggleCrouch
│   │   │   │   └── ToggleSprint
│   │   │   └── AccessibilitySettings/
│   │   │       ├── Subtitles
│   │   │       ├── ScreenShake
│   │   │       ├── JumpscareIntensity               # 跳吓强度
│   │   │       └── ColorblindMode
│   │   │
│   │   ├── AdminMenu/                               # 管理员面板
│   │   │   ├── PlayerList
│   │   │   ├── CommandConsole
│   │   │   ├── FacilityControls                     # 设施控制
│   │   │   ├── SpawnSCP                             # 生成SCP
│   │   │   └── EventTrigger                         # 触发事件
│   │   │
│   │   └── RulesMenu/                               # 规则/帮助
│   │       ├── ServerRules
│   │       ├── TeamGuides
│   │       ├── SCPGuides
│   │       ├── ControlsGuide
│   │       └── FAQ
│   │
│   ├── Popups/                                      # ===== 弹窗 =====
│   │   ├── DeathScreen/                             # 死亡界面
│   │   │   ├── DeathMessage                         # "You were killed by SCP-173"
│   │   │   ├── KillerInfo
│   │   │   ├── SpectateButton                       # 旁观按钮
│   │   │   └── RespawnTimer                         # 重生倒计时
│   │   │
│   │   ├── BreachAlert/                             # 收容失效警告
│   │   │   ├── WarningText                          # "CONTAINMENT BREACH"
│   │   │   ├── SCPInfo                              # 哪个SCP失效
│   │   │   ├── ProtocolInstructions                 # 协议指令
│   │   │   └── AlarmAnimation                       # 警报动画
│   │   │
│   │   ├── WarheadWarning/                          # 核弹警告
│   │   │   ├── CountdownTimer                       # 倒计时
│   │   │   ├── WarningText                          # "NUCLEAR WARHEAD ACTIVATED"
│   │   │   └── EvacuationInstructions               # 撤离指令
│   │   │
│   │   ├── LockdownNotice/                          # 封锁通知
│   │   │   ├── LockdownZone                         # 封锁区域
│   │   │   └── Duration                             # 持续时间
│   │   │
│   │   ├── PromotionPopup/                          # 晋升弹窗
│   │   │   ├── NewRankTitle
│   │   │   ├── RankBadge
│   │   │   └── Congratulations
│   │   │
│   │   ├── AccessDeniedPopup/                       # 权限不足弹窗
│   │   │   ├── RequiredLevel
│   │   │   └── CurrentLevel
│   │   │
│   │   ├── IntercomPopup/                           # 广播文字显示
│   │   │   ├── SpeakerName
│   │   │   └── BroadcastText
│   │   │
│   │   ├── VotekickPopup/                           # 投票踢人
│   │   ├── ReportPopup/                             # 举报
│   │   └── AchievementPopup/                        # 成就解锁
│   │
│   ├── Overlays/                                    # ===== 屏幕覆盖层 =====
│   │   ├── LoadingScreen/                           # 加载界面
│   │   │   ├── SCP_Logo
│   │   │   ├── LoadingBar
│   │   │   ├── LoadingTips                          # 加载提示
│   │   │   └── ClassifiedStamp                      # [CLASSIFIED]印章
│   │   │
│   │   ├── FadeOverlay                              # 淡入淡出
│   │   ├── DamageOverlay                            # 受伤红屏
│   │   ├── BleedingOverlay                          # 流血效果
│   │   ├── PoisonOverlay                            # 中毒绿屏
│   │   ├── BurningOverlay                           # 燃烧橙屏
│   │   ├── InsanityOverlay                          # 失去理智效果
│   │   │
│   │   ├── SCP173BlinkOverlay                       # 173眨眼黑屏
│   │   ├── SCP096ScrambleOverlay                    # 096触发时的画面
│   │   ├── SCP106DimensionOverlay                   # 106口袋维度滤镜
│   │   │
│   │   ├── NightVisionOverlay                       # 夜视仪效果(绿色)
│   │   ├── GasMaskOverlay                           # 防毒面具边框
│   │   ├── FlashbangOverlay                         # 闪光弹白屏
│   │   ├── DecontaminationOverlay                   # 消毒气体
│   │   ├── NuclearFlashOverlay                      # 核爆闪光
│   │   ├── StaticNoiseOverlay                       # 静电噪点(SCP附近)
│   │   ├── CinematicBars                            # 电影黑边
│   │   └── VignetteOverlay                          # 暗角效果
│   │
│   └── Shared/                                      # UI共享组件
│       ├── UIComponents/
│       │   ├── Button.lua
│       │   ├── IconButton.lua
│       │   ├── ToggleSwitch.lua
│       │   ├── Slider.lua
│       │   ├── ProgressBar.lua
│       │   ├── CircularCooldown.lua                 # 冷却圆环
│       │   ├── ScrollList.lua
│       │   ├── TabContainer.lua
│       │   ├── Tooltip.lua
│       │   ├── Modal.lua
│       │   ├── Toast.lua
│       │   ├── Badge.lua
│       │   ├── StatusIcon.lua                       # 状态图标
│       │   └── TypewriterText.lua                   # 打字机效果文字
│       │
│       ├── UIAnimations/
│       │   ├── TweenPresets.lua
│       │   ├── UIAnimator.lua
│       │   ├── GlitchEffect.lua                     # 故障效果
│       │   ├── StaticEffect.lua                     # 静电效果
│       │   └── SCPRedactedEffect.lua                # [REDACTED]遮挡效果
│       │
│       └── UITheme/
│           ├── Colors.lua                           # SCP主题颜色(暗色调)
│           ├── Fonts.lua                            # 打字机/军事字体
│           ├── Spacing.lua
│           └── SCPClassColors.lua                   # SCP分级颜色
│               -- Safe=Green, Euclid=Yellow, Keter=Red, Thaumiel=Blue
│
│
│ ══════════════════════════════════════════════════════════════════
│  📦 SERVER STORAGE — 服务端存储
│ ══════════════════════════════════════════════════════════════════
│
├── ServerStorage/
│   │
│   ├── FacilityVariants/                            # 设施变体(随机生成)
│   │   ├── LCZ_Variant_A/
│   │   ├── LCZ_Variant_B/
│   │   ├── HCZ_Variant_A/
│   │   └── HCZ_Variant_B/
│   │
│   ├── PocketDimensionRooms/                        # 口袋维度房间变体
│   │   ├── Room_Corridor
│   │   ├── Room_TrapPit
│   │   ├── Room_Coffins
│   │   ├── Room_Throne
│   │   └── Room_Exit
│   │
│   ├── BreachSequences/                             # 收容失效预设序列
│   │   ├── Sequence_173Only
│   │   ├── Sequence_049_096
│   │   ├── Sequence_FullBreach
│   │   └── Sequence_682Breakout
│   │
│   ├── Templates/
│   │   ├── PlayerDataTemplate.lua
│   │   └── TestLogTemplate.lua                      # 实验日志模板
│   │
│   └── PrivateModules/
│       ├── DataStoreWrapper.lua
│       ├── OrderedDataStoreWrapper.lua
│       ├── MessagingServiceWrapper.lua              # 跨服通信
│       └── AntiExploitCore.lua                      # 核心反外挂
│
│
│ ══════════════════════════════════════════════════════════════════
│  🔊 SOUND SERVICE — 音频
│ ══════════════════════════════════════════════════════════════════
│
├── SoundService/
│   │
│   ├── Music/                                       # 背景音乐
│   │   ├── Ambient/
│   │   │   ├── Facility_Normal                      # 日常氛围
│   │   │   ├── Facility_Tense                       # 紧张氛围
│   │   │   ├── Facility_Horror                      # 恐怖氛围
│   │   │   ├── Facility_Breach                      # 收容失效氛围
│   │   │   ├── PocketDimension_Theme                # 口袋维度
│   │   │   ├── Surface_Day                          # 地面白天
│   │   │   └── Surface_Night                        # 地面夜晚
│   │   │
│   │   ├── Event/
│   │   │   ├── BreachTheme                          # 收容失效主题
│   │   │   ├── CIRaidTheme                          # CI袭击主题
│   │   │   ├── WarheadTheme                         # 核弹倒计时
│   │   │   ├── ChaseTheme                           # 被SCP追击
│   │   │   ├── VictoryTheme                         # 重新收容成功
│   │   │   └── DeathTheme                           # 死亡
│   │   │
│   │   └── Stingers/                                # 短促音乐
│   │       ├── JumpscareSting                       # 跳吓
│   │       ├── DiscoverySting                       # 发现
│   │       ├── PromotionSting                       # 晋升
│   │       └── WarningShort                         # 短警告
│   │
│   ├── SFX/                                         # 音效
│   │   ├── Weapons/
│   │   │   ├── Pistol_Fire
│   │   │   ├── Pistol_Reload
│   │   │   ├── Rifle_Fire
│   │   │   ├── Rifle_Reload
│   │   │   ├── Shotgun_Fire
│   │   │   ├── Shotgun_Reload
│   │   │   ├── Sniper_Fire
│   │   │   ├── Melee_Swing
│   │   │   ├── Melee_Hit
│   │   │   ├── Taser_Fire
│   │   │   ├── Taser_Hit
│   │   │   ├── MicroHID_Charge
│   │   │   ├── MicroHID_Fire
│   │   │   ├── BulletImpact_Metal
│   │   │   ├── BulletImpact_Concrete
│   │   │   ├── BulletImpact_Flesh
│   │   │   ├── EmptyClip
│   │   │   ├── Grenade_Pin
│   │   │   ├── Grenade_Bounce
│   │   │   ├── Grenade_Explode
│   │   │   ├── Flashbang_Explode
│   │   │   └── SmokeGrenade_Pop
│   │   │
│   │   ├── Facility/
│   │   │   ├── Door_Open
│   │   │   ├── Door_Close
│   │   │   ├── Door_Lock
│   │   │   ├── Door_Unlock
│   │   │   ├── Door_Access_Granted                  # 权限通过
│   │   │   ├── Door_Access_Denied                   # 权限拒绝
│   │   │   ├── BlastDoor_Open
│   │   │   ├── BlastDoor_Close
│   │   │   ├── Keycard_Swipe
│   │   │   ├── Elevator_Move
│   │   │   ├── Elevator_Ding
│   │   │   ├── Elevator_Door
│   │   │   ├── Generator_Start
│   │   │   ├── Generator_Running
│   │   │   ├── Generator_Stop
│   │   │   ├── Alarm_Breach                         # 收容失效警报
│   │   │   ├── Alarm_Lockdown                       # 封锁警报
│   │   │   ├── Alarm_Warhead                        # 核弹警报
│   │   │   ├── Alarm_Decontamination                # 消毒警报
│   │   │   ├── Alarm_Fire
│   │   │   ├── Alarm_Intruder                       # 入侵者警报
│   │   │   ├── Intercom_On
│   │   │   ├── Intercom_Off
│   │   │   ├── Intercom_Static
│   │   │   ├── Terminal_Startup
│   │   │   ├── Terminal_Type
│   │   │   ├── Terminal_Error
│   │   │   ├── Terminal_Access
│   │   │   ├── Light_Flicker
│   │   │   ├── Power_Down                           # 停电
│   │   │   ├── Power_Up                             # 来电
│   │   │   ├── Sprinkler
│   │   │   └── VentilationHum
│   │   │
│   │   ├── SCP/
│   │   │   ├── SCP049_Footstep
│   │   │   ├── SCP049_Touch
│   │   │   ├── SCP049_Speak                         # "I am the cure"
│   │   │   ├── SCP096_Cry                           # 哭泣声
│   │   │   ├── SCP096_Scream                        # 尖叫声
│   │   │   ├── SCP096_Enrage                        # 暴怒声
│   │   │   ├── SCP096_Attack
│   │   │   ├── SCP106_Laugh                         # 笑声
│   │   │   ├── SCP106_Emerge                        # 从地面冒出
│   │   │   ├── SCP106_Corrode                       # 腐蚀声
│   │   │   ├── SCP106_Dimension                     # 口袋维度环境音
│   │   │   ├── SCP173_Scrape                        # 刮擦声
│   │   │   ├── SCP173_NeckSnap                      # 断颈声
│   │   │   ├── SCP173_Move                          # 移动声(不看时)
│   │   │   ├── SCP682_Roar
│   │   │   ├── SCP682_Stomp
│   │   │   ├── SCP682_Attack
│   │   │   ├── SCP939_Growl                         # 低吼
│   │   │   ├── SCP939_Mimic                         # 模仿人声
│   │   │   ├── SCP939_Attack
│   │   │   ├── SCP457_Burn                          # 燃烧声
│   │   │   ├── SCP457_Ignite
│   │   │   ├── SCP999_Giggle                        # 咯咯笑
│   │   │   ├── SCP999_Bounce
│   │   │   ├── SCP914_Activate                      # 914启动
│   │   │   ├── SCP914_Process                       # 914处理中
│   │   │   ├── SCP914_Complete                      # 914完成
│   │   │   └── FemurBreaker_Scream                  # 断股器惨叫
│   │   │
│   │   ├── Character/
│   │   │   ├── Footstep_Concrete
│   │   │   ├── Footstep_Metal
│   │   │   ├── Footstep_Tile
│   │   │   ├── Footstep_Grate
│   │   │   ├── Footstep_Grass
│   │   │   ├── Footstep_Water
│   │   │   ├── Jump
│   │   │   ├── Land
│   │   │   ├── Hurt_Light
│   │   │   ├── Hurt_Heavy
│   │   │   ├── Death
│   │   │   ├── Heartbeat                            # 低血量心跳
│   │   │   ├── Breathing_Heavy                      # 喘息
│   │   │   ├── Handcuff_Apply
│   │   │   ├── Handcuff_Break
│   │   │   └── Scream
│   │   │
│   │   ├── UI/
│   │   │   ├── Click
│   │   │   ├── Hover
│   │   │   ├── MenuOpen
│   │   │   ├── MenuClose
│   │   │   ├── Notification
│   │   │   ├── Error
│   │   │   ├── Success
│   │   │   ├── RadioClick
│   │   │   ├── RadioStatic
│   │   │   └── Classified                           # [CLASSIFIED]音效
│   │   │
│   │   └── Environment/
│   │       ├── Wind
│   │       ├── Rain
│   │       ├── Thunder
│   │       ├── FloorCreak
│   │       ├── PipeGroan
│   │       ├── DistantBang
│   │       ├── MetalStress
│   │       ├── WaterDrip
│   │       ├── ElectricalBuzz
│   │       └── DistantScream                        # 远处尖叫(氛围)
│   │
│   └── AmbientLoops/
│       ├── Facility_Hum                             # 设施低鸣
│       ├── Ventilation_Loop                         # 通风循环
│       ├── Computer_Room_Loop                       # 机房嗡嗡
│       ├── MedicalBay_Beep                          # 医疗仪器
│       ├── CellBlock_Echo                           # 牢房回声
│       ├── HeavyContainment_Deep                    # 深层低频
│       ├── PocketDimension_Drone                    # 口袋维度嗡鸣
│       └── Forest_Night                             # 森林夜晚
│
│
│ ══════════════════════════════════════════════════════════════════
│  💡 LIGHTING — 光照
│ ══════════════════════════════════════════════════════════════════
│
├── Lighting/
│   ├── Atmosphere
│   ├── Sky_Overcast                                 # 阴天天空盒
│   ├── Bloom
│   ├── ColorCorrection_Normal                       # 正常色调(微冷)
│   ├── ColorCorrection_Breach                       # 收容失效(红色调)
│   ├── ColorCorrection_PocketDim                    # 口袋维度(棕褐色)
│   ├── ColorCorrection_NightVision                  # 夜视仪(绿色)
│   ├── DepthOfField
│   ├── Blur_MenuEffect
│   └── SunRays
│
│
│ ══════════════════════════════════════════════════════════════════
│  🏷️ TEAMS & CHAT
│ ══════════════════════════════════════════════════════════════════
│
├── Teams/
│   ├── ClassD                                       # D级人员 (橙色)
│   ├── Security                                     # 安保 (蓝色)
│   ├── Research                                     # 研究部 (白色)
│   ├── Medical                                      # 医疗部 (绿色)
│   ├── MTF                                          # 机动特遣队 (深蓝)
│   ├── Engineering                                  # 工程部 (黄色)
│   ├── InternalAffairs                              # 内部事务 (紫色)
│   ├── EthicsCommittee                              # 伦理委员会 (金色)
│   ├── O5Council                                    # O5议会 (黑色)
│   ├── SiteDirector                                 # 设施主管 (暗红)
│   ├── ChaosInsurgency                              # 混沌分裂者 (暗绿)
│   ├── SerpentsHand                                 # 蛇之手 (暗紫)
│   ├── SCP                                          # SCP实体 (红色)
│   └── Spectator                                    # 旁观者 (灰色)
│
├── Chat/
│   └── ChatModules/
│       ├── RPNameTag.lua                            # RP名显示
│       ├── ProximityChat.lua                        # 距离聊天
│       ├── RadioChatIntegration.lua                 # 无线电聊天整合
│       ├── TeamChat.lua                             # 团队频道
│       ├── IntercomChat.lua                         # 广播频道
│       ├── WhisperSystem.lua                        # 耳语
│       └── CustomCommands.lua                       # /me /do /ooc /roll
│
│
│ ══════════════════════════════════════════════════════════════════
│  ⭐ STARTER PACK
│ ══════════════════════════════════════════════════════════════════
│
├── StarterPack/
│   └── (空 — 通过 TeamService + EquipmentService 动态给予)
│
│
│ ══════════════════════════════════════════════════════════════════
│  🧪 TEST SERVICE — 测试
│ ══════════════════════════════════════════════════════════════════
│
└── TestService/
    ├── Unit/
    │   ├── ClearanceServiceTest.lua
    │   ├── DoorServiceTest.lua
    │   ├── SCPBehaviorTest.lua
    │   ├── CombatServiceTest.lua
    │   ├── InventoryServiceTest.lua
    │   ├── KeycardServiceTest.lua
    │   ├── BreachEventTest.lua
    │   └── SCP914ProcessTest.lua
    │
    ├── Integration/
    │   ├── BreachFlowTest.lua                       # 完整收容失效流程
    │   ├── ClassDEscapeFlowTest.lua                 # D级逃跑流程
    │   ├── MTFRecontainmentTest.lua                 # MTF重新收容流程
    │   └── WarheadFlowTest.lua                      # 核弹流程
    │
    └── TestRunner.lua
    ```
