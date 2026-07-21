---
title: Topological decoding of grid cell activity via path lifting to covering spaces
title_zh: 通过路径提升到覆盖空间的网格细胞活动拓扑解码
authors: "Yao, Y. J., Yoon, I. H. R."
date: 2026-07-21
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.17.683158v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 拓扑解码网格细胞群体活动以重建空间轨迹
tldr: 网格细胞在环面流形上的周期性编码难以直接用于空间解码。本研究提出一种拓扑解码框架，通过拓扑数据分析从网格细胞种群活动中提取环面坐标，并利用路径提升技术重建物理空间轨迹，二者仅相差一个仿射变换。在仿真和实验数据上，仅用单个网格细胞模块即可可靠重建局部路径，无需外部位置信息或训练数据。该工作表明网格细胞模块内含路径整合的充分信息，为空间导航提供了新的计算机制。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-003.webp\", \"caption\": \"Figure 1. Constructing an internal representation of space from grid cell activity. A. The input data is grid cell activity collected while the mouse moves in an environment. Grid cell population activity is represented as a population vector P (t) evolving over time. B. Persistent cohomology indicates that the population vectors are organized on a torus. C. Each population vector P (t) is assigned toroidal coordinates (θtx, θ t y). Here, if the mouse is at location (x, y) at time t, we show the toroidal coordinates θtx (top) and θty (bottom) by color values over location (x, y). D. The toroidal coordinates form a path f on the grid cell torus. E. We finally lift f to a path f̃ in R2 that matches the subject’s movement up to an affine transformation.\", \"page\": 2, \"index\": 3, \"width\": 943, \"height\": 260}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-008.webp\", \"caption\": \"Figure 2. Lifting a discrete path Θ on the torus to a path Θ̃ in R2. A. Setup: given a discrete path Θ : {0, 1, . . . , T − 1} → S1 × S1 on the torus, and the goal is to construct a lifted path Θ̃ : {0, 1, . . . , T − 1} → R2 such that p ◦ Θ̃ = Θ, where p : R2 → S1 × S1 is a covering map. B. Algorithm. Base step: Θ̃(0) is placed in the tile closest to the origin (blue). Iterative step: Given Θ̃(t), the next lift Θ̃(t + 1) is determined by comparing the consecutive toroidal coordinates Θ(t) and Θ(t + 1) via Eq. 2. If they are similar (“Yes” branch), the underlying path (green) is assumed to not cross a torus edge and Θ̃(t + 1) is placed in the same tile as Θ̃(t). Otherwise (“No” branch), the underlying path (green) is assumed to cross at least one edge and Θ̃(t + 1) is placed in an adjacent tile, chosen to minimize |θ̃tx − θ̃t+1\", \"page\": 4, \"index\": 8, \"width\": 850, \"height\": 981}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-002.webp\", \"caption\": \"Figure 3. Illustration of path lifting on a simulated CAN data (56 × 44 grid cell network, T = 599, 999 time bins.). A. A simulated movement path, with a highlighted segment. B. Toroidal coordinates for each location on the map. The repeated values indicate that the map is large enough to require nontrivial lifting during path reconstruction. C. Enlarged view of the highlighted segment. The color indicates that the simulated mouse moves from dark to light. D. The toroidal coordinates corresponding to the path segment in panel C. E. The output of the reconstruction algorithm resembles the original path in panel C. F. The reconstructed path, post affine transformation, recovers the original movement path in panel C.\", \"page\": 6, \"index\": 2, \"width\": 708, \"height\": 419}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-001.webp\", \"caption\": \"Figure 4. Path lifting on CAN-simulated grid cell activity (G = 2, 464, T = 599, 999 time bins per simulation.) reconstructs the original movement path. A. Simulated movement trajectories in environments with 0, 1, and 2 holes. B. Toroidal coordinates for each location on the map. C. Reconstructed paths from the simulation of mouse movement on maps with 0, 1, and 2 holes reflect the topology of the maps. D. After optimal affine alignment, the reconstructed paths resemble the original movements in panel A. E. Reconstruction errors across 10 independent trials. For each environment, the error between simulated movement paths and reconstructed paths (teal) are compared against random baseline (orange), computed as the error between pairs of independently simulated trajectories in the same environment. The reconstruction errors are significantly smaller than the random baselines in all three environments.\", \"page\": 6, \"index\": 1, \"width\": 943, \"height\": 510}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-004.webp\", \"caption\": \"Figure 5. Example simulated grid cell activity with spontaneous firings that lead to low path reconstruction errors. (Top) Example activity trace from a CAN simulation. (Center) Simulated activity with additional spontaneous activity, generated with h = 0.4, p = 0.1% and σ = 50. The mean global reconstruction error for such noisy activity is 2.115% (see Table 1). (Bottom) Activity trace with additional spontaneous activity, generated with h = 0.4, p = 1% and σ = 10. The mean reconstruction error is 4.894% (see Table 1).\", \"page\": 7, \"index\": 4, \"width\": 521, \"height\": 367}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-007.webp\", \"caption\": \"Table 1. Average reconstruction errors (%) between the original trajectory and the reconstructed paths over 10 trials. Here, the maximum height of the spontaneous firing is fixed at h = 0.4. The rows represent the proportion of times during which a grid cell randomly fired, and the columns represent the variance σ of the noise added. An entry of N/A indicates that the method failed to compute toroidal coordinates in all 10 trials.\", \"page\": 8, \"index\": 7, \"width\": 931, \"height\": 238}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-006.webp\", \"caption\": \"Figure 6. Path reconstruction recovers one-dimensional environment from grid cell activity. Data are from mouse N2 (dataset “N2 200203 buildup track”; [44]) navigating a 320 cm virtual build-up track. 44 co-modular grid cells were identified. Firing rates were provided in 2cm spatial bins (160 bins per run, 441 total runs). A. Mouse position over time across 5 runs; each rising segment corresponds to one traversal of the track, after which the mouse is teleported to the start. A single run is highlighted in pink. B. The persistence diagram confirms that grid cells are organized on a torus: one connected component (H0), two one-dimensional cycles (H1), and one two-dimensional void (H2). C. Example path on the grid cell torus corresponding to a single run. For each time point t, the corresponding toroidal coordinates θx and θy are plotted. D. Toroidal coordinates from panel C visualized over position. Because the firing rate data is provided in 2cm spatial bins, the toroidal coordinates are also computed for each spatial bin. Each point on the plot corresponds to one spatial bin in a fixed run, plotted at its track position (x-axis) and spatial bin index (y-axis). Color encodes the toroidal coordinates θx (left) and θy(right). E. The reconstructed path lies close to a one-dimensional line. The red line indicates the line spanned by the first principal component (PC1) of PCA. F. Distribution of linearity scores (variance explained by PC1) across 441 runs; median = 98.8%.\", \"page\": 8, \"index\": 6, \"width\": 943, \"height\": 446}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-009.webp\", \"caption\": \"Figure 7. Reconstruction of local paths from two-dimensional experimental data [20] (rat R, module 1, day 2, open-field session; 111 co-modular grid cells ). A. The original trajectory of a rat exploring a 1.5m×1.5m open-field arena. B. The reconstructed global trajectory, which differs in overall shape from the original path. C. The persistence diagram indicates that the grid cells are organized on a torus. D. A visualization of the toroidal coordinates for each location. E. An example local path. F. The toroidal coordinates corresponding to panel E involve non-trivial liftings. G. A highlight of the reconstructed segment in panel B (left), the reconstructed path, before affine transformation (center), and after affine transformation (right). H - J. Another example local path and its reconstruction. K. Distribution of local reconstruction errors: pairs of original local paths and reconstructed paths (left) show significantly smaller errors than baseline consisting of mismatched local paths (right) (t(2014) = −14.6, p < 0.0001).\", \"page\": 9, \"index\": 9, \"width\": 943, \"height\": 518}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-005.webp\", \"caption\": \"Figure 8. Two possible errors in path reconstruction arising from sparsity of time points. A. The first type of error occurs when two consecutive toroidal coordinates are lifted to two distinct tiles when they should be lifted to a single tile. (Left) Original movement path. Circles indicate the location at select time points. (Center) The corresponding toroidal coordinates. (Right) The algorithm lifts the toroidal coordinates Θ(0), . . . ,Θ(3) to the blue tile. Because θ3y and θ4y are dissimilar, Θ̃(4) is in a different tile, shown in yellow. The resulting reconstructed path (orange) deviates from the original path (green). B. The second type of error occurs when two consecutive toroidal coordinates are lifted to the same tile when they should be lifted to different tiles. Here, the toroidal coordinates θ3y and θ4y have a small enough difference so the algorithm lifts Θ(3) and Θ(4) to the same tile. Again, the reconstructed path (orange) deviates from the original (green).\", \"page\": 10, \"index\": 5, \"width\": 943, \"height\": 214}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-17-683158-v2/fig-010.webp\", \"caption\": \"Figure 9. Selection of the proximity parameter ε for CAN-simulated data. A. Histogram of maximal coordinate differences max{|θtx − θt+1\", \"page\": 16, \"index\": 10, \"width\": 943, \"height\": 306}]"
motivation: 网格细胞的周期性编码如何使大脑理解其在空间环境中的状态尚不清楚。
method: 使用拓扑数据分析提取网格细胞群体活动的环面坐标，并通过路径提升到覆盖空间来重建空间轨迹。
result: 重建的轨迹与原始轨迹仅相差一个仿射变换，且仅需单个网格细胞模块即可可靠重建局部路径。
conclusion: 网格细胞模块包含足够信息进行路径整合，并暗示了空间导航的一种潜在计算机制。
---

## 摘要
高维神经活动通常存在于低维子空间中，称为神经流形。内侧内嗅皮层的网格细胞提供了一种周期性的空间编码，这些编码组织在一个环面流形附近，且独立于空间环境。由于其编码的周期性，大脑如何利用环面流形来理解其在空间环境中的状态尚不清楚。我们引入了一种新颖的框架，利用拓扑从网格细胞活动中解码空间信息。我们的方法使用拓扑数据分析从网格细胞群体活动中提取环面坐标，并采用路径提升在物理空间中重建轨迹。重建的路径与原始路径之间相差一个仿射变换。我们在连续吸引子网络模拟和网格细胞的实验记录上验证了该方法，证明可以仅从单个网格细胞模块，在没有外部位置信息或训练数据的情况下，可靠地重建局部轨迹。这些结果表明，共模的网格细胞包含足够的信息用于路径整合，并提示了一种潜在的空间导航计算机制。

## Abstract
High-dimensional neural activity often reside in a low-dimensional subspace, referred to as neural manifolds. Grid cells in the medial entorhinal cortex provide a periodic spatial code that are organized near a toroidal manifold, independent of the spatial environment. Due to the periodic nature of its code, it is unclear how the brain utilizes the toroidal manifold to understand its state in a spatial environment. We introduce a novel framework that decodes spatial information from grid cell activity using topology. Our approach uses topological data analysis to extract toroidal coordinates from grid cell population activity and employs path-lifting to reconstruct trajectories in physical space. The reconstructed paths differ from the original by an affine transformation. We validated the method on both continuous attractor network simulations and experimental recordings of grid cells, demonstrating that local trajectories can be reliably reconstructed from a single grid cell module without external position information or training data. These results suggest that co-modular grid cells contain sufficient information for path integration and suggest a potential computational mechanism for spatial navigation.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **核心问题**：内侧内嗅皮层（MEC）的网格细胞以周期性的六角形发放模式覆盖环境，其群体活动在拓扑上组织成一个环面（torus）。由于同一环面坐标对应物理空间中多个不同位置，大脑如何利用这种周期性的环面码来理解自身在空间环境中的状态，是一个根本性的不解之谜。
- **整体含义**：本研究回答“单个网格模块中到底蕴含多少空间信息”以及“能否仅从该模块中解码出运动轨迹”。它表明仅靠一个模块的群体活动即可实现路径积分式的轨迹重建，为空间导航提供了一种无须外部位置信号、无须训练的纯计算机制。

### 2. 方法论：核心思想与技术细节

- **核心思想**：将网格细胞群体向量从环面（S¹×S¹）提升（lift）到欧氏平面（R²），从而将环面上的周期性路径“展开”为物理空间中的轨迹。整个过程完全基于拓扑学，分为两步：
  1. **环面坐标分配**：利用持续上同调（persistent cohomology）确认群体向量位于一个环面上，并用环面坐标 $(\theta_x, \theta_y) \in [0,2\pi)^2$ 参数化每个时间点的群体向量。
  2. **路径提升**：将环面上的离散路径 $\Theta(t) = (\theta_x^t, \theta_y^t)$ 提升为 R² 中的路径 $\tilde{\Theta}(t)$，使得 $p \circ \tilde{\Theta} = \Theta$，其中 $p : \mathbb{R}^2 \to S^1 \times S^1$ 是覆盖映射。提升时通过整数 $M^t, N^t$ 确定点落在哪个“瓷砖”中：
     $$\tilde{\theta}_x^t = \theta_x^t + 2\pi M^t,\quad \tilde{\theta}_y^t = \theta_y^t + 2\pi N^t.$$
- **算法流程**：
  - 输入：$G\times T$ 活动矩阵（$G$ 个细胞，$T$ 个时间或空间分箱）。
  - 持续上同调检验环面结构（一个连通分量、两个一维圈、一个二维空洞）。
  - 为群体向量分配环面坐标（使用圆形坐标或环面坐标算法）。
  - 从 $t=0$ 开始，设 $M^0=N^0=0$。对于每对连续时间点，若坐标差 $|\theta_x^t - \theta_x^{t+1}| \le \varepsilon$ 且 $|\theta_y^t - \theta_y^{t+1}| \le \varepsilon$，则认为没有跨过环面边缘，$M^{t+1}=M^t, N^{t+1}=N^t$；否则，尝试将 $\tilde{\Theta}(t+1)$ 放置在相邻瓷砖中，并最小化与 $\tilde{\Theta}(t)$ 的逐坐标距离，确定 $M^{t+1}, N^{t+1}$。
  - 邻近阈值 $\varepsilon$ 根据连续坐标差分布自动选取（使绝大多数潜在跨边事件被测试）。
  - 重建路径与真实路径通过最优仿射变换对齐，计算归一化平均欧氏距离作为重构误差。
- **关键技术细节**：
  - 持续上同调使用 Vietoris–Rips 复形，地标点数在仿真中为 $T^*=250$，实验数据中为 $T^*=1200$。仿真用欧氏距离，实验用余弦不相似度。
  - 实验数据预处理：选择高总活动群体向量、z-score、PCA 到 6 维、采用 UMAP 式邻域选择子采样 1200 点，再计算模糊拓扑表示的不相似矩阵。
  - 环面坐标：仿真用 DREiMac 的环面坐标算法，实验采用 Gardner 等（2022）的上同调解码框架。

### 3. 实验设计

- **数据集与场景**：
  - **连续吸引子网络（CAN）仿真**：56×44 网格细胞网络，得到 $G=2464$ 细胞在 $T=599,999$ 时间点上的活动。模拟了三种 100×100 的环境：无洞、一个洞、两个洞。路径由随机游走生成（角范围 ±75°，最大步长固定）。
  - **一维实验数据**：来自 Wen 等（2024）的公开数据，小鼠在 320 cm 虚拟累积跑道上的 441 次跑动，44 个共模网格细胞，数据以 2 cm 空间 bin 给出（$T=160$ bins/次），分析以每次跑动为单位。
  - **二维实验数据**：来自 Gardner 等（2022）的公开数据，大鼠在 1.5 m×1.5 m 开放场地 21.1 分钟，111 个共模网格细胞，$T=126,728$ 时间 bin（10 ms）。
- **对比方法与基准**：
  - **随机基线（仿真）**：独立仿真的两条轨迹对齐后的误差，作为无真实对应时的期望误差。
  - **二维实验的局部路径基准**：所有局部段两两配对对齐后的误差分布。
  - **零提升模型与随机提升模型**（补充材料）：说明归纳式提升过程的必要性。
  - 还评估了噪声鲁棒性（加入不同比例和高斯噪声）。
- **评价指标**：
  - 全局重构误差：真实路径与重构路径经最优仿射对齐后的归一化平均欧氏距离。
  - 局部重构误差：将路径切分成短段后分别计算对齐误差。
  - 一维环境下路径的“线性分数”（第一主成分解释方差）。
  - 统计检验（t 检验、z 分数）比较误差与基线。

### 4. 资源与算力

- 文中明确提到使用单核 CPU：Intel Xeon Gold 6326 (2.90 GHz) 节点，512 GB RAM。
- 对于仿真数据（2464 神经元，600,000 时间点），完整管线约 12 分钟（仿真 3 分钟，环面坐标 9 分钟，路径提升 0.5 秒）。
- 对于二维实验数据（111 神经元，126,728 时间点），完整管线不到 1 分钟。
- 在一般笔记本上（MacBook Pro, Apple M2, 16 GB RAM）同样配置需约 80 分钟（仿真）和不到 1 分钟（实验）。
- **没有使用 GPU**，也没有提及 GPU 型号或训练时长。

### 5. 实验数量与充分性

- **实验组数**：
  - 仿真：三种环境（0孔、1孔、2孔），各进行 10 次独立试验（共 30 次完整重建）。
  - 噪声鲁棒性：在 1 孔环境下，设置 5 个噪声比例 $p$（0.1% 到 10%）和 4 个噪声方差 $\sigma$（1 到 100），固定峰值 $h=0.4$，每组 10 次试验。部分高噪声组合因无法计算环面坐标记为 N/A。
  - 一维实验：441 次跑动逐一重建并计算线性分数。
  - 二维实验：63 个局部段（20 秒一段）重建，并与 1953 对不匹配段对比。
  - 补充分析（附录）：不同参数影响、采样密度、度量选择、零提升/随机提升对照等。
- **充分性与客观性**：实验覆盖了仿真与真实数据、多种环境和维度、噪声消融以及局部/全局尺度，对比严格采用独立基准，统计数据量充分，分析客观。但仍存在局限性：二维实验全局重建失败的原因未完全消除，噪声测试仅针对 CAN 仿真，且高噪声下方法会失效。

### 6. 主要结论与发现

- 单个网格细胞模块的群体活动足以重建出物体的运动轨迹，重建结果与真实路径之间仅相差一个仿射变换。
- 在 CAN 仿真中，无论环境有无孔洞，重构轨迹均能保留拓扑特征（孔洞数量、连通性），且误差显著低于随机基线。
- 对于一维实验跑道，重构路径高度线性（中位线性分数 98.8%），成功恢复了一维空间结构。
- 对于二维开放场，全局重构形状变形，但局部路径（20 秒片段）能忠实复原，误差显著低于随机基线。
- 方法对中等程度的自发噪声具有鲁棒性，但在噪声过强破坏环面结构时会失效。
- 整个框架不需要任何位置标签、多模块相位差或训练过程，完全依赖拓扑特性，为空间导航提供了一种潜在的计算机制。

### 7. 优点

- **方法新颖性**：首次将拓扑学中的路径提升到覆盖空间的技术应用于计算神经科学，实现从神经活动到空间轨迹的直接解码。
- **仅需单个模块**：突破了以往需要多模块相位差或训练深度网络的方法，揭示了单个模块的内在导航能力。
- **无需求训练或位置信息**：解码过程无需外部标签或速度、方向等信息，纯无监督。
- **理论基础坚实**：基于持续上同调和覆盖空间理论，将神经流形结构转化为可操作的解码步骤。
- **验证全面**：在仿真、一维和二维实验数据上均得到验证，并提供了详细的噪声、参数敏感性分析。
- **计算效率高**：无论在高性能计算节点还是普通笔记本上，都可在分钟级完成，且不需要 GPU。

### 8. 不足与局限

- **全局重构鲁棒性不足**：在二维实验数据上，全局轨迹出现明显失真，尽管局部段可靠，但误差累积导致整体形状偏离。
- **时间采样要求苛刻**：算法假设采样足够密集，若时间点稀疏，易于发生“误提升”或“漏提升”，造成路径扭曲。
- **环境尺寸限制**：在远大于网格间距的环境中，环面坐标的重复性使得提升过程中的模糊性增加，可能降低重构质量。
- **噪声鲁棒性有限**：高比例、大幅值的自发噪声会破坏环面拓扑结构，导致环面坐标计算失败（N/A）。
- **仿射模糊性未解决**：重建结果与真实路径相差一个未知仿射变换，文中指出可通过其他细胞类型或多模块组合解决，但框架本身未整合此步骤，功能性解码仍存在对齐问题。
- **实验数据预处理依赖原方法**：二维实验数据的环面坐标计算借用了 Gardner 等（2022）的复杂预处理和上同调解码框架，若直接应用 DREiMac 会失败，说明方法对预处理步骤敏感。
- **路径提升仅依赖局部最小化**：提升规则仅根据相邻帧距离最小化来选择瓷砖，未考虑全局一致性或概率分布，可能积累误差。

（完）
