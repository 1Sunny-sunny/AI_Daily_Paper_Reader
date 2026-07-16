---
title: A layer-resolved diagnostic identifies bias-driven decisions in deep neural networks
title_zh: 一种逐层诊断方法识别深度神经网络中的偏差驱动决策
authors: "Nakuci, J."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.16.676625v7.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 层分辨诊断解释神经网络决策
tldr: 现代AI高置信度决策可能由输入无关偏置驱动，而非特征支持，导致信任问题。本文提出偏置主导指数(BDI)，一种层解析度量，将置信度分解为特征支持与偏置支持，量化偏置贡献。实验表明高置信度常与偏置驱动决策共存，BDI可定位偏置影响层，并稳定性能退化。结合BDI与置信度的规则可用于审计。BDI成为跨模型诊断决策构成的通用工具。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-16-676625-v7/fig-001.webp\", \"caption\": \"Table 2. Illustrative examples of BERT completed prompts\", \"page\": 19, \"index\": 1, \"width\": 927, \"height\": 523}]"
motivation: 模型置信度未揭示决策是否由输入特征支持，引发信任问题。
method: 提出偏置主导指数(BDI)，将置信度分解为输入依赖特征支持和输入无关偏移支持，层解析量化偏置的相对贡献。
result: 高置信度可与偏置驱动决策共存，BDI能映射偏置影响层，且偏置成分可抵御读出权重退化。
conclusion: BDI是一种通用诊断工具，能区分特征支持与偏置驱动的决策，适用于多种模型架构。
---

## 摘要
现代人工智能系统可以既准确又自信，但仅凭这一点并不能揭示决策是否得到了输入的良好支持。这带来了信任问题，因为置信度只表明模型的果断程度，而非支持该果断性的依据。在此，我们展示神经网络的置信度可分解为依赖于输入的特征支持和独立于输入的偏置支持。我们通过偏差主导指数（BDI）将这种分解形式化，这是一种逐层的度量，量化独立于输入的偏置对决策边界的相对贡献，从而揭示置信度主要是由特征支持还是由偏差驱动的。在卷积神经网络、视觉Transformer和一个Transformer语言模型中，BDI显示高置信度可以与偏差驱动的决策共存。逐层分析映射了偏差支持在网络深度上的分布位置。扰动分析进一步表明，当读出权重退化时，偏差成分可以稳定性能。最后，我们将决策构成操作为一种接受规则，该规则结合了置信度和BDI，用于机制感知的审计和分流。总之，这些结果使BDI成为决策构成的一般性诊断工具，能够区分不同模型家族中的特征支持决策和偏差驱动决策。

## Abstract
Modern AI systems can be accurate and confident, but this alone does not reveal whether a decision is well supported by the input. This creates a trust problem because confidence reports how decisive a model is, but not what supports that decisiveness. Here we show that neural-network confidence can be decomposed into input-dependent feature support and input-independent offset support. We formalize this decomposition through the Bias Dominance Index (BDI), a layer-resolved measure quantifying the relative contribution of input-independent offsets to the decision margin, revealing whether confidence is primarily feature-supported or bias-driven. Across convolutional neural networks, a vision transformer and a transformer language model, BDI shows that high confidence can coexist with bias-driven decisions. Layer-resolved analyses map where bias-driven support across network depth. Perturbation analyses further show that the bias component can stabilize performance when readout weights are degraded. Finally, we operationalize decision composition into an acceptance rule that combines confidence and BDI for mechanism-aware auditing and triage. Together, these results position BDI as a general diagnostic of decision composition that distinguishes feature-supported from bias-driven decisions across model families.