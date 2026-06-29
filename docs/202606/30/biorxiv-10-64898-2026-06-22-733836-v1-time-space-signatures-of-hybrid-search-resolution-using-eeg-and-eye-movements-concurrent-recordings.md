---
title: Time space signatures of hybrid search resolution using EEG and eye movements concurrent recordings
title_zh: 基于脑电图与眼动同步记录的混合搜索解析时空特征
authors: "Care, D., Gonzalez, J. E., Ison, M. J., Kamienkowski, J. E."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733836v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 基于反卷积的EEG分析以分离视觉搜索中的神经激活模式
tldr: 本研究针对自然场景下视觉搜索中神经信号重叠的难题，采用反卷积分析共注册的EEG与眼动数据，成功分离出混合视觉-记忆搜索任务中时间响应函数的细粒度激活模式。方法复制了视觉加工与目标检测的经典成分，并揭示了未命中目标的较弱类P300反应，表明反卷积可有效探究自由观看行为中注意与记忆的动态交互，为生态化认知研究提供了新途径。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统事件相关方法无法分离自然场景下重叠的神经信号，限制了生态效度下的认知研究。
method: 对混合搜索任务中的共注册EEG和眼动数据运用反卷积分析，估计时间响应函数并控制模型复杂度。
result: 反卷积捕获了视觉加工和目标检测的精细时空特征，包括目标检测的P300晚期成分及未命中目标的类似但更弱反应，模型性能随复杂度提升且保持稳定。
conclusion: 反卷积方法结合眼动与脑电可揭示自由观看中注意和记忆过程的动态交互，增强了生态化认知研究的可行性。
---

## 摘要
理解大脑如何在自然环境中支持视觉搜索，其中注意与记忆必须协同工作以在干扰项中找到目标，这需要分析那些在时间上响应重叠且多种环境变量同时交互的神经信号。传统的事件相关方法无法分离这些重叠信号，从而构成了在生态效度条件下研究认知的根本瓶颈。本研究旨在分离自然场景下混合视觉与记忆搜索任务中的激活模式。我们表明，将基于去卷积的方法应用于同步记录的脑电图和眼动数据可以解决这一问题，捕获时间响应函数（TRF）中主效应及其交互作用的精细激活模式。从假设驱动模型出发，我们在允许自由眼动的混合搜索任务中复现了视觉加工和目标检测的经典成分。此外，将我们的方法扩展至层级更大的数据驱动模型，使我们能够探索以往被分开研究的效应之间的交互作用。我们发现TRF估计值随模型复杂度增加而保持稳定，这通过改进的模型性能（皮尔逊相关系数）得到支持，并由方差膨胀因子（VIF）控制。我们识别出一个与目标检测相关的晚期激活，符合P300成分，并揭示漏检会引发类似但较弱的响应，表明其作用比简单的检测更为微妙。这些发现证明，去卷积方法辅以支持特征空间扩展的稳健模型性能指标，能够揭示自由观看行为下注意与记忆过程的动态相互作用。

## Abstract
Understanding how the brain supports visual search in naturalistic environments, where attention and memory must work together to find targets among distractors, requires analysing neural signals where responses overlap in time and multiple environmental variables simultaneously interact. Conventional event-related methods cannot disentangle these overlapping signals, creating a fundamental bottleneck for studying cognition in ecologically valid settings. Here, we seek to isolate activation patterns during a hybrid visual and memory search task in naturalistic scenarios. We show that our deconvolution-based approach applied to coregistered EEG and eye-tracking data resolves this problem, capturing fine grained activation patterns in the temporal response functions (TRFs) for main effects and their interactions. Starting from hypothesis driven models, we replicated established components for visual processing and target detection in a Hybrid Search task with unrestricted eye movements. Moreover, extending our approach to hierarchically larger data-driven models enabled us to explore interactions between the effects that have otherwise been studied separately. We showed that the TRF estimates remained stable with increasing model complexity, supported by improved model performance (Pearson s correlation coefficient) and controlled by the variance inflation factor (VIF). We identified a late activation consistent with the P300 component for target detection, and revealed that missed detections elicited similar but weaker responses, suggesting a more nuanced role than simple detection. These findings demonstrate how deconvolution methods, complemented with robust measures of model performance that support its expansion in features space, can uncover the dynamic interplay of attention and memory processes underlying free-viewing behavior.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

-   **研究动机**：自然场景下的视觉搜索需要注意与记忆协同工作，此时大脑产生的神经响应在时间上高度重叠，且多种环境因素同时交互。传统事件相关电位（ERP）方法依赖刺激锁时平均，无法分离这些重叠信号，成为在生态效度下研究认知的根本性瓶颈。
-   **核心问题**：如何在允许自由眼动的混合视觉–记忆搜索任务中，从共注册的脑电图和眼动数据里，分离出精细的、时间上重叠的神经激活模式。
-   **整体含义**：作者旨在打破自然情境下认知神经研究的僵局，通过反卷积方法重建“时间响应函数”，揭示注意与记忆动态交互的时空特征，使研究更贴近真实生活中的认知过程。

### 2. 论文提出的方法论

-   **核心思想**：将反卷积（去卷积）分析应用于同步记录的脑电图与眼动数据，把连续脑电信号视为多个事件（如注视点、目标检测、漏检等）引起的时间响应函数的线性叠加，从而分离出每个事件成分的独立激活波形。
-   **关键技术与流程**：
    -   **从假设驱动到数据驱动**：先构建包含经典认知成分（视觉加工、目标检测）的假设驱动模型，验证方法有效性；再逐步扩展特征空间，建立层级更大的数据驱动模型，探索不同效应间的交互作用。
    -   **时间响应函数估计**：将观测脑电信号表示为 $Y = X * \beta + \epsilon$ 的形式，其中 $X$ 为包含各事件出现时刻的卷积矩阵，$\beta$ 为待估计的时间响应函数（TRF）。通过回归或正则化方法求解 $\beta$，得到每个事件或条件对应的时域波形。
    -   **模型评估与控制**：
        -   使用**皮尔逊相关系数**衡量模型性能，即预测信号与真实脑电的相关性，随复杂度增加模型性能持续提升。
        -   引入**方差膨胀因子**监控多重共线性，确保特征扩展后系数估计的稳定性和可解释性。
-   **公式描述**（概念性）：观测脑电 $EEG(t)$ 由各事件 $e_i$ 的时间响应函数 $TRF_i(\tau)$ 与事件发生脉冲串 $s_i(t)$ 的卷积叠加而成：
    $$ EEG(t) = \sum_{i} \int_{0}^{T} TRF_i(\tau) \, s_i(t-\tau) d\tau + \epsilon(t) $$
    通过已知的眼动和任务标记构造 $s_i(t)$，反解出 $TRF_i(\tau)$。

### 3. 实验设计

-   **数据集与场景**：
    -   采用**混合视觉–记忆搜索任务**，被试需在自然场景图像的干扰项中寻找目标，任务同时涉及对视觉输入的加工和对记忆表征的匹配。
    -   实验中**允许完全自由的眼动**，以模拟真实观看行为。
    -   同步记录**脑电图和眼动数据**，获取高时间分辨率的神经信号和精确的视觉事件时间戳。
-   **基准与对比方法**：
    -   以传统事件相关方法作为隐含对比基线：传统方法无法在时间重叠信号下分离条件，而本方法则旨在克服此缺陷。
    -   通过复现已知的经典成分（如视觉诱发电位和 P300 类目标检测成分）来构建内部的“基准真值”。
-   **对比维度**：
    -   不同模型复杂度（假设驱动的小模型与层级增加的数据驱动大模型）之间的性能与稳定性对比。
    -   目标检测正确试次与目标漏检试次的时间响应函数对比，以揭示 P300 成分的精细角色。

### 4. 资源与算力

-   **说明**：论文摘要及提供的元数据中**未明确提及**所使用的 GPU 型号、数量或训练时长。该方法主要基于回归/反卷积的统计分析，可能不依赖大规模深度学习训练，因此对算力需求未作特别强调。若需精确评估，需查阅论文全文的实验方法部分。

### 5. 实验数量与充分性

-   **实验组数概览**：
    -   至少包含**假设驱动模型**与**多个层级的数据驱动模型**的对比。摘要提到“将我们的方法扩展至层级更大的数据驱动模型”，暗示可能进行了多组不同特征数量的模型构建实验。
    -   进行了**目标检测 vs 漏检**的效应对比实验。
    -   通过皮尔逊相关系数和方差膨胀因子两个指标，对模型性能与多重共线性做了定量评估。
-   **充分性与客观性评价**：
    -   在摘要描述范围内，实验设计较为充分：既有对经典先验的复现验证（假设驱动），也有允许新发现的数据驱动探索，形成了从确认到探索的递进逻辑。
    -   采用双指标（预测性能与共线性控制）量化模型的可靠性和复杂度代价，评价标准较为客观、公平。但具体样本量、试次数和被试数在摘要中未披露，完整评估需依赖正文细节。

### 6. 论文的主要结论与发现

-   **方法有效性**：反卷积分析成功从高度重叠的共注册信号中分离出精细的时间响应函数，复刻了经典的视觉加工和目标检测成分，证明该方法适用于自由观看的生态化任务。
-   **模型稳定性**：随着模型特征空间扩大，TRF 估计值保持稳定，同时模型预测性能（皮尔逊相关系数）持续提升，方差膨胀因子有效控制了共线性风险。
-   **P300 成分的精细角色**：
    -   确认目标检测会诱发一个晚期正成分，符合 P300 的特征。
    -   首次揭示**漏检目标**也会引发一个波形类似但振幅更弱的反应，表明 P300 并非简单的“目标检测”开关，其响应更细致，可能反映了决策置信度或类目标的记忆匹配过程。
-   **认知动态交互**：反卷积方法能够揭示注意与记忆过程在自由观看行为下的动态交互作用，为生态化认知研究提供了有力新途径。

### 7. 优点

-   **解决关键瓶颈**：直面自然场景下神经信号重叠的根本难题，突破了传统 ERP 方法的生态效度限制，具有重要的方法学创新意义。
-   **融合假设驱动与数据驱动**：先以先验知识验证方法，再扩展到数据驱动探索未知交互，研究框架严谨且具有扩展性。
-   **评估体系稳健**：同时采用皮尔逊相关系数和方差膨胀因子作为评判标准，兼顾模型拟合度和估计的统计可靠性，使结论更有说服力。
-   **精细认知分离**：深入分离出目标检测与漏检的不同神经响应形态，细化了 P300 成分的理论解释，将简单的“检测”概念推进到更连续的认知加工层面。

### 8. 不足与局限

-   **细节信息缺失**：从现有元数据与摘要中，无法获知样本量大小、被试特征、试次数量等关键设计参数，难以评估效应的统计效力和结论的可推广性。
-   **任务与模态局限性**：研究局限于特定的混合搜索任务范式，结果能否推广到其他更复杂或不同类型的自然任务（如社会交互、多感官整合）尚待检验。方法高度依赖眼动和脑电的精确同步，对数据质量和时间对齐精度要求苛刻，在实际嘈杂或低采样率环境中可能面临挑战。
-   **潜在干扰与假设**：反卷积基于线性叠加假设，而真实神经动力学中可能存在非线性交互，该方法可能低估或简化了某些复杂响应。方差膨胀因子虽能控制共线性，但在事件高度相关时，分离出的 TRF 仍可能存在解释上的模糊性。
-   **应用限制**：目前仅展示了对自由观看行为的神经解析，尚未与行为决策模型（如漂移扩散模型）或神经反馈调控等应用端深度结合，从发现到实际干预之间仍有距离。

（完）
