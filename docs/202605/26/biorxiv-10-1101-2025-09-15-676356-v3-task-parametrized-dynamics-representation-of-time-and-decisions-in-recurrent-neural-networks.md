---
title: "Task-Parametrized Dynamics: Representation of Time and Decisions in Recurrent Neural Networks"
title_zh: 任务参数化动力学：循环神经网络中时间与决策的表示
authors: "Jarne, C. G., Yoon, R., Eissa, T., Kilpatrick, Z., Josic, K."
date: 2026-05-22
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.15.676356v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: RNN时间动态分析用于决策任务中的时间表征
tldr: 该研究探究递归神经网络（RNN）如何内部表示时间以在延迟后启动决策，通过训练RNN执行二元决策、上下文依赖决策和感知整合等时间需求递增的任务，并分析网络连接、特征值谱、读取对齐和低维轨迹，发现网络可收敛到振荡或非振荡等性质不同但行为相当的动力学解，群体活动保持低维且分布于多个单元，读取对齐随任务时期动态变化，在符号对称任务中网络保持近似符号翻转等变性，表明时间和决策计算能以多种动力学机制实现，体现生物神经系统的简并性和功能冗余。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究RNN如何内部表示流逝的时间以在习得的延迟后发起反应。
method: 训练RNN在延迟决策任务上逐步增加时间要求，并通过连接统计、特征值谱、读取对齐和低维群体轨迹分析网络动力学。
result: 网络收敛到振荡、斜坡/衰减等不同但行为等价的动力学解；群体活动低维分布；读取对齐在反应前主要处于读取零空间，靠近决策时与输出对齐；符号对称任务中保持近似符号翻转等变性。
conclusion: 时间和决策相关计算可通过多种动力学机制涌现，同时维持结构化低维表示和可比行为，反映了生物系统的简并性与功能冗余原则。
---

## 摘要
循环神经网络（RNN）如何在内部表征经过的时间，从而在习得的延迟后发起反应？为探讨这一问题，我们在延迟决策任务上训练了RNN，这些任务的时间要求逐步增加，包括二元决策、情境依赖决策和知觉整合。我们通过连接统计、特征值谱、读出对齐和低维群体轨迹分析了训练后的网络。在不同任务中，网络收敛到在性质上不同但在行为上相当的动力学解，包括振荡和非振荡（渐变/衰减）模式，符合解的简并性。群体活动保持低维，并分布于各个循环单元，而非局限于个别神经元。读出对齐具有强烈的阶段依赖性：在反应产生之前，活动主要在读出零空间中演化，并在决策时间附近与输出维度的对齐程度增加。在符号对称任务中，尽管各试次间存在独立的噪声扰动，训练后的网络仍保留了一种近似的符号翻转等变性，这源自架构和训练的对称性，从而在刺激符号相反时产生镜像的群体反应。总之，这些结果表明，时间与决策相关的计算可以通过多种动力学模式涌现，同时保持结构化的低维表征和相当的行为表现，这反映了生物系统中简并性和功能冗余的原理。

## Abstract
How do recurrent neural networks (RNNs) internally represent elapsed time to initiate responses after learned delays? To address this question, we trained RNNs on delayed decision-making tasks with progressively increasing temporal demands, including binary decisions, context-dependent decisions, and perceptual integration. We analyzed trained networks using connectivity statistics, eigenvalue spectra, readout alignment, and low-dimensional population trajectories. Across tasks, networks converged to qualitatively distinct but behaviourally comparable dynamical solutions, including oscillatory and non-oscillatory (ramping/decaying) regimes, consistent with solution degeneracy. Population activity remained low-dimensional and distributed across recurrent units rather than localized to individual neurons. Readout alignment was strongly epoch-dependent: activity evolved largely in the readout-null subspace prior to response generation and became increasingly aligned with the output dimension near decision time. In sign-symmetric tasks, trained networks preserved an approximate sign-flip equivariance inherited from architecture and training symmetry, despite independent noisy perturbations across trials, yielding mirrored population responses across stimulus sign. Together, these results show that temporal and decision-related computations can emerge through multiple dynamical regimes, while maintaining structured low-dimensional representations and comparable behavioural performance, mirroring biological principles of degeneracy and functional redundancy.