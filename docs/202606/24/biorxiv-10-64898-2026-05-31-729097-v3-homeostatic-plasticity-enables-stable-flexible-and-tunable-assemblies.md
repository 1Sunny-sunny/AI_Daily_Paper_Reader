---
title: "Homeostatic Plasticity Enables Stable, Flexible, and Tunable Assemblies"
title_zh: 稳态可塑性支持稳定、灵活且可调的神经元集群
authors: "Miller, M. C., Miehl, C., Doiron, B."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729097v3.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 通过Hebbian和稳态可塑性研究神经集群形成，与群体编码相关
tldr: 传统基于Hebbian可塑性的神经元集合模型往往产生二元连接强度。本研究引入稳态抑制性可塑性，使兴奋性神经元放电率稳定在目标值，并在“稳态符合”条件下，发现突触权重存在连续的线吸引子，从而实现了连续可调的集合结构。该框架下，网络动态特性（如增益和时间尺度）可变，为灵活、稳定的记忆形成提供了新机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统Hebbian学习模型导致神经元集合连接强度呈二元分化，缺乏灵活性和可调性。
method: 采用脉冲神经元循环网络，结合兴奋性Hebbian可塑性与稳态抑制性可塑性，并运用平均场理论分析。
result: 在稳态符合条件下，突触权重空间形成线吸引子，使集合强度连续可调，放电率稳定但网络响应动态特性可变。
conclusion: 稳态可塑性为突触权重提供了连续稳定流形，使得神经元集合既稳定又灵活可调，为大脑学习机制提供了新见解。
---

## 摘要
强相互连接的神经元群体，称为集群，通过突触可塑性机制动态形成，并被认为是大脑中记忆的基质。许多集群形成模型使用赫布兴奋性-兴奋性可塑性，其中协调活动加强循环结构。然而，这些模型通常产生二元的集群结果：网络要么具有弱连接（无集群），要么具有最大强度连接（集群）。我们考虑结合赫布兴奋性-兴奋性可塑性和抑制性-兴奋性突触及可塑性共同作用的网络，该可塑性稳态地将兴奋性神经元发放稳定在目标值上。当我们将兴奋性-兴奋性可塑性设为稳态顺从，即增强和压抑在稳态目标发放率下达到平衡时，我们发现突触强度存在一个稳定的连续统，并且集群结构不再是二元的。我们使用脉冲神经元模型的循环网络和相关的平均场理论，识别出该连续统为突触权重空间中的线吸引子。虽然沿着吸引子，稳态确保神经元发放率不变，但网络的动态响应特性相当可塑，强耦合网络具有高增益和更长的时间尺度响应。利用我们的平均场理论，我们展示了兴奋性神经元之间的相关随机脉冲活动如何破坏线吸引子，但当相关输入在兴奋性和抑制性神经元之间共享时，这可以得到缓解。总之，我们提供了一个基于稳态的替代学习框架，其中可调且灵活的集群结构是可能的。

## Abstract
Strongly interconnected neuronal populations, called assemblies, dynamically form through synaptic plasticity mechanisms and are thought to be a substrate for memories in the brain. Many assembly formation models use Hebbian excitatory-to-excitatory plasticity, where coordinated activity strengthens recurrent structure. However, these models typically yield binary assembly outcomes: networks with either weak (no assembly) or maximally strong (assembly) connectivity. We consider networks with a combination of Hebbian excitatory-to-excitatory plasticity and inhibitory-to-excitatory synapses with plasticity that homeostatically stabilizes excitatory neuron firing at a target value. When we set excitatory-to-excitatory plasticity to be homeostatically compliant, in that potentiation and depression are balanced at the homeostatic target firing rate, we find a stable continuum of synaptic strengths, and assembly structure is no longer binary. We use a recurrent network of spiking neuron models and an associated mean-field theory to identify this continuum as a line attractor in synaptic weight space. While along the attractor, homeostasis ensures that neuronal firing rates are invariant, the dynamical response properties of the network are quite malleable, with strongly coupled networks having high gain and longer timescale responses. Using our mean-field theory we show how correlated stochastic spiking activity among the excitatory neurons can destroy the line attractor, yet this can be mitigated when correlated inputs are shared across the excitatory and inhibitory neurons. Altogether, we provide an alternative learning framework based on homeostasis, where a tunable and flexible assembly structure is possible.