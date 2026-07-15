---
title: "On the Optimal Temporal Resolution for Information Representation in Neural Activity: A Theoretical Analysis"
title_zh: 神经活动信息表征的最优时间分辨率：一个理论分析
authors: "Ahmed, H. F., Samiei, T., Nozari, E."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.19.726394v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 神经信息表征最优时间分辨率的理论分析
tldr: "神经信息表征的最优时间尺度选择缺乏理论解释，近期实验发现中尺度解码最优。本文构建多尺度模型，将神经活动按时间分辨率划分，建模信号与噪声的自相关衰减，推导解码敏感度（d'）的封闭表达式。分析表明：当信号与噪声自相关均衰减时，适度时间整合使中尺度最优；否则最优在微观或宏观极端。该框架揭示了时间整合的权衡机制，解释了预处理操作（如binning、平滑）对解码的影响，并提供跨系统可检验的预测。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-19-726394-v2/fig-001.webp\", \"caption\": \"Figure 1. Schematic of the computational framework used for relating temporal scale and information content in neural representations. (a) Spiking activity of N hypothetical neurons is shown over b microscale time bins and represented (integrated) at four different temporal resolutions. Each scale of temporal integration is illustrated by colored blocks, each forming one bin at the respective scale. (b) The temporally integrated neural activity at each scale is hyperdimensionally encoded into a D-dimensional representation called a trial hypervector (Eq. (2)). The similarities of pairs of trial hypervectors are then computed using inner products, both for the case pairs that belong to the same class (vc s and v̂c s) and those that belong to two different classes (vc s and v̂c′ s ), and referred to as P c s and Px s , respectively. (c) The amount of overlap between the distributions of P c s and Px s , measured by the sensitivity index d′, determine the ability of a normative decoder to decode stimulus condition c from neural representations at that scale.\", \"page\": 6, \"index\": 1, \"width\": 927, \"height\": 816}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-19-726394-v2/fig-002.webp\", \"caption\": \"Figure 2. Empirical validation of theoretical expressions for sensitivity index across temporal scales. (a) Heatmaps of empirical and theoretical sensitivity index d′ at the macroscale, together with the difference between the two, shown over the full range of (ρ, β) parameter space. (b–d) Corresponding heatmaps and differences for the coarse mesoscale, fine mesoscale, and microscale representations, respectively.\", \"page\": 14, \"index\": 2, \"width\": 924, \"height\": 969}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-19-726394-v2/fig-003.webp\", \"caption\": \"Figure 3. Optimal temporal resolution for information representation under persistent signal autocorrelations. (a) Regional depictions of the pairwise comparisons under persistent signal and decaying noise autocorrelations and varying number b of microscale time bins. Pairwise comparisons are shown between micro-, fine meso-, coarse meso-, and macroscale (cf. Eq. (21)). The boundary curves indicates the correlation values where Fs>s′\", \"page\": 18, \"index\": 3, \"width\": 1050, \"height\": 1178}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-19-726394-v2/fig-004.webp\", \"caption\": \"Figure 4. Optimal temporal resolution for information representation under decaying signal autocorrelations. (a) Similar to 3(a) but showing the pairwise comparisons of optimal regions for decaying noise and signal autocorrelations given by Eq. (23). Here boundary curves are given by Gs>s′\", \"page\": 20, \"index\": 4, \"width\": 1050, \"height\": 1171}]"
motivation: 尽管实验观察到神经解码在中间时间尺度达到最优，但缺少理论阐明其涌现条件和机制。
method: "构建多尺度神经群体活动模型，参数化信号与噪声的时间自相关，推导不同时间分辨率下的解码敏感度（d'）解析式。"
result: 信号与噪声自相关均衰减时，适度时间整合产生中尺度最优解码；否则最优在极端时间尺度。
conclusion: 时间整合作为链接多尺度神经动力学与信息表征的关键机制，解释了预处理操作的解码增益或损害，可指导跨模态神经数据分析。
---

## 摘要
引言：尽管神经活动跨越多个时间和空间尺度进行组织，但决定跨尺度信息表征的原则仍不清楚。特别地，虽然近期的实证结果报告了神经解码中中尺度最优性，但尚无理论解释可以说明这类中间尺度何时以及为何会成为最优。在此，我们建立了一个分析框架，以确定神经信息表征的最优时间尺度及其对信号和噪声动力学的依赖性。材料与方法：我们构建了一个多尺度模型，其中神经群体活动由在微观、粗中观、细中观和宏观分辨率下的时间编码试次向量表示。神经响应被建模为受时间相关噪声污染、依赖于刺激的平均激活，信号和噪声的自相关衰减率被参数化地改变。表征质量使用敏感度指标（d-prime）量化，衡量最优解码器区分刺激条件的能力。结果：我们推导出每个时间尺度上敏感度指标的闭式表达式，并指出信号和噪声自相关是可解码性的关键决定因素。然后，我们用合成神经数据的经验可解码性估计验证了理论预测。在不同信号和噪声自相关组合下比较这些表达式，揭示了两个主要机制。首先，当信号和噪声相关性随时间不存在或持续存在时，最优分辨率落在两个极端之一：如果信号自相关显著强于（或弱于）噪声自相关，则最优为宏观尺度（或微观尺度）。当信号和噪声自相关都衰减时，时间整合产生一种权衡：适度的整合通过抑制噪声同时保留一致信号来提高可解码性，而过度的整合则损害信号和可解码性。因此，仅在后一种机制下，中尺度表征在广泛的生物学合理参数范围内成为最优机制。讨论：这项工作为最优时间尺度如何依赖于信号和噪声自相关之间的相互作用提供了理论解释。该框架将时间整合确立为连接多尺度神经动力学与信息表征的原理性机制，解释了诸如分箱和平滑等预处理操作何时增强或降低可解码性，并为跨记录模态和神经系统提供了可检验的预测。

## Abstract
Introduction: Although neural activity is organized across multiple temporal and spatial scales, the principles determining information representation across scales remain unclear. In particular, while recent empirical results have reported mesoscale optimality in neural decoding, no theoretical accounts exist that can explain when and why such intermediate scales emerge as optimal. Here, we develop an analytical framework to determine optimal temporal scales of neural information representation and their dependence on signal and noise dynamics. Materials and Methods: We formulate a multiscale model where neural population activity is represented by temporally encoded trial vectors at micro-, coarse meso-, fine meso- and macroscale resolutions. Neural responses are modeled as stimulus-dependent mean activations corrupted by temporally correlated noise, with signal and noise autocorrelation decay rates varied parametrically. Representational quality is quantified using the sensitivity index (d-prime), measuring the ability of an optimal decoder to distinguish stimulus conditions. Results: We derive closed-form expressions for the sensitivity index at each temporal scale and identify signal and noise autocorrelations as key determinants of decodability. We then validate our theoretical predictions against empirical decodability estimates from synthetic neural data. Comparing these expressions under various combinations of signal and noise autocorrelations across time reveals two main regimes. First, when signal and noise correlations are absent or persistent over time, the optimal resolution falls at one of the two extremes: macroscale (resp. microscale) if signal autocorrelations are significantly stronger (resp. weaker) than noise autocorrelations. When both signal and noise autocorrelations decay, temporal integration creates a trade-off: moderate integration improves decodability by suppressing noise while preserving coherent signal, whereas excessive integration degrades signal and decodability. Therefore, only in the latter regime, mesoscale representations emerge as the optimal regime across a broad range of biologically plausible parameters. Discussion: This work provides a theoretical explanation for how optimal temporal scales depend on the interplay between signal and noise autocorrelations. The framework establishes temporal integration as a principled mechanism linking multiscale neural dynamics to information representation, explains when preprocessing operations such as binning and smoothing enhance or degrade decodability, and provides testable predictions across recording modalities and neural systems.

---

## 论文详细总结（自动生成）

好的，这是根据您提供的论文内容生成的结构化中文总结。

### 1. 论文的核心问题与整体含义

*   **研究动机**：神经活动在不同时间和空间尺度上组织，但目前缺乏理论原则来解释信息在这些尺度上如何表征，以及哪个尺度能最有效地捕捉与行为相关的信息。特别是，近期实验发现在中尺度（mesoscale）进行神经解码效果最优，这背后的理论机制尚不明确。
*   **核心问题**：本文旨在从理论上阐明神经信息表征的最优时间尺度，并解释这种最优尺度如何由神经信号（任务相关信息）和噪声（任务无关变异性）的时间自相关结构决定。
*   **整体含义**：论文构建了一个统一的理论框架，将时间整合（即平均）视为连接多尺度神经动力学与信息表征的关键操作。它量化分析了平均操作对信号和噪声的“双刃剑”效应，为理解何时以及为何中间时间分辨率会成为信息表征的最优选择提供了第一性原理的解释。

### 2. 论文提出的方法论

*   **核心思想**：构建一个多尺度模型，通过比较在不同时间分辨率（微观、细中观、粗中观、宏观）下神经活动表征的刺激解码准确度，来分析时间整合的影响。解码准确度由刺激条件间的可分离性决定，而后者又由信号和噪声的时间自相关结构共同塑造。
*   **关键技术细节**：
    1.  **神经活动模型**：
        *   将每个试次的群体神经活动建模为 $n_i^c = \mu_i^c + \sigma y_i^c$，其中，$\mu_i^c$ 是条件 $c$ 下时刻 $i$ 的刺激依赖性信号成分，$\sigma y_i^c$ 是噪声成分。
        *   噪声的跨时间自相关被建模为指数衰减，由参数 $\rho$ 控制其衰减率：$Cov(Y^c) = \Sigma_t \otimes R_N$，其中 $\Sigma_t$ 的第 $(i,j)$ 个元素为 $\rho^{|j-i|}$。
        *   信号成分 $\mu_i^c$ 的跨时间自相关被建模为两种：**持久性相关**（$\langle \mu_i^c, \mu_j^c \rangle / (\lVert \mu_i^c \rVert \lVert \mu_j^c \rVert) = \beta$）和 **衰减性相关**（$\langle \mu_i^c, \mu_j^c \rangle / (\lVert \mu_i^c \rVert \lVert \mu_j^c \rVert) = k\beta^{|j-i|}$），$\beta$ 控制衰减率。
    2.  **多尺度表征**：原始数据（微观尺度）通过不同窗口大小的平均操作，生成细中观、粗中观和宏观尺度的整合活动向量。
    3.  **解码框架**：
        *   为消除不同尺度下输入维度差异对解码器带来的混淆，使用**超维计算**将各尺度的活动向量无损地编码到统一高维空间中的试次超向量 $v_s^c$。
        *   解码能力通过**敏感度指标 d' **来度量，它直接关联最优贝叶斯解码器的准确度。$d'$ 定义为同一条件下试次超向量内积（$P_s^c$）和不同条件下试次超向量内积（$P_s^x$）的均值差与合并标准差的比值：
            $$ d'_s = \frac{E[P_s^c] - E[P_s^x]}{\sqrt{\frac{1}{2}(\text{Var}(P_s^c) + \text{Var}(P_s^x))}} $$
    4.  **理论推导**：基于上述模型，分别在每个时间尺度下推导出 $d'$ 的闭式表达式（定理 1-4）。这些表达式将 $d’$ 显式地表示为信号和噪声自相关参数（$\beta, \rho$）以及试次时长（$b$）的函数。

### 3. 实验设计

*   **模型与分析**：本文是**纯理论研究**，主要实验为数学推导和数值模拟，不涉及真实神经数据集。
*   **数值验证**：为验证推导出的闭式表达式，作者生成了**合成神经数据**。数据根据其统计模型生成，参数 $\rho$ 和 $\beta$ 在 $[0, 0.99]$ 范围内变化，共模拟 $N=50$ 个神经元，$b=20$ 个微观时间点。
*   **基准测试**：该研究没有与外部方法进行基准测试，其核心是比较**理论预测值与经验估计值**。经验估计值是从60个合成试次中计算得到的样本 $d'$，理论值则来自推导的解析式。通过比较这两者的热力图，验证了理论公式的正确性。
*   **对比分析**：研究的核心是对比不同时间尺度（微观、细中观、粗中观、宏观）下的理论最优性。作者定义了成对比较函数 $\mathcal{F}_{s > s‘}^b(\rho, \beta)$ 和 $\mathcal{G}_{s > s’}^b(\rho, \beta)$，通过分析这些函数在 $(\rho, \beta)$ 参数空间中的符号，来确定哪个尺度具有最大的 $d'$，从而划分出最优尺度的区域。

### 4. 资源与算力

*   文中**未明确提及**任何关于计算资源（如 GPU 型号、数量、训练时长）的细节。该研究为理论和数值模拟，计算量相对较小，不依赖于大规模深度学习训练，因此算力不是核心关注点。

### 5. 实验数量与充分性

*   **主要分析场景**：论文系统分析了四种核心场景，覆盖了从简单到复杂的信号和噪声相关性组合：
    1.  **情况 1**：信号与噪声皆无时间相关性（$\beta=0, \rho=0$）。
    2.  **情况 2**：信号完全相关，噪声无时间相关性（$\beta=1, \rho=0$）。
    3.  **情况 3**：信号自相关持久，噪声自相关指数衰减（$\beta \in [0,1), \rho \in [0,1)$）。
    4.  **情况 4**：信号与噪声自相关均指数衰减（$\beta, \rho \in [0,1)$）。
*   **参数化分析**：在情况 3 和 4 中，作者在完整的 $(\rho, \beta)$ 参数空间以及不同试次时长 $b$ 和初始衰减因子 $k$ 下，分析了最优尺度的变化。
*   **充分性与公平性**：该研究遍历了理论模型中的关键参数，系统地覆盖了从极端情况到更接近生物现实的广泛场景，分析是充分且自洽的。作为理论研究，其公平性体现在所有尺度的分析均基于同一套严密的数学推导和假设之上。

### 6. 论文的主要结论与发现

1.  **决定因素**：神经信息表征的最优时间尺度并非固定不变，而是由信号和噪声跨时间的自相关结构（即信号与噪声的相关性衰减率）动态决定。
2.  **极端情况的最优性**：当信号自相关**持久存在**时，最优尺度落在两个极端。若信号自相关显著强于噪声自相关，则宏观尺度最优；反之，则微观尺度最优。中观尺度永远不会是最优的。
3.  **中观尺度最优性的涌现**：**只有当信号和噪声的自相关都随时间衰减时，中观尺度表征才可能成为最优**。这种最优性在信号自相关衰减缓慢、而噪声自相关衰减迅速的生物合理参数区间内鲁棒地出现。
4.  **时间整合的权衡机制**：时间整合是一把双刃剑。适度整合能有效抑制快速衰减的噪声，同时保留部分一致的信号，从而提高信噪比。然而，过度整合会抹去信号中随时间衰减的精细结构，导致信号自身被“平均掉”，降低可解码性。中观尺度最优性是这一权衡达到最佳平衡点的结果。
5.  **理论验证与解释**：该理论框架不仅验证了此前关于中观尺度解码最优性的实证发现，还为理解为何神经数据处理中常用的分箱、平滑等预处理操作有时有效、有时无效提供了原理性解释。

### 7. 优点

*   **理论严密性**：从第一性原理出发，推导出多尺度下解码敏感度的闭式解，提供了精确的、可量化的预测。
*   **解释力强**：成功为已有的经验观察（中观尺度最优性）提供了清晰的理论基础和涌现条件。
*   **框架通用性**：提出的框架不依赖于特定的数据结构或大脑区域，适用于不同神经记录模态和任务条件。
*   **方法论创新**：通过超维计算编-解码方案，巧妙地分离了信息内容与输入维度对解码器性能的影响，使得跨尺度比较更加客观、纯粹。

### 8. 不足与局限

*   **模型假设的限制**：为获得解析解，模型对神经活动的统计结构做了简化假设，如假定噪声自相关为指数衰减、忽略神经元间的空间相关性（$R_N = I_N$）、并主要假设信号与噪声不相关。真实神经数据可能更复杂。
*   **实验覆盖度**：作为纯理论研究，该工作完全建立在合成数据和数学证明之上，未在任何真实神经数据集上验证其理论预测与实际解码性能的关系（尽管它引用和解释了已有的实验发现）。
*   **维度问题**：当前模型仅探讨了时间尺度，没有同时将空间尺度的整合纳入同一个优化框架。
*   **应用限制**：直接应用该理论来指导真实实验数据分析，需要预知或能准确估计数据中信号和噪声的时间自相关结构，这在实践中可能具有挑战性。

（完）
