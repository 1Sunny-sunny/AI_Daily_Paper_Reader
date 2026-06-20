---
title: Precision Functional Parcellation of the Human Cortex via Rest-Task fMRI Fusion
title_zh: 通过静息态-任务态 fMRI 融合的人脑皮层精准功能划分
authors: "Zhi, D., Du, J., Whitfield-Gabrieli, S., Diedrichsen, J., Ge, T."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731643v2.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 融合静息态和任务态fMRI的层级贝叶斯框架
tldr: 个体化皮层分割对揭示脑网络组织至关重要，但现有方法主要依赖静息态fMRI，未能充分利用任务数据提供的互补信息。本研究提出mRBM-HBP，一种可扩展的层次贝叶斯框架，通过融合静息态与任务fMRI并建模空间依赖，高效推断组及个体化分割。该方法在保持高性能的同时显著降低计算成本，发现静息态与任务态反映一致宏观网络，而任务数据提供功能边界细化。融合图谱提升了准确性、可靠性和个体特异性，表明多模态融合可增强脑功能组织映射的精度。
source: biorxiv
selection_source: fresh_fetch
motivation: 克服现有方法仅依赖静息态、未充分利用任务数据以及难以整合异质数据集的局限。
method: 提出mRBM-HBP，一种整合多项受限玻尔兹曼机以建模空间依赖的层次贝叶斯框架，实现静息态与任务fMRI的融合。
result: mRBM-HBP性能与最优静息态方法相当且计算成本更低；任务数据揭示一致网络并提供边界细化；融合图谱提升准确性、可靠性和个体特异性。
conclusion: 整合静息态与任务fMRI能够增强大脑功能组织的精确映射。
---

## 摘要
个体特异性皮层划分能够刻画常被群体水平图谱掩盖的脑网络组织，对基础神经科学和转化应用都具有广泛意义。然而，现有方法主要依赖静息态fMRI，未能充分利用任务诱发数据，后者提供了关于功能特化的互补信息。这一局限部分反映了整合异质性数据集的挑战，这些数据集在任务设计、样本量和皮层覆盖范围上各不相同。本文提出mRBM-HBP，一种可扩展的层级贝叶斯框架，结合多项受限玻尔兹曼机来建模空间依赖性，从而能够跨多样数据集高效灵活地整合静息态与任务态fMRI，并推断群体水平和个体水平的皮层划分。我们表明，mRBM-HBP在性能上与最先进的基于静息态的划分方法相当，同时大幅降低计算成本。通过整合大规模任务态fMRI数据集，我们得出了基于任务的划分，并证明静息态与任务条件揭示的宏观网络基本一致，而任务数据提供了功能边界的状态特异性细整。此外，融合静息态与任务态的群体水平图谱提高了推断划分的准确性、可靠性和个体特异性，尤其当个体水平数据有限时。这些结果表明，整合静息态与任务态fMRI增强了功能性脑组织的精准映射。

## Abstract
Individual-specific cortical parcellations enable the characterization of brain network organization that is often obscured by population-level atlases, with broad implications for both basic neuroscience and translational applications. However, existing methods rely primarily on resting-state fMRI and underutilize task-evoked data, which provide complementary information about functional specialization. This limitation partly reflects the challenge of integrating heterogeneous datasets that differ in task design, sample size, and cortical coverage. Here, we present mRBM-HBP, a scalable hierarchical Bayesian framework that incorporates a multinomial restricted Boltzmann machine to model spatial dependencies, enabling efficient and flexible integration of resting-state and task fMRI across diverse datasets and inference of both group-level and individual-level cortical parcellations. We show that mRBM-HBP achieves performance comparable to state-of-the-art resting-state-based parcellation methods while substantially reducing computational cost. By integrating large-scale task-fMRI datasets, we derive a task-based parcellation and demonstrate that resting-state and task conditions reveal largely consistent macroscopic networks, while task data provide state-specific refinements of functional boundaries. Moreover, a fused rest-task group-level atlas improves the accuracy, reliability, and individual specificity of inferred parcellations, particularly when individual-level data are limited. These results indicate that integrating resting-state and task fMRI enhances precision mapping of functional brain organization.