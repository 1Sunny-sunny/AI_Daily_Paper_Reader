---
title: Parallel processing of orthogonal manifolds enables zero-shot composition in recurrent networks
title_zh: 正交流形的并行处理使递归网络中的零样本组合成为可能
authors: "Osako, Y., Arango, A., Asabuki, T."
date: 2026-06-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732142v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 循环网络动力学和正交流形用于神经群体编码
tldr: 动物能灵活组合已学行为而不需练习，但机制未明。本研究用局部预测可塑性规则训练递归网络，发现学习时的反馈几何决定零样本组合能力：正交反馈向量将任务嵌入可分离子空间，允许并行激活生成复合输出；对齐反馈或BPTT网络则不支持。该原理复现了运动皮层到达-姿势几何，可推广至高维运动，揭示了反馈几何是递归网络动态组合重用的基础原理。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究独立习得的行为如何能被并行组合而不需联合训练的计算机制。
method: 使用局部预测可塑性规则训练递归网络，分析不同反馈向量几何对动态子空间结构的影响。
result: 正交反馈向量形成可分离的动态子空间，支持零样本并行组合；对齐反馈或BPTT网络则无法实现。
conclusion: 反馈几何是递归网络学习为未来组合重用结构化动态的关键计算原理。
---

## 摘要
动物能灵活地将已习得的行为组合成新动作，而无需练习这些组合，但支持独立习得的计算并行表达的神经计算机制仍不清楚。在这里，我们表明，学习过程中的反馈几何决定了递归动力学是否可以通过零样本并行组合进行重组。使用通过局部预测可塑性规则训练的递归网络，我们发现不同的反馈向量将独立习得的计算嵌入到可分离的动力学子空间中，从而允许新的输入组合共同激活这些组件并生成复合输出，而无需联合训练。相反，对齐的反馈向量以及通过时间反向传播训练的网络表现出准确的单任务表现，但无法支持并行组合，这表明任务习得和未来的可复用性是学习的可分离属性。组合输入唤起了一条单一的复合群体轨迹，其在反馈塑造的任务子空间上的投影恢复了独立习得的组件动力学。同一原理再现了在运动皮层中观察到的加法式到达-姿势几何形状，并推广到更高维的运动基元。这些结果将反馈几何确定为一个计算原理，学习系统通过该原理为未来的组合复用结构化递归动力学。

## Abstract
Animals flexibly combine learned behaviors into novel actions without practicing their combinations, yet the computational mechanisms that enable independently acquired computations to be expressed in parallel remain unclear. Here we show that feedback geometry during learning determines whether recurrent dynamics can be recombined through zero-shot parallel composition. Using recurrent networks trained by a local predictive plasticity rule, we found that distinct feedback vectors embed independently learned computations in separable dynamical subspaces, allowing novel input combinations to co-activate these components and generate composite outputs without joint training. In contrast, aligned feedback vectors, as well as networks trained by backpropagation through time, exhibited accurate single-task performance but failed to support parallel composition, demonstrating that task acquisition and future reusability are dissociable properties of learning. A combined input evoked a single composite population trajectory, whose projections onto feedback-shaped task subspaces recovered the independently learned component dynamics. The same principle reproduced additive reach-posture geometry observed in motor cortex and generalized to higher-dimensional movement primitives. These results identify feedback geometry as a computational principle by which learning systems structure recurrent dynamics for future compositional reuse.