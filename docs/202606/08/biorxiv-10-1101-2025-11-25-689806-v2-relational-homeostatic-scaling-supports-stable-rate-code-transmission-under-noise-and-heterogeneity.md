---
title: Relational homeostatic scaling supports stable rate-code transmission under noise and heterogeneity
title_zh: 关系性稳态缩放支持噪声与异质性下的稳定率码传输
authors: "Li, H., McDougal, R. A."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.25.689806v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 关系型稳态缩放实现稳定发放率传输
tldr: 为解释神经回路在噪声和异质性下实现稳定速率码传输的机制，引入关系型稳态缩放——一种局部突触规则，根据传入与传出活动痕迹调整兴奋性权重，无需全局目标。分析表明该规则能自发驱动网络进入临界传输状态，与STDP兼容且稳定资格迹，为速率码传输提供新基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 经典可塑性规则无法自行建立稳定速率码传输所需的突触耦合机制。
method: 提出关系型稳态缩放，突触后神经元通过缩小近期AMPA加权传入活动与自身活动痕迹的差异来调整总兴奋性强度。
result: 该规则使权重趋向临界区间，对异质性和噪声稳健，与STDP协同工作且稳定三因子学习中的资格迹。
conclusion: 关系型稳态缩放构成神经回路稳定速率码传输的潜在底层机制。
---

## 摘要
通过神经回路可靠地传输放电率信号需要突触耦合保持在由神经元异质性和噪声所塑造的狭窄范围内。在此范围之外，经典理论预测活动将消散或放大为同步。已有研究表明，稳定的率码传输在生物学上是可实现的，但如何建立所需的工作范围仍待解答。典型可塑性规则，包括赫布可塑性和传统稳态缩放，自身无法恢复这一范围。因此，我们引入了关系性稳态缩放，这是一种局部突触缩放规则，其中每个突触后神经元调整其总的兴奋性传入强度，以减少近期AMPA加权的传入活动痕迹与近期突触后活动痕迹之间的差异。这些痕迹共同捕捉了近期进入和离开神经元的速率，而无需全局速率目标。平均场分析和模拟显示，该规则能够在不精确权重初始化的情况下将突触权重驱动至临界状态。该规则对神经元异质性保持鲁棒性，能与脉冲时序依赖可塑性结合而不扰乱赫布竞争，并稳定三要素学习规则所需的资格迹。这些发现表明，关系性稳态缩放可能为神经回路中的稳定率码传输提供基础。

## Abstract
Reliable transmission of firing-rate signals through neural circuits requires synaptic coupling to remain within a narrow regime shaped by neuronal heterogeneity and noise. Outside this regime, classical theory predicts that activity will dissipate or amplify into synchrony. Studies have shown that stable rate-code transmission is biologically achievable, but they leave open how the required operating regime is established. Canonical plasticity rules including Hebbian plasticity and conventional homeostatic scaling do not by themselves recover this regime. We therefore introduce relational homeostatic scaling, a local synaptic scaling rule in which each postsynaptic neuron adjusts its total excitatory afferent strength to reduce the discrepancy between a recent AMPA-weighted afferent activity trace and a recent postsynaptic activity trace. Together, these traces capture the recent rate entering and leaving the neuron without requiring a global rate target. Mean-field analysis and simulations show that this rule drives synaptic weights toward the critical regime without precise weight initialization. The rule remains robust to neuronal heterogeneity, composes with spike-timing-dependent plasticity without disrupting Hebbian competition, and stabilizes the eligibility trace required by three-factor learning rules. These findings suggest that relational homeostatic scaling may provide a substrate for stable rate-code transmission in neural circuits.