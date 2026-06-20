---
title: A Structural Principle for Macroscopic Neural Dynamics Correlations
title_zh: 宏观神经动力学关联的结构原理
authors: "Wu, Q., Wen, Q., Liu, C."
date: 2026-06-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.14.729168v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 输入连接度与神经动力学相关性的数学原理
tldr: 大脑结构如何产生大规模神经动力学校正是一个核心问题。本研究利用动态平均场理论与随机网络仿真，发现“耦合相关”——脑区输入连接剖面的相似性——是关键结构决定因素，并与动力学校正呈近似线性映射。生物结构连接的重尾特征谱对维持跨物种强而尺度不变的功能相关至关重要，为解释结构-功能关系提供量化框架，并得到人、小鼠、果蝇数据验证。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示大脑结构连接产生大规模神经动力学校正的机制，填补现有现象学相关缺乏第一性原理解释的空白。
method: 采用动态平均场理论推导、随机神经网络数值仿真，并利用人类、小鼠、果蝇的多模态结构连接与神经活动数据进行实证验证。
result: 发现耦合相关阵的谱型决定结构-功能映射形式：重尾谱导致近似线性关系，且重尾谱是维持经验数据中强、尺度不变的动态相关之必要条件。
conclusion: 该结构原理为定量链接脑结构连接组与涌现神经动力学提供了机制性框架，可能推广至其他复杂网络系统。
---

## 摘要
神经科学的一个核心问题是，大脑的结构连接如何产生其涌现的、相关的动态。这些大尺度的动力学相关性构成了支持认知功能的功能网络。在此，我们将耦合相关性——即脑区输入连接模式之间的相似性——确定为宏观神经动力学相关性的关键结构决定因素。利用动力学平均场理论（DMFT）和随机神经网络模型的数值模拟，我们证明耦合相关性定量地支配着动力学相关性。这种结构-功能映射的函数形式由耦合相关矩阵的特征值谱决定：具有体特征谱的网络显示出精确的线性关系，而生物学上合理的重尾谱则产生近似线性的映射，除非耦合相关性的幅度接近一致。特别地，重尾谱对于再现经验数据中观察到的耦合相关性的适当幅度和尺寸不变性是必要的，从而维持非零的动力学相关性，这可能支持大系统中的脑功能。近似线性的理论预测在使用包括人类、小鼠和果蝇的结构耦合和神经动力学经验数据集的情况下得到了一致的验证。总之，这些结果提供了一个机制性和定量的框架，将宏观脑网络结构与涌现的神经动力学联系起来——这是朝着大脑结构-功能关系理论迈出的重要一步。

显著性声明：大脑的连接如何产生其协调活动是神经科学中一个未解决的基本问题。先前的工作已经确定了结构和功能连接之间的相关性，但这些关系缺乏机制性的、第一原理的解释。在这里，我们利用动力学平均场理论和随机神经网络模型推导出一个分析框架，表明单个结构统计量——耦合相关性，即脑区输入连接模式之间的相似性——线性地且因果地决定了神经动力学相关性的幅度。我们进一步表明，生物结构连接中的重尾特征值谱对于维持跨物种观察到的强、尺寸不变的功能相关性是必要的。在人类、小鼠和果蝇中使用多种成像和连接组学模式验证，这一原理可能提供一个结构连接组学和涌现的脑动力学之间的定量桥梁，其影响扩展到广泛的复杂网络系统类别。

## Abstract
A central question in neuroscience is how the brains structural connectivity gives rise to its emergent, correlated dynamics. These large-scale dynamical correlations underlie functional networks that support cognitive functions. Here, we identify coupling correlation--the similarity between the input connectivity profiles of brain regions--as a key structural determinant of macroscopic neural dynamical correlation. Using dynamical mean-field theory (DMFT) and numerical simulations of random neural network models, we demonstrate that coupling correlation quantitatively governs dynamical correlation. The functional form of this structure-function mapping is dictated by the eigenvalue spectrum of the coupling correlation matrix: networks with bulk eigenspectra exhibit an exact linear relationship, whereas biologically plausible long-tailed spectra yield an approximately linear mapping except when the magnitude of coupling correlation approaches unity. Particularly, a long-tailed spectrum is necessary to reproduce the appropriate magnitude and size-invariance of coupling correlations observed in empirical data, thereby sustaining non-vanishing dynamical correlations that may support brain function in large systems. The theoretical prediction of approximate linearity is consistently validated using empirical datasets that include both structural coupling and neural dynamics in humans, mice, and Drosophila. Together, these results provide a mechanistic and quantitative framework linking macroscopic brain network structure to emergent neural dynamics--an essential step toward a theory of structure-function relationship in the brain.

Significance StatementHow the brains wiring gives rise to its coordinated activity is a fundamental unsolved problem in neuroscience. Prior work has identified correlations between structural and functional connectivity, but these relationships lacked a mechanistic, first-principles explanation. Here, we derive an analytical framework using Dynamical Mean-Field Theory and random neural network models to show that a single structural statistic--coupling correlation, the similarity between the input connectivity profiles of brain regions--linearly and causally determines the magnitude of correlated neural dynamics. We further show that a long-tailed eigenvalue spectrum in biological structural connectivity is necessary to sustain the strong, size-invariant functional correlations observed across species. Validated in humans, mice, and Drosophila using multiple imaging and connectome modalities, this principle may provide a quantitative bridge between structural connectomics and emergent brain dynamics, with implications extending to a broad class of complex networked systems.