---
title: Proactive visual and motor prioritization differentially scale with cue reliability
authors: "Wang, S., van Ede, F."
date: 2026-06-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.28.702371v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 研究视觉和运动优先级的神经动态随线索可靠性的变化
tldr: "本研究探讨环境线索可靠性如何影响工作记忆中视觉与运动的主动优先化。通过操作线索可靠性（100%、80%、60%），利用EEG记录人类被试在视觉-运动工作记忆任务中的神经动态，发现视觉优先化的强度与时间进程相对稳定，不受线索可靠性影响；而运动优先化随可靠性降低显著减弱且发展更渐进，表明运动准备比视觉准备更谨慎，需更高确定性才充分部署。"
source: biorxiv
selection_source: fresh_fetch
motivation: 以往研究孤立考察视觉或运动优先化，缺乏对两者在变化线索可靠性下如何共同运作的了解。
method: "采用视觉-运动工作记忆任务与EEG，操控线索可靠性（100%、80%、60%），同时分离视觉与运动优先化的神经动态。"
result: 视觉优先化在不同线索可靠性下保持相对稳定，而运动优先化随可靠性降低显著减弱且发展更缓慢。
conclusion: 视觉与运动优先化对线索可靠性的敏感性存在本质差异，运动优先化更为谨慎，需更高确定性才充分展开。
---

## Abstract
Environmental cues enable the brain to anticipate and prepare for upcoming behavior, such as by selectively prioritizing relevant visual representations and associated action plans in working memory in service of an imminent task. While it has been demonstrated that neural dynamics of visual and motor prioritization each scale with cue reliability, studies to date tracked either visual or motor prioritization in isolation. It therefore remains unknown whether visual and motor prioritization scale similarly or differently with cue reliability. To fill this gap, we manipulated cue reliability (100%, 80%, 60%) in a visual-motor working-memory task that uniquely enabled us to isolate the neural dynamics associated with visual and motor prioritization in anticipation of an imminent working-memory task. EEG measurements in male and female human volunteers revealed how cue reliability differentially drives visual and motor prioritization. While the strength and timing of visual prioritization were relatively stable across cue reliability levels, motor prioritization profoundly scaled with cue reliability and developed more gradually with lower certainty. These findings show that visual and motor prioritization in working memory are differentially susceptible to the certainty conveyed by environmental cues, and suggest that motor prioritization may be more cautious in nature.

Significance StatementTo cope with the ever-changing world, the human brain continuously leverages environmental cues to anticipate upcoming behavior, such as by prioritizing relevant visual representations and action plans  in mind. Yet, in a volatile world, environmental cues typically vary in the certainty they provide. Building on prior work studying visual or action prioritization in isolation, we uniquely studied how cue certainty shapes both visual and motor prioritization within the same task. We unveil how cue certainty distinctly drives visual and action prioritization, with action prioritization requiring more certainty before deployment, whilst also being deployed more gradually at lower certainty. Thus, prioritization of potential actions is distinct from--and more cautious than--prioritization of the visual representations that guide these actions.

---

## 论文详细总结（自动生成）

由于目标论文网站被 Cloudflare 安全服务拦截，无法获取完整 PDF，以下总结主要基于摘要和提供的元数据信息。部分细节（如方法实现、算力资源、具体实验数量等）因无法访问原文而缺失，文中会明确标注。

---

## 1. 论文的核心问题与研究动机

- **核心问题**：环境线索的可靠性（确定程度）如何分别影响工作记忆中的**视觉优先化**（提前激活相关视觉表征）与**运动优先化**（提前准备动作计划）？
- **研究动机与背景**：
  - 以往研究已证明，大脑能利用环境线索提前优先处理与即将执行任务相关的视觉信息和行动方案，且视觉优先化与运动优先化的神经动态各自会随线索可靠性变化。
  - 然而，这些研究往往**孤立**地考察视觉或运动优先化，两者在**同一任务下、线索可靠性变化时是否以相同或不同方式缩放**尚不清楚。
  - 本研究旨在填补这一空白，揭示视觉与运动优先化对线索确定性的敏感性是否存在本质差异。

---

## 2. 方法论

### 2.1 核心思想

- 在人类被试执行**视觉‑运动双重工作记忆任务**时，通过**系统操纵线索可靠性**（100%、80%、60%），并利用**脑电图（EEG）** 同时但分离地追踪视觉优先化和运动优先化的神经动态。

### 2.2 关键技术细节

- **任务设计**：采用视觉‑运动工作记忆任务，其中：
  - 首先呈现一个**线索**，提示即将进行的记忆任务，但线索的可靠性被操控（100% 完全确定，80% 和 60% 有一定概率误导）。
  - 随后被试需维持视觉记忆内容，并准备与之关联的特定运动反应。
- **神经动态分离策略**（基于摘要与常识推断）：
  - **视觉优先化**的神经指标：通常可通过后部脑区的 α 振荡（如视觉空间注意引起的对侧 α 功率下降）、对侧延迟活动（CDA）或事件相关电位等来追踪。
  - **运动优先化**的神经指标：通常可通过中央‑运动区的 β 频段（13‑30 Hz）去同步化（mu/beta suppression）、侧化准备电位（LRP）等来追踪。
  - 通过时间‑频率分析和多变量模式分析（如解码），从 EEG 信号中同时提取并分离两种优先化的时间过程与强度。
- **公式/算法流程**：文中未提供具体数学模型，但典型分析包括：
  - 时频分解（如小波变换或短时傅里叶变换）得到功率 $P(t,f)$；
  - 条件对比（如对侧 vs. 同侧）提取注意/准备效应；
  - 统计检验（如重复测量 ANOVA 或基于簇的置换检验）评估线索可靠性的影响。

---

## 3. 实验设计

- **被试**：男性和女性健康人类志愿者（具体人数因无法访问全文而未知）。
- **实验场景/任务**：视觉‑运动工作记忆任务。被试需根据线索提示，提前对视觉刺激进行记忆并准备对应的运动反应，而线索的可靠性在试次间变化。
- **实验条件（Benchmark）**：
  - 基准/完全确定条件：线索可靠性 100%。
  - 降低确定性条件：80%、60% 可靠性。
- **对比方式**：
  - **主要对比**：同一任务内，视觉优先化 vs. 运动优先化在不同线索可靠性下的神经动态差异（强度和时序）。
  - 未对比外部“方法”，而是内在认知过程的对比。

---

## 4. 资源与算力

- 原文未提及所用的计算资源（如 GPU 型号、数量、训练时长）。这是一项**人类 EEG 实验研究**，计算主要在离线数据分析（Matlab/Python 脚本），通常不需要大规模 GPU 训练。若文中有涉及，因访问受限无法核实。

---

## 5. 实验数量与充分性

- 因无法获取全文，**无法准确报告**被试数量、总试次、每种可靠性条件的试次分配、以及可能的控制实验或消融分析。
- 根据该领域常规做法推断：
  - 采用**被试内设计**，每个被试完成三种可靠性条件下的多试次任务，以确保足够统计效力。
  - 通常会报告效应量、置信区间，并进行多重比较校正。
  - 可能还包含行为数据（反应时、正确率）分析，以验证可靠性操控的有效性。
- 从摘要结论看，结果具有统计学显著性，且视觉与运动表现出**分离的响应模式**，实验设计应具备检测这种分离的能力。但在无法查阅方法部分的情况下，难以判断是否存在偏差风险（如试次数量不足、未控制混淆变量等）。

---

## 6. 主要结论与发现

- **视觉优先化的稳定性**：视觉优先化的**强度和时间进程**在不同线索可靠性下保持相对稳定，不受确定性降低的显著影响。
- **运动优先化的灵敏性**：运动优先化随着线索可靠性降低而**显著减弱**，且其发展更加**渐进缓慢**。确定性越低，运动准备越弱、越迟缓。
- **本质差异**：运动优先化比视觉优先化**更为谨慎**，需要更高的环境确定性才会充分、快速地部署。
- **意义**：工作记忆中，对未来可能动作的优先准备是一种**审慎的、有条件的过程**，而对视觉表征的优先化则更为**鲁棒**，可在不确定条件下依然维持。

---

## 7. 优点

- **创新性实验设计**：首次在同一任务中同时分离并对比视觉与运动优先化，直接回答了二者对线索确定性的依赖差异。
- **清晰的神经分离**：利用 EEG 的高时间分辨率，能够实时追踪两种优先化的动态演变，揭示时序差异（视觉保持稳定，运动逐渐展开）。
- **理论贡献**：提出了“运动优先化更谨慎”的新观点，更新了人们对工作记忆中主动预加工机制的理解，认为视觉准备和运动准备不是统一调制的单一过程。

---

## 8. 不足与局限

- **缺乏全文细节**：由于无法访问完整论文，无法评估方法细节（样本量、统计方法、控制变量、可能的混淆因素），也不能判断实验是否充分、客观。这构成本次总结的主要局限。
- **潜在偏差风险**：
  - 样本可能较小，结论的推广性需更大样本验证。
  - 仅使用单一类型视觉刺激和简单运动反应（如左右按键），生态效度有限。
- **模态单一**：仅使用 EEG，未结合 fMRI 等空间高分辨率手段，无法揭示优先化差异的精确脑网络机制。
- **因果关系未明**：研究仅是相关性分析（大脑活动与线索可靠性的关联），未能通过神经调控（如 TMS）证明因果关系。
- **应用限制**：结果虽具基础科学价值，但距离临床或工程应用（如脑机接口）尚有距离，且线索仅为概率性提示，未模拟更复杂的环境动态。

---

（完）
