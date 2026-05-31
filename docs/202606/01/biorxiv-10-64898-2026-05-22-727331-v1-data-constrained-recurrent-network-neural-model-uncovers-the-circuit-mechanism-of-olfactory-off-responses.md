---
title: Data-Constrained Recurrent Network Neural Model Uncovers the Circuit Mechanism of Olfactory OFF Responses
title_zh: 数据约束的循环网络神经模型揭示嗅觉OFF反应的回路机制
authors: "Joshi, S., McLane-Svoboda, A., Navas Zuloaga, M. G., Stout, C., Saha, D., Bazhenov, M."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.22.727331v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: RNN模型将气味刺激与投射神经元放电动态关联
tldr: 本研究探索昆虫触角叶中嗅觉刺激终止（OFF）反应的神经回路机制。通过构建受生物学约束的发放率递归神经网络，并利用蝗虫投射神经元的活体电生理记录进行训练，成功重现了气味诱发的时间动态。研究发现OFF反应由两种不同通路产生：前馈通路直接传递气味受体神经元的终止信号，递归通路则依赖局部神经元间的相互抑制，通过暂时解除抑制产生净兴奋。这两条通路激活的投射神经元群体几乎不重叠，表明OFF反应身份是网络状态的涌现属性，而非细胞固有特征。该研究展示了数据约束模型从活体记录中剖析回路机制的能力。
source: biorxiv
selection_source: fresh_fetch
motivation: 感觉神经回路如何编码刺激终止的电路机制尚不明确。
method: 构建受生物约束的发放率递归神经网络，并用蝗虫触角叶110个投射神经元的活体记录进行训练。
result: OFF反应由前馈和递归两条通路产生，递归通路中的LN-LN相互抑制通过释放抑制产生兴奋，且两通路激活非重叠PN群体，表明OFF反应身份是网络涌现属性。
conclusion: 研究揭示了嗅球OFF反应的回路机制，并演示了数据约束递归神经网络可从活体记录中剖析神经回路功能。
---

## 摘要
感觉神经回路必须编码刺激的存在和终止。在气味刺激停止后，昆虫触角叶（AL）中的投射神经元（PN）表现出瞬时放电率增加，称为OFF反应，然而在递归兴奋-抑制网络中产生这些反应的回路机制仍不清楚。在此，我们构建了一个基于生物约束的、基于放电率的蝗虫触角叶递归神经网络（RNN）模型，并使用110个体内PN的电生理记录进行训练，以重建它们在五种气味刺激下由气味诱发的时间动态。训练后的模型忠实地再现了受约束神经元的放电率，而未受约束的PN和LN则发展出生物学上合理的时间响应模式和响应类型多样性。通过靶向输入和连接性扰动，我们发现OFF反应通过两条机制上不同的途径产生。一条前馈途径将偏移型嗅觉受体神经元（ORN）的输入直接传递给下游PN，而一条递归途径则独立于偏移输入产生刺激后兴奋。对单个递归连接的选择性扰动确定LN-LN相互抑制是主要的递归途径，兴奋性和抑制性输入的分解显示，它通过抑制的瞬时释放而非增加驱动来产生净兴奋。这两条途径招募的PN群体在很大程度上不重叠，表明OFF反应身份是网络状态的一种涌现属性，而不是细胞固有的特征。这些发现提供了对OFF反应产生的回路级别的解释，并展示了数据约束的RNN如何直接从体内记录中解析回路机制。

## Abstract
Sensory neural circuits must encode both the presence and termination of a stimulus. Following odor offset, projection neurons (PNs) in the insect antennal lobe (AL) exhibit transient increases in firing rate, termed OFF responses, yet the circuit mechanisms that generate them in recurrent excitatory-inhibitory networks remain poorly understood. Here, we constructed a biologically-constrained firing rate-based recurrent neural network (RNN) model of the locust AL and trained it on electrophysiological recordings from 110 in vivo PNs to reconstruct their odor-evoked temporal dynamics across five odorants. The trained model faithfully reproduced the firing rates of constrained neurons, while unconstrained PNs and LNs developed biologically plausible temporal response patterns and response-type diversity. Using targeted input and connectivity perturbations, we found that OFF responses arise through two mechanistically distinct pathways. A feedforward pathway transmits offset-type olfactory receptor neuron (ORN) input directly to downstream PNs, while a recurrent pathway generates post-stimulus excitation independently of offset input. Selective perturbation of individual recurrent connections identified LN-LN mutual inhibition as the dominant recurrent pathway, and decomposition of excitatory and inhibitory inputs revealed that it produces net excitation through the transient release of inhibition rather than through increased drive. The two pathways recruit largely non-overlapping PN populations, indicating that OFF response identity is an emergent property of the network state rather than a cell-intrinsic feature. These findings provide a circuit-level account of OFF response generation and demonstrate how data-constrained RNNs can dissect circuit mechanisms directly from in vivo recordings.

---

## 论文详细总结（自动生成）

# 论文总结：数据约束的循环网络神经模型揭示嗅觉 OFF 反应的回路机制

## 1. 核心问题与整体意义
- **研究背景与动机**：感觉神经回路不仅需要编码刺激的出现，也必须精确表征刺激的终止。在昆虫嗅觉系统中，气味消失后触角叶（AL）的投射神经元（PN）会爆发短暂的放电率升高，即 **OFF 反应**。然而，在由兴奋性和抑制性神经元组成的递归网络中，这类 OFF 反应究竟通过何种回路机制产生，长期未得到清晰解释。
- **整体意义**：本研究旨在从回路层面揭示 OFF 反应产生机制，并展示**数据约束的递归神经网络（RNN）** 如何直接从活体电生理记录中反向解析神经回路的工作原理，为感觉编码的计算机制提供新的研究范式。

## 2. 方法论
- **核心思想**：构建一个基于放电率、受生物学约束的蝗虫触角叶 RNN 模型，用真实的 PN 放电记录训练网络，使得模型不仅复现被约束神经元的动态，还能让未被约束的神经元涌现出符合生物实际的反应特性，随后通过对网络结构和输入的精细扰动，推断产生 OFF 反应的因果回路。
- **关键技术细节**：
  - **模型构建**：基于发放率的 RNN，包含气味受体神经元（ORN）输入、投射神经元（PN）和局部中间神经元（LN）群体，并融入已知的兴奋-抑制连接约束。
  - **训练数据**：使用 **110 个蝗虫 PN 的体内电生理记录**，涵盖五种不同气味刺激诱发的放电时间序列。训练目标是让模型中受约束的 PN 神经元忠实地复现这些记录发放率。
  - **机制解析方法**：
    - **靶向输入扰动**：选择性移除偏移型 ORN（在气味终止时发放的 ORN）的输入，检验前馈通路贡献。
    - **连接性扰动**：对递归连接进行选择性破坏，尤其扰动 LN 与 LN 间的相互抑制连接。
    - **输入分解**：将每个神经元的突触输入分解为兴奋性和抑制性成分，观察 OFF 反应期间的净变化。
  - **分析流程**：对比扰动前后或分解前后网络响应，判断特定通路或输入成分在产生 OFF 反应中的因果作用。

## 3. 实验设计
- **数据集与场景**：
  - **数据来源**：蝗虫触角叶中 **110 个 PN 神经元**在 **五种不同气味** 刺激下的胞内（活体）电生理记录。气味呈现包含明确的起始和终止时间，用于捕捉 ON 和 OFF 动态。
  - **模型验证基准**：以受约束 PN 的放电率复现精度为直接评估依据；对未受约束的 PN 和 LN，则考察其时间反应模式、反应类型多样性是否与已知生物学知识相符。
- **对比与检验**：
  - 未采取与传统分类器或独立模型的性能对比，而是通过 **内部扰动-复原对比**（即扰动网络后观察反应变化）作为主要分析手段。
  - 具体扰动条件包括：移除偏移 ORN 输入、单个递归连接的选择性失活等，以构建“有/无通路”的因果证明。

## 4. 资源与算力
- **算力说明**：论文摘要及所提供的元数据中 **未提及 GPU 型号、数量、训练时长** 等具体计算资源信息。鉴于该模型为基于放电率的 RNN 且仅针对 110 个神经元的时间序列进行训练，计算量可能相对较小，但文本中对此无直接陈述，因此无法给出定量概括。

## 5. 实验数量与充分性
- **实验组数和类型**：
  - 基础实验：在五种气味、110 个 PN 记录上的模型训练与复现。
  - **机制扰动实验**：
    - 前馈通路验证：移除偏移 ORN 输入。
    - 递归通路验证：独立于偏移输入的能量或扰动。
    - **选择性连接扰动**：针对 LN-LN 相互抑制等具体连接进行破坏。
    - **输入分解**：将突触电流分解为兴奋与抑制，观察净效应。
  - **群体分析**：比较两条通路所招募的 PN 群体重叠程度。
- **充分性与客观性**：
  - 实验设计具有明确的因果推理逻辑（通过精准扰动分离前馈/递归贡献，并进一步定位到 LN-LN 相互抑制），所采用的扰动均为内部网络干预，结果可对比性强。
  - 从摘要看，实验步骤环环相扣，对主要结论的支持比较充分；但受限于提供的内容，无法评估是否有其他未公开对照（如不同超参数、不同气味浓度等），总体而言在给定范围内是客观且公平的。

## 6. 主要结论与发现
- **双通路机制**：OFF 反应通过 **前馈通路** 和 **递归通路** 两种机制上截然不同的通路产生。
  - **前馈通路**：将偏移型 ORN 的直接输入传递给 PN，带来气味终止时的兴奋。
  - **递归通路**：不依赖偏移输入，主要依靠 **LN-LN 相互抑制**。气味期间抑制性 LN 被激活，气味终止后抑制解除（释放抑制），从而产生净兴奋，而非通过兴奋性输入的增加。
- **非重叠 PN 群体**：这两条通路激活的 PN 群体在很大程度上互不重叠，表明某个 PN 是否产生 OFF 反应并非该细胞的固有属性，而是 **网络状态的涌现特性**。
- **方法学示范**：证明数据约束的 RNN 可以作为有效工具，从活体群体记录中直接解析复杂的神经回路功能。

## 7. 优点
- **方法学创新**：将“生物学约束 + 数据驱动训练”的 RNN 与“精细扰动 + 输入分解”的回路分析方法相结合，为从活体数据反向推导机制提供了系统框架。
- **机制洞察清晰**：成功分离出前馈与递归两种通路，并精准定位递归通路中的关键突触类型（LN-LN 相互抑制）及其实质（释放抑制），回答了长期存在的回路级问题。
- **涌现属性揭示**：通过群体重叠分析，将 OFF 反应身份定义为网络涌现现象，超越了对单细胞固有特性的归因，具有概念上的推进。

## 8. 不足与局限
- **物种与数据量**：模型基于蝗虫触角叶的 110 个 PN 记录和五种气味，所揭示的机制能否推广到其他昆虫或更复杂脊椎动物嗅球，尚待验证。
- **模型简化**：使用发放率模型省略了脉冲时间细节，可能忽略某些由精确时序或同步性介导的回路机制。
- **扰动方式**：连接扰动和输入移除为计算性干预，虽能提供因果证据，但可能无法完全模拟真实的药理学或光遗传学操作效果。
- **信息不完整**：论文全文未能获取（仅为摘要和元数据），关于模型超参数、训练收敛验证、噪声鲁棒性等细节无从评估，且文中未提及算力消耗。
- **外部验证缺失**：结论主要基于模型内部分析，缺乏与真实扰动实验（如沉默特定 LN 亚型）的直接对比，降低了生物学证伪的严格性。

（完）
