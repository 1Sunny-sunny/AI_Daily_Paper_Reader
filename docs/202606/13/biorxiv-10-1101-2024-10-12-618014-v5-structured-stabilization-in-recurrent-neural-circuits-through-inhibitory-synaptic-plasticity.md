---
title: Structured stabilization in recurrent neural circuits through inhibitory synaptic plasticity
title_zh: 通过抑制性突触可塑性实现递归神经回路的结构化稳定
authors: "Festa, D., Cusseddu, C., Gjorgjieva, J."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.1101/2024.10.12.618014v5.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 抑制性可塑性塑造脉冲时序模式
tldr: 本文提出一类成对抑制性尖峰时间依赖可塑性规则，实现神经回路的结构化稳定：既能稳定兴奋性活动，又能自组织形成功能连接模式。在不同规模网络中，规则选择导致相互E/I连接或侧抑制，环网络中更形成墨西哥帽状连接，引发情境调制等响应，为皮层计算提供简单可塑性基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 抑制性神经元需同时实现活动稳定化和结构化连接以支持计算功能，但传统稳态可塑性缺乏结构。
method: 提出一类成对抑制性STDP规则，并在小规模E/I电路和大规模环网络中模拟分析其连接和动力学。
result: iSTDP规则可自组织出相互E/I连接或侧抑制；在环网络中形成墨西哥帽式有效连接，产生情境调制和空间模块化活动。
conclusion: 该可塑性规则家族保留了STDP的简单性，同时实现了稳定化和结构化连接，支持涌现网络计算。
---

## 摘要
在皮层回路中，抑制性中间神经元发挥双重作用：它们调节整体活动水平以防止兴奋失控，并参与多样化的计算。非结构化的抑制性突触连接通过稳态调节放电率实现第一个作用，而计算任务通常需要结构化的兴奋-抑制（E/I）连接。在此，我们考虑了一类广泛的成对抑制性脉冲时序依赖可塑性（iSTDP）规则，展示了抑制性连接如何自组织以稳定兴奋并生成功能相关的连接基序——我们将这一过程称为“结构化稳定”。我们表明，在小规模E/I回路和大规模脉冲递归神经网络中，选择不同的iSTDP规则可以导致相互连接的E/I对，或侧向抑制，即抑制性神经元连接到一个没有直接反向连接的兴奋性神经元。在一个一维环形网络中，有两个遵循这些不同iSTDP规则的抑制性亚群，兴奋性单元内的有效连接自组织成墨西哥帽状轮廓，中心为兴奋性影响，远离中心为抑制性影响。这导致涌现的网络响应，例如视觉皮层中的情境调制效应，以及发育期自发活动特征的空间模块化活动。我们的理论工作引入了一类规则，这些规则保留了基于脉冲时序的可塑性的广泛适用性和简洁性，同时稳定活动并促进支持涌现网络计算的特定连接基序。

## Abstract
In cortical circuits, inhibitory interneurons play a dual role: they regulate overall activity levels to prevent runaway excitation, and contribute to diverse computations. While unstructured inhibitory synaptic connections achieve the first role by homeostatically regulating firing rates, computational tasks often require structured excitatory-inhibitory (E/I) connectivity. Here, we consider a broad class of pairwise inhibitory spike-timing dependent plasticity (iSTDP) rules, demonstrating how inhibitory connections can self-organize to both stabilize excitation and generate functionally relevant connectivity motifs--a process we call "structured stabilization". We show that in both small E/I circuits and large spiking recurrent neural networks the choice of iSTDP rule can lead to either mutually connected E/I pairs, or to lateral inhibition, where an inhibitory neuron connects to an excitatory neuron that does not directly connect back to it. In a one-dimensional ring network with two inhibitory subpopulations following these distinct iSTDP rules, the effective connectivity within the excitatory units self-organizes into a Mexican-hat-like profile, with excitatory influence in the center and inhibitory influence away from the center. This leads to emergent network responses such as contextual modulation effects as in the visual cortex and spatially modular activity characteristic of developmental spontaneous activity. Our theoretical work introduces a family of rules that retains the broad applicability and simplicity of spike-timing-based plasticity, while stabilizing activity and promoting specific connectivity motifs which support emergent network computations.