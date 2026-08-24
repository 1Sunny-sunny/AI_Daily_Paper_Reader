---
title: Symbolic regression enables coarse-grained model discovery of intracellular signalling dynamics
title_zh: 符号回归实现细胞内信号传导动力学的粗粒度模型发现
authors: "de Pomereu, T., Fröhlich, F."
date: 2026-08-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.08.20.745973v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 符号回归可推断可解释的粗粒化动力学模型，可迁移用于神经编码模型解释
tldr: 细胞信号动力学建模受限于实验数据与计算资源，常需粗粒度降维，但经典方法依赖强假设。本研究以符号回归作为数据驱动手段，测试信号系统动力学能否在测量变量上紧凑粗粒度，并推断可解释模型。在合成酶系统中恢复米氏动力学，在ERK磷酸化数据中识别紧凑速率定律，表明符号回归可判断粗粒度是否合理并生成机制假设。
source: biorxiv
selection_source: fresh_fetch
motivation: 动态建模对理解癌症中失调的蛋白网络至关重要，但数据与计算限制需要确认部分观测是否支持低维粗粒度描述。
method: 采用符号回归从时间序列数据中自动发现紧凑、可解释的动力学速率定律，并与稀疏神经ODE基线比较。
result: 在合成酶系统恢复米氏动力学，在ERK数据中识别磷酸-ERK紧凑速率定律；符号回归失败时需更多输入的神经ODE，提示动力学更复杂。
conclusion: 符号回归能判断何时可采用紧凑粗粒度模型，为可学习场景提供机制假设，并为不可学习场景提示新测量方向。
---

## 摘要
细胞通过蛋白质网络响应环境，而这些网络在癌症中常发生失调，因此动力学建模至关重要。实验数据和计算资源的局限性促使使用粗粒度方法来构建低维描述。然而，经典的粗粒度建模方法依赖于强假设，使得部分实验观测何时支持系统动力学的简化描述尚不清楚。这里我们表明，符号回归（SR）提供了一种数据驱动的方法，用于检验信号系统动力学是否以及在多大程度上可以在测量变量上进行粗粒度化，并且当可以时，推断出机制上可解释的模型。在合成酶系统中，SR 恢复了两步机制的 Michaelis-Menten 动力学，并在三步扩展下也如此。当数据质量下降时，SR 会简化为有效的动力学定律，同时保持正确的理论极限。将 SR 应用于已发表的时间分辨 ERK 磷酸化数据，可在选定的癌症相关基因过表达背景下识别出紧凑的磷酸化 ERK 速率定律，从而产生可解释的动力学效应。稀疏神经常微分方程基线在 SR 成功的情况下仅需少量输入，但在失败的情况下平均需要更多输入，这表明当简化模型完全可学习时，SR 的失败与简单数学模型无法描述的更复杂动力学相关。总之，这些发现确立了符号回归作为一种方法，用于检验何时紧凑的粗粒度描述是合理的，在成立的情况下产生假设，在不成立的情况下激发潜在的新测量。

## Abstract
Cells respond to their environment through protein networks often dysregulated in cancer, making dynamical modelling crucial. Limitations in experimental data and computational resources motivate coarse-graining methods to build low-dimensional descriptions. Yet classical approaches to coarse-grained modelling rely on strong assumptions, leaving it unclear when partial experimental observations support reduced descriptions of system dynamics. Here we show that symbolic regression (SR) provides a data-driven way to test whether, and how compactly, the dynamics of a signalling system coarse-grain over the measured variables, and, when they do, infers mechanistically interpretable models. In synthetic enzyme systems, SR recovers Michaelis-Menten kinetics for the two-step mechanism and under three-step extensions. As data quality is degraded, SR simplifies toward effective kinetic laws while preserving correct theoretical limits. Applied to published time-resolved ERK phosphorylation data, SR identifies compact phospho-ERK rate laws in selected cancer-relevant gene overexpression contexts, yielding interpretable kinetic effects. A sparse neural ODE baseline requires few inputs where SR succeeds, but on average more where it fails, indicating that, where a reduced model is learnable at all, SR failure is associated with more complex dynamics that a simple mathematical model cannot describe. Together, these findings establish symbolic regression as a way to test when a compact coarse-grained description is warranted, generating hypotheses where one holds and motivating potential new measurements where it does not.