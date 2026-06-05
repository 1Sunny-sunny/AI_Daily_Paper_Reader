---
title: HCN channels enhance synchrony propagation in heterogeneous synfire chains
title_zh: HCN通道增强异质性同步链中的同步传播
authors: "Saini, S., Narayanan, R."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.728444v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 研究前馈网络中的同步传播和时间编码
tldr: 本研究利用大规模电导模型，在噪声高传导的异质性前馈链中探索同步脉冲传播。发现传播具有概率性，背景波动决定成败；增加异质性不改变平均效能但减少网络间变异性；HCN通道通过慢动力学显著增强传播可靠性，揭示了其关键调节作用和神经计算的简并性原理。
source: biorxiv
selection_source: fresh_fetch
motivation: 皮质回路中同步脉冲的可靠传递机制，尤其在存在内在异质性和高传导状态的活体条件下仍不清楚。
method: 利用随机搜索算法构建生理上有效的异质性神经元群体，并组织成前馈synfire链，在噪声环境中测试脉冲包传播。
result: 同步传播为概率性过程，背景活动导致随机成败；异质性增加不改变平均传播效能但稳定网络间变异性；HCN通道通过慢动力学增强传播可靠性。
conclusion: HCN通道是同步信息传递的关键调节器，揭示了内在传导、输入特性、异质性和背景活动间的相互作用，并凸显了简并性作为神经计算的基本原理。
---

## 摘要
动机：皮层回路中的信息流和时间编码关键依赖于精确时间同步脉冲模式的可靠传递。尽管皮层神经元集群在显著的内在异质性和随机高导状态条件下仍能实现这一传递，但在体内条件下有效同步传播的机制仍然知之甚少。方法：本研究利用大规模、基于电导的兴奋性和抑制性神经元模型，构建了前馈同步链，并在嘈杂、高导状态下运行，以填补这一空白。采用独立的随机搜索算法，我们首先识别出生理上有效的异质性皮层神经元群体。兴奋性和抑制性群体均表现出细胞尺度的简并性，即不同的生物物理分子组合产生标志性的生理特征。然后，我们用这些群体构建了具有不同异质性程度的同步链，并评估了不同脉冲包在神经元集群间的传播。结果：我们发现同步传播本质上具有概率性，揭示了一条随机分界线，它将始终成功传播的输入模式与始终失败的输入模式分开。这条分界线的随机特性凸显了背景突触波动的关键作用，确定了一个区域，其中相同的输入在不同试验中由于随机背景活动而交替成功或失败传播。比较具有不同内在异质性程度的网络，我们发现增加异质性并不改变平均传播效能，但减少了网络间的变异性，表明内在多样性具有稳定作用。引人注目的是，当我们测试神经元内在特性对同步传播的影响时，超极化激活环核苷酸门控（HCN）通道在所有异质性条件下都成为同步传播的稳健增强剂。在机制上，HCN电导的缓慢恢复动力学缩窄了脉冲启动的时间窗口，锐化了输出同步性，并提高了传播可靠性。当HCN动力学加速时，这一效应消失，突显了这些通道介导的缓慢负反馈的重要性。意义：综合来看，我们的分析确定了HCN通道是同步信息传递的关键调节器，并揭示了内在电导、输入特性、神经元异质性和随机背景活动在塑造皮层同步传播中的强烈相互作用。多样的细胞与网络配置能够实现相似传播效能的能力进一步突显简并性作为调控稳健且灵活神经计算的基本原则。

## Abstract
MotivationInformation flow and temporal coding in cortical circuits depend critically on the reliable transmission of precisely timed synchronous spike patterns. Although cortical assemblies achieve such transmission despite pronounced intrinsic heterogeneities and stochastic high-conductance states, the mechanisms underlying effective synchrony propagation under in vivo conditions remain poorly understood.

MethodologyIn this study, we address this gap using large-scale, conductance-based models of excitatory and inhibitory neurons organized into feedforward synfire chains operating in noisy, high-conductance regimes. Using independent stochastic search algorithms, we first identified physiologically valid heterogeneous populations of cortical neurons. Both excitatory and inhibitory populations exhibited cellular-scale degeneracy, whereby distinct combinations of biophysically identified molecular components produced signature physiological characteristics. We then constructed synfire chains with varying degrees of heterogeneity using these populations and assessed the propagation of different spike packets across neuronal assemblies.

ResultsWe found synchrony propagation to be inherently probabilistic, revealing a stochastic separatrix that separated input patterns that consistently succeeded from those that consistently failed in propagation. The stochastic nature of this separatrix highlighted a critical role for background synaptic fluctuations, defining a regime in which identical inputs alternately propagated or failed across trials solely due to stochastic background activity. Comparing networks with different degrees of intrinsic heterogeneity, we found that increasing heterogeneity did not alter mean propagation efficacy but reduced network-to-network variability, indicating a stabilizing role for intrinsic diversity. Strikingly, when we tested the impact of neuronal intrinsic properties on synchrony propagation, hyperpolarization-activated cyclic nucleotide-gated (HCN) channels emerged as robust enhancers of synchrony propagation across all heterogeneity regimes. Mechanistically, the slow restorative kinetics of HCN conductances narrowed the temporal window for spike initiation, sharpening output synchrony, and improving propagation reliability. This effect was abolished when HCN kinetics were accelerated, underscoring the importance of the slow negative feedback mediated by these channels.

ImplicationsTogether, our analyses identify HCN channels as key regulators of synchronous information transfer and reveal strong interactions among intrinsic conductances, input characteristics, neuronal heterogeneity, and stochastic background activity in shaping cortical synchrony propagation. The ability of diverse cellular and network configurations to achieve similar propagation efficacy further highlights degeneracy as a fundamental principle governing robust and flexible neural computation.