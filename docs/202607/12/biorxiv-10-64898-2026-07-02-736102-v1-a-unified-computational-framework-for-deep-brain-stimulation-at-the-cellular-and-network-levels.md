---
title: A Unified Computational Framework for Deep Brain Stimulation at the Cellular and Network Levels
title_zh: 深部脑刺激在细胞与网络水平的统一计算框架
authors: "Crompton, D. B., Milosevic, L., Lankarany, M."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736102v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 建模深部脑刺激对神经回路放电活动的调节
tldr: 本文提出一个统一的深部脑刺激计算框架，整合电刺激参数与实验约束，在细胞和网络层面研究DBS机制。模型分析刺激核团神经元放电活动受突触强度、密度及回路架构的影响，设计编码器揭示不同架构下的编码模式，并探索神经同步在下游回路中的传播。结果表明DBS效应取决于内在特性、架构组织和突触后回路 motif，为优化临床刺激参数提供了机制性见解。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-003.webp\", \"caption\": \"Fig 1. Deep Brain Stimulation Simulation framework. The motivation and underlying features of the abstraction of DBS. a) Schematic representation of a common network, the basal ganglia, where DBS is delivered. b) The cellular and synaptic features that an abstraction of DBS must account for, intensity recruitment, synaptic failure/stochasticity, and frequency dependent activity e.g. plasticity. c) The interaction of DBS with circuit architecture, feed-forward, lateral inhibition, recurrent inhibition. d) The meso-circuit properties, the interaction of DBS with connection sparsity and strength.\", \"page\": 3, \"index\": 3, \"width\": 752, \"height\": 326}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-005.webp\", \"caption\": \"Fig 2. Visualization of placement of parrot neurons preceding all efferent and afferent synapses, and connectivity to the DBS spike generator. Axonal (λ) and synaptic (δ) latencies are depicted. Arrows below depict the propagation direction induced by DBS, where λSxy represents the antidromic propagation time\", \"page\": 4, \"index\": 5, \"width\": 1128, \"height\": 460}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-004.webp\", \"caption\": \"Fig 4. Deep Brain Stimulation Exemplary Motif. Spike rasters of the stimulated (bottom half) and efferent population (top half) are shown under three conditions for the first 10 pulses of stimulation. DBS parameters such as frequency and recruitment fidelity are shown in the columns and rows respectively.\", \"page\": 8, \"index\": 4, \"width\": 752, \"height\": 806}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-007.webp\", \"caption\": \"Fig 5. Stimulation-connectivity interaction. Influence of network sparsity and connectivity strength on the spiking activity in a feed-forward network model. The left figure represents the synchrony of spiking activity with respect to connection probability on the x-axis, and synapse strength on the y-axis. The rasters depict exemplary inter-stimulus interval raster plots of the first pulse of DBS on the efferent population, with lines indicating to the figure on the left what the sparsity and strength values were. a Low connectivity and low strength, b low strength and medium connectivity, c medium strength and medium connectivity, d high strength and high connectivity.\", \"page\": 9, \"index\": 7, \"width\": 713, \"height\": 277}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-008.webp\", \"caption\": \"Fig 6. Properties of the inter-stimulus interval in a feed forward network. In all plots, the x-axis is connection probability, and the y-axis is synapse strength. a) The feature is spike synchrony (standard deviation). b) The features is number of peaks that surpass 250 Hz. c) Amplitude of the second peak response in the ISI normalized to the baseline, pre-stimulus, firing rate. Below b) & c) are example traces of instantaneous ISI firing rates as connectivity is varied, with maximal synapse strength.\", \"page\": 9, \"index\": 8, \"width\": 714, \"height\": 422}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-002.webp\", \"caption\": \"Fig 7. Circuit motif influence. Inter-stimulus spike synchrony with respect to connection probability on the x-axis, and synapse strength on the y-axis. a) Synchrony of the ISI in a feed-forward motif, as in Figure 5. b) Synchrony of the ISI in a network with lateral inhibition. c) Synchrony of the ISI in a network with recurrent inhibition.\", \"page\": 10, \"index\": 2, \"width\": 712, \"height\": 424}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-001.webp\", \"caption\": \"Fig 8. Evoked Field Oscillations. This figure depicts how certain motifs may give rise to oscillations that are a function of downstream connectivity that is modulated by DBS to give rise to an oscillatory or patterned response. a) is the feature space the model was simulated in. b) is the raster (black) and LFP (green) of the first 10 pulses to high frequency DBS\", \"page\": 11, \"index\": 1, \"width\": 710, \"height\": 273}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736102-v1/fig-006.webp\", \"caption\": \"Fig 9. Evoked Field Oscillations Modulated by Stimulation Parameters. How delayed local evoked potentials (DLEPs) are effected by different stimulation parameters such as stimulation intensity (column)1 and frequency (row).\", \"page\": 12, \"index\": 6, \"width\": 714, \"height\": 737}]"
motivation: 现有DBS计算模型在微/中观回路激活研究上受限，需开发一种不依赖详细纤维束表征、普适且可集成详细模拟的现象学方法。
method: 构建整合电刺激和突触/细胞约束的全面现象学模型，模拟同质神经元群体活动，系统改变突触连接强度与密度，并利用简单编码器分析下游网络中的活动传播与同步。
result: DBS调制活动受三项关键因素塑造：刺激核团内在突触和细胞特性、突触连接强度与密度的架构组织、以及突触后目标构成的回路motif，不同架构呈现独特编码模式。
conclusion: 该统一框架为理解DBS在神经元网络中的表征与传播提供了机制性解释，有望指导临床刺激参数优化。
---

## 摘要
深部脑刺激（DBS）已被证明是治疗神经系统疾病的一种成功干预手段，但其对神经元回路影响的机制仍不完全清楚。在本研究中，我们提出了一个全面的现象学计算模型，该模型考虑了电刺激参数对神经元回路的影响，同时纳入了实验验证的突触和细胞约束。我们研究了DBS脉冲如何调节代表受刺激核团的同质神经元群体的放电活动，系统地考察了回路结构的影响，包括突触连接强度（弱 vs 强）和组织（稀疏 vs 丰富）。为了表征DBS调节的神经元活动如何通过下游网络传播，我们开发了一个简单的编码器，揭示了受刺激核团的不同构型所产生的不同编码模式。

此外，通过将受刺激核团连接到循环连接的神经元群体，我们考察了DBS调节的神经元同步化在各种回路基序上的传播。我们的结果表明，三个关键因素塑造了DBS调节的神经元活动：(a) 受刺激核团的内在突触和细胞特性，(b) 受刺激核团在突触强度和连接密度方面的构型组织，(c) 受刺激核团的突触后靶点形成的回路基序。这一统一模型为理解DBS在神经元网络中的表征和传播提供了机制框架，为优化临床应用中的刺激参数提供了见解。

作者总结：深部脑刺激的计算模型已被证明在解开多种疾病治疗中观察到的临床益处和副作用方面极具价值。尽管如此，许多现有的计算模型解释微/中观回路激活的能力仍然有限，因为主要技术依赖于对DBS电极周围纤维束的详细表征，或依赖于非生理约束的注入电流来模拟电刺激的影响。基于纤维束的方法仅适用于我们有详细表征的纤维束，但许多靶结构如基底神经节缺乏这些表征。鉴于当前方法的局限性，我们着手定义一个现象学方法，该方法适用于尽可能多的模拟方法，包括那些缺少纤维束成像细节的方法，同时能够在获得详细模拟结果时随时整合。我们的方法具有可扩展性，并在一些最流行的计算神经科学工具包中实现了示例，便于集成到现有网络模拟中。此外，我们展示了该方法如何支持对网络的生理响应以及计算动力学（如信息多路复用和延迟局部诱发电位）的探究。

## Abstract
Deep brain stimulation (DBS) has been demonstrated to be a successful therapeutic intervention for neurological disorders, yet the mechanisms underlying its effects on neuronal circuits remain incompletely understood. In this study, we propose a comprehensive phenomenological computational model that accounts for the impact of electrical stimulation parameters on neuronal circuits while incorporating experimentally-validated synaptic and cellular constraints. We investigate how DBS pulses modulate spiking activity in populations of homogeneous neurons representing stimulated nuclei, systematically examining the influence of circuitry architecture, including synaptic connectivity strength (weak vs. strong) and organization (sparse vs. rich). To characterize how DBS-modulated neuronal activity propagates through downstream networks, we develop a simple encoder that reveals distinct encoding patterns arising from different architectural configurations of stimulated nuclei.

Furthermore, by connecting stimulated nuclei to recurrently connected neuronal populations, we examine the propagation of DBS-modulated neuronal synchrony across various circuit motifs. Our results demonstrate that three critical factors shape DBS-modulated neuronal activity: (a) the intrinsic synaptic and cellular properties of stimulated nuclei, (b) the architectural organization of stimulated nuclei in terms of synaptic strength and connectivity density, and (c) the circuit motifs formed by postsynaptic targets of stimulated nuclei. This unified model provides a mechanistic framework for understanding DBS representation and propagation in neuronal networks, offering insights that may inform optimization of stimulation parameters for clinical applications.

Author summaryComputational models of deep brain stimulation have proven to be supremely useful in disentangling the clinical benefits and adverse effects observed in the treatment of a variety of conditions. Despite this, the capacity for many of the existent computational models to account for micro/meso-circuit activation remains limited, as the major techniques rely on detailed characterization of tracts surrounding the DBS electrode, or depend on an non-physiologically constrained injected current intending to mimic the influence of electrical stimulation. The tract based methods only work for tracts that we have detailed characterization of, which are missing for many of the target structures, such as the basal ganglia. Given the restrictions of current methods we set out to define a phenomenological method that is applicable to as many simulation methods as possible, including those with missing details on tractography, while being able to readily integrate results of detailed simulations when available. Our approach is extensible and has examples implemented in some of the most popular computational neuroscience toolkits allowing for ready integration into existing network simulations. Further we demonstrate how this methodology supports interrogation of networks both for physiological responses but also computational dynamics, such as information multiplexing and delayed local evoked potentials.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义
*   **研究背景与动机**：深部脑刺激（DBS）是一种有效治疗神经性运动障碍（如帕金森病）的疗法，但其对复杂神经元回路的调控机制尚不完全清楚。现有DBS计算模型存在局限：
    *   **详尽的生物物理模型**：依赖对电极周围白质纤维束（如基底节内通路）的精细三维表征，计算成本极高，难以用于大规模网络研究。
    *   **抽象的模型**：通常简化为注入超阈值电流或修改群体放电率函数，可能忽略由轴突激活引起的逆向激活、体-轴突解耦等重要效应。
*   **核心问题**：如何构建一个既能在计算上高效模拟大规模网络活动，又能灵活且完整地捕捉DBS引发的复杂细胞和突触层面效应的统一计算框架。
*   **整体含义**：本研究旨在提出一个具有普适性的现象学方法，该方法不依赖于对脑内纤维束的精确几何重建，可作为一种标准组件无缝集成到现有的各类脉冲神经网络模拟平台中，以系统性地探究DBS在不同网络架构下的信息表征与传播机制。

### 论文提出的方法论
*   **核心思想：直接突触激活**
    *   模型的核心不是向神经元胞体注入电流，而是根据DBS脉冲时间，直接向受电刺激影响的神经元群（核团）的传入、传出和逆向突触传递信号。
    *   该方法无需DBS专属的电流生成，刺激效应完全继承所激活突触自身的动态特性（如短时程可塑性）。
*   **关键技术细节：“鹦鹉神经元”中介**
    *   为兼容如NEST、Brian等不允许直接向突触递送事件的模拟器，在所有传入和传出突触前插入一个中介“鹦鹉神经元”。该类神经元只简单地重复它接收到的每一个脉冲，从而将DBS诱导的脉冲与该神经元的生理性脉冲合并。
*   **算法流程**
    1.  **定义靶点**：确定受刺激的最大神经元群体（$Net$）。
    2.  **选择激活子集**：通过应用特定函数 $Choose(Net)$，基于刺激参数（强度、脉宽等，对应激活组织体积VAT）决定每个脉冲具体激活的神经元和突触子集。此过程由招募概率 $p_{act}, p_{eff}, p_{aff}, p_{anti}$ 等控制。
    3.  **计算并递送脉冲时间**：对于DBS脉冲序列中的每个时刻 $t$：
        *   **传出突触激活**：靶点神经元到下游神经元的突触（$S_{jx}$）在 $t + \lambda_{S_{jx}} + \delta_{S_{jx}}$ 被激活，其中 $\lambda$ 为轴突传播延迟，$\delta$ 为突触传递延迟。
        *   **传入突触激活**：上游神经元到靶点神经元的突触（$S_{xi}$）在 $t + \delta_{S_{xi}}$ 被激活。
        *   **逆向激活**：传入突触的轴突被逆向激活，脉冲在 $t + \lambda_{S_{xi}}$ 到达上游神经元胞体后，再经其传出突触（$S_{ji}$）在 $t + \lambda_{S_{xi}} + \lambda_{S_{ji}} + \delta_{S_{ji}}$ 激活更上一级网络。
*   **模型整合**
    *   **神经元模型**：采用泄漏整合发放（LIF）模型，其膜电位 $V$ 动态方程为 $C_m \frac{dV}{dt} = -g_L(V - E_L) + I_{syn}$。
    *   **突触动态**：突触电流 $I_{syn}$ 使用Alpha核函数建模，并集成了Tsodyks-Markram短时程可塑性模型，通过变量 $x, y, z, u$ 描述突触的资源耗竭（抑制）和利用率变化（易化），使刺激的效果能够被频率和脉冲历史动态塑造。

### 实验设计
*   **仿真环境与基准**：
    *   实验在NEST脉冲神经网络模拟器中完成。
    *   网络基础为LIF神经元模型，除特殊说明外，每个神经元群都接收来自10个兴奋性和2个抑制性Poisson脉冲发生器的背景输入。
    *   本研究并非与现有其他DBS模型进行定量基准对比，而是旨在展示提出的框架在不同场景下对网络动力学进行定性分析和“质询”的能力。
*   **探究场景与对比设计**：
    1.  **验证基本效应与可塑性交互**：构建一个包含短时程抑制和易化突触的双兴奋群体前馈-循环网络，在不同刺激频率（25Hz vs. 100Hz）和强度（低20% vs. 高80%招募率）下，观察受刺激群和传出群的放电栅图（raster）变化。这实质上是对比了不同刺激参数与突触频率依赖性交互的结果。
    2.  **信息编码与架构依赖性分析**：在前馈网络中，系统性地改变连接概率（稀疏度）和突触强度（弱 vs. 强），构成一个参数空间。在此空间中，考察并编码了三个特征：脉冲同步化（标准差）、高频功率峰值数量（频率编码）和归一化的第二峰幅度（归一化放电率编码）。这对比了不同的编码模态如何受网络连接构型影响。
    3.  **回路基序（motif）的影响**：在三种不同的回路基序（纯前馈、带侧抑制的前馈、带循环抑制的前馈）中，重复上述参数空间分析，比较脉冲同步化模式的差异。
    4.  **局部场电位（LFP）样响应分析**：在包含短时程易化的循环网络中，模拟不同频率（10, 50, 100 Hz）和强度（低、高）的刺激，观察并比较所诱发LFP样信号的振荡、延迟局部诱发电位（DLEPs）等波形特征。

### 资源与算力
*   论文中**未明确说明**进行仿真实验所使用的具体计算资源，如GPU型号、数量或CPU核心数，也未提及运行各个场景所需的训练时长或模拟时长。

### 实验数量与充分性
*   **实验组数量**：论文设计了多组概念验证性仿真，通过系统性地扫描参数空间（例如，连接度与强度的二维空间）和在数个关键回路基序上重复实验，构成了较为立体的定性分析。
*   **实验充分性与客观性**：
    *   **充分性**：实验充分展示了所提框架在捕捉DBS频强依赖效应、可塑性交互、不同编码模式的网络架构敏感性、以及复杂波形生成方面的能力，有效证明了其作为通用“质询”工具的灵活性。目标主要是概念验证，实验数量足够支撑其论点。
    *   **客观性与公平性**：作为一项方法论论文，其重点在于提出并示范新方法的应用，而非在特定任务上与现有方法比出“最优”。因此，缺乏严格的定量基准对比并不违背其研究性质。但其内部对比实验（如不同参数、不同基序）是系统、公平且客观的。最大的“不公平”风险在于，比较对象是特定的、高度简化的理论回路，而非真实的解剖或生理数据。

### 论文的主要结论与发现
*   **三要素塑造DBS效应**：在受刺激核团中，DBS调节的神经元活动由三个关键因素共同决定：
    1.  核团内在的细胞和突触特性（如短时程可塑性）。
    2.  核团的架构组织，特别是突触连接的强度和密度。
    3.  突触后目标群体形成的回路基序类型。
*   **架构与编码的关联**：网络连接的稀疏度和强度显著影响DBS效应的编码模式。例如，在纯前馈网络中，纯放电率编码与功能性连接强度呈单调递增关系，而时间精度和归一化放电率编码则呈现出非单调关系。不同回路基序（如前馈、侧抑制、循环抑制）彻底改变了时间精度与连接参数的“关系图景”。
*   **频率-频率交互**：突触的短时程可塑性（如易化或抑制）与刺激频率有强烈的相互作用，这解释了为何低强度、低频刺激可能无法招募传出群体，而高频刺激即使在低强度下也能通过累积易化效应实现招募。
*   **振荡与LFP的产生**：特定的回路基序（如带短时程易化的循环网络）能在特定高频/高强度DBS下，产生类似临床观察到的延迟局部诱发电位（DLEPs）和振荡行为，揭示了这些临床现象可能的网络机制。

### 优点
*   **高通用性与可移植性**：方法不限定特定的神经元或突触模型，可作为“即插即用”模块集成到NEST、Brian等多个主流脉冲神经网络模拟平台，解决了现有方法普适性差的问题。
*   **计算高效，可研究大规模网络**：通过将刺激效应简化为直接递送突触事件，避免了求解复杂电场或注入人工电流，极大地降低计算负荷，使得探索大规模群体动力学变得可行。
*   **生理约束性强**：通过直接作用于突触，该框架自然地继承了突触的短时程可塑性、释放概率（随机招募）和传导延迟等关键生理特性，更真实地反映了DBS与神经网络的交互，特别是频率依赖性效应。
*   **机制探索能力强**：提供了一个系统化“质询”网络的框架，能够解耦并研究网络架构（连接强度/密度）、回路基序和神经元内在特性等因素如何独立且协同地塑造DBS的输出。

### 不足与局限
*   **缺乏定量实验验证**：所有结论均基于理论仿真，没有与实际的在体动物实验或临床记录数据进行直接对比和参数拟合，模型预测的有效性有待实证检验。
*   **依赖前置的参数设定**：被激活神经元和突触子集的决定依赖于用户定义的`Choose`函数，该函数的准确性取决于对激活组织体积（VAT）或纤维招募模式的外部先验知识，若该前置步骤不准确，整个模拟结果将出现偏差。
*   **忽略阈下效应**：该方法仅考虑了DBS引起的脉冲产生和传递，未考虑电场对神经元胞体膜电位造成的阈下波动，这可能改变了神经元的兴奋性状态。
*   **潜在的计算开销**：插入鹦鹉神经元虽然实现了兼容性，但在大型密集连接的网络中，可能导致模拟中需要传递和处理的脉冲事件数量大幅增加，反而引入计算开销，减慢仿真速度。
*   **实验覆盖的局限性**：仿真研究仅探索了极简的、同质的回路基序，未在更复杂、更具异质性的网络（如基底节整体模型）中进行验证，其结论向真实神经系统的推广程度尚不明确。

（完）
