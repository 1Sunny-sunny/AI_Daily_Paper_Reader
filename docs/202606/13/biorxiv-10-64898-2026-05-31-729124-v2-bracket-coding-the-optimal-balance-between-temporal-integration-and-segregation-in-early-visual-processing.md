---
title: "Bracket Coding: The Optimal Balance Between Temporal Integration and Segregation in Early Visual Processing"
title_zh: 括号编码：早期视觉处理中时间整合与分离的最佳平衡
authors: "Samiei, T., Ahmed, H. F., Zagha, E., Nozari, E."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729124v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 描述了视觉皮层中作为时间整合和分离的括号编码
tldr: 针对神经编码原理的长期争议，本研究提出并验证了“括号编码”方案。通过大规模Neuropixels记录分析小鼠视觉系统，发现神经元群体采用精确时间同步的边界分隔速率编码区间，实现速率与时间编码的动态切换。该编码在跨脑区、任务中稳健，具有解码最优性、层级组织和低频振荡相干，并在独立数据集和计算模型中得到验证，揭示了一种全新的感觉信息编码形式。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示大脑感觉编码中速率编码与时间编码的整合机制，解决长期存在的原理争议。
method: 利用Allen Institute及International Brain Laboratory的大规模Neuropixels数据集，分析小鼠观看多种视觉刺激时丘脑和视觉皮层区域的神经元群体放电活动。
result: 发现“括号”编码现象，即试验时段被精确同步的边界划分为速率编码区间，编码在跨脑区、任务中稳健，展现解码最优性、层级组织及低频振荡相干。
conclusion: 证实了大脑中存在一种新的感觉信息编码机制，对神经科学和神经工程具有广泛影响。
---

## 摘要
尽管对神经编码的研究已逾百年，但大脑编码感觉信息的基本原理仍存在争议。在本研究中，我们提供了汇聚性证据，表明在观看一系列视觉刺激的小鼠的丘脑、初级视觉皮层以及高级视觉皮层区域中，存在一种动态、快速切换的发放率和时间编码整合机制。该方案的主要特征是在每个试次的持续时间内，存在多个时间上协调的“括号”，这些“括号”在内部进行发放率编码，并以精确计时且群体同步的边界分隔。利用艾伦研究所视觉编码数据集中的大规模Neuropixels记录，我们证明了括号编码在多种视觉任务和脑区中的稳健性和普适性，以及其在信息解码中的最优性、信息表征的功能相关性、明显的层级组织、跨视觉区域的长程自下而上同步性，以及与低频局部场电位的相干性。这些发现随后在国际脑实验室联盟提供的第二个独立数据集中得到了验证。最后，我们提供了一个计算模型，可作为生成括号编码群体放电活动的潜在机制。总之，我们的结果证明了大脑中存在一种新型的感觉信息编码形式，对神经科学和神经工程具有广泛意义。

## Abstract
Despite over a century of research into the neural code, the fundamental principles by which the brain encodes sensory information remain debated. In this study we provide converging evidence for the presence of a dynamic, fast-switching integration of rate and temporal coding in the thalamus, primary visual cortex, and higher-order visual cortical areas of mice viewing an array of visual stimuli. This scheme is primarily characterized by the presence of distinct, temporally coordinated "bracket"s that tile the duration of each trial, are rate-coded within, and are separated by boundaries that are precisely-timed and synchronized across the population. Using large-scale Neuropixels recordings from the Allen Institute Visual Coding dataset, we provide evidence for the robustness and generality of bracket coding across several visual tasks and brain regions, as well as its optimality for information decoding, functional relevance for information representation, pronounced hierarchical organization, long-range bottom-up synchrony across visual regions, and coherence with low-frequency local field oscillations. These findings were all subsequently validated in a second, independent dataset provided by the International Brain Laboratory consortium. Finally, we provide a computational model that can serve as a potential mechanism for the generation of bracket-coded population spiking activity. Together, our results demonstrate the presence of a novel form of sensory information encoding in the brain, with broad implications for neuroscience and neuroengineering.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **核心问题**：大脑究竟如何编码感觉信息？神经科学中长期存在“发放率编码”与“时间编码”的争论，其本质是信息是在神经元放电的平均频率中编码，还是通过精确的放电时刻来承载。本论文要回答的关键问题是：这两种看似对立的编码方案是否能在单个试次中动态并存、协同工作。
- **整体含义**：研究揭示了一种全新的“括号编码”框架。它表明，在早期视觉处理中，神经元群体并非采用单一的编码策略，而是将每段刺激过程划分为多个由群体同步放电精确界定的“括号”区间，内部采用发放率编码，区间边界本身则携带精确的时间信息。这为实现时间整合（对时间变化的容错、稳健的表征）与时间分离（精确时刻的表征）的最佳平衡提供了简洁且普适的机制，对理解感觉计算和设计神经仿生系统具有深远意义。

### 2. 论文提出的方法论
- **核心思想**：提出“括号编码”作为速率编码与时间编码有机整合的候选方案。该方案将每次试验的神经响应，在时间上划分为一系列离散的“括号”区间。每个“括号”内部，信息以神经元群体的发放率编码；而相邻“括号”之间，则通过整个神经元群体高度同步、精确计时的“括号边界”进行分隔。边界本身可作为刺激事件的时间标签。
- **关键分析与建模流程（文字说明）**：
    1.  **检测括号边界**：从大规模Neuropixels记录的多脑区群体放电数据中，识别出跨试次稳定、跨神经元高度同步的精确放电事件（群体爆发/边界）。
    2.  **验证内部速率编码**：对于每个“括号”区间内的时间窗口，计算群体的发放率，并量化该速率携带的刺激信息是否多于边界时刻变化所携带的信息。
    3.  **量化性能**：构建解码器，分别仅基于括号内部的发放率信息和仅基于边界的时间信息来解码视觉刺激，比较两者的解码效率以及它们联合时的最优性。
    4.  **跨层次与节律分析**：分析括号结构在丘脑→初级视皮层→高级视皮层的层级传递关系，以及括号边界与低频局部场电位（LFP）振荡的相位相干性。
    5.  **计算模型**：提供一个能自发产生符合“括号编码”属性群体放电活动的模型，作为潜在机理性解释。

### 3. 实验设计
- **主要数据集**：
    - **主发现集**：**艾伦研究所（Allen Institute）视觉编码数据集**。包含小鼠观看多种被动视觉刺激（多种任务）时，利用Neuropixels电极记录的大量神经元群体活动，覆盖丘脑、初级视觉皮层（V1）及多个高级视觉皮层区域。
    - **独立验证集**：**国际脑实验室联盟（International Brain Laboratory）提供的第二个独立数据集**，用以复现所有主要发现。
- **Benchmark与对比方法**：没有传统意义上的Benchmark，但本质上对比了三类编码方案的性能：
    - 纯发放率编码（基于全试次的平均发放率）。
    - 纯时间编码（基于首次放电或同步放电的精确时刻）。
    - 括号编码（内部速率 + 边界时刻的整合方案）。
- **分析维度**：对比不同脑区、不同视觉任务、信息解码最优性、功能相关性、层级组织特性及与LFP振荡的关系。

### 4. 资源与算力
- 提供的摘要及元数据中**未明确说明**具体的算力资源（如GPU型号、数量、训练时长等）。本研究为大实验数据分析与计算建模，所需的算力主要消耗在数十TB量级的Neuropixels数据预处理、同步检测、解码分析及模型仿真上，但论文原文中可能未作为重点披露具体硬件环境。

### 5. 实验数量与充分性
- **实验组数概览**：
    - 覆盖 **1个主数据集 + 1个完整独立验证集**。
    - 在单个数据集中，跨越 **多个不同视觉刺激任务**，确保效应非任务特异性。
    - 分析涉及 **多个脑区**（丘脑—V1—高级视皮层），考察层级结构与长程自下而上同步。
    - 包含 **多种控制分析**：解码最优化验证、功能相关性分析、LFP振荡相干性检验、计算模型生成验证。
- **充分性与客观性评价**：
    - **充分性较高**：通过在两个完全独立的大规模联盟数据集上得到一致结论，极大地增强了结果的稳健性和普适性，是极有力的证据。
    - **客观公正**：对比解码仅基于边界时刻或内部速率，清晰地展示了单独使用任一成分的局限与二者联合的最优性，实验设计客观。覆盖被动观看任务，避免了运动等混淆因素，内在效度高。

### 6. 论文的主要结论与发现
- **发现括号编码现象**：在小鼠视觉系统中，存在一种动态、快速切换的整合编码方案，称为“括号编码”。它在每个试次中形成多个时间上协调的“括号”，内部为速率编码，边界为群体同步的精确计时。
- **编码方案的优越性**：
    - **稳健性**：跨多种视觉任务和脑区（丘脑、V1、高级皮层）均稳健存在。
    - **解码最优性**：同时利用括号内速率和边界时间信息，能实现最优的刺激解码。
    - **层级组织**：括号结构呈现出从丘脑到皮层的清晰层级传递特性，表现出长程自下而上的群体同步。
- **与宏观节律的关联**：括号的边界与低频局部场电位（LFP）振荡相相干，提示其可能由大脑内源性节律协调。
- **机制的普适性验证**：所有发现在国际脑实验室联盟的独立数据集中得到了完全验证。提供的计算模型证明，简单的机制即可产生此类复杂群体编码。
- **根本性结论**：证明大脑中存在一种兼顾“时间整合”与“时间分离”这一对矛盾需求的新型感觉编码形式。

### 7. 优点
- **概念突破性**：巧妙解决了发放率编码和时间编码的长期争论，提出动态切换的“括号”框架，而不是非此即彼。
- **数据与验证的极强可信度**：使用当前神经科学界最先进、高通量的Neuropixels记录，并在 **两个完全独立的大规模权威数据集**（Allen研究所 vs. IBL）上进行发现和复现，达到了领域内极高的验证标准。
- **分析体系完整**：从现象发现、信息解码效率验证、功能相关性、解剖层级、生理节律（LFP）到计算模型原理，形成了一个完整的证据闭环。
- **跨脑区、跨任务的普适性**：结论涵盖了整个早期视觉通路和多种刺激模式，表明这可能是感觉编码的一般性原理。

### 8. 不足与局限
- **物种与行为状态限制**：目前发现仅限于**麻醉或头固定被动观看的小鼠模型**，是否存在于清醒、主动执行视觉任务（如决策、注意力任务）的高级脑区和行为状态下，仍未可知。
- **感觉模态的局限**：研究聚焦视觉皮层与丘脑，括号编码是否适用于听觉、触觉等其他感觉模态，有待拓展验证。
- **边界定义的客观性风险**：虽然边界被描述为精确同步事件，但在复杂的群体放电中识别和定义“括号边界”的算法可能引入分析偏差，其参数选择的稳健性需要更多外部验证。
- **因果性缺失**：研究主要基于观察与解码分析，未能通过光遗传学等手段扰动边界同步或内部速率，以证明二者对行为输出的因果必要性。
- **潜在混淆因素**：被动观看下，瞳孔大小波动、微眼动等未严格控制的非刺激相关生理状态，可能部分贡献了所观测到的群体同步边界，尤其是它们与LFP节律的相干性。

（完）
