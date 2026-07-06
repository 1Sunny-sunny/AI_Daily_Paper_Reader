---
title: Anticipatory organization of neural population dynamics speeds behavioral decisions
title_zh: 神经群体动态的预期性组织加速行为决策
authors: "Gorman, J. C., Sainburg, T., McPherson, T. S., Gentner, T. Q."
date: 2026-07-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.30.735699v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 听觉前脑神经群体动态与时间解码
tldr: 本研究探讨期望如何调节神经群体动力学以加速行为决策。通过对欧洲椋鸟听觉皮层神经元群体记录，发现期望在单神经元水平增强类别内刺激反应差异，但在群体水平却增加同类别反应相似性。作者构建动力学模型，揭示神经元间冗余性可实现群体水平表征的重映射，使群体轨迹在任务子空间中更紧密，从而减少噪声并预先组织活动于行为相关流形，最终提升决策速度和准确性。
source: biorxiv
selection_source: fresh_fetch
motivation: 理解期望在群体神经动力学水平上如何塑造行为决策，填补从单神经元到群体水平的机制空白。
method: 利用动态系统框架分析欧洲椋鸟在期望操纵下分类鸟鸣音节时的群体神经活动，并建立退化重映射模型。
result: 单神经元反应差异增大而群体轨迹在任务子空间中更相似；分类错误与轨迹向错误流形漂移相关，早期群体运动方向预测行为速度和准确性。
conclusion: 期望通过预期性组织群体活动于行为相关流形，预先准备神经群集动力学，实现快速准确的决策。
---

## 摘要
期望引导行为并塑造单个神经元的感觉反应，但它们对群体水平神经动态的影响尚不清楚。在此，我们采用动力学系统框架，研究欧洲椋鸟（一种鸣禽）听觉前脑中神经元群体的集体放电活动，在感觉期望被操纵的情况下，它们对自然歌曲音节进行分类。我们首先表明，感觉驱动的神经群体放电活动描绘出平滑、低维的潜在轨迹，这些轨迹密切反映感觉信号的身份。与单个神经元的刺激驱动反应一样，群体轨迹的几何形状也受期望的调节。在单个神经元中，期望增强了同一类别信号反应之间的差异，但在群体水平上，效果相反：期望增加了同一类别信号反应之间的相似性。为了理解群体水平的反应动态如何与单个神经元的不同，我们开发（并实验验证）了一个动力学模型，将这两个生物尺度上的放电活动联系起来。该模型利用了神经元之间的反应冗余，我们称之为简并性重映射的能力，并使得在任务有效子空间（即与行为分类相关的群体活动维度）中，同时观察到期望依赖的单个神经元反应可分离性增加和群体轨迹可分离性减少。通过详细检验期望调制的群体轨迹与行为之间的关系，我们发现单次试验的分类错误与轨迹向相反任务有效流形的漂移有关。这表明期望有助于建立结构化的、假设依赖的初始条件，这些条件先于目标驱动的群体反应。支持这一点的是，行为准确性和行为反应时间都由任务有效子空间内早期群体运动的方向预测。我们得出结论，期望驱动群体反应变异性的预期性组织，形成结构化的、行为相关的几何形状，将随后的群体活动预置在任务有效流形上，以支持快速、准确的行为结果。

## Abstract
Expectations guide behavior and shape sensory responses in single neurons, but their influence on population-level neural dynamics is unknown. Here, we employ a dynamical systems framework to examine the collective spiking activity of neuronal populations in the auditory forebrain of European starlings, a species of songbird, as they categorize natural song syllables while sensory expectations are manipulated. We show first that sensory-driven neural population spiking activity traces smooth, low-dimensional latent trajectories that closely reflect the identity of sensory signals. Like the stimulus-driven responses of single neurons, the geometry of the population trajectories is also modulated by expectation. In single neurons, expectation sharpens differences between responses to signals in the same category, but at the population-level the effect is opposite: expectation increases the similarity between responses to signals in the same category. To understand how population-level response dynamics can differ from those in single neurons, we develop (and test empirically) a dynamical model that relates spiking activity at these two biological scales. The model leverages response redundancy between neurons, a capacity we term degeneracy-enabled remapping, and enables the observed simultaneous expectation-dependent increases in the separability of single-neuron responses \textit{and} decreases in the separability of population trajectories in the task-potent subspace, i.e., the population activity dimensions tied to behavioral categorization. Examining the relationship between expectation-modulated population trajectories and behavior in detail, we find that single-trial categorization errors are tied to drift in the trajectory toward the opposing task-potent manifold. This suggests that expectations help establish structured, hypothesis-dependent initial conditions that precede the target-driven population response. In support of this, both behavioral accuracy and behavioral reaction time are predicted by the direction of early population motion within the task-potent subspace. We conclude that expectation drives anticipatory organization of population response variability into a structured, behaviorally relevant geometry that pre-positions subsequent population activity on task-potent manifolds to support rapid, accurate, behavioral outcomes.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **核心问题**：期望（expectation）如何塑造感觉皮层的**群体神经动力学**，这种群体层面的组织如何与单神经元反应产生差异，并最终影响行为决策的速度与准确性。
- **整体含义**：该研究揭示了感觉群体活动中一种**预期性组织原理**：预测性线索使神经群体在任务有效子空间内预先偏向正确的分类流形，同时利用神经元间的简并性将单细胞反应变化约束到行为无关的“空”子空间中。这解释了为何期望能在增强单神经元辨别力的同时压缩群体轨迹，从而实现快速、准确的行为分类。这项工作将运动系统中经典的准备活动（preparatory activity）概念推广至感觉加工，表明感知决策同样依赖于群体活动在行为相关维度的预先排列。

### 2. 方法论
- **核心思想**：采用动态系统框架与降维技术，将同时记录的神经元群体放电活动投射到低维潜在空间，分析轨迹几何如何随期望变化。并提出**简并性重映射模型**来解释单神经元与群体水平的反向效应。
- **关键技术细节**：
  - **群体轨迹构建**：对多神经元放电序列（20 ms bins，高斯平滑）进行主成分分析（PCA），取前8个主成分构建低维潜在轨迹。然后计算同一类别刺激轨迹之间的成对余弦相似度（CS）。
  - **任务有效与空子空间分解**：使用线性解码器（L2正则逻辑回归）从群体活动中识别区分类别A/B的**任务有效轴** $\mathbf{u}_{\text{task}}$。将群体位移分解为沿该轴的**有效分量**和与之正交的**空分量**，并定义空分数（null fraction）衡量位移在空子空间中的占比。
  - **简并性重映射模型**：一个低维潜在状态 $\mathbf{x}_t$ 按 $\mathbf{x}_{t+1}=\mathbf{A}\mathbf{x}_t+\mathbf{u}_t+\boldsymbol{\varepsilon}_t$ 演化，读出权重矩阵 $\mathbf{W}(t)$ 在目标刺激窗口内旋转：
    $$\mathbf{W}(t)=(1-\alpha_t)\mathbf{W}_{\text{pre}} + \alpha_t\mathbf{W}_{\text{post}}$$
    $\mathbf{W}_{\text{post}}$ 的更新分解为有效与空分量，有效线索下更新集中在空子空间（$\|\Delta\mathbf{W}_{\text{null}}\| \gg \|\Delta\mathbf{W}_{\text{potent}}\|$），无效线索下则反之。该机制使群体轨迹在任务有效轴上保持紧凑，而单神经元活动模式大幅变化。
  - **行为关联分析**：基于“无线索试次”训练的决策轴，计算试探次在有效轴上的符号边距（signed margin），并分析预刺激期的群体状态与反应时间的关系。

### 3. 实验设计
- **数据集与场景**：
  - **动物与脑区**：10只欧洲椋鸟（7只用神经记录）。记录区域包括听觉前脑的**field L、CMM、NCM**，使用32/64通道硅探针，共提取7524个单单元，形成201个同时记录的神经群体（每组10‑170个神经元）。
  - **行为任务**：操作式分类任务，受试者需将9条合成音节连续体上的目标音节分为A/B两类。引入预测性线索音节（概率80%有效，20%无效），线索概率强度被操纵以保持目标主导性。同时设置无线索条件以及被动播放对照（动物仅听不操作）。
- **对比的基准与方法**：
  - 主要对比条件：**有效线索 vs 无效线索**；主动操作 vs 被动播放。
  - 分析尺度：单神经元反应（放电率向量余弦相似度）vs 群体轨迹（PCA轨迹余弦相似度）。
  - 模型验证对比：仿真模型是否复现数据中的尺度依赖效应？是否预测空分数、子空间旋转、噪声相关等指标？均逐一检验。
  - 行为关联：比较不同线索条件下的心理测量函数移动、反应时间分布，并将单试次群体运动方向与行为准确率和反应时间对应。

### 4. 资源与算力
- 文中**未明确提及算力**。分析在Python（NumPy, SciPy, statsmodels, scikit-learn等）中运行，神经群体PCA、线性混合效应模型及模型仿真计算规模适中，无GPU需求。模型仿真仅使用CPU完成（种子固定），没有说明所用硬件或计算时间。

### 5. 实验数量与充分性
- **数据量庞大且多层次**：
  - 行为：10只受试，共2,434,924试次；神经记录：225个记录日，7524单单元，201个神经群体。
  - 统计检验普遍采用**线性混合效应模型（LME）**，包含受试者随机截距与群体随机截距，确保推断对受试者泛化。每一主要发现均附有受试者水平的非参数检验交叉验证。
  - 多层次实验对比：单神经元 vs 群体，有效 vs 无效，主动 vs 被动，正确 vs 错误试次，以及模型仿真 vs 实证数据。
  - 稳健性分析：使用多种子空间维度（k=2‑6）检验旋转效应，多种预刺激稳定性测量预测反应时间，补充材料非常详尽。
- **充分性与客观性**：
  - 实验设计通过平衡刺激组成（分层匹配试次）、采用独立解码器轴（无线索试次训练）避免循环分析；被动播放对照排除了纯刺激驱动的可能。总体实验数量充足，对比公平，统计控制严谨。

### 6. 主要结论与发现
- **尺度依赖的反向效应**：期望效应在单神经元水平表现为同类刺激反应相似性**降低**（锐化），而在群体轨迹水平表现为同类刺激相似性**升高**（压缩）。这一差异要求任务主动参与，被动播放时消失。
- **简并性重映射的组织原则**：有效线索使群体位移集中到空子空间（null fraction 更高），减少任务有效子空间的旋转。同时，有效线索增加了噪声相关性并重分配方差到前几个主成分，但不改变整体维度（参与率不变）。
- **行为预测**：有效线索使群体活动在任务有效轴上更偏向正确类别侧；分类错误与轨迹向相反类别有效轴的漂移显著相关。预刺激期群体状态与反应时间强相关：距离预刺激子空间更近或方差更小的试次，反应更快。
- **主动任务依赖**：上述所有神经效应在被动播放条件下均消失，确认其为自上而下期待驱动，而非纯感觉驱动。

### 7. 优点
- **创新的多尺度对比与理论统一**：首次在同一数据集上同时揭示单神经元与群体水平的期望效应反差，并用简并性重映射模型提供了机制性解释，弥合了感觉加工领域中的常见分歧。
- **跨区域、跨状态验证**：包含三条听觉通路区域，并设置主动/被动对照，实验设计严谨，排除了刺激驱动混淆。
- **群体几何与行为直接关联**：将群体动态分解为任务有效与空分量，并成功预测单试次行为误差和反应时间，实现了神经‑行为闭环。
- **模型预测的可检验性**：提出的模型不仅复现尺度效应，还对空分数、子空间旋转、噪声相关模式等给出定量预测并全部获得实证支持。

### 8. 不足与局限
- **区域分辨率受限**：探针常跨越多个脑区，无法精确定位每个单元，导致区域比较（如NCM vs CMM vs Field L）缺乏统计效力，尤其是Field L仅有2只受试。
- **模型为现象学而非电路机制**：简并性重映射模型是自顶向下的描述性构造，未从突触连接、细胞类型或具体反馈回路推导，未模拟产生线索信号的来源。
- **任务相对简单**：行为只涉及二元分类和两种线索概率，可能难以推广至更复杂的多线索、连续期望变化的任务。
- **普适性待验证**：实验仅在鸣禽听觉前脑中开展，未在其他物种或感觉模态中验证。
- **未与增益调制等解释充分对比**：论文虽讨论了与均匀增益模型的区别（如噪声相关和方差谱），但未在实证数据中直接排除或对比该替代假说的定量预测。

（完）
