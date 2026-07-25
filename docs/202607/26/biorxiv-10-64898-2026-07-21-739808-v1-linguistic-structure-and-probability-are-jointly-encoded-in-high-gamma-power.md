---
title: Linguistic structure and probability are jointly encoded in high gamma power
title_zh: 语言结构与概率在高伽马功率中共同编码
authors: "Slaats, S., Hervais-Adelman, A."
date: 2026-07-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.21.739808v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 高伽马功率中语言结构和概率的联合编码
tldr: 该研究探讨言语理解中大脑如何组合词汇，利用颅内记录的高伽马功率，结合多变量时间响应函数和模型比较，发现高伽马功率同时编码语言结构和词汇概率，句法构建依赖背侧与腹侧通路的交互，且词汇不确定性调节句法信息的神经表征，支持灵活的前馈-反馈模型。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739808-v1/fig-002.webp\", \"caption\": \"Table 1. Features in each of the 16 fitted TRF models in the ‘joint encoding analysis. Abbreviations: Env. = speech 385 envelope; WO = word onset; WF = word frequency. 386\", \"page\": 10, \"index\": 2, \"width\": 950, \"height\": 439}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739808-v1/fig-001.webp\", \"caption\": \"Table 2. Features in each of the 16 fitted TRF models in the ‘split feature’ analysis. Abbreviations: Env. = speech 414 envelope; WO = word onset; WF = word frequency; surp. = surprisal; entr. = entropy; BU = bottom-up; TD = 415 top-down. 416\", \"page\": 11, \"index\": 1, \"width\": 950, \"height\": 896}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739808-v1/fig-004.webp\", \"caption\": \"Figure 4. The coefficients that describe the contribution of each feature to the model of the signal. Blue indicates 470 a negative contribution to a model of the signal; red indicates a positive contribution to a model of the signal. 471 Smaller (mostly white) electrodes were insignificant. The figure displays the left hemispheric pial surface of the 472 fsaverage brain. The medial view is tilted by 130° to visualize the ventral temporal electrodes. 473\", \"page\": 13, \"index\": 4, \"width\": 944, \"height\": 460}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739808-v1/fig-003.webp\", \"caption\": \"Figure 6. 488 Sensitive 489 electrodes to 490 each feature 491 and feature 492 combinations. 493 A electrode is 494 displayed if 495 the feature (or 496 features) in 497 question (all) 498 made a 499 significantly 500\", \"page\": 14, \"index\": 3, \"width\": 929, \"height\": 907}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739808-v1/fig-005.webp\", \"caption\": \"Figure 9. Temporal 637 response functions for 638\", \"page\": 17, \"index\": 5, \"width\": 927, \"height\": 1419}]"
motivation: 探究言语理解中词汇组合过程是受统计模式驱动还是由层次结构机制主导。
method: 通过对颅内脑电图的高伽马功率进行多变量时间响应函数和模型比较分析，研究词汇概率与句法结构的神经编码。
result: 高伽马功率对句法结构和词汇概率均敏感，句法构建涉及背侧与腹侧通路交互，且词汇概率影响句法信息的神经表征。
conclusion: 言语理解中语言结构和概率信息被灵活整合，词汇不确定性调节自上而下的句法预期，支持线索的灵活前馈与反馈利用机制。
---

## 摘要
在言语理解过程中，大脑从感觉输入中动态推断出层级递增的抽象表征。推断层级中的一个关键步骤是将词组合成短语和句子。这一过程主要是由语言输入中的统计模式驱动，还是由将词语组合成层级表征的机制驱动，是一个存在相当大争议的话题，随着大语言模型的出现，这一争议重新变得重要。本研究探讨了颅内记录中的局部皮层活动（高伽马功率；70-150赫兹）是否受到词汇概率和句法结构的共同调节，以及词汇概率是否影响句法结构的推断。为此，我们使用多变量时间响应函数和模型比较方法，对一个开放的皮层脑电数据集进行了分析。结果表明，高伽马功率对多词成分结构和词汇概率的估计敏感，无论是单独考虑还是联合考虑。时间响应函数表明，句法结构的建构依赖于通过背侧和腹侧流连接的区域之间的区域间通信。此外，本研究提供的证据表明，自下而上的句法信息不太可能由强烈编码词汇概率度量的神经群体编码，而自上而下的句法信息则与词汇不确定性共享神经资源。我们认为词汇不确定性调节了预期结构信息的权重。因此，本研究支持那些提出在言语理解过程中，线索以灵活的前馈和反馈方式被利用的模型。

## Abstract
During speech comprehension, the brain dynamically infers a hierarchy of increasingly abstract representations from the sensory input. An important step in the inferential hierarchy is the combination of words to form phrases and sentences. Whether this process is driven primarily by statistical patterns in the linguistic input, or by a mechanism that combines words into hierarchical representations, is a subject of considerable debate that has regained importance with the arrival of large language models. This study investigates whether local cortical activity (high gamma power; 70-150 Hz) from intracranial recordings is jointly modulated by lexical probability and syntactic structure; and whether lexical probability affects the inference of syntactic structure. To this end, an open dataset of electrocorticography recordings is analyzed with multivariate temporal response functions and a model comparison approach. The results indicate that high gamma power is sensitive to multi-word estimates of constituency structure and lexical probability estimates, both in isolation and jointly. The temporal response functions suggest that syntactic structure building depends on interregional communication between regions connected through dorsal- and ventral streams. Furthermore, the study provides evidence that bottom-up syntactic information is less likely to be encoded by neural populations that strongly code for lexical probability measures, while top-down syntactic information shares neural resources with lexical uncertainty. We suggest that lexical uncertainty modulates the weighting of anticipatory structural information. With this, the current study supports models that suggest that cues are leveraged flexibly in a feed-forward and feed-back fashion during speech comprehension.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的结构化中文总结。

---

### 论文核心问题与整体含义
- **研究动机与背景**：言语理解中，大脑如何将词语组合成有意义的短语和句子，是认知神经科学的核心争论点。一种观点认为此过程主要由**统计模式（词汇概率）** 驱动，另一种则强调基于规则的**层级句法结构**构建。本研究旨在调解这一争论，探究这两种信息源是否在大脑局部神经活动中被共同表征，以及它们之间如何相互作用。
- **核心科学问题**：(1) 高伽马功率（HGP， 70-150 Hz）这一反映局部神经元群体活动的指标，是否同时编码了**词汇概率**（如预测度、不确定性）和**句法结构**（如成分节点数）？(2) 词汇概率是否影响句法结构构建的神经编码，即两者是否存在交互作用？
- **整体含义**：该研究旨在验证一个**动态、交互式的言语理解模型**，即大脑会灵活地整合来自概率统计和句法结构的线索，而非依赖单一机制，支持前馈与反馈相结合的语言加工框架。

### 方法论
- **核心思想**：利用**多变量时间响应函数**建模，通过线性回归的方式，将连续的神经信号（HGP）分解为多个语言特征（如词汇频率、预测度、句法节点数等）在时间维度上的贡献。通过**模型比较**来量化每个特征对信号变异的解释力。
- **关键技术细节**：
    - **信号处理**：对颅内脑电图（iEEG）数据进行预处理，通过Morlet小波变换提取70-150赫兹的高伽马功率（HGP），并转换为分贝（dB）尺度。
    - **特征工程**：
        - **基础特征**：语音包络、词起点、词频（用于剥离低层听觉和词汇加工）。
        - **词汇概率特征**：**预测度**（Surprisal， $I(w_i) = -\log_2 P(w_i|w_{i-1}...w_{i-n})$）和**不确定性**（Entropy， $H(w_i) = -\sum_k P(w_k|...)\log_2 P(w_k|...)$），这些值通过基于荷兰语微调的GPT-2模型计算得出。
        - **句法结构特征**：手动标注刺激材料的成分句法树，并基于**自下而上**（Bottom-up）和**自上而下**（Top-down）两种解析算法，计算在每个词位置所构建的**句法节点数**。
    - **模型构建与比较**：
        - **联合编码分析**：为每个电极构建包含不同特征组合的16个TRF模型（从仅包含基础特征到包含全部四种实验特征）。对于每个电极，使用普通最小二乘（OLS）回归，以R²值为因变量，以模型中是否包含某个特征为自变量，来评估该特征对模型拟合的**独立贡献度**。
        - **交互作用分析**：采用**特征分割法**，将句法节点数根据词汇概率（如预测度或不确定性）的中位数分为“高概率”和“低概率”两个特征。比较这种“系统性分割”模型的R²是否显著高于1000次“随机分割”的R²。若显著，则证明存在交互作用。
        - **统计检验**：采用**置换检验**确定效应显著性，以避免参数假设。

### 实验设计
- **数据集**：使用了公开的颅内脑电图数据集“Open multimodal iEEG-fMRI dataset”（OpenNeuro ds003688）。数据来自18名（12名女性，均为右利手，左侧语言优势）为治疗耐药性癫痫而植入电极的患者，共分析了左侧半球的1377个电极。
- **刺激与场景**：参与者观看荷兰语配音的电影《Pippi on the run》节选，分析了电影中6段、每段30秒的纯语音片段。这是一种高生态效度的**自然言语理解**场景。
- **baseline 与对比**：
    - **基准模型**：仅包含语音包络、词起点、词频三个基础特征的TRF模型。
    - **特征对比**：对比了**两种句法解析策略**（自下而上 vs. 自上而下）和**两种词汇概率度量**（预测度 vs. 不确定性）对HGP的贡献。
    - **模型对比**：通过对比包含不同特征组合的16个模型的拟合优度（R²），系统性地评估了每个特征的独特贡献及其联合编码模式。

### 资源与算力
- 论文未提及所需的GPU型号、数量或具体的模型训练时长。分析主要基于已预训练好的GPT-2模型进行概率估算，并使用线性回归模型（OLS和岭回归），这些计算对算力要求不高，通常在标准CPU工作站上即可完成。

### 实验数量与充分性
- **实验数量**：
    1.  **联合编码分析**：对554个有效电极，估计了16个TRF模型，并逐一评估了4个实验特征（预测度、不确定性、自下而上节点数、自上而下节点数）的贡献。
    2.  **交互作用分析**：测试了4种交互类型（2种句法特征 × 2种概率特征），对每个相关电极进行1000次随机分割的置换检验。
    3.  **时间进程分析**：对显著电极的TRF波形进行了峰值聚类和相关性分析。
- **充分性与公平性**：
    - **充分性**：实验设计**高度系统且充分**。通过穷举所有特征组合进行模型比较，能够独立有效地评估每个特征在存在多重共线性时的独特贡献，方法学上非常严谨。
    - **客观公平性**：研究使用了**公开数据集**，保证了结果的可重复性。对比分析基于客观的模型拟合优度（R²）和置换检验，避免了主观偏误。对比了不同类型的句法和概率度量，分析全面。

### 主要结论与发现
1.  **高伽马功率（HGP）对句法结构和词汇概率存在联合编码**：所有四个实验特征（预测度、不确定性、自下而上句法节点、自上而下句法节点）都能独立且显著地解释HGP的变异，证实了这些语言属性在局部皮层活动中被共同表征。
2.  **句法信息的空间分布与动态机制**：
    - **自下而上句法节点**主要作用于额下回岛盖部/三角部及颞叶前部。
    - **自上而下句法节点**则分布于缘上回、顶下小叶、颞中回等区域。
    - TRF波形显示，句法加工不是瞬时的，而是一个包含多个阶段、涉及**背侧和腹侧通路**间循环沟通的动态过程，波动频率处于delta-theta范围。
3.  **概率信息的关键作用**：**词汇预测度（Surprisal）** 是解释HGP变异最主要的因素，其效应在颞上回和额下回最大，表明意料之外的词会引发强烈的HGP增加。
4.  **概率与句法的交互作用**：
    - **分离性**：自下而上句法编码与词汇概率编码呈**负相关**，表明它们可能依赖不同的神经群体。
    - **共享性与调节**：自上而下句法编码与词汇不确定性呈**正相关**，且两者存在交互作用。证据显示，**词汇不确定性会调节自上而下句法预期的权重**：当词汇不确定性较低时，自上而下的预期性结构信息在理解中扮演更重要的角色。
5.  **总体结论**：言语理解是一个**动态地、灵活地整合多线索**的过程，概率期望和句法结构被大脑交互式地处理，支持了语言加工的前馈-反馈模型。

### 优点
- **方法论创新与严谨**：采用多变量TRF和穷举模型比较，有效解决了语言特征间的高共线性问题，能够客观地分离并量化每个特征的独立贡献。
- **分析维度全面**：不仅探讨了特征的“独立编码”，还深入分析了“联合编码”和“交互作用”，从多个层面刻画了神经动态。
- **高生态效度**：使用自然连续的语音材料（电影对白），而非人工编制的实验刺激，结果更贴近真实语言加工。
- **时空动态的精细刻画**：通过TRF提供了毫秒级的时间进程信息，并结合电极的空间分布，揭示了句法加工可能涉及的背/腹侧流网络动态。

### 不足与局限
- **数据量有限**：分析基于6段30秒的语音（仅442个词），数据量偏小，可能影响TRF模型估计的稳定性，并限制了交互作用的检出效力（检出电极数很少）。
- **侵入性记录限制**：颅内电极植入依赖于临床需求，导致电极覆盖在个体间不完整且不均一，难以进行全脑水平的群体推断。
- **概率度量的解释性**：从大语言模型（GPT-2）导出的预测度是一个综合性指标，可能混杂了语义、句法、语用等多种信息，难以将其效应纯粹归因为“概率加工”。
- **相关性局限**：TRF模型揭示的是刺激特征与神经活动的**相关性**，尚不能直接证明因果关系。
- **结论的普适性**：被试群体为特定癫痫患者，尽管采取了严格筛选（左侧语言优势、利手），结论向健康人群推广仍需谨慎。

（完）
