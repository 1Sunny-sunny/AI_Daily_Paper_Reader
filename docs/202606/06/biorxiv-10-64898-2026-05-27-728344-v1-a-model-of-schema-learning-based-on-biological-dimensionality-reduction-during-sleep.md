---
title: A model of schema learning based on biological dimensionality reduction during sleep
title_zh: 基于睡眠期间生物降维的图式学习模型
authors: "Yoshida, K., Shimizu, G., Kinoshita, Y., Inokuchi, K., Toyoizumi, T."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.27.728344v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 通过降维和流形对齐建模神经表征
tldr: 针对图式形成与迁移的神经机制不明，本文提出基于睡眠中生物降维的理论模型：通过重放驱动的Hebbian非线性降维，将高维输入重组为低维流形，并借助流形对齐实现跨任务表征共享，从而复现快速学习、睡眠依赖泛化及组合重组等核心认知能力。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示图式学习背后的计算和神经回路机制。
method: 构建了重放驱动的Hebbian非线性降维与流形对齐的理论模型。
result: 模型复现了快速迁移学习、睡眠依赖的传递推理泛化和图式组合解决新任务等关键现象。
conclusion: 睡眠中低维图式的形成、对齐和重组可能是支持未来学习的核心神经机制。
---

## 摘要
将已学知识重新组织为概括性表征并将其迁移到未来学习中，是认知的重要方面，通常被描述为图式的形成和使用。然而，这些过程背后的计算和神经回路机制仍不明确。本文提出一个理论模型，其中图式通过低维神经表征的形成和对齐而出现。在该模型中，高维输入模式通过重放驱动的赫布式非线性降维被重组为低维流形。流形对齐将具有共享任务结构的表征映射到共同格式，使下游读出回路能够在不同任务间复用。该模型捕捉了图式学习的三个核心特征：通过复用先前经验的低维表征快速学习类似任务；在传递推理中通过睡眠依赖的泛化观察到未呈现的关系；以及通过图式的组合性重组解决新任务。综上，这些结果揭示了形成、对齐和重组低维图式以支持未来学习的一种潜在神经机制。

## Abstract
Reorganizing learned knowledge into generalized representations and transferring it to future learning are essential aspects of cognition, often described as schema formation and use. However, the computational and circuit mechanisms underlying these processes remain unclear. Here, we propose a theoretical model in which schemas emerge through the formation and alignment of low-dimensional neural representations. In this model, high-dimensional input patterns are reorganized into low-dimensional manifolds through replay-driven Hebbian nonlinear dimensionality reduction. Manifold alignment simultaneously maps representations with shared task structure onto a common format, enabling downstream readout circuits to be reused across tasks. The model captures three core features of schema learning: rapid learning of similar tasks by reusing low-dimensional representations from prior experience, sleep-dependent generalization to unobserved relationships in transitive inference, and compositional recombination of schemas to solve novel tasks. Together, these results suggest a potential neural mechanism for forming, aligning, and recombining low-dimensional schemas to support future learning.