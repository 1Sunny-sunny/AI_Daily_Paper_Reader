---
title: "Bracket Coding: The Optimal Balance Between Temporal Integration and Segregation in Early Visual Processing"
title_zh: 括号编码：早期视觉处理中时间整合与分离的最佳平衡
authors: "Samiei, T., Ahmed, H. F., Zagha, E., Nozari, E."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729124v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 神经脉冲模式编码与时间动态
tldr: 该研究揭示了一种名为“括号编码”的新型神经编码方式，它动态整合速率与时间编码，以时间协调的窗口分块处理信息，通过大规模Neuropixels记录和小鼠视觉实验，证实其鲁棒性、最优信息解码、层次组织及长程同步，并在独立数据集中验证，为感觉编码理论提供新框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 研究大脑感觉信息编码的基本原理，解决长期存在的速率编码与时间编码之争。
method: 使用Neuropixels高密度电极记录小鼠视觉通路多个脑区，结合Allen Institute和IBL两大数据集进行分析。
result: 发现“括号编码”由时间对齐的编码块构成，块内速率编码、块边界精准同步，并具备最优解码、功能相关、层次结构和振荡相干等特性。
conclusion: 证实了一种新颖的感觉信息编码形式，对神经科学和神经工程具有广泛影响。
---

## 摘要
尽管对神经编码的研究已逾一个世纪，但大脑编码感觉信息的基本原理仍存在争议。在本研究中，我们提供了汇聚性证据，表明在观看系列视觉刺激的小鼠的丘脑、初级视觉皮层和高级视觉皮层区域中，存在一种动态、快速切换的发放率和时间编码整合。该方案的主要特征是存在不同的、时间协调的“括号”，这些括号铺满了每次试验的持续时间，内部采用发放率编码，并由跨群体精确计时和同步的边界分隔。利用来自艾伦研究所视觉编码数据集的大规模Neuropixels记录，我们证明了括号编码在多个视觉任务和脑区中的稳健性和普遍性，以及其在信息解码中的最优性、信息表征的功能相关性、显著的分层组织、跨视觉区域的自下而上长程同步性以及与低频局部场电位的相干性。这些发现随后在由国际脑实验室联盟提供的第二个独立数据集中得到验证。最后，我们提供了一个可作为产生括号编码群体发放活动的潜在机制的计算模型。总之，我们的结果证明了一种新颖的感觉信息编码形式存在于大脑中，对神经科学和神经工程具有广泛的意义。

## Abstract
Despite over a century of research into the neural code, the fundamental principles by which the brain encodes sensory information remain debated. In this study we provide converging evidence for the presence of a dynamic, fast-switching integration of rate and temporal coding in the thalamus, primary visual cortex, and higher-order visual cortical areas of mice viewing an array of visual stimuli. This scheme is primarily characterized by the presence of distinct, temporally coordinated "bracket"s that tile the duration of each trial, are rate-coded within, and are separated by boundaries that are precisely-timed and synchronized across the population. Using large-scale Neuropixels recordings from the Allen Institute Visual Coding dataset, we provide evidence for the robust- ness and generality of bracket coding across several visual tasks and brain regions, as well as its optimality for information decoding, functional relevance for information representation, pronounced hierarchical organization, long-range bottom-up synchrony across visual regions, and coherence with low-frequency local field oscillations. These findings were all subsequently validated in a second, independent dataset provided by the International Brain Laboratory consortium. Finally, we provide a computational model that can serve as a potential mechanism for the generation of bracket-coded population spiking activity. Together, our results demonstrate the presence of a novel form of sensory information encoding in the brain, with broad implications for neuroscience and neuroengineering.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：神经网络如何通过动作电位编码感觉信息，长期以来存在“发放率编码”（信息由发放次数承载）与“时间编码”（信息由精确脉冲时序承载）之争。
- **核心问题**：能否在群体活动中找到一种**动态整合发放率编码与时间编码的混合机制**，既能实现局部稳定表征，又能支持快速的状态切换与精确的时间协调。
- **整体含义**：作者提出并验证了一种名为**“括号编码” (Bracket Coding)** 的全新视觉信息编码方案——将每次刺激试验的神经响应在时间上划分为一系列离散的编码区间（括号），区间内采用发放率编码，区间边界则由跨神经元同步的精确时序标记。该方案为调和两类编码理论提供了统一视角，对理解大脑计算、大规模神经解码及类脑智能具有深远意义。

## 2. 论文提出的方法论

- **核心思想**：通过“扫掠整合‑解码”框架，探测群体脉冲活动中**最优整合窗口**的边界。
  - 若在某个时间窗口内整合发放能提高解码精度，表明窗口内脉冲携带相似信息；反之，当整合跨过某个时间点导致解码精度下降，则标记该点为信息切换的“括号边界”。
- **关键技术细节**：
  - **扫掠整合 (Sweeping Integration)**：对每个固定的“参考时间”$t_r$，向左右两侧逐步扩大整合窗口至“极限时间”$t_l$，将窗口内各神经元发放计数求和，送入解码器，得到随 $t_l$ 变化的解码误差轨迹 $E_{t_r}(t_l)$。
  - **波谷检测**：找出每条轨迹的局部极小值（波谷），它们定义了对应该参考时间的“信息切换点”。
  - **括号边界识别**：汇总所有参考时间下的波谷时间，绘制**波谷栅图**，若波谷时间与参考时间无关而锁定于刺激开始（即垂直排列），则表明存在固定的括号边界。
  - **相位锁定值 (PLV)**：定量衡量波谷分布的时间规律性。对频率 $f$，计算所有波谷时刻 $t_k$ 的相位 $\phi_k(f)=2\pi f t_k$，则 $\mathrm{PLV}(f)=|\frac{1}{N}\sum_{k} e^{i\phi_k(f)}|$。高 PLV 表示波谷在相位上集中（括号边界周期性或规律性）。
  - **密度估计与边界提取**：对波谷时间进行核密度估计 (KDE)，峰值位置作为最终括号边界。
  - **控制与对比**：通过**随机时间打乱**生成零分布，以检验真实波谷结构的显著性；再比较基于真实括号与随机括号积分的解码性能。
- **扩展分析**：
  - **时间相异性分析**：滑动两个相邻窗口，比较窗口内解码准确度分布向量的欧氏距离，检验括号边界是否对应表征突变。
  - **时间复用分析**：滑动小窗口得出各类别解码准确度时间序列，计算均值及其导数与括号边界密度的相关性。
  - **跨区域时滞分析**：对不同脑区的括号边界密度进行互相关，提取最佳时滞$\tau^*$，判断信息是自下而上（丘脑→V1→高级视觉区）还是自上而下传播。
  - **LFP相位锁定**：将括号边界与窄带局部场电位（θ、α‑β）进行相位锁相分析。

## 3. 实验设计

- **数据集**：
  - **主数据集**：Allen Institute Visual Coding – Neuropixels 数据集，10只小鼠，被动观看 Gabor 斑块、自然场景、移动光栅三种视觉任务。
  - **验证数据集**：International Brain Laboratory (IBL) Neuropixels 数据集，114只小鼠，执行主动视觉对比度辨别任务（转动轮子将光栅移至中央）。
- **脑区划分**：高级视觉区 (HVAs)、初级视觉皮层 (V1)、背外侧膝状体 (LGd) 为视觉通路；海马结构 (HPF) 作为对照区；在 IBL 中还分析了初级与次级运动皮层。
- **任务子划分**：每种刺激任务被拆分为多个独立的“子任务”（不相交的刺激子集分类问题），以增强统计效力并确证括号边界跨子任务一致。
- **对比基准与方法**：
  - 与 **随机打乱脉冲时间** 的代理数据比较 PLV、相异性、复用性等指标。
  - 与 **随机括号边界** 下的解码性能对比，验证真实括号的最优性。
  - 与海马区（非视觉区）对比，检验括号编码的视觉通路特异性。
  - 合成数据：用参数化非齐次泊松过程模拟不同条件下的发放率轨迹，验证交叉点和神经元同步开关可产生括号结构。

## 4. 资源与算力

- 论文提及所有分析运行于 **加州大学河滨分校高性能计算中心 (HPCC)** 集群，使用 Python 实现，通过 Slurm 调度，在 CPU 与 GPU 节点上执行。
- 每个作业通常使用 **2 个 CPU 核心**，内存需求在 **4–32 GB** 之间。
- **未明确提及 GPU 型号、数量、训练时长**等具体算力细节，仅说明使用了 GPU 节点。整体计算负担适中，主要受试次量、试验时长和重复次数影响。

## 5. 实验数量与充分性

实验设计层次丰富，覆盖全面，可认为**充分且客观**：

- **多任务**：Gabor 斑块（9个子任务）、自然场景（10个子任务）、移动光栅（10个子任务），外加 IBL 主动辨别任务（2个子任务）。
- **多脑区**：每条通路包含 HVAs、V1、LGd 三站，加 HPF 区作为阴性对照，IBL 分析还包含运动皮层作为额外对照。
- **多种定量指标**：PLV 频谱、最大$\Delta$PLV、显著频率数、解码优度对比、KDE 交叉相关、LFP‑边界锁相值、时间相异性/复用性相关性等。
- **消融与稳健性检验**：
  - 剔除刺激起始 70 ms 后重新计算 PLV，验证括号编码并非仅由刺激起始边界贡献。
  - 子任务级 PLV 分析，揭示全局与局部时间结构。
  - 合成数据实验：改变调制频率、相位，验证括号边界的生成逻辑。
- **统计检验**：多处采用 Wilcoxon signed‑rank 检验、FDR 多重比较校正、置换检验等，控制虚假发现。
- **双数据集互验**：Allen 被动观看与 IBL 主动决策两种范式相互印证，增强结论的泛化性。

总体来看，实验数量充足，设计严谨，多维度验证，且包含必要的阴性对照与消融分析，客观性强。

## 6. 论文的主要结论与发现

- **通用编码模式**：小鼠视觉通路（丘脑→V1→HVAs）中存在稳健的括号编码，信息被分割为数十毫秒级的**速率编码区间**，区间边界由群体精确同步的**时间编码**标记。
- **最优解码**：基于真实括号边界进行不等长积分，解码视觉种类/位置的准确率显著优于随机边界积分，证明括号结构对信息提取具有最优性。
- **表征转折**：括号边界对应解码信息结构的急剧变化（各类别解码准确度分布突变），且边界附近平均解码准确度下降，证实括号间编码的语义差异。
- **分层递增**：括号编码强度沿视觉层级递增（LGd < V1 < HVAs），且与刺激时间频率的调制也呈层级递进；HPF 则无此现象。
- **长程同步**：括号边界时间在视觉通路中主要为自下而上的长程同步（LGd 引领 V1，V1 引领 HVAs），表明括号结构随信息流传播并增强。
- **节律耦合**：括号边界与低频局部场电位（θ、α‑β 振荡）锁相，且锁相强度也呈层级递增，暗示慢波网络动态可能参与括号时序的协调。
- **机制线索**：合成数据证明，只要存在跨刺激条件的发放率轨迹交叉且跨神经元同步，即可自然产生括号边界，无需外部强制边界。
- **IBL 交叉验证**：在独立、主动行为数据集中同样观测到括号编码的多个特征（波谷对齐、边界相关性、解码最优性等），尽管效应稍弱，整体结论可靠。

## 7. 优点

- **理论创新**：首次系统定义并验证“括号编码”这一介于发放率和时间编码之间的新概念，给出了可操作的最优整合窗口检测方法。
- **方法严谨**：扫掠整合‑解码框架完全数据驱动，无需预设窗口大小；利用 PLV 量化时间一致性，并通过打乱控制排除有限样本伪迹。
- **多层面验证**：结合解码优度、表征相似性、层级流向、节律耦合四个维度，相互佐证，增强了结论的可信度。
- **双数据集泛化**：同时覆盖被动感官和主动决策两种实验条件，提升了发现的通用性和说服力。
- **合成数据阐释机制**：用简单生成模型复现括号效应，为生理机制提供了直观且可测的解释路径。
- **控制实验充分**：阴性脑区（海马、运动皮层）、去除早期边界、子任务分析等设计周全，排除了多项可能混淆。

## 8. 不足与局限

- **时域限制**：括号编码主要在刺激起始后前 250 ms 明显，后续时段无显著结构，对感觉编码的适用窗口存在明确边界。
- **任务依赖性**：未能发现运动相关信息的括号编码，表明该模式可能更适用于锁向离散外部事件的初级感觉响应，未必是全局编码策略。
- **数据要求苛刻**：需要大数量并行记录、充足试验数、多刺激类别的群体发放数据，可能在小型或噪声较大的数据集中难以复现。
- **IBL 效应减弱**：因试验数不均、混合构建“超级小鼠”及行为变异性，效应大小弱于被动任务，说明方法对数据质量和并行动态一致性敏感。
- **机制未明**：虽给出合成数据机制解释和 LFP 关联，但尚缺乏直接因果实验（如光遗传扰动）来揭示形成括号编码的具体回路机制。
- **分析方法可能的循环性**：从解码误差轨迹提取边界，再用相同数据评价解码优度，虽通过子任务交叉部分缓解，但仍需在新数据上做前瞻性验证。

（完）
