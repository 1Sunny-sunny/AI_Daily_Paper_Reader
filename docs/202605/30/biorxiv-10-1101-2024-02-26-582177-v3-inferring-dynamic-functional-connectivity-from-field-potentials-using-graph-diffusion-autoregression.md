---
title: Inferring Dynamic Functional Connectivity from Field Potentials Using Graph Diffusion Autoregression
title_zh: 基于图扩散自回归从场电位推断动态功能连接
authors: "Schwock, F., Bloch, J., Khateeb, K., Zhou, J., Atlas, L., Yazdan-Shahmorad, A."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.1101/2024.02.26.582177v3.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 图扩散自回归模型用于动态功能连接估计
tldr: 本研究针对现有功能连接估计多为静态且忽略结构连接的问题，提出图扩散自回归（GDAR）模型。该模型融合结构连接图与扩散约束，从场电位中推断高度动态的功能连接信号。模型在模拟数据和猕猴感觉运动皮层记录中得到验证，成功捕捉光遗传刺激、卒中后静息态变化及行为任务引起的快速神经通信动态，为动态功能连接分析提供了新途径。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有功能连接研究多为静态估计，无法捕捉高度动态的神经过程，且忽略了脑结构连接信息。
method: 提出图扩散自回归模型，在预定义的结构连接图上结合扩散约束，从场电位中推断动态功能连接。
result: 模型在模拟数据和猕猴微电极阵列记录中验证有效，能描述光遗传、卒中及行为任务引起的快速通信动态。
conclusion: GDAR模型可有效推断动态功能连接，揭示神经活动的快速变化，为认知研究提供有力工具。
---

## 摘要
随着多点神经记录技术的快速发展以及深入理解认知过程的需求，动态功能连接（dFC）估计正受到越来越多的关注。然而，大多数研究侧重于功能连接的静态估计，无法捕捉高度动态的神经过程，同时还忽略了大脑结构组织的信息。为了解决这些问题，我们引入了一类网络约束的线性自回归模型，该模型在预定义的结构连接图边上产生高度动态的功能连接信号。此外，我们展示了增加额外的扩散约束可以提升模型性能。我们成功地在模拟神经活动以及置于猕猴感觉运动皮层的硬膜下和皮层内微电极阵列记录上验证了所得到的图扩散自回归（GDAR）模型，证明其能够描述光遗传刺激引发的快速通信动态、中风和电刺激后静息态 dFC 的变化，以及伸手任务期间行为的神经相关活动。

## Abstract
Estimating dynamic functional connectivity (dFC) is attracting increased attention, spurred by rapid advancements in multi-site neural recording technologies and efforts to better understand cognitive processes. Yet, most studies focus on static estimates of functional connectivity that cannot capture highly dynamic neural processes, while also ignoring information about the structural organization of the brain. To address these issues, we introduce a class of network-constrained linear autoregressive models that give rise to a highly dynamic functional connectivity signal on the edges of a predefined structural connectivity graph. Furthermore, we demonstrate that adding an additional diffusion constraint improves the model's performance. We successfully validated the resulting graph diffusion autoregressive (GDAR) model on simulated neural activity and recordings from subdural and intracortical micro-electrode arrays placed in macaque sensorimotor cortex demonstrating its ability to describe rapid communication dynamics induced by optogenetic stimulation, changes in resting state dFC following stroke and electrical stimulation, and neural correlates of behavior during a reach task.