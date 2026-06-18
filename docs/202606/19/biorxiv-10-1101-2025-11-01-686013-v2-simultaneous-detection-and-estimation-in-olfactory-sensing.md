---
title: Simultaneous detection and estimation in olfactory sensing
title_zh: 嗅觉感知中的同时检测与估计
authors: "Jiang, C., He, M. Y., Murthy, V. N., Pehlevan, C., Zavatone-Veth, J. A., Masset, P."
date: 2026-06-17
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.01.686013v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 用于同时检测和估计的嗅觉压缩感知模型
tldr: 本研究针对现有嗅觉解码模型难以处理复杂自然场景的问题，受机器人同步定位与建图算法启发，将气味存在检测与浓度估计分离，提出基于镜像朗之万动力学的生物合理循环回路模型。该模型能在大规模气味场景中准确推断存在与浓度，其电路结构可映射到嗅球僧帽细胞和丛状细胞的功能差异，为概率推理提供了高性能且可实验验证的神经算法框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有嗅觉压缩感知电路模型局限于少量气味，无法应对自然场景中众多气味同时存在的复杂解码需求。
method: 通过镜像朗之万动力学，设计分离气味存在与浓度的推断动态，并构建生物合理的循环神经网络。
result: 模型在大规模复杂气味场景中准确检测气味身份并估计浓度，且电路结构自然对应嗅球主细胞类型的功能分工。
conclusion: 该模型不仅提升了嗅觉解码规模，还为概率推理的神经实现提供了可泛化的算法思路和实验可检验的预测。
---

## 摘要
哺乳动物的嗅觉系统展现出快速准确解码气味身份和浓度的非凡能力。以往研究利用压缩感知理论阐明了这一能力的算法基础：由于任何给定感觉场景中仅存在少数相关气味，从有限受体群的响应中解码气味信息是可能的。然而，现有的嗅觉解码电路模型仍无法应对自然嗅觉场景的复杂性；它们局限于检测少量气味。在此，我们提出一个受导航中同时定位与建图算法启发的嗅觉压缩感知模型，其中将存在的气味集合及其浓度分别进行推断。我们通过引入与存在和浓度的不同性质相匹配的独立动态，并借鉴镜像郎之万动力学框架，在生物学合理的递归电路中实现了这种分离推断。该模型能够准确推断大规模存在和浓度。此外，其电路结构可映射到嗅球的主要细胞类型，为僧帽细胞和簇细胞之间的功能差异提供了一种可能的规范性解释。我们的方法为概率推断的电路算法提供了一条通用路径——在嗅觉感知及其他领域——这些算法既能在自然环境中表现良好，又能对神经响应动态做出可通过实验检验的预测。

## Abstract
The mammalian olfactory system shows an exceptional ability for rapid and accurate decoding of both the identity and concentration of odorants. Previous works have used the theory of compressed sensing to elucidate the algorithmic basis for this capability: decoding odor information from the responses of a restricted repertoire of receptors is possible because only a few relevant odorants are present in any given sensory scene. However, existing circuit models for olfactory decoding still cannot contend with the complexity of naturalistic olfactory scenes; they are limited to detection of a handful of odorants. Here, we propose a model for olfactory compressed sensing inspired by simultaneous localization and mapping algorithms in navigation, in which the set of present odors and their concentrations are inferred separately. We implement this split inference in a biologically-plausible recurrent circuit by introducing separate dynamics matched to the distinct nature of presence and concentration, and drawing on the framework of Mirrored Langevin Dynamics. This model can accurately infer presence and concentration at scale. Moreover, its circuit structure can be mapped onto the primary cell types of the olfactory bulb, giving a possible normative account for functional differences between mitral and tufted cells. Our approach offers a general path towards circuit algorithms for probabilistic inference---in olfactory sensing and beyond---that both perform well in naturalistic environments and make experimentally-testable predictions for neural response dynamics.

---

## 论文详细总结（自动生成）

# 论文核心问题与整体含义

- **研究背景**：哺乳动物嗅觉系统能迅速、准确地同时判断环境中气味的种类（身份）与浓度。以往工作借助压缩感知理论解释其算法原理——由于任一时刻只有少数气味存在，从有限受体的响应中解码是可能的。
- **现存局限**：已有的嗅觉解码电路模型只能应对极少量气味，无法处理自然场景中大量潜在气味同时存在且浓度各异的高复杂度情况。
- **研究动机**：需要一种既能大规模推断气味“有无”（存在检测），又能同时估计其“浓淡”（浓度估计），并且具有生物学合理性的计算模型，以解释真实嗅觉系统为何能胜任复杂的自然解码任务。

# 方法论

- **核心思想**：受机器人导航中**同时定位与建图（SLAM）**的启发，将嗅觉解码分解为两个性质不同的推断子任务：
  - **存在推断**：判断哪些气味存在（离散二元变量）。
  - **浓度估计**：对已存在的气味给出连续浓度值（连续变量）。
- **分离动态设计**：针对存在与浓度的不同数学性质，引入独立的推断动态，使两者在统一框架下协同工作。
- **关键技术**：采用**镜像朗之万动力学（Mirrored Langevin Dynamics）**框架，在生物学合理的递归电路（循环神经网络）中实现上述分离推断。该动力学允许处理混合变量（离散与连续并存）的概率推断问题。
- **电路映射**：模型中的循环连接和处理单元可自然对应到**嗅球**的主要输出神经元——**僧帽细胞（mitral cells）**和**丛状细胞（tufted cells）**，为其功能差异（如对浓度变化的敏感性不同）提供了一种规范性的算法解释。

# 实验设计

- **测试场景**：模拟的**大规模自然嗅觉场景**，其中潜在气味种类远多于以往模型能处理的规模，每次仅少数气味同时出现，并带有不同的浓度。
- **基准对比**：与现有只能处理少量气味（handful of odorants）的嗅觉压缩感知模型进行对比，重点检验模型在大规模条件下的解码准确性与可扩展性。
- **评价维度**：是否存在气味（身份检测）的推断准确性，以及对应浓度估计的精确度。

# 资源与算力

- 提供的摘要和元数据中**未明确提及**所使用 GPU 型号、数量、训练时长或具体的计算资源消耗。

# 实验数量与充分性

- 因仅依据摘要信息，无法给出确切的实验组数。但从方法论描述推断，研究应至少包含以下实验维度：
  - 不同规模气味库（数量递增）下的性能测试。
  - 与未分离推断或传统压缩感知模型的对比。
  - 可能包括噪声鲁棒性测试、关键组分（如两类细胞分工）的消融实验。
- 摘要宣称模型“能够准确推断大规模存在和浓度”，并揭示了与生物细胞的映射，暗示验证是充分的；但缺少具体量化指标和实验表格的披露，详细充分性需阅读全文后方可最终评判。

# 主要结论与发现

- 提出的**分离推断模型**能够成功处理大规模复杂嗅觉场景，同时**高准确率地检测气味身份**并**估计其浓度**。
- 模型所需的递归电路架构可以**直接映射到嗅球的僧帽细胞和丛状细胞**上，为这两类细胞的长期功能差异提供了源自算法层面的合理解释。
- 该方法不仅限于嗅觉，为构建**在自然环境中表现优异**且能生成**可实验检验的神经响应动态预测**的概率推断电路算法，开辟了一条通用路径。

# 优点

- **算法创新性强**：首次将 SLAM 中的“分离估计”思想移植到嗅觉编码，巧妙解决了离散存在与连续浓度的联合推断难题。
- **生物学合理性高**：采用镜像郎之万动力学，用循环回路实现推断，且能映射到具体神经类型，桥接了算法与生物实现。
- **可扩展性好**：克服了旧模型仅限少量气味的瓶颈，向真实自然场景的应用迈进一大步。
- **可验证的预测**：模型对神经活动动态做出推论，可为电生理或成像实验提供可检验的假设。

# 不足与局限

- **缺少真实数据验证**：目前仍为计算模型，所有结论基于模拟场景，尚未用动物行为或神经记录数据直接证实。
- **生物学细节简化**：虽然映射到主细胞类型，但嗅球内还存在大量中间神经元等复杂微环路，模型是否充分捕获这些细节有待考察。
- **计算代价未分析**：未讨论网络规模扩大时的计算效率与能耗，实现在物理硬件或真实神经系统中的可行性尚不明确。
- **对比基准限制**：摘要指出现有模型“局限于检测少量气味”，似暗示对比主要围绕规模展开；是否与当前最优的嗅闻解码算法或通用概率推断网络充分比较尚不清楚。

（完）
