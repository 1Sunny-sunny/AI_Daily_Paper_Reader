---
title: Hill-Based Reformulation of the Hodgkin-Huxley Model for Interpretable Neuronal Excitability
title_zh: 基于希尔函数的Hodgkin-Huxley模型重构以实现可解释的神经元兴奋性
authors: "Saab, B., Fahs, J., Daou, A."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.06.730614v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 基于Hill方程的HH模型重构用于可解释的神经元兴奋性
tldr: 霍奇金-赫胥黎模型的门控方程基于经验拟合，缺乏生物学解释性。本研究提出Hill函数重述框架，用Hill型S形函数替代激活和失活曲线，拟合更优且保留原始行为。该框架将门控参数与放电特征关联，揭示了兴奋性表型的调节机制，为可解释建模提供途径。
source: biorxiv
selection_source: fresh_fetch
motivation: 经典HH模型的门控速率方程完全基于经验拟合，缺乏生物学解释性，难以推广到不同细胞类型。
method: 采用Hill型sigmoid函数重述HH模型的稳态激活与失活曲线，并对钠失活速率进行重构，通过系统基准测试验证拟合优势。
result: Hill函数在所有门控目标上均优于四种紧凑型sigmoid替代方案，混合模型成功重现了原始模型的尖峰波形和频率-电流关系。
conclusion: Hill-based重述将门控参数与兴奋性表型直接联系起来，为构建细胞特异性电导模型和解析神经功能变化提供了可解释的框架。
---

## 摘要
基于电导的神经元兴奋性模型关键取决于描述电压依赖性离子通道门控的数学形式。经典的Hodgkin-Huxley（HH）形式体系采用根据枪乌贼巨轴突数据拟合的经验速率表达式，这些表达式不易跨细胞类型迁移，也难以通过可测量的门控特性进行解释。在此，我们引入一种基于希尔函数的HH模型重构，其中稳态钠和钾激活曲线以及钠失活速率使用希尔型S形函数重新表达，这是一个具有生物学动机的函数族，广泛用于描述酶动力学、基因调控和受体结合中的协同与饱和过程。与四种紧凑的S形替代方案的系统基准比较表明，希尔函数在所有三个目标上对原始HH导出的门控数据提供了更优的拟合。由此得到的混合模型再现了典型的锋电位波形和频率-电流行为，保留了原始模型的广泛输入-输出组织。重要的是，这种重构将特定的门控参数与放电机制和锋电位特征联系起来，揭示了激活、失活和陡度的变化如何系统性地重塑兴奋性表型。通过使通道动力学与神经元输出之间的关系更加透明，该框架为将基于电导的模型适应于细胞特异性的兴奋性和神经功能中通道依赖的变化提供了一条可解释的途径。

## Abstract
Conductance-based models of neuronal excitability depend critically on the mathematical form used to describe voltage-dependent ion channel gating. The classical Hodgkin-Huxley (HH) formalism employs empirically derived rate expressions fitted to squid giant axon data that are not readily transferable across cell types or interpretable in terms of measurable gating properties. Here we introduce a Hill-based reformulation of the HH model in which steady-state sodium and potassium activation curves and the sodium inactivation rate are recast using Hill-type sigmoidal functions, a biologically motivated family widely used to describe cooperative and saturating processes in enzyme kinetics, gene regulation, and receptor binding. Systematic benchmarking against four compact sigmoid alternatives demonstrates that Hill functions provide superior fits to the original HH-derived gating data across all three targets. The resulting hybrid model reproduced canonical spike waveforms and frequency-current behavior, preserving the broad input-output organization of the original model. Importantly, the reformulation linked specific gating parameters to firing regimes and spike features, revealing how shifts in activation, inactivation, and steepness can systematically reshape excitability phenotypes. By making the relationship between channel kinetics and neuronal output more transparent, this framework provides an interpretable route for adapting conductance-based models to cell-specific excitability and channel-dependent changes in neural function.