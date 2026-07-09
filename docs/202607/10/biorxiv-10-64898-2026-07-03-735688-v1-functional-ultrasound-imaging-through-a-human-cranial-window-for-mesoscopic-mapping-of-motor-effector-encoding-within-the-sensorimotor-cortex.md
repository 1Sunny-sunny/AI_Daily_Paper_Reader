---
title: Functional ultrasound imaging through a human cranial window for mesoscopic mapping of motor effector encoding within the sensorimotor cortex
title_zh: 通过人体颅窗进行功能性超声成像用于感觉运动皮层内运动效应器编码的中尺度映射
authors: "Lin, L. J., Callier, T., Heiles, B., Pejsa, K., Liu, C. Y., Shapiro, M. G., Andersen, R. A."
date: 2026-07-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.03.735688v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 功能性超声用于脑机接口运动解码
tldr: 功能超声成像通过声透明颅窗，以亚毫米分辨率无创记录人脑感觉运动皮层的神经活动，实现对多身体部位和单指运动的精细躯体定位映射。在单试次水平解码运动，并发现不同布罗德曼区对单指信息编码不同，且模式可跨会话迁移。这填补了侵入式电生理与非侵入式血流成像之间的空白，为脑机接口提供了高分辨率微创神经记录新方法。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-004.webp\", \"caption\": \"Fig. 1: fUSI general overview and decoding pipeline. A) Simulated image of fUSI transducer recording brain activity (highlighted regions of brain) through an acoustically transparent cranial implant. fUSI is a small and portable neuroimaging modality that can image epidurally or from above the skin when paired with an acoustically transparent cranial implant, providing a deep, large field of view (3.5 cm W x 4.9 cm H) compared to electrophysiology. B) fUSI images can be preprocessed using spatiotemporal filtering to generate maps of task-correlated activity and decode behavior using neural signal. The displayed fUSI plane includes regions of M1, S1, and SMG and was used for all later analyses. C) Average fUSI signal over time, represented by percent change in cerebral blood volume (CBV), within the highlighted ROI. Grey, shaded boxes indicate movement execution periods.\", \"page\": 3, \"index\": 4, \"width\": 976, \"height\": 377}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-007.webp\", \"caption\": \"Fig. 2: fUSI can detect single-trial event-related neurovascular activity. A-C) Multi-body-part movement. D-F) Single digit movement. A,D) Statistical parametric map of overall task activity and their corresponding Cohen d effect sizes (bonferroni correction, p<0.01). B,F) Statistical maps across different time points during execution for an arbitrarily selected effector – lip and middle finger, respectively. Significant event-related activity began at approximately 3.2 s after cue and peaked between 6- 9 s for both multi-body-part and single digit movement (bonferroni correction, p<0.01). C,E) Average fUSI signal within the highlighted ROI (blue = multi-body-part, red = single digit) over time. Grey, shaded boxes indicate movement execution periods.\", \"page\": 5, \"index\": 7, \"width\": 991, \"height\": 504}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-003.webp\", \"caption\": \"Fig. 3: fUSI can robustly detect multi-body-part somatotopy in the sensorimotor cortex. A) Multi-body-part movement task design. B) Example single-session combined map of statistically significant ROIs generated from general linear modelling (GLM) for each effector – contralateral wrist, contralateral finger, lip, and tongue - and the individual ROIs per effector and their corresponding beta weights (p<1e-3 w FDR correction, white solid lines show the cortical surface and sulci, PS = Postcentral Sulcus, CS = Central Sulcus). C) Percent change in CBV per ROI for each effector represented as mean ± SEM, averaged across sessions. D) Centroids of activation per ROI averaged across sessions. Centroids were calculated based on the regions of activation per condition within the S1 subregion and are indicated by a colored dot corresponding to each effector per session. Average centroid position was displayed as ellipses with the mean as the center of the ellipse and ± SEM as the x and y dimensions of the ellipse. The white dotted lines between averaged centroids represent the connections between adjacent effectors based on the somatotopic model, with calculated Euclidian distances between centroids being displayed by their corresponding lines. E) Session averaged overlap among each ROI compared to the other ROIs using the Dice-Sørensen index. For each graph, one ROI, indicated by color, was used as a reference to calculate the Dice-Sørensen index compared to all the other conditions’ ROIs, shown as mean ± SEM. This represents how similar the activity distribution for a condition is to all the other conditions. Dice-Sørensen indices from individual sessions were reported as single dots on the bar graph.\", \"page\": 7, \"index\": 3, \"width\": 981, \"height\": 597}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-006.webp\", \"caption\": \"Fig. 4: fUSI can identify single digit activity during individual finger movement in the sensorimotor cortex. A) Single digit movement task design. B) Example single-session combined map of statistically significant ROIs generated from GLMs for individual fingers and the ROIs per finger and their corresponding beta weights (p<1e-3 w FDR correction, white solid lines show the cortical surface and sulci, PS = Postcentral Sulcus, CS = Central Sulcus). C) Average percent change in CBV per ROI for each finger represented as mean ± SEM, averaged across sessions. D) Centroids of activation per ROI averaged across sessions. Centroids were calculated based on the regions of activation per condition within the BA 1 subregion and are indicated by a colored dot corresponding to each effector per session. Average centroid position was displayed as ellipses with the mean as the center of the ellipsoid and ± SEM as the x and y dimensions of the ellipse. The white dotted lines between averaged centroids represent the connections between adjacent effectors based on the somatotopic model, with calculated Euclidian distances between centroids being displayed by their corresponding lines. E) Session averaged overlap among each ROI compared to the other ROIs using the Dice-Sørensen index. For each graph, one ROI, indicated by color, was used as a reference to calculate the Dice-Sørensen index compared to all the other conditions’ ROIs, shown as mean ± SEM. This represents how similar the activity distribution for a condition is to all the other conditions. Dice-Sørensen indices from individual sessions were reported as single dots on the bar graph.\", \"page\": 9, \"index\": 6, \"width\": 979, \"height\": 608}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-001.webp\", \"caption\": \"Fig. 5: Multi-body-part and single digit movement effector information can be decoded from fUSI recordings of the sensorimotor cortex. A-C) Multi-body-part movement. D-F) Single digit movement. A,D) Movement effector decoding accuracy over time and the corresponding confusion matrix for the timepoint with the best decoding accuracy. Peak decoding reaches >90% accuracy for multi-body-part movements and >75% accuracy for single digit movements. The shaded region shows the execution period. The color of the decoding accuracy line shows statistical significance (1-sided binomial test). Confidence intervals were calculated using bootstrapping over 1000 permutations. B,E) Searchlight analysis of local regions containing sufficient information for decoding movement effector information (searchlight radius = 600 µm, FDR correction, p<0.05). The fUSI plane was then segmented into separate brain regions - SMG (peach), S1 (light orange), M1 (dark orange) - to examine the contributions of individual brain regions to decoding. C,F) Decoding accuracy over time and the corresponding confusion matrix for the timepoint with the best decoding accuracy using significant task-correlated voxels only within SMG, S1, and M1. The shaded region shows the execution period. The color of the decoding accuracy line shows statistical significance (1-sided binomial test).\", \"page\": 11, \"index\": 1, \"width\": 976, \"height\": 559}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-005.webp\", \"caption\": \"Fig. 6: Motor effector representation varies across cytoarchitectonic regions. A) Segmentation of fUSI plane into BA 2 (dark blue), 1 (light blue), 3b (green), and 3a (yellow) based on probabilistic maps and anatomical definitions. Decoding and RSA was performed using the fUSI signal within the entirety of each segment. B) Average decoding accuracy over time. Only BA 1 produced significant decoding performance above chance. The shaded region shows the execution period. The plotted line shows mean ± SEM, n = 3 sessions. Color of the decoding accuracy line shows statistical significance (1-sided binomial test). C) The corresponding confusion matrix for the timepoint with the best decoding accuracy for each BA. D) RDMs generated for each BA to compare representational differences across cytoarchitectonic regions. RDMs were generated by calculating the Crossnobis distances from trial-averaged signal per voxel at peak activation for each effector and each run. Shaded boxes marked with the symbol “ns” represent nonsignificant Crossnobis values.\", \"page\": 13, \"index\": 5, \"width\": 987, \"height\": 489}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-735688-v1/fig-002.webp\", \"caption\": \"Fig. 7: fUSI can provide stable mappings of similar neuronal populations across sessions.\", \"page\": 15, \"index\": 2, \"width\": 974, \"height\": 942}]"
motivation: 缺乏微创、高分辨率且足够灵敏的人脑运动编码神经记录方法。
method: 在一位具有声透明颅骨植入物的受试者中，利用功能超声成像记录多身体部位和单指运动任务下的皮层活动。
result: 成功描绘出符合经典躯体定位的精细映射，实现单试次解码，并发现布罗德曼区对运动信息编码差异及跨会话解码能力。
conclusion: 功能超声成像能可靠地以亚毫米分辨率解析人体感觉运动皮层的运动表征，有效连接侵入式与非侵入式成像技术。
---

## 摘要
理解人类皮层回路中的运动编码对于推进脑机接口（BCI）至关重要。然而，现有的微创、高分辨率神经记录方法很少能敏感地检测到单次试验的运动相关神经活动。功能性超声成像（fUSI）可提供深层皮层组织的亚毫米空间分辨率，具有高灵敏度，当与透声颅骨植入物结合时，能够经皮记录人神经血管变化。先前的研究已在具有透声颅骨植入物的受试者中使用fUSI进行开关任务映射和解码。在此，我们展示了fUSI能够在具有透声颅骨植入物的受试者中可靠地解析初级感觉运动皮层内的多身体部位和单指运动编码。我们获得了与经典躯体拓扑结构一致的个体效应器表征的精细映射，适用于多身体部位和单指运动。我们能够解析单次试验的事件相关活动，实现了对两种条件的单次试验解码。对解码重要体素的分析表明，单指运动信息在不同布罗德曼分区中的编码存在差异。最后，我们表明这些模式可以在不同会话中近似，允许跨会话解码。这些结果证实，fUSI能够以亚毫米分辨率可靠地描绘躯体拓扑组织的运动表征，填补了人体中侵入性电生理学与非侵入性血流动力学成像之间的关键空白。

## Abstract
Understanding movement encoding within human cortical circuits has been essential for advancing brain computer interfaces (BCIs). However, there are limited minimally invasive, high resolution neurorecording methods sensitive enough to detect single-trial movement-correlated neural activity. Functional ultrasound imaging (fUSI) provides submillimeter spatial resolution of deep cortical tissue with high sensitivity and, when paired with acoustically transparent skull implants, enables transcutaneous recording of human neurovascular changes. Prior studies have used fUSI in participants with acoustically transparent skull implants for on-off task mapping and decoding. Here, we demonstrate fUSI's ability to reliably resolve multi-body-part and single digit movement encoding within the primary sensorimotor cortex in a participant with an acoustically transparent skull implant. We obtained fine-grained mappings of individual effector representation that were consistent with classic somatotopy for both multi-body-part and single digit movement. We were able to resolve single-trial event-related activity, enabling single-trial decoding of both conditions. Analysis of voxels important for decoding suggested differential encoding of single digit movement information across the different Brodmann areas. Finally, we show that these patterns can be approximated across different sessions, allowing for cross session decoding. These results establish that fUSI can reliably delineate somatotopically organized motor representations at submillimeter resolution, bridging a critical gap between invasive electrophysiology and noninvasive hemodynamic imaging in a human subject.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的结构化、深入、客观的总结。

### 1. 论文的核心问题与整体含义

*   **研究动机**：开发脑机接口（BCI）需要高分辨率、微创且能检测单次试验神经活动的神经记录方法。现有方法存在局限：
    *   **侵入式电生理法**（如犹他阵列、ECoG）虽然时空分辨率高，但手术创伤大，记录范围有限，且信号长期稳定性差。
    *   **非侵入式成像法**（如fMRI、EEG）虽然无创、视野大，但时空分辨率不足（fMRI空间分辨率通常为3-4毫米，EEG更低），且fMRI无法在自然行为中进行扫描。
*   **核心问题**：本研究旨在验证功能性超声成像（fUSI）作为一种新型神经成像技术，能否在人体上通过透声颅窗，以亚毫米级空间分辨率精细地映射和解码感觉运动皮层中的运动效应器（身体部位和单指）编码。
*   **整体含义**：fUSI试图在侵入性与非侵入性技术之间架起一座桥梁，提供一种兼具高灵敏度、高空间分辨率、大视野和微创（硬膜外或经皮）特性的“中尺度”神经记录方案，为未来的BCI和神经科学研究提供新工具。

### 2. 论文提出的方法论

*   **核心思想**：利用功能性超声成像（fUSI）技术，通过检测与神经活动相关的局部脑血容量（CBV）的瞬时变化，来间接反映大脑皮层的神经活动。
*   **关键技术细节**：
    *   **成像原理**：使用一个128阵元、中心频率7.5MHz的线性阵列超声换能器，放置在受试者头皮表面的透声颅骨植入物上，发射平面波并接收回波，生成高帧率的复合平面波图像（400 Hz帧率）。
    *   **信号处理**：每300帧复合图像通过奇异值分解（SVD）滤波器分离组织信号与血液信号，最终生成每1.65秒一帧（0.6 Hz采样率）的能量多普勒图像，该图像反映了CBV的变化。
    *   **任务范式**：采用模块化设计，受试者按指令重复执行特定身体部位或手指的运动（执行期）与静息（注视期）交替进行。
    *   **数据分析流程**：
        1.  **预处理**：对原始fUSI数据进行低通滤波（0.1 Hz截止）、空间高斯平滑（仅用于解码）、体素级去趋势和基线归一化。
        2.  **统计映射**：
            *   **统计参数图**：使用体素级学生t检验，比较执行期与注视期的活动，以定位任务相关体素。
            *   **通用线性模型（GLM）**：通过将任务条件（经血液动力学响应函数卷积）与fUSI信号进行拟合，生成每个效应器的统计激活图（T对比），用于精细描绘运动表征的躯体拓扑分布。
        3.  **解码分析**：
            *   **特征降维与分类**：使用主成分分析（PCA，保留95%方差）降低数据维度，然后应用线性判别分析（LDA）在单次试验水平上对不同效应器进行分类。采用10折交叉验证评估解码性能。
            *   **搜索光分析**：通过在图像上移动一个半径为600微米的圆形兴趣区（ROI），评估局部区域信息是否足以完成解码任务。
        4.  **表征相似性分析（RSA）**：计算不同效应器表征之间的Crossnobis距离（一种噪声归一化的交叉验证距离度量），以构建表征不相似矩阵（RDM），量化不同皮层区域（如布罗德曼分区）内的信息编码差异。
        5.  **跨会话对齐**：采用基于图像强度的刚性配准和复杂小波结构相似性指数（CW-SSIM）来评估和比较不同记录会话间成像平面的位置相似性。

### 3. 实验设计

*   **数据集/场景**：
    *   **受试者**：一名因创伤性脑损伤后接受去骨瓣减压术和颅骨成形术，植入了定制聚甲基丙烯酸甲酯（PMMA）透声颅骨植入物的人类受试者（左半球）。这是一个单一受试者的案例研究。
    *   **任务**：受试者执行两项提示运动任务。
        1.  **多身体部位运动**：移动对侧手腕、对侧手指、嘴唇和舌头。
        2.  **单指运动**：移动对侧手的拇指、食指、中指、无名指和小指。
*   **基准（Benchmark）与对比方法**：
    *   本研究并非一个多方法性能对比研究，其本身是对fUSI技术能力的验证。
    *   **内部比较**：主要比较了不同运动条件（身体部位/手指）和不同皮层区域（M1, S1, SMG, 不同BA分区）的解码准确率和表征模式。
    *   **技术对比**：在讨论部分，将fUSI的解码性能与文献中报道的其他微创技术（如fMRI）的性能进行了比较（例如，fMRI解码单指运动的准确率约为63%）。

### 4. 资源与算力

*   论文中**未明确说明**进行数据处理和分析时使用的GPU型号、数量或具体训练时长。文中仅提及数据分析和可视化在MATLAB 2023a环境中，使用标准台式计算机进行。

### 5. 实验数量与充分性

*   **实验组数**：
    *   **任务类型**：2种（多身体部位运动、单指运动）。
    *   **多身体部位运动分析会话**：至少3次会话（B1, B2, B3）用于组水平分析，另有会话用于跨会话解码（B4等）。
    *   **单指运动分析会话**：至少3次会话（F1, F2, F3）用于组水平分析，另有会话用于跨会话解码（F4, F5等）。
    *   **具体分析模块**：进行了统计映射、GLM建模、单试次解码、解码权重图、搜索光分析、RSA分析、跨会话解码及平面相似性对解码影响的分析等一系列实验。
*   **充分性与公平性**：
    *   **充分性**：实验设计全面，从多部位粗粒度映射到单指精细映射，从会话内解码到跨会话解码，逐层深入，验证了fUSI的多项潜力，实验流程逻辑严密。
    *   **局限性**：该研究为**单一受试者的案例研究（n=1）**。这是最关键的局限，结果的普适性有待在更大样本中验证。此外，任务采用模块化设计，可能引入了预期效应，与自然运动场景有差异。

### 6. 论文的主要结论与发现

*   **精细的躯体拓扑映射**：fUSI能够可靠地描绘出感觉运动皮层中多身体部位和单指运动的经典躯体拓扑分布，其质心呈背内侧至腹外侧排列。
*   **单试次解码能力**：凭借高灵敏度，fUSI信号可以在单试次水平上解码不同的运动效应器。多身体部位解码准确率>95%，单指解码准确率>75%。
*   **不同脑区的差异化编码**：
    *   **多部位运动**：S1解码准确率最高（97%），M1较低（76%），缘上回（SMG）也表现出良好的解码性能（87%）。
    *   **单指运动**：S1解码表现最佳（64%），且BA 1区包含最显著的可解码信息和最大的指间表征差异，而BA 3b， 3a， 2区的解码表现不显著，提示单指精细信息可能主要在BA 1进行高阶整合。
*   **跨会话的稳定性**：尽管单次会话的精细表征图存在差异，但运动表征的总体模式在不同记录日期保持稳定，使得跨会话解码成为可能。解码准确率与成像平面的相似性（CW-SSIM）在多部位运动中有正相关，但在单指运动中不显著。

### 7. 优点

*   **技术突破性**：首次在人体上通过透声颅窗，利用fUSI同时实现对多部位和单指运动的精细映射和单试次解码，展示了其作为微创BCI的巨大潜力。
*   **高分辨率与灵敏度**：在300微米空间分辨率下成功区分高度重叠的单指表征，性能优于传统无创成像技术（如fMRI）。
*   **分析深度**：结合了GLM、PCA-LDA解码、搜索光分析和RSA等多种分析手段，不仅在宏观脑区层面，还在细胞构筑（BA分区）层面深入探究了运动编码的机制。
*   **临床转化潜力**：证明了利用临床必需的颅骨植入物作为“声窗”进行高级神经科学研究的可行性，为开发新型、便携、微创的BCI或长期神经监测方案提供了概念验证。

### 8. 不足与局限

*   **样本量极小（仅1人）**：这是最核心的局限。所有结论均来自单个受试者，无法评估个体差异，结果的普适性存疑。
*   **2D成像的局限**：使用线性阵列探头，仅能采集单个二维平面的信息，无法获得大脑三维活动的全貌，可能遗漏平面外的关键信息。
*   **透声植入物带来的信号衰减**：由于PMMA植入物导致信号衰减和信噪比下降，任务必须采用模块化设计以积累足够信号，这限制了其检测快速、序列性单个事件的能力。
*   **时间分辨率受限**：fUSI信号本质是血液动力学信号（CBV变化），其时间分辨率（本研究中为0.6 Hz）远低于电生理信号，不适合解码需要毫秒级精度的快速神经过程。
*   **实验设置限制**：当前fUSI系统仍需连接较大的采集和处理设备，限制了受试者的活动范围，且探头的放置和位置重复性仍是一个挑战。
*   **伪迹风险**：文中虽提及解码权重位于功能相关脑区，表明解码器并非主要依赖运动伪迹，但完全排除肌肉活动或头动等伪迹的影响仍具挑战性。

（完）
