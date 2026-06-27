---
title: "Getting Blood from a Stone: Improving Neural Inferences without Additional Neural Data"
title_zh: 从石头里榨血：不增加神经数据而改进神经推断
authors: "Halpern, D. J., Gureckis, T. M."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.1101/2021.01.21.427334v4.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 利用行为数据改进神经推断
tldr: 认知神经科学常因统计效力低受限，传统方案是增加昂贵神经数据。本文提出仅收集额外行为数据并采用替代估计器，即可更经济地提升神经影像推断精度。通过模拟与数学推导，证实了解行为边际分布能改善认知-神经映射的推断，效益取决于估计目标和参数，为研究设计提供了调节行为被试数的新自由度。
source: biorxiv
selection_source: fresh_fetch
motivation: 认知神经科学文献普遍存在低统计效力，传统方法需增加神经数据，但成本高昂且不易实施。
method: 通过模拟实验和数学推导，分析利用行为数据及替代估计器改进神经推断的理论基础与效果。
result: 在现实条件下，额外行为数据能像增加神经数据一样提高推断精度，且成本更低、更易获取，收益大小取决于估计量和研究参数。
conclusion: 研究者可在神经成像研究设计中平衡扫描被试与外部行为被试的数量，以低成本提升统计效力。
---

## 摘要
近年来，认知神经科学文献因包含许多低统计效力的研究而受到批评，这限制了进行可靠统计推断的能力。通常，提高统计效力的建议是收集更多的神经信号数据。然而，许多认知神经科学研究使用从行为数据估计的参数来推断神经信号（如fMRI BOLD信号）。在本文中，我们探讨了认知神经科学家如何仅通过收集行为数据，并使用旨在利用这些信息的替代估计量，来获取更多有关其神经影像信号的知识。我们通过模拟和数学推导证明，对行为边际分布的更多了解可以改进关于认知过程与神经数据之间映射的推断。我们分析了这种益处的幅度，发现它取决于所需的估计目标和几个潜在的研究参数。尽管在许多情况下，精确度的绝对增益可能不大，但我们的结果表明，在现实情境下，额外的行为数据可以比从神经影像研究中收集更多被试数据更便宜、更便捷地带来相同的推断精确度提升。这意味着，在进行神经影像研究时，研究人员现在在设计分析中有了另一个可调因素：在扫描仪内收集的被试数量与在扫描仪外（实验室或在线）收集的行为被试数量。

## Abstract
In recent years, the cognitive neuroscience literature has come under criticism for containing many low-powered studies, limiting the ability to make reliable statistical inferences. Typically, the suggestion for increasing power is to collect more data with neural signals. However, many studies in cognitive neuroscience use parameters estimated from behavioral data in order to make inferences about neural signals (such as fMRI BOLD signal). In this paper, we explore how cognitive neuroscientists can learn more about their neuroimaging signal by collecting data on behavior alone and using alternative estimators designed to leverage this information. We demonstrate through simulation and mathematical derivations that knowing more about the marginal distribution of behavior can improve inferences about the mapping between cognitive processes and neural data. We analyze the magnitude of this benefit, finding that it depends on the desired estimand and several underlying study parameters. While in many cases the absolute gains in precision can be modest, our results demonstrate that, in realistic settings, additional behavioral data can lead to the same improvement in the precision of inferences more cheaply and easily than collecting additional data from subjects in a neuroimaging study. This means that when conducting a neuroimaging study, researchers now have another knob to turn in a design analysis: the number of subjects collected in the scanner and the number of behavioral subjects collected outside the scanner (in the lab or online).