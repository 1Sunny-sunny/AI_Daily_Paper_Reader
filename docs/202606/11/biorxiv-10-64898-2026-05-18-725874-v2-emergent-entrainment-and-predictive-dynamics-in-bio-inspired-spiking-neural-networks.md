---
title: Emergent Entrainment and Predictive Dynamics in Bio-Inspired Spiking Neural Networks
title_zh: 生物启发脉冲神经网络中的涌现夹带与预测动力学
authors: "Manriquez, R., Kotz, S. A., Ravignani, A., de Boer, B."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.18.725874v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 尖峰神经网络用于听觉节律夹带
tldr: 为理解节奏感知的神经计算基础，该研究构建了一种生物启发的脉冲神经网络框架，通过在听觉夹带任务上训练，分析了网络发放率和膜电位动态。结果显示，网络自发产生与节拍锁相的内生振荡及预期去极化，无需显式振荡器，表明脉冲神经网络能自然涌现预测编码和节奏夹带特性，为探索生物脑计算机制提供了有力工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 需要构建连接算法功能与生物实现的模型，以揭示节奏感知的计算基底。
method: 采用递归脉冲神经网络在听觉夹带任务上训练，并通过分析发放率和膜电位波动来表征潜在动态。
result: 模拟神经群体表现出对节拍的相位锁定的内生振荡，且突触可塑性自然产生预期动态。
conclusion: 脉冲神经网络可作为强有力的探索工具，揭示预测编码和节奏夹带如何从生物神经计算的内在约束中涌现。
---

## 摘要
节律是人类音乐、言语和许多其他人类活动的关键构建模块。理解节律感知的计算基础需要能够沟通算法功能与生物学实现的模型。我们提出一个基于生理学的脉冲神经网络（SNN）框架，以研究听觉节律的涌现表征与解析。利用一个在听觉夹带任务上训练的循环SNN架构，我们通过分析发放率和膜电位波动来刻画网络的潜在动力学。我们的结果表明，模拟的神经群体展现出对刺激节拍的锁相，内源性振荡由节律输入所驱动。我们进一步表明，以刺激前去极化为特征的预期动力学，从网络的突触可塑性和时间整合特性中自然涌现，而非来自显式定义的振荡器。通过将网络层视为皮层群体的功能类比，该框架允许应用实验电生理学中典型的光谱和信息论分析。更一般地，该方法将SNNs确立为一种健壮的探索工具，用于揭示预测编码和节律夹带如何从生物神经计算的内在约束中产生。

## Abstract
Rhythm is a key building block of human music, speech and numerous other human activities. Understanding the computational substrates of rhythm perception requires models that bridge algorithmic function with biological implementation. We propose a physiologically grounded spiking neural network (SNN) framework to investigate the emergent representation and interpretation of auditory rhythms. Utilizing a recurrent SNN architecture trained on an auditory entrainment task, we characterize the network's latent dynamics through the analysis of firing rates and membrane potential fluctuations. Our results demonstrate that simulated neural populations exhibit phase-locking to the stimulus beat, with endogenous oscillations driven by rhythmic input. We further show that anticipatory dynamics--characterized by pre-stimulus depolarization--emerge naturally from the network's synaptic plasticity and temporal integration properties, rather than from explicitly defined oscillators. By treating network layers as functional analogs of cortical populations, this framework allows for the application of spectral and information-theoretic analyses typical of empirical electrophysiology. More in general, this approach establishes SNNs as robust exploratory tools for uncovering how predictive coding and rhythmic entrainment arise from the inherent constraints of biological neural computation.