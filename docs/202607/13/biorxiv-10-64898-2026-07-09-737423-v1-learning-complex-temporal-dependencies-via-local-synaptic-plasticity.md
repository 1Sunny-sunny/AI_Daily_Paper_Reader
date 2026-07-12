---
title: Learning complex temporal dependencies via local synaptic plasticity
title_zh: 通过局部突触可塑性学习复杂的时间依赖性
authors: "Ng-Kee-Kwong, J., Tang, M., Akam, T., Bogacz, R."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.09.737423v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 研究通过局部突触可塑性学习时间依赖性的时间预测编码
tldr: 本文研究生物可行的局部突触可塑性规则如何学习复杂时间依赖关系。通过分析时间预测编码(tPC)框架，揭示其与通过时间反向传播(BPTT)变体、储层计算和资格传播的关系，证明tPC仅用局部赫布更新即可实现梯度截断式时间学习，并利用分层动力学和资格迹处理长程依赖与抗干扰任务，表明简单递归网络可支持更复杂的时间学习。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-004.webp\", \"caption\": \"Fig 1. Temporal predictive coding model. a: Graphical model of tPC, in which the output yt depends on the hidden state zt, which in turn depends on the input xt and the previous hidden state zt−1. b: Possible circuit implementation of tPC using value and error units, which represent estimates of latent or observed variables and the discrepancy between neural activity and its top-down prediction, respectively.\", \"page\": 4, \"index\": 4, \"width\": 752, \"height\": 429}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-003.webp\", \"caption\": \"Fig 2. tPC inference induces implicit flow of information from observation to hidden state. a: Comparison of three models on the position estimation task: tPC, RNN, and RNN-P. Red arrows indicate flow of information from observation to hidden state. b: Schematic of the position estimation task, in which the model must predict the particle’s new position at each time step given a velocity input sampled from a standard Gaussian distribution (µ = 0, σ = 1). c: Training loss curves for the position estimation task, showing that a standard RNN trained using tBPTT1 fails to learn the task. d: Predicted particle trajectories for a representative sequence of velocity inputs, illustrating that both the tPC and RNN-P models can closely reproduce the target trajectory.\", \"page\": 8, \"index\": 3, \"width\": 752, \"height\": 729}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-007.webp\", \"caption\": \"Fig 3. tPC shapes reservoir dynamics via local plasticity to facilitate downstream readout from the reservoir. a: The reservoir computing framework typically uses an RNN with fixed input and recurrent weights. Only the output weights are trained, as indicated by the dashed lines. b: Training loss curves for the alternating two-state task given a block length of either 2 or 4. tPC substantially improves performance over standard reservoir computing as the task becomes more difficult. c: Visualisation of tPC hidden state trajectories in the space of the first two principal components (PC1 and PC2) before and after training.\", \"page\": 9, \"index\": 7, \"width\": 752, \"height\": 866}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-006.webp\", \"caption\": \"Fig 4. tPC-H supports learning of complex temporal dependencies through hierarchical recurrent dynamics. a: Comparison between tBPTT and tPC-H. On the left, the coloured arrows indicate which temporal influences are included when computing gradients of the loss using tBPTT, with progressively lighter shades of blue corresponding to longer truncation horizons. In tPC-H, the orange arrows instead indicate the local influences at each hierarchical levels that contribute to the gradient computation. b: Training loss curves for the delayed 3-bit and 4-bit parity tasks, highlighting how hierarchical recurrent dynamics may provide an alternative to tBPTT for learning more complex temporal dependencies.\", \"page\": 12, \"index\": 6, \"width\": 752, \"height\": 637}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-002.webp\", \"caption\": \"Fig 5. tPC-H confers robustness to strong distractors through selective temporal integration. a: Schematic of the distractor task, where the model is cued with one of two possible signals and then exposed to an intervening distractor before receiving a ‘Go’ prompt. b: Training loss curves for the distractor task, assuming either weak (σ = 1) or strong (σ = 10) distractors. As distractor strength was increased, the standard tPC model failed to reproduce the original cue.\", \"page\": 13, \"index\": 2, \"width\": 752, \"height\": 533}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-001.webp\", \"caption\": \"Fig 6. tPC-E enables long temporal gaps to be bridged via eligibility traces. a: In the absence of eligibility traces, Hebbian plasticity depends on the simultaneous activity of neurons encoding the input and the error signal. By contrast, eligibility traces preserve a transient synaptic memory of past activity, allowing later learning signals to drive plasticity. Hence in the presented example, the first prediction error in the right display triggers plasticity as the eligibility trace maintains memory of recent activity in the input. b: Schematic of the delayed response task, where each trial begins with the presentation of one of two possible cues, which the model had to reproduce after a delay of variable duration. Trials were separated by an inter-trial interval (ITI) of variable length (1 to 3 time steps). c: Training loss curves for the delayed response task, assuming either a short delay (1 to 5 time steps) or long delay (5 to 10 time steps). Eligibility traces were necessary for the model to recover the original cue even after short delays, although RFLO performance saturated as the delay length increased.\", \"page\": 15, \"index\": 1, \"width\": 752, \"height\": 866}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737423-v1/fig-005.webp\", \"caption\": \"Fig 7. Relationship between different algorithms. tPC is closely related to several established frameworks for learning temporal dependencies. In this work, we showed that tPC is functionally equivalent to tBPTT1, both of which extend the reservoir computing framework by introducing plasticity at the input and recurrent weights. tPC can also be combined with eligibility traces or hierarchical recurrent dynamics, giving rise to tPC-E and tPC-H, respectively. Eligibility traces had previously been explored in RNNs through eligibility propagation (e-prop), which can be made more biologically plausible by incorporating random feedback weights (RFLO). More generally, tBPTT remains the standard training procedure for RNNs, using a truncated backward pass of length k. In contrast to the aforementioned algorithms, BPTT and RTRL compute exact gradients by propagating error through the full sequence or by accounting for all possible dependencies, respectively. Arrows denote modifications from one model to the next, with top-to-bottom progression indicating an improvement in prediction accuracy over the preceding model.\", \"page\": 17, \"index\": 5, \"width\": 752, \"height\": 497}]"
motivation: 现有时间学习模型依赖生物合理性有限的BPTT，需探索符合局部可塑性原则的高效时间依赖学习机制。
method: 基于时间预测编码(tPC)框架，建立其与tBPTT1、储层计算和资格传播的理论联系，并通过分层递归网络和资格迹扩展tPC的能力。
result: tPC与仅回传一步梯度的tBPTT1功能等价，能够利用储层动态编码短期上下文、塑造神经轨迹，分层架构可学习复杂依赖且抗干扰，加入资格迹后可解决长时程任务。
conclusion: 遵循局部突触可塑性的简单递归网络，如tPC，能在比以往认知更复杂的情境下实现时间学习。
---

## 摘要
在各种任务中提取和利用时间结构的能力是人类认知的核心。神经科学家在建模决策和运动控制等神经与行为过程时，通常依赖通过时间反向传播（BPTT）训练的循环神经网络（RNN）。然而，该算法的生物学合理性有限，因此高效学习时间依赖性的计算原理仍未解决。在此，我们研究时间预测编码（tPC），这是一个最近提出的框架，它将预测编码扩展到时间领域，同时保留了局部的赫布更新规则。我们分析并扩展了tPC，以建立其与RNN中几种有影响力的学习计算模型的关系，包括BPTT、储备池计算和资格传播（e-prop）。我们首先证明了tPC与tBPTT1之间的功能等价性，tBPTT1是BPTT的一种变体，其中梯度仅向过去传播一个时间步长。然后我们表明，tPC可以利用储备池动力学来编码短程时间上下文，并同时在状态空间中塑造神经轨迹以支持下游读出。我们进一步证明，层次化的循环动力学可以促进学习更复杂的时间依赖性，同时对强干扰提供鲁棒性。最后，我们展示tPC网络可以通过生物启发的资格迹增强，以解决时间上扩展的上下文依赖任务。这些结果共同揭示，由局部可塑性控制的相对简单的循环网络可以在比以前认为的更复杂的环境中支持时间学习。

## Abstract
The ability to extract and exploit temporal structure across diverse tasks is central to human cognition. Neuroscientists have typically relied on recurrent neural networks (RNNs) trained with backpropagation through time (BPTT) when modelling neural and behavioural processes such as decision-making and motor control. However, this algorithm has limited biological plausibility, hence the computational principles underlying efficient learning of temporal dependencies remain unresolved. Here, we investigate temporal predictive coding (tPC), a recently proposed framework that extends predictive coding to the temporal domain while preserving local Hebbian update rules. We analyse and extend tPC to establish its relationship with several influential computational models of learning in RNNs, including BPTT, reservoir computing, and eligibility propagation (e-prop). We first demonstrate a functional equivalence between tPC and tBPTT1, a variant of BPTT in which gradients are propagated only one time step into the past. We then show that tPC can leverage reservoir dynamics to encode short-range temporal context, and simultaneously sculpt neural trajectories in state space to support downstream readout. We further demonstrate that hierarchical recurrent dynamics can facilitate learning of more complex temporal dependencies, while additionally conferring robustness to strong distractors. Finally, we show that tPC networks can be augmented with biologically inspired eligibility traces to solve temporally extended context-dependent tasks. Together, these results reveal that relatively simple recurrent networks governed by local plasticity can support temporal learning in more complex settings than previously appreciated.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：人类能够利用时间结构完成序列预测、决策等任务。在计算神经科学中，通常使用通过时间反向传播（BPTT）训练的循环神经网络（RNN）来建模这类过程。然而，BPTT需要存储过去状态并沿时间反向传播误差，被认为在生物学上不合理。
- **核心问题**：能否设计出一种仅依赖局部突触可塑性（类似赫布规则）的循环网络学习机制，使其能够解决需要复杂时间依赖的任务？
- **整体含义**：本文以“时间预测编码”（tPC）框架为基础，首先建立其与BPTT截断版本（tBPTT1）的理论联系，然后通过引入分层动态和资格迹，展示即使是遵循局部学习规则的简单循环网络，也能在比以往认为更复杂的时间场景下实现高效学习。

## 2. 论文提出的方法论

- **核心思想**：tPC 将预测编码扩展到时间域。其生成模型假定隐状态 $z_t$ 依赖上一时刻隐状态 $z_{t-1}$ 和当前输入 $x_t$，观测 $y_t$ 由 $z_t$ 线性或非线性生成：
  $$
  z_t = f(A z_{t-1} + B x_t) + \omega_z,\quad y_t = C z_t + \omega_y
  $$
  其中 $\omega_z,\omega_y$ 为高斯噪声。通过最小化变分自由能
  $$
  F_t = \frac{1}{2}\|\epsilon_z\|^2 + \frac{1}{2}\|\epsilon_y\|^2,
  $$
  其中 $\epsilon_z = z_t - f(A z_{t-1} + B x_t)$、$\epsilon_y = y_t - C z_t$。推断（更新 $z_t$）和学习（更新权重 $A,B,C$）交替进行，所得到的权重更新规则满足局部可塑性：
  $$
  \Delta A \propto (f'(\hat{z}_t)\odot \epsilon_z) z_{t-1}^\top,
  $$
  即变化仅依赖于突触前后活动的局部变量。

- **与 tBPTT1 的关系**：证明 tPC 的权重更新与仅将梯度回传一步的 tBPTT1 在形式上等价。区别在于 tPC 的推断过程会引入观测对隐状态的直接信息流，线性情况下固定点为
  $$
  z_t = (I + C^\top C)^{-1}(A z_{t-1} + B x_t + C^\top y_t),
  $$
  而纯 RNN 没有这一项。

- **两层分层 tPC (tPC‑H)**：每层接收前一层当前及上一时刻隐状态（引入时滞），形成层次化的自由能：
  $$
  F_t = \frac{1}{2}\|\epsilon_s\|^2 + \frac{1}{2}\|\epsilon_z\|^2 + \frac{1}{2}\|\epsilon_y\|^2,
  $$
  各层拥有独立的预测误差和局部推断，对应权重更新仍为局部赫布规则。三层模型可以类似定义。

- **带资格迹的 tPC (tPC‑E)**：在状态动态中加入泄露项 $\tilde{z}_t = (1-\alpha)z_{t-1} + \alpha(A z_{t-1} + B x_t)$，并引入指数衰减的资格迹 $e_t^A = (1-\alpha)e_{t-1}^A + \alpha z_{t-1}^\top$，权重更新变为 $\Delta A \propto \epsilon_z e_t^A$。这样，误差信号可以与历史上短暂的活动痕迹结合，实现长距离时间信用分配。

## 3. 实验设计

论文采用一系列合成序列预测任务，以评估模型逐步提升的时间学习能力。主要任务和对比方法如下：

- **位置估计任务**：给定速度输入，预测粒子位置。对比模型：标准 RNN（用 tBPTT1 训练）、tPC、以及接收前一时刻真实位置的 RNN（RNN‑P）。目的是验证 tPC 推断过程中隐式引入的观测信息流。

- **交替双态任务**（块长度 2 或 4）：输入由交替的 0 和 1 块组成，预测下一符号。对比：标准储备池计算（固定 $A,B$）、tPC 仅训练输出权重、标准 tPC（也训练 $A,B$）、以及重置隐状态的 tPC（防止时间传播）。用于展示 tPC 利用储备池动态并进一步塑造状态空间轨迹。

- **延迟奇偶校验任务**（3‑bit 和 4‑bit）：需要统计序列中 1 的个数的奇偶性，信息分布在多个时间步上。对比：标准 tPC、不同层数的 tPC‑H、以及不同截断长度 $k$ 的 tBPTT。证明层次化结构能够替代深度时间反向传播来学习复杂跨时间依赖。

- **干扰任务**：先呈现线索，接着插入不同强度的高斯噪声干扰，最后提示模型输出线索。对比：tPC、tPC‑H 和 tBPTT。展示层次化动态对强干扰的鲁棒性。

- **延迟响应任务**（短延迟与长延迟）：呈现初始线索，经过一段可变的延迟后复现线索。对比：标准 tPC、tPC‑E、e‑prop 和 RFLO。评估资格迹在跨越长时间间隔时进行信用分配的能力。

每个实验均在统一框架下进行，参数量在可比较时进行匹配，学习率等超参数通过网格搜索确定。

## 4. 资源与算力

- 论文明确提到所有模型均使用 PyTorch 实现，并采用 Adam 优化器。
- 文中未提供任何关于 GPU 型号、数量或具体训练时长的信息。因此，无法从已有内容评估算力开销。

## 5. 实验数量与充分性

- **实验规模**：共进行了 5 组主要实验任务，每组又包含不同难度变体（如不同块长度、奇偶校验位数、延迟时长、干扰强度等）。总计约有 10 余个具体的实验条件。
- **鲁棒性验证**：每个实验曲线均基于至少 5 个随机种子（部分采用 20 个种子），并报告了均值与标准误差。超参数经过网格搜索，模型间关键参数（如隐含层尺寸）在对比时保持一致。
- **消融与分析**：在交替任务中设置了重置隐状态的控制组；在 tPC‑H 中比较了不同层数；tPC‑E 中与无资格迹变体及多种基线（e‑prop/RFLO）对比；并通过 PCA 可视化了 tPC 的状态空间变化。
- **充分性与公平性**：对于所选取的计算神经科学动机性任务而言，实验设计是充分的，逐步挑战了模型的不同能力，比较基准选择合理，对比条件公平。但所有任务均为维度低、长度短的合成序列，未涉及真实世界高维时间序列或与大规模深度学习模型对比。

## 6. 论文的主要结论与发现

1. **功能等价性**：tPC 的递归权重更新在形式上与 tBPTT1 等价，但由于推断过程，tPC 在活动层面隐式引入了观测到隐状态的信息流，使其在需要外部位置校正的任务中具有优势。
2. **储备池效应与塑形**：tPC 能够像储备池计算一样，利用递归动态编码短程时间上下文，并通过局部可塑性重塑神经轨迹，使下游读出更为容易。
3. **分层结构的助力**：引入分层时间动态后，tPC‑H 能够学习非平凡的跨时间依赖（如 4‑bit 延迟奇偶校验），其效果接近具有更长时间截断的 tBPTT，同时对强干扰表现出更高的鲁棒性。
4. **资格迹扩展长程学习**：在泄露循环状态动态基础上引入资格迹的 tPC‑E，能够解决传统 tPC 无法解决的长延迟响应任务，表明局部学习结合生物学合理的记忆机制可以支持扩展的时间信用分配。
5. **统一视角**：论文将 tPC 与储备池计算、截断 BPTT、e‑prop 和 RFLO 等框架联系起来，给出了它们之间的层次关系图（Fig 7）。

## 7. 优点

- **理论严谨性**：清晰推导了 tPC 与 tBPTT1 的等价性，并给出了分层和资格迹扩展的自由能函數与更新规则，保证了扩展模型仍完全基于局部学习。
- **渐进式任务设计**：实验任务难度递增，明确指向不同的计算需求（短时上下文、长程依赖、抗干扰、长延迟），有助于清晰解析各机制（储备池动态、分层、资格迹）的独特作用。
- **多基线对比**：不仅与 tBPTT 不同截断版本对比，还与储备池计算、e‑prop、RFLO 等生物合理学习方法进行了比较，建立了 tPC 在该领域中的位置。
- **可视化与状态分析**：通过 PCA 展示了 tPC 学习后状态空间的线性可分性提升，直观支撑了解释。

## 8. 不足与局限

- **任务简单**：所有实验均基于低维合成序列，未在大规模真实世界时序数据（如语音、文本、视频）上验证，因此结论的推广性有限。
- **网络规模较小**：实验中隐单元数最多为 64，与当前深度学习应用差距大，未探讨扩展到大规模网络时的性能与训练稳定性。
- **资格迹模型简化**：tPC‑E 中将非线性放置于输出模型而非状态动态中，与标准 tPC 不完全一致，这一点作者已做说明，但可能影响与早期 tPC 公理的严格对应。
- **资格迹时间常数固定**：$\alpha=0.5$ 为单一固定值，未考虑生物学中时间常数的异质性，也未探讨多时间尺度的整合。
- **离散时间处理**：tPC‑H 的时滞通过离散时间步实现，作者承认更严格的处理需连续时间建模。
- **算力信息缺失**：未报告计算资源消耗，难以评估方法在更大任务上的实际可行性。
- **未与全 BPTT 或门控架构对比**：论文未与标准全 BPTT、LSTM 或 GRU 等专门用于解决长期依赖的架构进行直接性能比较，因而无法判断 tPC 系列在处理极长依赖时的相对效率。

（完）
