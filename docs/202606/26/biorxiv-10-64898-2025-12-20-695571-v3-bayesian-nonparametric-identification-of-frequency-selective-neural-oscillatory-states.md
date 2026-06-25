---
title: Bayesian Nonparametric Identification of Frequency-Selective Neural Oscillatory States
title_zh: 贝叶斯非参数方法识别频率选择性神经振荡状态
authors: "Yamada, S., Nagel, S. E., Kobeleva, X., Schmidt, R."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2025.12.20.695571v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 贝叶斯非参数方法从神经数据中识别频率选择性振荡状态
tldr: 针对神经振荡检测中需预定义频带和状态数的问题，本文提出一种贝叶斯非参数方法。通过时间延迟嵌入与狄利克雷过程高斯混合模型结合，可从数据中自动推断振荡状态数目，并捕捉频率特异性特征。在合成数据和脑磁图数据上验证表明，该方法能准确恢复多个频率成分，识别出多种短暂振荡状态及个体差异，为无监督振荡发现提供了新框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有神经振荡检测方法依赖预定义的频带或状态数，易受主观选择影响，并可能导致模型过拟合或欠拟合。
method: 将时间延迟嵌入与狄利克雷过程高斯混合模型结合，利用延迟嵌入捕捉频率特异性局部自协方差结构，并通过狄利克雷过程先验自动推断状态数目。
result: 合成数据中可靠恢复多个频率成分并正确推断状态数；MEG数据识别出多个频率选择性短暂振荡状态及不同非周期状态，并揭示了个体间异质性。
conclusion: 提出了一种无监督贝叶斯非参数框架，无需预定义频带和状态数即可发现频率选择性神经振荡状态，为脑动力学研究提供了新工具。
---

## 摘要
识别神经振荡对于将快速大脑动态与潜在认知过程联系起来至关重要。然而，这具有挑战性，因为振荡事件可能短暂、嵌入在类似1/f的背景活动中，并且可能包含未知数量的频谱上不同的状态。传统方法通常对一个或几个预定义的频带应用窄带带通滤波器，然后使用幅度阈值来识别振荡事件，但检测结果对这些选择可能高度敏感。尽管最近基于隐马尔可夫模型（HMM）的无监督替代方案解决了这些局限性，但它们仍然需要预先指定状态数量，并且当该数量指定错误时可能欠拟合或过拟合。我们提出了一种贝叶斯非参数方法，该方法在直接从数据推断适当状态数量的同时，识别不同的振荡状态。该方法将时间延迟嵌入（TDE）与狄利克雷过程高斯混合模型（DP-GMM）相结合。TDE 通过时间偏移副本增强信号，使 DP-GMM 能够捕获频率特定的局部自协方差结构，而狄利克雷过程先验通过修剪不活跃成分来适应模型复杂性。我们使用模拟神经时间序列（例如脑电图 EEG、脑磁图 MEG 和局部场电位 LFP）的单通道合成数据，将所提方法与基于滤波器的阈值方法以及时间延迟嵌入的 HMM 进行了基准测试，这些数据中包含多个频率成分，并被类似 1/f 的噪声所掩盖。在这种设置下，所提出的模型在噪声条件下可靠地恢复了多个不同的频率成分，同时推断出了振荡状态的数量。应用于静息态运动皮层 MEG 数据集，该模型识别出了多个频率选择性的、短暂的振荡状态，以及具有不同频谱轮廓的明显非周期性状态。这些状态在峰值频率、发生率和功率方面表现出显著的个体间异质性。总之，这提供了一个无监督框架，用于发现频率选择性的振荡状态，无需预定义频带或固定状态数量。

## Abstract
Identifying neural oscillations is essential for linking fast brain dynamics to underlying cognitive processes. However, this is challenging because oscillatory events can be brief, embedded in 1/f-like background activity, and may comprise an unknown number of spectrally distinct states. Conventional approaches often apply narrowband band-pass filters to one or a few predefined frequency bands and then use amplitude thresholding to identify oscillatory events, but detection outcomes can be highly sensitive to these choices. Although recent unsupervised alternatives based on hidden Markov models (HMMs) address these limitations, they still require the number of states to be specified in advance and can underfit or overfit when this number is misspecified. We propose a Bayesian nonparametric method that identifies distinct oscillatory states while inferring an appropriate number of states directly from the data. This method combines time-delay embedding (TDE) with the Dirichlet-process Gaussian mixture model (DP-GMM). TDE augments the signal with time-shifted copies, enabling the DP-GMM to capture frequency-specific local autocovariance structures, while the Dirichlet-process prior adapts model complexity by pruning inactive components. We benchmarked the approach against a filter-based thresholding method and the time-delay embedded HMM using single-channel synthetic data designed to mimic neural time series (e.g., EEG, MEG, and local field potentials), with multiple frequency components masked by 1/f-like noise. In this setting, the proposed model reliably recovered multiple distinct frequency components under noisy conditions while also inferring the number of oscillatory states. Applied to a resting-state motor-cortex MEG dataset, the model identified multiple frequency-selective, short-lived oscillatory states alongside distinct aperiodic states with different spectral profiles. These states exhibited substantial inter-individual heterogeneity in peak frequency, occurrence rate, and power. Overall, this provides an unsupervised framework for discovering frequency-selective oscillatory states without predefining frequency bands or fixing the number of states.