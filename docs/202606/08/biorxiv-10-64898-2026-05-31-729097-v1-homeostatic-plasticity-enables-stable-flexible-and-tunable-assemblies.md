---
title: "Homeostatic Plasticity Enables Stable, Flexible, and Tunable Assemblies"
title_zh: 稳态可塑性实现稳定、灵活且可调的神经集群
authors: "Miller, M. C., Miehl, C., Doiron, B."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729097v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 稳态可塑性模型支持稳定神经元集群
tldr: 传统赫布可塑性的神经元集群模型常导致连接强度的二元结果，缺乏灵活性。本文引入稳态可塑性，将抑制性突触可塑性与兴奋性可塑性结合，并在稳态目标发放率处平衡兴奋性可塑性。通过脉冲神经网络和平均场理论，发现突触强度空间中的线吸引子，使网络能在连续谱上稳定存在，且集群结构不再二元。该方案下神经元发放率保持不变，但网络动态增益和时间常数可调，实现了稳定、灵活且可调的集群，并分析了相关输入的影响及缓解策略。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统赫布可塑集群模型产生全或无的二元连接，无法实现灵活的连续变化。
method: 在循环脉冲网络中结合赫布兴奋性可塑性与稳态抑制性可塑性，并假设兴奋性可塑性在目标发放率处平衡，利用平均场理论分析。
result: 发现突触权重的线吸引子，使得网络可稳定于连续强度的集群结构，且发放率恒定但动态增益和时间常数可调。
conclusion: 稳态可塑性框架实现了连续、可调的灵活集群，相关噪声可能破坏但可通过共享相关输入给抑制性神经元来缓解。
---

## 摘要
高度互连的神经元群体，称为神经集群，通过突触可塑性机制动态形成，并被认为是大脑中记忆的基底。许多神经集群形成模型使用赫布型兴奋性至兴奋性可塑性，其中协调的活动增强循环结构。然而，这些模型通常产生二元的神经集群结果：网络要么具有弱（无集群）连接，要么具有最强（有集群）连接。我们考虑结合赫布型兴奋性至兴奋性可塑性和抑制性至兴奋性突触的网络，这些突触具有可塑性，能稳态地将兴奋性神经元放电稳定在目标值。当我们将兴奋性至兴奋性可塑性设定为稳态顺应性，即在稳态目标放电率下增强和抑制达到平衡时，我们发现突触强度的一个稳定连续谱，神经集群结构不再是二元的。我们使用脉冲神经元模型的循环网络及相关的平均场理论，将这一连续谱识别为突触权重空间中的线吸引子。尽管沿着吸引子，稳态确保神经元放电率不变，但网络的动态响应特性相当可塑，强耦合网络具有高增益和更长的时间尺度响应。利用我们的平均场理论，我们展示了兴奋性神经元之间的相关随机放电活动如何破坏线吸引子，但当相关输入在兴奋性和抑制性神经元之间共享时，这可以得到缓解。总之，我们提供了一个基于稳态的替代学习框架，其中可能实现可调且灵活的神经集群结构。

## Abstract
Strongly interconnected neuronal populations, called assemblies, dynamically form through synaptic plasticity mechanisms and are thought to be a substrate for memories in the brain. Many assembly formation models use Hebbian excitatory-to-excitatory plasticity, where coordinated activity strengthens recurrent structure. However, these models typically yield binary assembly outcomes: networks with either weak (no assembly) or maximally strong (assembly) connectivity. We consider networks with a combination of Hebbian excitatory-to-excitatory plasticity and inhibitory-to-excitatory synapses with plasticity that homeostatically stabilizes excitatory neuron firing at a target value. When we set excitatory-to-excitatory plasticity to be homeostatically compliant, in that potentiation and depression are balanced at the homeostatic target firing rate, we find a stable continuum of synaptic strengths, and assembly structure is no longer binary. We use a recurrent network of spiking neuron models and an associated mean-field theory to identify this continuum as a line attractor in synaptic weight space. While along the attractor, homeostasis ensures that neuronal firing rates are invariant, the dynamical response properties of the network are quite malleable, with strongly coupled networks having high gain and longer timescale responses. Using our mean-field theory we show how correlated stochastic spiking activity among the excitatory neurons can destroy the line attractor, yet this can be mitigated when correlated inputs are shared across the excitatory and inhibitory neurons. Altogether, we provide an alternative learning framework based on homeostasis, where a tunable and flexible assembly structure is possible.

---

## 论文详细总结（自动生成）

## 论文总结：稳态可塑性实现稳定、灵活且可调的神经集群

### 1. 核心问题与整体含义
- **研究动机**：神经集群（assemblies）被认为是大脑中记忆等功能的物质基础，通过突触可塑性动态形成。传统的赫布型兴奋性-兴奋性可塑性模型虽能形成循环连接结构，但结果往往呈现“全或无”的二元特征——网络要么处于弱连接（无集群）状态，要么达到最大强度连接（有集群）状态，缺乏中间过渡的灵活性。
- **整体含义**：本文旨在打破这种二元局限，通过引入稳态可塑性机制，实现连续、可调且稳定的神经集群强度谱，为大脑如何产生灵活的记忆表征提供新的理论框架。

### 2. 方法论
- **核心思想**：将赫布型兴奋性至兴奋性（E→E）可塑性与抑制性至兴奋性（I→E）稳态可塑性相结合。关键设定是使E→E可塑性具有“稳态顺应性”，即在稳态目标发放率处，长时程增强（LTP）和长时程抑制（LTD）达到平衡。
- **关键技术细节**：
  - 使用**脉冲神经元循环网络**模型。
  - 引入抑制性突触的稳态可塑性，使兴奋性神经元发放率稳定在目标值。
  - 假设E→E可塑性在目标发放率处净变化为零，从而在突触权重空间中产生**线吸引子**（line attractor）：一组连续的稳定平衡点，而非孤立的不动点。
- **理论分析工具**：建立**平均场理论**，对网络活动进行降维分析，解释线吸引子的动力学特性和网络的动态响应。

### 3. 实验设计
- **实验场景**：计算神经科学中的理论建模与数值模拟，未使用传统机器学习中的数据集或基准任务。实验围绕脉冲神经网络的自组织动力学展开。
- **对比方法**：隐含对比传统赫布可塑性模型（产生二元集群结果），展示本文提出的稳态可塑性模型能够生成连续的集群强度谱。
- **评价指标**：神经元发放率不变性、突触权重分布、网络动态增益和时间常数等。

### 4. 资源与算力
- 论文摘要及提供的元数据中**未提及**所使用的GPU型号、数量、训练时长等具体算力信息。考虑到工作以平均场理论分析与脉冲网络数值模拟为主，应属轻量级计算，但确切细节未予说明。

### 5. 实验数量与充分性
- 无法从现有信息中获悉具体实验组数（如不同参数扫描、消融实验等）。摘要仅概括了主要发现：稳态可塑性产生连续谱、线吸引子、动态响应可调以及相关噪声的影响和缓解策略。
- 从科学论证角度看，该理论工作通过平均场理论给出解析解释，并辅以仿真验证，逻辑连贯；但摘要未提供详细的实验体量、参数空间覆盖或鲁棒性消融，因而充分性难以评估。

### 6. 主要结论与发现
- **连续集群结构**：稳态可塑性框架使突触权重不再收敛于两个极端，而形成一条稳定的连续谱，网络可停留在线吸引子上的任意强度，集群结构灵活可调。
- **发放率不变性与动态可塑性**：沿着线吸引子，神经元稳态发放率保持不变，但网络的动态增益和时间常数随耦合强度显著变化——强耦合网络具有高增益和更长时程的响应。
- **相关噪声的影响与缓解**：兴奋性神经元之间的相关随机发放活动可能摧毁线吸引子；若将相关输入也共享给抑制性神经元，则能有效缓解此破坏效应。

### 7. 优点
- **理论创新**：巧妙的稳态顺应性设定将原本二元的赫布可塑性转化为连续可调机制，并揭示权重空间的线吸引子结构，理论分析严谨。
- **功能解释力**：在不改变发放率的前提下实现网络动态可塑，为记忆的精细调节和灵活表征提供了可能机制。
- **实用启示**：指出相关噪声的破坏作用及共享抑制性通路作为缓解策略，具有生物学合理性。

### 8. 不足与局限
- **实验覆盖有限**：仅从摘要推断，未看到大规模参数搜索、多种网络配置或不同刺激范式的系统比较，实验的广度与深度不明确。
- **生物学细节缺失**：关于“稳态顺应性”的具体生物学实现途径、抑制性可塑性规则的形式缺少更细致的论证；模型的适用边界未探讨。
- **偏差风险**：作为纯计算模型，结论建立在平均场近似和特定可塑性规则上，向真实生物神经回路的迁移性需要更多实验验证。
- **应用限制**：目前仅分析了单一集群的自组织，对于多集群交互、记忆存储容量等复杂认知功能尚未涉及。

（完）
