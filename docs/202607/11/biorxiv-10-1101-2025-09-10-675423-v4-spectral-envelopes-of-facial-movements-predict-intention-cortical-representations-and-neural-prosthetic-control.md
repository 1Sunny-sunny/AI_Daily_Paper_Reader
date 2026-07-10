---
title: "Spectral envelopes of facial movements predict intention, cortical representations, and neural prosthetic control"
title_zh: 面部运动的光谱包络预测意图、皮层表征与神经假体控制
authors: "Hakim, R., Jaggi, A., Heo, G., Matsumoto, H., Uchida, N., Watabe-Uchida, M., Datta, S. R., Musall, S., Sabatini, B. L."
date: 2026-07-09
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.10.675423v4.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 面部运动解码用于神经假体控制
tldr: 啮齿动物通过节律性面部运动与环境互动，但精确测量这些运动并关联神经活动存在困难。本研究提出 face-rhythm 无监督流水线，结合无标记点跟踪、谱分析和非负张量分解，将面部视频分解为可解释的组分。在小鼠多任务中，这些组分可跨个体一致地解码任务变量、解释皮层活动，并揭示运动皮层对高频面部运动的相位不变编码。该方法在低维可解释性与解码性能上具有竞争力。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-002.webp\", \"caption\": \"Figure 4. Uninstructed facial behavior predicts brain-machine interface reward events. Uninstructed facial behavior around BMI reward events and decoding analysis. A) Experiment diagram. The mouse performs a brain-machine interface (BMI) task, increasing the activity of a set of neurons selected on a baseline day (‘day 0’) to earn rewards at a threshold (see Methods 5.11). B) Face-camera field-of-view. C) Diagram of a single threshold-crossing reward event. D) Representative example illustrating consistent uninstructed behavioral sequencing around threshold crossings. Rows are FR components from an asymmetric (right-side-only) sliding window (see Methods 5.14.2). Left: temporal-factor rasters aligned to threshold crossings. Left-middle: averaged temporal factors (error bars, s.d. across events). Middle: spectral factors. Right-middle: spatial factors (‘x’ displacement blue, ‘y’ red). Right: interpretation. E)Decoding analysis. Ei) Decoders predict the instantaneous probability of currently achieving reward from either raw tracked points (Points-linear) or FR temporal factors (FR-linear, FR-RNN), assessed by receiver-operatingcharacteristic (ROC) analysis (see Methods 5.6). Eii) Area under the ROC curve (AUC) for Points-linear, FR-linear, FR-RNN, and Points-RNN versus temporal lag of inputs relative to outputs (negative lags predict future events; controls randomly shifted; Points-RNN uses PCA-reduced points). Shaded regions are s.e.m. across mice (N = 4).\", \"page\": 15, \"index\": 2, \"width\": 968, \"height\": 900}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-003.webp\", \"caption\": \"Figure 5 supplement 1. Motion-energy PCA performs similarly to point-tracking in the convolutional reduced-rank regression of M1 activity. Comparison of motion-energy PCA and point-tracking predictors (see Methods 5.7.5). FR point-tracking is raw and uncompressed. In both panels, color encodes the model arm (basic, Hilbert-spectral, hybrid) and line style the predictor (point-tracking, solid; motion energy, dashed); thin lines, individual mice; bands, 95% confidence intervals across mice; thick lines, crossanimal mean; grey traces, temporally shifted null (N = 5 mice). A) Total held-out EVR versus model rank; each predictor’s ridge penalty tuned independently. B) Frequency-resolved EVR versus the center frequency of the behavioral signals’ filtered band (rank fixed at 6).\", \"page\": 21, \"index\": 3, \"width\": 967, \"height\": 1214}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-001.webp\", \"caption\": \"Figure 6 supplement 1. All joint neural-behavioral components for representative mice. Each row is one component from the joint coherence-tensor decomposition (Figure 6Eii) for two representative mice. Columns, left to right: trial factor (magnitude over trials), spectral factor, spatial factor (‘x’ blue, ‘y’ red), neural factor (per-neuron loading), and the decoder correlation (Pearson R between the neural factor and each day-0 factor; blue bar marks the day-0 decoder factor). The component whose trial factor increases most across sessions is orange (same as Figure 6F); others are gray. Shaded regions in the trial column are the interquartile range of a sliding-window smooth.\", \"page\": 25, \"index\": 1, \"width\": 966, \"height\": 1079}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-004.webp\", \"caption\": \"Table 3: Glossary of dimensions.\", \"page\": 58, \"index\": 4, \"width\": 794, \"height\": 196}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-005.webp\", \"caption\": \"Table 5: Glossary of operators.\", \"page\": 59, \"index\": 5, \"width\": 698, \"height\": 372}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-09-10-675423-v4/fig-006.webp\", \"caption\": \"Table 6: Glossary of Einstein summation notation examples.\", \"page\": 59, \"index\": 6, \"width\": 826, \"height\": 198}]"
motivation: 精确测量啮齿动物面部运动并将其与神经活动关联是一项关键挑战。
method: 提出 face-rhythm 流水线，通过无标记点跟踪、谱分析与非负张量成分分析无监督分解面部视频。
result: 所得运动组分可解码任务变量和内部状态，解释皮层活动，并发现 M1 神经元对高频运动使用相位不变编码，对低频运动依赖相位可变表征。
conclusion: face-rhythm 提供了一种低维、可解释且与皮层活动紧密联系的面部行为描述，在多任务中表现有竞争力。
---

## 摘要
包括人类在内的动物利用协调的面部运动来采样环境、摄取营养和交流。啮齿类动物在自发行为和认知任务中尤为典型地产生节律性面部运动。精确测量这些运动并将其与神经活动联系起来仍具挑战。我们引入了face-rhythm，一种无监督流程，结合无标记点跟踪、光谱分析和非负张量成分分析，将面部视频分解为少量可解释的成分。将其应用于小鼠在巴甫洛夫气味奖励任务、脑机接口任务和自由行为中的视频，face-rhythm恢复了人类可解读的行为，如拂须、嗅探、舔舐和更细微的基序。所得成分在动物间一致，足以解码任务变量或内在信念状态，并用低秩表征解释皮层活动。我们还发现，与面部相关初级运动皮层中的神经元活动可由约0.5 Hz以上面部运动的相位不变光谱变换较好预测，而较慢的运动则保留相位变异表征，由面部瞬时位置更好地预测；单个神经元可显示一种或两种调谐形式。与深度学习点跟踪模型、对比学习嵌入和视觉变换器特征的系统比较表明，face-rhythm在各任务中具有竞争力，同时实现了对与皮层活动密切相关的啮齿动物面部行为进行低维、可解释描述的目标。

## Abstract
Animals, including humans, use coordinated facial movements to sample the environment, ingest nutrients, and communicate. Rodents, in particular, produce rhythmic facial movements during spontaneous behavior and cognitive tasks. Measuring these movements precisely and linking them to neural activity remains challenging. We introduce face-rhythm, an unsupervised pipeline that combines markerless point-tracking, spectral analysis, and non-negative tensor component analysis to decompose facial video into a small set of interpretable components. Applied to videos of mice during a Pavlovian odor-reward task, a brain-machine interface (BMI) task, and free behavior, face-rhythm recovers human-interpretable behaviors such as whisking, sniffing, licking, and subtler motifs. The resulting components are consistent across animals, are sufficient to decode task variables or internal belief states, and explain cortical activity using a low-rank representation. We also find that the activity of neurons in face-associated primary motor cortex (M1) is predicted well by a phase-invariant spectral transformation of facial movements above ~0.5 Hz, while slower movements retain a phase-variant representation better predicted by the instantaneous position of the face; individual neurons can show either or both forms of tuning. A systematic comparison against deep-learning point-tracking models, contrastive-learning embeddings, and vision-transformer features places face-rhythm competitively across tasks while also achieving the goal of producing a low-dimensional, interpretable description of rodent facial behavior that is closely linked to cortical activity.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

*   **研究动机**：啮齿动物通过高度协调的、节律性的面部运动（如拂须、嗅探、舔舐等）来探索环境、完成任务。这些行为蕴含着丰富的信息，能够反映动物的感知、决策和内部状态。然而，精确量化这些复杂的面部动态并将其与神经活动关联起来，构成了一个长期的挑战。
*   **核心问题**：如何从面部视频中无监督地提取一组低维、时间连续、可解释的行为原语，使其既能解码任务变量和内在信念状态，又能直接预测皮层神经活动，并且在不同任务中被深度学习基线方法验证为有效。
*   **整体含义**：该研究意味着一种新的计算框架——`face-rhythm`——能够将原始面部视频压缩为与神经活动紧密耦合的“光谱包络”基元，揭示了运动皮层对面部高频运动的**相位不变编码**与对低频运动的**相位可变编码**的分离机制。这不仅为量化行为提供了强大的工具，也为理解运动皮层如何表征节律性输出、并据此开发神经假体控制提供了理论基础。

### 2. 论文提出的方法论

核心思想是结合现代计算机视觉与多线性代数，从面部视频中提取具备生理可解释性的时空频谱成分。

*   **流程图**：`face-rhythm` 包含三个关键步骤：
    1.  **无标记点跟踪**：对小鼠面部视频帧，应用无标记关键点跟踪模型（文中应与深度学习点跟踪模型进行了对比，但其基础流程也包括基于点的运动提取），获取面部关键点的时间序列轨迹。
    2.  **频谱分析**：对每个点的运动轨迹进行时频变换（如短时傅里叶变换或小波变换），提取其在不同频率上的**功率包络**（即光谱包络），将点位置的瞬时变化提升为频率分辨的运动能量表征。这一步使高频节律性运动（>~0.5 Hz）的强度信息变得显式可用。
    3.  **非负张量成分分析**：将所有关键点的多维频谱数据组织成张量（维度：点×频率×时间），应用非负张量分解（类似非负矩阵分解的高阶扩展）将该张量分解为一组非负的**成分**（components）。每个成分由一个时间因子（temporal factor，描述成分强度如何随时间变化）、一个频谱因子（spectral factor，描述成分的能量集中在哪些频段）、一个空间因子（spatial factor，描述面部哪些点主要参与）组成。
*   **关键特性**：分解的非负性保证了解释的直观性（每个成分代表某种行为被“激活”的程度，而非正负抵消的模式）。该流程完全无监督，不依赖行为标注，且得到的成分在动物间具有一致性。

### 3. 实验设计

*   **应用场景/数据集**：研究在三种不同行为范式下采集的小鼠面部视频上验证了方法：
    *   **场景一**：经典的巴甫洛夫气味-奖励任务（Pavlovian odor-reward task）。用于检验成分能否解码任务条件（气味类型、奖励交付）。
    *   **场景二**：脑机接口（BMI）任务。小鼠需通过增加特定神经元集合的活动来获取奖励，面部行为作为非指令性的“读出”被分析，检验其能否预测神经元阈值穿越事件（奖励时刻）和动物自身意图。
    *   **场景三**：自由自发行为（free behavior）。在无外部任务结构时，检查所挖掘的行为基元是否具有通用性。
*   **基准与对比方法**：系统性地将 `face-rhythm` 的表现与多种特征提取策略进行了比较：
    *   **点跟踪基线**：基于深度学习的点跟踪模型（Deep-learning point-tracking）所输出的原始点轨迹。
    *   **运动能量PCA**：传统上常用的基于运动能量（motion-energy）的主成分分析。
    *   **表征学习嵌入**：基于对比学习（contrastive-learning）的嵌入向量。
    *   **视觉变换器特征**：现代视觉变换器（Vision Transformer）提取的高级视觉特征。
    *   **解码器类型**：在解码任务变量时，不同特征（如`Points`原始点、`FR`面部分解的时间因子）均配合线性（Linear）模型或循环神经网络（RNN）进行测试，从而全面评估低维表示的有效性。

### 4. 资源与算力

*   论文摘要与提供的片段中**未明确提及**所使用的 GPU 型号、数量、模型训练时长或总计算开销。这类信息通常见于正文的方法或附录部分，基于当前语料无法确知。

### 5. 实验数量与充分性

*   **实验丰富度**：实验设计立体且层次化，至少包含：
    *   在3个不同性质的任务/场景下进行验证。
    *   与至少4类异质基线方法（经典点跟踪、运动能量、对比学习、视觉变压器）进行性能对比。
    *   关键解码性能评估涉及多个模型（线性模型、RNN），且对多只小鼠（N≥4）进行了跨个体分析。
    *   机制解释性实验：通过频谱分辨的回归模型（frequency-resolved regression）探究了M1区神经元对相位不变/可变编码的依赖，并对单个神经元进行了调谐性质分类。
    *   消融/补充分析：包含对运动能量PCA与点跟踪预测性能的专门比较（Figure 5 supplement 1），以及对联合张量分解成分的详细展示（Figure 6 supplement 1）。
*   **充分性与公平性**：实验覆盖了多种行为范式，对比基线全面且具有当代代表性（对比学习、视觉变压器），评估指标多样（解码AUC、皮层活动解释方差等），且通过随机时间平移等方法建立了零分布（chance level），实验设计公平、严谨。

### 6. 论文的主要结论与发现

*   `face-rhythm` 可以从面部视频中无监督地分解出与拂须、嗅探、舔舐等一致的行为基元，这些成分在个体间具有良好的可重复性。
*   该低维表示足够强大，能够**解码任务变量**（如气味刺激、奖励）和**内在状态**（如BMI任务中即将获得奖励的概率），其性能与原始点轨迹或深度神经网络的复杂嵌入相当甚至更优（AUC更高）。
*   运动皮层（M1）的面部相关神经元活动可以从面部运动的**光谱包络**中被高度预测，且该预测呈现明显的频率依赖性：
    *   对于 **> 约0.5 Hz的高频运动**，神经元主要采用**相位不变**的编码方式，即对运动振幅或功率敏感，而不锁定运动的精确相位。
    *   对于**低频运动**，则主要依赖**相位可变**编码，即对瞬时位置信息敏感。
    *   单个神经元可以同时呈现这两种编码特性。
*   `face-rhythm` 提取的成分能够通过一个低秩结构**解释皮层活动**，为行为到神经的映射提供了一个简洁的线性接口。

### 7. 优点

*   **可解释性**：非负张量分解直接产生对应可命名行为（如 sniffing, whisking）的成分，每个成分具有明确的时空频谱模态，克服了深度学习嵌入的黑箱问题。
*   **神经生理学的紧密联系**：通过聚焦于“频谱包络”，捕获了皮层尤其擅于处理的节律性运动能量信息，直接揭示了M1编码的频率依赖特性，这是单纯基于位置的特征难以完成的。
*   **跨任务、跨个体的稳健性**：方法在三种差异显著的任务中均表现有效，无需针对特定任务重新训练特征提取器，展现出了良好的泛化性。
*   **计算效率与低秩性**：用极少量的成分即可解释大部分与行为和神经活动相关的方差，在数据压缩和预测性能之间达到了极佳的平衡。

### 8. 不足与局限

*   **物种与行为范畴的局限性**：目前仅在小鼠的节律性面部运动中验证。对于具有更复杂、更随意面部肌肉控制的物种（如灵长类），或非节律性的表情，该“频谱包络+张量分解”范式的适用性未知。
*   **因果性缺失**：研究证明面部运动谱特征与神经活动高度相关并能解码意图，但未通过扰动实验（如光遗传抑制M1或肌肉）因果验证这种编码关系与行为执行的必要性。
*   **离线分析为主**：虽然论文提到了“神经假体控制”的前景，但描述主要基于离线解码分析。实时闭环控制系统的性能、延迟、稳定性等关键问题尚未涉及。
*   **技术依赖性**：`face-rhythm` 依赖高质量的无标记点跟踪作为前处理，其性能会受到面部视频分辨率、光照、遮挡等底层计算机视觉问题的影响。

（完）
