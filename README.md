# 项目A｜负压吸附爬壁机器人（BEETLE 2S 原版复现）

首届特种机器人六周开源复现挑战赛 · 赛道A · 第 2 组

## 团队

| 代号 | 姓名 | GitHub | 主责 |
|---|---|---|---|
| S | 薛锴杰 | @Fearless-x-00 | 组长 / 集成协调 |
| M | 待填 | @taotouzhidai-cmyk | 结构与制造 |
| C | 郭梓泓 | @12567g | 控制与实验 |

## 一句话

复现 Circuit-Digest BEETLE 负压吸附爬壁机器人 **2S 原版方案**：4300KV 电机 + 3 英寸桨在腔体内造负压，
目标是**水平面安全移动 + 可重复的静态吸附力测量 + 实验报告**。垂直爬升须专项审查。

## 当前状态（W1 末）

| 项 | 状态 | 位置 |
|---|---|---|
| 任务书 v1 | 完成 | `docs/requirements.md` |
| 系统图（四条路径） | 完成 | `docs/system_architecture.md` + `docs/img/` |
| 原版基线档案 | 完成 | `docs/upstream-baseline.md` |
| BOM v1 | 完成，价格待询价 | `hardware/hardware_BOM.md` |
| 固件 / 结构 / 实测 | W2 起 | — |

## 快速开始

1. 读 `docs/requirements.md`：目标、验收、分工、风险。
2. 读 `docs/upstream-baseline.md`：原版参数与 5 个已知缺口。
3. 看 `docs/system_architecture.md` 与 `docs/img/system-architecture-2s.png`。
4. 按 `hardware/hardware_BOM.md` 分两批采购。
5. 上电前必须过 `docs/safety-checklist.md`。

## 目录

| 目录 | 内容 |
|---|---|
| `docs/` | 任务书、系统架构、原版基线、安全清单、周报 |
| `cad/` | STEP / STL 与装配图 |
| `hardware/` | BOM、接线、规格、测试台架 |
| `firmware/` | 固件工程与配置模板 |
| `tests/` | 测试清单与验收步骤 |
| `data/` | 原始数据索引、单位、校验 |
| `reports/` | 每周报告、实验记录、失败复盘 |
| `LICENSES/` | 第三方资料与许可证 |

## 六周节点

| 周 | 交付 |
|---|---|
| W1 | 任务书 v1、系统图、BOM v1、仓库；通过 G0 |
| W2 | 低压台架验证双轮、编译与网页命令、断联停车 |
| W3 | 腔体与裙边 CAD、打印测试件、测质量与尺寸 |
| W4 | 授权后测输入功率、压差、有效吸附力 |
| W5 | 两种密封/接触设计对比；水平低速运动与滚动阻力 |
| W6 | 基础控制 + 力学数据 + 版本对比 + 答辩 |

## 来源与致谢

基于 Circuit-Digest 的 BEETLE Wall Climbing Robot。

- 上游：https://github.com/Circuit-Digest/BEETLE-ROBOT
- 锁定提交：`dfad0b544459b171927d50707d58ace401587524`（2026-07-21）
- 许可证：作者在 README 声明 MIT，仓库无 LICENSE 文件；处理见 `LICENSES/README.md`

## 安全声明

本项目涉及 2S 锂电池、高速桨与负压腔体。未经 G0 与专项授权，不进行风机高速运转、整机上墙或垂直爬升；
出现异响、异常电流、通信失联或防护松动，立即停机并报告。
