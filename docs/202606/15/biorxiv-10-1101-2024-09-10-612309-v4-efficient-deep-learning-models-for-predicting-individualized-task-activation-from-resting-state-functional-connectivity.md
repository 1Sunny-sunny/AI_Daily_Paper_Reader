---
title: Efficient Deep Learning Models for Predicting Individualized Task Activation from Resting-State Functional Connectivity
title_zh: 基于静息态功能连接预测个体化任务激活的高效深度学习模型
authors: "Madsen, S. J., Lee, Y.-E., Quah, S. K. L., Uddin, L. Q., Mumford, J. A., Barch, D. M., Fair, D. A., Gotlib, I. H., Poldrack, R. A., Kuceyeski, A., Saggar, M."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.1101/2024.09.10.612309v4.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用深度学习从静息态功能磁共振预测任务诱发的大脑激活
tldr: 本研究评估了从静息态功能连接预测个体任务激活的深度学习模型效率与可扩展性。基于人类连接组计划数据，复现BrainSurfCNN并扩展出引入通道注意力的BrainSERF和利用皮层网格拓扑的BrainSurfGCN。三个模型预测性能相当，但BrainSERF略优地捕捉个体特征，BrainSurfGCN大幅减少参数量和训练时间。此外，预测精度受行为表现、数据质量与激活变异性共同限制，表明拓扑与功能先验可提升效率，但根基在于神经信号的可靠性。
source: biorxiv
selection_source: fresh_fetch
motivation: 提升静息态功能连接预测个体任务激活的深度学习模型的效率与可扩展性。
method: 基于HCP数据复现BrainSurfCNN，并扩展引入注意力机制的BrainSERF和图结构的BrainSurfGCN，系统比较预测性能。
result: 模型预测精度相似，但BrainSERF个体识别略优，BrainSurfGCN效率显著提升；预测受任务表现、数据质量与激活变异性制约。
conclusion: 结合拓扑与功能先验可提升效率而不牺牲精度，但预测上限受限于神经信号可靠性。
---

## 摘要
深度学习模型已展现出从静息态功能磁共振成像（fMRI）预测任务诱发脑激活的潜力，这为无需任务态数据即可实现个体化脑图谱绘制提供了途径。在本研究中，我们系统评估了提高此类模型效率和可扩展性的架构策略。利用人类连接组计划的数据，我们复现了BrainSurfCNN框架，并引入了两种扩展：BrainSERF，通过压缩-激励模块整合了通道注意力机制；以及BrainSurfGCN，一种基于图的模型，利用皮层网格拓扑进行高效消息传递。在包括空间相关性、Dice分数、Dice AUC和受试者识别准确率在内的多种评估指标上，所有模型均取得了相当的预测性能。尽管准确率相似，但提出的模型提供了明显的优势。BrainSERF在捕捉个体特异性特征方面有适度改进，而BrainSurfGCN则显著减小了模型规模和训练时间，突显了性能与计算效率之间的良好权衡。除了架构比较，我们还研究了驱动预测准确性变异的因素。我们发现，行为任务表现、静息态数据质量以及任务激活的个体间变异性共同制约了预测保真度。特别是，信号可靠性较低且变异性较高的对比在所有模型中均表现出较低的可预测性。总之，这些发现表明，融入拓扑和功能结构先验可以在不牺牲准确性的前提下提高深度学习模型的效率，同时也强调预测性能从根本上受限于底层神经信号的可靠性。

## Abstract
Deep learning models have demonstrated the potential to predict task-evoked brain activation from resting-state fMRI, offering a pathway toward individualized brain mapping without requiring task-based data. In this study, we systematically evaluate architectural strategies for improving the efficiency and scalability of such models. Using data from the Human Connectome Project, we replicate the BrainSurfCNN framework and introduce two extensions: BrainSERF, which incorporates channel-wise attention through squeeze-and-excitation modules, and BrainSurfGCN, a graph-based model that leverages cortical mesh topology for efficient message passing. Across multiple evaluation metrics, including spatial correlation, Dice score, Dice AUC, and subject identification accuracy, all models achieve comparable predictive performance. Despite similar accuracy, the proposed models o!er distinct advantages. BrainSERF provides modest improvements in capturing individual-specific features, while BrainSurfGCN achieves substantial reductions in model size and training time, highlighting a favorable trade-off between performance and computational efficiency. Beyond architectural comparisons, we investigate factors driving variability in prediction accuracy. We find that behavioral task performance, resting-state data quality, and inter-subject variability in task activation jointly constrain prediction fidelity. In particular, contrasts with lower signal reliability and higher variability exhibit reduced predictability across all models. Together, these findings demonstrate that incorporating topological and functional structural priors can improve the efficiency of deep learning models without sacrificing accuracy, while also emphasizing that prediction performance is fundamentally limited by the reliability of the underlying neural signals.