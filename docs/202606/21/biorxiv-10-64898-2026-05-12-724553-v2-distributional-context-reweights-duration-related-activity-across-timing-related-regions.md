---
title: Distributional context reweights duration-related activity across timing-related regions
title_zh: 分布性情境重新加权跨时间相关脑区的时长相关活动
authors: "Baykan, C., Cheng, S., Shi, Z."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.12.724553v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: fMRI研究解码不同情境下与持续时间相关的神经活动模式
tldr: 时间知觉中，近期经验时长统计（分布上下文）如何影响脑活动尚不明确。本研究用fMRI和视觉时间二分任务，考察短时长与长时长偏向两种上下文下时长判断的神经机制。发现分布上下文重塑了多个时间加工脑区（如左侧岛叶、SMA/pre-SMA）的时长相关活动权重，而非调用独立系统。行为上，上下文仅偏移主观判断，不改变精度。表明大脑通过对已有计时区域活动进行重新加权来适应环境统计概率。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究分布上下文（近期时长经验统计）如何在人脑计时相关区域中影响时长判断的神经表征。
method: 采用功能磁共振成像（fMRI），让24名参与者在短时长偏向和长时长偏向两种分布上下文条件下执行视觉时间二分任务。
result: 行为上，上下文偏移了主观时长判断但不影响时间精度；神经上，左侧岛叶在短偏向上下文呈现更强的时长调制，SMA/pre-SMA活动表现出上下文特异的不对称性，且连接分析显示上下文调制了时长相关的功能耦合。
conclusion: 分布上下文通过对既有计时相关脑区的活动重新加权来影响时长判断，而非招募新的独立计时系统。
---

## 摘要
时长判断由近期时间经验的统计信息进行校准，但情境影响在人类时间相关脑区中如何表达尚不清楚。我们使用功能磁共振成像，让24名参与者在两种分布性情境下执行视觉时间二分任务：一种偏向较长时长，另一种偏向较短时长。行为上，分布性情境改变了主观时长判断，但未改变时间精度，这与先验相关的偏差一致。神经上，时长相关的BOLD响应在不同先验时间脑区随情境变化。最清晰的区域特异性证据是，在短偏向情境中，左侧脑岛的时长调制更强。辅助运动区/前辅助运动区对更广泛的时间网络模式有贡献，并且其特定情境的不对称性对时长回归因子的对齐敏感。以辅助运动区为种子点的探索性连通性分析提供了汇聚证据，表明情境还调制了时长相关的与时间及注意相关脑区的耦合。综上，这些发现表明，分布性情境在时长判断过程中影响了既定时间相关脑区的相对权重，而非招募解剖学上分离的时间系统。

## Abstract
Duration judgments are calibrated by the statistics of recent temporal experience, but how this contextual influence is expressed across human timing-related brain regions remains unclear. We used functional MRI while 24 participants performed a visual temporal bisection task under two distributional contexts: one biased toward longer durations and one biased toward shorter durations. Behaviorally, distributional context shifted subjective duration judgments without changing in temporal precision, consistent with a prior-related bias. Neurally, duration-related BOLD responses varied across a priori timing regions as a function of context. The clearest region-specific evidence was stronger left-insula duration modulation in the short-biased context. SMA/pre-SMA contributed to the broader timing-network pattern, and its context-specific asymmetry was sensitive to the alignment of the duration regressor. Exploratory SMA-seeded connectivity analyses provided converging evidence that context also modulated duration-related coupling with timing- and attention-related regions. Together, these findings indicate that distributional context impacts the relative weighting of established timing-related regions during duration judgments, rather than recruiting anatomically separate timing systems.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究问题**：时长知觉不仅依赖于物理时间，还会受到近期经验中时长统计分布（分布性情境）的校准，但这种情境影响如何在人脑计时相关脑区中表达，此前并不清楚。
- **整体含义**：本研究试图揭示大脑是通过“重新加权”既有的计时网络活动来适应环境统计规律，还是调用一套解剖上分离的新计时系统。结果表明，分布性情境通过改变已有计时脑区（如岛叶、辅助运动区/前辅助运动区）的相对活动权重，而非招募独立系统，来影响时长判断。

### 2. 论文提出的方法论

- **核心思想**：在受控的时长分布情境下，使用功能磁共振成像（fMRI）记录全脑BOLD信号，并通过时长调制分析、感兴趣区（ROI）分析和功能连接分析，考察不同情境如何重塑时长相关的神经活动。
- **关键技术细节与流程**：
  - **视觉时间二分任务**：被试需判断当前呈现的视觉刺激时长更接近长或短标准。操纵刺激呈现的时长分布，形成“短时长偏向”和“长时长偏向”两种分布性情境。
  - **行为建模**：分析主观相等点（PSE）和判断精度（如韦伯分数），检验情境对偏差和精度的分离影响。
  - **fMRI数据分析**：
    - 构建一般线性模型（GLM），纳入时长作为回归因子，估计各体素的时长调制效应（如 $ \beta_{\text{duration}} $）。
    - 比较两种情境下时长调制效应的差异（情境 $ \times $ 时长交互作用），定位受情境显著调制的脑区。
    - **ROI分析**：基于先验计时相关脑区（如左侧岛叶、SMA/pre-SMA）提取信号，检验情境特异性的时长调制模式。
    - **探索性功能连接分析**：以SMA为种子点，计算情境调制的时长相关心理生理交互（PPI），考察情境如何改变计时脑区与其他脑区（如注意相关区域）的功能耦合。

### 3. 实验设计

- **被试**：24名健康成人参与者。
- **实验场景与任务**：
  - 采用视觉时间二分任务，刺激为视觉呈现的某一持续时长。
  - 操纵“短偏向分布”和“长偏向分布”两种条件：在短偏向情境中，大部分刺激时长更短；长偏向情境则相反。
- **对比策略**：该研究为被试内设计，核心对比是两种分布性情境下的行为和神经活动差异，未与外部独立方法或模型进行横向 benchmark 比较。
- **数据集**：仅为该研究采集的专有fMRI数据集，未使用公开数据库。

### 4. 资源与算力

- 论文文本中**未明确说明**所使用的计算资源（如GPU型号、数量、训练时长）。该研究为人类fMRI实验，主要依赖磁共振扫描仪和标准神经影像分析软件（如SPM、FSL或AFNI），计算负载集中于统计建模而非深度学习，因此通常不涉及大规模GPU计算请求。文中未提供算力相关信息。

### 5. 实验数量与充分性

- **实验层级与数量**：
  - **主要实验**：一组（24人）在两种情境下完成行为与fMRI扫描，对应行为对比、全脑GLM交互分析、ROI分析及连接分析。
  - **分析维度**：包含行为层、单变量激活层（全脑和ROI）和功能连接层（PPI），构成多层次的汇聚证据。
- **充分性与客观性评价**：
  - 实验设计采用被试内操纵，控制了顺序效应等混淆，提高了统计效力。
  - 样本量（24人）属于典型fMRI研究规模，但绝对数量偏小，可能限制群体推断的稳健性。
  - 未提及独立的复制实验或留出验证集；亦未见严格意义上的消融实验（如移除某一情境或脑区验证因果性）。
  - 总体实验设计较严谨、分析路径清晰，能达成论文目标，但更大样本或外部验证将进一步提升证据强度。

### 6. 论文的主要结论与发现

- **行为层面**：分布性情境显著偏移了主观时长判断（短偏向情境下更倾向于判断为“长”），但未改变时间判断的精度（灵敏度），符合贝叶斯框架下先验分布引起的偏差推断。
- **神经层面**：
  - 左侧岛叶在短偏向情境下表现出更强的时长调制活动，提示其在“短时间环境”中对时长信息的权重增强。
  - 辅助运动区/前辅助运动区（SMA/pre-SMA）的活动呈现情境特异的不对称性，且这种不对称性对时长回归因子的对齐方式敏感，可能反映计时网络动态重组。
  - 以SMA为种子点的功能连接分析显示，分布性情境调制了SMA与计时及注意相关脑区之间与时长相关的功能耦合。
- **总体结论**：大脑并非招募一套全新脑区来处理不同情境下的时间判断，而是通过**重新加权**已有计时脑区（如岛叶、SMA/pre-SMA）的活动和它们之间的连接强度，来实现对环境时长统计规律的适应。

### 7. 优点

- **机制解释明确**：将行为层面的“先验偏差”与神经层面的“区域权重重分配”直接挂钩，超越了对激活区域的简单定位。
- **多模态证据汇聚**：结合行为、单变量激活和功能连接三种分析，一致指向“重加权”解释，增强了结论的可靠性。
- **目标明确的实验操纵**：通过对称地操纵短偏向和长偏向分布，有效分离了情境对偏差和精度的影响，设计简洁有力。
- **关注先验计时网络**：基于先验假设选取ROI，避免了纯粹数据驱动的探索可能带来的假阳性，同时揭示了区域特异性的调制模式。

### 8. 不足与局限

- **样本量相对较小**：24名被试可能不足以稳定检测较微弱的交互效应，也不利于考察个体差异与行为的相关。
- **缺乏因果性证据**：fMRI提供的仅为相关性证据，无法断定岛叶或SMA的“重加权”是导致行为变化的直接原因（需TMS或病损研究补充）。
- **情境生态效度有限**：实验室中用显式二分任务和极端时长分布来诱导情境，与现实生活中逐步积累的时间统计经验可能不同。
- **分析未预注册**：摘要未提及分析流程是否预注册，无法完全排除多重比较和选择性报告的风险（作为预印本尚可理解）。
- **通用性局限**：仅采用视觉模态和二分任务，结论能否推广到听觉计时或其他计时范式（如时间产生、复现）尚需验证。

（完）
