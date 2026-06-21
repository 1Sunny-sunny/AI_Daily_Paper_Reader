---
title: Quantum machine learning for detection of sleep deprivation from EEG signals
title_zh: 基于EEG信号的睡眠剥夺检测的量子机器学习
authors: "Sarma-Sarkar, P., Saini, R., Roy, P. P."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732153v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 使用量子机器学习从EEG分类睡眠剥夺
tldr: "睡眠剥夺普遍影响健康，EEG可客观评估。本研究采用量子支持向量机和混合量子神经网络，通过提取频谱功率、Hjorth参数等功能连接特征并编码为量子态进行分类。在时段级和受试者级评估中，混合量子神经网络分别取得96.88%和81.25%的最高准确率，优于传统方法，展示了量子机器学习在EEG睡眠剥夺检测中的潜力。"
source: biorxiv
selection_source: fresh_fetch
motivation: 睡眠剥夺普遍存在且影响健康，需要基于EEG的自动化检测方法。
method: 使用量子支持向量机和混合量子神经网络，结合谱特征与功能连接，将经典特征编码为量子态进行分类。
result: "混合量子神经网络在时段级和受试者级准确率分别达96.88%和81.25%，均优于先前方法。"
conclusion: 量子机器学习在EEG睡眠剥夺检测中展现出竞争力，具有生物医学应用前景。
---

## 摘要
据估计，印度约有50%的人口存在睡眠相关障碍。睡眠剥夺是一种普遍存在的状况，会对认知表现、神经功能和整体健康产生不利影响。脑电图（EEG）提供了一种客观的方法来捕捉与睡眠不足相关的神经变化，使其非常适合自动化检测框架。在本研究中，我们探索了使用量子支持向量机（QSVM）和混合量子神经网络（HQNN）对睡眠剥夺和休息良好状态进行分类的方法，利用静息态EEG信号。采用了一个全面的特征提取流程，包括频谱带功率、带比值、Hjorth参数和功能连接度量。这些特征随后被编码为量子态，以构建量子核，然后用于分类。模型性能在时段级和受试者级数据划分方案下进行评估。混合量子神经网络（HQNN）在两种评估设置下均取得了最高的性能，在时段级别达到96.88%的准确率，在受试者级别达到81.25%。QSVM模型在时段级别和受试者级别评估中分别达到了93.75%和75.00%的准确率。在受试者级别和时段级别评估中，HQNN优于先前报道的结果（68.23%和95.72%）。总体而言，这些发现凸显了量子机器学习作为基于EEG的睡眠剥夺检测的一种有竞争力的方法的潜力，对现实世界中的生物医学应用具有广阔前景。

## Abstract
Approximately 50% of the population in India is estimated to experience sleep-related disorders. Sleep deprivation is a prevalent condition that adversely impacts cognitive performance, neural functioning, and overall health. Electroencephalography (EEG) offers an objective means of capturing neural alterations associated with sleep loss, making it well-suited for automated detection frameworks. In this study, we explore the application of a Quantum Support Vector Machine and Hybrid Quantum Neural Networks to classify sleep-deprived and well-rested states using resting-state EEG signals.

A comprehensive feature extraction pipeline is employed, incorporating spectral band power, band ratios, Hjorth parameters, and functional connectivity measures. These features are subsequently encoded into quantum states to construct a quantum kernel, which is then utilized for classification. Model performance is evaluated under both epoch-level and subject-level data partitioning schemes.

The Hybrid Quantum Neural Network (HQNN) achieves the highest performance across both evaluation settings, attaining an accuracy of 96.88% at the epoch level and 81.25% at the subject level. The QSVM model achieves accuracies of 93.75% and 75.00% for epoch-level and subject-level evaluations, respectively. At subject-level and epoch -level evaluation, HQNN outperforms previously reported results (68.23% and 95.72%). Overall, these findings highlight the potential of quantum machine learning as a competitive approach for EEG-based sleep deprivation detection, with promising implications for real-world biomedical applications.