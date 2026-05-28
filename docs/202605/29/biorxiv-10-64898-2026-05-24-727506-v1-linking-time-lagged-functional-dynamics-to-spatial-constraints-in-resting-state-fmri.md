---
title: Linking time-lagged functional dynamics to spatial constraints in resting-state fMRI
title_zh: 将静息态fMRI中的时滞功能动力学与空间约束相联系
authors: "Benozzo, D."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.24.727506v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 静息态fMRI的时间滞后功能动力学
tldr: 本研究运用线性状态空间模型分析小鼠静息态fMRI数据，聚焦于差分协方差矩阵，通过Schur分解提取二维旋转模式，旨在弥合模型与连接组模型的解释差距。研究发现，较快的旋转模式与结构距离矩阵主导特征向量一致对齐，揭示了时间滞后功能动态受制于区域间空间距离约束的机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究静息态fMRI中时间滞后功能动态背后的空间结构约束。
method: 对小鼠fMRI数据的Jacobian矩阵进行Schur分解，提取二维旋转模式并关联结构距离矩阵。
result: 较快的Schur模式在小鼠间一致对齐结构距离矩阵的主导特征向量。
conclusion: 差分协方差编码的空间约束可通过Schur分解解释，为脑动态的生成式建模提供了新见解。
---

## 摘要
线性状态空间模型已被证明能有效再现大规模脑动力学。我们将该方法应用于20只小鼠的静息态fMRI数据，重点关注系统的雅可比矩阵，即有效连接，特别是其编码非零滞后交互的分量：微分协方差矩阵。在该矩阵中，我们集中于非对角线分量（dC-Cov），它反映了内源性时滞相关。我们的目标是从机制角度确定雅可比矩阵的一种分解，以便于解释。由于dC-Cov捕获了信号轨迹的旋转成分，我们采用舒尔分解提取二维旋转模式，每个模式由一对正交向量和一个关联的角频率表征。这为该建模框架提供了更具生成性的表述，从而缩小了该方法与基于连接组的耦合神经群网络模型之间的可解释性差距。在此框架内，精度矩阵支配着不同舒尔模式之间的耦合，而我们假设dC-Cov反映了由区域间距离施加的空间约束。通过检查dC-Cov与脑区空间布局所施加的结构约束之间的关系，我们发现小鼠间较快的舒尔模式与结构距离矩阵的主特征向量之间存在一致的对应关系。

## Abstract
Linear state-space models have been shown to effectively reproduce large-scale brain dynamics. We applied this approach to resting-state fMRI data acquired from 20 mice, focusing on the system's Jacobian matrix, i.e. the effective connectivity, and specifically on its component encoding nonzero-lag interactions: the differential covariance matrix. Within this matrix, we concentrated on the off-diagonal component (dC-Cov), which reflect endogenous time-lagged correlations. Our aim was to identify a decomposition of the Jacobian matrix that facilitates its interpretation from a mechanistic perspective. Since the dC-Cov captures the rotational component of signal trajectories, we employed Schur decomposition to extract 2D rotational modes, each characterized by a pair of orthogonal vectors, and an associated angular frequency. This provides a more generative formulation of the modeling framework, thereby reducing the interpretability gap between this approach and connectome-based network models of coupled neural masses. Within this framework, the precision matrix governs the coupling between different Schur modes, while we hypothesize that the dC-Cov reflects spatial constraints imposed by inter-regional distances. By examining the relationship between dC-Cov and structural constraints imposed by the spatial placement of brain areas, we found a consistent alignment between the faster Schur modes across mice and the leading eigenvectors of the structural distance matrix.