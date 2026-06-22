---
title: Inhibitory Gain and Hub Architecture Confer Dynamic Resilience to Microcircuit Degeneration
title_zh: 抑制性增益与枢纽架构赋予微环路退化动态韧性
authors: "Mengiste, S. A. A., Aertsen, A., Kumar, A., Battaglia, D. A."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732346v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 脉冲网络中的脉冲编码原理
tldr: 该研究探讨了神经环路在结构退化时为何仍能保持功能稳定，发现鲁棒性取决于抑制性神经元是否处于结构中心。通过大规模脉冲网络模拟突触与神经元退化，揭示抑制性增益在环路架构中的嵌入方式决定了网络能否维持正常发放、同步水平和信息带宽，其中总有效突触耦合是关键结构描述符，为从结构退化预测动力学变化提供了框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究神经环路在大量突触和神经元损失下仍维持稳定集体动力学的结构原理。
method: 使用大规模脉冲网络，系统比较了突触和神经元退化模式下的经验和合成微环路架构，并分析了结构描述符。
result: 抑制性神经元占据中心位置的网络稳健维持功能，总有效突触耦合是主导结构描述符，而缺乏此类嵌入的架构则出现严重动力学扰动。
conclusion: 抑制性架构是环路动态鲁棒性的机制性决定因素，提供了一个预测结构退化影响的统一框架。
---

## 摘要
神经退行性疾病逐步移除突触和神经元，然而神经回路尽管遭受实质性结构损失，仍能保持稳定的集体动力学。何种结构原理赋予这种韧性仍不清楚。我们使用涵盖经验和合成微环路架构的大规模脉冲网络，在受控修剪策略下系统比较了突触和神经元两种退化模式。我们发现韧性并非仅由连接损失决定，而是取决于抑制性增益如何嵌入回路架构。抑制性神经元占据结构中心位置的网络能够在退化阶段稳健地维持类似健康的放电率、同步水平和信息带宽，而缺乏这种嵌入的架构则表现出放大的动力学扰动。在不同机制下，活动的演化由一组紧凑的权重感知结构描述符组织，这些描述符在不同的网络规模和类别中具有普遍性，其中总有效突触耦合提供了一个主要组织轴。这些结果确定了抑制性架构是回路韧性的机制性决定因素，并提供了一个将结构退化与集体动力学联系起来的预测框架。

## Abstract
Neurodegeneration progressively removes synapses and neurons, yet neural circuits can retain stable collective dynamics despite substantial structural loss. Which structural principles confer this resilience remained unclear. Using large-scale spiking networks spanning empirical and synthetic microcircuit architectures, we systematically compared synaptic and neuronal modes of degeneration under controlled pruning strategies. We found that resilience was not determined by connectivity loss alone, but by how inhibitory gain was embedded within circuit architecture. Networks in which inhibitory neurons occupied structurally central positions robustly maintained health-like firing rates, levels of synchrony, and informational bandwidth across degeneration stages, whereas architectures lacking such embedding exhibited amplified dynamical disruption. Across regimes, the evolution of activity was organized by a compact set of weight-aware structural descriptors that generalized across network sizes and classes, with total effective synaptic coupling providing a dominant organizing axis. These results identified inhibitory architecture as a mechanistic determinant of circuit resilience and provided a predictive framework linking structural degeneration to collective dynamics.