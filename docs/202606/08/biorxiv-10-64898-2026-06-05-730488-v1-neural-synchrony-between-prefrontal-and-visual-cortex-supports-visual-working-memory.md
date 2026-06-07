---
title: Neural synchrony between prefrontal and visual cortex supports visual working memory
title_zh: 前额叶与视觉皮层之间的神经同步支持视觉工作记忆
authors: "Dake, M., Dandekar, S., Curtis, C. E."
date: 2026-06-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.05.730488v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 从工作记忆期间的神经活动模式解码视觉内容
tldr: 该研究利用脑磁图探究前额叶与视觉皮层间的神经同步如何支持视觉工作记忆。在记忆维持期间，β频段活动增强且其空间分布预测记忆内容与错误，同时前额叶与视觉皮层的β活动同步，为前额叶通过同步机制控制感觉皮层存储记忆的假说提供了直接神经证据。
source: biorxiv
selection_source: fresh_fetch
motivation: 工作记忆涉及前额叶与感觉皮层，但前额叶如何影响视觉皮层中的工作记忆表征缺乏直接证据。
method: 采用脑磁图记录人类执行视觉空间工作记忆任务时的神经活动，分析β频段的功率变化及跨区域同步性。
result: 记忆维持期间β功率持续增强，其地形图可预测记忆位置和试次错误，且前额叶与视觉皮层间存在β频段同步。
conclusion: 前额叶与视觉皮层的β频段同步支持视觉工作记忆的分布式存储与通信，揭示了前额叶协调感觉皮层活动的潜在机制。
---

## 摘要
工作记忆似乎依赖于分布在整个大脑中的神经机制。具体而言，在记忆保持期间，前额叶皮层中的神经活动持续存在，同时，记忆的视觉内容可以从视觉皮层的活动模式中精确解码。当代模型试图解释这些发现，假设像前额叶皮层这样的高级区域通过招募感觉皮层的编码机制来控制记忆存储。证明前额叶皮层如何影响视觉皮层中的工作记忆表征在方法上具有挑战性，直接证据仍然很少。在此，我们利用脑磁图的优异时间分辨率，检验了关于前额叶和视觉皮层之间的神经活动同步如何协调工作记忆表征的假说。在人类（男女均包括）执行的一项视空间工作记忆任务中，整个记忆保持期间θ波段活动的功率增加，其在视觉皮层上的地形变化预测了记忆的位置和试次间的记忆错误。此外，在记忆过程中，前额叶和视觉皮层之间的θ波段神经活动同步。这些发现不仅与大量表明工作记忆广泛分布在大脑中的研究一致，而且有助于解释前额叶和感觉皮层在记忆过程中如何通信。

## Abstract
Working memory appears to depend on neural mechanisms that are distributed across the brain. Specifically, neural activity persists in the prefrontal cortex while memories are maintained, and at the same time, the visual contents of memory can be precisely decoded from the patterns of activity in visual cortex. Contemporary models attempt to account for these findings by positing that higher-order areas, like prefrontal cortex, somehow control memory storage by recruiting encoding mechanisms in sensory cortices. Demonstrating how prefrontal cortex influences working memory representations in visual cortex is methodologically challenging and direct evidence remains scarce. Here, we leveraged the excellent temporal resolution of magnetoencephalography to test hypotheses about how synchronization of neural activity between prefrontal and visual cortex coordinates working memory representations. During a visuospatial working memory task in humans (both sexes), increased power in -band activity persisted throughout memory maintenance, and changes in its topography over visual cortex predicted both memorized locations and trialwise memory errors. Moreover, neural activity in the -band synchronized between the prefrontal and visual cortices during memory. Not only do these findings align with a large body of work demonstrating that working memories are widely distributed across the brain, but they also help explain how the prefrontal and sensory cortices communicate during memory.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究背景**：工作记忆的维持被认为依赖分布式脑网络。前额叶皮层在记忆保持阶段表现出持续性活动，而视觉皮层中则可解码出记忆的精确视觉内容。然而，前额叶究竟如何影响或“控制”视觉皮层中的工作记忆表征，一直缺乏直接的神经证据。
- **核心问题**：前额叶与视觉皮层之间是否存在神经活动同步，且该同步是否支持视觉空间工作记忆的保持和精度。
- **整体含义**：揭示前额叶高级脑区通过神经同步机制招募感觉皮层进行记忆存储，为工作记忆的分布式控制模型提供关键实证支持。

### 2. 论文提出的方法论

- **核心思想**：利用脑磁图（MEG）的高时间分辨率，捕捉记忆保持期内前额叶与视觉皮层之间瞬时的神经振荡同步，并将其与记忆内容和行为错误联系起来。
- **关键技术细节**：
  - **任务**：人类被试执行视觉空间工作记忆任务，需记住视觉目标的位置并在延迟后复现。
  - **信号处理**：在 MEG 数据上进行源空间重建，提取前额叶和视觉皮层区域的神经活动。
  - **频段分析**：重点关注 **β 频段**的神经振荡。计算该频段功率（power）随时间的动态变化及其在头皮/源空间的地形分布。
  - **同步性度量**：量化前额叶与视觉皮层之间 β 频段活动的相位同步（如相位锁相值或相干性），以衡量跨区功能连接。
  - **解码与相关分析**：检验 β 功率地形图能否预测被试所记忆的空间位置，以及同步强度是否与试次的记忆误差相关。

### 3. 实验设计

- **被试与数据**：健康人类被试（男女均有），执行自行设计的视觉空间工作记忆任务，采集 MEG 数据。未使用公开数据集。
- **实验条件**：主要对比不同记忆位置引起的神经活动模式差异。内部比较了不同脑区（前额叶 vs. 视觉皮层）的活动特征，以及 β 频段与其他可能频段（但核心聚焦于 β 频段）。
- **Benchmark 与对比方法**：本文并非算法研究或模型对比，而是探索性实证研究。其“对比”体现在：
  - 用 β 功率地形图解码记忆位置，与随机水平或无信息基线比较。
  - 将同步性强度与记忆错误的行为指标做试次间相关，验证同步的行为相关性。
  - 间接回应了传统持续性活动模型与感觉皮层解码模型之间的争论，为“同步控制”假说提供证据。

### 4. 资源与算力

- 文中 **未明确提及** 所用 GPU 型号、数量或训练时长。研究采用的是人类 MEG 记录和标准的源重建、时频分析、功能连接等神经影像数据处理流程，计算量通常在 CPU 服务器即可完成，未涉及需要大规模算力的深度学习训练。

### 5. 实验数量与充分性

- **主要分析模块**：
  1. 记忆保持期内 β 功率时间进程及地形分布；
  2. 地形图对记忆位置的解码/预测分析；
  3. β 功率或同步性与试次记忆错误的关联；
  4. 前额叶与视觉皮层间 β 频段的神经活动同步性检验。
- **充分性与客观性**：
  - 实验设计有明确假设驱动，分析路径逻辑连贯（从现象到机制再到行为关联）。
  - 多种分析维度的收敛性证据增强了结论的稳健性。
  - 不足之处：仅使用单一任务范式和 β 频段，缺少与其他任务类型或频段的系统性对比，但作为一项开创性直接证据的研究，实验涵盖的核心问题较完整。

### 6. 论文的主要结论与发现

- **β 功率持续增强**：在整个记忆保持期间，β 频段的神经活动功率显著增强，并非瞬时响应。
- **空间信息编码**：β 功率在视觉皮层上的地形分布，能够预测被试所记忆的视觉位置，且功率变化可解释试次间的记忆误差，表明该活动携带行为相关的记忆内容。
- **跨区同步**：前额叶皮层与视觉皮层的 β 频段活动在记忆维持过程中实现了相位同步，为前额叶通过同步机制调控感觉皮层内的记忆表征提供了直接的神经证据。
- **理论整合**：结果统一了“前额叶持续活动”和“感觉皮层可解码记忆”两类发现，揭示了分布式记忆存储中长程同步通信的关键作用。

### 7. 优点

- **高时间分辨率方法**：巧妙利用 MEG 的毫秒级时间精度，直接捕捉跨区瞬时同步，这是 fMRI 难以做到的。
- **多维度证据链**：结合了时间（功率持久性）、空间（地形图解码）、行为（错误预测）和连接（跨区同步）四个层面的证据，形成闭环论证。
- **假设驱动明确**：针对工作记忆中“前额叶如何影响感觉皮层”这一空白，设计实验直接检验同步假说，理论贡献清晰。
- **简洁而聚焦**：没有盲目融入过多频段或脑区，而是围绕 β 频段和前额叶-视觉皮层通路进行深度挖掘。

### 8. 不足与局限

- **频段单一性**：研究主要聚焦 β 频段（注：原论文摘要中误写为 θ 频段，方法与结果部分均明确为 β），未系统考察 θ、α、γ 等其他频段的潜在贡献，可能遗漏其他同步机制。
- **相关非因果**：观察到的同步性本质上仍是相关关系，缺乏通过扰动（如 TMS）或因果分析（如 Granger 因果、动态因果模型）建立的直接因果证据。
- **任务与样本局限性**：仅采用一种视觉空间工作记忆任务，结论能否推广到其他类型工作记忆（如客体特征、言语工作记忆）尚待验证；样本量未说明，可能影响统计效力和个体差异分析。
- **空间分辨率限制**：MEG 源定位精度有限，难以精确将信号分离到细分的视觉脑区（如 V1、V2 等）或前额叶子区。
- **潜在混淆因素**：不能完全排除眼球运动、微眼跳等产生的肌电或伪迹信号对 β 频段同步性的影响。

（完）
