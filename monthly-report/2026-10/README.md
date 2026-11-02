# 具身智能开源观察 · 2026 年 10 月

> **一句话速览**：star 方面，论文代码依然是新仓库起量最快的方式，星动纪元的 VPP2 三周拿到 347 star；使用方面，用户 fork 最多的仍是仿真、RL 训练和 SDK 这类基础配套，新机型的适配问题开始集中出现。

<sub>本报告由 LimX 团队撰写，数据来自 GitHub 公开 API 每日采集存档。star 净增取 2026-09-30 与 10-31 两次快照之差；fork、issue、PR 按创建时间落在 10 月统计（北京时间）。完整口径与利益披露见[文末](#数据口径与披露)。</sub>

## 本月速览

| 数字 | 含义 |
| --- | --- |
| **+1,199** | 其余 8 家 10 月 star 合计净增（存量从 40,145 增至 41,344，增速 3.0%，与 9 月的 3.1% 基本持平） |
| **46%** | 宇树占这 8 家合计增量的比例，9 月为 69% |
| **+347** | 星动纪元 10-08 新建的 video-prediction-policy-2 当月 star，其余 9 个当月新建仓库合计只有 12 |
| **57%** | 9 家当月新增的 star 中，来自 2026 年 4 月以前就已建立的老仓库的比例 |
| **49%** | 10 月 286 个新 fork 中，仿真 / RL 训练与 SDK / ROS 两类仓库的占比 |
| **6 / 21** | 宇树 21 个用户提问中，询问 H2、R1 等新机型适配的数量 |
| **第 4 名** | LimX（含 FluxVLA）10 月 star 净增 +93，排在宇树 553、星动纪元 373、智元 153 之后 |

## 本月趋势

1. **论文代码仍是新仓库最快的起量方式**：VPP2 上线首日 +85、一周 +221；其余 9 个新仓库合计 12 star。
2. **老仓库提供稳定增量**：57% 的新增 star 来自半年以上的老仓库，其中四成来自 10 月没有任何推送的仓库。
3. **用户拿去用的，主要是让机器人跑起来的基础配套**：仿真 / RL 训练和 SDK / ROS 两类占新 fork 的一半，延续 9 月的趋势。
4. **新机型带来适配需求，开源越来越像产品配套**：宇树的用户提问集中在 H2、R1 等新机型；智元为新品 OmniGlove 同步开源了 SDK 和工具包。
5. **提问的响应速度开始拉开差距**：VPP2 的 11 个提问全部得到回复；头部组织的未关闭 issue 普遍在百个以上。

[查看趋势详解 ↓](#本月趋势详解)

---

## 本月详细

### 谁在涨

![10 月 star 净增与增速](images/star-growth-by-company-2026-10.png)

> 宇树净增 553 居首，星动纪元凭一个新仓库 +373 升至第二，智元 153、LimX（含 FluxVLA）93 分列三四。傅利叶 +1，松延动力本月零增长。

### 涨在哪些仓库

![10 月新增 star 的仓库来源](images/star-sources-by-repo-2026-10.png)

> 星动纪元 93% 的增量来自 video-prediction-policy-2；宇树 554 个新增分散在 35 个仓库，其中 485 个（88%）来自 2026 年 4 月以前建立的仓库；LimX 约六成来自 FluxVLA。

### 谁开了新仓库

按 GitHub 建仓时间（`created_at`）统计：

| 企业 | 10 月新建 | 代表项目 | 10 月底 star |
| --- | --- | --- | --- |
| 星动纪元 | 1 | [video-prediction-policy-2](https://github.com/roboterax/video-prediction-policy-2)（视频预测策略论文代码，10-08） | 347 |
| 宇树 | 2 | unitree_robotskills（技能框架，10-28）、D2-Arm（机械臂交付资料，10-29） | 5 |
| 智元 | 4 | agilink_omniglove_sdk / agilink_omniglove_toolbox（数据手套 SDK 与工具，10-27 / 10-30）、agibot_agentsdk_sample_code（AgentSDK 示例，10-15）、vine-code | 7 |
| LimX | 2 | tron2_visual_grasp（视觉抓取示例）、embodied-ai-insights（本月报） | 0 |
| ANYbotics | 1 | Leg-KILO（腿式机器人里程计） | 0 |
| 其余 4 家 | 0 | — | — |

> 10 个新仓库中，只有论文代码 VPP2 获得了明显关注；其余 9 个多为 SDK、示例、交付资料这类产品配套，合计 12 star。

### 用户在用什么

10 月 fork 最多的仓库（fork 代表有人把代码拿去自己改、自己用）：

| 类别 | 仓库（10 月新 fork） | 合计 |
| --- | --- | --- |
| 仿真 / RL 训练 | unitree_rl_mjlab 21、unitree_rl_gym 20、unitree_mujoco 17、unitree_rl_lab 15、genie_sim 9、unitree_sim_isaaclab 8 | 90 |
| 基础模型 / VLA | unifolm-wla 17、FluxVLA 14、video-prediction-policy-2 11、unifolm-world-model-action 5、Genie-Envisioner-V1 5、ACoT-VLA 3 | 55 |
| SDK / ROS | unitree_sdk2_python 16、unitree_sdk2 13、unitree_ros 11、unitree_ros2 8、r1-7a_sdk 3 | 51 |
| 遥操作 | xr_teleoperate 14、teleimager 5 | 19 |
| 建图 | grid_map 6 | 6 |

> 上表为 fork 数前 20 的仓库，合计 221 个，占 10 月全部 286 个新 fork 的 77%。仿真 / RL 训练与 SDK / ROS 两类合计 141 个，占全部新 fork 的 49%。

### 用户在问什么

10 月 9 家共新增 45 个 issue。其中 8 个来自同一个第三方账号（PHM-Audit），于 10-25 至 10-27 向 5 家企业提交了机器人模型质量、惯量核查和代码审查类 issue，下文的用户提问统计不含这 8 个。

- **宇树（21 个，分布在 10 个仓库）**：
  - 新机型适配 6 个：H2 的灵巧手、LeRobot、腰部和头部控制，R1 的上层接口和电源故障，以及"SDK2 是否支持所有机型"；
  - UnifoLM-WLA 复现与部署 4 个：评测仿真环境、演示用货架尺寸、遥操作采数与 G1 部署等；
  - RL 策略低速指令测试 3 个；
  - 模型参数与仿真转换 3 个；
  - 其他 5 个，包括"示例代码在哪里"。
- **星动纪元（11 个，全部在 VPP2）**：集中在训练细节、数据来源和后续开放计划。
- **智元（3 个）**：genie_sim 自定义物体和评分 bug、A3 USD 模型问题。

> 用户提问以"怎么在我的机型上用起来"为主。新机型发布后，SDK、示例和文档是否同步到位，直接体现在 issue 里。

### 社区活跃度（9 月 → 10 月）

| 企业 | 新 fork | 新 issue | 新 PR |
| --- | --- | --- | --- |
| 宇树 | 215 → 195 | 26 → 23 | 20 → 21 |
| 智元 | 32 → 28 | 2 → 3 | 7 → 4 |
| LimX（含 FluxVLA） | 20 → 28 | 5 → 4 | 27 → 45 |
| 星动纪元 | 3 → 14 | 0 → 12 | 0 → 0 |
| 云深处 | 19 → 8 | 2 → 0 | 6 → 2 |
| ANYbotics | 9 → 8 | 0 → 0 | 2 → 0 |
| 星海图 | 17 → 3 | 4 → 2 | 1 → 0 |
| 傅利叶 | 2 → 2 | 0 → 1 | 0 → 0 |
| 松延动力 | 0 → 0 | 0 → 0 | 0 → 0 |

> 10 月初国庆长假（10-01 至 10-08），多数企业的新 fork 环比回落。宇树 10 月新增 fork 是其余 8 家之和（91 个）的 2.1 倍。星动纪元的 fork 和 issue 增长全部来自 VPP2。LimX 的 PR 增长主要是内部的文档整改。
>
> 本月版本发布：智元 agilink_omnihand_sdk v1.1.10（10-15）、agilink_omniglove_sdk v1.0.0（10-30），云深处 station-openapi-devkit v1.1.0（10-20），FluxVLA v0.2.0（10-30）。

### 增长榜

| # | 仓库 | 企业 | 10 月 +star | 方向 |
| --- | --- | --- | --- | --- |
| 1 | [video-prediction-policy-2](https://github.com/roboterax/video-prediction-policy-2) 🆕 | 星动纪元 | 347 | 视频预测策略 |
| 2 | [unitree_rl_gym](https://github.com/unitreerobotics/unitree_rl_gym) | 宇树 | 69 | RL 训练 |
| 3 | [genie_sim](https://github.com/AgibotTech/genie_sim) | 智元 | 61 | 仿真 |
| 4 | [unifolm-wla](https://github.com/unitreerobotics/unifolm-wla) | 宇树 | 57 | 人形基础模型 |
| 5 | [FluxVLA](https://github.com/FluxVLA/FluxVLA) | LimX | 55 | VLA 工程平台 |
| 6 | [unitree_rl_lab](https://github.com/unitreerobotics/unitree_rl_lab) | 宇树 | 54 | RL 训练 |
| 7 | [unitree_ros](https://github.com/unitreerobotics/unitree_ros) | 宇树 | 46 | ROS |
| 8 | [unitree_rl_mjlab](https://github.com/unitreerobotics/unitree_rl_mjlab) | 宇树 | 46 | RL 训练 |
| 9 | [unitree_mujoco](https://github.com/unitreerobotics/unitree_mujoco) | 宇树 | 45 | MuJoCo 仿真 |
| 10 | [unitree_sdk2](https://github.com/unitreerobotics/unitree_sdk2) | 宇树 | 42 | SDK |
| 11 | [xr_teleoperate](https://github.com/unitreerobotics/xr_teleoperate) | 宇树 | 34 | XR 遥操作 |
| 12 | [unitree_ros2](https://github.com/unitreerobotics/unitree_ros2) | 宇树 | 33 | ROS 2 |
| 13 | [sonic_for_a3](https://github.com/AgibotTech/sonic_for_a3) | 智元 | 24 | 人形全身控制 |
| 14 | [elevation_mapping](https://github.com/ANYbotics/elevation_mapping) | ANYbotics | 23 | 地形建图 |

> 🆕 为 10 月新建仓库。榜单 14 个仓库中 8 个是仿真、RL 训练、SDK 和 ROS 类，合计 396 star；基础模型 / VLA 类 3 个，合计 459 star，其中 347 来自 VPP2。

---

## 本月趋势详解

### 1. 论文代码仍是新仓库最快的起量方式

- VPP2 是论文《Video Prediction Policy 2》的官方实现，10-08 建仓，首日 +85，一周 +221，到 10-31 共 347 star。单个仓库的月增量超过了除宇树外任何一家企业。
- 增长集中在前两周：第二周日增约 12 个，第三周起降到 4 个左右。
- 10 月其余 9 个新仓库以 SDK、示例代码和交付资料为主，合计 12 star。和 9 月一样，没有配合论文、视频或新品发布的新仓库很难获得第一批关注。

### 2. 老仓库提供稳定增量

- 9 家当月新增的 1,301 个 star（只算有新增的仓库）中，739 个（57%）来自 2026 年 4 月以前建立的仓库，525 个（40%）来自 10 月没有任何推送的仓库。
- 宇树最明显：554 个新增中 485 个来自老仓库。增长最多的 unitree_rl_gym 自 2025-07 以来没有新推送，10 月仍 +69。
- 这些老仓库大多是 RL 训练、仿真、SDK 和 ROS 包，也就是买了机器人之后用得上的配套。配套完整的机型，不发新仓库也能持续获得关注。

### 3. 用户拿去用的，主要是让机器人跑起来的基础配套

- 10 月 fork 前 20 的仓库里，仿真 / RL 训练 90 个、SDK / ROS 51 个，合计占全部新 fork 的 49%；基础模型 / VLA 55 个，遥操作 19 个。
- unitree_rl_mjlab 连续两个月位列 fork 前三（9 月 21 个、10 月 21 个）。训练框架延续 Isaac Lab 与 MuJoCo / mjlab 双轨并行。
- star 更多反映"关注"，fork 更接近"使用"。两张榜单的差别在于：基础模型拿到的 star 更多，仿真、训练和 SDK 拿到的 fork 更多。

### 4. 新机型带来适配需求，开源越来越像产品配套

- 宇树 21 个用户提问中有 6 个围绕 H2、R1 等新机型：SDK 能否控制腰部和头部、LeRobot 是否支持 H2、灵巧手是否适配 H2，以及"SDK2 是否支持所有机型"。新机型的出货速度，正在考验 SDK 和示例的覆盖速度。
- 智元在新品 OmniGlove 发布时同步开源了 SDK（v1.0.0）和工具包，并新建了 AgentSDK 示例代码仓库；宇树新建了 D2 机械臂的交付资料仓库和 RobotSkills 技能框架。
- 越来越多新仓库的定位是"随产品交付的配套"：它们不一定带来 star，但直接决定了用户拿到机器人后能否上手。

### 5. 提问的响应速度开始拉开差距

- VPP2 的 11 个提问全部有回复，9 个已关闭，从提出到关闭的中位时间为 1.6 天，论文作者团队直接在 issue 里答疑。
- 头部组织普遍积压着大量未关闭的 issue：截至 11-01，宇树 798 个、ANYbotics 267 个、智元 153 个。宇树 10 月的 21 个用户提问中，5 个有评论，尚无关闭。
- 第三方开始系统性地核查各家的机器人模型文件：PHM-Audit 一个账号在三天内向 5 家提交了 8 个 issue，其中 5 个是模型文件的质量、惯量核查。对用户来说，模型参数是否准确，直接影响仿真结果能否迁移到真机。

---

## 数据口径与披露

**统计对象**

- LimX：limxdynamics 主账号（10 月底 52 个公开仓库，其中 6 个为 fork 派生仓）加 FluxVLA 组织（FluxVLA、FluxBisim、FluxDAgger、FluxThemis、FluxMimir）。"LimX（含 FluxVLA）"指二者之和。
- 其余 8 家：宇树（unitreerobotics）、智元（AgibotTech）、云深处（DeepRoboticsLab）、星海图（OpenGalaxea）、ANYbotics、星动纪元（roboterax）、傅利叶（FFTAI）、松延动力（pndbotics）。
- 乐聚（LejuRobotics）应读者建议，自 2026-10-30 起加入采集，因 10 月数据不完整，从 11 月月报开始纳入比较。

**数据来源**

GitHub REST API 公开数据，每日采集存档；背景信息取自 [video-prediction-policy-2](https://github.com/roboterax/video-prediction-policy-2) 的 README。

**统计周期**

2026 年 10 月自然月（北京时间）。star 净增取 2026-09-30 与 2026-10-31 两次快照之差，跨企业比较含 fork 派生仓。fork、issue、PR 按 `created_at` 落在 2026-10 统计，issue 已排除 PR。环比的 9 月数据按同一口径用当前存档重新计算，因少量 fork 或 issue 已被删除，与 9 月月报的数字可能相差 1–5 个。

**口径细节**

- 智元 agillink_omnihand_sdk 在 10 月更名为 agilink_omnihand_sdk，按同一仓库计算。
- 9 家合计的 1,301 个新增 star 只计有新增的仓库；按企业的净增已扣除少数仓库 1–2 个的减少。
- FluxVLA 组织的 star 由逐条 star 记录按两次快照的采集时刻截取（765 → 828），比 9 月月报的估算更准确。因此 LimX 9 月底存量记为 1,328，比 9 月月报少 1。
- "用户提问"不含 PHM-Audit 账号提交的 8 个 issue。"有回复"指 issue 下至少有一条评论，不区分是否为官方回复。关闭状态截至 11-01 的采集。

**局限**

- star、fork 反映关注度和使用意愿，不等于实际使用量。
- issue / PR 统计未区分企业内部与外部贡献者。
- 其余 8 家无法获取逐条 star 记录，只能计算仓库级总量差。VPP2 的逐日走势来自每日快照的仓库总数，不涉及逐条记录。
- 趋势基于一个月的数据归纳，将在后续月报中持续验证。

**利益披露**

本报告由 LimX 团队撰写并维护。LimX 及 FluxVLA 相关仓库的逐条 star、fork 来源和内部活跃度由内部直接采集，粒度高于其他企业；其他企业仅使用 GitHub 公开聚合数据。为保持可比性，跨企业排名与趋势判断只采用所有企业都可获得的同口径公开数据；LimX 独家深度数据仅用于案例复盘，不单独用于得出"某家更强 / 更弱"的结论。报告观点仅代表作者，欢迎通过 issue 指正。
