---
title: Condition-Dependent Noise Correlations without Condition-Dependent Spike Counts
title_zh: 无伴随条件依赖性发放计数的条件依赖性噪声相关
authors: "Kim, D., Panichello, M., Moore, T."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.08.723078v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 研究条件依赖性噪声相关性作为神经编码信息源
tldr: 大脑编码信息依赖神经元群体协调活动，噪声相关性（NCs）通常与锋电位计数（SCs）选择性相关。本研究记录猕猴前额叶皮层神经元在空间延迟反应任务中的活动，发现即使神经元对的SCs未表现出条件依赖性，其NCs仍可呈现条件依赖性，且幅度与有SCs选择性的神经元对相当，证明相关性变异性可独立于SCs编码条件信息。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究噪声相关性是否能在无锋电位计数选择性的情况下仍提供条件依赖信息。
method: 记录猕猴前额叶皮层大神经元群体在空间延迟反应任务（包含视觉、记忆和运动阶段）中的锋电位活动。
result: 无锋电位计数选择性的神经元对仍存在条件依赖的噪声相关性，且其幅度与有选择性的神经元对相当。
conclusion: 噪声相关性可独立于锋电位计数编码条件信息，提示其作为神经信息编码的独立途径。
---

## 摘要
大脑编码信息和控制行为的能力依赖于大量分布式神经元群体的协调活动。同一条件下的重复试验中神经元发放活动的相关性，即噪声相关性（NCs），被视为共享突触连接的反映，也是影响神经元群体信息容量的一个因素。通常认为噪声相关性对编码的影响主要体现在那些其发放计数（SCs）中包含稳健条件依赖性信息的神经元群体中。然而，理论研究表明，噪声相关性可能提供一个独立于发放计数的条件依赖性信息源。我们研究了猕猴前额叶皮层中大量神经元群体在执行包含视觉、记忆和运动阶段的延迟空间响应任务时的活动。结果发现，那些在发放计数上表现出视觉、记忆和运动选择性的神经元对，其噪声相关性也常常表现出选择性，且这种选择性独立于发放计数。此外，我们发现在任务各阶段无发放计数选择性的神经元对，同样表现出条件依赖性的噪声相关性。并且，无论神经元对是否具有发放计数选择性，其条件依赖性噪声相关性的幅度在很大程度上是可比的。这些结果表明，即使在缺乏条件依赖性发放计数的情况下，发放活动的相关变异性也可以是条件依赖性的。

## Abstract
The ability of the brain to encode information and control behavior depends on the coordinated activity of large and distributed neuronal populations. Correlations in neuronal spiking activity across trials of the same condition, or noise correlations (NCs), have been interpreted as a reflection of shared synaptic connectivity and as a contributing factor to the information capacity of neuronal populations. The impact of NCs on coding is most often considered in populations of neurons exhibiting robust condition-dependent information in their spike counts (SCs). However, theoretical work suggests that NCs could provide a source of condition-dependent information separate from SCs. We examined the activity of large neuronal populations in prefrontal cortex of macaques while they performed a spatial delayed response task composed of visual, memory, and motor epochs. We found that pairs of neurons that displayed visual, memory, and motor selectivity in their SCs often exhibited selectivity in their NCs, independent of spike count. However, we also found that pairs of neurons without SC selectivity during the different task epochs nonetheless exhibited condition-dependent NCs. Moreover, we found that the magnitude of condition-dependent NCs were largely comparable across neuronal pairs with or without SC selectivity. These results demonstrate that correlated variability in spiking activity can be condition-dependent even in the absence of condition-dependent SCs.

---

## 论文详细总结（自动生成）

# 论文总结：《Condition-Dependent Noise Correlations without Condition-Dependent Spike Counts》

## 1. 核心问题与整体含义
*   **研究动机**：神经编码传统上侧重单个神经元的**发放计数（Spike Counts, SCs）**如何携带条件信息，而**噪声相关性（Noise Correlations, NCs）**被认为是共享突触输入的反映，通常只在发放计数已有条件依赖的神经元群体中被研究。然而，理论推测 NCs 自身可能独立于 SCs 编码条件信息。
*   **核心问题**：在**完全没有发放计数选择性**的神经元对中，噪声相关性是否依然能表现出**条件依赖性**？若能，其幅度是否与有 SC 选择性时的 NC 相当？
*   **整体含义**：若 NCs 可独立携带条件信息，则意味着群体编码存在一条**独立于发放率编码的平行通路**，这对理解大脑信息容量和编码策略有深刻影响。

## 2. 方法论
*   **核心思想**：将神经元活动分解为两个维度——**发放计数（SCs）**和**跨试次协调变异性（NCs）**，并分别检验二者的条件依赖性，尤其关注**仅 NCs 变、SCs 不变**的神经元对。
*   **关键技术与流程**：
    *   **记录技术**：在清醒执行任务的猕猴前额叶皮层，用多电极阵列记录**大神经元群体**的锋电位。
    *   **任务设计**：采用经典的**空间延迟反应任务**，包含视觉提示、记忆维持和运动响应三个连续阶段，以剖析不同认知过程。
    *   **选择性定义**：分别计算单个神经元和神经元对的**条件依赖性**。对于 SCs，用常规的选择性指数（如区分不同空间位置/条件的能力）；对于 NCs，用 Pearson 相关或类似的跨试次相关性，并检验其在不同任务条件下是否显著差异。
    *   **对比分析**：将神经元对划分为“**有 SC 选择性**”和“**无 SC 选择性**”两组，比较两组的 NCs 条件依赖性概率及幅度。

## 3. 实验设计
*   **实验对象/数据**：猕猴前额叶皮层（PFC）神经元群体，在执行延迟空间响应任务时记录。
*   **基准/对比维度**：
    *   **不同任务阶段**：视觉、记忆、运动阶段分别检验。
    *   **神经元对分组**：基于发放计数是否选择性，构成两种关键对比场景——有 SC 选择性对 vs. 无 SC 选择性对。
*   **对比方法**：文中直接比较两组神经元对中，出现“条件依赖性 NCs”的比例，以及 NCs 的条件调制幅度大小。

## 4. 资源与算力
*   **算力情况**：本研究为**动物电生理实验与统计分析**，不涉及 GPU 训练或深度学习模型计算。文中未提及使用特定硬件或算力资源。分析主要依赖常规统计测试，算力需求极低。

## 5. 实验数量与充分性
*   **实验规模**：摘要中提到记录了“大神经元群体”，但未给出具体动物数量、神经元总数或纳入分析的神经元对数量。从结果能判断的是，他们覆盖了多个任务阶段，并比较了至少两种不同类型的神经元对（有/无 SC 选择性）。
*   **充分性与客观性**：
    *   核心对比明确，且使用同一群体数据内部自身对照，排除了记录偏倚。
    *   结论声称无 SC 选择性对的 NC 幅度“基本可比”，这暗示做了统计检验，但摘要未报告具体 $p$ 值或效应量。
    *   整体实验设计直接瞄准核心假设，逻辑上是充分且客观的，但若缺乏更详尽的样本量和统计检验细节，严谨性无法完全评估。

## 6. 主要结论与发现
*   **独立性发现**：即使神经元对在任务各阶段**没有任何发放计数选择性**，其噪声相关性依然可以表现出**稳健的条件依赖性**。
*   **幅度可比性**：无 SC 选择性对的 NCs 条件调制幅度，与有 SC 选择性对的 NCs 调制幅度**在大体上具有可比性**。
*   **编码含义**：发放活动的相关变异性可以独立于发放计数编码条件信息，构成一条**独立的信息通路**。

## 7. 优点
*   **理论挑战**：直接验证并证实了理论预测，打破了“NCs 仅辅佐 SCs”的固有框架，是观念上的重要推进。
*   **设计严谨**：利用同一任务的多认知阶段，且在同一数据内做分组对比，控制了神经元群体和记录状态的异质性。
*   **发现清晰**：明确展示了“无 SC 选择性可以有 NC 选择性”，且幅度相当，结论极具说服力。

## 8. 不足与局限
*   **脑区局限性**：仅考察了前额叶皮层，该结论是否适用于感觉皮层（如 V1、MT）或运动皮层尚不清楚，可能具有脑区特异性。
*   **机制不明确**：揭示了现象，但未探讨产生这种“独立 NCs”的突触或环路机制（例如，是否存在与突触输入同步但不改变平均发放率的连接模式）。
*   **信息量未量化**：未从信息论角度计算这种独立 NCs 到底能额外提供多少比特的编码信息，其实用价值未完全明确。
*   **实验细节缺失**：从当前摘要无法获知样本量、统计方法细节及效应大小，难以评估结论的统计稳健性和可重复性。

（完）
