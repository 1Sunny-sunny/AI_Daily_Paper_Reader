---
title: Tuning Diversity Improves Discrimination and Detection Performance under Metabolic Constraints
title_zh: 在代谢约束下，调谐多样性改善辨别和检测性能
authors: "Ringach, D."
date: 2026-07-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.29.735317v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 研究皮层群体调谐多样性以提升判别性能
tldr: 皮层神经元调谐特性多样，其功能是特性还是缺陷存在争议。本研究在代谢约束下，构建编码圆形变量的异质与均质群体模型，比较发现异质群体在相同发放预算下判别和检测性能更优，均质调谐不稳定。结果表明进化压力促使调谐异质化以优化编码性能。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究调谐多样性是否有利于群体编码及在代谢约束下的意义。
method: 构建编码圆形变量的异质与均质调谐群体模型，在相同代谢成本下比较两者的判别与检测性能。
result: 异质调谐群体的判别和检测性能均优于同等规模的均质群体。
conclusion: 均质调谐在代谢约束下不稳定，进化压力推动调谐向异质化发展以提升编码性能。
---

## 摘要
皮层神经元群体表现出广泛的调谐特性，这引出了一个问题：这种变异性是皮层功能的特性还是缺陷。先前的研究表明，调谐多样性可以通过减轻相关噪声的影响，并增加几何表征的辨别和识别能力来改善群体编码。受这些发现的启发，我们研究了一个模型，其中编码一个圆形变量的异质调谐曲线族，在等间距的首选角度上复制。我们证明，这个异质群体在相同的脉冲预算下，比由该族平均调谐曲线的平移副本构建的等规模同质群体实现了更好的辨别和检测。因此，在保持平均调谐曲线的扰动下，同质调谐是不稳定的，因为这种扰动在保持代谢成本不变的同时提高了编码性能。我们提出，这种不稳定性产生了朝向调谐异质性的演化压力，使其普遍性成为在代谢约束下优化编码性能过程的结果。

## Abstract
Cortical populations exhibit a wide range of tuning properties, raising the question of whether such variability is a feature or a bug of cortical function. Prior work has shown that tuning diversity can improve population codes by mitigating the effects of correlated noise and increasing the discrimination and identification capacity of geometric representations. Motivated by these findings, we study a model in which a heterogeneous family of tuning curves, coding for a circular variable, is replicated at equally spaced preferred angles. We show that this heterogeneous population achieves better discrimination and detection than an equally sized homogeneous population constructed from shifted copies of the family's mean tuning curve, while using the same spike budget. Thus, homogeneous tuning is unstable under perturbations that preserve the mean tuning curve, because such perturbations leave metabolic cost unchanged while improving coding performance. We propose that such instability creates evolutionary pressure toward heterogeneity of tuning, making its prevalence a consequence of a process that optimizes coding performance under metabolic constraints.