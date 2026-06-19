---
title: "DeltaQ: Value-Guided Hebbian Learning in Spiking Neuronal Networks for Multi-Goal Navigation"
title_zh: DeltaQ：多目标导航中脉冲神经元网络的值引导赫布学习
authors: "Earl, C., Unal, G., Hazan, H., Neymotin, S. A."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.12.731882v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用网格细胞的尖峰神经网络导航模型
tldr: 针对动物在稀疏延迟反馈下导航的需求，本文提出脉冲神经网络模型，结合网格细胞空间表征、ΔQ调制的赫布可塑性及上下文调制，使共享网络能学习多个导航目标。模型在迷宫中展示了高效策略学习和灵活的行为切换，为融合神经机制与强化学习提供了桥梁。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统模型侧重重现神经动态，忽视如何从稀疏奖励中学习导航任务，需构建生物可行的任务驱动网络。
method: 采用脉冲神经网络，利用网格细胞关联编码、ΔQ调制的赫布可塑性及上下文细胞任务调制实现价值引导的空间学习。
result: 模型在迷宫中生成了区分性的空间表征，学会稀疏奖励下的最优导航，并支持多目标共享网络。
conclusion: 生物启发的表征、价值可塑性和上下文调制能共同支撑灵活导航，验证了神经机制与功能学习的整合可行性。
---

## 摘要
动物常常必须在关于目标进展的反馈稀疏或延迟的环境中进行导航，这需要空间的内部表征和先前经验的记忆。海马-内嗅系统被认为通过指导目标导向行为的分布式空间表征来支持这一能力。然而，许多针对这些回路的计算模型主要关注再现神经动力学，而非展示此类表征如何支持导航任务的学习。我们提出一个受生物启发的脉冲神经元网络（SNN）模型，该模型结合了网格细胞衍生的空间表征、ΔQ调制的赫布可塑性以及上下文依赖的调制，以在稀疏奖励条件下支持导航。网格细胞群体生成分布式的空间编码，这些编码被关联细胞群体转化为更具空间选择性的内部表征。学习由根据目标条件的Q表计算出的Q值变化（ΔQ）驱动，使局部突触可塑性能够融入关于长期导航结果的信息。对于包含多个导航目标的环境，上下文细胞群体提供任务依赖的调制，使得共享的网络架构能够支持不同的导航策略。在两个互补的迷宫环境中，该模型展示了三个核心能力：生成独特的空间表征，在稀疏和延迟奖励下学习高效的导航策略，以及在共享环境中支持多个导航目标。结果进一步表明，上下文调制在基本共享的群体表征中引入了微妙的、依赖任务的变化，使得相同的空间位置能够支持不同的导航行为。这些发现证明，受生物启发的空间表征、值引导的可塑性和上下文调制可以协同支持脉冲神经元网络中的灵活导航，从而在机制性神经回路模型和功能性强化学习之间架起一座桥梁。

## Abstract
Animals must often navigate environments where feedback about progress toward a goal is sparse or delayed, requiring internal representations of space and memory of prior experience. The hippocampal-entorhinal system is believed to support this capability through distributed spatial representations that guide goal-directed behavior. However, many computational models of these circuits focus primarily on reproducing neural dynamics rather than demonstrating how such representations support learning on navigation tasks. We present a biologically inspired spiking neuronal network (SNN) model that combines grid-cell-derived spatial representations, {Delta}Q-modulated Hebbian plasticity, and context-dependent modulation to support navigation under sparse reward conditions. Grid Cell populations generate distributed spatial codes that are transformed by an Association Cell population into more spatially selective internal representations. Learning is driven by changes in Q-values ({Delta}Q) computed from a goal-conditioned Q-table, allowing local synaptic plasticity to incorporate information about long-term navigation outcomes. For environments containing multiple navigation objectives, a Context Cell population provides task-dependent modulation that enables a shared network architecture to support distinct navigation policies. Across two complementary maze environments, the model demonstrates three core capabilities: generation of distinct spatial representations, learning of efficient navigation policies under sparse and delayed reward, and support for multiple navigation objectives within a shared environment. The results further show that contextual modulation introduces subtle task-dependent variations into a largely shared population representation, allowing identical spatial locations to support different navigation behaviors. These findings demonstrate that biologically inspired spatial representations, value-guided plasticity, and contextual modulation can jointly support flexible navigation in spiking neuronal networks, providing a bridge between mechanistic neural circuit models and functional reinforcement learning.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **核心问题**：动物如何在奖励稀疏或延迟的环境中学习导航，并灵活切换多个目标？传统海马-内嗅回路的计算模型偏重再现神经动态，未能解释这些空间表征如何支撑**从有限反馈中学习任务**。
- **整体含义**：论文试图弥合机制性神经回路模型与功能强化学习之间的鸿沟，证明**生物启发的表征、值引导的可塑性及任务调制**可以协同使脉冲神经网络（SNN）具备灵活多目标导航能力。

### 2. 方法论核心思想与关键技术

- **核心思想**：利用 **ΔQ 调制的赫布可塑性** 将稀疏、延迟的长期价值信号转化为局部突触更新，在保留生物合理性的同时实现策略学习。
- **网络架构**：
  - **网格细胞群体**：生成分布式空间编码（类似内嗅皮层网格细胞）。
  - **关联细胞群体**：将网格编码转化为更空间选择性的内部表征。
  - **上下文细胞群体**：在多目标场景下提供任务依赖调制，使同一共享网络产生不同导航策略。
- **学习规则**：
  - 使用**目标条件 Q 表**计算 Q 值变化量 $\Delta Q$，驱动突触可塑性。
  - 可塑性形式为**赫布学习**（局部协同活动），但被 $\Delta Q$ 全局调制，将长期回报信息注入局部权重更新。
- **流程**：网格空间编码 → 关联细胞生成内部状态 → 根据当前目标与内部状态选择动作 → 环境返回稀疏奖励 → 更新 Q 表并计算 $\Delta Q$ → 调制赫布规则更新关联权重。

### 3. 实验设计与对比

- **实验场景**：两种互补的迷宫环境（文中未详述具体尺寸或结构，从摘要可知为迷宫）。
- **核心能力展示（三类实验）**：
  1. 生成独特的空间表征；
  2. 在稀疏、延迟奖励下学习高效导航策略；
  3. 共享环境内支持多个导航目标。
- **对比/基准**：摘要未提及其他对比模型（如经典 RL 算法、非脉冲网络等），可能仅自我验证三重能力，**未明确 benchmark 或对比方法**。

### 4. 资源与算力

- **文中提供的信息**：摘要及元数据均未提及 GPU 型号、数量、训练时长或任何算力指标。
- **结论**：**算力信息缺失**，无法评估计算开销。

### 5. 实验数量与充分性

- **实验组数**：从摘要推断，至少包含 3 组核心能力验证（表征分析、单一迷宫学习、多目标共享网络），可能还有消融（如移除上下文调制、移除 $\Delta Q$ 调制等），但摘要未列明。
- **充分性评价**：
  - 若仅展示现象而无系统对比或消融，实验可能**单薄**；
  - 若在两类迷宫中重复上述 3 项且包含必要的消融，则相对充分；
  - 由于全文不可得，无法判断**统计稳健性**（如重复次数、误差线）或**公平对比**（如与 Q-learning 等经典算法的学习效率、路径最优性对比）。

### 6. 主要结论与发现

- **表征生成**：网格细胞驱动关联群体生成具有区分度的空间表征。
- **学习能力**：$\Delta Q$ 调制赫布可塑性使网络在稀疏/延迟奖励下习得**最优或高效导航策略**。
- **多目标灵活性**：上下文调制在基本共享的群体表征中引入**微妙的任务依赖变异**，使同一空间位置可支持不同导航行为。
- **整体结论**：生物启发表征、值引导可塑性与上下文调制三者协同，可在脉冲网络中实现灵活导航，证明了神经机制与功能学习的整合可行性。

### 7. 优点与亮点

- **生物合理性与功能学习的结合**：用脉冲神经元、网格编码、赫布规则等贴近神经科学的元件，解决类强化学习的导航问题，设计新颖。
- **ΔQ 调制机制**：将全局时序差分误差转化为局部突触事件，既是理论创新，又为神经环路中的信用分配提供一种假设。
- **多目标共享网络**：通过上下文调制避免为每个目标训练独立网络，提高参数效率和泛化潜力。
- **双迷宫验证**：在两种环境中重复核心发现，增加结果泛化性（若文中确实如此）。

### 8. 不足与局限

- **实验对比缺失风险**：摘要未提及其它算法（如深度 Q 网络、经典 Actor-Critic、非脉冲导航模型）的性能对比，难以判断所提方法的相对效率或最优性。
- **可扩展性与任务复杂度**：仅在迷宫环境验证，面对高维、连续或动态环境的可行性未知；Q 表的存在可能限制扩展到大规模状态空间。
- **生物保真度的局限性**：网格细胞、赫布规则等均被简化，与真实神经数据（如相位进动、重放、波纹等）的对应关系未提及。
- **算力信息缺失**：无法评估训练代价和实际部署难度。
- **理论分析欠缺**：$\Delta Q$ 调制赫布学习的收敛性、稳定性等未在摘要中讨论。
- **多目标冲突**：多目标共享网络虽精巧，但目标间若策略高度冲突，共享是否导致干扰或灾难性遗忘未讨论。

（完）
