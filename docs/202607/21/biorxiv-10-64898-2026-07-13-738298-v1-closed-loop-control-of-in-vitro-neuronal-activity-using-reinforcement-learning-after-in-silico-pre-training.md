---
title: Closed-loop control of in vitro neuronal activity using reinforcement learning after in silico pre-training
title_zh: 基于计算机预训练的强化学习实现体外神经元活动的闭环控制
authors: "Carvalho, E., Mateus, J. C., Pinto, R., Aroso, M., Aguiar, P."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.13.738298v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 通过硅上预训练强化学习闭环控制神经元爆发活动
tldr: 为应对强化学习神经调节中长时探索与活体组织生理极限的矛盾，本研究通过生物物理校准的数字孪生预训练控制策略，再将其转移到体外培养的神经元网络，实现了对网络爆发的有效闭环控制。该策略优于传统启发式方法，刺激用量更少，并通过钙成像揭示其利用局部拓扑和生理动态的机制，展示了数字孪生策略向活体网络直接转移的可行路径。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738298-v1/fig-001.webp\", \"caption\": \"\", \"page\": 5, \"index\": 1, \"width\": 1610, \"height\": 840}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738298-v1/fig-002.webp\", \"caption\": \"\", \"page\": 8, \"index\": 2, \"width\": 1610, \"height\": 1390}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738298-v1/fig-003.webp\", \"caption\": \"\", \"page\": 10, \"index\": 3, \"width\": 1610, \"height\": 912}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738298-v1/fig-004.webp\", \"caption\": \"\", \"page\": 13, \"index\": 4, \"width\": 1596, \"height\": 1573}]"
motivation: 强化学习闭环控制神经活动面临探索时间长与活体组织生理极限的冲突。
method: 在生物物理校准的数字孪生中预训练强化学习策略，再转移到体外培养的神经元网络。
result: 转移策略控制网络爆发效果优于启发式方法，刺激用量受限，并揭示了时空优化机制。
conclusion: 体外脑芯片培养可作为强化学习神经调节的有效试验平台，数字孪生策略可直接转移至活体网络。
---

## 摘要
通过电刺激控制特定神经元动态对治疗性神经调控至关重要，然而由于生物神经元网络的复杂性和非平稳性，推导最优控制策略仍具挑战。尽管强化学习（RL）提供了强大的闭环控制框架，但其对长时间刺激驱动探索的依赖与活体组织的生理极限难以调和。在此，我们展示了一种从计算机模拟到体外实验的迁移策略，实现了对培养神经元网络爆发的有效状态依赖控制。迁移后的策略优于启发式控制，同时保持了有限的刺激使用。同步钙成像揭示了所学策略的机制基础：智能体在空间和时间上优化刺激，利用局部网络拓扑和内在的生理时间动态。这些结果确立了体外脑芯片培养作为基于RL的神经调控的可行跳板，并证明可在生物物理校准的数字孪生中推导有效控制策略，并将其直接迁移到活体网络。

## Abstract
Controlling specific neuronal dynamics with electrical stimulation is critical for therapeutic neuromodulation, yet deriving optimal control policies remains challenging due to the complex and non-stationary nature of biological neuronal networks. While reinforcement learning (RL) offers a powerful closed-loop control framework, its reliance on prolonged stimulus-driven exploration is difficult to reconcile with the physiological limits of living tissue. Here, we demonstrate an in silico-to-in vitro transfer strategy that achieves efficient state-dependent control of network bursting in cultured neurons. The transferred policy outperforms heuristic controls, while maintaining constrained stimulation usage. Concurrent calcium imaging reveals the mechanistic basis of the learned policy: the agent optimizes stimulation spatially and temporally, exploiting local network topology and intrinsic physiological temporal dynamics. These results establish in vitro brain-on-chip cultures as a tractable stepping stone for RL-based neuromodulation and demonstrate that effective control policies can be derived in biophysically calibrated digital twins and transferred directly to living networks.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：通过电刺激对生物神经元网络（BNNs）实现精准的闭环控制极具挑战。强化学习（RL）虽然提供了一种强大的自适应框架，但其训练过程需要大量的探索性刺激，这与活体组织的生理耐受极限（如细胞损伤、网络疲劳、非平稳性漂移）存在根本冲突。
- **整体含义**：本研究旨在解决“RL的样本低效”与“生物网络的生理约束”之间的矛盾。其核心思路是：先在生物物理校准的**数字孪生**（in silico model）中预训练RL控制策略，再将学习到的“通用策略”（Generalist）直接迁移到**体外培养的神经元网络**上执行闭环控制，从而规避在线学习对活体网络造成的累积性损伤。
- **动机**：现有多数闭环神经调控要么采用开环或启发式规则，要么在线RL训练因刺激时间过长导致网络性能衰退，使得学到的策略沦为“移动靶”。本研究提出“硅上预训练→体外迁移”的范式，旨在为后续更复杂的治疗性神经调控（如自适应深部脑刺激）提供概念验证。

### 2. 论文提出的方法论
#### 核心思想
- 建立能重现体外培养网络关键爆发动态的**生物物理详细模型**（200个Hodgkin-Huxley神经元，含突触短时程可塑性）。
- 在该数字孪生上，将神经元爆发控制问题建模为**非线性上下文赌博机（contextual bandit）**任务：智能体根据当前网络状态选择在哪个电极（或无刺激）施加单个电脉冲，目标是最大化立即诱发网络爆发的概率，同时惩罚过多刺激。
- 通过在线RL训练多个环境特异的“专家”（Specialist）策略，再用**策略蒸馏**（policy distillation）得到一个“通用”（Generalist）策略，该策略能捕获跨网络的共性兴奋性动态。
- 将该通用策略直接部署于体外微电极阵列（MEA）培养网络，实现零在线训练的闭环控制。

#### 关键技术细节
- **状态表示**（State representation）：
  $$s_t = [\tau, w_1, w_2, \dots, w_E]$$
  其中 $\tau$ 为归一化的自上一网络爆发（NB）以来的时间（相对于最近5次网络爆发间隔的中位数），$w_e$ 为基于最近5次NB中各电极尖峰时间和顺序计算的归一化权重，用以捕获兴奋性的时空恢复状态。
- **动作空间**：对单一电极施加单相阴极脉冲（-400 mV，200 μs）或“不刺激”，共 $E+1$ 个离散动作。
- **奖励函数**：
  $$R(s_t, a_t, s_{t+1}) =
  \begin{cases}
  +1, & \text{若诱发NB（刺激后≤100 ms）} \\
  -0.25, & \text{若刺激但未诱发NB} \\
  +0.25, & \text{若不刺激且无自发NB} \\
  -1, & \text{若不刺激却发生自发NB}
  \end{cases}$$
- **算法**：采用修改的PPO（近端策略优化），将critic改为估计 $Q(s,a)$ 而非 $V(s)$，以适应上下文赌博机中动作特异性信用分配。折扣因子 $\gamma=0$（即纯贪婪/近视策略）。训练时使用32单元单隐层MLP的策略网络。
- **策略蒸馏**：汇聚多个专家策略产生的状态-动作对，训练一个通用策略网络，目标是最小化其输出分布与各专家分布之间的KL散度。
- **体外闭环控制**：实时采集MEA信号，<20 ms延迟完成刺激决策与输出，每步200 ms，精确同步。

### 3. 实验设计
- **数据集/场景**：
  - **In silico**：200个Hodgkin-Huxley神经元的稀疏网络，多个随机实例，用于训练专家和通用策略。
  - **In vitro**：胚胎大鼠海马神经元接种于6孔MEA芯片（9个TiN电极），培养至DIV 17-42，共计132个独立培养孔，15批独立生物学制备。仅包含表现出自发爆发的网络。
- **Baseline与对比方法**：
  - **专家策略（Specialist）**：在特定in silico网络上从头训练的策略，用于衡量通用策略的性能上限。
  - **启发式控制（Protocol 2）**：
    - *Without Best*：剥夺通用策略发现的最佳电极，测试空间选择性贡献。
    - *Random*：保持通用策略的平均刺激频率，但随机化刺激电极和时间，剥离学习的时空模式。
  - **在线学习对比（Protocol 1）**：允许在体外网络上进行10分钟的PPO在线训练（Specialist in vitro），与直接部署的预训练通用策略比较。
- **评估指标**：主要指标为网络爆发间隔（NIBI）的降低（控制效能），以及刺激使用率（控制效率，即刺激步数占比）。同时关注干预后自发活动的恢复（网络疲劳度）。

### 4. 资源与算力
- 论文中**未明确提及**训练该RL模型所使用的GPU类型、数量或具体训练时长。提及的计算环境包括：in silico模型基于NEURON模拟环境（Python），体外实时控制软件运行于配备Intel i7-6700和32GB RAM的工作站，推理延迟在20 ms以内。强化学习的训练可能在该工作站或类似普通计算资源上完成，但无具体算力数据。

### 5. 实验数量与充分性
- **In silico验证**：
  - 生成了50组in silico网络（用于统计分析）和200组留出网络（用于泛化检验）。
  - 训练了999个专家策略用于策略蒸馏，展示了充分的学习轨迹。
  - 进行了网络切换压力测试（Network A $\to$ Network B）。
- **In vitro验证**：
  - **Protocol 1**（在线学习vs通用策略）：N=23个体外网络，交叉平衡顺序。
  - **Protocol 2**（通用策略vs启发式控制）：N=55个体外网络（含部分整合钙成像实验N=5）。
- **实验设计公平性**：交叉平衡顺序控制时序效应，并验证了Protocol 2的疲劳效应远小于Protocol 1。对比中采用配对检验，关联分析使用Kendall秩相关，统计方法严谨。实验覆盖面较广，既有in silico大规模训练与检验，又在体外多批次、多发育时间点测试，但钙成像的机械论分析样本量较小（N=5），可能不足以捕获全部变异性。

### 6. 论文的主要结论与发现
- 通用策略在体外网络上能显著缩短网络爆发间隔，且性能与同等条件下在线学习的专家策略无显著差异，但**刺激使用率显著更低**（更精简）。
- 在线RL训练（约11分钟累计刺激）会诱导明显的**“网络疲劳”**：自发爆发率降低，甚至约22%的网络完全沉默。而短时部署的通用策略（约3分钟刺激）导致的疲劳显著较弱。
- 通用策略在缩短NIBI方面**显著优于两种启发式控制**（Without Best 和 Random），证明其学到了**空间特异性的刺激优化**，而非仅仅提供非特异性兴奋。
- 网络的自发NIBI是所有策略下控制性能的主要决定因素，存在一个由内在不应期等决定的性能上限，但通用策略能尽可能逼近该上限。
- **钙成像机制解释**：刺激电极的效能与其40 μm半径内检测到的活跃神经元胞体数量高度正相关。高效能电极能更快、更可靠地招募全网络活动，验证了刺激利用局部拓扑结构的假说。

### 7. 优点
- **范式创新**：明确提出了“硅上预训练-体外迁移”的闭环框架，有效规避了RL在活体组织中长期探索的固有问题，为后续应用（如自适应DBS）提供了可行路线图。
- **严格对照**：实验设计系统性地对比了预训练 vs 在线学习、通用策略 vs 剥夺空间/时间信息的启发式控制，量化了各成分的贡献。
- **机制验证**：通过并发钙成像，将策略的性能优势直接与可观测的细胞拓扑特征（电极附近体密度、激活潜伏期）联系起来，增强了结果的生物学可解释性。
- **工程实现**：构建了完整的in silico-in vitro闭环系统，延迟低于20 ms，实现了实时状态依赖控制。
- **算法与问题的匹配**：将问题定义为上下文赌博机，采用修改后的PPO ($\gamma=0$) 并特征工程出具有生物学含义的状态表示，使得学习更为高效且可扩展。

### 8. 不足与局限
- **模型假设简化**：in silico模型仅包含胞体区室，采用点源电场近似和Stoney关系来估计激活，可能低估了轴突激活等更复杂的刺激机制。虽然与本研究采用的30 μm电极相匹配，但可能限制复杂刺激模式下的预测准确性。
- **任务较为简单**：当前控制目标为最大化爆发频率（贪婪式诱发），未来需要拓展到抑制病理性同步、多目标优化等更复杂的闭环任务，这可能需要对状态表示和算法进行扩展（例如引入长期信用分配）。
- **网络漂移处理有限**：虽然预训练策略可通过状态表示适应一定的网络变化，但若网络经历剧烈的突触重塑或丧失，固定架构的通用策略可能逐渐失效。论文未探讨在线微调或持续学习机制。
- **钙成像样本小**：机理验证的钙成像仅限于5个网络，观察到一些例外情况（如无邻近胞体但仍有效的电极），其背后的具体机制尚不完全清楚，结论的普适性需更多数据支持。
- **状态表示依赖人工特征**：当前由研究者定义的特征（归一化时间、尖峰权重）虽然有效，但可能错过数据中其他高维特征，端到端的学习方法或许值得探索，尽管成本更高。
- **刺激参数固定**：仅使用单一脉冲幅度和时长，未探索波形优化或模式化刺激对控制效能和疲劳的影响。

（完）
