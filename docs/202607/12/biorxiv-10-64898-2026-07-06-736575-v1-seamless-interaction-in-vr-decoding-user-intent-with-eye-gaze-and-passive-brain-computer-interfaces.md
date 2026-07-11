---
title: "Seamless interaction in VR: decoding user intent with eye gaze and passive brain-computer interfaces"
title_zh: VR中的无缝交互：利用眼动和被动脑机接口解码用户意图
authors: "Pan, Y., Rabe, L., Zander, T., Klug, M."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.06.736575v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 使用EEG和注视解码VR BCI中的交互意图
tldr: "本研究探索利用眼动追踪与被动脑机接口解码VR交互意图，包含物体可交互性评估和趋避决策。23人参与VR游戏，离线与在线分类均超随机水平（约66-70%），特定类别准确率超80%，用户认为BCI交互更有趣但控制感下降，首次实现动态VR中实时EEG意图解码。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-003.webp\", \"caption\": \"Fig. 1 Game environment. The participant fixated on an incoming rock to stop and destroy it. Shield status was displayed by the health bar in front of the participant, with the currently held inventory item, here armor, displayed at the bottom of the view\", \"page\": 7, \"index\": 3, \"width\": 775, \"height\": 479}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-006.webp\", \"caption\": \"Fig. 3 Trial procedure. In both calibration and online BCI sessions, gaze entry on an incoming rock triggered its deceleration and disappearance within 0.7 s, followed by item onset and a 1 s decision period. During the decision period, participants maintained fixation on the item, evaluated its task-relevant properties, and mentally decided which action to execute, while no overt action was allowed. At the end of this period, the item began to shake, indicating the onset of a 1.5 s action period. In the calibration sessions, participants executed take or discard actions manually using the controller, providing ground-truth labels for offline classifier training. In the online BCI session, the pre-trained classifier decoded EEG signals in real time, and the predicted action was transmitted via Lab Streaming Layer to the Unity environment for automatic in-game execution. Participants provided corrective feedback via button press only when the system executed an incorrect action\", \"page\": 9, \"index\": 6, \"width\": 508, \"height\": 831}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-004.webp\", \"caption\": \"Fig. 4 Classification accuracy for the post hoc category-level analyses. Raincloud plots Allen et al. (2019) show the per-participant decoding accuracies for each binary classification, with the distribution density, individual participant accuracies, and the median with interquartile range. Blue rows show actionable-category classifications, and green rows show actionable-versus-non-actionable classifications. The dotted vertical ticks indicate the simulation-based chance level (p = .05) for each classification. The figure complements the classification results reported in Table 2 by visualizing the robust separability observed in both the clearly valenced approach–avoidance classifications and the affordance-related classifications, as well as the near-chance performance of the context-dependent non-coin take versus non-bomb discard classification\", \"page\": 14, \"index\": 4, \"width\": 777, \"height\": 627}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-002.webp\", \"caption\": \"Table 2 Classification performance for post hoc category-level classifications\", \"page\": 15, \"index\": 2, \"width\": 756, \"height\": 328}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-001.webp\", \"caption\": \"Table 3 Exploratory questionnaire results for subjective evaluation of BCI interaction relative to controller baseline\", \"page\": 15, \"index\": 1, \"width\": 687, \"height\": 548}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-007.webp\", \"caption\": \"Fig. 5 Grand-average event-related potentials (ERPs; mean ± SEM, N=19) at midline electrodes (Fz, Cz, Pz, Oz) for all item categories. Time 0 ms marks item onset, followed by the 0–1000 ms decision period. Waveforms are shown for coins, bombs, non-coin take items, non-bomb discard items, and non-actionable rock fragments. Shaded regions indicate the standard error of the mean. The action period began after 1000 ms\", \"page\": 16, \"index\": 7, \"width\": 777, \"height\": 682}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-005.webp\", \"caption\": \"Fig. 6 Subjective evaluation of BCI interaction relative to controller baseline. Raincloud plots show the distribution of participant rating differences for the current BCI system and the hypothetical near-perfect BCI system, relative to the controller baseline. Positive values indicate more favorable ratings for the BCI condition under comparison, and negative values indicate less favorable ratings. Each raincloud displays the distribution density, individual participant responses, and the median with interquartile range. The dashed vertical line at zero indicates no difference between conditions. Significance levels from Wilcoxon signed-rank tests against the controller baseline are indicated next to each dimension label (*p ≤ .05, **p ≤ .01, ***p ≤ .001). The figure complements the results reported in Table 3 by visualizing the mixed rating pattern of the current BCI system and the more consistently positive rating pattern of the near-perfect BCI condition\", \"page\": 17, \"index\": 5, \"width\": 723, \"height\": 831}]"
motivation: VR交互依赖显式输入，需从神经信号直接解码交互意图以实现无缝自然交互。
method: 23名参与者通过眼动和被动脑机接口采集脑电，离线训练分类器，并在VR游戏中进行在线测试。
result: "离线平均分类准确率66.28%，在线69.64%，明显趋避配对达80.84%，可交互性分类达77-83%，用户认为BCI范式更有趣但控制感下降。"
conclusion: 首次展示动态VR中实时EEG解码交互意图，推动基于生理信号的直觉化自适应界面发展。
---

## 摘要
虚拟现实（VR）交互仍主要依赖于显式的运动输入，限制了无缝和自适应交互。本研究探讨了基于脑电图（EEG）的被动脑机接口（BCI）结合眼动能否在动态VR游戏过程中直接从潜在的神经生理相关活动中解码交互意图。我们将交互意图操作化为两个成分：示能性相关评估，指示被关注对象是否提供交互可能性；以及趋近-回避评估，指示交互指向期望或非期望结果的方向性倾向。23名参与者完成了一个包含两个校准阶段和一个在线BCI阶段的VR游戏。离线分析显示，在所有可操作试次中，二分趋近-回避决策分类的解码准确率高于随机水平，参与者间总平均准确率为66.28%。这一解码性能迁移至在线闭环游戏中，总平均准确率仍高于随机水平，达到69.64%。类别层面的分析进一步揭示分类可分性存在显著差异。在趋近-回避相关分类中，明确正负效价的奖励与惩罚类别配对准确率最高，达80.84%，但对于动机效价模糊、更依赖情境的配对，准确率下降至接近随机水平（59.03%）。不可操作与可操作物品类别之间的示能性相关分类准确率始终较高，范围为77.76%至83.50%。用户体验问卷结果表明，尽管存在一些局限导致感知失控和易用性下降，参与者仍认为基于BCI的交互范式比控制器基线更有趣。据我们所知，这是首次在动态VR游戏过程中实时通过EEG解码交互意图的演示，有助于构建由生理信号驱动的沉浸式环境中的直观用户自适应界面。

## Abstract
Virtual reality (VR) interaction remains largely dependent on explicit motor input, limiting seamless and adaptive interaction. This study investigated whether electroencephalography (EEG)-based passive brain-computer interfaces (BCIs), combined with eye gaze, can decode interaction intent directly from its underlying neurophysiological correlates during dynamic VR gameplay. We operationalized interaction intent as comprising two components: affordance-related evaluation, indicating whether an attended object affords interaction, and approach-avoidance evaluation, indicating the directional tendency of interaction toward desirable or undesirable outcomes. Twenty-three participants completed a VR game with two calibration sessions and one online BCI session. Offline analyses showed above-chance decoding of the binary approach-avoidance decision classification across all actionable trials, with a grand-average accuracy of 66.28% across participants. This decoding transferred to online closed-loop gameplay, where grand-average accuracy remained above chance at 69.64%. Category-level analyses further revealed substantial variability in classification separability. For approach-avoidance-related classifications, accuracy reached 80.84% for the most distinct pairing between clearly valenced reward and punishment categories, but dropped to near chance at 59.03% for the more context-dependent pairing with ambiguous motivational valence. Affordance-related classifications between non-actionable and actionable item categories were consistently high, ranging from 77.76% to 83.50%. User Experience questionnaire results showed that, despite limitations leading to perceived loss of control and reduced ease of use, participants found the BCI-based interaction paradigm itself more fun than the controller baseline. To our knowledge, this is the first demonstration of real-time EEG decoding of interaction intent during dynamic VR gameplay, contributing toward intuitive user-adapted interfaces driven by physiological signals in immersive environments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有虚拟现实（VR）交互严重依赖控制器或手动跟踪等显性运动输入，存在运动负担重、交互摩擦大、缺乏对认知情感状态的感知等问题，无法实现无缝、自适应的交互。本研究旨在探索一种**融合眼动追踪与被动脑机接口（pBCI）** 的新范式，从脑电图（EEG）信号中直接解码用户的**交互意图**，而非依赖传统的代理信号（如刺激前负波 SPN）。
- **整体含义**：将交互意图操作化为两个可分类的认知成分：**示能性评估**（注视对象是否可交互）和**趋近–回避评估**（对期望/非期望结果的方向性倾向）。通过在动态 VR 游戏中进行**离线训练与在线闭环测试**，首次证明 EEG 能够实时解码此类意图，为构建由生理信号驱动的直觉化、自适应 VR 界面提供了概念验证。

### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

- **核心思想**：利用被动 BCI 直接从脑活动推断认知状态，结合眼动注视解决“迈达斯触碰”问题（区分有意选择与随意注视），构建闭环神经适应交互。
- **关键技术细节**：
  - **范式与任务**：参与者注视飞来的石头使其停下并暴露物品，进入 1 秒的**决策期**（仅进行心理评估，不做外显动作），随后进入动作期。物品分为**可交互**（硬币、炸弹、食物、护甲）和**不可交互**（岩石碎片）两类；其中可交互物品又根据效价分为直接奖励/惩罚（硬币/炸弹）和情境依赖（食物/护甲）。
  - **信号采集与处理**：使用 64 通道有源电极系统，采样率 500 Hz，数据与事件通过 Lab Streaming Layer 同步。离线训练时，对校准 session 数据进行 0.1–15 Hz 带通滤波、共平均重参考，以物品起始为 0 点，取 0–800 ms 决策期数据，按 50 ms 无重叠分箱，提取每个通道在每箱的平均幅值，得到每试次 **64 通道 ×16 时间窗 = 1024 维特征**。
  - **分类器**：使用**正则化线性判别分析（LDA）**，结合自动协方差收缩和类别均衡。离线评估采用 5 折时序交叉验证；在线阶段将预训练分类器应用于实时流数据，预测结果通过 LSL 发至 Unity 执行动作，参与者仅在系统误判时按压按钮提供纠正标签。
  - **事后分析**：通过 ICA 去除眼动和肌电伪迹后，重新评估不同类别配对的分类性能。

### 3. 实验设计：使用了哪些数据集/场景，它与什么基准对比，对比了哪些方法

- **数据集/场景**：自建 VR 游戏场景（Unity 实现），23 名参与者（最终有效样本：离线 19 人、在线 18 人）。任务为连续防御护盾，通过注视和决策获取不同物品以恢复血量或降低伤害。游戏包含两个校准 session 和一个在线 session，每个 session 含 4 波难度递增的关卡。
- **基准对比**：
  - **离线与在线**：分类准确率与**模拟随机水平**（基于实际试次数分布多次仿真的 95% 上限）进行比较。
  - **事后类别配对**：对比了**可交互性相关**（可操作 vs 不可操作）和**趋避效价相关**（硬币 vs 炸弹；非硬币拿取 vs 非炸弹丢弃）等多个二分类问题。
- **对比方法**：本研究**未与其他解码方法或算法进行横向比较**，主要是对自身提出的 BCI 范式的可行性验证。用户体验问卷则将**当前 BCI 系统**和**假想准完美 BCI 系统**分别与**手柄控制器基线**进行主观评分对比。

### 4. 资源与算力

- 文中**未明确提及**所使用的 GPU 型号、数量、训练耗时等具体算力信息。仅提到 EEG 数据处理和分类在 MATLAB（R2024a）环境下使用 EEGLAB、BCILAB 等工具箱进行，分类器训练和在线推理均在常规实验计算机上完成，相关计算资源详情缺失。

### 5. 实验数量与充分性

- **实验组别**：主要进行了离线二分类（拿取 vs 丢弃）1 组；在线闭环测试 1 组；事后类别配对分析约 **6 组**（硬币 vs 炸弹，非硬币拿取 vs 非炸弹丢弃，以及四种可交互 vs 不可交互的配对）。此外，还有用户体验问卷分析。
- **充分性评价**：
  - **优点**：离线–在线顺序验证，类别层面分析揭示了可交互性和明确效价的可解码性，实验设计考虑到了真实游戏生态，较完整地支撑了概念验证。
  - **不足**：没有额外的消融实验（如不同特征窗、分类器对比、脑电通道子集等），也未对视觉混淆（如硬币更明亮）进行严格控制。样本量较小（19 人），缺乏对个体差异和跨被试泛化的系统分析。从方法论验证角度看，实验数量偏少，但作为首次动态 VR 在线 BCI 演示，其覆盖范围尚可接受。

### 6. 论文的主要结论与发现

- **可解码性**：交互意图的两个成分可以从 EEG 中解码。离线总体拿取 vs 丢弃准确率 **66.28%**（超随机），在线准确率 **69.64%**（超随机）。
- **类别差异化**：示能性相关分类（可交互 vs 不可交互）稳定可靠，准确率介于 **77.76%–83.50%**；在趋避评估中，明确效价的硬币 vs 炸弹准确率高达 **80.84%**，而情境依赖物品的分类（非硬币拿取 vs 非炸弹丢弃）接近随机水平（**59.03%**），表明决策模糊性显著影响解码。
- **神经生理特征**：可交互物品诱发了明显的额-中央区 **P300 样正波**（约 200–300 ms），不可交互物品无此成分；情境依赖类别 ERP 波形高度重叠，解释了其难分性。
- **用户体验**：与控制器相比，当前 BCI 系统被认为**更有趣**，但**控制感、易用性和满意度显著降低**。准完美 BCI 在多数维度上获得显著更高的评价，表明当前局限主要来自技术性能而非交互概念本身。
- **首次实现**：据作者称，这是**首次在动态 VR 游戏中实时通过 EEG 解码交互意图**的完整闭环展示。

### 7. 优点：方法或实验设计上的亮点

- **直接解码意图**：突破以往依赖 SPN 等代理信号的方法，从决策期神经活动直接解码意图。
- **二成分分解**：将交互意图细化为示能性评估和趋避评估，为神经适应系统提供了可单独利用的维度。
- **在线闭环验证**：不满足于离线分析，构建了端到端的实时 BCI‑VR 系统，证明了从校准到在线迁移的可行性。
- **生态化任务设计**：使用动态变化、难度递增的 VR 游戏作为测试平台，更接近真实 HCI 场景，而非简单实验室刺激。
- **多层面评价**：结合分类性能（离线、在线、类别层次）和主观用户体验，综合评估系统的可行性与接受度。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **视觉混淆**：硬币等物品在视觉上更明亮，可能部分混淆了效价相关的神经区分，尚未完全分离感知差异与评估差异。
- **在线标注方式**：在线准确率依赖参与者实时按压按钮报告系统误判，可能引入**标注噪声**和反应错误，且打扰游戏流。
- **样本量与统计力**：最终有效样本 18–19 人，用户体验分析为探索性，结果推广性受限。
- **解码性能局限**：情境依赖的趋避决策几乎无法解码（59%），意味着当前方法不能可靠解读需要信息整合的主观意志，限制了其在复杂决策场景中的应用。
- **未考虑用户状态变化**：虽提及信号非平稳性，但未采取在线自适应校准策略，长时间使用可能导致性能下降。
- **技术约束**：使用湿电极 EEG、较长的准备时间、固定的延迟（约 300 ms）以及未包含在线伪迹去除，都影响实用性和实时性。
- **缺乏严格对比**：未与其他意图解码算法或混合 BCI 架构比较，无法量化本方法相对于其他方案的优劣。

（完）
