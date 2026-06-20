---
title: Sparse Autoencoders Reveal Interpretable Features in Single-Cell Foundation Models
title_zh: 稀疏自编码器揭示单细胞基础模型中的可解释特征
authors: "Pedrocchi, F., Barkmann, F., Joudaki, A., Boeva, V."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.22.681631v3.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 使用稀疏自编码器揭示单细胞基础模型中的可解释特征
tldr: 单细胞基础模型应用广泛但内部机制不明。本研究通过训练稀疏自编码器分析三个预训练模型（scGPT、scFoundation、Geneformer）的隐藏表示，揭示了可解释的生物与技术特征，发现不同模型编码信息存在差异。进一步通过干预这些特征，成功抑制批次效应改善数据整合，并模拟药物扰动响应，为提升模型可解释性与可控性开辟了新路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 单细胞基础模型的内在机制尚未被充分理解，限制了其透明度和可控性。
method: 在三种单细胞基础模型的隐藏层上训练稀疏自编码器，以提取可解释的特征。
result: 提取的特征涵盖了丰富的生物和技术信号，并能通过抑制批次特征改善整合、激活药物特征模拟扰动，实现功能干预。
conclusion: 稀疏自编码器能揭示单细胞基础模型的可解释特征，并通过干预这些特征增强模型的透明度和控制能力。
---

## 摘要
单细胞基础模型（scFMs）在细胞类型注释、数据整合以及预测细胞扰动效应等应用中具有潜力，但其内部机制仍不甚明了。我们通过在三种广泛使用的scFMs（scGPT、scFoundation和Geneformer）的隐藏表征上训练稀疏自编码器（SAEs），来研究这些模型的结构。学习到的特征揭示了多样且复杂的生物学与技术信号，这些信号甚至在预训练模型中就已出现。我们还观察到，这类信息的编码方式在不同训练协议和架构的scFMs之间存在差异。最后，我们证明SAE衍生的特征与模型行为存在功能关联，并可进行干预。抑制批次相关特征能减少不想要的技术变异，改善数据整合，同时保留核心生物学信号。激活药物编码特征则会以浓度依赖的方式引导对照细胞向药物扰动状态转变。这些发现为构建更具可解释性和可控性的单细胞基础模型指明了一条道路。

## Abstract
Single-cell foundation models (scFMs) hold promise for applications in cell type annotation, data integration, and prediction of the effects of cell perturbations, but their internal mechanisms remain poorly understood. We investigate the structure of these models by training sparse autoencoders (SAEs) on the hidden representations of three widely used scFMs: scGPT, scFoundation, and Geneformer.The learned features reveal diverse and complex biological and technical signals, which emerge even in pre-trained models. We also observe that the encoding of this information differs between scFMs with distinct training protocols and architectures. Finally, we demonstrate that SAE-derived features are functionally related to model behavior and can be intervened upon. Suppressing batch-associated features reduces unwanted technical variation and improves data integration while preserving the core biological signal. Activating drug-encoding features steers control cells toward drug-perturbed states in a concentration-dependent manner. These findings provide a path toward more interpretable and controllable single-cell foundation models.