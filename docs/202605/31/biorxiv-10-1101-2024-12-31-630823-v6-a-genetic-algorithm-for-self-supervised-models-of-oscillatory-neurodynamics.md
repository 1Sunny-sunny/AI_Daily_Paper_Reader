---
title: A genetic algorithm for self-supervised models of oscillatory neurodynamics
title_zh: 用于自监督振荡神经动力学模型的遗传算法
authors: "Nejat, H., Sherfey, J., Bastos, A. M."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.1101/2024.12.31.630823v6.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 拟合振荡神经动力学的遗传算法
tldr: 针对预测处理理论中神经模型难以兼顾自监督计算与振荡动态、且手动调参繁重的问题，本文提出遗传随机delta规则（GSDR），一种进化优化框架，可自动将非线性神经模型拟合至电生理目标。GSDR在简化优化及视觉皮层放电率、频谱比率等真实spike网络目标上，能有效搜索参数空间、减少手动调参，并再现预测路由相关的谱与电路表型。该框架不限于特定模型类，为振荡神经模型的多目标探索提供了方法论。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有预测处理模型在实现自监督计算时往往忽略振荡spike动态，或生物物理spike模型需大量手动调参，亟需自动化优化方法。
method: 提出遗传随机delta规则（GSDR），一种进化优化框架，用于拟合非线性神经模型至放电率、频谱比率等电生理目标。
result: GSDR在简化优化和猕猴视觉皮层spike网络目标上，成功搜索约束参数空间，减少手动调参，并再现了与预测路由相关的gamma动态及频谱特征。
conclusion: GSDR为振荡神经模型的多目标探索提供了灵活且无需手动调参的方法论框架，有助于研究预测处理理论的神经机制。
---

## 摘要
预测处理理论提出，大脑通过减少内部生成预测与外部感觉信号之间的差异来构建其环境的内部模型。先前的工作已将这些过程与gamma频段（40-100 Hz）和alpha/beta频段（10-30 Hz）的振荡活动联系起来。当前的计算方法面临权衡：抽象的预测处理模型可以实现自监督计算，但通常忽略了振荡的发放动态；而生物物理约束的发放模型能够产生神经节律，但往往需要大量的手动调参。在此，我们引入了遗传随机delta规则（GSDR），这是一种将非线性神经模型拟合到电生理目标的进化优化框架。我们首先在简化的优化设置中评估GSDR，然后将其应用于涉及发放率、beta/gamma频谱比以及来自视觉皮层的经验性猕猴刺激诱发gamma动态的发放网络目标。我们证明，GSDR能够搜索受约束的突触参数空间，减少对手动调参的依赖，并重现与预测路由相关的频谱和回路级表型。我们还使用Izhikevich仿真作为模型类鲁棒性分析，表明该方法不限于原始的霍奇金-赫胥黎式实现。这些结果将GSDR定位为一种用于振荡神经模型多目标探索的方法论框架。

## Abstract
Predictive processing theories propose that the brain builds internal models of its environment by reducing the discrepancy between internally generated predictions and external sensory signals. Prior work has linked these processes to oscillatory activity in gamma (40-100 Hz) and alpha/beta (10-30 Hz) frequency ranges. Current computational approaches face a trade-off: abstract predictive-processing models can implement self-supervised computations but often omit oscillatory spiking dynamics, whereas biophysically constrained spiking models can generate neural rhythms but often require extensive manual tuning. Here, we introduce the Genetic Stochastic Delta Rule (GSDR), an evolutionary optimization framework for fitting nonlinear neural models to electrophysiological objectives. We first evaluate GSDR in simplified optimization settings, then apply it to spiking-network objectives involving firing rates, beta/gamma spectral ratios, and empirical macaque stimulus-evoked gamma dynamics from visual cortex. We show that GSDR can search constrained synaptic parameter spaces, reduce reliance on manual tuning, and reproduce spectral and circuit-level phenotypes associated with predictive routing. We also used Izhikevich simulations as a model-class robustness analysis, showing that the approach is not limited to the original Hodgkin-Huxley-style implementation. These results position GSDR as a methodological framework for multi-objective exploration of oscillatory neural models.