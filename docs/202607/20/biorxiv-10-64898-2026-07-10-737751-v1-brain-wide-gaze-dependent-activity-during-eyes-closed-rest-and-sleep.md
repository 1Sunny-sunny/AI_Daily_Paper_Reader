---
title: Brain-wide gaze-dependent activity during eyes-closed rest and sleep
title_zh: 闭眼静息和睡眠期间全脑范围的注视依赖活动
authors: "Nudelman, Z., Nau, M."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737751v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 从fMRI重建注视行为
tldr: 闭眼状态下，注视行为与大脑活动的耦合关系尚不清楚，主要因为闭眼时难以同步测量眼动和脑活动。本研究利用基于MRI的眼动追踪技术，从fMRI数据重建闭眼休息和睡眠期间的注视行为，发现推断的注视与大脑皮层及小脑的广泛区域活动耦合，这种动态在两个状态中基本持续，且考虑注视会显著改变大尺度功能连接估计，揭示了注视作为内在脑信号隐藏维度的重要性，并为了解闭眼意识状态提供新窗口。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737751-v1/fig-001.webp\", \"caption\": \"Figure 1: Inferring gaze from eye-voxel patterns during eyes-closed rest and sleep. (A) Dataset overview. Concurrent fMRI and EEG were recorded during 15-minute scanning runs in which participants (n=31) attempted to fall asleep. (B) Analysis logic. Gaze dynamics are inferred by comparing eye-voxel patterns across consecutive functional volumes using Pearson correlation. Greater dissimilarity reflects larger displacement of the eyes (1-Pearson’s r). (C) Single-participant example. Gaze predictor for an example participant (Participant 17 Run 3) separated into Wake (blue) and Sleep (orange). (D) Linking gaze to brain activity. The gaze predictor from each run was denoised with respect to head motion parameters, separated by state, convolved with the hemodynamic response function (HRF), and mean-centered. This procedure yielded a final gaze predictor which was then related to brain activity using a voxel-wise general linear model (GLM) analysis.\", \"page\": 3, \"index\": 1, \"width\": 718, \"height\": 544}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737751-v1/fig-002.webp\", \"caption\": \"Figure 2: Widespread gaze-dependent brain activity during eyes-closed rest and sleep. A) Voxel-wise general linear model results estimated for the eye voxel-based gaze predictor in Wake (top) and Sleep (bottom). Maps display group-level results of one-sample t-tests performed against zero using FSL’s FLAMEOmixed-effects model (FLAME 1+2), with cerebral results projected on FreeSurfer’s FSaverage surface and cerebellar results mapped onto SUITPy’s flatmap surface. No t-thresholding was applied in order to show the global topographic organization of effects, with white contours indicating regions surviving False Discovery Rate (31) correction (q < 0.05, cluster extent > 20 voxels). B) Post-hoc regions of interest (ROI) analysis for atlas-defined retinotopic regions displayed on a posterior FSAverage surface (28). Shown are whisker box plots (central line: median; box: 25th and 75th percentile; whiskers: all data not considered outliers; outliers: data points outside 1.5×interquartile range), with color indicating ROI and statistics indicating results of sign-flipping permutation-based (10,000 permutations) two-tailed one-sample tests of subjectlevel t-scores against zero after false-discovery-rate correction (q = 0.05) across ROIs: * p < 0.05, ** p < 0.01, *** p < 0.001. See Table S1 for precise p-values. Eyes-closed gaze-dependent brain activity was distributed across regions involved in vision.\", \"page\": 5, \"index\": 2, \"width\": 898, \"height\": 832}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737751-v1/fig-003.webp\", \"caption\": \"Figure 3: Across-state comparison between Wake vs. Sleep. (A) Searchlight-based local similarity reveals widespread overlap between Wake and Sleep. Statistical maps show the local similarity between the group-level t-statistic results for Wake and Sleep shown in Figure 2. The maps were compared using Pearson correlation (r) within local geodesic searchlights of 23mm radius for the cerebral cortex and 11mm for the cerebellum. Warm colors indicate spatial consistency across states, whereas cool colors indicate localized differences. (B) Comparison of gaze metrics across states. Left panel: across-run mean number of functional volumes in each state. Center and right panels: group-level mean and standard deviation of gaze predictor amplitude, respectively. Dots represent individual participants. No significant differences were found between Wake and Sleep for any of these metrics (one-sample t-tests on pseudo-z scores from within-participant state-flipping permutation tests, all p > 0.05).\", \"page\": 7, \"index\": 3, \"width\": 540, \"height\": 579}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737751-v1/fig-004.webp\", \"caption\": \"Figure 4: Eyes-closed gaze behavior shapes estimates of large-scale brain organization. (A) Analysis logic. BOLD time series were parcellated using the Schaefer 500-parcel atlas (34). Parcel-to-parcel Pearson correlation matrices were computed with and without removing variance explained by the raw and HRF-convolved gaze predictor. (B) Group-level edge-wise differences in functional connectivity. The lower triangle displays the unthresholded group-level mean differences in Pearson correlations between with vs. without gaze denoising; the upper triangle displays edges surviving False Discovery Rate correction at q = 0.05, two-sided sign-flipping permutation test, 10,000 permutations. Red values indicate higher functional connectivity after gaze denoising of each voxel’s time series, with blue indicating the opposite. Results were grouped by the Yeo 7-networks for overview (36), with each network comprising many parcels.\", \"page\": 8, \"index\": 4, \"width\": 898, \"height\": 533}]"
motivation: 探究闭眼休息和睡眠状态下注视行为与全脑活动是否存在耦合，弥补该领域测量方法的不足。
method: 采用可扩展的基于MRI的眼动追踪方法，从fMRI数据中重建闭眼时的注视行为。
result: 推断的注视行为与大脑皮层、小脑等广泛区域活动显著耦合，且该耦合在闭眼休息和睡眠中持续存在，并systematically改变了功能网络估计。
conclusion: 注视是闭眼状态下内在脑信号的关键行为维度，眼脑动态或可成为理解意识状态的新途径。
---

## 摘要
在感知和心理意象过程中，注视行为与大脑活动紧密耦合。这种耦合是否延伸至闭眼状态目前仍基本未知，主要原因是闭眼时难以同时测量眼动和大脑活动。在此，我们采用了一种可扩展的基于磁共振的眼动追踪方法，从闭眼静息和睡眠期间的fMRI数据中重建注视行为。我们发现，推断出的注视行为与广泛分布于大脑皮层和小脑大部分区域（包括通常与视觉相关的许多区域）的大脑活动之间存在广泛耦合。这些动态模式在很大程度上在这两种状态中持续存在。此外，考虑注视因素会系统性地改变大规模脑组织的功能连接估计。总体而言，这些结果强调了即使在闭眼状态下，注视也应被视为内在fMRI信号中一个隐藏的行为维度。更广泛地说，我们的发现表明，眼-脑动态可能为了解闭眼意识状态提供一个窗口。

## Abstract
Gaze behavior and brain activity are tightly coupled during perception and mental imagery. Whether this coupling extends to eyes-closed states remains largely unknown, primarily because measuring eye movements alongside brain activity is difficult when the eyes are closed. Here, we used a scalable MR-based eye-tracking approach to reconstruct gaze behavior from fMRI data during eyes-closed rest and sleep. We found widespread coupling between inferred gaze behavior and brain activity distributed through much of the cerebral cortex and cerebellum, including many regions typically associated with vision. These dynamics largely persisted across the two states. Additionally, accounting for gaze systematically altered functional connectivity estimates of large-scale brain organization. Together, these results underscore the importance of considering gaze as a hidden behavioral dimension of intrinsic fMRI signals, even in eyes-closed states. More broadly, our findings suggest that eye-brain dynamics may provide a window into eyes-closed states of consciousness.

---

## 论文详细总结（自动生成）

## 论文详细总结

### 1. 论文的核心问题与整体含义
- **核心问题**：在感知和心理意象中，注视行为与脑活动紧密耦合，但**这种耦合在闭眼状态下（如静息和睡眠）是否存在**，此前几乎未知。主要障碍是闭眼时难以同步、准确地测量眼动和脑活动。
- **整体含义**：该研究旨在证明，即使在闭眼、无外部视觉输入的情况下，**注视行为仍然是内在脑信号的一个隐藏维度**。通过揭示闭眼状态下眼‑脑动态的广泛存在，为**理解闭眼意识状态（如睡眠、冥想等）** 提供新的观察窗口，并提示在分析内在功能磁共振成像（fMRI）信号时必须考虑注视因素，否则会系统性地扭曲大尺度功能连接估计。

### 2. 论文提出的方法论
- **核心思想**：利用fMRI数据本身，通过**基于MRI的眼动追踪**方法，从眼窝体素（eye‑voxel）的信号模式中**重建注视动态**，无需额外眼动仪。
- **关键技术细节**：
    - **注视预测因子构建**：
        1. 对连续的功能体积（volume）中的眼窝体素模式逐对计算**皮尔逊相关系数** $r$。
        2. 将模式不相似性 $1-r$ 作为眼位移的代理指标：值越大表示眼动位移越大。
        3. 对每个run的注视预测因子进行**头动参数回归去噪**，并**按清醒（Wake）和睡眠（Sleep）状态分段**。
        4. 将去噪后的预测因子与**血流动力学响应函数（HRF）卷积**，再将时间序列**均值中心化**，得到最终的注视预测因子。
    - **脑‑注视关联分析**：
        - 采用**体素一般线性模型（GLM）**，将注视预测因子与全脑BOLD信号进行回归，得到注视依赖脑活动的统计图。
        - 使用**FSL的FLAME 1+2混合效应模型**进行组水平单样本t检验，并用**错误发现率（FDR，$q<0.05$）** 进行多重比较校正。
    - **状态比较与功能连接分析**：
        - 用**搜索光（searchlight）局部相似性**（测地线搜索光半径：皮层23 mm，小脑11 mm）比较清醒与睡眠状态的脑活动空间模式。
        - 通过对比**是否从BOLD时间序列中移除注视解释方差**（原始与HRF卷积后的预测因子），评估注视对**大尺度功能连接**（基于Schaefer 500脑区图谱）的塑造作用。

### 3. 实验设计
- **数据集与场景**：31名参与者，在**15分钟扫描run**中尝试入睡，**同步记录fMRI和EEG**，根据EEG将数据分为**清醒（Wake）和睡眠（Sleep）** 两种状态。
- **基准与对比方法**：本研究**未设定传统意义上的benchmark或与其他方法的定量对比**。其核心贡献在于提出一种重建闭眼注视行为的方法，并在同一样本内进行：
    - 两种意识状态（清醒vs.睡眠）的**脑‑注视耦合的空间模式比较**。
    - **计入与不计入注视信息**时全脑功能连接矩阵的差异比较。
    - 与**头动参数**的去噪处理作为必要控制。

### 4. 资源与算力
- 文中**未明确报告**所使用的GPU型号、数量或训练时长。该研究基于传统统计分析（GLM、相关、置换检验），属于计算资源需求较低的分析流程，未涉及深度学习等大规模训练，因此**算力信息缺省**。

### 5. 实验数量与充分性
- **实验数量**：
    - **组水平脑映射**：清醒和睡眠状态分别生成注视依赖活动的全脑t统计图。
    - **ROI分析**：在**图谱定义**的视网膜区域进行事后验证。
    - **状态间比较**：搜索光局部相似性分析，以及**注视幅度、可用体积数目**等指标的组水平比较（均使用基于置换的显著性检验）。
    - **功能连接分析**：对比有无注视去噪的**边对边功能连接差异**，并依据Yeo 7网络进行汇总。
- **充分性评价**：
    - 实验设计**层层递进**，从发现耦合、比较状态到探测功能组织影响，逻辑链完整。
    - 使用了严格的**非参数置换检验**和**多重比较校正**，统计推断较为可靠。
    - **潜在不足**：缺少与**独立眼动测量**（如闭眼时有限的眼电或红外方法）的交叉验证；未进行系统的**消融实验**（如不同去噪策略、不同HRF模型）；样本量和扫描时长属中等，对睡眠阶段的细分（如N1、N2）未体现，可能削弱状态特异的结论精度。

### 6. 论文的主要结论与发现
- **广泛注视‑脑活动耦合**：推断的注视行为与大脑**广泛皮层及小脑**区域的活动显著耦合，涵盖了众多传统**视觉相关区域**，表明即使在闭眼状态下，注视仍广泛嵌入脑动力学。
- **状态持续性**：清醒和睡眠状态下注视依赖的脑活动**空间模式高度重叠**，且注视幅度、可用体积等指标无显著差异，提示该耦合是**跨意识状态**的稳健特征。
- **功能连接被系统性改变**：在未考虑注视时，功能连接估计存在**显著的系统性偏差**，而回归掉注视解释方差后，连接模式发生改变。这直接证明**视是内在fMRI信号中一个不可忽视的行为维度**，应当在功能连接分析中被建模。

### 7. 优点
- **方法创新**：首次实现**完全从fMRI数据重建闭眼注视行为**，避免了额外眼动设备的限制，可扩展至大量现有数据集。
- **范式严谨**：将HRF卷积、头动去噪、状态分段等步骤纳入流程，使注视预测因子更符合神经‑血流响应特征，减少了混淆。
- **多维验证**：不仅报告了耦合的存在，还通过状态比较、网络连接影响分析，从多个角度确证了信号来源的行为相关性，而非单纯噪声。
- **开放性提示**：为内在脑功能研究设立了**新的行为回归基线**，并指出眼‑脑动态可能作为意识状态的生物标志物。

### 8. 不足与局限
- **推断间接性**：注视行为由体素模式不相似性**代理**，缺乏与真实眼位/眼动轨迹的直接标定，其精度受限于fMRI的时间分辨率和信噪比。
- **睡眠状态粗糙**：仅以EEG区分清醒与睡眠，未细分睡眠阶段（如NREM各期、REM），可能掩盖睡眠深度特异性的眼‑脑耦合变化。
- **混淆因素控制**：虽然回归了头动，但**生理噪声（如心跳、呼吸）** 以及与注视相关的高阶头动或躯体动作未被充分建模。
- **样本与推广性**：31名健康成人的样本量有限，且均在扫描中尝试入睡，结果向自然睡眠、不同人群（如患者）的推广性需进一步验证。
- **无外部验证**：未与任何同步、独立的眼动测量技术进行对比，方法的绝对准确性尚不可知。
- **因果方向不明**：相关性质的分析无法分辨是**脑活动驱动眼动**还是**眼动传入反馈塑造脑活动**，或二者由共同机制导致。

（完）
