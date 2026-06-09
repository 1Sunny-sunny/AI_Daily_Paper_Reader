---
title: "Homeostatic Plasticity Enables Stable, Flexible, and Tunable Assemblies"
title_zh: 稳态可塑性实现稳定、灵活且可调控的神经元集群
authors: "Miller, M. C., Miehl, C., Doiron, B."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729097v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 通过可塑性形成神经元组装，基于尖峰的群体编码
tldr: 传统Hebbian可塑性模型导致神经元集群结构呈二元化（弱连接或无集群、最强连接），本文结合稳态可塑性，通过设定兴奋性突触可塑性在稳态目标放电率处平衡，发现突触强度可连续变化，形成线吸引子，集群结构不再二元，而是可调且灵活，为记忆形成提供新框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统集群形成模型产生二元的连接强度，无法实现连续可调的记忆表征。
method: 结合Hebbian兴奋性可塑性和稳态抑制性可塑性，利用尖峰神经元网络及平均场理论分析突触权重空间动力学。
result: 突触权重收敛至线吸引子，放电率不变但网络动态增益和响应时间尺度可调，相关输入的影响可通过共享输入缓解。
conclusion: 稳态可塑性实现了集群结构的稳定、灵活和可调，突破了二元局限。
---

## 摘要
高度互连的神经元群体，即神经元集群，通过突触可塑性机制动态形成，被认为是大脑中记忆的基底。许多集群形成模型使用赫布型兴奋性-兴奋性可塑性，其中协调活动强化了循环结构。然而，这些模型通常产生二元的集群结果：网络要么具有弱连接（无集群），要么具有最强连接（集群）。我们考虑的网络结合了赫布型兴奋性-兴奋性可塑性和抑制性-兴奋性突触的可塑性，后者通过稳态将兴奋性神经元放电稳定在目标值。当我们将兴奋性-兴奋性可塑性设为稳态兼容，即增强和抑制在稳态目标放电率下达到平衡时，我们发现突触强度存在稳定的连续统，且集群结构不再是二元的。我们使用脉冲神经元模型的循环网络及相关的平均场理论，将这一连续统识别为突触权重空间中的线吸引子。沿着吸引子，稳态确保神经元放电率不变，但网络的动态响应特性却相当可塑，强耦合网络具有高增益和更长的时间尺度响应。利用我们的平均场理论，我们展示了兴奋性神经元之间的相关随机脉冲活动如何破坏线吸引子，但当相关输入在兴奋性和抑制性神经元间共享时，这种破坏可被减轻。总之，我们提供了一个基于稳态的替代学习框架，其中可调谐且灵活的集群结构成为可能。

## Abstract
Strongly interconnected neuronal populations, called assemblies, dynamically form through synaptic plasticity mechanisms and are thought to be a substrate for memories in the brain. Many assembly formation models use Hebbian excitatory-to-excitatory plasticity, where coordinated activity strengthens recurrent structure. However, these models typically yield binary assembly outcomes: networks with either weak (no assembly) or maximally strong (assembly) connectivity. We consider networks with a combination of Hebbian excitatory-to-excitatory plasticity and inhibitory-to-excitatory synapses with plasticity that homeostatically stabilizes excitatory neuron firing at a target value. When we set excitatory-to-excitatory plasticity to be homeostatically compliant, in that potentiation and depression are balanced at the homeostatic target firing rate, we find a stable continuum of synaptic strengths, and assembly structure is no longer binary. We use a recurrent network of spiking neuron models and an associated mean-field theory to identify this continuum as a line attractor in synaptic weight space. While along the attractor, homeostasis ensures that neuronal firing rates are invariant, the dynamical response properties of the network are quite malleable, with strongly coupled networks having high gain and longer timescale responses. Using our mean-field theory we show how correlated stochastic spiking activity among the excitatory neurons can destroy the line attractor, yet this can be mitigated when correlated inputs are shared across the excitatory and inhibitory neurons. Altogether, we provide an alternative learning framework based on homeostasis, where a tunable and flexible assembly structure is possible.

---

## 论文详细总结（自动生成）

# 论文总结

## 1. 研究背景与核心问题
- **背景**：大脑中的记忆被认为以“神经元集群”（高度互连的神经元群体）的形式存储，其形成依赖于突触可塑性。传统模型多采用 **赫布型兴奋性-兴奋性可塑性**（Hebbian plasticity），使协同活动的神经元之间的连接增强。
- **核心问题**：此类传统模型通常产生 **二元的集群结构**：网络要么处于弱连接状态（无集群），要么突触强度饱和到最大值（形成集群），无法生成连续可调的中间状态。这限制了记忆表征的丰富性和灵活性。
- **研究目标**：探索能否通过引入稳态可塑性机制，使集群结构突破二元限制，实现稳定、灵活且可调控的突触连接连续统。

## 2. 方法论与技术要点
- **核心思想**：将 **赫布型兴奋性-兴奋性可塑性** 与 **抑制性-兴奋性稳态可塑性** 结合。前者根据共同活动调整兴奋性突触权重，后者通过抑制性突触的可塑性将兴奋性神经元的放电率稳定在目标值 $r_{\text{target}}$。
- **稳态合规条件**：设兴奋性-兴奋性可塑性的 **增强（potentiation）** 与 **抑制（depression）** 过程在 $r_{\text{target}}$ 处恰好平衡。这意味着当网络达到目标放电率时，兴奋性突触权重不再有净变化。
- **模型与理论工具**：
  - 使用 **脉冲神经元网络模型（spiking neuron models）** 进行数值模拟。
  - 发展相应的 **平均场理论（mean-field theory）**，将突触权重空间中的动力学投影为低维方程，识别出 **线吸引子（line attractor）**：一组连续的稳定权重状态，使网络可停留在任意耦合强度上。
- **关键公式/机制**：沿该线吸引子，尽管放电率被稳态固定不变，但网络的动态增益（gain）和响应时间尺度随总兴奋性耦合强度连续变化，实现功能可塑性。

## 3. 实验设计与对比
- **模拟场景**：采用循环连接的兴奋性（E）和抑制性（I）脉冲神经元网络，不依赖外部数据集，以理论驱动的数值实验为主。
- **对比基准**：与 **仅含传统Hebbian可塑性（无稳态抑制可塑性）** 的网络进行对比，后者必然收敛到二分状态。
- **核心实验**：
  - 展示所提网络在权重空间中自发收敛到线吸引子，突触强度形成连续分布。
  - 分析沿吸引子的网络响应特性（增益、时间常数）如何连续变化。
  - 研究随机脉冲输入的 **共享相关性** 对线吸引子稳定性的影响：若相关性仅存在于兴奋性神经元之间，会破坏吸引子；若相关性被兴奋性和抑制性神经元共享，则可缓解破坏。

## 4. 资源与算力
- **文中未明确说明**所用计算资源（GPU 型号、数量、训练时长等）。由于工作属于理论神经科学范畴，以数值模拟和平均场分析为主，对算力的需求通常不高，文中并未提供相关细节。

## 5. 实验充分性分析
- **实验组数**：论文虽未列出具体数字，但从描述可知包含多组控制实验：
  - 有无稳态可塑性的对比；
  - 不同网络耦合强度下的动态特性扫描；
  - 有无共享相关输入对线吸引子结构的影响。
- **充分性与客观性**：作为一项以机理揭示为主的理论建模研究，实验设计紧扣提出的线吸引子假设，通过理论与模拟相互印证，覆盖了核心主张的关键方面。对比清晰，控制变量合理。但缺乏与生物实验数据的直接拟合或跨模型泛化测试，这符合此类研究的常规范围。

## 6. 主要结论与发现
- **突破二元限制**：稳态可塑性实现了兴奋性突触权重的 **连续稳定分布**，集群结构不再是非弱即强的极端状态，而是 **可调谐、灵活的**。
- **线吸引子机制**：突触权重空间中的线吸引子使网络可以稳定在任意耦合强度，赋予记忆形成以连续的容量和表达空间。
- **功能解耦**：稳态固定放电率的同时，网络动态特性（增益、时间尺度）可独立调节，即“表征”与“动力学”解耦。
- **相关性影响的缓解**：当相关输入在 E/I 神经元间共享时，线吸引子对破坏性波动更具鲁棒性，暗示生物网络中 E-I 共享输入可能是稳定连续吸引子的设计原则。

## 7. 论文优点
- **理论创新**：将稳态可塑性引入Hebbian学习框架，提出“稳态合规”条件，成功解释了连续吸引子如何自然涌现。
- **机制清晰**：通过平均场理论给出简洁的线吸引子数学图像，增强了模型的可解释性。
- **功能启示**：揭示了记忆基底不必是离散、饱和的集群，而可以是连续可变的“耦合度”，为记忆的泛化、消退和上下文调制提供了新视角。
- **生物学合理性**：稳态可塑性在生物大脑中广泛存在，将其纳入集群形成模型提升了生物学保真度。

## 8. 不足与局限
- **简化假设**：模型使用简化的脉冲神经元和平均场近似，可能忽略真实神经元中复杂的树突整合、短期可塑性等细节。
- **缺乏行为/数据验证**：研究停留在理论层面，未与实际的神经元群体记录数据（如记忆任务中观察到的集群活动）直接对照。
- **相关输入的处理**：虽然分析了共享输入的保护作用，但未系统探讨更一般的噪声结构或异质输入对线吸引子的影响。
- **可塑性规则的具体形式**：依赖于兴奋性可塑性在精确目标放电率处平衡，生物中该平衡可能随神经调质状态漂移，模型的鲁棒性有待进一步检验。

（完）
