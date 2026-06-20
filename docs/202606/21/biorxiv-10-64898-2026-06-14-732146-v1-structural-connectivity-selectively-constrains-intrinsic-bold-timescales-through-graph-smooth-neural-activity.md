---
title: Structural Connectivity Selectively Constrains Intrinsic BOLD Timescales through Graph-Smooth Neural Activity
title_zh: 结构连接通过图平滑神经活动选择性地约束内源性BOLD时间尺度
authors: "Soltanian-Zadeh, H., Bashirgonbadi, A., salehi, m."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.732146v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 通过图信号处理分析BOLD时间尺度与结构连接的关系
tldr: 结构连接如何约束大脑信号的时间尺度尚不明确。本研究采用图信号处理框架，将BOLD信号分解为结构耦合与解耦成分，发现结构耦合成分的内在时间尺度与结构连接强度显著正相关，解耦成分则较弱，且慢速解耦动态集中在联合皮层。结果表明网络拓扑选择性地约束平滑神经活动的时间统计。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究结构连接网络如何约束大脑内在时间尺度，以及哪些信号成分驱动这种关系。
method: 利用图信号处理将BOLD信号图谱分解为结构耦合（低频）与解耦（高频）成分，分析其内在时间尺度与结构连接强度的关联。
result: 结构耦合信号的内在时间尺度与结构连接强度呈稳定正相关；解耦信号相关性弱，慢解耦动态优先表达在高级联合皮层。
conclusion: 结构网络拓扑通过图平滑机制选择性约束神经活动的时间统计，建立结构-时间尺度耦合的图谱解释。
---

## 摘要
结构连接定义了支持大规模脑动力学的网络架构，然而该网络如何约束其上信号的时间统计特性仍知之甚少。已有研究报告了静息态fMRI内源性时间尺度与结构连接强度之间的关联，但尚不清楚哪种信号成分主要驱动了这种关系。在此，我们采用图信号处理框架来分析网络化脑信号的内源性时间特性。区域血氧水平依赖（BOLD）活动被建模为结构连接组上的图信号，并通过图谱滤波分解为低频（结构耦合）和高频（结构解耦）成分。利用来自人类连接组计划100名无关参与者的扩散MRI衍生结构连接和静息态fMRI，使用相对低频功率量化内源性时间尺度，并关联到节点水平的结构连接强度，同时控制区域体积。我们表明，从结构耦合信号得出的内源性时间尺度在群体和个体间水平上均与结构连接强度呈现稳健的正相关，而结构解耦信号则显示出明显较弱的耦合。值得注意的是，缓慢的结构解耦动态优先表达于高级联合皮层。图谱零模型进一步证明这些效应关键依赖于结构网络的经验组织。总之，这些结果建立了结构-时间尺度耦合的图谱解释，表明网络拓扑结构选择性地约束了图平滑神经活动的时间统计。

## Abstract
Structural connectivity defines the network architecture supporting large scale brain dynamics, yet how this network constrains the temporal statistics of signals defined on it remains poorly understood. Prior work has reported associations between intrinsic timescales of resting-state fMRI and structural connectivity strength, but it is unclear which signal components primarily drive this relationship. Here, we adopt a graph signal processing framework to analyze intrinsic temporal properties of networked brain signals. Regional Blood Oxygenation Level Dependent (BOLD) activity is modeled as a graph signal supported on the structural connectome and decomposed via graph spectral filtering into low-frequency (structure-coupled) and high-frequency (structure-decoupled) components. Using diffusion MRI derived structural connectivity and resting-state fMRI from 100 unrelated participants of the Human Connectome Project, intrinsic timescales are quantified using relatively low-frequency power and related to node-wise structural connectivity strength while controlling for regional volume. We show that intrinsic timescales derived from structure-coupled signals exhibit robust positive associations with structural connectivity strength at both group and inter individual levels, whereas structure decoupled signals display substantially weaker coupling. Notably, slow structure decoupled dynamics are preferentially expressed in higher order association cortex. Graph spectral null models further demonstrate that these effects critically depend on the empirical organization of the structural network. Together, these results establish a graph spectral interpretation of structure timescale coupling, showing that network topology selectively constrains the temporal statistics of graph smooth neural activity.