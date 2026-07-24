---
title: Single-neuron and population contributions of hippocampal LFPs to spike prediction
title_zh: 海马局部场电位对锋电位预测的单神经元和群体贡献
authors: "Sato, R., Sommer, F. T., Agarwal, G."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738489v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 从局部场电位特征预测单神经元放电
tldr: 本研究针对海马局部场电位(LFP)中难以区分的单神经元与群体活动信号，通过分析LFP不同频率预测大鼠空间导航时神经元发放的空间分布和跨情境泛化性，发现锥体细胞的theta频段(~10Hz)预测主要反映分布式群体活动，高频预测反映局部单神经元活动，而gamma频段信息量少；中间神经元的分布式预测频段更宽。由此将海马CA1的LFP尖峰相关物分为theta分布式模式和高频局部模式。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738489-v1/fig-004.webp\", \"caption\": \"Fig. 1. Predicting spiking activity from different LFP frequency bands. A) A 64- or 256- channel electrode array was implanted in the CA1 region of the hippocampus (panel from Agarwal et al., 2014, with permission). B) Spikes and local field potentials (LFPs), sampled at 1250 Hz, were recorded from the electrode array. Spike counts and LFPs were decomposed into frequency-specific components, which were complex-valued (imaginary components indicated using dotted lines), and separate linear models were trained at each frequency to predict spiking activity from LFPs filtered in that band. C) Rats ran on a linear track in both directions. D) Linear models were trained on data from one running direction and tested on held-out trials from the same (“in-context”, or “IC”) and opposite (“out-of-context”, or “OOC”) running directions. Differences in predictive accuracy across contexts determine whether spike information in the LFP arises from the activity of peers, which is context-specific (dotted line), or the neuron’s own activity, which is context-independent due to its stereotyped impact on the LFP.\", \"page\": 27, \"index\": 4, \"width\": 976, \"height\": 860}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738489-v1/fig-003.webp\", \"caption\": \"Fig. 2. Frequency-dependent spike-LFP prediction for place cells and interneurons. A) Predictive accuracy (real part of the complex-valued Pearson’s correlation coefficient r, see methods) as a function of LFP frequency for pyramidal cells (left, n = 93 neurons from 2 sessions) and interneurons (right, n = 14 neurons from 2 sessions). Red (blue) lines indicate correlation coefficients calculated for in-context (out-of-context) predictions. Theta-band predictions generalize poorly across contexts for place cells but remain robust for interneurons. High-frequency predictions generalize for both cell types. Shaded regions indicate the standard error of the mean (SEM). B) Actual (top) and predicted (bottom) responses of a place cell and an interneuron using theta-band (10 Hz) and high-frequency (313 Hz) LFPs, as a function of position. For pyramidal cells, theta-band predictions reproduce place fields only in the training context. High-frequency predictions generalize across running directions. Colors denote the phase of spiking activity relative to the global theta rhythm. The in-context and out-of-context correlation coefficients (𝑟𝐼𝐶 and 𝑟𝑂𝑂𝐶) for the selected neurons are noted above the predicted responses in the bottom row.\", \"page\": 28, \"index\": 3, \"width\": 976, \"height\": 812}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738489-v1/fig-002.webp\", \"caption\": \"Fig. 3. Frequency-dependent spatial structure of spike-LFP prediction. A) Complex-valued model weights estimated from theta-band (10 Hz) and high-frequency (313 Hz) LFPs. The weights are reshaped according to the electrode geometry in the CA1 region. Theta-band weights are broadly distributed across the array. High-frequency weights are concentrated on the shank most proximal to the cell (located at the red dot). B) Weights across frequencies for a pyramidal cell and an interneuron. White dotted lines demarcate the 8 electrodes belonging to the same shank as the predicted cell. At low frequencies, predictive weights are broadly distributed across electrodes; at higher frequencies, contributions become concentrated near the cell’s location (red arrow). C) Average magnitude of weights along the medio-lateral (M-L) axis, relative to the cell’s location. Negative position indicates more dorsal locations. Average weight amplitudes show a localized component that becomes more prominent at high frequencies (black) and a distributed component that dominates at low frequencies (red).\", \"page\": 29, \"index\": 2, \"width\": 976, \"height\": 402}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738489-v1/fig-001.webp\", \"caption\": \"Fig. 4. Local and distributed sources of spike prediction in LFPs. A) Predictive accuracy for models using LFPs from the shank nearest the predicted cell (“Proximal”) or from all other shanks (“Distal”). For pyramidal cells, distal theta-band (10 Hz) models outperform proximal models, with both showing decreased accuracy out-of-context. In contrast, high-frequency proximal models outperform distal models and generalize across contexts. For interneurons, proximal and distal models show similar prediction accuracy across contexts over a broader range of frequencies. B) The in-context (IC) accuracy of proximal or distal models, relative to full model accuracy (𝑟𝐷𝑖𝑠𝑡𝑎𝑙 = 𝛽𝐷𝑖𝑠𝑡𝑎𝑙𝑟𝐹𝑢𝑙𝑙 or 𝑟𝑃𝑟𝑜𝑥𝑖𝑚𝑎𝑙 = 𝛽𝑃𝑟𝑜𝑥𝑖𝑚𝑎𝑙𝑟𝐹𝑢𝑙𝑙). The shaded gray indicates the 95% confidence interval (see methods). Proximal ratios increase to 1 at high frequencies for pyramidal cells; interneurons remain at around 1 for all frequencies. Distal ratios decrease at 20 Hz for pyramidal cells and 70 Hz for interneurons. C) Accuracy of models predicting pyramidal cell (left) and interneuron (right) activity using simultaneously recorded cells (peers) as regressors. Peer-based predictions closely resemble distal predictions for each cell type. Distal curves are identical to those shown in A. D) Similarity of proximal and distal models to peer-based models (see methods) for pyramidal cells (left) and interneurons (right). Each dot represents a single cell; dots above the identity line (blue) indicate greater similarity of peer-based models to distal models.\", \"page\": 30, \"index\": 1, \"width\": 976, \"height\": 479}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738489-v1/fig-005.webp\", \"caption\": \"Fig. 5. Generalized linear models (GLMs) provide cross-frequency predictions. Results are for a 64-channel array implanted in the pyramidal cell layer of CA1 (Fig. 1A, yellow array). A) Accuracy of pyramidal cell (top) and interneuron (bottom) predictions estimated by a GLM trained using LFPs filtered at different frequencies, as indicated above each column. Unlike linear models, GLMs predict spiking activity at frequencies outside the regressors’ frequency range, with prediction accuracy often peaking near theta (~8-10 Hz). For pyramidal cells, predictions driven by regressors above theta frequencies arise primarily from LFPs recorded on the same (proximal) shank. In contrast, interneurons are similarly predicted by proximal and distal LFPs across a broader range of frequencies. B) Overlays of in-context predictions from A) for pyramidal cells and interneurons showing that regressors from a broad range of frequencies generate predictions that peak near theta. Colors from black to red (5 -> 312 Hz) indicate increasing frequency.\", \"page\": 31, \"index\": 5, \"width\": 976, \"height\": 384}]"
motivation: 区分海马LFPs中单个神经元活动与群体协同活动的贡献仍是一个挑战。
method: 通过评估不同频率LFP预测单神经元发放的空间分布和行为情境泛化性来分离局部与分布式贡献。
result: 锥体细胞theta频段预测主要源于群体分布式信号，高频预测源于局部单神经元信号；gamma频段信息有限；中间神经元预测在更宽频段呈分布式。
conclusion: 海马CA1的LFP尖峰相关物可被分离为theta频段的分布式群体模式和高频的局部单神经元模式。
---

## 摘要
局部场电位包含了由单个神经元和协调性群体活动产生的信号，但区分这些贡献仍然是一个挑战。我们利用两个数据集，考察了在雄性大鼠空间导航过程中，不同频率的海马局部场电位如何预测单个神经元的发放。在每个频率上，我们评估了基于局部场电位的预测在整个电极阵列上的空间分布，以及其在行为环境变化时的泛化能力，即当某个神经元保持活跃但其协同活跃的同伴发生变化时。对于锥体细胞，空间分布性的局部场电位特征（与群体活动一致）主要在θ节律（~10 Hz）及其谐波上对发放预测做出贡献。相反，空间局域性信号（与所记录神经元的活动一致）主要在较高频率上占主导地位。值得注意的是，伽马波段局部场电位（30-80 Hz）对锥体细胞发放提供的信息相对较少，而分布性的局部场电位特征在更宽的频率范围内预测了中间神经元的发放。总体而言，这种预测方法分离了局部场电位中局域性和分布性的发放相关成分。在海马CA1区，这些相关成分呈现两种时空模式：分布性模式主要在θ频率上表达，而局域化模式反映了较高频率上的单神经元活动。

## Abstract
Local field potentials (LFPs) contain signals generated by individual neurons and by coordinated population activity, but distinguishing these contributions remains a challenge. We examined how hippocampal LFPs at different frequencies predict single-neuron spiking during spatial navigation in male rats using two datasets. At each frequency, we assessed the spatial distribution of LFP-based prediction across the electrode array and its generalization across behavioral contexts in which a neuron remained active, but its co-active peers changed. For pyramidal cells, spatially distributed LFP features, consistent with population-level activity, contributed primarily to spike prediction at theta (~10 Hz) and its harmonics. In contrast, spatially localized signals, consistent with the recorded neuron's activity, contributed predominantly at higher frequencies. Notably, gamma-band LFPs (30-80 Hz) provided comparatively little information about pyramidal-cell spiking, while distributed LFP features predicted interneuron spiking across a broader frequency range. Together, this predictive approach separates local and distributed correlates of spiking within the LFP. In hippocampal CA1, these correlates fell into two spatiotemporal regimes: a distributed regime expressed primarily at theta frequencies and a localized regime reflecting single-neuron activity at higher frequencies.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- 研究动机：局部场电位（LFP）同时包含单神经元活动（如胞外动作电位波形）和群体协同活动产生的信号，但在预测单个神经元发放时难以区分这两种贡献。
- 核心问题：不同频率和空间位置的 LFP 信息，到底来自所记录神经元本身的局部活动，还是来自周围神经元的分布式群体活动？
- 整体含义：通过分离 LFP 中的局部与群体成分，可以更清楚地理解海马 θ(~10 Hz)、γ(~30-80 Hz) 和高频振荡在神经编码中的不同角色，并重新审视 γ 节律在细胞集群组织中的经典解释。

## 2. 论文提出的方法论

- 核心思想：利用线性预测模型，将多通道 LFP 的复数化带通信号映射到同一频带的发放活动，再从空间分布和行为情境泛化性两个维度分离局部与群体贡献。
- 关键技术细节：
  - 连续小波变换（CWT）将发放计数与 LFP 同时分解为复值带通信号，保留相位信息。
  - 每个频率单独训练复数岭回归模型（$w = (X^{H} X + \lambda I)^{-1} X^{H} Y$），预测目标神经元的同频发放。
  - 以复值 Pearson 相关系数的实部 $\Re(r)$ 作为预测精度指标。
- 区分局部与分布式信号的策略：
  - 跨情境泛化：利用位置细胞的方向选择性，将同一跑动方向训练（in-context）与相反方向测试（out-of-context）的精度差作为群体依赖程度的度量（泛化好→神经元自身信号，泛化差→群体依赖）。
  - 解剖分离：将电极分为最近 shank（Proximal）与其余 shank（Distal），分别建模，比较两者精度相对于全模型的比率。
  - 权重空间分布：将模型权重按电极阵列几何重新排列，观察不同频段下权重的空间集中度。
- 补充分析：
  - 用同时记录的同伴神经元（peer）替换 LFP 作为回归子，验证群体预测能力。
  - 用广义线性模型（GLM）替代线性模型，探测 γ 波段是否通过非线性整流产生跨频率的预测。

## 3. 实验设计

- 数据集：两个公开数据集（hc‑3 和 AB3），来自雄性大鼠在 250 cm 直线跑道上的双向跑动任务。
- 电极：64 或 256 通道硅探针，主要植入海马 CA1 区锥体细胞层；部分分析涉及横跨 CA1 全层及齿状回的 256 通道阵列（红阵列）。
- 神经元类型：93 个锥体细胞、14 个中间神经元（来自 2 个 session），以发放率 >0.03 Hz 为筛选标准。
- 对照与比较的方法：
  - 线性模型（主要框架）vs. GLM（探测跨频率预测）。
  - LFP 回归子 vs. 同伴神经元回归子（peer-based 模型）。
  - 近端 vs. 远端 vs. 全模型。
  - In-context vs. out-of-context 测试。
  - 不同频段预测精度的比较（特别关注 θ 与 γ 的差异）。
  - 对 Harris 等 (2003) 的平滑核进行频域分析，证明其并非 γ 带通滤波器。

## 4. 资源与算力

- 论文未明确说明使用的 GPU 型号、数量或训练时长。
- 所有分析在 MATLAB 环境中完成，涉及 CWT 滤波、岭回归闭式解和 GLM 拟合，计算量中等，未提及大规模并行计算需求。

## 5. 实验数量与充分性

- 主要定量实验组数（可区分）：
  1. 全频段（5-312 Hz）线性模型在 in‑context 和 out‑of‑context 下的预测精度曲线（锥体细胞和中间神经元）。
  2. 近端/远端模型与全模型的精度对比（频率函数，两种细胞类型）。
  3. 模型权重的空间分布可视化（多个示例细胞及群体平均，沿频率和正则化强度展示）。
  4. 同伴神经元回归模型精度曲线，及其与近端/远端模型的相似性比较。
  5. GLM 在单频输入下产生的全频段预测分析（两种细胞类型，近端/远端对比）。
  6. 重复上述核心分析于 256 通道树突-体细胞跨层阵列（红阵列）以检验解剖泛化性。
  7. Harris 等 (2003) 平滑核的功率谱分析，揭示其低通而非 γ 选择特性。
- 充分性与公平性评价：
  - 实验设计通过多重交叉验证（情境、电极分组、细胞类型、模型类型、阵列类型）形成趋同证据，逻辑严密。
  - 中间神经元样本量较小（n=14），但其主要结论（分布式预测频段更宽）仍与锥体细胞形成清晰对照，且统计学检验均明确报告。
  - 对不同模型假设（线性 vs. GLM、LFP vs. peer）和经典文献（Harris 2003）进行了系统性检验，实验较为充分、客观。

## 6. 论文的主要结论与发现

- 海马 LFP 对锥体细胞发放的预测存在两个不同时空模式：
  - 低频（θ 及谐波）：预测依赖空间分布广泛、情境特异性强的群体活动，权重覆盖整个电极阵列，泛化性差。
  - 高频（>100 Hz）：预测依赖紧邻被预测神经元的局部信号，可跨跑动方向泛化，权重集中在该神经元的记录 shank 上。
- γ 频段（30-80 Hz）对锥体细胞发放几乎不提供额外的分布式预测信息（在全模型、peer 模型、GLM 以及树突层 LFP 分析中均一致），挑战了 γ 节律直接编码细胞集群发放率的传统观点。
- 中间神经元则不同：分布式 LFP 预测在更宽频率范围（包括 θ）保持高效，且跨情境泛化良好，表明其接收的群体信号维度较低、全局性更强。
- 线性模型估得的近端/远端权重过渡频率（锥体细胞 ~20 Hz，中间神经元 ~70 Hz）与两者胞外波形宽度差异一致。

## 7. 优点

- 思路精巧：利用位置细胞的方向敏感性设计跨情境泛化测试，无需事先定义行为变量即可区分局部与群体贡献，兼有预测建模和溯源分析的优势。
- 方法严谨：复数域线性模型自然捕捉相位关系，岭回归正则化；通过近端/远端分离、peer 模型、GLM、不同电极阵列等形成多维度趋同证据。
- 重要纠偏：通过频域分析证明经典研究（Harris 2003）的最优预测窗实为低通而非 γ 选择，对环环相扣的 γ 节律-细胞集群假设提出有力修正。
- 结果解释清晰：两个时空模式对应于两类神经元的差异化群体组织（高维位置编码 vs. 低维中间神经元信号），为后续研究提供了分离 LFP 信号源的实用框架。

## 8. 不足与局限

- 样本规模与多样性：中间神经元数量较少（n=14），统计分析效能受限；仅使用雄性大鼠和线性轨道任务，行为范式较简单，限制了结论在其他物种、性别或复杂空间记忆任务中的推广。
- 预测而非因果：模型只反映 LFP 对发放的统计预测关系，不能判定胞外电场是否通过触突耦合等方式因果性地影响发放。
- 神经元类型划分：未进一步细分中间神经元亚型（如 PV+、SOM+），不同类型的群体预测特性可能不同。
- 解剖覆盖：主要分析 CA1，虽测试了树突层 LFP，但未系统比较不同海马子区（CA3、齿状回）或跨脑区的 LFP 预测模式。
- 技术局限：CWT 选用单一 Morlet 小波族，未与其他时频分解方法对比；线性模型假设平稳性，未考虑跨试次学习或动态变化。
- 潜在偏差：排除慢速运动和静止期可能遗漏部分重要的非运动相关群体事件（如回放）；滤波和重采样可能引入边缘效应或相位失真。

（完）
