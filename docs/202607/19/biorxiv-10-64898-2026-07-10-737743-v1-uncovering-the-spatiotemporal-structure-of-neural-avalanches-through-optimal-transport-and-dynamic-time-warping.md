---
title: Uncovering the spatiotemporal structure of neural avalanches through optimal transport and dynamic time warping
title_zh: 通过最优传输与动态时间规整揭示神经雪崩的时空结构
authors: "Novicky, F., Jajcay, N., Hlinka, J."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737743v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用最优传输和动态时间规整解码神经雪崩的时空结构
tldr: 本研究针对神经雪崩时空结构分析中事件变异性难题，提出结合不平衡最优传输与子序列动态时间规整的灵活对齐方法，应用于裸盖菇素 EEG 数据，层次聚类发现12种复现传播模式，并揭示裸盖菇素显著减少振荡序列、极性平衡趋向稳定，该方法已开源为stppy包。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-006.webp\", \"caption\": \"Table 1: Cluster composition showing distribution of drug conditions, tasks, and training status (values in %). The subject column represents in how many participants the avalanches were observed. The statistics showed that there was no statistically significant difference in drug condition, task or training status after the Benjamini-Hochberg FDR correction.\", \"page\": 9, \"index\": 6, \"width\": 1004, \"height\": 350}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-001.webp\", \"caption\": \"Figure 2: Cluster self-detection and cross-detection validation. (a) Cross-cluster correlation matrix for avalanche data: each cell shows the average maximum absolute correlation when using the detector cluster (column) to identify source avalanches (row). The diagonal (self-detection) is visibly higher than off-diagonal entries. (b) Self-detection versus best competitor for sign-encoded data: violin plots comparing, for each cluster, the maximum absolute correlation achieved by self detection (green) against the highest-scoring competing detector (red). (c) Cross-cluster correlation matrix for continuous avalanches, (i.e., EEG data at the same time windows as individual avalanches). The diagonal advantage is reduced, reflecting the loss of sparsity in continuous signals. (d) Self-detection versus best competitor for continuous data: the gap between self-detection and the best competitor narrows considerably compared to the sign-encoded case, indicating substantial overlap among cluster templates in continuous recordings. (e) Inter-cluster correlation matrix. Pairwise Pearson correlations between the 12 consensus cluster templates. High off-diagonal values (mean r = 0.532, max r = 0.862) reflect substantial spatial overlap among clusters distributed across the same 64-electrode array. This overlap motivated the selection of a high detection threshold (ρ = 0.825) to minimize spurious co-detections during backfitting.\", \"page\": 10, \"index\": 1, \"width\": 993, \"height\": 1076}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-005.webp\", \"caption\": \"Figure 3: Psilocybin shifts the polarity balance of recurring sequences toward stable Oscillating sequences are those where successive detections of the same cluster alternate in polarity while stable sequences maintain consistent polarity. Bars show within-condition proportions (each condition sums to 100%). Significance brackets show FDR-corrected subject-level permutation tests (see Methods). (a) Overall comparison between control and psilocybin sessions. The oscillating share (O) falls from 86% to 65% and the stable share (S) rises correspondingly; significant by within-subject permutation (pFDR = 0.022). (b) Task consistency: the shift is in the same direction across tasks, but no individual task survives the permutation test (pFDR > 0.1). (c) Drug effect within each training group: significant within untrained (pFDR = 0.006) but not trained (pFDR = 0.10); the groups do not differ from each other (pFDR = 0.72). (d) Cluster-specific sequence counts: intrinsically oscillating clusters (notably 2 and 5, which also exhibit the clearest spatial propagation across the scalp) show the largest reductions under psilocybin, while intrinsically stable clusters (7, 9, 11, with fixed topographic arrangements) remain relatively unchanged. Cluster 8 is the only cluster exhibiting a substantial within-cluster shift from oscillating to stable dynamics under psilocybin. Significance levels are denoted as: n.s. = not significant (p > 0.05), ∗ p < 0.05, ∗ ∗ p < 0.01, ∗ ∗ ∗ p < 0.001.\", \"page\": 12, \"index\": 5, \"width\": 997, \"height\": 594}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-003.webp\", \"caption\": \"Table 2: Cluster-specific polarity profiles reveal distinct pattern subgroups. For each cluster, the number and percentage of stable versus oscillating sequences is shown separately for control and psilocybin sessions, after removal of temporally overlapping detections (>44ms). Clusters fall into three categories: intrinsically stable (7, 9, 11), intrinsically oscillating (0, 1, 2, 4, 5, 10), and mixed/drug-sensitive (6, 8). Cluster 3 contained only one sequence and is omitted. Statistical significance is assessed via within-subject permutation tests (Methods) with FDR correction; only cluster 8 showed a statistically significant within-cluster drug effect (pFDR = 0.019).\", \"page\": 13, \"index\": 3, \"width\": 808, \"height\": 455}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-002.webp\", \"caption\": \"Figure 4: Neural avalanche identification process. The figure illustrates the three-step procedure for detecting and characterizing neural avalanches from multi-electrode recordings. (a) Threshold Detection: Raw signals from three electrodes (E1, E2, E3) are z-score normalised, with each electrode’s trace vertically offset for clarity. Dashed horizontal lines indicate the detection thresholds at ±3σ for each electrode. The yellow-shaded region marks the detected avalanche period, bounded by red vertical lines indicating avalanche start and end times. During the avalanche, E1 (blue) crosses the negative threshold while E2 (purple) and E3 (orange) cross the positive threshold. (b) Active Time Points: Time points where electrode signals exceed the absolute threshold (|threshold| = 3σ) are highlighted as colored dots, shown against the full signal traces (gray). The yellow-shaded region and red vertical lines mark the avalanche boundaries. Only supra-threshold activity is retained for avalanche analysis. (c) Sign-encoded Avalanche: Detected avalanche activity is sign-encoded while preserving polarity: positive threshold crossings are set to +1, negative crossings to -1, and sub-threshold activity to 0. E1 exhibits negative polarity (blue dots below zero line) while E2 and E3 show positive polarity (dots above their respective zero lines). The yellow-shaded region and red vertical lines continue to mark the avalanche boundaries across all panels.\", \"page\": 18, \"index\": 2, \"width\": 991, \"height\": 694}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-004.webp\", \"caption\": \"Figure 5: Hungarian Algorithm for Spatial Pattern Alignment with Cardinality Imbalance. The linear sum assignment problem is solved through matrix reduction to find optimal electrode matching between spatial patterns. (a) Original Cost Matrix: X and Y represent spatial patterns with positive or negative activity values from the dataset. The matrix entries contain normalised Euclidean distances between electrode positions, where each element dij represents the physical distance from source electrodeXi to target electrode Yj . In this example, pattern X has 3 active electrodes while pattern Y has 4, creating a cardinality imbalance. (b) Extended Matrix with Dummy Row: To handle the imbalance, the matrix is extended by adding a dummy row. Each dummy row entry is set to the minimum value of its corresponding column: dummyj = mini(dij), allowing unmatched target electrodes to be assigned to the dummy with minimal penalty. (c) Hungarian Algorithm and Optimal Assignment: The algorithm proceeds in two steps: Step 1 subtracts the minimum value from each row (minj(dij) for row i), then Step 2 subtracts the minimum value from each column (mini(d ′ ij) for column j). Cells containing zeros after reduction indicate potential optimal assignments (highlighted in gold). The final optimal assignment minimises total transport cost, calculated as the sum of original matrix values at assigned positions: 0.3 + 0.4 + 1.1 + 0.5 = 2.3. This approach ensures both polarity-matched assignments and handles cardinality imbalances through dummy assignments.\", \"page\": 19, \"index\": 4, \"width\": 993, \"height\": 392}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737743-v1/fig-007.webp\", \"caption\": \"Figure 6: This figure demonstrates how subDTW finds the optimal alignment between avalanche sequences of different durations, allowing the shorter sequence to match a contiguous portion of the longer sequence while maintaining temporal correspondence and minimizing the total alignment cost.\", \"page\": 20, \"index\": 7, \"width\": 983, \"height\": 977}]"
motivation: 神经雪崩事件在持续时间和空间范围上的高度变异性阻碍了对其详细时空结构和重现性的研究。
method: 采用不平衡最优传输与子序列动态时间规整组合的距离度量，对 EEG 数据聚类得到传播模板，并在连续记录中追踪模板重复序列以区分振荡与稳定模式。
result: 裸盖菇素条件下振荡序列相对减少，极性平衡偏向稳定，且该效应主要由特定传播簇驱动。
conclusion: 所提方法有效揭示了裸盖菇素对神经雪崩动态极性平衡的调节作用，工具包可促进相关研究。
---

## 摘要
神经雪崩——即由阈值定义的协调活动爆发——传统上以无标度统计特征为特点。然而，对其详细时空结构及其在自发活动中重现的研究，一直受到雪崩持续时间和空间范围变异的阻碍。为应对这一挑战，我们提出使用灵活比对：采用一种结合非平衡最优传输与子序列动态时间规整的距离度量，从而能够比较不同长度和空间构型的事件。将此方法应用于PsiConnect裸盖菇素研究的63名参与者64通道脑电图数据，层次聚类揭示了12种重复出现的传播模式。随后在原始连续记录中追踪这些聚类模板，识别出相同模式至少连续立即重复两次的序列。极性交替的序列被归类为振荡型；极性一致的序列被归类为稳定型。振荡序列主要对应于表现出视觉确认的空间传播的聚类，而稳定序列对应于空间固定的模式。在裸盖菇素作用下，振荡序列相对于稳定序列减少，极性平衡向稳定型偏移；这种总体偏移通过受试者水平置换检验得到确认，而明显的任务和训练特异性效应未能通过检验。这一效应也主要由一个特定聚类驱动，表明存在受裸盖菇素摄入影响的特定神经动力学在时间上发生改变。所开发的方法已在公开的stppy Python包中实现。

## Abstract
Neural avalanches - or threshold-defined bursts of coordinated activity - are traditionally characterised by scale-free statistics. However the study of their detailed spatiotemporal structure and their recurrence within spontaneous activity has been hindered by the variability of avalanches in duration and spatial extent. To tackle this challenge, we propose the use of flexible alignment: we employ a distance metric combining unbalanced optimal transport with subsequence dynamic time warping, enabling comparison across events of different lengths and spatial configurations. Applied to 64-channel EEG from 63 participants in the PsiConnect psilocybin study, hierarchical clustering revealed 12 recurring propagation patterns. These cluster templates were then traced in the original continuous recordings, identifying sequences where the same pattern recurred consecutively and immediately at least twice. Sequences with alternating polarity were classified as oscillating; those with consistent polarity as stable. Oscillating sequences predominantly corresponded to clusters exhibiting visually confirmed spatial propagation, while stable sequences corresponded to spatially fixed patterns. Under psilocybin, oscillating sequences were reduced relative to stable sequences, shifting the polarity balance toward stable; this overall shift was confirmed by a subject-level permutation test, while the apparent task- and training-specific effects did not survive it. This effect was also mostly driven by a specific cluster, suggesting that there is concrete neural dynamics that are temporally affected by the consumption of psilocybin. The developed methodology has been implemented in a publicly available stppy Python package.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义
该论文旨在解决**神经雪崩**（neural avalanches）研究中一个长期瓶颈：传统分析几乎只关注雪崩的尺寸‑持续时间无标度统计，但忽略了事件本身的**时空形状与重现性**。由于雪崩持续时间、空间覆盖范围差异极大，难以对单个雪崩进行有意义的比较和归类。因此，作者提出一种全新的对齐方法，能够比较不同长度和空间构型的雪崩，挖掘潜在的重现传播模式，并将这些模板用作探测器，在连续脑电记录中追溯其动态。  
在应用层面，论文将这一框架用于**裸盖菇素**（psilocybin）对大脑时空动力学影响的研究，发现药物会系统地改变模式重现的极性平衡——振荡序列减少，稳定序列相对增加。这一结果不仅提供了对致幻剂神经机制的具体洞察，还表明数据驱动的雪崩聚类能够自然桥接**微状态**、**行波**和**临界雪崩**这三个原本独立的研究领域。

### 2. 方法论
#### 2.1 雪崩检测与符号编码
- 对每导联信号做 z‑score 标准化，以 ±3σ 阈值检测活跃时刻；
- 连续超阈值片段作为候选雪崩，要求最少持续 11 时间步（40 ms，250 Hz）；
- 应用空间过滤器：在任一时刻，某活跃电极周围 8 个邻近电极中至少有 5 个同等极性的活跃电极，且需正、负极性各满足一次；
- 仅保留超阈值值，并转换为符号表示（+1/−1/0）。

#### 2.2 雪崩间距离计算：UOT + subDTW
**空间对齐**  
- 对两个雪崩的每个时间点对，按正、负极性分别计算**不平衡最优传输**（UOT），使用电极三维坐标的欧氏距离作为地面度量；
- 以**匈牙利算法**求解同极性电极的最佳匹配，电极数量不等时通过添加虚拟节点（惩罚值为对应列最小距离）处理；
- 总代价归一化，除以两雪崩总活跃电极数。

**时间对齐**  
- 使用**子序列动态时间规整**（subDTW），允许较短雪崩对齐到较长雪崩的任意连续子段；
- 插入惩罚为最小非零代价的 0.1%，删除为 0.2%，倾向对角路径且保证路径长度不小于短序列长度；
- 最终输出标量距离，形成雪崩间的距离矩阵。

#### 2.3 聚类与共识模板
- 采用**平均链接层次聚类**，截断距离阈值 3.5，保留成员数 ≥30 的簇，其余视为噪声；
- 每个簇内以 **medoid**（至其他成员总距离最小的雪崩）为时间参考，将其他雪崩通过 subDTW 路径对齐至 medoid 时间轴，逐帧平均得到共识模板。

#### 2.4 模板回溯与序列检测
- 因 UOT+subDTW 在整段数据上计算成本过高，使用基于**逐帧空间相关**的快速匹配：计算模板与滑动窗口的帧间皮尔逊相关系数平均，阈值 ρ=0.825；
- 检测至少 2 次连续检测（允许 1 帧延迟）的序列，标记为稳定（同极性）或振荡（异极性）；
- 移除来自不同簇且时间重叠 >44 ms 的序列以避免重复计数。

#### 2.5 统计分析
- 因序列嵌套于受试者内，使用**受试者水平置换检验**（受试者内交叉设计时打乱药物标签，受试者间设计时打乱训练标签）评估显著性；
- 报告经 Benjamini‑Hochberg FDR 校正的 p 值；
- 所有比例比较均在条件内归一化，排除序列总数差异的影响。

### 3. 实验设计
- **数据集**：PsiConnect 裸盖菇素研究，63 名参与者，64 通道 EEG（10‑20 系统），包含基线（对照）和急性裸盖菇素（19 mg）两次记录；
- **任务条件**：静息态、冥想、音乐聆听、视频观看，各约 4‑5 分钟；
- **参与者分组**：33 名完成 8 周 MBCT 正念训练的“训练组”，30 名未训练的“未训练组”；
- **分析方法比较**：论文并未设置传统意义上的基准方法（如与现有微状态、行波检测算法直接定量对比），而是通过自身模板回溯和序列极性分析，验证聚类发现的可靠性与生物学意义。反向匹配的有效性则是通过簇内自检 vs. 跨簇检验的相关系数分布来评估的。

### 4. 资源与算力
- 文中明确提到：计算 10 216 个雪崩的 UOT+subDTW 距离矩阵**约耗时 300 小时**；
- 未提及 GPU 型号、数量或并行方案，推测该计算主要基于 CPU；
- 回溯部分因计算成本改用相关法，但未报告其具体算力开销。

### 5. 实验数量与充分性
论文围绕一个大型且多条件的数据集展开了全面的分析：
- 从原始记录中提取约 5 108 个雪崩（翻转为 10 216 用于聚类），得到 12 个簇，回溯后获得 2 915 个有效序列；
- 药物主效应采用受试者内置换检验（FDR 校正）；同时分析了任务、训练对照，以及簇特异极性变化；
- 实验设计客观：所有判决阈值（雪崩检测、聚类截止距离、回溯相关阈值等）虽为启发式，但通过**反向验证**（回溯到连续数据中能重现，且呈现对称性和一致的药物效应）间接证明其稳健性；
- 存在一定的探索性，但总体实验步骤周全，统计检验充分考虑到数据嵌套结构，避免伪重复。

### 6. 主要结论与发现
1. **发现 12 种可重现的雪崩时空模式**，其中部分簇（2、5 等）呈现清晰的枕‑顶叶行波，另有簇（7、9 等）呈现类似传统微状态的固定地形。簇间具有双侧对称性。
2. **裸盖菇素改变序列极性构成**：振荡序列占比从 85.7% 降至 65.2%，稳定序列相对增高，总体效应在受试者水平显著（pFDR=0.022）。该偏移在冥想、音乐、静息任务中方向一致，但各任务单独不显著。
3. **效应来源**：主要由两类机制驱动——① 内在振荡簇（尤其簇 2 和 5）的总检测次数大幅下降；② 簇 8 内部出现从振荡到稳定的显著转移（pFDR=0.019），是唯一在单个簇层面存活置换检验的模式。
4. **方法学统一**：该工作表明，神经雪崩、微状态和行波可能是对同一底层动力学不同侧面的描述，雪崩聚类有望成为统一框架。

### 7. 优点
- **技术创新**：首次将非平衡最优传输与子序列 DTW 结合用于雪崩形状比较，有效处理持续时间不一、空间覆盖不均的问题，并提供开源包 `stppy`。
- **管道完整**：从事件提取、对齐聚类、模板回溯到动态分析，形成闭环，并包含合理的统计检验设计。
- **生物学发现**：不仅发现特定模式的药物敏感变化，还揭示了簇内在的对称性与极性逻辑（例如镜像簇具有相同动力学类型）。
- **概念整合**：自然连接此前互相隔离的雪崩、微状态和行波研究，为跨领域对话提供实证基础。

### 8. 不足与局限
- **参数依赖性**：雪崩检测阈值、聚类截止距离、回溯相关阈值等均为启发式选择，未系统调优或灵敏度分析；全参数空间探索计算成本过高。
- **回溯方法的次优性**：因算力限制，回溯使用空间相关而弃用 UOT+subDTW，导致簇间区分度下降，必须依赖高阈值和重叠排除，可能漏掉或错误分配某些模式。
- **无替代假说检验**：未使用能同时保留空间与时间相关性的替代数据（如线性时空模型生成的替代 EEG）检验聚类的必然性，无法完全排除线性相关足以解释发现的可能性。
- **空间分辨率限制**：64 电极头皮 EEG 受体积传导影响，难以分辨皮层源，部分“传播”可能带有模糊性，更高密度或源重建数据有助于确证。
- **行为/任务效应的不稳定性**：分任务统计检验未达显著，对训练效应的组间比较也不显著，限制了结论的泛化性；视频任务样本少、方向相反，无法定论。

（完）
