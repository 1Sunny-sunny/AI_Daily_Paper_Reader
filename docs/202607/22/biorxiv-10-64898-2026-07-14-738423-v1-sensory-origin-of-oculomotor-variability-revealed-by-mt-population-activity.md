---
title: Sensory origin of oculomotor variability revealed by MT population activity
title_zh: MT 群体活动揭示动眼变异的感觉来源
authors: "Yip, H. M. K., Cloherty, S. L., Hagan, M. A., Price, N. S. C."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738423v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 使用PLS从MT群体活动解码眼动变异性
tldr: 运动输出的变异性即使源于相同感觉输入，其感觉运动通路起源仍不明确。本研究通过记录狨猴MT区神经元群体活动，采用偏最小二乘回归分析神经活动与眼动的关系，发现刺激诱发的群体活动能可靠预测眼动速度的逐试次波动，且闭环中眼动与后续神经反应存在对应关系。结果支持感觉噪声沿通路传播的假说，但传统模型仅凭神经变异性无法充分预测行为变异，揭示运动系统可能只选择性利用部分感觉表征。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-005.webp\", \"caption\": \"Figure 1. Open loop model to reconstruct eye speed and direction from middle temporal (MT) population activity before eye movement onset. (A) Experimental paradigm. Each trial began with the presentation of a stationary large field stimulus (diameter = 28°) and a peripheral fixation target located 5° from the center of the screen. Monkeys were required to fixate the peripheral target for 150-250 ms. Upon successful fixation, the target disappeared and reappeared centrally, prompting a\", \"page\": 4, \"index\": 5, \"width\": 888, \"height\": 1208}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-004.webp\", \"caption\": \"Figure 2 Closed-loop models examining the relationship between early eye movement and later neural activities. (A) Scatter plots illustrating the relationship between observed and PLS reconstructed eye speed (upper panel) and direction (lower panel) at 80 ms, based on neural activity recorded at 120 ms in an example session. Each small dot represents an individual trial, with colors indicating different stimulus directions. Larger dots denote the mean values for each condition. The inset displays the distribution of correlation coefficients obtained from shuffled models, with the red dotted line indicating the experimental values. (B) Scatter plots of predicted and observed eye speed and direction after centering values within each stimulus condition to remove stimulus direction dependent effects. (C) Distribution of correlations in speed and direction in all recording sessions in two animals. Each dot represents one session (nB = 22; nM = 18). Green dots indicate significant correlation in that session. The red bar shows the median across sessions. (D) Similar to (C), but with z-scored speed and centered directions.\", \"page\": 8, \"index\": 4, \"width\": 884, \"height\": 754}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-002.webp\", \"caption\": \"Figure 3. Temporal evolution of model performance of reconstructing eye movement with neural activities at different time points. (A) PLS models were performed with eye movement at 80 ms (dashed line) and neural activities at different time points ranging from 0 to 160 ms with 5 ms time step. Model performance of z-scored speed was plotted against the neural time window used. Light and dark blue regions indicate the exemplar open-loop and closed-loop period for neural activities. The light grey line and grey shaded area shows the mean and 5% - 95% percentile of shuffled data respectively. Significant correlations are indicated with green dots at top. (B) Across session results for both animals. Thin grey lines are the results from individual sessions, and the thick black line is the average across sessions. Graded green dots at the top indicate the percentage of significant sessions at each time point. Absence of dot means no significant results found in all sessions. (C,D) Similar to (A,B) but for centered direction.\", \"page\": 10, \"index\": 2, \"width\": 888, \"height\": 767}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-006.webp\", \"caption\": \"Figure 4 PLS models conducted with a broad range of time points for eye movement and neural activities. (A, B) Heatmaps depicting the correlation between reconstructed and observed z-scored eye speed and centered direction across a range of eye and neural times for an example session from Monkey B (A) and Monkey M (B). Each pixel represents the correlation value for a model using neural activity from a given time point (y-axis) to reconstruct eye movement at another time point (x-axis). The light and dark blue regions highlight the open-loop and closed-loop periods examined in Figure 3. In each panel, grayscale maps on the right show significance, with white regions indicating statistically significant correlations (p < 0.05) and grey regions indicating non-significant correlations. (C, D) Mean heat map for z-scored speed and centered direction across sessions (nB = 22; nM = 18). The maps on the right show the percentage of significant sessions.\", \"page\": 12, \"index\": 6, \"width\": 888, \"height\": 881}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-003.webp\", \"caption\": \"Figure 5. PLS outperformed PCR. (A,B) Model performance of PLS (green) and PCR (red) in z-scored speed across different numbers of latent components. The solid line shows the mean correlation value across all sessions, while the shaded area represents the standard error estimates. (C,D) Similar to A and B, but for centered direction. (E, F) Cumulative percentage of variance explained by PLS and PCR components.\", \"page\": 14, \"index\": 3, \"width\": 750, \"height\": 729}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738423-v1/fig-001.webp\", \"caption\": \"Figure 6. Vector averaging failed to reconstruct eye movements (A) Scatter plots illustrating the relationship between observed and PLS reconstructed eye speed (upper panel) and direction (lower panel) at 80 ms, based on neural activity recorded at 40 ms in an example session of Monkey B. Each small dot represents an individual trial (B) Scatter plot with data from an example session of Monkey M (C) Distribution of correlations in speed and direction in all recording sessions of Monkey B. Each dot represents one session. Green dots indicate significant correlation in that session. The red bar shows the median across sessions. (D) Distribution of correlations across sessions for Monkey M\", \"page\": 15, \"index\": 1, \"width\": 886, \"height\": 479}]"
motivation: 探索感觉运动通路中运动变异性的起源，特别是检验感觉表征的变异性是否能解释行为波动。
method: 使用Neuropixels探针记录狨猴MT区在眼球跟随任务中的群体活动，通过偏最小二乘回归提取神经与眼动的共享方差，并进行开环与闭环分析。
result: 刺激诱发的MT活动可预测眼动速度的逐试次变异，且眼动与后续神经反应存在试次对应，但仅捕获神经变异性的传统模型预测行为的能力差。
conclusion: 感觉神经群体的变异性确实贡献于运动变异性，但运动系统可能只访问了部分感觉表征。
---

## 摘要
即使面对相同的感觉输入，运动输出仍会变化，但感觉运动通路中这种变异的起源尚未解决。本研究评估了感觉表征的变异性如何解释反射性动眼任务中的行为波动。我们使用 Neuropixels 探针记录了狨猴 MT 脑区在眼动跟随反应期间的神经元活动，并应用偏最小二乘回归提取群体活动与眼动之间的共享变异。刺激诱发的活动可靠地预测了开环眼速的逐试次变异性。此外，闭环分析揭示了眼动与后续神经反应在逐试次上的对应关系。这些结果表明，感觉神经元群体的变异性对运动变异性有贡献，支持了感觉噪声沿感觉运动通路传播的观点。然而令人惊讶的是，传统模型仅捕捉试次间的神经变异，却难以预测行为变化，这表明只有一部分感觉表征能被运动系统所利用。

## Abstract
Motor outputs vary even in response to identical sensory inputs, yet the origin of this variability within the sensorimotor pathway remains unresolved. Here, we evaluate how variability in sensory representations can explain behavioural fluctuations in a reflexive oculomotor task. We used Neuropixels probes to record neuronal activity in area MT of marmosets during ocular following responses and applied partial least squares regression to extract the shared variance between population activity and eye movements. Stimulus-evoked activity reliably predicted trial-by-trial variability in open-loop eye velocity. Additionally, closed-loop analyses revealed trial-by-trial correspondence between eye movements and subsequent neural responses. These results demonstrate that variability in sensory neural populations contributes to motor variability, supporting the claim that sensory noise is propagated through the sensorimotor pathway. Surprisingly, however, traditional models trained to only capture neural variability across trials poorly predicted behavioural variations, suggesting that only a subset of sensory representations is accessible to the motor system.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容生成的结构化、深入、客观的中文总结。

### 1. 论文的核心问题与整体含义

*   **核心问题**：本论文旨在探究一个感觉神经科学中的根本问题：即使在相同的感官输入下，运动输出（如眼动）的逐次试变异（trial-by-trial variability）是否起源于感觉系统中神经活动的内源性噪声。
*   **研究背景与分歧**：运动行为的变异性来源存在两种主要假说。
    1.  **下游主导假说**：认为神经噪声主要在感觉运动的后期阶段（如运动区）产生影响，早期感觉区的噪声会在层级处理中逐步被平均和消除。
    2.  **感觉起源假说**：认为感觉编码层面的神经变异性会沿着感觉运动层级忠实传播，是行为变异性的主要来源，下游区域噪声的影响相对较小。
*   **整体含义**：该研究通过直接记录感觉皮层（MT区）的大规模神经元群体活动，结合先进的数据降维方法，为“感觉起源假说”提供了直接证据。研究揭示，即使在不涉及复杂认知决策的反射性行为中，感觉皮层的神经变异性也能显著预测行为的逐次试变异性。然而，这种与行为相关的神经信号并非神经元群体的主要活动模式，暗示运动系统可能只选择性地读取了一部分感觉信息，这对传统的神经解码模型构成了挑战。

### 2. 论文提出的方法论

*   **核心思想**：采用有监督的降维回归方法——**偏最小二乘回归（Partial Least Squares regression, PLS）**，来寻找群体神经活动与眼动行为之间的共享变异。与传统的无监督降维方法（如主成分回归，Principal Component Regression, PCR）不同，PLS的目标是最大化预测变量（神经活动）和响应变量（眼动速度）之间的协方差，从而提取出最具行为相关性的神经活动成分。
*   **关键技术细节**：
    *   **数据预处理**：将神经元脉冲序列与标准差为5毫秒的高斯核卷积，以获得发射率估计，并离散化为5毫秒的时间片（bin）。眼动速度也做同样的离散化处理。
    *   **偏最小二乘回归（PLS）**：对于给定的神经活动矩阵 \( X \)（试次 × 神经元）和眼动速度矩阵 \( Y \)（试次 × 眼动测量），PLS模型框架为：
        $$ X = T P^T + E $$
        $$ Y = U Q^T + F $$
        其中 \( T \) 和 \( U \) 分别是 \( X \) 和 \( Y \) 的得分矩阵，\( P \) 和 \( Q \) 是载荷矩阵，\( E \) 和 \( F \) 是残差矩阵。PLS通过寻找一个低维的潜在空间 \( T \)，使其在解释 \( X \) 变异的同时也最能预测 \( U \) 的变异，从而提取同时作用于神经与行为的共同成分。
    *   **模型验证与评估**：
        1.  使用**10折交叉验证**确定最佳成分数量。
        2.  通过**打乱试次标签**的随机化检验（shuffle test）来评估模型的统计显著性。
        3.  为了分离出独立于刺激方向的逐次试变异性，对眼动速度和方向数据进行了**z-分数化**和**中心化**处理（即，在每个刺激条件内减去条件均值）。
    *   **对比方法**：
        1.  **主成分回归（PCR）**：先对神经活动进行主成分分析（PCA），再用主要主成分的得分进行回归。
        2.  **向量平均（Vector Averaging）**：一种假设驱动的解码方法，根据每个神经元的偏好方向对其反应进行加权求和。

### 3. 实验设计

*   **数据集与场景**：
    *   **实验对象**：两只成年普通狨猴（callithrix jacchus）。
    *   **行为任务**：**眼动跟随反应（ocular following responses）**，这是一种由大范围视觉运动诱发的反射性、短潜伏期眼动，旨在最小化自上而下的认知影响。
    *   **视觉刺激**：一种“运动云”，在所有试次中各参数（如速度、空间频率）固定，运动方向从8个等间距方向中选取。
    *   **神经记录**：使用Neuropixels探针在MT脑区进行高密度记录，同时采集单神经元和multi-unit的活动，平均每次会话记录350-504个单元。
*   **Benchmark（基准）**：主要的比较基准是与PLS同源的PCA方法（即PCR）和经典的向量平均解码方法。
*   **对比方法分析**：
    1.  **主成分回归（PCR）**：PCR仅关注解释神经活动自身的主要变异，其解码行为的能力显著弱于PLS，说明神经群体中方差最大的主成分并非与行为最相关的维度。
    2.  **向量平均**：该方法在消除刺激方向影响后（即评估逐次试变异性时），完全无法预测眼动，说明简单的加权组合不能捕捉复杂的群体信息与行为变异的对应关系。

### 4. 资源与算力

*   **文中提及**：论文未提到具体的GPU型号、数量或模型训练时长。计算主要涉及MATLAB中的统计分析（PLS、PCR等）、Neuropixels数据的spike sorting（Kilosort 4，通常在GPU上运行）以及行为数据的处理。其计算需求更多集中于数据统计和算法实现，而非大规模的深度学习训练。

### 5. 实验数量与充分性

*   **实验规模**：共进行了**40次有效记录会话（sessions）**（猴B：22次，猴M：18次），行为试次（trials）总数在几百至数千级别。该样本量在灵长类电生理研究中是相对较大的。
*   **分析层次与充分性**：实验设计周密且充分，涵盖了多个层面：
    1.  **时间窗口分析**：通过详尽的时移扫描，系统性地验证了开环（神经活动先于眼动）和闭环（眼动先于神经活动）预测的合理性。
    2.  **控制变量**：通过移除刺激方向的影响，分离并聚焦于逐次试变异性这一核心问题。
    3.  **方法学对比**：与PCR和向量平均两种以上方法进行了客观、公平的比较，突出了PLS在捕获行为相关信号方面的独特优势。
    4.  **神经集群特性研究**：进一步分析了记录到的群体特性（单元数、调谐强度、偏好方向方差）对模型性能的影响，增加了结论的稳健性。

### 6. 论文的主要结论与发现

1.  **开环预测**：眼动运动起始前（约40ms）的MT群体神经活动，可以显著预测之后（约80ms）单次试次的开环眼动速度，平均相关系数 \( r=0.16-0.19 \)，证明了感觉变异性可向下游传播并影响行为。
2.  **闭环关系**：早期眼动速度（80ms）也能反过来预测后续的MT群体神经活动（120ms），平均相关系数 \( r=0.2-0.29 \)，证实了眼动行为对视觉皮层活动的反馈影响存在于单次试次的水平。
3.  **方法学对比的启示**：
    *   **PLS 优于 PCR**：用于预测行为时，PLS用更少的成分实现了比PCR更高的预测精度。这表明解释行为变异的神经变异子空间并非神经活动中方差最大的子空间。
    *   **向量平均模型失败**：该模型无法解释刺激方向恒定时眼动速度的逐次试变异，说明简单的群体解码无法捕捉行为相关的神经波动。
4.  **核心推论**：感觉神经系统（MT区）的固有噪声确实是导致运动变异性的来源之一。但只有部分特定的感觉表征（而非所有感觉活动或最主要的感觉活动模式）被运动系统读取并转化为行为输出。

### 7. 优点

*   **方法学严谨先进**：使用PLS作为核心分析工具，相比于PCR等传统方法，更能有针对性地揭示神经-行为间的共享信息，是本研究的一个关键创新点。
*   **任务与记录范式出色**：采用反射性眼动任务，有效排除了注意力、决策等高级认知因素的干扰，使神经变异性与行为间的因果关系更为清晰。同时使用Neuropixels进行大规模群体记录，克服了以往单电极记录无法观察群体编码特性的局限。
*   **分析全面系统**：通过对比开环、闭环模型，细致的时间窗口扫描，以及消除刺激条件均值的影响，从多个维度验证并强化了核心结论。

### 8. 不足与局限

*   **神经元分类粗糙**：分析中混用了单神经元和multi-unit活动，虽有助于保留群体信息，但可能影响对单一神经元贡献的解释精度，并且spike sorting的过度分裂问题可能造成神经元数量高估。
*   **未完全控制的混淆变量**：研究提到，刺激运动开始前（如之前扫视导致的）视网膜滑移变异可能影响神经基线状态，该因素未被完全控制，是潜在的影响因素。
*   **任务类型限制**：结论基于反射性眼动这一特定任务。其在需要意向性行为的场景中能否推广，仍有待验证。
*   **解释程度的局限性**：虽然PLS模型预测显著，但其相关系数（均值约0.2）表明，MT感觉变异性只能解释总体运动变异性的一小部分，大部分变异的来源仍未得到解释。

（完）
