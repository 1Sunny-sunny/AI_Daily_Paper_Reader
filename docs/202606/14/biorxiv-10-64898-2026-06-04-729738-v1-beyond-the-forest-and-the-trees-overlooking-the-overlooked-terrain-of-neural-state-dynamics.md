---
title: "Beyond the Forest and the Trees: Overlooking the Overlooked Terrain of Neural State Dynamics"
title_zh: 超越森林与树木：重审神经状态动力学中被忽视的地形
authors: "Asai, T., Kashihara, S., Chiyohara, S."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.729738v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 神经状态动态状态转移方法时间度量
tldr: 传统 EEG 微状态分析严重依赖模板定义，导致可重复性差和跨研究比较困难。本文从拓扑几何视角重新审视该问题，将微状态模板视为状态空间中的地标而非聚类中心，保留电压图极性作为有意义的几何关系，重新将微状态定义为连续神经状态地形的离散代表。实验表明，地标方法比传统模板更能捕捉状态结构，为神经动态分析提供了更稳定、可比较的基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统 EEG 微状态分析严重依赖模板定义，导致可重复性差和跨研究比较困难。
method: 采用拓扑几何视角，将微状态模板视为状态空间中的地标，保留电压图极性，通过全局相似性构建状态空间并找出主导轴的离散代表。
result: 基于地标的定义相比传统模板能更好地捕捉状态结构并提高分析性能。
conclusion: 从模板转向地标为微状态分析提供了更原则和稳定的基础，可扩展到 fMRI 等其他模态。
---

## 摘要
状态转换方法，包括脑电图微状态分析及相关的功能磁共振成像方法如隐藏马尔可夫模型（HMM）和共激活模式（CAP）分析，为将神经动力学粗粒化为一小组准稳定状态提供了广泛使用的工具。其效用已在静息态和任务范式中得到证实，并被广泛应用于认知神经科学乃至精神疾病与神经系统疾病的候选生物标志物。然而，一个根本性的局限依然存在：几乎所有下游时间度量都依赖于初始定义的模板图。在传统流程中，模板通过对全局场强（GFP）峰值处电压图进行极性不变聚类得到，这使得最终的状态定义对预处理、采样、初始化、聚类算法以及聚类数选择十分敏感。因此，该方法虽能捕捉脑电图动力学中的粗略规律，但仅微弱约束了涌现这些状态的更大几何组织。这种模板依赖性对结果的可重复性以及跨研究和脑电图帽系统的比较构成了重大挑战。本文从拓扑-几何视角重新审视该问题。我们不再将模板视为从全局场强峰值图提取的聚类中心，而是将其视作嵌入状态空间全局结构中的地标，该状态空间由头皮电压图之间的相互相似性构建而成。在此表述下，微状态模板被重新发现为组织连续神经状态地形的优势轴的离散代表。这种重构保留了极性作为有意义的几何关系，而非一开始就作为分析冗余加以消除，同时将注意力从孤立的状态标签转向状态空间本身的地形：即更广泛的关系结构，其中局部状态得以解释。通过该方法，我们证明基于地标的状态定义在捕捉状态结构和提升分析性能上优于传统模板。这些发现表明，脑电图微状态分析的核心问题不止于聚类优化，更在于如何为连续动力学的粗粒化定义有效节点，而不丢弃组织其结构的拓扑特征。通过将微状态分析的概念基础从模板转向地标，本文所提方法为状态定义（包括在功能磁共振成像中）提供了更具原则性且可能更稳定的基础。这种拓扑-几何的重新评估拓展了传统微状态分析，为跨数据集、范式和记录系统的更统一比较开辟了路径。

## Abstract
State-transition approaches, including EEG microstate analysis and related fMRI methods such as hidden Markov models (HMMs) and co-activation pattern (CAP) analysis, provide widely used tools for coarse-graining neural dynamics into a small set of quasi-stable states. Its utility has been demonstrated across resting-state and task paradigms, with broad applications ranging from cognitive neuroscience to candidate biomarkers for psychiatric and neurological disorders. A fundamental limitation remains, however: nearly all downstream temporal measures are conditional on the template maps defined at the outset. In the conventional pipeline, templates are derived from polarity-invariant clustering of voltage maps at global field power (GFP) peaks, making the resulting state definitions sensitive to preprocessing, sampling, initialization, clustering algorithms, and the choice of cluster number. Consequently, the method captures coarse regularities in EEG dynamics, while only weakly constraining the larger geometric organization from which those states emerge. This template dependence poses a major challenge for reproducibility and for comparisons across studies and EEG caps. Here, we revisit this problem from a topological-geometric perspective. We treat templates not as cluster centroids extracted from GFP-peak maps, but as landmarks embedded in the global structure of a state space constructed from mutual similarities among scalp voltage maps. In this formulation, microstate templates are rediscovered as discrete representatives of dominant axes that organize continuous neural-state topography. This reformulation preserves polarity as a meaningful geometric relation instead of eliminating it at the outset as analytical redundancy. It also shifts attention from isolated state labels to the terrain of the state space itself: the broader relational structure within which local states become interpretable. Using this approach, we show that landmark-based state definitions outperform conventional templates in capturing state structure and improving analytical performance. These findings suggest that the central problem in EEG microstate analysis is broader than clustering optimization: it concerns how to define valid nodes for coarse-graining continuous dynamics without discarding the topology that organizes them. By shifting the conceptual basis of microstate analysis from templates to landmarks, the present approach provides a more principled and potentially more stable foundation for state definition, including in fMRI. This topolo-geometric reappraisal extends conventional microstate analysis and opens a path toward more unified comparisons across datasets, paradigms, and recording systems.