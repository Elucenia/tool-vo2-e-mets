<!-- ELUCENIA technical documentation · vo2-e-mets · zh · no clinical/professional/rights approval -->

# 估算 VO₂、METs 与功能能力

[条件、来源与许可](https://elucenia.org/zh/tools/vo2-e-mets)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 运动时间（Bruce）

`tempo`

min · 范围: 1–27

### 年龄

`idade`

年 · 范围: 15–100

### 性别

`sexo`

- `F` — 女性
- `M` — 男性

### 是否经常身体活动？

`ativo`

- `0` — 否
- `1` — 是

## 方法版本

Foster 1984 Bruce多项式；Bruce 1973年龄/活动VO₂；MET=VO₂/3.5；FAI

## 已记录的公式

VO₂ (Foster, Bruce): 14.8 − 1.379 × t + 0.451 × t² − 0.012 × t³ (mL/kg/min; t为分钟)

METs = VO₂ ÷ 3.5

预计VO₂ (Bruce): 久坐男性 57.8 − 0.445 × 年龄; 活跃男性 69.7 − 0.612 × 年龄; 久坐女性 42.3 − 0.356 × 年龄; 活跃女性 42.9 − 0.312 × 年龄

功能损害 (FAI) = (预计VO₂ − 实测值) ÷ 预计VO₂ × 100

## 限制与适用人群

用于估计 VO₂ 的时间必须来自相应的 Bruce 跑台方案，而非任意运动的持续时间。方程给出预测值，不是通过气体分析测得的耗氧量。MET 使用 3.5 mL/kg/min 的约定值，并非测量个体静息代谢。预期运动能力参考值和预后关联具有特定人群范围：Myers 2002 研究的是转诊接受临床测试的男性。不要自动外推至儿童、其他方案或个体死亡风险。

## 参考文献

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
