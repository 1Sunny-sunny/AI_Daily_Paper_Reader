---
title: "Sleep to forget: active control of consolidation and forgetting by slow-wave sleep dynamics"
title_zh: 以睡眠来遗忘：慢波睡眠动态对巩固和遗忘的主动控制
authors: "Golden, R., Wei, M., Coury, S., Mizrahi-Kliger, A., Ganguly, K., Bazhenov, M."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732460v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 具有脉冲时序依赖性可塑性的生物物理丘脑皮层网络模型用于研究睡眠相关记忆巩固
tldr: 睡眠中记忆巩固与遗忘的灵活调控机制尚不清楚，近期发现慢波睡眠中的慢波和δ波可能分别促进巩固与遗忘。本研究利用含突触时序依赖可塑性的丘脑皮层网络模型，通过操控钙离子动力学在同一网络产生两种Up状态，模拟序列学习任务，揭示慢波Up状态的长时程允许记忆被选择性再激活而得到保护，δ波则无法支持，且δ波更显著地稀疏化突触表征，最终预测二者比例可灵活调节记忆平衡。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究睡眠中皮层如何通过慢波睡眠的不同波动动态主动控制记忆巩固与遗忘的机制。
method: 使用生物物理丘脑皮层网络模型，结合突触时序依赖可塑性，通过调节锥体细胞钙动力学产生慢波和δ波Up状态，并采用序列学习任务范式进行模拟。
result: 模型重现光遗传学实验发现，即慢波期间的可塑性对记忆巩固至关重要，而δ波期间的可塑性去除反而增强巩固；机制上，慢波Up状态长时程能在干扰后自发再激活记忆痕迹，δ波则不能，且δ波导致更稀疏的突触表征。
conclusion: 慢波与δ波在慢波睡眠期间竞争性调控记忆巩固与遗忘，其相对比例可主动调节突触可塑性，从而灵活控制记忆存储结果。
---

## 摘要
睡眠既支持新记忆的巩固，也促进其他记忆的遗忘，但皮层如何灵活调控这些结果仍知之甚少。近期研究表明，慢波睡眠（SWS）期间两种类型的Up状态可能发挥截然不同且相互竞争的作用：慢波主动巩固记忆痕迹，而delta波则促进记忆痕迹的弱化。本文采用带有脉冲时间依赖可塑性的生物物理丘脑-皮层网络模型，探究这一分离现象背后的突触机制。通过操控皮层锥体细胞的内在Ca2+动力学，我们在单一网络中同时生成了慢波和delta波的Up状态。利用序列学习任务范式，我们重现了光遗传学所揭示的分离现象：在慢波期间移除可塑性会损害记忆，而在delta波期间移除可塑性则增强巩固。从机制上看，模型揭示出较长的慢波Up状态能提供一个自发再激活阶段，该阶段发生在干扰输入之后，在此期间训练后的记忆被选择性再激活并得到保护，而缩短的delta波Up状态则无法支持这一阶段。我们进一步发现，delta波比慢波更能稀疏化突触表征，并预测巩固与遗忘之间的平衡可以通过慢波与delta波在SWS中的比例灵活调节。

## Abstract
Sleep supports both the consolidation of new memories and the forgetting of others, but how the cortex flexibly controls these outcomes remains poorly understood. Recent work has shown that two types of Up states may play distinct, competing roles during slow-wave sleep (SWS): slow waves actively consolidate memory traces, whereas delta waves promote their weakening. Here we use a biophysical thalamocortical network model equipped with spike-timing-dependent plasticity to investigate the synaptic mechanisms underlying this dissociation. By manipulating the intrinsic Ca2+ dynamics of cortical pyramidal cells, we generate both slow and delta wave Up states within a single network. Using a sequence-learning task paradigm we recapitulate the optogenetic dissociation: removing plasticity during slow waves degrades the memory, while removing it during delta waves enhances consolidation. Mechanistically, the model reveals the longer slow wave Up state affords a spontaneous reactivation phase, occurring after the interfering input, during which the trained memory is selectively reactivated and protected, a phase the truncated delta Up state cannot support. We further find that delta waves sparsen the synaptic representation more than slow waves and predict that the balance between consolidation and forgetting can be flexibly tuned by the ratio of slow to delta waves during SWS.