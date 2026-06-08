---
title: Cross-domain encoding models reveal shared and domain-specific neural representations across language and mathematics
title_zh: 跨领域编码模型揭示语言与数学共享且领域特定的神经表征
authors: "Nakai, T., Kubo, T., Nishimoto, S."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.07.730750v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 使用LLM特征的跨域编码模型解释神经表征
tldr: 本研究利用大型语言模型的潜在特征和顶点编码模型，在句子理解与计算任务的fMRI数据中探讨语言和数学的神经表征异同。发现左侧55b等区域存在部分共享表征，同时左前颞上回及角回对语言更具特异性，左中央前回及顶内沟对数学更具特异性，并揭示了相应的功能连接差异，表明两领域既有共享也有独特神经基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决认知神经科学中关于语言和数学是否依赖共享或独立神经表征的争议。
method: 采用大型语言模型的潜在特征和顶点编码模型，分析32名被试执行句子理解和计算任务的fMRI数据。
result: 跨域预测发现左侧55b为共享表征区域，任务特异性分析显示语言相关在左前颞上回和角回，数学相关在左中央前回和顶内沟，且不同区域权重分布不同，功能连接也呈现任务依赖性。
conclusion: 语言和数学涉及部分共享的神经表征，同时保留领域特异性的皮层组织。
---

## 摘要
语言与数学是否依赖共享或独特的神经表征，仍然是认知神经科学中一个悬而未决的问题。本研究将大型语言模型的潜在特征与基于顶点的编码模型相结合，以考察语言与数学之间的跨领域泛化。32名参与者在fMRI扫描中执行句子理解与计算任务，并使用嵌入在共同潜在空间中的特征训练编码模型。跨领域预测识别出与部分共享表征相关的皮层区域，最显著的是左侧55b区，而控制分析表明这些效应不能完全归因于低级视觉处理或简单任务一般性因素。任务特异性对比显示，左侧颞上回前部与角回与语言相关的预测更强，而左侧中央前回与顶内沟则与数学相关的预测更强。模型权重分析进一步表明，共享与领域特定的预测模式在皮层区域间表现为不同的权重分布。连接分析显示，跨领域区域与语言或数学相关网络之间存在任务依赖的功能耦合。综上，这些发现表明语言与数学涉及部分共享的神经表征，同时伴随领域特定的皮层组织，有助于调和先前对其神经基础的对立观点。

## Abstract
Whether language and mathematics rely on shared or distinct neural representations remains an unresolved question in cognitive neuroscience. Here we combine latent features from a large language model (LLM) with vertex-wise encoding models to examine cross-domain generalization between language and mathematics. Thirty-two participants performed sentence comprehension and calculation tasks during fMRI, and encoding models were trained using features embedded in a common latent space. Cross-domain prediction identified cortical regions associated with partially shared representations, most prominently the left 55b, while control analyses suggested that these effects could not be fully explained by low-level visual processing or simple task-general factors. Task-specificity contrasts revealed stronger language-related prediction in the left anterior superior temporal and angular gyri and math-related prediction in the left precentral and intraparietal sulci. Model-weight analyses further showed that shared and domain-specific prediction patterns were reflected in distinct weight profiles across cortical regions. Connectivity analyses showed task-dependent functional coupling between cross-domain regions and language- or math-related networks. Together, these findings suggest that language and mathematics involve partially shared neural representations alongside domain-specific cortical organization, helping reconcile previous contrasting views on their neural basis.

---

## 论文详细总结（自动生成）

好的，作为资深学术论文分析助手，我将使用中文、以 Markdown 形式，对该论文进行结构化、深入、客观的总结。

---

# 跨领域编码模型揭示语言与数学共享且领域特定的神经表征

## 1. 研究背景与核心问题

*   **核心问题**：认知神经科学领域一个悬而未决的根本问题是，语言和数学这两种高阶认知功能，究竟是依赖完全独立的神经系统，还是在某种程度上共享神经基础。
*   **现有争议**：目前存在两种对立观点。
    *   **独立观**：大量神经影像学和神经心理学证据表明，语言主要涉及左侧额下回和颞上回皮层，而数学则更多与背外侧前额叶和顶叶皮层相关。失语症患者保留计算能力的案例也支持此观点。
    *   **共享观**：另有研究发现，语言和数学任务在左侧额叶皮层存在激活重叠，且左侧额叶损伤会同时影响语言和数学能力。这可能反映了二者共有的、处理符号序列结构关系的神经机制。
*   **研究动机**：为了弥合这一分歧，本文旨在通过一个统一的定量框架，利用跨领域编码模型，系统性地探究语言和数学在神经表征层面的共性与特性。

## 2. 方法论核心思想与技术细节

*   **核心思想**：利用大型语言模型（LLM）作为特征提取器，将语言和数学刺激映射到一个**共享的潜在特征空间**中。然后，通过构建顶点的编码模型，检验在一个领域（如语言）上训练的模型能否预测另一个领域（如数学）的大脑活动（即跨领域泛化），从而量化神经表征的共享程度。
*   **关键技术细节与流程**：
    1.  **特征提取与共享空间构建**：
        *   使用日文版 LLM（Llama3，Gemma2 等多个模型）为每个语言刺激（句子）和数学刺激（算式）提取潜在特征。
        *   对语言和数学训练刺激的 LLM 特征进行拼接，然后通过**联合主成分分析**将高维特征降至 100 维，形成一个共享的潜在特征空间。PCA 变换仅在训练集上拟合，然后应用于独立的测试集。
    2.  **顶点编码模型构建**：
        *   为每个皮层顶点拟合一个有限脉冲响应模型，用于预测血氧水平依赖（BOLD）信号。
        *   输入为时间上延迟了 3-6 秒的 100 维特征矩阵，输出为该顶点的 fMRI 时间序列。
        *   使用 L2 正则化线性回归（岭回归）训练模型权重，正则化参数通过 5 折交叉验证确定。
    3.  **跨领域预测与分析**：
        *   **域内预测**：用语言数据训练的模型预测语言任务下的脑活动；数学模型同理。此为基线。
        *   **跨领域预测**：用语言模型预测数学任务下的脑活动；数学模型反之。此为检验共享表征的关键。
        *   **联合分析**：通过最小统计量法，找出在四种预测（语言→语言，数学→数学，语言→数学，数学→语言）中都显著的大脑区域，作为“跨领域区域”。
        *   **领域特异性分析**：通过对比域内预测与跨领域预测的平均准确度，分别定位语言和数学特异性脑区。

## 3. 实验设计与对比方法

*   **数据集**：
    *   **被试**：32 名以日语为母语、右利手的健康成年人。
    *   **任务与刺激**：被试在 fMRI 扫描中执行 4 种任务。
        *   **语言目标条件**：理解含有关系从句的句子（如“追了松鼠的猫从篱笆上掉下来”）。
        *   **语言控制条件**：记忆一系列无关联的单词列表。
        *   **数学目标条件**：计算包含两个运算符的算式（如 “7 × 6 + 3”）。
        *   **数学控制条件**：记忆一系列无关联的数字列表。
*   **基准与对比方法**：研究设计了多重控制分析以验证结果的稳健性。
    *   **与无结构刺激对比**：将编码模型应用于语言和数学的控制条件，以评估共享表征是否由任务一般性因素（如工作记忆、视觉注意力）驱动。
    *   **与低级视觉模型对比**：使用 AlexNet 的浅层特征作为预测变量，执行相同的跨领域分析，以排除低级视觉加工的影响。
    *   **与独立特征空间对比**：分别对语言和数学特征进行**独立 PCA** 降维，而非共享的联合 PCA，以验证共享特征空间的必要性。
    *   **时间序列置换检验**：通过随机打乱特征时间序列，破坏刺激与特征的对应关系，进行 100 次迭代的控制分析。
    *   **跨模型与跨层检验**：使用 6 种不同的 LLM 及其多个中间层的特征重复分析，以检验结果的跨模型可重复性。

## 4. 资源与算力

*   文章研究方法部分未提及训练或运行模型所需的 GPU 型号、数量及具体训练时长。其计算主要集中在离线的特征提取（LLM）和相对轻量级的顶点岭回归模型拟合。

## 5. 实验充分性与评估

*   **实验数量充足**：研究进行了大量实验，包括多种主要分析、多重控制分析、补充分析和可视化。覆盖了 6 个 LLM 的 5 个不同层次特征，并对子层（注意力/MLP）进行了单独分析。
*   **评估客观公平**：实验设计严谨，通过多重对比（域内 vs. 跨域、目标 vs. 控制、LLM 模型 vs. 视觉模型、联合 PCA vs. 独立 PCA）系统性地排除了众多潜在混淆因素。统计上采用了被试间的非参数检验（Wilcoxon 符号秩检验）并进行了多重比较校正，保证了结论的客观性和公平性。
*   **样本量合理**：32 名被试的样本量在认知神经科学领域的编码模型研究中属于较高水平。

## 6. 主要结论与发现

*   **发现部分共享神经表征**：跨领域编码模型能够成功预测脑活动，最显著和一致的跨领域区域是**左侧 55b 区**。控制分析表明，此共享表征不能被低级视觉、工作记忆等简单任务一般性因素所解释。
*   **证实领域特异性表征**：
    *   **语言特异性**：更强的语言特异性预测出现在经典的“语言网络”区域，如左侧颞上沟前部、角回和额下回。
    *   **数学特异性**：更强的数学特异性预测出现在经典的“数学网络”区域，如双侧顶内沟、左侧中央前回和外侧前额叶皮层。
*   **表征差异体现在模型权重中**：共享区域（如左侧 55b）的权重在语言和数学模型间呈正相关，而领域特异性区域的权重则呈负相关，表明其功能映射存在差异。
*   **功能连接的动态重构**：跨领域区域（尤其是左侧 55b）在语言任务中与语言网络的功能连接增强，而在数学任务中则与数学网络的功能连接增强，表现出动态的、任务依赖的网络整合能力。
*   **模型架构的贡献差异**：Transformer 中的自注意力子层对跨领域预测贡献更大，而 MLP 子层则对领域特异性预测贡献更大。

## 7. 优点与亮点

*   **统一且定量的框架**：利用 LLM 特征和跨领域编码模型，为长期存在的“语言-数学”神经基础之争提供了一个定量的、可检验的解决方案，超越了传统的激活重叠分析。
*   **多重严格的控制分析**：实验设计包含了一系列巧妙的控制分析，有力地排除了视觉、记忆、任务难度、特征空间结构等混淆因素的干扰，极大地增强了核心结论的说服力。
*   **发现关键脑区**：精确地将**左侧 55b 区**确定为语言和数学共享表征的核心节点，并勾勒出其动态连接模式，为后续研究提供了明确的靶点。
*   **分析方法的全面性**：从预测准确性、模型权重相关、主成分分析到功能连接，进行了多维度、多层次的表征分析，全面而深入地刻画了神经表征的共性与特性。

## 8. 不足与局限

*   **刺激结构的局限性**：研究使用的语言和数学刺激结构相对简单且有限（如数学表达式仅包含两个运算符），生态效度不足，结论能否推广到更复杂的自然语言对话或高级数学推理中尚待考察。
*   **认知因素未完全分离**：虽然排除了低级视觉和工作记忆，但右侧 PF 区等部分跨领域区域可能还与注意力、符号操作等通用领域认知过程有关，其贡献未能彻底分离。
*   **模型的“黑箱”性质**：虽然利用 LLM 成功预测了脑活动，但 LLM 内部表征的机制与大脑的真实计算过程并非完全一致，两者间的对齐机制仍有待深入探索。研究明确声明 LLM 仅作为特征提取器，而非大脑的计算模型。
*   **功能连接的因果性不明**：功能连接分析揭示了相关性，但无法确定脑区之间是否存在直接的因果交互关系。

（完）
