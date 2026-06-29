---
title: Preserved geometry during representational drift enables stable perception and memory
title_zh: 表征漂移期间保持的几何结构实现稳定的感知与记忆
authors: "Zaid, H., Schaffer, E. S."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.25.734656v1.full.pdf"
tags: ["query:sr"]
score: 10.0
evidence: 在漂移的神经群体表征中实现稳定解码的数学框架
tldr: 表征漂移现象中神经编码的不稳定性对感知和记忆构成挑战。本文提出一个数学框架，证明在大规模前馈和循环网络中，输入的几何结构得以保持，从而使漂移表征可通过自适应解码实现稳定读取。该理论表明，只要神经元群体足够大，几何结构的保持是漂移表征的普遍特征，解释了大脑如何利用漂移编码维持稳定功能。
source: biorxiv
selection_source: fresh_fetch
motivation: 解释大脑如何在表征漂移的情况下实现稳定的感知和记忆检索。
method: 构建数学框架分析前馈和循环网络中几何结构保持与解码条件。
result: 证明足够大的网络能够保持输入几何结构，且具有稳定几何的漂移表征可通过自适应解码器稳定解码。
conclusion: 只要神经元群体足够大，表征漂移就会保持几何结构，从而允许稳定解码，这为实证研究提供了理论指导。
---

## 摘要
在许多脑区，神经元对刺激的调谐在数小时的时间尺度上保持稳定，但在数周的时间尺度上却不稳定，这种现象通常被称为“表征漂移”。这似乎意味着这些脑区无法用于稳定识别感觉刺激或检索数周前学习的关联记忆。然而，解码方法已表明，在某些情况下，可以对漂移的表征进行稳定解码。原则上，自适应解码为大脑如何在漂移表征下运作的悖论提供了一种合理的解决方案，但我们仍缺乏对实现稳定解码所需条件的深刻理解。在此，我们提供了一个通用的数学框架，解释了何时以及为何能够从漂移的表征中实现稳定解码。首先，我们证明，当前馈和循环网络足够大时，它们会保持输入的几何结构，这意味着在这些网络中表征漂移也必须保持几何结构。其次，我们证明，具有稳定几何结构的漂移表征可以通过自适应解码器进行解码。因此，不仅在存在表征漂移时保持几何结构，而且从漂移表征中解码的能力，仅需要表现出表征漂移的神经元群体足够大。这一理论框架不仅表明保持几何结构应是漂移表征的一个普遍特征，还解释了在何种条件下测量稳定几何结构的实证工作将会成功。

## Abstract
In many brain regions, the stimulus tuning of neurons is stable on a timescale of hours but not on a timescale of weeks, a phenomenon often called 'representational drift'. This would seem to imply that these brain regions cannot be used for stable recognition of sensory stimuli or the retrieval of associative memories learned several weeks prior. However, decoding approaches have demonstrated that in some cases, stable decoding of drifting representations is possible. In principle, adaptive decoding provides a plausible resolution to the paradox of how the brain operates with drifting representations, but we lack a deep understanding of what the requirements are for stable decoding to be possible. Here, we offer a general mathematical framework that explains when and why stable decoding from a drifting representation can be achieved. First, we demonstrate that both feedforward and recurrent networks preserve the geometry of their inputs when the network is sufficiently large, meaning that representational drift must also preserve geometry in these networks. Second, we demonstrate that drifting representations that have stable geometry are decodable with adaptive decoders. Therefore, not only the existence of preserved geometry in the presence of representational drift but also the ability to decode from drifting representations simply requires the population of neurons exhibiting representational drift to be large. This theoretical framework not only suggests that preserved geometry should be a general feature of drifting representations, it also explains the conditions under which empirical efforts to measure stable geometry will be successful.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **问题背景**：许多脑区存在“表征漂移”现象，即神经元对刺激的调谐在数小时稳定，但在数周尺度上逐渐变化。这种现象对稳定感知、长期记忆检索构成挑战，因为若表征不断变化，下游脑区如何能可靠地读出信息？
- **核心矛盾**：若漂移脑区无法维持稳定信息，则需假设其他脑区负责长期功能；但这与漂移广泛存在于海马、皮层等区域的观测矛盾。
- **整体含义**：该文提出一种一般性数学框架，指出**只要下游神经元群体足够大，表征的几何结构（刺激间关系）即使在大规模突触变化时仍会被保持**；进而证明，稳定的几何结构使得基于少量样本的自适应解码器便能维持对任意刺激的稳定读出，无需表征本身稳定。这为“漂移大脑如何支撑稳定行为”提供了原则性解释。

### 2. 方法论
- **核心思想**：将“表征漂移”建模为前馈或循环网络中突触的随机缓慢更新，分析在此过程中上游输入几何结构（刺激间角度）向下游输出的传递失真，并证明该失真仅由网络尺寸比 $N_x/N_y$ 决定。随后利用稳定几何设计自适应解码规则，证明其可维持对未见过刺激的选择性。
- **关键技术细节与公式**：
  - **前馈网络模型**：$y_s = J_t x_s$，其中 $x_s \sim \mathcal{N}(0, N_x^{-1})$，$J_{ij,t}$ 按概率 $p$ 重新从 $\mathcal{N}(0, N_y^{-1})$ 采样以模拟突触更新。
  - **几何失真界限**（输入几何失真 $\epsilon_{in} = y_{s1}^\top y_{s2} - x_{s1}^\top x_{s2}$）：
    - 对于典型随机输入，以高概率有 $|\epsilon_{in}| \le d / \sqrt{N_y}$（$d$ 为标准差倍数）。
    - 对所有可能输入的最坏情况上界：$|\epsilon_{in}| \le 2\sqrt{N_x/N_y}$。
  - **时间漂移的几何失真**：当 $J_0$ 与 $J_t$ 充分去相关时，$\epsilon_t \approx \sqrt{2}\,\epsilon_{in}$，界限为 $|\epsilon_t| \le d\sqrt{2/N_y}$。
  - **循环网络**：采用标准 RNN $\tau \dot{y}_i = -y_i + g \sum_k K_{ik} \tanh(y_k) + I_i$，证明在外界输入抑制混沌时，稳态响应近似线性，因此前馈结论可推广。
  - **自适应解码器**：一个线性读出 $z_s = w^\top y_s$，初始权重通过 Hebb 规则设为 $w_0 \propto y_*$。利用差分目标传播（DTP）更新：
    $$w_t^\top \leftarrow w_{t-1}^\top + (z_{S,ref} - z_{St}) Y_{St}^+$$
    其中 $Y_{St}^+$ 是 $Y_{St}$ 的伪逆，$z_{S,ref}$ 可以是过去输出（需记忆），或通过“直接/间接电路”由稳定输入 $x$ 提供参考（$z_{S,ref} = x_* X_S$）。
  - **评估指标**：读出对目标刺激的信噪比 $\mathrm{SNR}(t) = \mathbb{E}[(z_*t - z_st)^2] / \mathrm{Var}(z_st)$。

### 3. 实验设计
- **数据集与场景**：纯理论仿真，无外部数据集。输入 $x_s$ 从多元高斯分布抽取，模拟随机刺激集合。网络连接随机生成并随时间更新。
- **基准与对比方法**：
  - 无自适应更新的固定权重读出。
  - 独立噪声漂移（对每个神经元响应直接加累积噪声，而非通过 $J_t$ 变化），以区分“几何保持”与“独立漂移”的效果。
  - 不同尺寸参数 $N_x$、$N_y$ 下的网络。
  - 不同刺激样本数 $N_s$（如 5, 40）。
  - 有无直接/间接电路提供参考信号。
  - 限制采样刺激与目标的相关性（$\le 0.05$ 或严格正交）。

### 4. 资源与算力
- 文中**未提及任何 GPU 型号、数量或训练时长**。模型为仿真与解析推导，计算量极小，可在普通个人计算机上完成。

### 5. 实验数量与充分性
- **实验组数丰富**：覆盖了前馈网络和循环网络的验证；对 $N_x$、$N_y$、$g$、$N_s$、更新规则、“直接/间接”架构、噪声类型进行了系统扫描与消融。每组均与理论界限对比。
- **实验充分性**：通过大量重复仿真（隐式或显式）验证了概率界限和渐近性质（如图1f-h, 图2d-e, 图3c-d, 图4c-l, 图5b-d），并在补充图中补充了更多参数组合。对比公平，变量控制清晰。实验设计足以支撑结论。

### 6. 主要结论与发现
- **几何保持的充分条件**：只要漂移脑区的神经元数量 $N_y$ 远大于输入维度 $N_x$，表征几何结构（刺激间相似关系）就会被保留，与突触更新无关。
- **循环网络同样适用**：在外界输入驱动下，即使强递归也能保持近似线性关系，不会破坏输入几何。
- **稳定解码的可行性**：几何保持使得用**少量任意刺激**更新读出权重即可维持对原始目标的特异性，哪怕那些刺激与目标本身几乎无关（仅需非零投影）。
- **直接/间接电路方案**：通过让读出同时接收稳定输入层和漂移层的投射，并以稳定输入产生的响应作为校正目标，可完全避免对过去状态的记忆需求，且性能相当。
- **理论与实验的对接**：该框架解释了为何在梨状皮层等高维输入端脑区难以观测到几何保持（因输入维度高而记录神经元少），并给出发现保持几何的实验条件。

### 7. 优点
- **理论严谨性与一般性**：给出了严格的数学界限，明确将“几何保持”与“网络尺寸比”挂钩，为实验设计提供了定量指导。
- **模型简洁但延展性强**：从前馈线性模型出发，逐步推广到非线性循环网络，证明核心结论不依赖于特定动力学。
- **生物可行性**：提出的自适应解码规则（基于伪逆的DTP）和直接/间接电路都有具体生物学对应，并指出其与已知脑回路（如梨状皮层、海马）的一致性。
- **解决开放悖论**：为“表征漂移下如何维持稳定行为”提供了一个无需稳定表征的完整理论框架，统一了多个先前独立的观察。

### 8. 不足与局限
- **未使用真实神经数据验证**：所有实验均为合成数据，没有在已发表的记录数据上测试模型预测的信噪比改善或几何保持现象。
- **线性与静态假设**：模型读出为线性，且网络在稳定点附近工作，未充分考虑复杂时间动力学、脉冲发放、多种塑性规则等。
- **漂移机制单一**：仅考虑随机突触更新引起的漂移，未涵盖兴奋性变化、持续性学习、结构可塑性等其他潜在因素。
- **解码器生物学可行性**：伪逆计算 $Y_{St}^+$ 需全局信息，文中虽提出差分目标传播作为近似，但仍需完整的反馈连接和精确匹配，生物实现细节有待补充。
- **高维输入的局限**：当输入维度极高（如嗅觉受体）时，需要极大的下游神经元群体才能维持理想几何，这在实际脑区中可能不现实；不过论文指出在子空间或受相关刺激约束时影响会减弱。
- **几何保持无法绝对保证**：严格正交的刺激投影可能使读出无法泛化，尽管概率极低。

（完）
