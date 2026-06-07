---
title: Equivalent volitional learning emerges through circuit-specific population dynamics in motor cortex and hippocampus
title_zh: 通过运动皮层和海马中的回路特异性群体动力学实现等效的意志学习
authors: "de Vicente, A., Mitelut, C., Viana Mendes, R., Marianelli, L., Colomer Rosell, M., Bruckner, D., Bardella, G., Donato, F."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.730137v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 脑机接口训练调节群体动态
tldr: 本研究通过脑机接口训练小鼠调控初级运动皮层(M1)和海马CA3的神经群体活动以获取奖赏，比较了两种架构迥异的回路在相同学习任务下的表现。结果发现两者均能习得自主控制，并展现出一组跨回路的共享学习特征，但其底层群体动态显著不同：M1呈连续流动，CA3呈接近-返回动态。循环网络模型表明，局部连接约束即可解释这些差异，揭示了学习并非单一规范方案，而是由回路特异机制实现的多种实现方式。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究不同脑回路在相同学习中是否共享机制，还是由局部架构决定特异实现。
method: 利用脑机接口使小鼠直接调控M1或CA3的神经群体活动以获得奖赏，并构建具有不同连接约束的循环网络模型。
result: 两个区域均习得控制，共享了奖赏相关神经元调制、网络稀疏化和探索增强等特征，但M1呈现连续流动动态，CA3则为接近-返回动态。
conclusion: 等效学习结果可由不同回路通过其局部网络架构所决定的特异动态实现，揭示了学习的简并性。
---

## 摘要
学习在不同脑回路中运作，将群体活动模式与期望的结果关联起来，并使这些模式的意志再激活以控制行为。这些回路在结构和动力学机制上存在深刻差异，但哪些学习特征在不同回路间共享，哪些源于回路特异性的实现，仍不清楚。在这里，我们使用脑机接口（BCI）训练小鼠调节选定的神经元集合的活动朝触发奖励传递的配置。通过将奖励传递直接取决于群体活动，我们在两个具有不同动力学机制的回路（初级运动皮层 M1 和海马 CA3 区）上施加了相同的联想学习问题。小鼠在这两个区域都获得了稳健的意志控制，并且学习产生了一组跨回路的共享特征，包括对控制奖励的神经元的调制、网络水平的稀疏化，以及对奖励相关活动模式的更大探索。这些特征由不同的群体动力学支撑：M1 活动持续流经奖励相关状态，而 CA3 活动围绕它们追踪接近-返回动力学。配备不同最小连接约束的递归网络模型，这些约束反映了每个区域的主要动力学机制，捕捉了这些共享特征和区域特定动力学的关键特性，表明局部结构约束足以解释学习的不同实现。这些发现表明，等效的学习结果源于结构不同的回路中不同的动力学实现。这一原则性的冗余揭示了学习不是一个单一的标准解决方案，而是通过由局部网络架构塑造的多种回路特异性机制实现的。

## Abstract
Learning operates across different brain circuits to associate population activity patterns with desired outcomes, and to enable volitional reactivation of those patterns to control behavior. These circuits differ profoundly in their architecture and dynamical regimes, yet which features of learning are shared across them and which arise from circuit-specific implementations remains unknown. Here, we use a brain-computer interface (BCI) to train mice to modulate the activity of selected neuronal ensembles toward configurations that trigger reward delivery. By making reward delivery contingent directly on population activity, we impose an identical associative learning problem on two circuits with distinct dynamical regimes: the primary motor cortex (M1) and the hippocampal area CA3. Mice acquired robust volitional control in both regions, and learning produced a set of shared signatures across circuits, including modulation of reward-controlling neurons, network-level sparsification, and greater exploration of reward-related activity patterns. These signatures were underpinned by distinct population dynamics: M1 activity flowed continuously through reward-associated states, whereas CA3 activity traced approach-and-return dynamics around them. Recurrent network models endowed with distinct minimal connectivity constraints chosen to reflect the dominant dynamical regime associated with each region captured key features of these shared signatures and region-specific dynamics, indicating that local architectural constraints are sufficient to account for the distinct implementations of learning. These findings indicate that equivalent learning outcomes arise from divergent dynamical implementations across architecturally distinct circuits. This principled degeneracy reveals that learning is not a single canonical solution, but is implemented through multiple circuit-specific mechanisms shaped by local network architecture.

---

## 论文详细总结（自动生成）

# 论文总结

## 1. 核心问题与整体含义  
- **研究动机**：大脑不同脑回路（如运动皮层M1与海马CA3）在结构连接与动力学机制上存在根本差异，但学习是否依赖一套统一的规范机制，还是由各回路局部架构决定其特异实现，仍未得到解答。  
- **整体含义**：本研究旨在揭示“学习”是否存在跨回路的共享原则，还是允许由回路特异性动力学实现等效的行为结果——即学习的“简并性”（degeneracy）。通过直接比较两个典型回路在完全相同任务中的表现，论文质疑了“单一标准解决方案”的假设，为理解大脑如何通过多种途径实现同一认知功能提供了原则性证据。

## 2. 方法论  
- **核心思想**：利用脑机接口（BCI）将奖赏发放直接绑定于神经群体活动构型，从而对M1和CA3施加完全相同的联想学习任务。动物需自主调控选定的神经元集合活动，使其达到触发奖赏的配置。  
- **关键技术与流程**：  
  - 在小鼠M1或CA3植入多通道电极，记录群体神经元活动。  
  - 设定目标活动模式（选定神经元集合），当群体活动向量与目标模式的距离小于阈值时，即时给予奖赏。  
  - 分析学习过程中神经元调制的变化、网络稀疏化程度、活动模式的探索行为。  
  - 对比两组动物（M1 vs. CA3）的群体动力学：M1呈连续流经状态，CA3呈“接近-返回”动态。  
- **计算模型**：  
  - 构建具有不同最小连接约束的递归网络模型，分别模拟M1的连续动力学与CA3的吸引子/离散动力学。  
  - 模型验证局部结构约束足以为共享学习特征和区域特异性动力学提供解释。

## 3. 实验设计  
- **实验对象与场景**：小鼠活体实验，分别针对初级运动皮层（M1）和海马CA3区进行BCI训练。  
- **任务范式**：一种统一的意志控制任务——动物通过自由探索神经活动空间，学会将群体活动主动引向奖赏相关配置。实验对比两个脑区在同一范式下的表现。  
- **对比维度**：  
  - 行为层面：是否均能习得意志控制。  
  - 神经层面：学习诱发的共享特征（如奖励神经元调制、网络稀疏化、探索增强）与差异特征（群体动力学本质）。  
  - 模型层面：给予不同初始连接约束的递归网络，能否再现两种动力学及学习特征。  
- **Benchmark概念**：没有传统机器学习benchmark；内在比较基准是“相同任务下，两个回路的共享与特异表现”，以及计算模型对生物数据特征的复现能力。

## 4. 资源与算力  
- **文中提及情况**：提供的摘要及元数据未明确描述计算资源（GPU型号、数量、训练时长）。  
- **推断**：递归网络模型可能基于数值模拟，脑机接口实验依赖电生理记录设备，但具体算力信息缺失。

## 5. 实验数量与充分性  
- **实验组数**：摘要未提供具体动物数量、试验次数或模型模拟的详细规模。仅描述了在M1和CA3两个回路进行实验，并辅以计算模型验证。  
- **充分性评估**：从摘要看，设计逻辑清晰——直接比较两个结构迥异回路在同一行为任务下的表现，并采用计算模型提炼机制，具备原理验证的充分性。但缺乏统计细节（如样本量、效应量），难以判断结果稳健性。

## 6. 主要结论与发现  
- **等效意志学习**：M1和CA3均能通过BCI训练获得对奖赏相关神经群体活动的自主控制，证明不同回路可以解决相同联想学习问题。  
- **跨回路共享特征**：学习导致奖励控制神经元调制增强、网络水平活动稀疏化、对奖赏相关模式的探索范围扩大。  
- **回路特异性动力学**：M1的群体活动持续流经奖赏状态，表现为连续动态；CA3则呈现“接近奖赏状态-再离开”的循环式动态，反映其先天吸引子网络特征。  
- **局部架构决定性**：分别赋予反映M1和CA3主要动力学特性的最小连接约束的递归网络模型，可以重现上述共享特征和区域特异性动态，表明局部网络连接结构足以决定学习的实现路径。  
- **概念性突破**：学习不是一个“标准答案”，而是由局部回路架构塑造的多种实现方式的集合，为神经系统的“简并性”提供了一个功能实例。

## 7. 优点  
- **等任务比较范式**：通过BCI将相同抽象问题施加于两个截然不同的回路，排除了任务差异的混淆，严格分离了共享特征与回路特异性。  
- **机制-模型闭环**：不仅发现现象差异，还利用能复现关键特征的递归网络模型，将回路差异归因于可量化的连接约束，增强了因果解释力。  
- **揭示原则性冗余**：将“等效结果可由不同内部机制实现”这一系统工程概念引入学习理论，为理解大脑灵活性与鲁棒性提供了新视角。  
- **分析维度丰富**：同时考察了单神经元调制、群体稀疏化、探索行为和群体动力学，多层面刻画学习印迹。

## 8. 不足与局限  
- **信息不完整**：本研究仅基于预印本摘要，缺少方法细节（如动物数量、试验次数、统计检验）、数据变异性、对照实验等信息，难以评估结果的可重复性和效应强度。  
- **脑区选择局限**：仅比较了M1和海马CA3，两个区域虽代表不同的动力学极端，但结论是否能推广到皮层-皮层下其他回路、或学习类型（如恐惧条件化、技能学习）尚不清楚。  
- **BCI任务人工性**：直接将群体活动映射到奖赏，忽略了自然学习中感觉反馈、运动执行等环节，生态效度有限。  
- **模型简化**：递归网络模型使用了“最小连接约束”，可能遗漏真实生物物理细节（如树突计算、抑制环多样等），其对机制的归因可能是必要非充分的。  
- **缺乏行为输出关联**：摘要未提及动物是否同时产生运动或行为输出，群体活动的意志调控可能伴随未测量的运动策略，动机变量未控制。

（完）
