---
title: A genetic algorithm for self-supervised models of oscillatory neurodynamics
title_zh: 一种用于振荡神经动力学自监督模型的遗传算法
authors: "Nejat, H., Sherfey, J., Bastos, A. M."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.1101/2024.12.31.630823v5.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 用于拟合自监督振荡神经模型的遗传算法
tldr: 本文针对预测处理理论中抽象模型忽略振荡放电动态、而生物物理放电模型需大量手动调节的权衡问题，提出遗传随机Delta规则（GSDR）——一种进化优化框架，可自动将非线性神经模型拟合到电生理目标（如放电率、beta/gamma谱比和猕猴视觉皮层gamma动态），减少手动调参依赖，并再现与预测路由相关的神经动力学，为振荡神经模型的多目标探索提供方法论工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 当前计算模型在自监督预测处理与生物物理振荡动力学之间难以兼顾，需大量手动调节以复现神经活动。
method: 开发遗传随机Delta规则（GSDR），通过进化多目标优化自动搜索突触参数空间，使非线性神经模型匹配电生理目标。
result: GSDR成功搜索受限参数空间，减少手动调节，再现放电率、谱比及猕猴视觉皮层诱发gamma动态，并展示对Hodgkin-Huxley和Izhikevich模型的鲁棒性。
conclusion: GSDR为一有效的多目标优化框架，能系统探索振荡神经模型，促进预测路由相关神经机制的计算研究。
---

## 摘要
预测处理理论提出，大脑通过减少内部生成的预测与外部感官信号之间的差异来构建其环境的内部模型。先前的研究已将这一过程与伽马频段（40-100 Hz）和阿尔法/贝塔频段（10-30 Hz）的振荡活动联系起来。目前的计算方法面临一个权衡：抽象的预测处理模型可以实现自监督计算，但通常忽略了振荡的脉冲动力学，而受生物物理约束的脉冲模型可以产生神经节律，但通常需要大量手动调参。在这里，我们引入了遗传随机增量规则（GSDR），这是一种将非线性神经模型拟合到电生理目标的进化优化框架。我们首先在简化的优化设置中评估GSDR，然后将其应用于涉及放电率、贝塔/伽马频谱比以及来自视觉皮层的经验性猕猴刺激诱发伽马动力学的脉冲网络目标。我们证明，GSDR可以搜索受限的突触参数空间，减少对手动调参的依赖，并重现与预测路由相关的频谱和回路水平表型。我们还使用了Izhikevich模拟作为模型类别鲁棒性分析，表明该方法不限于原始的Hodgkin-Huxley风格实现。这些结果将GSDR定位为一个对振荡神经模型进行多目标探索的方法学框架。

## Abstract
Predictive processing theories propose that the brain builds internal models of its environment by reducing the discrepancy between internally generated predictions and external sensory signals. Prior work has linked these processes to oscillatory activity in gamma (40-100 Hz) and alpha/beta (10-30 Hz) frequency ranges. Current computational approaches face a trade-off: abstract predictive-processing models can implement self-supervised computations but often omit oscillatory spiking dynamics, whereas biophysically constrained spiking models can generate neural rhythms but often require extensive manual tuning. Here, we introduce the Genetic Stochastic Delta Rule (GSDR), an evolutionary optimization framework for fitting nonlinear neural models to electrophysiological objectives. We first evaluate GSDR in simplified optimization settings, then apply it to spiking-network objectives involving firing rates, beta/gamma spectral ratios, and empirical macaque stimulus-evoked gamma dynamics from visual cortex. We show that GSDR can search constrained synaptic parameter spaces, reduce reliance on manual tuning, and reproduce spectral and circuit-level phenotypes associated with predictive routing. We also used Izhikevich simulations as a model-class robustness analysis, showing that the approach is not limited to the original Hodgkin-Huxley-style implementation. These results position GSDR as a methodological framework for multi-objective exploration of oscillatory neural models.