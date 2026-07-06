---
title: A unified theory of context-conditioned efficient and predictive coding
title_zh: 上下文条件化高效与预测编码的统一理论
authors: "Tavoni, G."
date: 2026-07-06
pdf: "https://www.biorxiv.org/content/10.1101/2025.02.24.639817v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 上下文条件高效和预测编码的统一理论
tldr: 神经编码受多模态背景影响，本文提出统一高效编码与预测编码的理论，证明背景条件高效编码等价于预测编码：背景提供期望，局部神经元编码预测偏差，并通过循环连接白化残差。该框架解释了跨模态抑制等实验现象，为分布式神经编码提供原则基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 局部感觉电路如何在利用多模态背景信息的同时高效编码其输入。
method: 通过分析推导将背景条件高效编码映射为可解释的预测编码算法，并建立数学等价性。
result: 证明了背景条件高效编码与预测编码的等价性，统一解释了跨模态抑制和多模态感受野等实验现象。
conclusion: 该理论将编码目标、电路机制与现象统一，为理解背景如何塑造分布式神经表征提供了原则性基础。
---

## 摘要
感觉处理并非孤立发生：特定感觉模态中神经元所表征的内容，会受到来自其他感觉、动作和行为背景信号的影响。这种背景依赖性给神经编码理论提出了一个根本问题：电路如何在利用大脑其他部分可用信息的同时，高效地编码其局部输入？在此，我们发展了一个统一的高效与预测编码理论，揭示了多模态背景信息如何优化局部感觉电路内的表征。我们通过分析证明，高效编码方案可映射为一种可解释的神经算法：背景信号为局部电路提供关于感觉输入的预期，局部神经元编码与这些预期的偏差，而循环相互作用则对残差信号进行白化。这一结果建立了背景条件化高效编码与预测编码之间的数学等价性，揭示了预测计算可以从背景引导的高效输入压缩中产生。由此得到的框架既不同于单一模态内的经典冗余削减，也不同于层级贝叶斯推断。该理论解释并统一了多种实验现象，包括对预期输入的跨模态反应抑制以及感觉运动、视听、视觉-嗅觉和听觉-体感通路中的多模态感受野，同时将经典的单模态编码效应作为极限情况予以复现。通过将编码目标、电路机制和实验观察到现象联系在单一分析框架中，这项工作为理解分布式神经系统如何利用背景塑造局部表征提供了原则性基础。

## Abstract
Sensory processing does not occur in isolation: what neurons represent in a given sensory modality is shaped by signals from other senses, actions, and behavioral context. This context dependence raises a fundamental question for theories of neural coding: how can circuits efficiently encode their local input while using information available elsewhere in the brain? Here we develop a unified theory of efficient and predictive coding that shows how multimodal contextual information can optimize representations within a local sensory circuit. We demonstrate analytically that the efficient-coding solution maps onto an interpretable neural algorithm: contextual signals provide expectations about the sensory input to the local circuit, local neurons encode deviations from those expectations, and recurrent interactions whiten the residual signals. This result establishes a mathematical equivalence between context-conditioned efficient coding and predictive coding, revealing that predictive computations can emerge from efficient input compression guided by context. The resulting framework is distinct from both classical redundancy reduction within a single modality and hierarchical Bayesian inference. The theory explains and unifies diverse experimental phenomena, including cross-modal suppression of responses to predicted inputs and multimodal receptive fields across sensorimotor, audiovisual, visual-olfactory, and auditory-somatosensory circuits, while recovering classical unimodal coding effects as limiting cases. By linking coding objectives, circuit mechanisms, and experimentally observed phenomena within a single analytical framework, this work provides a principled foundation for understanding how distributed neural systems use context to shape local representations.