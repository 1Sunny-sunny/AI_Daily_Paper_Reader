---
title: Neural-vocal phase coupling reveals structured timing in birdsong production
title_zh: 神经-发声相位耦合揭示鸟鸣产生中的结构化时序
authors: "Leites, F. L., Boaretto, B. R. R., Masoller, C., Amador, A."
date: 2026-07-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.21.739824v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 神经-发声相位耦合揭示鸟类鸣唱的结构化时序
tldr: 理解神经活动与行为的时间协调是神经科学的核心挑战。本研究以鸣禽为模型，同步记录金丝雀前脑神经群体活动与自发鸣唱，采用相位分辨互相关及替代数据统计验证，量化短时、多变歌唱片段中的神经-发声交互。结果发现交互呈现先导、同步、跟随三种时序模式，且反相关集中于近零滞后，揭示了神经活动减少与发声对齐的瞬态关系，为从复杂生物信号中提取神经-行为交互提供了通用框架。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-002.webp\", \"caption\": \"Fig 1. Simultaneous recordings of vocal behavior and neural population activity. (a) Example oscillogram of canary song (Bird 1). Black bars indicate song phrases, and letters denote phrase identity within the bird’s repertoire. (b) Acoustic envelope of the song (ENV), highlighting the rhythmic temporal structure of vocal production. (c) Extracellular neural recordings obtained simultaneously from HVC during singing. (d) Multi-unit activity (MUA) derived from the extracellular recordings, providing a mesoscopic representation of coordinated neural population activity.\", \"page\": 7, \"index\": 2, \"width\": 950, \"height\": 542}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-006.webp\", \"caption\": \"Fig 2. Examples of the time series of MUA (X) and ENV (Y ), and the corresponding cross-correlation functions, CXY (τ) and CY X(τ). The analyzed interval corresponds to the full song duration (excluding the maximum lag, τmax = 1000 ms, required for the cross-correlation computation). We show three representative datasets used throughout this study: (a) Bird 3, (b) Bird 2, and (c) Bird 1. These recordings serve as illustrative examples that are further developed in the following sections. Here, the cross-correlation is computed over the entire song, whereas later analyses apply a sliding-window approach to the same datasets.\", \"page\": 8, \"index\": 6, \"width\": 764, \"height\": 700}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-003.webp\", \"caption\": \"Fig 3. Examples of cross-correlation analysis. For each example, the top left panel shows the MUA(X) signal, the bottom left panel shows the corresponding ENV(Y ) signal, and the right panel displays the cross-correlation functions CXY (τ) (orange) and CY X(−τ) (blue), computed with τmax = 200 ms. Dashed red horizontal lines indicate the significance thresholds obtained from surrogate data. Candidate peaks are marked by gray arrows, while matching peaks identified in both directions are highlighted in green. Peaks were considered valid only if they exceeded both surrogate thresholds and a fixed minimum correlation value of 0.5. Panel (a) shows several candidate peaks, but none exceed the surrogate thresholds, and therefore no significant correlation is identified. In panel (b), two prominent peaks with similar amplitudes are detected at opposite lags, preventing an unambiguous estimation of the lag. In panel (c), significant peaks are detected, but they are not symmetric between CXY (τ) and CY X(−τ), resulting again in an indeterminate lag estimation. Finally, panel (d) shows a clear and significant peak that is symmetric across both directions, allowing an unambiguous determination of the correlation and lag values.\", \"page\": 10, \"index\": 3, \"width\": 772, \"height\": 489}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-001.webp\", \"caption\": \"Fig 4. Temporal evolution of the cross-correlation values C∗ and the corresponding lags τ∗ (a) X (MUA) and (b) Y (ENV) signals for Bird 3 (sample 837). Cross-correlations were computed using sliding windows of 1200 ms. Each point represents the correlation analysis of the subsequent 1200 ms segment beginning at that time point. (c) Cross-correlation peak values C∗ and (d) corresponding lags τ∗ computed as described in the Materials and methods section. Only statistically significant values according to both block-shuffled and surrogate-data tests are shown. Blue and orange dots indicate correlation and anticorrelation, respectively. The window step was reduced to 20 ms for visualization purposes. Panels (e) and (f) show representative examples of the cross-correlation analysis for two selected 1200 ms segments. In each example, the left panels show the MUA (X) and ENV (Y ) signals, while the right panel displays the cross-correlation functions CXY (τ) (orange) and CY X(−τ) (blue), computed with τmax = 200 ms. Dashed red horizontal lines indicate significance thresholds obtained from surrogate data, and statistically significant matching peaks are marked with asterisks.\", \"page\": 11, \"index\": 1, \"width\": 761, \"height\": 781}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-005.webp\", \"caption\": \"Fig 5. Neural-vocal interactions cluster into discrete temporal regimes. Each column corresponds to one bird dataset. Histograms and kernel density estimates of lag values (τ∗) reveal discrete temporal classes rather than continuous distributions. Boxplots summarize the phase regimes identified from the density peaks and surrounding valleys (see Methods). Blue and yellow points indicate correlated and anticorrelated interactions, respectively. Distinct phase regimes are consistently observed across birds, revealing structured temporal organization in neural-vocal coordination during singing. Detailed values in Table S1.\", \"page\": 13, \"index\": 5, \"width\": 863, \"height\": 604}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739824-v1/fig-004.webp\", \"caption\": \"Fig 6. Representative examples of neural–vocal coupling regimes between the sound envelope (ENV) and the MUA. Each panel shows the envelope (top, black), the MUA (middle, blue or yellow), and their superposition after shifting the MUA by the estimated lag τ∗ (bottom). In anticorrelation cases, the MUA is inverted prior to alignment to facilitate peak–trough matching. Arrows indicate the temporal shift applied to the neural signal. (a) Correlation (C∗ > 0.5) with τ∗ > 0: neural activity precedes the acoustic signal (premotor regime). (b) Correlation (C∗ > 0.5) with τ∗ ≈ 0: neural and acoustic signals are temporally aligned (synchronous coupling). (c) Correlation (C∗ > 0.5) with τ∗ < 0: neural activity follows the acoustic signal (sensory-driven regime). (d) Anticorrelation (C∗ < −0.5) with τ∗ > 0: neuronal suppression precedes the acoustic signal. (e) Anticorrelation (C∗ < −0.5) with τ∗ ≈ 0: neuronal suppression is synchronized with sound production (antiphase). (f) Anticorrelation (C∗ < −0.5) with τ∗ < 0: neuronal suppression follows the acoustic signal.\", \"page\": 14, \"index\": 4, \"width\": 901, \"height\": 631}]"
motivation: 量化神经-发声交互的难点在于神经与声音信号均具有节律性、噪声和非平稳性。
method: 采用相位分辨互相关框架结合基于替代数据的统计验证，分析同步记录的神经群体活动与鸣唱行为。
result: 神经-发声交互组织为先导、同步、跟随三种时序模式，且反相关交互集中在近零滞后，揭示了神经活动减少与声音产生对齐的信息。
conclusion: 研究揭示了神经群体活动与发声行为之间的稳健时间结构，并提供了从复杂生物信号中提取瞬态神经-行为交互的通用方法。
---

## 摘要
理解神经群体活动如何在时间上与行为协调仍是神经科学的核心挑战。鸣禽为解决这一问题提供了强有力的模型系统，因为习得性发声需要神经动力学、时间结构化的运动输出和听觉反馈之间的精确协调。然而，量化神经-发声交互具有挑战性，因为神经和声学信号都具有节律性、噪声性和高度非平稳性。在此，我们通过同时记录鸣禽发声系统前脑区域的神经群体活动和发声行为，研究金丝雀自发鸣唱中的神经-发声协调。我们使用基于相位分辨的互相关框架结合基于替代数据的统计验证，在短且高度变化的鸣唱段落中量化神经-发声交互。我们的分析揭示，神经-发声交互被组织成不同的时间模式，包括正滞后、接近零滞后和负滞后，分别对应于神经活动先于、伴随或跟随发声输出。这些模式的共存与所记录脑区的整合作用一致，该脑区接收听觉输入，参与前运动控制，并参与支持鸣唱学习和成年鸣唱持续维持的神经回路。我们进一步发现，在鸣唱过程中，正相关和反相关交互共存，且反相关交互始终集中在接近零滞后的时间段。这些反相关关系识别出神经群体活动下降与发声密切对应的时期，揭示了被基于完整鸣唱段落分析所掩盖的生物学相关信息。总之，这些结果揭示了将神经群体活动与发声行为联系起来的稳健时间结构，并提供了一个从复杂生物信号中提取瞬时神经-行为交互的广泛适用框架。

## Abstract
Understanding how neural population activity is temporally coordinated with behavior remains a central challenge in neuroscience. Songbirds provide a powerful model system for addressing this question because learned vocal production requires precise coordination among neural dynamics, temporally structured motor output, and auditory feedback. However, quantifying neural-vocal interactions is challenging because both neural and acoustic signals are rhythmic, noisy, and highly nonstationary. Here, we investigate neural-vocal coordination during spontaneous canary singing using simultaneous recordings of neural population activity in a forebrain region of the song system and vocal behavior. Using a phase-resolved cross-correlation framework combined with surrogate-based statistical validation, we quantify neural-vocal interactions in short and highly variable song segments. Our analysis reveals that neural-vocal interactions are organized into distinct temporal regimes comprising positive, near-zero, and negative lags, consistent with neural activity preceding, accompanying, or following vocal output. The coexistence of these regimes is consistent with the integrative role of the recorded region, which receives auditory input, contributes to premotor control, and participates in the neural circuitry supporting song learning and the ongoing maintenance of adult song. We further find that correlated and anticorrelated interactions coexist throughout singing, with anticorrelated interactions consistently concentrated around near-zero lags. These anticorrelations identify periods in which decreases in neural population activity are closely aligned with sound production, revealing biologically relevant information that is obscured by analyses performed over complete song renditions. Together, these results uncover a robust temporal structure linking neural population activity to vocal behavior and provide a broadly applicable framework for extracting transient neural-behavioral interactions from complex biological signals.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义
- **研究动机**：理解神经群体活动如何在时间上与行为（尤其是复杂、节律性运动输出）相协调，是神经科学的核心难题。鸣禽（金丝雀）的习得性发声兼具节律性、噪声和非平稳性，且需要精确的神经‑运动‑听觉反馈协调，为研究这一问题提供了理想模型。
- **目标**：量化神经活动与发声行为之间的瞬时时间关系，揭示其潜在的时间结构，而非局限于传统的时间平均分析。
- **整体含义**：通过与行为时间对齐的神经‑发声相位耦合分析，作者发现该耦合并非由单一固定滞后描述，而是组织为多种离散的时间模式（神经先导、同步、跟随），其中反相关（神经抑制与发声对齐）是一种被传统方法掩盖的重要关系。该框架可推广至其他具有非平稳、节律信号的生物系统。

## 2. 方法论
- **核心思想**：在短滑动窗口内计算神经信号（多单元活动，MUA）与声学信号（包络，ENV）的相位分辨互相关，并通过严格的替代数据检验提取可靠的时间滞后（$\tau^*$）和耦合强度（$C^*$），避免全局平均掩盖瞬态耦合。
- **关键步骤**：
  1. **预处理**：从原始神经信号提取多单元活动（MUA），对声音计算RMS包络（ENV），均降采样至1 kHz。
  2. **滑动窗口互相关**：对每个窗口（长 $N=1200$ ms，最大滞后 $\tau_{\text{max}}=200$ ms）计算两个方向的互相关函数 $C_{XY}(\tau)$ 和 $C_{YX}(\tau)$（$X$=MUA，$Y$=ENV）。
  3. **峰值检测与筛选候选峰**：在 $|C_{XY}(\tau)|$ 和 $|C_{YX}(\tau)|$ 上寻找峰值，需同时满足：
     - 突出度 $>0.1$；
     - 绝对值 $>0.5$；
     - 统计显著性：超出基于迭代幅度调整傅里叶变换（IAAFT）生成的替代数据阈值，以及超出随机块混洗（不同窗口随机配对）获得的阈值。
  4. **一致性检验**：要求两个互相关函数中距零滞后最近的显著峰近似对称，即 $|\tau^*_{YX} + \tau^*_{XY}|<10$ ms，且两峰高度差异不超过10%，否则该窗口无有效滞后。
  5. **滞后与方向赋值**：取高度更高的峰，$C^*=C^*_{XY}$（或 $C^*_{YX}$），$\tau^*=\tau^*_{XY}$（或 $-\tau^*_{YX}$），保留符号以区分正相关（$C^*>0$）和反相关（$C^*<0$）。
  6. **分布分析与聚类**：对所有有效窗口的 $\tau^*$ 进行核密度估计，检测密度峰作为候选时间模式类，划分离散的滞后群体。

## 3. 实验设计
- **数据集**：3只成年雄性金丝雀（*Serinus canaria*），在繁殖季节自发鸣唱时同步记录。
  - **神经信号**：使用微电极阵列在鸣唱前脑核团HVC记录细胞外多单元活动（MUA）。
  - **声音信号**：同时录制音频，提取包络。
- **分析方式**：将每只鸟的完整鸣唱分割为1200 ms的滑动窗口，对每个窗口独立进行上述互相关分析，仅保留显著且一致的窗口，汇总 $\tau^*$ 分布。
- **对照/基准**：
  - **替代数据检验**：IAAFT方法生成保留频谱和幅度分布但破坏时间耦合的替代数据，计算100次获得置信阈值。
  - **随机块检验**：从同一记录中随机抽取MUA和ENV窗口配对1000次，评估偶然相关水平。
  - **无基准方法对比**：论文旨在描述性发现神经‑发声耦合模式，未与其他同步量化方法（如相位锁定值、格兰杰因果）进行直接比较。
- **统计模型**：使用线性混合效应模型（固定效应为相关类型，随机截距为个体/电极）检验 $\tau^*$ 是否因正/反相关而异。

## 4. 资源与算力
- **文中未提及GPU型号、数量或训练时长**。信号预处理和分析均在MATLAB离线完成，计算仅涉及互相关、替代数据生成和峰检测，无需大规模并行计算。未给出具体算力消耗或运行时间。

## 5. 实验数量与充分性
- **实验规模**：
  - 样本量：3只鸟，每只鸟可能包含若干记录片段（文中展示3个代表性数据）。
  - 分析单元：每个1200 ms窗口产生一个 $\tau^*$ 观测值，最终每只鸟的有效窗口数从数十到数百不等（如表S1：鸟1相关性类408个，鸟2相关性类358个等）。
  - 附加分析：进行了线性混合效应模型、核密度聚类等，对正/反相关进行了组内和跨个体的比较。
- **充分性与公平性**：
  - **优点**：在多个个体中重复观察到了相似的离散滞后类（如近零滞后、正滞后），且反相关的近零集中模式高度一致，增强了结论的可靠性。
  - **不足**：样本量较小（仅3只鸟），且均来自同一物种、相同脑区，结论的泛化性有限；未进行跨脑区或跨行为状态的对比；参数（窗口大小、阈值）虽基于经验选择，但可能随数据集变化，缺乏严格的交叉验证或参数敏感性分析。

## 6. 主要结论与发现
- 神经‑发声交互并非以单一固定滞后进行，而是**聚类为多个离散的时间模式**：正滞后（神经活动先于发声）、近零滞后（同步）和负滞后（神经活动跟随发声）。
- 这些**时间模式在记录个体的不同鸣唱段落中动态出现**，形成短暂的局部耦合体制，而非随机分布。
- **正相关与反相关交互共存**，且反相关模式**始终集中在近零滞后**区域，表明神经群体活动的抑制与声音产生在时间上紧密对齐，这一信息被全曲平均分析所掩盖。
- 滞后模式的存在与HVC脑区整合听觉输入、参与前运动控制和鸣唱维持的多种功能角色相符。
- 该方法成功从非平稳、节律性信号中提取了瞬时的神经‑行为交互，具有**广泛的适用性**。

## 7. 优点
- **方法创新**：结合滑动窗口、双向互相关、多准则峰值验证和替代数据统计检验，能稳健提取瞬态耦合的时间滞后，有效解决了传统全曲平均分析的模糊性。
- **生物学洞察**：首次在金丝雀鸣唱中系统揭示反相关耦合主要集中在近零滞后，凸显神经抑制与发声时间对齐的可能功能意义，扩展了只关注正激活的视角。
- **重现性**：主要发现（离散滞后类、反相关集中近零）在3只鸟中一致复现。
- **严谨的统计框架**：双重替代检验（IAAFT和随机块）为显著性提供了可靠依据。
- **普适性**：方法仅需两路同步时间序列，对动力学假设极少，可推广至其他类似生物信号。

## 8. 不足与局限
- **样本量小**：仅3只鸟，均在相同实验条件和脑区下，结果的外推性受限，尤其是不同物种、不同鸣唱核团或不同行为状态下是否成立未知。
- **参数敏感性**：窗口长度、最大滞后、峰值阈值等关键参数依赖人工设置，文中未系统探索不同参数对结果的影响，实际应用中可能需要针对不同数据集调整。
- **因果推断缺失**：互相关分析只能反映时间先后，不能确定因果方向。同时记录区域同时具有感觉和运动属性，难以区分是前运动输出、感觉反馈还是二者的混合。
- **空间分辨率**：使用的多单元活动反映局部群体脉冲，未分离单个神经元，可能混淆不同类型神经元的贡献。
- **分析范围有限**：仅关注包络与MUA的整体耦合，未分析音节/音素水平的精细对应，也未考察相位同步的其他指标（如相位锁定值、相干性），与现有方法的横向对比不足。
- **行为背景限制**：只分析了自发鸣唱，未涉及其他发声类型（如求偶鸣唱、听觉反馈扰动）或非鸣唱行为，限制了生态效度。

（完）
