---
title: Generating whole-brain neural activity and behavior through unified latent dynamics
title_zh: 通过统一潜在动力学生成全脑神经活动与行为
authors: "Nuzzi, D., Mattia, M., Pezzulo, G."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.05.730482v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 从潜在动态生成全脑神经活动和行为的生成模型
tldr: 神经科学面临高维神经活动与行为如何从共享底层动力学中涌现的挑战。本研究提出NEBULA生成框架，基于线虫全脑记录，学习统一潜在动力学，实现长时间神经与行为轨迹生成、真实行为模拟及靶向虚拟干预，扰动揭示行为转捩点，引导干预实现状态操控，为脑-行为链接和可扩展虚拟实验奠定基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 理解高维神经活动与行为如何从共享动力学涌现是构建活体数字孪生的关键挑战。
method: 提出NEBULA框架，通过统一潜在动力学联合建模全脑神经活动与行为，使用线虫全脑记录训练。
result: 模型支持长期神经行为轨迹生成、真实模拟和虚拟干预，扰动揭示行为转捩点，引导干预实现无重训状态操控。
conclusion: 建立了连接脑动力学与行为的框架，为神经科学可扩展虚拟实验提供基础。
---

## 摘要
理解高维神经活动与行为如何从共享的底层动力学中涌现，仍然是神经科学中的一个基本挑战。解决这一问题对于构建能够忠实地重现和预测活体系统多尺度脑-行为动态的数字孪生至关重要。在此，我们提出NEBULA（通过统一潜在动力学进行神经与行为建模），这是一个联合建模全脑神经活动与行为的生成式框架。利用秀丽隐杆线虫的全脑记录，该模型学习了一个统一的潜在动力学结构，能够支持神经和行为轨迹的长期生成、行为的真实模拟以及有针对性的虚拟干预。对学习到的动力学进行扰动揭示了与行为相关的转换点，而引导干预则无需重新训练即可实现对神经和行为状态的受控操纵。这些结果建立了一个将大脑动力学与活体生物行为联系起来的框架，并为神经科学中的可扩展虚拟实验奠定了基础。

## Abstract
Understanding how high-dimensional neural activity and behavior emerge from shared underlying dynamics remains a fundamental challenge in neuroscience. Addressing this problem is key to enabling digital twins that can faithfully reproduce and predict the multiscale brain-behavior dynamics of living systems. Here we present NEBULA (NEural and Behavioral modeling through Unified LAtent dynamics), a generative framework that jointly models whole-brain neural activity and behavior. Using brain-wide recordings from C. elegans, the model learns a unified latent dynamical structure that supports long-horizon generation of neural and behavioral trajectories, realistic simulations of behavior, and targeted virtual interventions. Perturbations of the learned dynamics reveal behaviorally relevant transition points, whereas steering interventions enable controlled manipulation of neural and behavioral states without retraining. These results establish a framework for linking brain dynamics to behavior in a living organism and provide a foundation for scalable virtual experimentation in neuroscience.