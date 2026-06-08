---
title: Working Memory as Programmable Fast Weight Computation
title_zh: 工作记忆作为可编程快速权重计算
authors: "Jiang, L., Zhu, Y., Liu, J."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729709v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 猕猴前额叶工作记忆的神经几何与递归快速权重模型
tldr: 为探究工作记忆存储与检索的统一机制，本研究结合猕猴背外侧前额叶神经活动几何分析及计算模型，发现记忆几何在延迟期动态重组，并利用循环快速权重程序员模型重现该过程，揭示了突触状态写入、突触动力学组织与读出查询的计算原理，表明工作记忆是一种可编程快速权重计算，且与Transformer架构共享临时记忆的算法原则。
source: biorxiv
selection_source: fresh_fetch
motivation: 工作记忆如何在感官输入消失后存储信息并以任务相关格式检索的统一机制尚不清楚。
method: 结合猕猴视空间延迟匹配样本任务中的神经几何分析，与循环快速权重程序员模型进行仿真。
result: 记忆位置几何在样本呈现时强烈表达，早期延迟退化，需求前在部分独立子空间重现，模型复现了此动态并揭示了突触写入、动力学组织与读出查询机制。
conclusion: 生物工作记忆与Transformer家族架构均遵循可编程临时记忆的算法原理，提供了存储与检索的统一理论。
---

## 摘要
工作记忆在感觉输入消失后存储信息，随后以任务相关格式进行检索，但统一存储与检索的机制仍不清楚。在这里，我们将猕猴背外侧前额叶皮层在视觉空间延迟匹配样本任务中的神经几何分析与计算建模相结合，以检验工作记忆是否可以实现为循环快速权重计算。我们发现，记忆位置的关联几何在样本呈现期间强烈表达，在早期延迟期间退化，并在需要之前以部分不同的助记子空间重新出现。一个循环快速权重编程器模型，实现了一种与线性Transformer计算密切相关的动态快速权重记忆，再现了这些潜在到助记的动力学。模型的直接检查和扰动揭示，神经活动将刺激信息写入可快速修改的突触状态，突触动力学随时间组织这种潜在记忆，循环读出查询不断演变的状态以产生任务相关活动。这些发现为工作记忆的存储和检索提供了统一解释，并表明生物工作记忆和Transformer系列架构共享一种可编程临时记忆的算法原理。

## Abstract
Working memory (WM) stores information after sensory input disappears and later retrieves it in a task-relevant format, but the mechanism unifying storage and retrieval remains unclear. Here we combine neural geometry analyses of macaque dorsolateral prefrontal cortex activity during a visuospatial delayed-match-to-sample task with computational modeling to test whether WM can be implemented as recurrent fast-weight computation. We found that the relational geometry of remembered locations was strongly expressed during sample presentation, degraded during the early delay, and reemerged before requirement in a partially distinct mnemonic subspace. A recurrent fast-weight programmer model, which implements a form of dynamic fast-weight memory closely related to linear Transformer computation, reproduced these latent-to-mnemonic dynamics. Direct inspection and perturbation of the model revealed that neural activity writes stimulus information into rapidly modifiable synaptic states, synaptic dynamics organize this latent memory over time, and recurrent readout queries the evolving state to generate task-relevant activity. These findings provide a unified account of WM storage and retrieval and suggest that biological WM and Transformer family architectures share an algorithmic principle of programmable temporary memory.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **核心问题**：工作记忆如何在没有感觉输入的情况下存储信息，并在后续时刻以任务相关的格式进行检索？即存储与检索的统一机制究竟是什么？
- **研究背景**：工作记忆是认知系统的核心功能，经典理论多将维持性放电视为存储载体，但对如何动态编码关系信息、记忆表征为何在延迟期内不直接可用却在需要时重现等问题缺乏统一解释。近年来，快速权重（fast weight）计算和Transformer类架构在人工序列建模中取得成功，但其与生物工作记忆的算法同源性尚不明确。
- **整体含义**：该工作试图为生物工作记忆提供一个算法级别的计算解释，并揭示其与人工临时记忆架构（如线性Transformer）共享“可编程快速权重计算”这一基本原理。

### 2. 论文提出的方法论
- **核心思想**：将工作记忆视为一种循环快速权重计算，其中神经活动将刺激信息写入可快速修改的突触权重（fast weight），突触动力学在延迟期组织潜在记忆（latent memory），循环读出查询（recurrent readout query）不断访问演化的突触状态以生成任务相关活动。
- **关键技术细节**：
  - 生物端：分析猕猴背外侧前额叶皮层（dlPFC）在视空间延迟匹配样本（DMS）任务中的神经群体活动几何结构。
  - 模型端：构建并训练**循环快速权重编程器模型**（Recurrent Fast-Weight Programmer, R-FWP）。该模型动态更新快速权重矩阵，其形式与线性 Transformer 中的键-值注意力更新紧密相关。模型包含：
    - 写入阶段：神经活动将感觉输入转换为权重更新。
    - 存储阶段：突触状态（快速权重）按自身内在动力学演变，形成隐蔽的记忆表征。
    - 读出阶段：循环信息流根据当前突触状态查询并产生输出。
  - 对比分析：将模型产生的神经活动几何与真实神经数据几何进行定性、定量比较；通过对模型的直接检查和扰动实验（突触屏蔽、读出解耦等）验证机制。
- **算法流程概述**（文字描述，非公式）：输入样本 → 神经活动编码 → 更新快速权重 → 延迟期快速权重自主演化 → 匹配测试时读出网络以任务要求的形式检索信息。整个动力学可被形式化为类似线性自注意力的计算图式。

### 3. 实验设计
- **生物数据来源**：猕猴在视空间延迟匹配样本任务中背外侧前额叶皮层的多通道电生理记录。
- **分析基准**：记忆位置的关系几何（relational geometry）在表征空间中的动态变化，具体包括样本期、延迟早期和匹配前的神经种群几何结构。
- **对比方法**：
  - 将 R-FWP 模型产生的伪神经活动的几何动态与真实神经数据对比。
  - 模型变体消融（如去除快速权重写入、动力学组织或循环读出），观察几何重现的失败。
  - 讨论与标准储存类模型（如维持性吸引子模型）以及 Transformer 类架构的异同。
- **实验场景**：单一的视空间 DMS 任务范式，未报告跨任务泛化或多脑区对比。

### 4. 资源与算力
- 提供的摘要与元数据中**未明确说明**模型训练所使用的具体硬件（GPU型号、数量）或训练时长。由于原文是计算建模与神经数据分析的结合，可能不涉及大规模深度学习训练；模型规模或算力需求或非本文重点。

### 5. 实验数量与充分性
- 从摘要可见的实验组：
  1. 神经数据几何分析：样本期、延迟期（早期/晚期）、匹配前的几何测量。
  2. R-FWP 模型的模拟重现实神经几何动力学。
  3. 模型直接检查：突触写入、存储动力学、读出查询的可视化或统计验证。
  4. 扰动实验（消融）：破坏快速权重、动力学或读出环节以观察记忆表征的崩溃。
- **充分性评估**：
  - 从概念验证角度，实验设计紧凑且因果性强（扰动验证机制）。
  - 但任务单一（视空间DMS），缺乏跨范式、跨物种、跨脑区的系统比较。
  - 与基线模型的对比（如经典吸引子网络、纯前馈序列模型）在该摘要中未详细列明，可能需查看全文以判断公平性。

### 6. 论文的主要结论与发现
- 记忆位置的关系几何在样本呈现时强烈表达，随后在延迟早期“消退”（隐蔽状态），到需要匹配前又重新出现在部分独立的助记子空间中。
- R-FWP 模型成功重现了这一“潜伏-重现”（latent-to-mnemonic）动力学，并揭示：
  - 神经活动将感觉信息**写入**可快速修改的突触权重。
  - 突触状态的**内在动力学**随时间组织此潜在记忆。
  - 循环**读出**查询动态演化的突触状态，以产生任务恰当的响应。
- 生物工作记忆与 Transformer 家族架构在算法层面共享**可编程临时记忆**原理，为工作记忆的存储与检索提供了统一解释。

### 7. 优点
- **理论新颖性**：首次将快速权重程序化记忆的概念直接对应到前额叶神经动力学，提供存储与检索的统一机制。
- **因果验证**：不仅做描述性神经-模型相似性，还通过模型扰动实验确认机制的必要性。
- **跨域链接**：在生物认知和机器智能（Transformer）之间架设了算法级同构，启发性强。

### 8. 不足与局限
- **任务范围窄**：仅验证单个视空间 DMS 范式，机制在其他工作记忆任务（语音、特征绑定、操作记忆）中的普遍性有待检验。
- **模型生物真实性局限**：快速权重实现形式是否对应生物脑中突触可塑性的具体形式（如短期可塑性）仍悬而未决，摘要未讨论生物合理性约束。
- **分析深度未知**：摘要中未报告效应量、试次数、跨动物变异性等统计细节，实验稳健性需查看全文。
- **缺失细节**：未给出模型训练的损失函数、优化方法、网络规模等，可复现性受限。
- **预印本性质**：该文发表于 biorxiv，尚未经同行评审，结论需谨慎引用。

（完）
