---
title: Using Disinhibition versus Direct Control in a Spiking Neural Model of Dopamine-Driven Reinforcement Learning
title_zh: 在多巴胺驱动的强化学习脉冲神经模型中对比去抑制与直接控制
authors: "Sautto, R., Cuperlier, N., Manos, T., Belkaid, M."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.22.727086v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 在dopamine驱动的强化学习的脉冲神经模型中比较去抑制和直接控制
tldr: 本研究针对多巴胺驱动的强化学习，模拟并比较了直接控制与去抑制两种脉冲神经网络模型。在3臂老虎机任务中，去抑制模型展现出更强的鲁棒性和更好的学习性能，表明尽管结构更复杂，但其在操作环境中具有优势，为理解大脑决策机制和类脑系统设计提供了启示。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究多巴胺能控制的直接投射与去抑制模式各自的计算与功能优势。
method: 构建并仿真仅基于去抑制或直接兴奋/抑制的脉冲神经网络模型，并在3臂老虎机任务中评估学习表现。
result: 直接整合模型对输入信号更敏感且易受干扰，而去抑制模型在异步不规则放电下学习效果更佳。
conclusion: 去抑制控制虽不简约，但在实际运行中比直接控制更具优势，对决策脑回路研究有参考价值。
---

## 摘要
多巴胺能信号在价值学习与决策中起着核心作用。已有观察表明，向中脑多巴胺能神经元投射的通路具有不同的连接模式，其中一些涉及直接的兴奋性投射，而另一些则涉及去抑制。然而，这些模式对多巴胺控制的不同贡献，以及它们的计算和功能优势仍不清楚。在本文中，我们模拟并评估了两种完全基于脉冲的多巴胺能控制神经模型，一种仅基于去抑制，另一种仅基于直接的抑制性和兴奋性投射。我们从工程特性、产生的脉冲发放模式以及在3臂老虎机任务中成功习得期望价值表征的能力等方面对这两种模型进行了比较。我们发现，两种模型都能在异步不规则放电状态下运行，但直接整合模型的放电模式对干扰的抵抗力较弱，且对输入信号更敏感。此外，去抑制模型在学习任务中表现更佳。我们得出结论：虽然直接模型更为简约，但基于去抑制的控制在操作环境中仍具有优势。我们的结果对决策脑回路的研究以及类脑系统的设计都具有指导意义。

## Abstract
Dopaminergic signalling is central to value learning and decision making. It has been observed that multiple pathways with different patterns of connectivity project to midbrain dopaminergic neurons, some involving direct excitatory projections while others involve disinhibition. However, the respective contributions of these patterns to dopamine control, and their computational and functional advantages remain unclear. In the current work we simulate and evaluate two fully spiking neural models of dopaminergic control, based either solely on disinhibition, or solely on direct inhibitory and excitatory projections. We compare these models in terms of their engineering properties, their resulting spiking profiles, and their ability to successfully acquire representations of expected value in a 3-armed bandit task. We find that both models are able to operate at an asynchronous-irregular firing regime, but that the firing profile of the direct integration model is less resilient to disruption and more sensitive to incoming signals. In addition, the disinhibition model performs better in the learning task. We conclude that while the direct model is more parsimonious, disinhibition-based control remains advantageous in the operational context. Our results have implications for the study of decision-making brain circuits as well as for the design of brain-inspired systems.