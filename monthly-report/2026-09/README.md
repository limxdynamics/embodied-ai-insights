# 具身智能开源观察 · LimX 版 · 2026年9月

2026年10月10日 · @LimX-Gwen

**利益披露**：本报告由 LimX 团队撰写并维护。LimX 及 FluxVLA 相关仓库的逐条 star、fork 来源和内部活跃度由内部直接采集，粒度高于其他企业；其他企业仅使用 GitHub 公开聚合数据。为保持可比性，跨企业排名与趋势判断优先采用所有企业可获得的同口径公开数据；LimX 独家深度数据仅用于案例复盘，不单独用于得出“某家更强/更弱”的结论。报告观点仅代表作者，欢迎指正。

## 一、数据来源

全部数据来自 GitHub REST API（[api.github.com](http://api.github.com)）提供的公开数据，每日采集存档，少量背景信息取自仓库 README 和 arXiv。

**统计对象**

- LimX：limxdynamics 主账号（9 月底 50 个公开仓库）+ FluxVLA 组织（FluxVLA、FluxBisim、FluxDAgger 三仓）。文中“LimX 合计”指二者之和，FluxVLA 部分单独标出。

- 其余 8 家企业：宇树（unitreerobotics）、智元（AgibotTech）、云深处（DeepRoboticsLab）、星海图（OpenGalaxea）、ANYbotics、星动纪元（roboterax）、傅利叶（FFTAI）、松延动力（pndbotics）。

背景资料：[UnifoLM-WLA README](https://github.com/unitreerobotics/unifolm-wla)、[sonic_for_a3 README](https://github.com/AgibotTech/sonic_for_a3)、[FluxVLA 技术报告 arXiv:2609.17210](https://arxiv.org/abs/2609.17210)。

**统计周期：** 2026 年 9 月自然月：2026-09-01 00:00 至 2026-10-01 00:00（北京时间），环比取 8 月同口径。

## 二、数据呈现

### 2.1 各家动作

9 月有 4 家企业新开了仓库，共 14 个；模型与全身控制类新仓上线即获关注，工具与基础类新仓首月热度较低。

### 2.2 九家公司 star 增长

![9 月 star 净增：宇树 +846 居首，LimX（含 FluxVLA）约 +143 列第三](images/star-growth-by-company-2026-09.png)

![9 月新增 star 来源分解：宇树一家 849，LimX 六成靠 FluxVLA](images/star-sources-by-repo-2026-09.png)



### 2.3 社区活跃度

**解读**：9 月开源社区的互动主要围绕新模型发布和可训练的仓库展开，各家社区规模与节奏差异明显。

1. **新模型发布是本月社区讨论的主要来源。** 宇树 26 个新 issue 中有 9 个集中在 9 月新发布的 UnifoLM-WLA，其中多数关心模型权重与部署代码的开放节奏。这反映出开发者对“可直接跑起来”的完整开源模型有强烈需求。

2. **fork 集中在仿真与训练类仓库。** 宇树 fork 最多的是 unitree_mujoco、unitree_rl_mjlab、unifolm-wla、unitree_rl_lab；星海图 17 个新 fork 中 14 个来自 GalaxeaVLA；云深处最多的是 rl_training。开发者 fork 的主要目的是在自己的环境里训练和复现策略。

3. **第三方评测开始覆盖主流机型。** 本月有外部 benchmark 项目在宇树的 RL 训练仓库下提交评测结果，说明开源机器人策略正在被放到统一标准下比较，机型是否进入通用仿真库与评测框架将越来越重要。

4. **社区活跃度分化。** 宇树每月新 fork 超过 200 个，约为其余 7 家之和的 2.7 倍；傅利叶、松延动力、星动纪元 9 月没有新的 issue 或 PR。

注：issue / PR 统计未区分企业内部与外部贡献者。

### 2.4 热门与新开源项目

- 版本发布：宇树 unitree_sdk2_rs v0.2.0 / v0.3.0、智元 agillink_omnihand_sdk v1.1.9、FluxVLA v0.1.5（9-11）。

**解读**：本月热门项目集中在基础模型、训练与仿真工具链、人形全身控制三个方向。

1. **基础模型与 VLA 是增长主力。** 榜单 13 个项目中有 5 个属于基础模型、VLA 或世界模型（unifolm-wla、FluxVLA、unifolm-vla、unifolm-world-model-action、GalaxeaVLA），合计约 437 star，占榜单总增量的一半。基础模型正在从单个项目走向系列化：宇树 UnifoLM 已覆盖世界模型、VLA、WLA 三类，分别发布于 2025 年 9 月、2026 年 1 月和 9 月。

2. **训练与仿真工具链是长期刚需。** unitree_mujoco、unitree_rl_lab、unitree_rl_gym、unitree_rl_mjlab、genie_sim 都是发布半年以上的仓库，9 月仍各增长 44–73 star。开发者拿到机器人后的第一步往往是在仿真里训练策略，这类仓库的热度不依赖新发布。基于 MuJoCo / mjlab 的训练仓库在多家企业中都已出现。

3. **存量项目持续贡献。** 榜单中 9 月新建的 unifolm-wla、sonic_for_a3 合计 261 star，约占榜单增量的 30%；其余 11 个为已有仓库。头部企业的存量项目仍在持续吸引新用户。

## 三、行业趋势

具身智能开源正在从“发布机器人配套代码”转向“以模型为核心、以生态为壁垒”的新阶段，同时头部集中度持续上升。

### 开源重心从运动控制转向具身基础模型

本月增长最快的项目中，基础模型、VLA 和世界模型占了一半热度。宇树 UnifoLM 已形成世界模型、VLA、WLA 三条线，智元有 ACoT-VLA 和 Genie Envisioner 世界模型，星海图的增长几乎全部来自 GalaxeaVLA。过去以 SDK、ROS 包为主的开源内容热度靠后。模型正在成为各家开源的核心展示窗口。

### 人形控制走向“动作数据驱动 + 通用框架适配”

至少 3 家在 9 月开放了动作模仿、动作重定向或全身控制仓库（智元 sonic_for_a3、云深处 mimic / retarget、LimX luna-beyondmimic / GMR）。sonic_for_a3 直接把 NVIDIA 的 SONIC 适配到自家机型，一周获 62 star。人形控制正在从各家自研策略，转向基于人体动作数据和公共框架做机型适配，开发者可以在不同机器人之间复用同一套方法。

### 仿真训练成为开发者上手首站

fork 最多的仓库几乎都是仿真和 RL 训练类，unitree_mujoco、unitree_rl_lab、genie_sim 等老仓库在没有新发布的情况下每月仍稳定增长。训练框架呈 Isaac Lab 与 MuJoCo / mjlab 双轨并行，多家都同时维护两套训练仓库。对开发者来说，“能否在仿真里快速跑起来”已成为选择机器人平台的重要因素。

### 头部集中加剧，梯队分化明显

宇树一家占 8 家（不含 LimX）合计增量的 69%；第二梯队（智元、LimX、云深处、星海图）月增 50–180 star；另有 3 家 9 月几乎没有公开活动。

宇树的领先不只靠硬件保有量，还靠生态覆盖：它为 LeRobot、Isaac Lab、MuJoCo、ROS 等主流框架都提供了官方适配，并有 6 款机型被 [MuJoCo Menagerie](https://github.com/google-deepmind/mujoco_menagerie) 收录，其余企业最多 2 款。被公共工具默认支持，正在把硬件优势放大为开发者优势。

### “完整开放”成为开发者的核心诉求

新模型发布后，社区讨论集中在权重、部署代码和训练脚本是否完整开放。开发者已不满足于论文加演示视频，而是要求“拿来就能在自己的机器人上跑”。开放的完整度，将直接影响一个项目能否从短期热度转为长期使用。

### 仓库发布不天然带来热度，需要配合宣发

9 月各家共新开 14 个仓库，只有 unifolm-wla 和 sonic_for_a3 获得了明显关注（合计 261 star），其余 12 个合计仅 10 star。这两个仓库都伴随新模型或新机型的对外发布。FluxVLA 在新版本发布、技术报告上线的那一周，日均 star 增长是前后时段的两倍多。

GitHub 上的自然流量更多流向已经有热度的老仓库，新仓库很难被自动发现。演示视频、技术报告、社交媒体和社区渠道的同步发布，是新项目获得第一批用户的关键。不过这一判断目前只有少数案例支撑，各家的宣发力度也无法从公开数据中量化。

**注：**以上趋势基于一个月的 GitHub 公开数据归纳，将在后续月报中持续验证。

