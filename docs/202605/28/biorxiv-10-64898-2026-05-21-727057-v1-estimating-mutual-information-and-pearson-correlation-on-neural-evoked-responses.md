---
title: Estimating mutual information and Pearson correlation on neural evoked responses
title_zh: 估计神经诱发响应中的互信息与皮尔逊相关系数
authors: "Hukari, A., Cotroneo, S. F., Salmelin, R."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.21.727057v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 估计神经诱发响应相似性的互信息方法
tldr: 神经诱发反应中的微小时序变化削弱了皮尔逊相关的相似性检测能力，互信息(MI)虽能捕捉非线性依赖，但其估计器在连续数据上的行为不明确。本文通过模拟和真实脑磁图数据，系统比较了皮尔逊相关与三种MI估计器，提出了自适应阈值和参数设置策略，揭示了各度量在灵敏度与信号特性间的权衡，为神经时间序列相似性分析提供了实用指南。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决神经诱发反应中传统相关性度量因时序变化而失效的问题，并克服互信息估计器在连续神经数据上应用缺乏共识的障碍。
method: 使用模拟信号和真实脑磁图数据，系统比较样本皮尔逊相关与三种常见互信息估计器在多种现实变换下的表现。
result: 皮尔逊相关在低噪声线性关系中可靠，而经过参数调整的互信息估计器能稳定捕捉复杂信号依赖，两者存在灵敏度与特性的权衡。
conclusion: 提出了互信息的参数选择和阈值策略，为神经诱发反应相似性分析中相似度量的选择与解释提供了实践指导。
---

## 摘要
在神经诱发响应中，当相同的功能性反应在不同试次、不同实验条件或由不同传感器记录时，可以观察到响应时间或持续时间上的微小变化。这些变化限制了基于相关性的方法检测信号间相似性的能力。互信息（MI）提供了一种替代的相似性度量，能够捕捉线性与非线性依赖关系，但由于在连续数据估计量上缺乏共识，以及对估计量在真实信号上行为的理解有限，其实际应用受到阻碍。在本工作中，我们通过系统比较样本皮尔逊相关性与三种最常用的MI估计量，研究如何估计神经诱发响应的相似性。我们利用模拟信号和真实脑磁图数据来描述它们的行为。在模拟中，我们针对一组描绘神经诱发响应实际变化的变换来测试估计量。随后，我们提出了一些指导原则，用于定义相似性估计的自适应下界，并分析由不同估计量产生的相似性排序。我们的发现揭示了度量灵敏度与不同信号特性之间的权衡。我们证实，皮尔逊相关性在描述低噪声信号的线性关系方面是可靠的，并确定了能够稳定MI估计量的参数设置，使其能够捕捉复杂的信号依赖关系。这些结果共同引入了互信息的实用参数选择和阈值策略，并为在神经诱发时间序列分析中选择和解释相似性度量提供了指导。

## Abstract
In neural evoked responses, small variations in the timing or duration of responses can be observed when the same functional response is recorded in different trials, different experimental conditions or by different sensors. These variations limit the ability of correlation-based methods to detect similarities between signals. Mutual information (MI) provides an alternative similarity measure, capable of capturing both linear and non-linear dependencies, yet its practical use is hindered by lack of consensus on estimators for continuous data and the limited understanding of the behavior of the estimators on realistic signals. In this work, we investigate how to estimate the similarity of neural evoked responses by systematically comparing sample Pearson correlation with three of the most common MI estimators. We describe their behavior using both simulated signals and real magnetoencephalographic data. In the simulations, the estimators are tested against a set of transformations that depict realistic changes in neural evoked responses. Subsequently, we propose guidelines for defining adaptive lower bounds on the similarity estimates and analyzing the similarity rankings induced by the different estimators. Our findings reveal trade-offs between measures sensitivity and different signal properties. We confirm that Pearson correlation is reliable in describing linear relationships for low-noise signals, and we identify parameter settings that stabilize MI estimators, enabling them to capture complex signal dependencies. Together, these results introduce practical parameter choices and thresholding strategies for mutual information and provide guidance for selecting and interpreting similarity measures in the analysis of neural evoked time series.