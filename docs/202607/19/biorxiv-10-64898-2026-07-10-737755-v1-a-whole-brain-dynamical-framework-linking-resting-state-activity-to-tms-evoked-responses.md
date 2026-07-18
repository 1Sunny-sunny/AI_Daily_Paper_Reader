---
title: A Whole-Brain Dynamical Framework Linking Resting-State Activity to TMS-Evoked Responses
authors: "Veronese, A., Momi, D., Sarasso, S., Corbetta, M., Allegra, M., Suweis, S."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737755v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 全脑动态模型连接TMS诱发反应与静息态活动
tldr: 本研究提出一个解析可处理的全脑生成模型，将静息态EEG活动与TMS诱发皮层反应联系起来。通过推导交叉谱密度的闭式解，无需时域模拟即可拟合静息态频谱并推断局部动力学参数，随后仅用少量TMS试次估计刺激特异有效连接。模型能准确预测不可见试次的TMS诱发电位时空模式，组级模板即可捕捉个体典型传播特征，为基于模型的个体化神经调控提供了分析框架。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-004.webp\", \"caption\": \"Fig. 1 Methodological workflow. Subject-specific connectome-based neurophysiological modelling of resting state EEG and generation of TMS–EEG TEPs. (A) The cortical surface is parcellated according to the Schaefer-200 atlas, with each parcel modelled as a network node governed by Hopf local dynamics. (B) The whole-brain model is constructed by embedding these nodes into a network defined by structural connectivity (SC) and individualized connectivity gains. This stage includes the derivation of the source-to-sensor mapping to project simulated source activity into the EEG channel space. (C) Model parameters are optimized by fitting the analytical covariance derived from the linearized system to the empirical resting state EEG covariance matrix, establishing the intrinsic dynamical scaffold. (D) The TMS pulse is reconstructed in source space by weighting parcels according to electric field magnitudes. A small subset (10%) of empirical TEP trials is selected for connectivity refinement. (E) Keeping fixed all local and global parameters derived from the resting, the effective connectivity obtained at rest is re-optimized using the 10% TEP training subset. The resulting generative model is driven by the reconstructed pulse to predict the full spatiotemporal evolution of the TEP for the remaining 90% of unseen empirical trials.\", \"page\": 4, \"index\": 4, \"width\": 700, \"height\": 446}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-001.webp\", \"caption\": \"Fig. 2 Hopf Whole Brain model resting state fit. (A) Empirical (left) and model (right) covariance matrices for a representative subject; the model captures the intrinsic spectral fingerprint. (B) Spatial distribution of the bifurcation parameter a on the Schaefer-200 parcellation, reflecting local neural population excitability. (C) The inferred effective connectivity (logECRest) exhibits a biologically plausible structure.\", \"page\": 6, \"index\": 1, \"width\": 700, \"height\": 619}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-002.webp\", \"caption\": \"Fig. 3 Site-specific TMS model simulations. Comparison of empirical (left column) and model (right column) responses in a representative subject (Subject 1). Temporal TEP correspondence for Motor (top row; ρ = 0.88 and R2 = 0.65) and Prefrontal (bottom row; ρ = 0.76 and R2 = 0.57) stimulation.\", \"page\": 7, \"index\": 2, \"width\": 775, \"height\": 398}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-006.webp\", \"caption\": \"Fig. 4 Evaluation of null conditions. Group-level goodness-of-fit metrics comparing the fully optimized personalised WBM against three control conditions: SC (structural connectivity only, paired with group-average local parameters), Rest Params (subject-specific, TMS-refined effective connectivity (EC) paired with donor resting-state parameters), and EC TMS (subject-specific resting WBM paired with donor TMS-refined EC). (Top) Pearson correlation (ρ) and (Bottom) Coefficient of determination (R2) between empirical and simulated TMS-evoked responses for the Prefrontal and Motor stimulation sites. Error bars represent standard deviation across subjects (N = 6 for Prefrontal and N = 5 for Motor). Significant differences from the personalised WBM are indicated (paired t-test, Bonferroni corrected; ∗p < 0.05, ∗ ∗ p < 0.01, n.s. = not significant).\", \"page\": 9, \"index\": 6, \"width\": 698, \"height\": 638}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-003.webp\", \"caption\": \"Fig. 5 Mechanisms of TMS-induced effective connectivity. (A) Differential effective connectivity matrices. Full ∆log(EC) matrices for Motor (top) and Prefrontal (bottom) stimulation, ordered by canonical Yeo networks.(B) Cortical topography of major enhanced sources. Spatial projection of the nodal source scores calculated from consistently enhanced edges (surviving a 95th percentile magnitude threshold and a strict subject-consensus mask). (C) Subject consistency of EC modulation. Pearson correlation (ρ) between individual-subject differential EC matrices and the group-level average for Motor (top, n = 5) and Prefrontal (bottom, n = 6) stimulation setups.\", \"page\": 10, \"index\": 3, \"width\": 777, \"height\": 523}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-005.webp\", \"caption\": \"Fig. 6 Validation of early TEP prediction using group-average effective connectivity. Comparison of empirical TEPs (left column) and model simulations utilizing a group-averaged ECTMS matrix (right column) for the Motor (top row; ρ = 0.69, R2 = 0.46) and Prefrontal (bottom row; ρ = 0.43, R2 = 0.18) stimulation sites in a representative subject (Subject 1). The topographies highlight that the model accurately captures the localized initial cortical response (6 ms) for both targets and early propagation (15 ms) for the motor target. Conversely, the timeseries illustrate the model’s systematic underestimation of late-stage amplitudes (50 ms), where complex or non-linear recurrent network dynamics typically emerge.\", \"page\": 12, \"index\": 5, \"width\": 781, \"height\": 392}]"
motivation: 理解内在脑动力学如何约束TMS诱发活动的传播仍存在挑战，全脑EEG层面的有效连接难以估计。
method: 推导模型交叉谱密度的闭式解，直接拟合静息态EEG频谱以推断局部参数，并利用少量TMS-EEG试次估计刺激位点特异有效连接。
result: 模型能准确预测未见过TMS试次中的TEP时空结构，且组水平有效连接模板即可复现单被试早期TMS反应的典型传播模式。
conclusion: 建立了适用于个体化全脑TMS-EEG建模的分析框架，对基于模型的神经调控具有潜在应用价值。
---

## Abstract
A major challenge in systems neuroscience is understanding how external perturbations interact with ongoing brain activity. Transcranial magnetic stimulation (TMS), increasingly used in both basic and clinical neuroscience and often combined with electroencephalography (EEG), provides a unique opportunity to probe this interaction. However, how intrinsic dynamics constrain the propagation of TMS-evoked activity remains poorly understood. In particular, effective connectivity (EC)--capturing directed, state-dependent interactions between brain regions--is thought to critically shape perturbational spread, yet remains difficult to estimate at the whole-brain EEG level. Here we introduce an analytically tractable, generative whole-brain model that links spontaneous EEG activity to cortical responses under perturbation. By deriving a closed-form expression for the models cross-spectral density, we directly fit empirical resting-state EEG spectra and infer biophysically interpretable local dynamical parameters without time-domain simulations. We then estimate stimulation-site-specific EC using only a small fraction of the TMS-EEG trials. The resulting model accurately predicts the spatiotemporal structure of TMS-evoked potentials (TEPs) in unseen trials. Moreover, even without subject-specific refitting, group-level EC templates capture canonical site-specific propagation motifs underlying single-subject early TMS responses. Together, our results establish an analytical framework for individualized whole-brain modeling of TMS-EEG with potential applicability to model-based neuromodulation.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义

- **研究问题**：外部扰动（经颅磁刺激，TMS）如何与大脑进行中的内在活动交互？内在动力学如何约束 TMS 诱发活动的传播？
- **背景与动机**：
  - TMS 联合脑电图（TMS‑EEG）能毫秒级观测局部皮层扰动如何在全脑传播，已在基础与临床神经科学中广泛使用。
  - 然而，扰动的传播机制仍未被充分理解，尤其是反映有向、状态依赖交互的**有效连接（effective connectivity, EC）**在全脑 EEG 水平上难以估计。
  - 现有模型或局限于少量节点（动态因果模型），或仅依赖解剖连接（虚拟大脑），难以同时复现静息态频谱与 TMS 诱发电位（TEP）。
- **整体含义**：本文提出一个**分析可处理、生成式全脑模型**，将静息态 EEG 活动与 TMS 扰动下的皮层响应联系起来，旨在建立从自发活动到诱发反应的桥梁，并为个体化神经调控提供计算框架。

### 2. 方法论

- **核心思想**：采用**Hopf 分岔模型（Stuart‑Landau 振子）**描述每个脑区的局部动力学，并用带延迟的结构连接矩阵耦合各脑区；通过线性化推导出**交叉谱密度的闭式解**，实现无需时域模拟的模型反演。
- **关键技术细节**：
  - 局部动力学：
    - 第 $j$ 个节点的实部动力学方程为：
      $$\frac{dx_j}{dt} = [a_j - (x_j^2 + y_j^2)] x_j - \omega_j y_j + g\sum_{k\neq j} C_{jk}[x_k(t - \tau_{jk}) - x_j(t)] + \eta_{x,j} + p_j(t)$$
    - $a_j$ 为分岔参数（控制局部兴奋性），$\omega_j$ 为固有频率，$g$ 为全局耦合强度，$C_{jk}$ 为连接增益（基于结构连接矩阵并加权），$\tau_{jk}$ 为传导延迟，$p_j(t)$ 为 TMS 脉冲在源空间的重构。
  - 频域求解：在线性化后得到频域算子 $U(\nu)$，交叉谱密度为 $\psi(\nu) = U(\nu) Q U^\dagger(\nu)$，源空间协方差 $\Sigma^{\text{src}} = 2\int_0^\infty \mathrm{Re}[\psi(\nu)] d\nu$。
  - 传感器映射：通过个体化导程矩阵 $\mathbf{G}$（利用模板 MRI 和 MNE 算法）投影到 EEG 通道：$\mathbf{Y}(t) = \mathbf{G X}(t) + \epsilon(t)$，得到传感器协方差 $\Sigma^{\text{sens}} = \mathbf{G} \Sigma^{\text{src}} \mathbf{G}^\top + \Sigma^{\text{noise}}$。
- **算法流程（两步训练）**：
  1. **静息态拟合（步骤一）**：
     - 利用静息态 EEG 数据，通过最小化模型预测与经验**对数传感器协方差矩阵**的 Frobenius 范数，估计节点特异性参数（$a_j$、$\omega_j$）、全局耦合 $g$、噪声标准差 $\sigma_{\text{in}}$、传导速度 $v_d$ 以及连接增益矩阵 $W_{ij}$（形成初始有效连接 $EC^{\text{Rest}}$）。
     - 此阶段完全基于静息态，生成“动态骨架”。
  2. **TMS 扰动下有效连接细化（步骤二）**：
     - 固定所有局部和全局静息态参数，仅利用**10% 的 TMS‑EEG 试次**重新拟合连接增益 $W_{ij}$，得到刺激位点特异有效连接 $EC^{\text{TMS}}$。
     - 优化时加入**高斯先验**，强制 $EC^{\text{TMS}}$ 接近静息态骨架 $EC^{\text{Rest}}$，防止过拟合。
     - 使用重构的 TMS 脉冲 $p_j(t)$ 驱动模型，预测剩余 90% 试次的 TEP 时空演化。
  - TMS 输入：利用 SimNIBS 计算电场分布，阈值化后归一化到峰值，作为各脑区的刺激权重。

### 3. 实验设计

- **数据集**：11 名健康被试（前额叶刺激组 $n=6$，运动区刺激组 $n=5$，另排除 1 名因伪迹过多者），每位被试均采集 60 通道静息态 EEG 和 TMS‑EEG 数据。
- **分区与连接**：皮层按 Schaefer‑200 图谱划分节点，结构连接使用 HCP 组平均纤维追踪，延迟按距离计算。
- **主要对比基准**：
  - **SC（结构连接基线）**：仅用结构连接和组平均局部参数，不进行有效连接推断。
  - **Rest Params（静息态参数交换）**：使用被试自身的 TMS 细化 EC，但静息态参数取自另一被试。
  - **EC TMS（TMS‑EC 交换）**：使用被试自身的静息态骨架，但 $EC^{\text{TMS}}$ 取自另一被试。
- **评估场景**：
  - 静息态拟合：用 20% 样本训练协方差矩阵，80% 测试，报道 $R^2$。
  - TEP 预测：运动区与前额叶两个刺激位点，在 0‑250 ms 窗口内计算时间序列 $\rho$ 和 $R^2$。
  - 跨站点泛化：额外测试前运动区和顶叶刺激数据（未参与主分析）。
  - 组平均模板测试：使用组平均 $EC^{\text{TMS}}$，结合个体静息态参数，预测早期 TEP（0‑100 ms）。
  - 控制实验：在相位乱化静息态 EEG 上验证模型不收敛。

### 4. 资源与算力

- 论文**未明确提及**所使用的 GPU 型号、数量或训练时长。
- 由于模型依靠闭式解直接计算协方差矩阵，避免大量时域模拟，反演过程主要依赖数值优化，计算量相对较小，可能未采用大规模 GPU 集群。

### 5. 实验数量与充分性

- 实验覆盖较全面，主要包括：
  - 静息态模型拟合与评估（1 组主要实验）。
  - TEP 预测（两个主要刺激位点，分别评估，共 2 组）。
  - **消融实验**（3 种控制条件：SC、Rest Params 交换、EC TMS 交换），比较个性化全脑模型相对于各基线的优势，使用配对 $t$ 检验和 Bonferroni 校正。
  - 跨站点泛化（额外 2 个位点）。
  - 组平均 EC 对早期 TEP 的预测能力（2 个位点）。
  - 相位乱化数据测试。
- **充分性评价**：
  - 实验设计系统、公平，通过消融清晰论证了“静息态先验”与“个性化 EC”的关键作用。
  - 跨位点测试与组平均泛化增加了结论的鲁棒性。
  - 但样本量较小（每刺激位点 5‑6 人），可能影响组水平模板的统计稳定性。

### 6. 主要结论与发现

- **静息态拟合成功**：模型在传感器空间高度复现静息态协方差结构（组平均 $R^2 = 74\% \pm 9\%$），推断出局部的**超临界动力学（$a_j > 0$）**，表明 α 节律源自主动极限环振荡而非噪声驱动。
- **有效预测 TEP**：
  - 仅用 10% TMS 试次训练，模型即能准确预测运动区 TEP（平均 $R^2 = 0.77$，可复现 N15‑P30‑N45 波形）和前额叶 TEP（平均 $R^2 = 0.50$）。
  - 运动区预测精度高于前额叶，提示前额叶可能激活更复杂、状态依赖的非线性动态。
- **关键组分的确定**：
  - 个性化有效连接 $EC^{\text{TMS}}$ 是准确预测的必要条件：交换 $EC^{\text{TMS}}$ 会大幅降低预测能力；仅依靠结构连接或交换静息态参数则影响较小。
  - 静息态骨架起到正则化作用，防止无约束优化产生生物学荒谬的解。
- **TMS 引起的连接重组模式**：
  - 广泛抑制多数通道，同时选择性地增强源自刺激靶区的少量通路，形成低维传播骨干。
  - 该调制模式在个体间高度一致（个体 $EC$ 变化矩阵与组平均的 $\rho$：运动区 ≈0.58，前额叶 ≈0.46）。
- **组平均模板的泛化性**：
  - 组平均 $EC^{\text{TMS}}$ 结合个体静息态参数，能近似预测单被试早期 TEP（0‑100 ms，运动区 $\rho$ 平均 0.52），尤其在极早期（0‑20 ms）吻合更好；晚期成分需要个性化 EC。
  - 这表明早期反应受共享的、位点特异的传播基序约束，而晚期动态则由被试特异的循环活动主导。

### 7. 优点

- **方法创新**：
  - 推导了耦合 Hopf 模型的**交叉谱密度闭式解**，无需时域模拟，大幅提高反演效率与稳定性。
  - 两步训练策略（先静息态后细化）为扰动预测引入生物学合理的先验，避免过度拟合。
- **解释性强**：
  - 参数具有生物物理可解释性（局部兴奋性、固有频率、传导速度），且优化不会收敛于相位乱化数据，增强了参数的可信度。
  - 清晰展示了 TMS 诱发的连接变化（全局抑制 + 选择性增强）及其与刺激位点的关系。
- **临床转化潜力**：
  - 模型仅需少量刺激试次即可实现个性化连接校准，为**在硅谷中前瞻性测试不同刺激靶点与方案**提供了可能。
- **可复现性**：代码已开源，所有分析可重复。

### 8. 不足与局限

- **样本量较小**：11 名被试分别分配在两个刺激位点（每类 5‑6 人），可能限制组水平结论的外推稳健性。
- **刺激位点不对称**：前额叶预测精度明显低于运动区，文中解释为可能涉及更复杂的非线性动态，现有静态 EC 模型未能充分捕获，但未深入解决。
- **模型假设**：
  - 有效连接被视为**静态**（不随时间变化），可能无法充分模拟晚期 TEP 中出现的非线性、时变交互。
  - 使用组平均解剖连接（因缺乏个体 DTI），可能降低个体化耦合的精度。
- **实验覆盖**：
  - 仅测试了运动区和前额叶两个主要位点（加上两个跨站点泛化验证），尚未涵盖更广泛的刺激脑区。
  - 未探讨不同脑状态（如睡眠、麻醉、认知任务）下静息态骨架的变化及其对 TEP 的影响。
- **TMS 脉冲重建**：依赖 SimNIBS 电场计算，假设模板个体化，可能与真实感应电场存在偏差。

（完）
