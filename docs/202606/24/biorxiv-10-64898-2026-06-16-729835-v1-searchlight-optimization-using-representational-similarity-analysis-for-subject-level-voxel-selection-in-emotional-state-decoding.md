---
title: Searchlight Optimization Using Representational Similarity Analysis for Subject-Level Voxel Selection in Emotional State Decoding
title_zh: 使用表征相似性分析进行搜索光优化以实现情绪状态解码中的被试级体素选择
authors: "Wang, X., Zweerings, J., Lührs, M., Cong, F., Mathiak, K., Linden, D. E. J., Goebel, R., Ciarlo, A., Mehler, D. M. A."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.16.729835v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 搜索光RSA从fMRI时间序列解码情绪状态
tldr: 针对fMRI多条件分析中难以捕捉精细表征差异的挑战，本研究提出一种个体水平探照灯优化框架。该框架结合基于一般线性模型的单变量分析和基于表征相似性分析的多变量精炼，并通过贝叶斯优化自动调参，从情绪想象fMRI数据中识别既任务相关又条件敏感的体素。实验表明，该方法改善了表征结构对齐，比分类器法更好保留情绪状态的表征几何，为情感脑状态的多变量研究提供了实用方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有体素选择方法依赖预定义脑区或激活标准，不足以捕获多条件fMRI中的精细表征差异，尤其限制了神经反馈等干预的靶点精准性。
method: 提出融合单变量GLM和多变量RSA的探照灯优化框架，并引入数据驱动的贝叶斯优化从小数据集自动调参。
result: 在四类情绪想象任务中，RSA精炼比单纯单变量选择提升了表征对齐度，且相较于分类器法，更好地保留了表征几何结构并维持判别力。
conclusion: 所提RSA框架在多条件情感fMRI中能高效稳健地选择条件敏感体素，支持精准的多变量脑状态研究。
---

## 摘要
在功能磁共振成像（fMRI）中，识别信息性体素是关键但具有挑战性的一步，特别是对于涉及多个相关条件的多变量分析。现有方法通常依赖于预定义的感兴趣区（ROI）或基于激活的标准，这可能不足以捕捉精细的表征差异。这一挑战在实验设置和干预（如神经反馈训练）中尤为相关，其中体素不仅作为神经反应被测量，还根据其先前观察到的活动模式被用作干预目标。在本研究中，我们提出了一个被试级搜索光优化框架，该框架将基于体素的一般线性模型（GLM）的单变量分析与基于表征相似性分析（RSA）的多变量细化相结合，以识别既与任务相关又对条件敏感的体素。为了提高实际应用性，该框架进一步结合了基于贝叶斯优化的数据驱动超参数调优步骤，能够从小型试点数据集中高效识别高性能配置，并在应用于更大样本时保持一致的性能。所提出的框架使用包含四种情感条件的情绪想象fMRI数据集进行了评估。结果表明，与仅使用单变量选择相比，多变量细化改善了经验与目标表征结构之间的一致性。与基于分类器的体素选择方法相比，基于RSA的方法在保持判别能力的同时，更好地保留了情绪状态的表征几何结构。这些发现凸显了所提出的RSA框架的有效性、效率和稳健性，为识别条件敏感体素提供了一个实用的解决方案，并支持在多条件fMRI研究中对情感脑状态进行更精确的多变量研究。

## Abstract
Identifying informative voxels is a critical, yet challenging step in functional magnetic resonance imaging (fMRI), particularly for multivariate analyses involving multiple related conditions. Existing approaches often rely on predefined regions of interest (ROIs) or activation-based criteria, which may be insufficient for capturing fine-grained representational differences. This challenge becomes particularly relevant in experimental settings and interventions such as neurofeedback training, where voxels are not only measured as neural responses but also used as targets for intervention based on their previously observed activity patterns. In this study, we propose a subject-level searchlight optimization framework that integrates voxel-wise general linear model (GLM)-based univariate analysis with representational similarity analysis (RSA)-based multivariate refinement to identify voxels that are both task-relevant and condition-sensitive. To enhance practical applicability, the framework further incorporates a data-driven hyperparameter tuning step based on Bayesian optimization, enabling efficient identification of high-performing configurations from small pilot datasets, with consistent performance when applied to larger samples. The proposed framework was evaluated using an emotion imagery fMRI dataset with four affective conditions. Results demonstrate that the multivariate refinement improves alignment between empirical and target representational structures compared with univariate selection alone. Compared with a classifier-based voxel selection approach, the RSA-based approach better preserves the representational geometry of emotional states while maintaining discriminative capacity. These findings highlight the effectiveness, efficiency, and robustness of the proposed RSA framework, providing a practical solution for identifying condition-sensitive voxels and supporting more precise multivariate investigation of affective brain states in multi-condition fMRI studies.

---

## 论文详细总结（自动生成）

好的，以下是根据论文内容生成的结构化中文总结。

### 1. 论文的核心问题与整体含义

*   **研究动机与背景**：在功能性磁共振成像（fMRI）的多变量分析中，如何选择信息性体素（voxel）是一个基础但困难的步骤。传统方法，无论是基于解剖预定义的感兴趣区（ROI），还是基于单变量激活强度的对比，都存在局限。
    *   **ROI方法的局限**：假设同一解剖区域的体素具有相同的功能属性，忽略了皮层表征的精细异质性。
    *   **单变量激活方法的局限**：对振幅差异敏感，但无法捕捉跨条件分布式的多变量活动模式中所携带的丰富信息，特别是在需要区分多个相关条件（如不同情绪状态）的范式中。
*   **核心问题**：如何开发一个能够识别既与任务相关、又对条件间精细表征差异敏感的个体化体素选择方法？
*   **整体含义**：本研究旨在提出一个系统化、可优化的框架，解决多条件fMRI研究中的体素选择难题，尤其适用于神经反馈等需要精准定位干预靶点的应用场景，从而支持对情感脑状态更精确的多变量研究。

### 2. 论文提出的方法论

*   **核心思想**：提出一个被试级“搜索光优化框架”（Searchlight Optimization Framework），其核心是结合单变量激活分析和多变量表征相似性分析（RSA）的优势，并辅以数据驱动的超参数自动调优，以精确筛选体素。
*   **关键技术流程**：
    1.  **单变量预选**：
        *   对每个条件（情绪）的fMRI run，使用体素级一般线性模型计算“任务 vs. 静息”对比的 $t$ 值。
        *   根据 $t$ 值的百分位区间（由 `univThr` 定义，如 50%-80%）和集群大小阈值（`clusterThr`）筛选体素。
        *   将各条件下筛选出的体素图进行逻辑“或”运算，得到最终的**单变量选择图谱**，包含至少在一种情绪下被强烈激活的体素。
    2.  **多变量精炼**：
        *   在单变量选择图谱的范围内，进行搜索光分析。对每个体素，以其为中心，根据预设形状（`shape`，如立方体）和半径（`radius`）定义局部邻域。
        *   提取邻域内所有体素的 $t$ 值作为局部多变量模式，通过计算各条件间局部模式的成对皮尔逊相关，构建每个体素的表征不相似性矩阵（RDM）。
        *   将每个体素的搜索光RDM与一个预定义的**目标模型RDM**（编码了对条件间相似性关系的假设，如仅唤醒度、仅效价或两者结合）进行比较，计算相似性（`metric`，如斯皮尔曼相关）。
        *   根据相似性得分（`multThr`）和集群大小阈值（`clusterThr`），筛选出最终的多变量选择体素集。
    3.  **超参数优化**：
        *   **方法**：使用**贝叶斯优化**，在小型试点数据集上，通过少量迭代（如100次）高效探索超参数空间（共6,480种组合），寻找使经验RDM与目标模型RDM斯皮尔曼相关性最大化的最优配置。
        *   **目的**：解决体素选择中大量超参数（搜索光形状/半径、阈值、相关性度量等）难以手动设定的问题，并验证从小样本得到的最优配置推广到更大样本时的表现。

### 3. 实验设计

*   **数据集与场景**：
    *   **任务**：情绪想象任务（fMRI），包含四种情感条件：愉悦放松、悲伤、热情、愤怒。
    *   **数据**：分为两组。**试点数据集**包含6名健康被试，用于超参数搜索与优化；**主数据集**包含27名健康被试，用于验证框架的泛化性能和最终效果。数据来源于一项预注册的神经反馈研究。
*   **基准与对比方法**：
    *   **内部基准**：比较**单变量选择阶段**与**多变量选择阶段**（即框架最终输出）的RDM，以验证多变量精炼步骤的增益。
    *   **外部对比**：将RSA方法与经典的**基于分类器的搜索光体素选择方法**进行全面比较。分类器方法使用L2正则化的逻辑回归（LR），在相同搜索光内进行5折交叉验证，根据分类准确率选择体素，并匹配RSA方法选出的体素数量。
*   **评估指标**：
    *   **表征对齐度**：经验RDM与目标模型RDM之间的斯皮尔曼相关系数。
    *   **判别能力**：基于所选体素的情绪状态分类准确率。

### 4. 资源与算力

*   论文中**未明确提及**进行数据分析所使用的GPU型号、数量或具体训练/计算时长。研究主要涉及统计计算（如GLM、相关性分析）和贝叶斯优化，这些计算通常对CPU依赖较高，但文中未给出算力配置细节。

### 5. 实验数量与充分性

*   **实验数量**：
    *   **超参数分析**：在试点数据集（6人）上，对全部6,480种超参数组合进行了网格搜索和100次贝叶斯优化迭代；并使用线性混合效应模型（LMM）对所有超参数的主效应进行了统计分析。
    *   **方法验证**：在主数据集（27人）上，使用优化后的最优配置评估了RSA方法在内部阶段（单变量 vs. 多变量）的改进，并与分类器方法（LR）进行了对比。
    *   **目标模型泛化性**：所有分析均在4种不同的目标模型RDM上进行，以考察框架对不同表征假设的鲁棒性。
*   **充分性与客观性**：
    *   **充分**：实验设计严谨，系统地探索了超参数空间，并使用独立的试点数据和主数据分别进行探索和验证，评估了泛化性。对比分析公平，使用了多种评估指标（相关性、准确率）和多个目标模型。
    *   **客观公平**：对比分类器方法时，保证了搜索光大小等关键配置一致，并控制了最终选择的体素数量，使得比较基础公平。

### 6. 论文的主要结论与发现

1.  **框架有效性**：所提出的融合单变量GLM与多变量RSA的搜索光优化框架，能成功识别出既与任务相关又对精细情绪条件敏感的体素。多变量精炼步骤显著提升了所选体素群的特异性，使其表征结构与目标模型更一致。
2.  **调参高效性**：基于贝叶斯优化的超参数调优步骤，能用极少（100次迭代）的试点数据高效找到高性能配置，且这些配置在应用到更大样本时仍能维持性能增益轨迹。
3.  **方法互补性**：RSA方法与分类器方法各有所长，存在互补关系。
    *   **RSA方法**：在**表征对齐度**（斯皮尔曼相关）上表现更优，能更好地保留情绪状态的连续表征几何结构。
    *   **分类器方法**：在**分类准确率**上表现更优，更擅长寻找最大化类别间可分性的体素。
    *   **空间差异**：两者所选的体素集存在部分重叠，但也展现出不同的空间偏好。RSA方法更倾向于选择内侧前额叶和边缘系统区域（如前扣带皮层、杏仁核、海马体）。
4.  **反直觉发现**：最优的单变量阈值并非最高的激活百分位（如80%-100%），而是中等百分位区间（如50%-80%），表明中等但可靠的任务激活对于区分多个相关条件可能更为有效。

### 7. 优点

*   **方法论创新**：首次系统性地提出了一个可优化的、结合单变量和多变量信息的体素选择框架，超越了传统的纯激活或纯解剖先验方法。
*   **实用的调优策略**：引入数据驱动的贝叶斯优化超参数调优，解决了手动调参的困难和不稳定性，并证明了从小数据集调优到大数据集应用的可行性，提升了方法的实际应用价值。
*   **评估全面且客观**：不仅进行了内部阶段验证，还与主流的分类器方法进行了多维度的公平比较（既比表征对齐度，又比分类准确率），深刻揭示了两类方法的互补特性。
*   **理论匹配度高**：RSA方法的选择标准与将情绪等心理过程视为连续维度空间的理论视角高度契合，为研究此类问题提供了更合适的工具。

### 8. 不足与局限

*   **对先验模型的依赖**：体素选择效果高度依赖于预定义的目标模型RDM。如果模型本身质量不高或不符合神经表征，会直接影响结果。未来可探索模型自适应或融合行为数据的方法。
*   **数据充分性受限**：由于每个实验run的任务block数量（10个）有限，无法评估体素反应的“重测信度”，而这被认为可以提升多变量分析的稳定性。将其纳入超参数优化目前尚不可行。
*   **效度比较的局限**：与分类器方法的对比仅基于离线分析指标（准确率和相关性），缺乏在真实的应用任务（如神经反馈调控）终端的直接效果对比。离线指标的优势不一定能转化为应用中的优势。
*   **被试样本**：试点数据集（6人）的样本量较小，其得出的超参数效应估计（尽管模式稳定）可能仍需谨慎解读。

（完）
