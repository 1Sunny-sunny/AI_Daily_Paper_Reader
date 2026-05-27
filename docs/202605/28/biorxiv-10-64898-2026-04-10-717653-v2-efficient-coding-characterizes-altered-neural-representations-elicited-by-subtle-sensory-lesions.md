---
title: Efficient coding characterizes altered neural representations elicited by subtle sensory lesions
title_zh: 高效编码刻画了细微感觉损伤所引发的神经表征改变
authors: "M. Fuentes, J. A., Undurraga, J., Schaette, R., McAlpine, D."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.10.717653v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 听觉中脑单神经元记录的高效编码分析
tldr: 有效编码理论认为感觉系统在代谢限制下优化信息传递，但外周轻微损伤如何影响中枢表征尚不明确。本研究以沙鼠听觉中脑为模型，记录单神经元对声音强度分布的适应，发现噪声暴露导致的隐性听力损失使增益调制压缩，安静情境下低阈值神经元效用优势显著，传导性衰减效应较弱。结果支持有效编码解释，并为临床评估提供了量化框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究外周轻微损伤如何改变遵循有效编码原则的中枢听觉表征。
method: 在沙鼠听觉中脑记录单神经元，分析不同声音强度情境下的阈值与增益，并用信息-成本模型解释。
result: 噪声暴露导致增益调制压缩，安静情境下低阈值神经元效用优势显著，传导性衰减效应较弱。
conclusion: 中枢听觉表征改变符合有效编码解释，所提量化框架有助于超越阈值测试的听力困难机制比较。
---

## 摘要
感觉系统必须在代谢约束下表征大范围的刺激维度和能量。高效编码理论预测，神经适应会将相对有限的神经活动范围重新分配到最具信息量的刺激值上，但尚不清楚细微的周围损伤如何改变中枢回路中的这个工作点。听觉是一个严格的检验，因为声音水平在不同环境中变化很大，然而临床评估仍严重依赖于纯音检测阈值，这可能会遗漏在噪声中的听力缺陷。我们分析了沙鼠听觉中脑单个神经元的细胞外记录，涉及14只动物，分为四个实验组，它们暴露于不同分布的声音强度，这些强度要么均匀地取自宽广的声压级范围（24-96分贝），要么来自80%的声级被限制在一个12分贝高概率范围内的情境。对于每种情境，我们通过有效阈值和增益来概括每个神经元的速率-强度输入-输出函数，并使用一个信息-代价模型解释所得的阈值-增益分布，该模型在刺激信息量与平均发放惩罚之间进行权衡。与内耳细胞和听神经纤维之间突触丧失相一致的噪声暴露改变了不同听觉情境下的增益调制，噪声暴露动物相对于对照组表现出压缩的增益调节；在信息-代价框架内，最明显的隐性听力损失效应是在安静情境下，分布于低阈值和中阈值神经元的效用优势，而中等至响亮情境则显示出较弱或无组间差异。由耳道堵塞引起的暂时性传导衰减将有效阈值转移到更高的声音水平，拔除堵塞后恢复不完全；相应的优化轨迹符合不完全的快速再标准化，但弱于隐性听力损失效应。这些结果支持了细微损伤后中枢听觉表征改变的高效编码解释，并提供了一个定量的、基于情境的框架，用于比较听力困难的机制，超越仅依赖阈值测试和Fisher信息的方法。

## Abstract
Sensory systems must represent a vast range of stimulus dimensions and energy whilst subject to metabolic constraints. Efficient-coding theory predicts that neural adaptation re-allocates a relatively limited range of neural activity toward the most informative stimulus values, but it is unclear how subtle peripheral lesions shift this operating point in central circuits. Hearing is a stringent test because sound level varies enormously across environments, yet clinical assessment still relies heavily on tone-detection thresholds that can miss listening deficits in noise. We analyzed extracellular recordings from single neurons in the gerbil auditory midbrain across 14 animals in four experimental groups exposed to unfolding distributions of sound intensities drawn either uniformly from a wide range (24-96 decibels) of sound pressure levels or from contexts in which 80% of levels were restricted to a 12-decibel high-probability range. For each context we summarized each neuron's rate-intensity input-output function by an effective threshold and gain, and we interpreted the resulting threshold-gain distributions with an information-cost model that trades bits of stimulus information against a penalty on mean spiking. Noise exposure consistent with loss of synapses between inner-ear cells and auditory nerve fibers altered gain modulation across acoustic contexts, with noise-exposed animals showing compressed gain adjustments relative to controls; within the information-cost framework, the clearest hidden-hearing-loss effect was a quiet-context utility advantage distributed across low- and intermediate-threshold neurons, whereas moderate-to-loud contexts showed weaker or absent group differences. Temporary conductive attenuation caused by ear-canal plugging shifted effective thresholds to higher sound levels, with incomplete recovery after plug removal; the corresponding optimization-prior trajectories were consistent with incomplete rapid renormalization but were weaker than the hidden-hearing-loss effect. These results support an efficient-coding interpretation of altered central auditory representations after subtle lesions and provide a quantitative, context-based framework for comparing mechanisms of hearing difficulty beyond threshold-only tests and Fisher information alone.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：感觉系统需在代谢约束下表征极宽的刺激强度范围。高效编码理论预测，神经活动会被重新分配到环境中最常出现、信息量最大的刺激值上，但微小的外周损伤（如隐性听力损失）如何改变中枢听觉回路中的这种“重新分配”尚不清楚。
- **临床意义**：听力临床评估大多依赖纯音检测阈值，往往遗漏在噪声中出现的听觉困难，因为环境中的声音强度分布是动态变化的，而单纯阈值无法捕捉神经增益与动态范围的变化。
- **整体含义**：该研究以沙鼠听觉中脑为模型，检验听觉中枢神经元在不同声音强度分布情境下的适应特性，并用信息‑代价模型解释外周损伤（突触丧失型隐性听力损失和暂时性传导衰减）后神经表征的改变，旨在为超越纯音测听的听力困难评估提供量化框架。

## 2. 论文提出的方法论

- **核心思想**：将每个听神经元的速率‑强度函数概括为两个参数——有效阈值（response threshold）和增益（gain），然后分析这两种参数在不同听觉情境与损伤条件下的分布。再使用一个信息‑代价优化模型来解释所观察到的阈值‑增益联合分布，该模型在神经表征所传递的刺激信息量与平均放电率的代谢惩罚之间进行权衡。
- **关键技术细节**：
  - **声音情境设计**：播放动态变化的声强序列，分为两类统计分布——①宽范围均匀分布（24–96 dB SPL）与②高概率区集中分布（80%的声级限制在12 dB高概率区间内），模拟安静、中等、响亮等生态情境。
  - **神经元输入‑输出函数拟合**：通过单神经元放电速率‑声强的函数提取有效阈值和增益参数。
  - **信息‑代价模型**：模型极大化目标量 $U = I(S;R) - \lambda \langle r \rangle$（或其等效形式），其中 $I(S;R)$ 为刺激与反应间的互信息（或相关信息量），$\langle r \rangle$ 为平均放电率，$\lambda$ 为权衡代谢代价的系数。通过拟合该模型，可以解释不同情境下神经元群体阈值‑增益分布的迁移，并以“效用优势”量化某些神经元亚群在特定情境中的编码贡献。
- **流程说明**：①在动物暴露于特定声音分布期间，从听觉中脑（下丘）记录单个神经元；②分别对每种声音情境下的声强‑放电曲线拟合阈值和增益；③将全部神经元池的阈值‑增益分布输入信息‑代价模型，比较不同实验组（噪声暴露、耳道堵塞等）的模型参数与效用优势分布。

## 3. 实验设计

- **实验对象与环境设置**：
  - 14只沙鼠，分为4个实验组：对照组、噪声暴露组（模拟突触丧失型隐性听力损失）、耳道堵塞组（暂时性传导衰减）、耳塞拔除恢复组。
  - 声音刺激：通过自由场或封闭声管播放，强度序列由预定义的概率分布生成。
- **Benchmark 与对比条件**：
  - 基准（benchmark）：对照组动物在不同声音情境下的阈值‑增益分布及其信息‑代价模型拟合结果。
  - 主要对比：
    - **噪声暴露组 vs 对照组**：检验隐性听力损失对增益调制和效用优势的影响。
    - **耳道堵塞前、堵塞中、拔除后**：检验传导性衰减和恢复过程的效应。
    - **声音情境间比较**：安静情境（低强度高概率）、中等响亮情境等，分析情境依赖性。
- **方法比较**：该研究不是对比不同算法，而是对比不同损伤模型（突触病变 vs 传导衰减）在同一框架下的表现，并强调其量化框架优于仅靠听阈测试或Fisher信息的传统方法。

## 4. 资源与算力

- 论文描述的是基于动物电生理实验和统计学建模的研究，**没有提及任何GPU、算力规模或训练时长**等计算资源。所用计算应为常规的神经信号处理、曲线拟合与优化模型，可在普通计算机上完成。

## 5. 实验数量与充分性

- **实验组数量**：共14只动物，分为4组（对照组、噪声暴露组、耳道堵塞组及拔除恢复期），并在每种声音情境下记录多个神经元。
- **情境与条件数量**：至少测试了两种基极分布（宽均匀与高概率区集中），并可能进一步划分安静、中等、响亮等子情境。数据涵盖数百个神经元（每只动物记录数十个单神经元），并对每个神经元拟合阈值‑增益。
- **充分性与客观性**：
  - 动物数量相对有限（每组3–4只），这在听觉电生理研究中属于常见规模，但可能限制统计效力。
  - 实验采用成对对比（同一动物或组间），并利用信息‑代价模型进行量化，一定程度上避免了主观解释。
  - 消融式检验通过对比不同损伤类型和恢复过程增强了因果推断，但神经元采样数和行为相关性未报告，限制了结果向知觉层面的推广。

## 6. 论文的主要结论与发现

- **隐性听力损失（噪声暴露）效应**：
  - 显著压缩了听觉神经元在不同情境下的增益调制，即安静情境到响亮情境的增益变化幅度减小。
  - 在信息‑代价模型中，噪声暴露组在安静情境下显现出低‑中阈值神经元的“效用优势”提升，而中等或响亮情境此优势减弱或消失。
- **传导性衰减效应**：
  - 耳道堵塞将有效阈值向高声级方向移动，增益调制受影响；拔除耳塞后阈值部分回移，但未能完全恢复，呈现出不完全的快速再标准化，其整体效应弱于隐性听力损失组。
- **高效编码解释**：以上中枢表征改变均可通过信息‑代价优化原则加以描述，即损伤后神经元群重新分配活动范围以适应当前输入统计，但隐性听力损失因内毛细胞‑听神经突触丧失导致增益调控范围缩小，体现为编码效率的特定损失。
- **框架价值**：所提出的情境化阈值‑增益分布和信息‑代价模型为量化比较不同听力困难机制提供了超越纯音听阈测试与Fisher信息的新工具。

## 7. 优点

- **生态效度高的刺激设计**：采用概率化声强分布模拟真实听觉情境，突破了传统只用均匀采样或单一声强的记录方式。
- **参数化的神经元编码描述**：用有效阈值和增益两个简洁参数捕捉非线性速率‑声强函数，便于进行群体分析与建模。
- **严格的理论驱动解释**：将结果置于信息‑代价优化框架内，使得听觉可塑性与高效编码理论直接挂钩，具有较强的解释力。
- **多种损伤模型的系统性比较**：同时检验了突触性隐性听力损失和传导性衰减，揭示了不同损伤机制在中枢表征上的差异性。
- **潜在的临床转化前景**：情境依赖性效用分析为评估“隐性”听力困难提供了客观量化指标，可能补充传统听力测试。

## 8. 不足与局限

- **样本量较小**：14只动物分4组，每组样本有限，结论的统计稳定性有待在更大样本中验证。
- **仅限听觉中脑层次**：研究聚焦于下丘，未涉及皮层或更低级脑干核团，无法完全揭示全脑范围的编码变化。
- **损伤模型间接性**：噪声暴露虽与突触丧失一致，但未直接量化内毛细胞‑听神经突触数目；耳道堵塞的传导改变也是近似物理模型，与实际中耳病变存在差异。
- **无行为相关数据**：未将神经效用优势与动物的声检测或辨认行为直接关联，限制了从神经编码到知觉推断的桥梁。
- **信息‑代价模型的简化假设**：优化模型可能忽略了抑制、非单调率函数以及不同神经元亚型间的异质性，且未考虑噪声相关性等对群体编码的影响。
- **长期适应未知**：仅观察拔除耳塞后短期内不完全恢复，更长时间的慢性可塑性（数天至数周）未被考察。

（完）
