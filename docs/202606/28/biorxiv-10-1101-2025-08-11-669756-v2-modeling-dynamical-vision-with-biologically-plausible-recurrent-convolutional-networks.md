---
title: Modeling Dynamical Vision with Biologically Plausible Recurrent Convolutional Networks
title_zh: 利用生物可行的递归卷积网络对动态视觉进行建模
authors: "Gutzen, R., Lindsay, G. W."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.1101/2025.08.11.669756v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 生物可信递归CNN建模视觉皮层动态
tldr: 针对卷积神经网络缺乏生物视觉递归连接导致难以捕捉时空现象的问题，本研究开发了DynVision开源工具箱，支持异构延迟和多种递归类型。通过系统探索，发现递归配置决定时序动力学和噪声鲁棒性，连续时间递归无需显式归一化即可产生皮层现象，另一配置接近人类噪声鲁棒性。这强调了建模选择的重要性与统一框架需求。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有CNN模型缺乏生物视觉中普遍存在的递归连接，无法模拟时空现象，且缺乏系统比较不同递归架构影响的工具。
method: 提出DynVision工具箱，实现带异构延迟的数值ODE求解器和五种侧向递归类型，采用配置驱动设计分离科学建模与实现。
result: 递归集成目标位置和损失时间窗口等隐式选择显著影响时序动力学；连续时间递归自然产生皮层现象；特定配置实现接近人类水平的噪声鲁棒性。
conclusion: 递归配置呈现功能分化，创建完全真实视觉模型极具挑战，亟需统一框架辅助探索。
---

## 摘要
用于图像识别的卷积神经网络(CNNs)已展现出与灵长类腹侧视觉通路显著的概念相似性，但其标准的前馈架构缺乏视觉皮层中普遍存在的递归连接。这种递归被视为适应、延迟归一化和对噪声输入鲁棒性等时空现象的基础。然而，将功能上有益的递归整合到捕捉生物视觉时空现象的CNN中仍然具有挑战性。尽管近期进展已纳入神经生物学约束，该领域仍缺乏可访问的工具，用以系统比较不同架构选择（如递归类型、时间延迟和连接模式）如何塑造神经动力学和行为。在此，我们介绍DynVision，这是一个模块化的开源工具箱，用于构建和评估生物可行的递归卷积神经网络(RCNNs)。DynVision实现了具有异构延迟的数值ODE求解器，支持从简单的自连接到皮层组织的局部递归的五种侧向递归类型，并通过配置驱动的设计将科学建模决策与实现细节分离。训练具有计算效率，相比参考实现实现了52%的加速。我们通过系统探索参数空间展示了该框架，揭示了时间动力学中的定性差异对通常隐式的建模选择高度敏感，例如递归集成的目标位置和用于损失计算的时间窗口。关键的是，我们发现连续时间递归动力学可以自然地产生皮层时间现象，而无需显式的除法归一化，而另一种递归配置则产生了接近人类水平的噪声鲁棒性。这些发现表明递归的功能不同配置，并突显了创建完全真实模型的挑战，从而强调了需要一个全面且统一的建模框架以辅助探索。代码和文档可在 https://github.com/Lindsay-Lab/DynVision/ 获取。

## Abstract
Convolutional Neural Networks (CNNs) trained for image recognition have demonstrated remarkable conceptual similarities to the primate ventral visual pathway, but their standard feedforward architectures lack the recurrent connections that are ubiquitous in visual cortex. Such recurrence is thought to underlie spatiotemporal phenomena including adaptation, delayed normalization, and robustness to noisy input.However, incorporating functionally beneficial recurrence into CNNs that captures spatiotemporal phenomena of biological vision remains challenging. Although recent advances have incorporated neurobiological constraints, the field lacks accessible tools for systematically comparing how different architectural choices, such as recurrence type, temporal delays, and connectivity patterns, shape neural dynamics and behavior. Here, we introduce DynVision, a modular open-source toolbox for constructing and evaluating biologically plausible recurrent convolutional neural networks (RCNNs). DynVision implements numerical ODE solvers with heterogeneous delays, supports five types of lateral recurrence ranging from simple self-connections to cortically-organized local recurrence, and separates scientific modeling decisions from implementation details through a configuration-driven design. Training is computationally efficient, achieving a 52% speedup over reference implementations.We demonstrate the framework through systematic exploration of the parameter space, revealing that qualitative differences in temporal dynamics are highly sensitive to often-implicit modeling choices such as the target location of recurrent integration and the temporal window used for loss computation. Critically, we find that continuous-time recurrent dynamics can naturally give rise to cortical temporal phenomena without requiring explicit divisive normalization, while a different recurrent configuration produces noise robustness approaching human-level performance. These findings suggest functionally distinct configurations of recurrence and highlight the challenge of creating fully realistic models, thus emphasizing the need for a comprehensive and cohesive modeling framework to aid exploration. Code and documentation are available at https://github.com/Lindsay-Lab/DynVision/.