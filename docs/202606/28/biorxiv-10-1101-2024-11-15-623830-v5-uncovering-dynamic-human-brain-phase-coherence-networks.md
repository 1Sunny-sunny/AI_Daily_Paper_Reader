---
title: Uncovering dynamic human brain phase coherence networks
title_zh: 揭示动态人脑相位相干网络
authors: "Olsen, A. S., Brammer, A., Fisher, P. M., Moerup, M."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.1101/2024.11.15.623830v5.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 引入了用于脑信号动态相位一致性网络的混合模型
tldr: 复杂认知功能依赖脑区协调通信，但传统振幅相关分析易受干扰。本文提出复角中心高斯混合模型，通过建模脑信号相位直接研究大规模同步动态网络。应用于fMRI数据，该模型无需任务标签即可识别重复出现的同步状态，能可靠区分认知任务并泛化至新个体，揭示了相位信息在揭示脑动态协调中的价值。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统脑功能连接依赖振幅相关性，对噪声和头动敏感，难以捕捉动态相位同步。
method: 引入复角中心高斯混合模型，从脑信号相位角度建模全脑动态相干网络。
result: 模型识别出可区分的重复性状态，能泛化到未见个体并区分不同认知任务。
conclusion: 相位建模为大规模神经同步动态研究提供了干净有效的新途径。
---

## 摘要
复杂的认知功能依赖于分布式脑区之间的协调通信，然而捕捉这些随时间演化的相互作用仍然极具挑战。传统的功能性脑连接分析主要依赖于信号幅度的相关性，这些相关性对噪声和头动等伪迹较为敏感。在此，我们引入一种混合建模方法，聚焦于脑信号的相位，从而能够直接且全面地研究大脑相位相干网络中的大规模同步动态模式。我们为相位建模奠定了数学和概念基础，并引入复角中心高斯混合模型，提供了一种分析全脑相位交互的原则性方式。应用于功能磁共振成像数据时，该模型识别出全脑同步活动的重复状态，这些状态能够可靠地区分认知任务，并泛化到先前未见过的个体，且训练期间无需任何任务标签。这些结果表明，对信号相位建模为观察大脑同步动力学提供了一种清晰且信息丰富的视角，为研究大规模神经协调开辟了新途径。

## Abstract
Complex cognitive functions rely on coordinated communication between distributed brain regions, yet capturing these interactions as they evolve over time remains challenging. Traditional analyses of functional brain connectivity largely rely on correlations in signal amplitude, which are sensitive to noise and artifacts such as head motion. Here, we introduce a mixture modeling approach that focuses on the phase of brain signals, allowing dynamic patterns of large-scale synchronization in brain phase coherence networks to be studied directly and in their entirety. We lay the mathematical and conceptual groundwork for phase modeling and introduce the complex angular central Gaussian mixture model, providing a principled way to analyze phase-based interactions across the brain. Applied to fMRI data, the model identifies recurring states of brain-wide synchronized activity that reliably distinguish cognitive tasks and generalize across previously unseen individuals, without requiring any task labels during training. These results show that modeling signal phase offers a clean and informative view of brain synchronization dynamics, opening new avenues for studying large-scale neural coordination.