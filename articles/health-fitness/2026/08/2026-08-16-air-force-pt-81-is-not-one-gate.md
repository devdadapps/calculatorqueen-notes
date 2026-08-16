---
title: "Air Force PT 算出 81.0，为什么还要检查四道门"
date: 2026-08-16
description: "按 2026 USAF 标准 PFRA 版本复算 81.0，并解释总分、分项最低分、WHtR 与适用范围。"
category: "health-fitness"
target_slug: "air-force-pt-calculator"
language: "zh-CN"
ownership: "CalculatorQueen 第一方内容"
verification: "2026-08-16"
status: "published"
---

# Air Force PT 算出 81.0，为什么还要检查四道门

结果先说：一组 23 岁、male chart、海拔低于 5,250 英尺的标准 USAF Total Force 示例，45 次一分钟俯卧撑、45 次一分钟仰卧起坐、2 英里 15:00、身高 70 英寸、腰围 35 英寸，得到 **81.0/100，Satisfactory**。

但 Air Force PFRA 不是“总分过 75 就收工”的单闸门。总分、受测体能分项最低要求、身体组成分支和适用人群都要同时成立。把 81 写得很大，不能把脚注吓跑。

## 先锁定版本，不跨表借分

本文只讨论 2026 年 7 月 1 日起生效的标准 USAF PFRA：采用 2026 年 3 月最终计分表和 2026 年 3 月 24 日版 AFMAN 36-2905，适用于页面明确支持的标准 Total Force、海拔低于 5,250 英尺情形。

它不覆盖 AFSPECWAR/EOD、Space Force、训练或职业专用标准，也不套用高海拔修正表。政策、表格或个人正式记录若有更新，以当前官方文件、管理员和 myFitness 为准；这篇文章与工具均为非官方规划复核，不是命令决定或正式 fitness record。

## 把 81.0 拆成四张收据

页面按已达到年龄组与 male/female chart 查表。上述示例落在 Under 25 male 列，四项结果为：

- 45 次一分钟俯卧撑：7.5 分；
- 45 次一分钟仰卧起坐：8.5 分；
- 2 英里 15:00：46.0 分；
- 腰高比：19.0 分。

腰高比不是常规四舍五入。按官方记录的 0.5 英寸增量输入，先算并向下截断到两位小数：

$$
WHtR=\operatorname{truncate}_2(35/70)=0.50
$$

0.50 对应 19 分。再把四张收据相加：

$$
7.5+8.5+46.0+19.0=81.0
$$

2026 年 8 月 16 日核对 [CalculatorQueen 的 Air Force PT Calculator](https://calculatorqueen.com/calculators/air-force-pt-calculator) 实时默认结果，页面显示 81.0/100、Satisfactory，并逐项显示 7.5、8.5、46.0、19.0；手算与页面一致。

## 75 分是一道门，不是万能钥匙

标准无豁免路径的规划综合分为：

$$
S=100\times\frac{\text{非豁免项目所得分}}{\text{非豁免项目可得分}}
$$

通常可得 100 分，综合分需至少 75；同时受测 cardio 至少 35 分、strength 至少 2.5 分、core 至少 2.5 分。也就是说，某人即使靠其他项目把合计推过 75，只要一个受测体能项目未达最低值，结果仍不是通过。总分负责汇总，最低分负责兜底，两者没有谁能替谁值夜班。

90 分及以上在无相关豁免且满足条件时才进入 Excellent；81.0 因而是 Satisfactory。类别不是对训练质量的完整评价，只是按当前规则对这次正式输入的分类。

发生支持范围内的豁免时，分母也会变化，而不是把空白项目机械记成零。页面用“非豁免项目所得分 ÷ 非豁免项目可得分”重新标准化到 100。这个处理解释了为什么 raw points 与 composite score 可能不再同数；若只抄最后的百分制结果，会看不见究竟哪些项目被计入。规划记录应同时保存项目、表现、分项分、可得总分和豁免依据。

## 两个分支不能靠猜

2 公里步行只适用于当前 AF Form 469 医疗授权、且禁止 2 英里跑与 20 米 HAMR 的情形。通过步行后 cardio 按豁免处理、不计分，并不能获得 Excellent；没有授权时页面会停止，而不是替用户发一张想象中的表格。

身体组成先用管理员记录的最终腰围和身高。若截断后的 WHtR 高于 0.55，且初步 PFRA 不满足标准，才会触发 Tier 2 BFA 分支。BFA 结果必须来自授权的正式评估，不能填家庭体脂秤、自测皮尺或猜测百分比。页面支持的是规则演算，不是医疗资格判断。

## 使用前的停止条件

输入年龄应为测评日已达到年龄；动作次数、秒数和 shuttle 数应是正式计入值；身高与最终腰围应来自管理员程序。若地点达到或超过 5,250 英尺、适用特殊人群表、存在未建模豁免，或者政策版本不是本文所述版本，应停止使用这一结果并转向主管单位的当前官方流程。

页面公式虽有工程测试，仍未获得独立 USAF fitness-policy 专家审查。训练安排、受伤风险、医疗限制、申诉和行政后果都不能由这个数字决定。最终正式结果以 myFitness 和有权人员记录为准。

临界点附近尤其不应拿家庭测量替代正式输入。身高与腰围按页面要求使用管理员记录的半英寸增量，WHtR 采用截断而非四舍五入；一次自测差异可能把数值送到另一行。规划时可以观察“如果正式输入落在相邻档位会怎样”，却不能把较有利的一档当作已经取得的官方结果。

## 官方来源与披露

- [U.S. Air Force：Culture of Fitness](https://www.af.mil/Fitness/)，确认新标准自 2026 年 7 月 1 日生效、四类分值及官方 DAFMAN/计分表入口。
- [Air Force Personnel Center：AFMAN 36-2905，2026 年 3 月 24 日版](https://www.afpc.af.mil/Portals/70/documents/FITNESS/afman36-2905.pdf)，用于适用范围、最低要求、豁免、WHtR 与正式记录规则。
- [Air Force Personnel Center：Final USAF PFRA Scoring Charts](https://www.afpc.af.mil/Portals/70/documents/FITNESS/Tab%202.%20PFRA%20Scoring%20Charts%2C%20cao%2017%20Mar%2026.pdf)，用于各年龄与 chart 的分值门槛。
- [Secretary of the Air Force Public Affairs：2026 测评时间线](https://www.af.mil/News/Article-Display/Article/4371953/air-force-updates-fitness-test-requirements/)，确认诊断过渡期和 7 月 1 日恢复正式测试。

本文是 CalculatorQueen 团队依据自有计算合同、实时页面输出和 Department of the Air Force 一手资料编写的第一方内容。AI 协助整理结构与复核加总；编辑负责版本、来源、高影响边界及非官方用途说明。本文不提供医疗建议，也不冒充 Air Force 官方发布。
