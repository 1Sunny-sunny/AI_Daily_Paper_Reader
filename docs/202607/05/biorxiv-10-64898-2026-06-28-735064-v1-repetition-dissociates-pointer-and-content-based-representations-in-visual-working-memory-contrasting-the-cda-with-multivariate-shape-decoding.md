---
title: "Repetition Dissociates Pointer and Content-based Representations in Visual Working Memory: Contrasting the CDA with Multivariate Shape Decoding"
title_zh: 重复分离了视觉工作记忆中基于指针和基于内容的表征：对比CDA与多元形状解码
authors: "Duncan, D. H., Kandemir, G., Olivers, C. N. L."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.28.735064v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 工作记忆期间从EEG多变量解码形状内容
tldr: 通过EEG研究重复如何影响视觉工作记忆，发现随着刺激重复六次，反映主动对象存储的对侧延迟活动（CDA）逐渐减弱，而解码形状内容的多变量模式保持稳定。这表明重复消除了主动的、个体化的指针式表征，但保留了被动的、源无关的内容表征，揭示了工作记忆向长时记忆转换的神经机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究重复学习过程中，工作记忆中的指针式表征和内容表征如何分离与转换。
method: 30名被试记忆侧化的连续形状，每个项目重复六次，记录EEG并对比CDA与多变量形状解码。
result: CDA随重复显著降低，而形状解码在保持期和扰动后均保持稳定。
conclusion: 重复学习通过消除主动个体化的对象表征、保留被动内容表征，实现记忆从工作记忆到长时记忆的过渡。
---

## 摘要
记忆一个新的电话号码或地址起初很困难，但随着重复变得容易，因为信息从工作记忆转移到长期记忆。这里，我们通过比较主动对象存储的单变量神经标记与记忆内容的多元解码，研究了重复如何影响不同方面记忆信息的存储和转换。三十名参与者将来自连续形状空间的单侧化刺激编码到记忆中。记忆项目连续重复六次以诱导学习。与早期工作一致，脑电图记录显示，重复导致对侧延迟活动（CDA）减少，CDA是一种主动存储的测量指标，被认为反映了对个体对象或其原始来源的指针式表征。相反，在保持阶段以及脉冲扰动后，形状解码在不同重复次数间保持恒定。这些结果表明，通过重复的学习反映了主动且个别化的对象记忆表征的消除，同时被动、来源无关的记忆表征得以保留。

## Abstract
Memorizing a new phone number or address is hard at first, but becomes easier with repetition, as information shifts from working memory to long-term memory. Here we investigated how repetition affects the storage and transition of different aspects of mnemonic information by comparing univariate neural markers of active object storage with multivariate decoding of memory content. Thirty participants encoded lateralized stimuli from a continuous shape space into memory. Memory items were repeated six times in a row to induce learning. In line with earlier work, EEG recordings revealed that repetition led to a reduction in contralateral delay activity (CDA), a measure of active storage that has been taken to reflect a pointer-like representation of the individual object or its original source. In contrast, shape decoding during the retention and also after an impulse perturbation remained constant across repetitions. These results suggest that learning over repetitions reflects the abolishment of active and individuated object memory representations while passive, source-independent memory representations are retained.

---

## 论文详细总结（自动生成）

## 论文核心问题与整体含义

- **研究动机**：工作记忆中的信息通过重复学习会向长时记忆转移，伴随事件相关电位 CDA（对侧延迟活动）幅值下降，但尚不清楚 CDA 的下降究竟反映的是内容表征的消退，还是情境性指针表征的减弱。
- **核心问题**：重复学习到底使视觉工作记忆中的**指针式表征**（与空间源、对象个体化相关的 CDA）与**内容表征**（可通过多变量解码读取的具体形状信息）如何变化，二者是否发生分离？
- **整体含义**：该研究试图从神经信号层面区分“记住什么”（内容）和“记住哪个/来自哪里”（指针），并揭示重复学习过程中记忆表征从工作记忆向长时记忆过渡的动态机制。

## 方法论

### 核心思想
- 利用重复学习范式（同一形状线索连续重复 6 次），同时记录 EEG，以**单变量**的 CDA 作为指针式表征指标，以**多变量形状解码**（MVPA）作为内容表征指标。
- 为进一步考察活动静默（activity-silent）记忆痕迹，实验在保持晚期插入**任务无关的视觉脉冲（ping）**，观察脉冲后内容表征能否被重新激活以及其是否受重复影响。

### 关键技术细节
- **CDA 计算**：取目标刺激对侧电极（PO7/PO8）的电位减去同侧电极的电位，获取 500–1500 ms 时间窗的平均差异波。
- **多变量形状解码**：
  - 采用 17 个后部电极的 EEG 信号。
  - 使用 8 折交叉验证，每个折内对 6 种形状绘制平均事件相关模式。
  - 利用收缩估计（Ledoit-Wolf）计算训练集的协方差矩阵。
  - 以马氏距离衡量测试试次与各类形状模板的相似性。
  - 对距离进行中心化、符号反转后，通过余弦卷积得到逐时间点的解码准确率。
- **脉冲扰动解码**：对脉冲前后采用 100 ms 滑动窗进行基线归一化，降采样至 100 Hz 后拼接各通道特征，再进行多变量解码，以消除 CDA 衰减对基线的影响。
- **眼动控制**：将眼动仪记录的眼位坐标按相同解码流程分析，检验 EEG 解码是否受眼动混淆。

### 统计评估
- 行为与 CDA 数据采用重复测量方差分析，辅以 Bonferroni 校正的事后比较。
- 解码显著性的检验使用基于符号置换的集群校正检验（cluster-based permutation test）。

## 实验设计

- **数据集/场景**：30 名年轻成人，每名被试完成 4 个 session，共 1728 个试次。每个试次中，侧化呈现记忆目标（从连续圆形形状空间中选取的 6 种形状之一）和干扰刺激。
- **实验设计**：同一种形状在连续 6 个试次中重复出现（重复1–6），之后更换为新形状。刺激位置在左、右侧随机变化，无空间记忆要求；被试仅需判断探测形状与记忆目标是否相同。
- **对比条件**：
  - 不同重复次数（1–6，以及合并后的 1&2、3&4、5&6）。
  - 单变量 CDA 与多变量形状解码结果的对比。
  - 脉冲扰动后有/无解码、不同重复次数间的解码稳定性对比。
  - EEG 解码与仅基于眼位坐标的解码对比。
- **基准与参照**：以 CDA 随重复下降的经典效应作为内部参照，检验内容解码是否亦下降、不变或上升。

## 资源与算力

- 论文未提及 GPU 型号、数量及训练时长。所有分析均为传统 EEG 信号处理与多变量解码，无需大规模深度学习算力。数据采集使用 Biosemi Active 2 系统，处理在 MATLAB 内完成。

## 实验数量与充分性

- 共完成 **4 组主要分析**：行为表现、CDA、早期保持阶段的形状解码、脉冲后的形状解码，并辅以眼动控制分析。
- 主要对比在 **3 个合并重复条件**（1&2、3&4、5&6）下进行，既保证了试次数量充足以支持解码，又减少了多重比较的维度。
- 每种解码均通过重复 100 次随机采样来均衡形状和位置，避免选择偏差，统计方法较为严谨。
- 总体实验数量适中，设计覆盖了从单变量到多变量、从早期保持到晚期的多个层面，且预注册了三种可能的解码变化方向，客观性较好。但解码对试次数量敏感，群体试次可能仍不够丰富以探测较小的重复效应。

## 主要结论与发现

- **CDA 随重复显著下降**：特别是在合并条件中，重复 1&2 的 CDA 显著大于 3&4 及 5&6，后两者间无差异，印证了指针式表征减弱的观点。
- **形状解码保持稳定**：
  - 早期保持窗口（500–1500 ms）内，形状解码在不同重复条件下均显著高于随机，且条件间无显著差异，也未出现下降趋势。
  - 脉冲扰动后，所有重复条件下的形状解码均再次显著出现，同样保持稳定，数值上甚至有微弱增强。
- **眼动解码在脉冲后期出现**，但时间晚于 EEG 解码且主要在探测呈现前，可能反映战略性的眼动准备，而非混淆早期内容解码。
- **核心结论**：重复学习选择性地消退了主动的、个体化的对象指针表征（CDA），而保留了被动、源无关的内容表征。这为 CDA 仅反映对象指针而非内容活动的假设提供了有力证据，并表明在有限的学习次数内，内容表征并未必然移出工作记忆或转移到静默存储。

## 优点

- **新颖的分离范式**：在同一范式内直接对比 CDA 与内容解码，为 CDA 的指针属性提供了新的支持。
- **引入连续形状空间**：首次将 Li 等人（2020）的形状空间用于 EEG 解码，扩展了可解码的视觉特征维度。
- **脉冲扰动技术**：探究了活动静默记忆表征如何受重复影响，延伸了仅观察持续活动的设计。
- **严谨的控制**：通过随机子抽样平衡试次、协方差估计和基于符号置换的统计检验，并特别控制了可能混淆的眼动信号。
- **预注册**：三种可能的解码变化方向被预先设定，增加了结论的客观性和可信度。

## 不足与局限

- **样本量较小**（N=30），对于多变量解码，试次数仍可能限制检测小效应变化的能力，尤其是各组差异不显著时，不能完全排除II型错误的可能性。
- **重复次数有限**：仅重复 6 次，可能尚未达到学习曲线的平稳阶段，长于 6 次的重复是否会引发内容表征的变化未知。
- **记忆负载单一**：未操纵记忆项目数量，因此无法观察 CDA 的负载敏感性与内容解码在重复学习中的交互。
- **解码的因果解释有限**：解码稳定仅表明神经模式中可读取形状信息，并未直接证明该信息被主动用于行为选择；且脉冲后眼动解码出现，暗示部分晚期解码可能受眼动策略影响。
- **外部效度**：实验材料为简单几何形状，结果能否推广至复杂视觉刺激或更生态的记忆情境还需验证。

（完）
