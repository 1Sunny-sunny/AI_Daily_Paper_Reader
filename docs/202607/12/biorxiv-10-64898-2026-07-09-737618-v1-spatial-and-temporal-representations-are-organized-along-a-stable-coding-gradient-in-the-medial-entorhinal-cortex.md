---
title: Spatial and temporal representations are organized along a stable coding gradient in the medial entorhinal cortex
title_zh: 内侧内嗅皮层中空间与时间表征沿稳定编码梯度组织
authors: "Lee, H.-W., Bowler, J. C., Heys, J. G."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.09.737618v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 内嗅皮层时空编码梯度
tldr: 内嗅皮层内侧区（MEC）既编码空间也编码时间信息，但其组织规律不明。本研究通过记录小鼠在计时和空间导航任务中的MEC神经元活动，发现空间和时间表征沿稳定梯度分布：强空间调谐神经元（如网格细胞）偏好稳定空间编码，弱空间调谐神经元则灵活切换至时间编码，且该梯度在不同环境中保持稳定。这揭示了MEC编码功能的分级组织原则。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737618-v1/fig-003.webp\", \"caption\": \"Figure 1. Experimental design and behavior for time and spatial tasks in head-fixed setup a. An example recording sequence consisted of an odor-based timing task (tDNMS), a dark session without sensory cues or reward, a virtual reality (VR) spatial navigation task, and open field foraging. Neural activity was recorded from MEC using Neuropixels probes. b. Schematic of the tDNMS task. In each trial, a pair of odor durations were presented (LongShort, Short-Long, or Short-Short), and mice were trained to discriminate the odor durations and respond accordingly. They needed to lick after the second odor to receive the reward in either Long-Short or Short-Long trials, whereas for Short-Short trials, mice needed to withhold licking. c. Lick raster plots from a representative session for each trial type. d. Behavioral performance of individual mice showing successful acquisition of the timing task. e. The VR environment used for the experiment from the mouse’s point of view. f. In the VR spatial task, mice ran along the track and received a water reward at the end of the track. Top panel shows a lick raster plot from a representative session, and the bottom panel\", \"page\": 21, \"index\": 3, \"width\": 791, \"height\": 713}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737618-v1/fig-004.webp\", \"caption\": \"Figure 3. Spatial and temporal information are represented by largely segregated populations in the MEC. a. Representative neurons for each cell type (grid cell, spatial cell, and time cell) across the VR, Dark, and tDNMS tasks. Left and middle panels are the same as those in Figure 2a. Right panel shows activity during the tDNMS task, with average rate map (top) and trial rate maps for each trial type (bottom). Gray shading indicates odor presentation. b. Proportion of spatial and temporal cell types (left) and Sankey diagram showing transitions between spatial and temporal classifications (right). Grid cells and spatial cells exhibited less overlap with time cells than expected by chance. c. Distribution of cell types in individual mice (n=7).\", \"page\": 24, \"index\": 4, \"width\": 641, \"height\": 968}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737618-v1/fig-001.webp\", \"caption\": \"Figure 4. Inhomogeneous coding flexibility across the MEC population a. Difference in GLM performance between spatial and temporal models (\", \"page\": 25, \"index\": 1, \"width\": 647, \"height\": 433}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737618-v1/fig-002.webp\", \"caption\": \"Figure 5. Grid cell population persists distance-tuned activity during the timing task. a. Time-lagged cross correlation matrices of simultaneously recorded MEC neurons during the Dark, tDNMS, and VR tasks. Neurons were sorted by agglomerative clustering of the correlation matrix during the Dark, and the same cell ordering was applied to the other tasks. The inset shows zoomed-in view of a highly correlated cluster, identified as a grid module, in the ensemble. b. Population activity of a representative grid module plotted as a function of traveled distance during the Dark (top) and the tDNMS task (bottom). Cells were sorted in the same order for the Dark and tDNMS tasks and showed similar sequential activity across tasks. c. Representative grid module activity was projected into a low-dimensional embedding. The projector was computed based on the neural activity during Dark and applied to activity during both Dark and tDNMS. Background gray dots represent population states and lines show state trajectories during the specified epochs in b. Population trajectories were similar across the two tasks.\", \"page\": 26, \"index\": 2, \"width\": 727, \"height\": 979}]"
motivation: MEC中空间与时间编码的神经组织方式尚未明确。
method: 采用高密度硅探针记录小鼠在计时任务和虚拟空间导航任务中MEC神经元的电活动。
result: 空间调谐强度与时间编码倾向呈负相关，强空间神经元鲜有可靠时间编码，弱空间神经元则更灵活，且该梯度在多个环境中稳定存在。
conclusion: MEC沿稳定梯度组织，从专用空间编码神经元到灵活的任务适应性编码神经元，按认知需求动态表征信息。
---

## 摘要
内侧内嗅皮层（MEC）传统上被视为空间编码脑区，但越来越多的证据表明它也包含时间表征。然而，空间和时间编码在MEC内如何组织仍不清楚。本研究在小鼠执行依赖MEC的计时任务和类似头部固定的虚拟现实空间导航任务时，用高密度硅探针记录了MEC神经元。我们发现空间和时间表征部分重叠，但在MEC群体中存在系统性偏倚。具有较强空间调谐的网格细胞和非网格细胞在计时任务中较少表现出可靠的时间锁定活动。相反，空间调谐较弱的神经元在计时任务中更灵活地将编码模式转换为时间编码。此外，空间调谐强度及其与时间调谐的负相关关系在一个不同的开放场地环境中得以保留，表明单个神经元的编码偏好受稳定的网络级组织所约束。总之，这些发现表明MEC沿编码梯度组织，从专门稳定空间编码的神经元到更灵活的空间或时间编码神经元，后者根据认知需求表征信息。

## Abstract
The medial entorhinal cortex (MEC) has classically been viewed as a spatial coding region, but growing evidence indicates that it also contains temporal representations. However, how spatial and temporal codes are organized within the MEC remains unclear. Here we recorded MEC neurons with high-density silicon probes while mice performed a MEC-dependent timing task and a virtual reality spatial navigation task in a similar head-fixed setup. We found that spatial and temporal representations were partially overlapping but systematically biased across the MEC population. Grid cells and non-grid cells with strong spatial tuning were less likely to show reliable time-locked activity during the timing task. In contrast, neurons with weaker spatial tuning more flexibly shifted their coding scheme to temporal coding during timing task. Moreover, spatial tuning strength and its negative relationship with temporal tuning were preserved in a distinct open field environment, indicating that the coding preferences of individual neurons are constrained by a stable network-level organization. Together, these findings suggest MEC is organized along a coding gradient, ranging from dedicated stable spatial coding neurons to more flexible spatial or temporal coding neurons which represent information according to cognitive demands.

---

## 论文详细总结（自动生成）

### 1. 论文核心问题与整体含义
- 内侧内嗅皮层（MEC）已被证实既包含空间表征（如网格细胞、位置细胞），又包含时间表征（如时间细胞），但这两类信息在 MEC 内部是如何组织的一直不明确。
- 核心疑问是：MEC 神经元是稳定地专司空间或时间编码，还是随任务需求动态切换？是否存在一个统一的组织梯度？
- 本研究旨在直接比较**同一批 MEC 神经元**在空间任务和时间任务中的编码特性，探讨空间与时间编码是分离、重叠还是以梯度形式分布，并检验编码偏好的环境稳定性。

### 2. 方法论
- **行为范式**：设计了一套可在同一头部固定装置上切换的两种任务——
  - **时间延迟非匹配样本任务（tDNMS）**：小鼠需判断两种气味持续时间的组合（长‑短、短‑长、短‑短）以决定是否舔舐获取水奖赏，依赖时间估计。
  - **虚拟现实（VR）线性轨迹空间导航任务**：小鼠在虚拟轨道上移动到终点获得奖赏，依赖空间位置。
  - 两任务间插入**黑暗会话**（无外部感觉线索和奖励），用于在缺乏空间参考时识别网格细胞的距离调谐特性。
- **电生理记录与细胞追踪**：使用 Neuropixels 2.0 高密度硅探针在 MEC 连续记录，所有任务在同一会话中依次进行，实现同一神经元的跨任务追踪。
- **细胞分类标准**：
  - **网格细胞**：基于黑暗会话中放电序列相对行走距离的功率谱密度（PSD），若峰值超过洗牌分布 $5\sigma$ 则认定为距离调谐网格细胞，并利用开放场地的二维网格评分进行交叉验证。
  - **非网格空间细胞**：在 VR 任务中空间互信息（MI）显著（$MI>0.3$，$p<0.001$）但未通过网格细胞判据的细胞。
  - **非空间细胞**：其余主细胞。
  - **时间细胞**：在 tDNMS 任务中，至少一种 trial 类型满足：存在显著时间野（持续≥750 ms）、试次间时间可靠性相关系数 $>0.15$（$p<0.01$）且野内放电参与率 $>40\%$。
- **量化编码偏好**：
  - 使用空间 MI 量化空间调谐强度，试次间相关系数量化时间调谐可靠性。
  - **广义线性模型（GLM）**：以泊松回归分别建立空间模型（位置/距离 spline）和时间模型（耗时 spline），计算相对空模型的对数似然提升 $LLHi_{spatial}$ 和 $LLHi_{temporal}$，并定义 $\Delta LLHi = LLHi_{spatial} - LLHi_{temporal}$，正值代表空间编码主导，负值代表时间编码主导。
- **群体动力学分析**：通过时间滞后互相关和凝聚聚类识别网格模块，经 PCA 和 UMAP 降维可视化状态空间轨迹，比较黑暗、tDNMS、VR 下的群体活动结构。

### 3. 实验设计与基准
- **实验动物与数据集**：
  - 主要数据集：7 只 C57BL/6J 小鼠（4 雄 3 雌），每只 1 次记录会话，共获得 1068 个 MEC 主细胞，依次执行 tDNMS → 黑暗 → VR 任务。
  - 交叉验证数据集：另外 4 只小鼠（4 次会话，825 个细胞），额外执行开放场地觅食任务，以验证 1D 距离调谐细胞与 2D 网格细胞的一致性。
- **对比与分析**：
  - 比较网格细胞、非网格空间细胞、非空间细胞与时间细胞的身份重叠，采用 Fisher 精确检验判断是否偏离随机期望。
  - 对比不同细胞类型在时间任务中的时间调谐强度（GLM ΔLLHi 和时间可靠性）以及在空间任务中的空间 MI。
  - 分析跨任务相关性：空间 MI（VR） vs. 时间可靠性（tDNMS），以及 VR 空间 MI vs. 开放场地空间 MI 的相关性。
  - 群体层面检验网格模块在计时任务中是否保持距离序列激活。
- **统计基准**：广泛使用洗牌方法构建零分布，用 Wilcoxon 秩和检验、符号秩检验、McNemar 检验等进行差异比较。

### 4. 资源与算力
- 文中未提及使用 GPU 或大规模算力。所有分析基于 Python（NumPy、SciPy、scikit-learn、statsmodels 等）完成，不涉及大型神经网络训练，对计算资源要求较低。
- 记录、预处理及 spike sorting 使用标准工作站即可，无特殊算力说明。

### 5. 实验数量与充分性
- 主要实验包括 7 个独立记录会话（1068 个细胞）的核心分析，以及 4 个额外会话用于网格细胞验证，合计 11 次记录。
- 实验设计相当系统：
  - 细胞分类与重叠分析（网格 vs 时间、空间 vs 时间）
  - 单细胞编码灵活性分析（GLM 跨任务偏转、空间 MI 与时间可靠性的相关）
  - 编码稳定性验证（VR 与开放场地空间 MI 的相关）
  - 群体网格模块动力学（互相关、排序、降维、事件对齐程度）
- 统计手段多样且严谨，洗牌控制抽样误差，多重比较时未见明显 p-hacking。
- 可能的局限：样本量仍属中等，未分别分析性别或 MEC 亚层；但总体实验设计对科学问题的回答是充分且客观的。

### 6. 主要结论与发现
- **空间与时间编码在 MEC 中部分重叠但存在显著偏斜**：网格细胞和时间细胞的重叠比例（6.7%）显著低于偶然水平；非网格空间细胞与时间细胞的重叠（9.6%）也偏低。
- **编码灵活性随空间调谐强度呈梯度变化**：
  - 强空间调谐的神经元（包括网格细胞和非网格空间细胞）在计时任务中时间调谐弱，且 GLM 表明其活动仍偏好空间模型。
  - 弱空间调谐的神经元更倾向于在计时任务中显示时间编码，表现出编码模式的灵活切换。
  - 空间 MI（VR）与时间可靠性（tDNMS）在全细胞群体中呈显著负相关。
- **编码偏好是神经元内在的稳定属性**：空间调谐强度在 VR 线性轨道和二维开放场地间显著相关，且该相关性在排除网格细胞后依然存在；开放场地的空间 MI 同样与时间调谐呈负相关。
- **网格细胞群体在计时任务中顽固保留距离调谐活动**：时间滞后互相关结构、顺序排布、低维状态空间轨迹在黑暗和 tDNMS 任务间高度相似，网格模块不随 trial 事件对齐，说明网络并未因时间任务需求而重组。

### 7. 优点
- **实验设计精巧**：在同一头部固定装置和可比运动状态下执行空间与时间任务，大幅减少行为状态混淆；通过黑暗会话统一识别网格细胞，并用开放场地交叉验证，增加了分类可信度。
- **多层次分析**：从单神经元身份重叠、调谐强度、GLM 编码主导性，到群体模块动力学和跨环境稳定性，系统地揭示了组织原则。
- **提出“编码梯度”新概念**：将 MEC 描述为从稳定空间细胞到灵活混合编码细胞的连续谱，为解释先前文献中重叠程度不一的现象提供了一个统一框架。
- **数据与代码透明**：详细的方法描述和预注册分析流程（代码库可用）提升了可重复性。

### 8. 不足与局限
- **任务未同时涉及空间与时间需求**：两种任务分离，无法直接观察同一行为情境下混合编码是独立表征还是整合编码。
- **感觉刺激差异**：计时任务以气味为线索，空间任务以 VR 视觉为主，可能影响 MEC 细胞参与度，但作者已以此解释与某些研究的重叠差异。
- **网格细胞分类依赖黑暗会话**：可能遗漏那些只在有外部线索时才表现网格模式的细胞，但 1D‑2D 验证缓解了这一顾虑。
- **样本量与层特异性**：总体细胞数适中，但未分析 MEC 浅层和深层的差异，也未探讨雌雄间的潜在不同。
- **因果性缺乏**：纯观察性研究，未通过光遗传或药物手段验证特定细胞类型在行为中的必要性。

（完）
