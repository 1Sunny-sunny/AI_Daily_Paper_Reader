---
title: "A unified model of short- and long-term plasticity: Effects on network connectivity and information capacity"
title_zh: 短时与长时可塑性的统一模型：对网络连接与信息容量的影响
authors: "Ahokainen, I., Linne, M.-L."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.07.687160v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 建模尖峰时序依赖可塑性，连接短时和长时动力学
tldr: 现有计算模型常忽略短时程可塑性对长时程可塑性的影响，本研究提出一种统一模型SL-STDP，直接整合短时程动态与长时程STDP，并基于视觉皮层层V数据拟合。将该规则应用于循环网络后发现，神经元自组织形成稳定的发放率集群，且在储备池计算任务中信息容量优于未耦合模型，加入兴奋-抑制易化突触后进一步提升。该工作揭示了短时程动态通过调制长时程可塑性频率依赖性来塑造网络连通性与信息处理。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统STDP模型常忽略短时程可塑性的影响，需要新模型探究短时程动态如何调控长时程可塑性及网络功能。
method: 提出SL-STDP规则，将Tsodyks-Markram短时程模型与突触后长时程可塑性直接耦合，并应用于循环网络模拟和储备池计算评估。
result: SL-STDP网络自组织出稳定的发放率集群，信息容量在多数任务中优于无直接耦合网络，且兴奋-抑制易化突触进一步增强了性能。
conclusion: 短时程可塑性通过改变长时程可塑性的频率依赖性，对循环网络的自组织和信息处理能力起关键作用。
---

## 摘要
活动依赖的突触可塑性是一种基本的学习机制，塑造神经回路的连接与活动。现有的脉冲时序依赖可塑性（STDP）计算模型在不同程度的生物学细节上捕捉长时突触变化。一种常见方法是忽略短时动态对长时可塑性的影响，这可能对某些神经元类型过于简化。因此，需要新的模型来研究短时动态如何影响长时可塑性。为填补这一空缺，我们引入了一种新颖的现象学模型，即短时长时STDP（SL-STDP）规则，该规则直接将Tsodyks-Markram短时动态模型与突触后长时可塑性结合起来。我们根据视觉皮层第5层的记录拟合了新模型，并研究了单个突触中短时可塑性如何影响长时可塑性的发放率频率依赖性。我们的分析揭示，长时可塑性的突触前和突触后频率依赖性在塑造递归神经网络（RNN）的自组织及其通过源和汇节点的涌现进行的信息处理中起着关键作用。我们将SL-STDP规则应用于RNN，发现SL-STDP网络中的神经元自组织成不同的发放率簇，从而稳定了动力学。我们通过加入稳态平衡（即权重归一化和兴奋性-抑制性可塑性）来扩展实验，并观察到SL-STDP网络与没有短时和长时可塑性直接耦合的网络之间度相关性的差异。最后，我们评估了修改后的连接如何在储备池计算任务中影响网络的信息容量。SL-STDP规则在大多数任务中优于非耦合系统，且包含兴奋性-抑制性易化突触进一步提升了信息容量。我们的研究表明，短时动态诱导的长时可塑性频率依赖性变化在塑造网络动态中起关键作用，并将突触机制与RNN中的信息处理联系起来。

## Abstract
Activity-dependent synaptic plasticity is a fundamental learning mechanism that shapes the connectivity and activity of neural circuits. Existing computational models of Spike-Timing-Dependent Plasticity (STDP) capture long-term synaptic changes with varying degrees of biological detail. A common approach is to neglect the influence of short-term dynamics on long-term plasticity, which may be an oversimplification for certain neuron types. Thus, there is a need for new models to investigate how short-term dynamics influence long-term plasticity. To address this gap, we introduce a novel phenomenological model, the Short-Long-Term STDP (SL-STDP) rule, which directly integrates the Tsodyks-Markram model of short-term dynamics with postsynaptic long-term plasticity. We fit the new model to recordings from layer 5 of the visual cortex and study how short-term plasticity affects the firing rate frequency dependence of long-term plasticity in a single synapse. Our analysis revealed that the pre- and postsynaptic frequency dependence of long-term plasticity plays a crucial role in shaping the self-organization of recurrent neural networks (RNNs) and their information processing through the emergence of sinks and source nodes. We applied the SL-STDP rule to RNNs and found that neurons in the SL-STDP network self-organize into distinct firing rate clusters, stabilizing the dynamics. We extended the experiments by including homeostatic balancing, namely weight normalization and excitatory-to-inhibitory plasticity, and observed differences in degree correlations between the SL-STDP network and a network without direct coupling between short-term and long-term plasticity. Finally, we evaluated how the modified connectivity affects the networks' information capacity in reservoir computing tasks. The SL-STDP rule outperformed the uncoupled system in the majority of tasks, and including excitatory-to-inhibitory facilitating synapses further improved information capacity. Our study demonstrates that short-term dynamics--induced changes in the frequency dependence of long-term plasticity play a pivotal role in shaping network dynamics and link synaptic mechanisms to information processing in RNNs.