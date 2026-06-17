---
title: "Prediction of fMRI activity using vector autoregressive models: a comparison of sparse and low-rank approaches"
title_zh: 基于向量自回归模型的功能磁共振活动预测：稀疏与低秩方法比较
authors: "Tian, X., Gibberd, A., Roy, S., Nunes, M."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731556v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 使用向量自回归模型预测随时间变化的fMRI脑活动
tldr: 本文针对功能MRI研究中向量自回归(VAR)模型因区域数量多导致参数方差高、预测不稳定问题，提出低秩预平滑方法，即在拟合VAR前对观测数据低秩近似，并在个体任务态和静息态数据上与稀疏和无约束估计对比，发现该方法能显著降低预测误差、实现稳健参数估计，合成实验验证其有效性。
source: biorxiv
selection_source: fresh_fetch
motivation: VAR模型在fMRI功能连接分析中参数多、方差高，需鲁棒的参数估计新方法。
method: 先对fMRI观测值进行低秩近似，再拟合VAR模型，超参数在群体水平调优。
result: 低秩预平滑方法提升了个体参数估计的鲁棒性，并显著降低了预测误差，优于稀疏和全估计方法。
conclusion: 低秩预平滑是有效的fMRI功能连接建模策略，可改善个体分析中的预测性能和参数可靠性。
---

## 摘要
向量自回归（VAR）模型历来被用于研究功能磁共振成像（fMRI）所捕捉的脑功能连接。这类模型允许估计大脑各感兴趣区之间的格兰杰因果关系。然而，由于VAR模型的参数数量与区域数的平方成正比，而区域数通常远大于时间观测数，参数估计会呈现高方差。为应对这一挑战，我们提出了一种低秩预平滑方法，在拟合VAR模型前对观测值应用低秩近似。我们利用任务态和静息态条件下的个体被试数据估计模型，并在群体层面调谐超参数。我们的低秩方法与稀疏和无约束估计方法直接比较。预测性能和模型结构的评估表明，我们的预平滑技术能够实现稳健的个体参数估计并显著降低预测误差，这一发现通过已知真实参数的合成实验进一步得到验证。

## Abstract
Vector autoregressive (VAR) models have a history of being used to examine functional connectivity in the brain, as captured by functional MRI studies. Such models allow for an estimation of Granger-causal relationships between regions of interest across the brain. Unfortunately, since the number of parameters in the VAR model scales as the square of the number of regions, and this is typically large compared to the number of temporal observations, these parameter estimates will exhibit high variance. To address this challenge, we introduce a low-rank pre-smoothing method that applies a low-rank approximation to the observations before fitting a VAR model. We estimate these models using individual subject data from both task-based and resting-state conditions, tuning hyperparameters at the population level. Our low-rank approach is directly compared against sparse and unconstrained estimation methods. Evaluations of predictive performance and model structure reveal that our pre-smoothing technique enables robust individual-level parameter estimation and significantly reduces prediction error, a finding further validated by synthetic experiments where the ground-truth parameters are known.