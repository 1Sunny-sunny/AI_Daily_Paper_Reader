---
title: "Beyond Phase Estimation: A Multidimensional Gating Framework for Robust Real-Time Closed-Loop Neural Stimulation"
title_zh: 超越相位估计：一种用于鲁棒实时闭环神经刺激的多维门控框架
authors: "Zheng, W., Shen, L., Han, B."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.26.727783v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 用于实时闭环神经刺激的多维门控框架
tldr: 神经振荡相位虽常用于实时闭环刺激的控制变量，但其在严格因果和噪声条件下的可靠性未经系统验证。本研究提出多维门控框架（MGF），一个与估计器无关的插件模块，通过瞬时幅度、窄带信噪比和频谱峰值比在因果窗口内筛选有效相位。在静息态EEG数据上，MGF显著降低相位分散并抑制灾难性错误，而无门控方法则出现系统失败，证明了该框架可增强实时刺激的鲁棒性。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经振荡相位在闭环刺激中广泛使用，但缺乏在因果约束和噪声条件下有效性的系统检验。
method: 提出多维门控框架（MGF），基于瞬时幅度、窄带信噪比和频谱峰值比在严格因果窗口内对相位信息进行准入控制。
result: 在EEG数据集上，MGF显著降低了相位分散，并抑制了灾难性相位错误，而无门控方法出现系统性失败。
conclusion: MGF作为一种即插即用模块，可有效提升实时闭环神经刺激中相位控制的鲁棒性。
---

## 摘要
神经振荡相位被广泛用作实时闭环刺激中的控制变量，然而其在严格因果约束和噪声条件下的有效性很少被系统性地检验。我们引入了一种多维门控框架（MGF），这是一个即插即用且与估计器无关的模块，通过在严格因果窗口内评估瞬时振幅、窄带信噪比（SNR）和频谱峰值比（PR）来决定是否允许相位信息进入控制。我们使用公开静息态EEG数据集上的因果流式重放，对基于希尔伯特的相位估计和端点校正希尔伯特估计在有无MGF的情况下进行了基准测试。在可行受试者中，MGF显著降低了两种估计器的相位分散，同时鲁棒地抑制了灾难性相位误差。相比之下，未采用门控的方法在相同条件下表现出系统性失效。

## Abstract
Neural oscillatory phase is widely used as a control variable in real-time closed-loop stimulation, yet its validity under strict causal constraints and noisy conditions has rarely been systematically examined. We introduce a Multidimensional Gating Framework (MGF), a plug-in and estimator-agnostic module that determines whether phase information should be admitted into control by evaluating instantaneous amplitude, narrowband signal-to-noise ratio (SNR), and spectral peak ratio (PR) within a strictly causal window. Using causal streaming replay on a public resting-state EEG dataset, we benchmarked Hilbert based phase estimation and endpoint-corrected Hilbert estimation with and without MGF. Among feasible subjects, MGF significantly reduced phase dispersion for both estimators, while robustly suppressing catastrophic phase errors. In contrast, ungated approaches exhibited systematic failures under the same conditions.