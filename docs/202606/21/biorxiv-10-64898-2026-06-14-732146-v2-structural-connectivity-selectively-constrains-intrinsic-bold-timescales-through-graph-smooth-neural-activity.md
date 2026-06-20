---
title: Structural Connectivity Selectively Constrains Intrinsic BOLD Timescales through Graph-Smooth Neural Activity
title_zh: 结构连接通过图平滑神经活动选择性限制内在BOLD时间尺度
authors: "Bashirgonbadi, A., salehi, m., Soltanian-Zadeh, H."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732146v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 图信号处理框架将结构连接与BOLD时间尺度联系起来
tldr: 本研究采用图信号处理框架，将静息态BOLD信号建模为结构连接组上的图信号，并分解为结构耦合与解耦成分。通过分析100名健康被试的数据发现，固有时间尺度与结构连接强度的正相关主要由结构耦合信号驱动，解耦信号相关性较弱，且慢速解耦活动优先出现在高级联合皮层。该结果揭示了结构网络拓扑如何通过图平滑神经活动选择性约束脑信号的时间统计特性。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索结构连接网络如何约束脑信号的时间统计特性。
method: 利用扩散MRI和静息态fMRI数据，将BOLD信号进行图信号分解，分析固有时间尺度与节点结构连接强度的关系。
result: 结构耦合信号的固有时间尺度与结构连接强度呈稳健正相关，解耦信号相关性弱，且慢速解耦动力在高级皮层更显著。
conclusion: 结构网络拓扑通过图平滑神经活动选择性地约束了脑信号的时间尺度。
---

## 摘要
结构连接定义了支持大规模脑动态的网络架构，然而该网络如何约束其上定义信号的时间统计特征仍不甚明了。此前研究报道了静息态fMRI的内在时间尺度与结构连接强度之间的关联，但尚不清楚哪些信号成分主要驱动了这一关系。本研究采用图信号处理框架，分析网络化脑信号的内在时间特性。将区域血氧水平依赖(BOLD)活动建模为结构连接组上的图信号，并通过图谱滤波分解为低频(结构耦合)和高频(结构解耦)成分。利用人类连接组计划中100名无关参与者的扩散MRI结构连接与静息态fMRI数据，在控制区域体积的同时，通过相对低频功率量化内在时间尺度，并将其与节点结构连接强度相关联。结果表明，源自结构耦合信号的内在时间尺度在群体和个体间水平上均与结构连接强度呈稳健正相关，而结构解耦信号则表现出明显较弱的耦合。值得注意的是，缓慢的结构解耦动态优先在高级联合皮层中表达。图谱零模型进一步表明，这些效应关键依赖于结构网络的经验组织。总体而言，这些结果建立了结构-时间尺度耦合的图谱解释，表明网络拓扑结构选择性限制图平滑神经活动的时间统计特性。

## Abstract
Structural connectivity defines the network architecture supporting large scale brain dynamics, yet how this network constrains the temporal statistics of signals defined on it remains poorly understood. Prior work has reported associations between intrinsic timescales of resting-state fMRI and structural connectivity strength, but it is unclear which signal components primarily drive this relationship. Here, we adopt a graph signal processing framework to analyze intrinsic temporal properties of networked brain signals. Regional Blood Oxygenation Level Dependent (BOLD) activity is modeled as a graph signal supported on the structural connectome and decomposed via graph spectral filtering into low-frequency (structure-coupled) and high-frequency (structure-decoupled) components. Using diffusion MRI derived structural connectivity and resting-state fMRI from 100 unrelated participants of the Human Connectome Project, intrinsic timescales are quantified using relatively low-frequency power and related to node-wise structural connectivity strength while controlling for regional volume. We show that intrinsic timescales derived from structure-coupled signals exhibit robust positive associations with structural connectivity strength at both group and inter individual levels, whereas structure decoupled signals display substantially weaker coupling. Notably, slow structure decoupled dynamics are preferentially expressed in higher order association cortex. Graph spectral null models further demonstrate that these effects critically depend on the empirical organization of the structural network. Together, these results establish a graph spectral interpretation of structure timescale coupling, showing that network topology selectively constrains the temporal statistics of graph smooth neural activity.