---
title: Effects of EEG Preprocessing on Channel-Wise Attention and Effective Connectivity Alignment in Visual EEG Decoding
title_zh: 视觉脑电解码中EEG预处理对通道注意力与有效连接对齐的影响
authors: "Elichatiti, V. V., Basari, B., Arif, M., Ikhsan, M."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736026v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 评估脑电图预处理对基于Transformer的视觉脑电图解码和注意力机制的影响
tldr: 本研究探讨了EEG预处理策略如何影响Transformer模型在视觉解码中的注意力机制与生物脑有效连接的对齐。使用ATM模型对比仅MVNN和加入ICA与陷波滤波的清洗流程，发现全面预处理能抑制非神经伪迹且保持解码性能稳定，注意力空间模式在不同流程下高度一致，并与GPDC等有向连接网络存在结构对应，为构建神经生理可解释的脑机接口提供了实证依据。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-004.webp\", \"caption\": \"Fig. 1. Overall methodology and architecture framework. (A) The EEG preprocessing workflow, comparing the baseline pipeline with the proposed pipeline (incorporating notch filtering, ICA, and MVNN). (B) The analytical framework for evaluating the alignment between the model’s attention matrix and the reference effective connectivity using Node Strength Comparison and Representational Similarity Analysis (RSA). (C) The Adaptive Thinking Mapper (ATM) encoder architecture, highlighting the extraction of the channel-wise attention matrix from the multi-head self-attention layer [2].\", \"page\": 2, \"index\": 4, \"width\": 1076, \"height\": 767}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-007.webp\", \"caption\": \"Fig. 2. Power Spectral Density (PSD) analysis comparing the baseline and proposed preprocessing pipelines across different brain regions. (A)-(C) PSD distribution in the Frontal, Occipital, and Whole Head regions before MVNN normalization, highlighting the suppression of line noise (50 Hz) and frontal artifacts in the proposed pipeline. (D)-(F) The corresponding PSD distributions after MVNN normalization, demonstrating a more balanced spectral power across regions.\", \"page\": 3, \"index\": 7, \"width\": 1076, \"height\": 606}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-009.webp\", \"caption\": \"Fig. 3. Model training dynamics and classification performance. (A) Top-1 and (B) Top-5 accuracy learning curves over 40 epochs, showing stable convergence for both baseline and proposed models. (C) Comprehensive accuracy comparison (Top-1, Top-5, V10, V4, and V2 settings) evaluated at the final epoch across 10 subjects.\", \"page\": 4, \"index\": 9, \"width\": 1076, \"height\": 483}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-012.webp\", \"caption\": \"Fig. 4. Ablation study results evaluating the contribution of specific EEG components to model performance. (A) Top-1 and (B) Top-5 accuracy drops following the removal of specific frequency bands, indicating the critical role of low frequencies (θ and δ). (C) Top-1 and (D) Top-5 accuracy drops following the removal of specific time windows, highlighting the importance of early visual ERP responses (0–400 ms). (E) Top-1 and (F) Top-5 accuracy show a consistent and significant decline in performance for both models as the noise intensity levels increase from 0.0 to 1.0.\", \"page\": 5, \"index\": 12, \"width\": 1076, \"height\": 606}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-001.webp\", \"caption\": \"Fig. 5. Alignment analysis between the data-driven AI attention weights and the biological effective connectivity (GPDC, PDC, and DTF) across broadband (BB) and specific frequency bands. (A) Spearman’s correlation of node strength, comparing network topology between the models. (B) Representational Similarity Analysis (RSA) scores, showing a general trend toward higher RSA-based structural alignment under the proposed preprocessing pipeline.\", \"page\": 6, \"index\": 1, \"width\": 1076, \"height\": 654}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-005.webp\", \"caption\": \"Fig. 6. Topographical comparison between AI channel-wise attention and reference EEG effective connectivity. These maps illustrate the spatial patterns of Incoming, Outgoing, and Total Node Strengths across 63 EEG channels. The first two columns display the data-driven attention weights extracted from the baseline and proposed models. The last two columns display the corresponding reference connectivity derived from the GPDC metric in the θ (4–8 Hz) and α (8–13 Hz) frequency bands. Color scales are normalized independently for the attention and connectivity representations to emphasize the alignment of spatial network patterns rather than absolute magnitude differences.\", \"page\": 7, \"index\": 5, \"width\": 1076, \"height\": 596}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-011.webp\", \"caption\": \"TABLE I TOP-1 ACCURACY COMPARISON BETWEEN BASELINE AND PROPOSED PREPROCESSING PIPELINES ACROSS SUBJECTS\", \"page\": 9, \"index\": 11, \"width\": 522, \"height\": 247}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-006.webp\", \"caption\": \"TABLE II SPECTRAL ABLATION ANALYSIS RESULTS\", \"page\": 10, \"index\": 6, \"width\": 527, \"height\": 495}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-002.webp\", \"caption\": \"TABLE III TEMPORAL ABLATION ANALYSIS RESULTS\", \"page\": 11, \"index\": 2, \"width\": 514, \"height\": 473}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-003.webp\", \"caption\": \"TABLE IV NOISE ROBUSTNESS ANALYSIS RESULTS\", \"page\": 11, \"index\": 3, \"width\": 532, \"height\": 409}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-010.webp\", \"caption\": \"TABLE V NODE STRENGTH CORRELATION ANALYSIS\", \"page\": 12, \"index\": 10, \"width\": 1076, \"height\": 601}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-008.webp\", \"caption\": \"TABLE VI REPRESENTATIONAL SIMILARITY ANALYSIS (RSA) RESULTS\", \"page\": 13, \"index\": 8, \"width\": 456, \"height\": 559}]"
motivation: 探究EEG预处理差异对深度学习模型的通道注意力与真实脑有效连接之间对齐程度的影响。
method: 采用ATM模型，比较基线（仅MVNN）与综合清洗（ICA+陷波滤波）预处理流水线，通过交叉泛化、噪声鲁棒性分析及与GPDC等参考网络的节点强度相关和表征相似性分析，评估注意力权重与有效连接的对应关系。
result: 综合预处理有效抑制额叶噪声和电气干扰，保持解码准确率；注意力空间组织高度稳定，能捕捉关键有向连接动态，但全局表征几何存在细微信号依赖性变化。
conclusion: EEG预处理虽影响伪迹抑制，但数据驱动的注意力模式与神经生理网络在空间结构上具有稳健的对应性，为开发透明可解释的脑机接口提供了重要参考。
---

## 摘要
基于Transformer的深度学习模型在视觉脑电信号解码方面展现出巨大潜力。然而，其内部的注意力机制通常主要根据优化目标进行评估，使其与生物脑连接的对应关系成为一个开放问题。本研究以Adaptive Thinking Mapper (ATM)模型为框架，实证评估了EEG预处理策略变化对这些注意力表征的影响。我们将基线处理流程（仅MVNN）与整合了ICA和陷波滤波的全面清洗流程进行了比较。通过交叉泛化、噪声鲁棒性和频谱-时间消融分析对模型进行了评估。此外，我们利用节点强度相关和表征相似性分析(RSA)，研究了模型数据驱动的注意力权重与神经生理参考网络（GPDC、PDC和DTF）之间的结构对应关系。结果表明，全面预处理有效抑制了非神经伪迹，如额叶噪声和电干扰，同时保持可比的解码精度和基线鲁棒性。对齐分析揭示，学习到的注意力模式的广泛空间组织在不同处理流程中保持高度稳定，捕捉到关键的有向连接动态，但在整体表征几何上存在细微的、依赖于度量标准的差异。本研究为连接数据驱动的注意力权重与神经生理一致性提供了实证探索，为更透明的脑机接口提供了见解。

## Abstract
Transformer-based deep learning models have shown great potential for decoding visual EEG signals. However, their internal attention mechanisms are often evaluated primarily on optimization objectives, leaving their alignment with biological brain connectivity an open question. This study empirically evaluates how variations in EEG preprocessing strategies affect these attention representations using the Adaptive Thinking Mapper (ATM) model as a framework. We compared a baseline pipeline (MVNN only) against a comprehensive cleaning pipeline integrating ICA and notch filtering. The models were evaluated through cross-generalization, noise robustness, and spectral-temporal ablation analyses. Furthermore, we investigated the structural correspondence between the models data-driven attention weights and neurophysiological reference networks (GPDC, PDC, and DTF) using Node Strength Correlation and Representational Similarity Analysis (RSA). The results show that the comprehensive preprocessing successfully suppresses non-neural artifacts, such as frontal noise and electrical interference, while maintaining comparable decoding accuracy and baseline robustness. Alignment analyses revealed that the broad spatial organization of the learned attention patterns remains highly stable across pipelines, capturing key directed connectivity dynamics with subtle, metricdependent variations in global representational geometry. This work provides an empirical exploration into bridging data-driven attention weights with neurophysiological consistency, offering insights toward more transparent brain-computer interfaces.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将基于提供的论文内容，为您生成一份结构化、深入、客观的中文总结。

### 1. 核心问题与整体含义

- **核心问题**：本研究旨在探究**不同的EEG预处理策略**（基线仅MVNN vs. 综合清洗流程）如何影响基于Transformer的视觉EEG解码模型（ATM）内部的**通道注意力机制**，特别是注意力权重与神经生理学中**有效连接**网络的**结构对应关系**（即生物可解释性）。
- **研究动机与背景**：
  - 基于Transformer的深度学习模型在EEG视觉解码中潜力巨大，但其数据驱动的注意力机制是否与真实的脑连接动态一致尚不明确，这限制了模型的透明度和医学可信度。
  - 预处理（如ICA、陷波滤波）能抑制伪迹，但可能引入数据分布偏移，改变模型学到的表征，进而影响其生物可解释性。
  - 有效的脑连接度量（GPDC, PDC, DTF）可提供有向的参考网络，用于评估AI注意力的神经生理合理性。

### 2. 方法论

- **核心思想**：不局限于优化目标（解码准确率），而是通过对比不同预处理下模型的注意力模式与生物学参考连接网络的对齐程度，来评估预处理对模型生物可解释性的影响。
- **关键技术细节与流程**：
  - **预处理流水线对比**：
    - **基线流程**：仅进行多元噪声归一化 (Multivariate Noise Normalization, MVNN)。
    - **全面清洗流程**：在MVNN之前，先应用50Hz陷波滤波器（抑制工频干扰）和独立成分分析（Independent Component Analysis, ICA，用于移除眼动等生理伪迹）。
  - **模型架构**：采用Adaptive Thinking Mapper (ATM) 编码器，重点关注其**多通道注意力层**。该层通过多头自注意力机制学习EEG通道间的关系，其注意力权重计算公式为：
      $$ \text{Attention}(\hat{Q}, \hat{K}, \hat{V}) = \text{softmax}\left(\frac{\hat{Q}\hat{K}^\top}{\sqrt{d_k}}\right)\hat{V} $$
  - **有效连接参考矩阵构建**：基于多元自回归模型(Multivariate Autoregressive, MVAR)，计算三种频域有效连接度量作为生物学对照：
    - **偏定向相干 (Partial Directed Coherence, PDC)**:
        $$ \pi_{ij}(f) = \frac{|A_{ij}(f)|}{\sqrt{\sum_{m=1}^n |A_{mj}(f)|^2}} $$
    - **广义偏定向相干 (Generalized PDC, GPDC)**:
        $$ \pi_{gij}(f) = \frac{\frac{1}{\sigma_i}|A_{ij}(f)|}{\sqrt{\sum_{m=1}^n \frac{1}{\sigma_m^2}|A_{mj}(f)|^2}} $$
    - **定向传递函数 (Directed Transfer Function, DTF)**:
        $$ \gamma^2_{ij}(f) = \frac{|H_{ij}(f)|^2}{\sum_{m=1}^n |H_{im}(f)|^2} $$
  - **对齐分析方法**：
    - **节点强度相关性**：计算并比较AI注意力图和生物连接图中各通道的节点强度（总连接权和），使用斯皮尔曼秩相关评估局部拓扑的对齐程度。
    - **表征相似性分析 (RSA)**：分别构建注意力矩阵和连接矩阵的表征不相似矩阵(Representational Dissimilarity Matrices, RDMs)，再计算两个RDM之间的相关性，以评估整体网络几何结构的相似性。

### 3. 实验设计

- **数据集**：使用公开的 **THINGS-EEG2** 数据集，包含10名健康被试，采用快速序列视觉呈现(RSVP)范式。数据由63导联采集，采样率1000Hz，包含16,540张训练图像和200张测试图像。
- **基准方法 (Benchmark)**：以仅使用MVNN预处理的ATM模型作为基线。
- **对比方法**：
  - **预处理对比**：全面评估基线预处理模型和全面清洗预处理模型的性能。
  - **交叉泛化测试**：将在一种预处理下训练的模型在另一种预处理的数据上测试，评估其对分布偏移的鲁棒性。
  - **消融实验**：
    - **频谱消融**：依次移除delta，theta，alpha，beta，gamma和工频噪声(45-55Hz)频段。
    - **时间消融**：依次移除0-200ms，200-400ms，400-600ms，600-800ms，800-1000ms的时间窗口。
  - **噪声鲁棒性测试**：在测试数据中注入不同强度（σ=0.0, 0.1, 0.3, 0.5, 1.0）的高斯噪声。
  - **生物可解释性对齐**：将两种预处理模型学到的注意力权重，分别与GPDC、PDC、DTF三种参考有效连接在不同频段下进行相关性分析。

### 4. 资源与算力

- 论文中**未明确说明**所使用的GPU型号、数量及具体训练时长。
- 提及的训练超参数包括：优化器为AdamW，学习率3e-4，批大小64，训练40个epochs，并固定了随机种子(24)。

### 5. 实验数量与充分性

- **实验数量**：实验设计较为全面，涵盖了性能评估（5种Top-k和候选集设置）、泛化性（交叉测试）、鲁棒性（5种噪声等级）、内部属性（6种频谱消融、5种时间消融）和生物可解释性（3种连接度量×7个频段的节点强度和RSA分析）等**超过50个维度的评估**。
- **充分性与公平性**：
  - 实验采用了**固定的随机种子和评估条件**（如使用最终epoch模型而非最优模型），确保了模型间对比的公平性。
  - 在统计分析上，使用了**配对t检验**，并计算了**效应量**，同时对多重比较问题进行了**FDR校正**，保证了结论的严谨性。
  - 消融和鲁棒性实验系统地分析了模型的行为，为理解其工作机制提供了充分证据。
  - 局限性在于仅在10名被试的单一数据集上验证，样本量相对有限。

### 6. 主要结论与发现

- **预处理效果**：综合预处理成功抑制了额叶的肌电/眼动伪迹和50Hz工频干扰，且解码准确率与基线流程相比**没有显著下降**，两种流程性能可比。
- **模型驱动力**：Transformer模型的视觉解码能力**主要依赖于低频EEG成分（特别是theta和delta频段）和早期事件相关电位(ERP)时间窗口（0-400ms）**。移除这些成分会极大地降低模型性能。
- **网络对齐**：模型学到的注意力权重在**广泛的空间组织上高度稳定**，不受预处理流程严重影响。与有效连接的比较中，注意力模式与**GPDC度量**的对齐度最高，尤其在theta和alpha频段。
- **生物可解释性的度量依赖性**：预处理对齐结果的影响存在度量依赖性：
  - **局部拓扑（节点强度）**上，两种预处理的对齐度均稳定，无显著差异。
  - **整体表征几何（RSA）**上，全面预处理流程展现出细微的、统计上不显著的积极偏移，表明其学到的全局结构可能与生物学连接模式更为接近。

### 7. 优点

- **多维度的综合评估**：研究不仅仅依赖解码准确率，而是从性能、鲁棒性、内部驱动机制和生物可解释性等多个层面系统地评估预处理的影响，框架非常全面。
- **将AI模型与神经生理学对齐的深度探索**：首次系统性地将Transformer的通道注意力与多种频域有效连接度量（GPDC, PDC, DTF）进行拓扑和几何上的对齐分析，为模型的可解释性提供了全新的量化视角。
- **严谨的统计分析**：使用配对检验、效应量和FDR校正，确保了实验结论的统计可靠性和客观性。
- **利用“双算子”关联分析**：同时使用节点强度（关注局部Hub）和RSA（关注全局几何结构）这两种互补的分析方法，提供了关于网络对齐的更细致洞察。

### 8. 不足与局限

- **样本与数据集单一**：实验仅在THINGS-EEG2一个数据集的10名被试上进行，结论的普适性（如推广到其他视觉刺激、其他范式的数据集）有待验证。
- **生物学对齐的解释深度**：虽然研究发现GPDC对齐度最高，但未深入阐明为何是GPDC而非PDC或DTF更贴合注意力机制。RSA对齐度在绝对值上较低且提升不显著，这可能削弱“提高可解释性”这一论断的强度。
- **缺乏与更简单基线模型的对比**：研究的可解释性分析仅限于Transformer架构，未与非注意力机制模型（如EEGNet，LSTM）的权重模式进行对比，难以说明是Transformer特有的现象还是通用模式。
- **预处理IOC的选择标准**：研究仅说明了基于“时间特性和头皮地形图”来识别ICA伪迹成分，但具体选择标准和拒绝成分数量的透明度不高，这为复现研究带来了一定不确定性。
- **未报告计算资源**：缺失关于GPU算力和训练时间的信息，使得评估该工作的可复现成本和效率变得困难。

（完）
