---
title: Parameter scaling of multivariate Granger causality
title_zh: 多元格兰杰因果性的参数缩放
authors: "Pirenne, T., Florin, E."
date: 2026-06-02
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.01.679714v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 稀疏多变量格兰杰因果关系用于神经因果推断
tldr: 因果推断广泛用于脑信号分析，但基于多元自回归模型的方法在高维数据中面临可扩展性瓶颈。本文提出稀疏多元格兰杰因果性（sMVGC），利用因果连接稀疏性约束搜索空间，并通过参数缩放模拟研究揭示样本数、信号数和模型阶数的二次方影响规律。sMVGC在保持估计准确性的同时提升参数可扩展性，并提供实际分析中的参数范围与模型选择指导。
source: biorxiv
selection_source: fresh_fetch
motivation: 高维脑信号数据导致传统多元自回归因果估计方法可靠性差、计算量无法扩展。
method: 提出稀疏多元格兰杰因果性（sMVGC），基于稀疏因果连接假设约束候选搜索空间，并结合模拟数据探索参数缩放行为。
result: 所有算法均随参数二次方扩展；sMVGC在保持准确性的同时改善可扩展性，且准确推理所需样本量随信号数增加。
conclusion: sMVGC有效缓解高维参数下的可扩展性问题，并提供实际应用的参数选择建议。
---

## 摘要
估计信号间的因果相互作用可为其动力学提供独特见解，且因果推断已广泛应用于电生理数据以阐明大脑通信。多元自回归模型（MVAR）构成了大多数因果估计方法的基础。然而，全脑数据的高维度使得 MVAR 难以可靠估计，而将维度降低到合理范围又会影响到因果推断。为解决这些可扩展性限制，我们开发了稀疏多元格兰杰因果性（sMVGC），这一新方法基于信号间真实因果连接是稀疏的假设，从而约束候选搜索空间并提高可扩展性。为从经验上推动 sMVGC，我们模拟了具有已知因果关系的电生理数据，并建模了样本数、信号数和 MVAR 阶数如何影响当前算法的性能和计算时间。所有算法至少与这些参数呈二次方关系缩放，但它们对信号数与样本数的敏感性不同，且准确推断所需的样本量随信号数增加而增加。在这些发现的指导下，sMVGC 在保持估计精度的同时改善了参数可扩展性，我们为实际分析提供了实用的参数范围和模型选择指导。

## Abstract
Estimating causal interactions between signals provides unique insights into their dynamics, and causal inference has been widely applied to electrophysiological data to elucidate brain communication. Multivariate autoregressive models (MVAR) form the basis of most causal estimation methods. However, the high dimensionality of whole-brain data renders MVARs difficult to estimate reliably, and reducing the dimensions to a reasonable range affects causal inference. To address these scalability limitations, we develop sparse Multivariate Granger Causality (sMVGC), a novel method premised on the assumption that true causal connections between signals are sparse, thereby constraining the candidate search space and improving scalability. To motivate sMVGC empirically, we simulate electrophysiological data with known causalities and model how the number of samples, signals, and MVAR order affect the performance and computation time of current algorithms. All algorithms scale at least quadratically with these parameters, yet differ in their sensitivity to signal versus sample count, and the sample requirements for accurate inference scale with the number of signals. Guided by these findings, sMVGC improves parameter scalability while preserving estimation accuracy, and we provide practical parameter ranges and model selection guidance for real-world analyses.