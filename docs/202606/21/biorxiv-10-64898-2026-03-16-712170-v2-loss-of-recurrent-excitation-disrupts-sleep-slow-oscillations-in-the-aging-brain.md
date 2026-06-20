---
title: Loss of Recurrent Excitation Disrupts Sleep Slow Oscillations in the Aging Brain
title_zh: 老年大脑中回返性兴奋的丧失扰乱睡眠慢振荡
authors: "Navas Zuloaga, M. G., Purcell, S. M., Bazhenov, M."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.16.712170v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: "多尺度丘脑皮层模型,研究慢振荡的尖峰神经元"
tldr: 老年大脑中睡眠慢振荡（SO）异常与记忆巩固受损相关，但其回路机制不明。本研究构建了基于人脑连接的多尺度全脑丘脑皮层网络模型，模拟突触丧失发现，选择性降解循环兴奋性连接（而非兴奋-抑制连接）可重现衰老相关的SO变化：SO时程延长由Down状态延长驱动，Up状态时长和放电密度下降，提示衰老可能通过破坏循环兴奋性损害了睡眠慢波阶段的关键时间结构，从而影响记忆巩固。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示衰老如何通过影响神经回路导致睡眠慢振荡异常，进而损害记忆巩固的机制。
method: 使用基于扩散MRI纤维束成像构建的全脑丘脑皮层网络模型，模拟进行性突触丧失。
result: 仅循环兴奋性连接丧失即可重现衰老相关的SO变化，表现为SO时程延长、Down状态延长、Up状态缩短和放电减少。
conclusion: 衰老通过选择性破坏循环兴奋性连接，干扰了睡眠慢振荡的时间结构，这可能是认知衰退的回路机制。
---

## 摘要
摘要 依赖睡眠的记忆巩固依赖于慢振荡（SOs），它在慢波睡眠（SWS）期间协调丘脑-皮层-海马动态。衰老会扰乱SO特性，降低SO振幅、密度和斜率，然而连接大脑结构变化与这些扰乱的环路水平机制仍知之甚少。在此，我们提出了一个多尺度、全脑丘脑-皮层网络模型，该模型结合了基于扩散MRI纤维束成像的生物真实人脑连接，每个半球包含超过10,000个皮层柱，具有发放的锥体神经元和抑制性神经元，以及一个解剖上分化的丘脑网络。模拟进行性突触丧失，我们发现选择性降解回返性兴奋连接，而非兴奋-抑制投射，能够重现经验观察到的与年龄相关的SO变化。SO持续时间增加主要由延长的Down状态驱动，而Up状态持续时间和发放密度降低，提示了记忆巩固受损的可能机制。这些结果表明，衰老选择性扰乱了对于无干扰记忆巩固至关重要的SWS的时间结构，为老年大脑中的认知衰退提供了机制性洞见。

资助来源：NIH（给MB的资助 1R01MH125557, 1RF1NS132913, 1R01AG099626）

## Abstract
AbstractSleep-dependent memory consolidation relies on slow oscillations (SOs) that coordinate thalamocortical-hippocampal dynamics during slow-wave sleep (SWS). Aging disrupts SO properties, reducing SO amplitude, density, and slope, yet the circuit-level mechanisms linking structural brain changes to these disruptions remain poorly understood. Here we present a multi-scale, whole-brain thalamocortical network model incorporating biologically grounded human connectivity derived from diffusion MRI tractography, comprising over 10,000 cortical columns per hemisphere with spiking pyramidal and inhibitory neurons and an anatomically differentiated thalamic network. Simulating progressive synaptic loss, we find that selective degradation of recurrent excitatory connectivity, but not excitatory-inhibitory projections, reproduces empirically observed age-related SO changes. Increased SO duration was driven primarily by prolonged Down states, while Up state duration and spike density were reduced, suggesting a possible mechanism for impaired memory consolidation. These results suggest that aging selectively disrupts the temporal structure of SWS critical for interference-free memory consolidation, providing mechanistic insight into cognitive decline in the aging brain.

Supported by: NIH (grants 1R01MH125557, 1RF1NS132913, 1R01AG099626 to MB)

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：慢波睡眠中的慢振荡（Slow Oscillations, SOs）是协调丘脑‑皮层‑海马动态、实现记忆巩固的关键节律。衰老会显著改变 SO 特性（振幅、密度、斜率下降，时程延长），并与认知衰退相关。
- **核心问题**：目前尚不清楚大脑结构衰老（如突触丢失）究竟通过何种环路机制导致 SO 异常。需要明确**哪一种突触通路**的退化是主因，以及从局部神经元活动到宏观脑电信号的跨尺度因果链。
- **整体含义**：通过构建受约束的全脑计算模型，揭示衰老选择性破坏**回返性兴奋（PY–PY）连接**足以重现老年 SO 变化，进而为理解睡眠依赖记忆巩固受损提供环路层面的机制解释。

### 2. 方法论
- **模型架构**：构建了一个多尺度、整半球丘脑‑皮层网络模型。
  - **皮层**：10,242 个皮层柱，每个柱包含 6 层，每层有 1 个锥体神经元（PY）和 1 个抑制性中间神经元（IN）。神经元采用计算高效的**映射模型**（Komarov 等提出的差分方程模型），能够复现 Up/Down 状态转换。
  - **丘脑**：包含丘脑‑皮层中继细胞（TC）和网状核细胞（RE），分为核心和基质系统，采用 **Hodgkin‑Huxley 动力学**。
  - **连接组**：长程皮层‑皮层连接基于 **HCP 多模态图谱**和**扩散 MRI 束路成像**数据构建。连接概率随纤维距离指数衰减，传导延迟与距离成正比。层流连接强度根据大脑皮层区域的**髓鞘层级**进行缩放。
- **老化模拟**：以概率方式选择性移除某一类突触，模拟进行性突触丧失（0%~40%），并对比 PY–PY、PY–IN、IN–PY 等不同连接类型的降解效应。
- **信号采集与分析**：通过在大范围（~150 mm 半径）平均神经元膜电位模拟 EEG 通道（C3、Fz、Oz），小范围（5 mm 半径）模拟局部场电位（LFP）。SO 检测沿用 Djonlagic 等提出的基于振幅阈值和零交叉的方法，随后计算振幅、密度、斜率、半波时程等指标。

### 3. 实验设计
- **经验数据集**：使用 MESA 研究中的年龄分层 EEG 数据（C4‑M1 单通道），以及独立队列的双导联记录（Oz‑Cz、Cz‑Fz），涵盖 50–80 岁人群。以此作为模型老化效应的基准（benchmark）。
- **模型对照**：将模型的 0% 突触丧失状态视作“年轻”基线，通过增加 PY–PY 丧失比例（0–30%）模拟从年轻到衰老的过渡（约 10% 丧失对应最年轻的经验组）。
- **对比方法**：在模型内部进行了消融对比，系统扫描不同 PY–PY、PY–IN、IN‑PY 丧失组合对 SO 振幅的影响，以确定哪种突触丧失能最佳重现经验趋势。
- **跨尺度验证**：同步收集模型生成的 EEG 尺度信号、局部 LFP 信号以及单细胞膜电位，将宏观 SO 形态变化与微观 Up 状态动态联系起来。

### 4. 资源与算力
- 论文中**未明确提及**所使用 GPU 型号、数量、训练时长或具体计算资源需求。考虑到模型规模（超过 10,000 个皮层柱及丘脑神经元）和模拟时长，该研究必然依赖高性能计算，但作者未对这些细节进行说明。

### 5. 实验数量与充分性
- **实验组数**：
  - 系统性扫描 3 类突触（PY–PY、PY‑IN、IN‑PY）在 0–40% 丧失下的多种组合，生成 SO 振幅变化曲面图。
  - 聚焦 PY–PY 丧失（0–30%）绘制全部 SO 指标随丧失程度的变化曲线，并与 3 个 EEG 通道的经验数据进行直接对比。
  - 在“年轻”（0% 丧失）与“老化”（30% PY–PY 丧失）条件下，进行局部 LFP 空间分布比较以及单细胞 Up 状态统计分析。
- **充分性与公平性**：实验设计较为完整，既有不同突触类型的消融，又有与公共人类数据的直接定性／定量对比，还包含跨尺度（EEG ↔ LFP ↔ 单细胞）的机制解释。对比均在同一模型框架下进行，内部基准统一。但外在验证仅限于已发表的群体趋势，缺少对同一样本集的多模态数据直接拟合。

### 6. 主要结论与发现
- **选择性回路损伤**：仅当**回返性兴奋（PY–PY）连接**选择性丧失时，模型才能一致地重现衰老相关的 SO 变化（振幅、密度、斜率降低，时程延长）。削弱 PY–IN 或 IN–PY 通路则不能，甚至产生相反效果。
- **跨尺度机制**：SO 宏观时程延长并非源自局部 Up 状态变长。相反，单细胞 Up 状态变短、发放密度降低且相位同步性减弱。由于皮层群体间同步性下降，时间上分散的局部 Up 状态在 EEG 大空间平均后表现为**展宽的慢波**。
- **记忆受损的可能解释**：老化通过回返兴奋丧失使局部活动变弱、同步性降低，破坏了 NREM 睡眠中用于无干扰记忆巩固的精确时间结构。

### 7. 优点
- **高生物真实性**：通过扩散 MRI 束路成像和髓鞘层级约束，将大规模结构连接转化为涌现动力学，远超传统的小网络模型。
- **明确的因果推断**：通过选择性操纵特定突触类型的消融实验，直接定位到 PY–PY 连接的关键作用，弥补了纯观察性研究的不足。
- **跨尺度桥接**：成功解释了看似矛盾的宏观（SO 变长）和微观（Up 状态变短）现象，揭示了空间平均与同步性丧失导致的尺度效应。
- **可验证性**：将模拟结果与公开发表的人类 EEG 衰老趋势直接比较，为结论提供了经验支撑。

### 8. 不足与局限
- **老化建模的简化**：仅模拟了均匀、随机的突触丧失，未考虑生物衰老中神经元内在兴奋性变化、神经调质改变、区域异质性退化以及白质传导速度下降等复杂因素。
- **半球限制**：模型仅包含单个半球，忽视了半球间连接对大规模慢波同步的潜在贡献。
- **经验数据对齐**：模型 EEG 通道与经验电极位置仅为近似对应，且年龄映射为假设性推断（10% 丧失 ↔ 最年轻组），缺乏逐个体的精细拟合。
- **数据驱动局限**：模型连接组基于年轻成人（HCP），将其直接应用于模拟衰老过程可能忽视了生命周期内连接组本身的重塑。
- **适用范围**：结论主要针对 SO 形态变化，对更广泛睡眠‑记忆巩固异常（如纺锤波耦合等）的解释力有待进一步研究。

（完）
