---
title: A Computational Perspective on the No-Strong-Loops Principle in Brain Networks
title_zh: 从计算视角看脑网络中的“无强环路”原则
authors: "Hadaeghi, F., Fakhar, K., Khajehnejad, M., Hilgetag, C."
date: 2026-06-11
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.24.678310v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 脑网络不对称性对记忆容量的计算建模
tldr: 哺乳动物脑皮层网络遵循“无强环路”原则，即前馈连接强于反馈，但其计算功能未知。本研究通过计算建模，分析稀疏、模块化、分层递归神经网络，发现连接不对称性可提升工作记忆容量和表征多样性，而增加互惠性则降低性能；在猕猴、狨猴、大鼠和小鼠的脑连接组上验证了该规律，揭示了限制强互惠回路在稀疏网络中带来计算优势，为人工神经网络提供生物启发设计思路。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究脑网络中“无强环路”原则（前馈连接强于反馈）的实际计算影响。
method: 采用储层计算模型，系统构建并比较稀疏、模块化、分层等不同拓扑结构的递归网络，并在多种哺乳动物脑连接组数据上验证。
result: 连接不对称性支持高工作记忆容量，增加互惠性显著降低记忆容量和表征多样性，稀疏模块分层网络仅在限制互惠时性能最优。
conclusion: 限制强互惠回路可提升稀疏脑网络的信息处理效率，这一原则可作为稳定高效人工神经系统的设计准则。
---

## 摘要
哺乳动物大脑的皮层网络表现出非随机组织结构，其中交互投射虽然广泛存在，但在强度上系统性地不对称：前馈连接始终强于其反馈对应物，特别是在感觉皮层。这种“无强环路”原则被认为可以防止过度兴奋并维持稳定，但其实际的计算影响尚不清楚。在此，我们使用计算分析和建模表明，连接不对称性支持高工作记忆容量，而在递归神经网络的储备池计算模型中，增加互惠性会降低记忆容量和表征多样性。我们系统地研究了受哺乳动物皮层连接启发的合成架构，并发现稀疏、模块化和分层网络相对于随机、小世界或核心-外围图实现更优的性能，但仅在限制互惠性时如此。在有向的哺乳动物（猕猴、狨猴、大鼠和小鼠）连接组上验证后，这些结果表明，限制互惠基序在稀疏网络中产生功能益处，这与大脑中稳定、高效信息处理的进化策略一致。这些发现为人工神经系统提出了一种受生物启发的设计原则。

## Abstract
Cerebral cortical networks in the mammalian brain exhibit a non-random organization in which reciprocal projections, although widespread, are systematically asymmetric in strength: feedforward connections are consistently stronger than their feedback counterparts, particularly in sensory cortices. This ``no-strong-loops'' principle is thought to prevent runaway excitation and maintain stability, yet its actual computational impact remains unclear. Here, we use computational analysis and modeling to show that connectivity asymmetry supports high working-memory capacity, whereas increasing reciprocity reduces memory capacity and representational diversity in reservoir-computing models of recurrent neural networks. We systematically examine synthetic architectures inspired by mammalian cortical connectivity and find that sparse, modular, and hierarchical networks achieve superior performance, relative to random, small-world, or core-periphery graphs, but only when reciprocity is constrained. Validated on directed mammalian (macaque, marmoset, rat, and mouse) connectomes, these results indicate that restricting reciprocal motifs yields functional benefits in sparse networks, consistent with an evolutionary strategy for stable, efficient information processing in the brain. These findings suggest a biologically-inspired design principle for artificial neural systems.