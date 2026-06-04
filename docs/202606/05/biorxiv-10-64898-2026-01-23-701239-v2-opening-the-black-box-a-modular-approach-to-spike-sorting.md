---
title: "Opening the black box: a modular approach to spike sorting"
title_zh: 打开黑箱：一种模块化的脉冲分类方法
authors: "Garcia, S., Halcrow, C., Windolf, C., McKenzie, Z. M., Adkisson-Floro, P., Mayorquin, H. R., Dichter, B. K., Buccino, A. P., Yger, P."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.23.701239v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 模块化尖峰排序提取单个神经元尖峰模式
tldr: 随着高密度神经探针的普及，spike sorting变得日益耗时且计算昂贵，现有工具多为黑箱，难以分离各算法步骤的影响。本研究提出模块化通用框架，可独立基准测试峰检测、特征提取、聚类和模板匹配等关键步骤。基于此框架构建的组件式sorter在模拟数据上超越Kilosort 4，在真实数据上表现相当，并揭示探针物理运动是主要瓶颈，为社区贡献和灵活构建端到端方案提供了基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有spike sorting工具作为黑箱难以评估单个算法步骤的性能，限制了优化和社区协作。
method: 开发模块化框架，利用快速生物物理模拟生成真实可靠的基准数据，对spike sorting各步骤进行独立评估和组装。
result: 组件式spike sorter在密集大型模拟记录上优于Kilosort 4，在真实数据上产生类似定量结果，并发现探针物理运动是所有流程中的核心瓶颈。
conclusion: 模块化框架降低了贡献门槛，提供了灵活构建端到端解决方案的能力，有望推动spike sorting领域的社区参与和技术进步。
---

## 摘要
脉冲分类是一种从细胞外电生理记录中提取单个神经元活动的算法过程。随着高密度探针（如Neuropixels）的使用日益增加，这一关键处理步骤正变得越来越耗时且计算成本高昂。尽管已有许多软件工具被提出用于脉冲分类，但它们通常被构建和基准测试为单一的“黑箱”，使得难以分离出各个算法步骤对最终结果的影响，尤其是在数据集和参数变化时。为解决这一问题，我们开发了一个模块化的通用框架，用于开发、基准测试和组装当前最先进的脉冲分类算法中的关键计算步骤。基于快速且高效的生物物理合理记录的基准真值生成，我们展示能够单独基准测试并精确量化脉冲分类流程（即峰值检测、特征提取与聚类、模板匹配）中不同步骤的性能。随后，我们利用这些结果构建了一个模块化、基于组件的脉冲分类器，在密集的大型模拟记录上能够优于Kilosort 4，并在真实数据上产生相似的定量结果。此外，我们发现所有现代脉冲分类流程的主要瓶颈在于探头的物理移动，无论采用何种漂移校正策略。此处提出的基于组件的脉冲分类框架，通过降低贡献门槛并提供一个灵活而强大的框架来构建端到端的脉冲分类解决方案，有望促进该领域的社区参与。

## Abstract
Spike sorting is an algorithmic process that extracts the activity of individual neurons from extracellular electrophysiology recordings. With the ballooning use of high density probes, such as Neuropixels, this essential processing step is increasingly becoming time consuming and computationally expensive. Although many software tools have been proposed to address spike sorting, they are usually constructed and benchmarked as monolithic "black boxes", making it difficult to factor out the effects of individual algorithmic steps on the final outcome, especially when varying datasets and parameters. To address this issue, we developed a modular and common framework to develop, benchmark and assemble the key computational steps that are used in state-of-the-art spike sorting algorithms. Relying on fast and efficient ground truth generation of biophysically plausible recordings, we show that we are able to individually benchmark and precisely quantify the performance of different steps in a spike sorting pipeline (i.e. peak detection, feature extraction and clustering, and template matching). We then leverage these results to create a modular, component-based spike sorter that can outperform Kilosort 4 on dense and large simulated recordings and produce similar quantitative results on real data. In addition, we find that the major bottleneck of all modern spike sorting pipelines is in the physical motion of probes, regardless of the drift-correction strategy. The component-based spike sorting framework presented here has the potential to foster community engagement in the field by lowering the barrier to contributions and providing a flexible yet powerful framework to construct end-to-end spike sorting solutions.