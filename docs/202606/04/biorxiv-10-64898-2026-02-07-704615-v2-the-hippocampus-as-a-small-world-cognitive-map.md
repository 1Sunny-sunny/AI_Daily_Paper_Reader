---
title: The hippocampus as a small-world cognitive map
title_zh: 海马体作为小世界认知地图
authors: "Kim, J. Z., Sethna, J. P., Cohen, I., Sun, W."
date: 2026-05-31
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.07.704615v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 海马体认知地图作为时空动态的小世界网络
tldr: 本研究探究海马认知地图如何兼顾局部精度与全局搜索效率。通过对小鼠海马CA1区钙成像数据建模，发现神经表征呈现小世界网络结构：群体螺旋动力学保持时空局部信息，而多场神经元提供长程捷径，实现高效搜索。
source: biorxiv
selection_source: fresh_fetch
motivation: 认知地图如何既保持局部细节又能全局快速搜索远距离解尚未明确。
method: 使用几何感知自编码器对小鼠学习记忆导向导航任务的海马CA1神经元钙成像数据进行建模。
result: 发现小世界网络结构，群体螺旋动力学保留局部信息，多场神经元创建远距离捷径，静止期解码出现状态跳跃。
conclusion: 海马表征通过小世界结构优化搜索，为神经科学与人工智能提供启示。
---

## 摘要
当老鼠感知到鹰的影子时，它可能只有几秒钟来决定跑到哪里，然而最安全的庇护所往往既不在视线内，也不在附近。为了生存，它必须迅速搜索其认知地图，以便在众多可能性中做出选择，并且足够准确，以避开沿途的死胡同和危险，而随着路径、庇护所和威胁随时间变化，“安全”的定义也在不断改变。这一情景凸显了一个核心设计问题：认知地图必须保留精细的局部结构以保证可靠行动，同时又保持全局可搜索性，以便在空间和时间上高效地找到遥远而有用的解决方案。海马体被认为支持这样的地图，其群体活动表征了世界状态及其转换——然而，这些地图如何结构化以解决这一设计问题尚不清楚。在此，我们使用了一种新颖的几何感知自编码器，对小鼠在学习记忆引导的导航任务时数千个海马CA1神经元的纵向钙成像数据进行了建模，以揭示认知地图的结构。我们发现，海马群体编码通过神经表征空间中的小世界网络结构实现了局部保真度和全局可搜索性，这利用了两种互补机制。在群体层面，相对于过去经验的螺旋（旋转加漂移）动力学构建了新地图，这些地图保留了关于附近空间和时间位置的局部信息，同时与先前的表征保持可区分性。在细胞层面，具有协调的多野活动的神经元在远距离表征之间创建了稀疏的长程捷径。在不动的同步群体事件中，解码的活动经常跳跃到空间、时间和任务条件下的远距离状态，表明这些捷径在离线处理期间被使用。这种功能组织对神经科学和人工智能都有启示，揭示了海马表征如何可能针对智能系统面临的一个基本挑战进行优化：高效地搜索准确的世界内部模型。

## Abstract
When a mouse perceives a hawks shadow, it may have only seconds to decide where to run, yet the safest refuge is often neither visible nor nearby. To survive, it must search its cognitive map quickly enough to choose among many possibilities, and accurately enough to avoid dead ends and hazards along the way, all while what counts as "safe" changes as paths, refuges, and threats shift with time. This scenario highlights a core design problem: cognitive maps must preserve fine local structure for reliable action, yet remain globally searchable so that distant, useful solutions can be found efficiently in both space and time. The hippocampus is thought to support such maps, with population activity representing world states and their transitions--yet how these maps are structured to solve this design problem is not well understood. Here, we used a novel geometry-aware autoencoder to model the structure of the cognitive map from longitudinal calcium imaging from thousands of hippocampal CA1 neurons in mice learning a memory-guided navigation task. We discovered that the hippocampal population code achieves both local fidelity and global searchability through small-world network structure in the space of neural representations that leverages two complementary mechanisms. At the population level, helical (rotation-plus-drift) dynamics of neural representations relative to past experience build new maps that preserve local information about nearby positions in space and time while remaining distinguishable from earlier representations. At the cellular level, neurons with coordinated multi-field activity create sparse, long-range shortcuts between distant representations. During synchronous population events in immobility, decoded activity often jumps to distant states in space, time, and task conditions, suggesting these shortcuts are engaged during offline processing. This functional organization, with implications for both neuroscience and artificial intelligence, sheds light on how hippocampal representations may be optimized for a fundamental challenge faced by intelligent systems: efficiently searching through accurate internal models of the world.