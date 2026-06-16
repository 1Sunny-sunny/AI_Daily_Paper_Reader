---
title: Equivariant neuronal populations enable simultaneous tuning and invariance
title_zh: 等变神经元群体实现同时调谐与不变性
authors: "Hoeller, J., Zhong, L., Heinrich, L., Saalfeld, S., Pachitariu, M., Romani, S."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.1101/2024.08.02.606398v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 等变框架连接视觉视角与神经活动
tldr: 大脑如何同时实现对视角变换的敏感性与场景身份的不变性？本研究提出等变性框架，将神经元群体响应分解为调谐与不变正交子空间。通过小鼠四个视觉皮层区域的大规模记录发现，高阶区域（LM、AL）的等变结构更明显，解释了调谐与不变性的同时提升。相比之下，人工神经网络后期层牺牲调谐换取不变性。这揭示等变性是灵活计算的群体编码原则。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索大脑如何同时实现场景视角不变性与对变换的敏感性，提出等变性可能成为关键机制。
method: 分析小鼠四个视觉皮层区域的大规模神经元记录，分解群体响应为调谐和不变正交子空间，并与人工神经网络对比。
result: 等变结构在高阶区域（LM、AL）更显著，同时提升调谐和不变性；人工神经网络后期层则牺牲调谐换取不变性。
conclusion: 等变性是实现神经元群体灵活计算的重要原则，平衡了调谐与不变性。
---

## 摘要
当我们在世界中移动时，我们从不同视角看到相同的视觉场景。但是，大脑如何编码与视角无关的场景身份，同时对这些变换保持敏感？我们提出了一种通过等变性来实现的解决方案，即视角变换会在神经元群体反应中引起结构化变化。这一框架意味着将群体反应分解为调谐子空间和不变子空间。通过四个小鼠视觉皮层区域的大规模神经元记录来测试我们的框架，我们发现等变结构在一些高阶区域（LM, AL）比在其他区域（V1, RL）更为显著。这种等变结构解释了观察到的群体调谐和不变性同时增强的现象。相比之下，在图像分类任务上训练的人工神经网络的早期层表现出类似的结构，但后期层在增加不变性的同时牺牲了调谐性。这些结果表明等变性是神经元群体实现灵活计算的一项原理。

## Abstract
As we move through the world, we see the same visual scene from different perspectives. But how does the brain encode scene identity invariant to perspective, while remaining sensitive to these transformations? We propose a solution through equivariance, where perspective transformations induce structured changes in neuronal population responses. This framework implies a decomposition of population responses into orthogonal subspaces that are tuned and invariant. Testing our framework with large-scale neuronal recordings across four mouse visual cortical areas, we find that the equivariant structure is more pronounced in some higher-order areas (LM, AL) than in other areas (V1, RL). This equivariant structure accounts for the observed simultaneous increase in both population tuning and invariance. In comparison, early layers of an artificial neural network trained on image classification show similar structure, but later layers increase invariance at the cost of tuning. These results suggest equivariance is a principle to achieve flexible computations with neuronal populations.