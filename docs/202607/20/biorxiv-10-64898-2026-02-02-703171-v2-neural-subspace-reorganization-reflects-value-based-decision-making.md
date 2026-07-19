---
title: Neural subspace reorganization reflects value-based decision making
title_zh: 神经子空间重组反映基于价值的决策
authors: "Li, H., Chrysanthidis, N., Brincat, S. L., Rose, J., Miller, E. K."
date: 2026-07-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.02.703171v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 解码价值决策中LPFC的神经活动模式
tldr: 价值决策需要维持和比较选项，本研究通过记录非人灵长类外侧前额叶皮层活动，发现决策后选项表征发生神经子空间重组：选中与未选选项旋转至正交子空间，选中选项表征扩展并映射到一致动作表征子空间，表明决策驱动表征变化以高效指导行为。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-004.webp\", \"caption\": \"Figure 1. Experimental paradigm and behavioral results A Time course of a task trial, proceeding from left to right. Two spatial targets (T1 and T2) were shown, paired with abstract cues (R1 and R2) signaling the reward value available if the preceding target was chosen. The NHPs’ task was to choose the target associated with the higher reward. B Probability of choosing the high-reward target for NHP T (top) and NHP I (bottom) across all combinations of first and second reward values. Values along the diagonal — where the same reward was offered for both targets — were not tested. C Probability (mean ± SD across sessions) of choosing the first presented target at different relative reward levels (first-target reward – second-target reward). Both NHPs reliably chose the higher-value target across all pairs of first and second reward values.\", \"page\": 4, \"index\": 4, \"width\": 754, \"height\": 829}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-006.webp\", \"caption\": \"Figure 2. LFP encoded information about both reward cue value and target location A Decoding accuracy of first (R1; cyan) and second (R2; purple) reward cue value. B, C Decoding accuracy for the first (T1; green) and second (T2; orange) target location in trials where the first target was chosen (R1>R2; B) and where the second target was chosen (R1<R2; C) for both NHPs. Width of markers at top indicates significance: p<0.05, p<0.01, p<0.001 for thin, medium, thick markers respectively (corrected one-sided bootstrap against chance level).\", \"page\": 5, \"index\": 6, \"width\": 915, \"height\": 479}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-001.webp\", \"caption\": \"Figure 3. Between- and within-class variance of target information A, C Between-class variance of target locations for the first (green) and second (orange) targets, averaged over all neurons for trials where the first target was chosen (A) and where the second target was chosen (C). B, D Within-class variance of target locations, averaged over all neurons for trials where the first target was chosen (B) and where the second target was chosen (D). The within-class variance has only a single curve because it was computed for each combination of first and second target locations (i.e. each “cell” in the T1 x T2 design; see Methods). After the decision, the representation of chosen target locations became more separated, resulting in increased decoding accuracy.\", \"page\": 6, \"index\": 1, \"width\": 923, \"height\": 335}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-002.webp\", \"caption\": \"Figure 4. Chosen and unchosen targets became orthogonal after decision A Schematic figure showing the contrast between representations of the same target (first/T1 or second/T2) conditions between trials that resulted in different choices (choose T1 [R1>R2] vs choose T2 [R1<R2]). B Subspace alignment between representation of chosen and unchosen first targets (or between chosen and unchosen second targets) was computed as the average Pearson correlation between population coding vectors of corresponding locations between the two targets. C Geometry of chosen (red lines) and unchosen (blue lines) first targets before (left) and after (right) decision in reduced 3D space. Four colored dots correspond to the four target locations for each condition. After decision, chosen and unchosen targets are rotated into orthogonal subspaces. C Dynamics of subspace alignment (mean ± SD across pseudopopulation bootstraps) between chosen vs unchosen first targets (green line) and between chosen vs unchosen second targets (orange line) across time. The gray dashed line shows information reflecting the second reward value (R2; replotted from Figure 2A), for temporal comparison. Markers at top represent corrected one-sided bootstrap of Pearson correlation for first targets (green) and second targets (orange) against zero. Marker width indicates significance: p<0.05, p<0.01, p<0.001 for thin, medium, thick respectively. Arrows at bottom represent the latency of R2 information (gray arrow) and the decrease in correlation for the first target (green arrows) and for the second target (orange arrow).\", \"page\": 7, \"index\": 2, \"width\": 975, \"height\": 377}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-003.webp\", \"caption\": \"Figure 5. Target representations were reorganized by choice after decisions A Schematic figure showing the contrast between targets with different order of presentation but resulting in the same choice. B Subspace alignment between first and second targets when they were each chosen (or between the two targets when they were both unchosen) was computed as the average Pearson correlation between population coding vectors of corresponding locations across the two targets. C Geometry of the first (solid lines) and second (dashed lines) targets when they were chosen, before (left)\", \"page\": 8, \"index\": 3, \"width\": 987, \"height\": 396}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-02-703171-v2/fig-005.webp\", \"caption\": \"Figure 6. Aligned target subspaces remained separable by choice A Decoding accuracy of choice (whether the first or second target was chosen) before and after decision for both NHPs. The markers at top represent corrected one-sided bootstrap of decoding accuracy of choice against chance level. B The mean projection of population coding vectors of chosen targets (first target chosen: green line; second target chosen: orange line) onto the decoder choice axis. Lighter lines show the projection of each individual location for each chosen target. C Subspace alignment between choice axis and target location axes. Green line represents the alignment between choice axis and the first target chosen and orange line represents the alignment between choice axis and the second target chosen.\", \"page\": 9, \"index\": 5, \"width\": 937, \"height\": 463}]"
motivation: 理解价值决策如何动态重塑选项神经表征。
method: 猴子在执行顺序呈现的选项-价值保持与选择任务时，记录外侧前额叶皮层神经活动。
result: 决策后，选项表征旋转到正交子空间，选中选项表征扩展，并与动作表征一致子空间对齐。
conclusion: 决策促使神经子空间重组，以利于动作的精准读出。
---

## 摘要
基于价值的决策需要维持和比较与不同价值相关联的多个选项表征。然后，所选选项必须传递给下游脑区以驱动行为。参与基于价值决策的神经环路日益清晰，但决策如何塑造选项表征却鲜为人知。我们在非人灵长类动物（NHPs）工作记忆中保持两个相继呈现的选项-价值配对（空间目标和抽象奖励线索），然后选择价值更高的选项，同时记录外侧前额叶皮层（LPFC）——一个将选项转化为动作的中心枢纽。这揭示了决策如何动态重组LPFC中的选项表征。我们发现，一旦可以做出决策，所选和未选选项的表征会旋转到正交子空间中，且所选选项的表征得到扩展。在决策前，首先呈现和第二次呈现的选项是分别维持的。决策后，所选选项被旋转到一个子空间，该子空间对规定动作有一致的表征，无论其呈现顺序如何。这表明了一种基于价值决策的机制，其中决策驱动神经子空间重组，从而促进所选动作的选择性和高效读出。

## Abstract
Value-based decision making requires maintaining and comparing multiple option representations associated with different values. Then, the chosen option must be communicated to downstream regions to drive behavior. The neural circuits involved in value-based decisions are increasingly well understood, but less understood is how decisions shape option representations. We recorded from lateral prefrontal cortex (LPFC), a central hub for transforming options into actions, while non-human primates (NHPs) held two sequentially presented option-value pairs (spatial targets and abstract reward cues) in working memory, then chose the option with the higher value. This revealed how decisions dynamically reorganize option representations in LPFC. We found that, once decisions could be made, representations of chosen and unchosen options rotated into orthogonal subspaces and the chosen option representation was expanded. Before decisions, the first- and second-presented options were maintained separately. After decisions, the chosen option was rotated into a subspace with a consistent representation of the prescribed action, regardless of its presentation order. This suggests a mechanism for value-based decisions where the decision drives a neural subspace reorganization that facilitates selective and efficient readout of the chosen action.

---

## 论文详细总结（自动生成）

好的，这是根据您提供的论文内容进行的结构化、深入的分析总结。

### 1. 论文的核心问题与整体含义

-   **研究背景与动机**：
    -   基于价值的决策（value-based decision making）是一个多阶段过程，包括：表征可用选项、赋予价值、比较价值、选择高价值选项。
    -   虽然选项价值如何被编码和比较已有较多研究，但对于**多个选项是如何在工作记忆中同时被表征，以及决策如何动态重塑这些表征**的理解尚不清晰。
    -   外侧前额叶皮层（LPFC）被认为是连接选项、价值和动作，并基于价值选择动作的关键脑区，是研究此问题的理想靶点。

-   **核心问题**：
    -   在基于价值的决策过程中，LPFC神经元群体活动的**表征几何（representational geometry）如何动态变化**，尤其是决策前后选项表征的神经子空间（neural subspace）如何重组。
    -   具体而言，研究探讨了决策如何改变选项表征的组织原则：是从保持呈现顺序信息转向表征选择状态（选中vs未选中）。

-   **整体含义**：
    -   该研究揭示了**价值决策驱动神经子空间重组**这一机制。决策前，选项按呈现顺序被分隔在正交子空间中以保持独立。决策后，这些表征发生“旋转”，所选选项被整合到一个共同的动作准备子空间中，而未选选项则被置于一个正交的子空间里。这种重组有助于下游脑区**选择性且高效地读出所选动作**，同时减少干扰。

### 2. 论文提出的方法论

-   **核心思想**：利用群体水平的神经活动降维和几何分析，来刻画选项表征在决策前后的动态变化，而非仅仅关注单个神经元的活动变化。

-   **关键技术细节与分析流程**：
    1.  **数据获取与预处理**：
        -   记录非人灵长类动物（NHPs）在执行任务时LPFC的神经元脉冲（spiking）活动。
        -   构建**伪群体（pseudopopulation）**：将所有记录时段的神经元组合起来，模拟为同时记录的神经群体，并通过多次（1000次）随机重采样试验来控制各条件下的试验数量。

    2.  **群体状态空间分析**：
        -   使用**Lasso回归**来量化每个神经元对第一和第二目标空间位置的独立反应，得到回归系数 $$\beta$$，作为神经元的“调谐”参数。
        -   回归模型：神经元 $i$ 在时间 $t$ 的放电率 $y_{i,t}$ 是目标位置 $X$ 的线性组合，因设计矩阵欠定，引入 Lasso 正则化以防止过拟合并解决共线性问题。群体编码向量即为所有神经元对某一目标位置的回归系数构成的向量。

    3.  **表征几何量化——子空间对齐（Subspace Alignment）**：
        -   定义“子空间对齐”的度量：计算两种条件下，对应目标位置（如位置1 vs 位置1）的群体编码向量之间的**皮尔逊相关系数（Pearson‘s correlation）**，然后对所有位置求平均。该指标反映两个子空间及其内部条件排列的几何对齐程度。
        -   也使用了**主角度（principal angles）** 进行补充验证，通过计算两个子空间的前两个主成分（PC）之间的最小主角度来衡量对其程度。

    4.  **信息解码**：
        -   使用**线性判别分析（LDA）** 解码器来量化神经群体对奖励值、目标位置、所选价值、相对价值等信息变量的编码能力。
        -   将解码性能的增加分解为**类间方差（between-class variance）** 和**类内方差（within-class variance）** 的变化。

### 3. 实验设计

-   **实验对象与任务范式**：
    -   **受试者**：两只成年猕猴（Macaca mulatta）。
    -   **任务**：一项新颖的、基于价值的顺序选择任务。在每个试次中，猴子首先看到两个相继呈现的空间目标（T1和T2）。每个目标出现后，会跟随一个抽象的奖励线索（R1和R2），其颜色预示选择该目标后可获得的奖励大小。在经历一段“决策后延迟”后，两个目标重新出现，猴子通过眼跳选择其中一个以获得对应的奖励。任务是选出奖励价值更高的目标。
    -   **关键设计**：该范式将**选项呈现**与**价值赋值**在时间上分离开，从而可以清晰地区分决策前（比较价值前）和决策后（比较价值后）的神经活动。分析主要聚焦于第二个奖励线索（R2）呈现前后的时间段，此时猴子才获得足够信息进行价值比较和决策。

-   **对比分析（Benchmarks & Comparsons）**：
    -   **对比1：同一呈现顺序，不同选择状态**。比较同一个目标（如T1）在它被选中（当R1>R2）和未被选中（当R1<R2）的试次中的表征几何。
    -   **对比2：不同呈现顺序，相同选择状态**。比较不同目标（T1 vs T2）在它们都被选中（来自不同试次）或都未被选中的条件下的表征几何。
    -   **解码泛化（Cross-decoding）**：训练解码器在某一选择状态（如选中T1）下解码目标位置，然后测试其在另一种选择状态（如选中T2）下的表现，以验证共同子空间的存在。

### 4. 资源与算力

-   **算力提及情况**：论文内容主要关注神经科学方法和数据分析，**未明确提及**所使用的具体计算资源，如GPU型号、数量或训练时长。所有分析使用 Python 编写，属于常规的数据处理、统计建模和机器学习方法，通常不需要大规模算力支持。

### 5. 实验数量与充分性

-   **实验规模**：
    -   该研究记录了2只猴子的LPFC神经活动（猴子T：23个时段，316个神经元；猴子I：17个时段，422个神经元），数据量在灵长类电生理研究中属于中等偏上规模。
    -   通过构建伪群体并进行1000次自举法（bootstrap）重采样，确保了统计分析的稳健性。

-   **分析维度与消融实验**：
    -   **多个分析层面**：包括单神经元选择性分析、群体信息解码、表征几何（子空间对齐、主角度）分析。
    -   **控制与分析**：
        -   将解码准确性变化分解为类间和类内方差。
        -   排除了可“早期决策”（即第一个奖励线索为极值）的试次进行主分析，并单独分析了这些早期决策试次中的神经活动作为补充证据。
        -   通过移除疑似额叶眼区（FEF）和运动前区皮层的记录位点进行控制分析，证实了结果的稳健性（见补充材料图S12）。
        -   分析了神经元群体的重叠情况，以证明正交子空间源于**同一批神经元的复杂活动模式**（混合选择性），而非独立的神经元亚群。

-   **实验评估**：
    -   主要结论在两个受试者身上都得到了重复验证，尤其是在行为表现更好的猴子T上效应更明显（猴子I的行为表现出更强的梯度偏好和轻微偏差），表明结果的可靠性。使用了如Bootstrap、多重比较校正（Benjamini/Hochberg法）等统计方法，实验设计严谨、分析客观。

### 6. 论文的主要结论与发现

-   **决策后选项信息的增强**：决策后，LPFC对**选中目标位置**的群体解码准确率显著提升，而未选目标的解码准确率下降或不变。这种提升是由于**类间方差（表征分离度）的增加**，而非噪音的减少。
-   **决策驱动的神经子空间正交化**：决策前，同一目标（如T1）在将来会被选中和不会被选中的试次中，其表征是**平行对齐**的。决策后，这两种表征**旋转为接近正交**，表明所选和未选选项的信息被分隔到独立的子空间，减少了干扰。
-   **决策驱动的神经子空间对齐**：决策前，第一和第二目标在群体空间中占据**接近正交**的子空间，保持相互独立。决策后，无论呈现顺序如何，**被选中的目标**（来自不同试次）的表征**旋转到同一个对齐的子空间中**，形成了一个与动作准备相关的共同编码格式。
-   **选择信息与空间信息并存**：虽然选中目标的子空间按空间位置对齐，但代表“选择了哪个目标”的选择信息并未消失，而是被编码在与目标位置子空间**正交的决策轴**上。这表明了从呈现顺序信息到动作选择信息的复杂几何重组，而非简单转化为纯粹的运动预备信号。
-   **部分价值信息即可引发早期重组**：当第一个奖励线索为极值，猴子可以提前决策时，与决策相关的解码增强和子空间重组也会相应**提前发生**。

### 7. 优点

-   **新颖的任务设计**：通过时序上分离目标呈现和价值线索，巧妙地将工作记忆（决策前）和价值决策（决策后）阶段区分开，这是本研究的核心方法学亮点。
-   **深入的群体几何分析**：没有停留于单神经元或简单的解码分析，而是深入到**表征几何**层面，揭示了**正交化（orthogonalization）** 和**对齐（alignment）** 这两种关键的群体计算机制，为理解LPFC如何组织信息提供了深刻的见解。
-   **机制性解释**：将变化的几何与功能意义直接联系起来——正交化保护信息免于干扰，而对齐则便于下游高效读出——提供了一个逻辑自洽的计算模型。
-   **分析严谨性**：通过Lasso回归克服任务设计的非独立性偏差，区分方差来源，并使用多种度量（相关性、主角度、交叉解码）进行交叉验证，增强了结论的可靠性。

### 8. 不足与局限

-   **潜在的解剖特异性问题**：尽管移除了FEF/PMC位点后结果仍稳健，但LPFC记录区域广阔，不同亚区的功能可能存在差异。目前的分析将整个LPFC作为一个整体，可能掩盖了更精细的空间-功能对应关系。
-   **因果性证据缺失**：该研究是纯观察性的。虽然发现了“价值信号引导几何重组”的时间顺序，但并未通过干预（如微电刺激或光遗传）来证明价值信号和几何变化之间的**直接因果关系**。
-   **行为差异的影响**：两只猴子的行为表现有明显差异（猴子T的选择更二元化，猴子I更梯度化），部分神经结果在猴子I上表现为趋势但未达显著。这虽然反映了行为-神经的个体差异，但也可能提示该机制在不同行为策略下的表现不尽相同，需要更深入探讨。
-   **环路基底的简化**：研究集中于LPFC内的表征几何，但LPFC的输入（来自OFC的价值信号）和输出（至运动区）在整个转换中同样关键。目前的研究只是揭示了LPFC内部发生的“重编码”现象，未涉及更宏观环路层面的相互作用机制。

（完）
