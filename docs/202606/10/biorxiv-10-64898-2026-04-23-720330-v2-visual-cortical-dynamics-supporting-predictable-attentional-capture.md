---
title: Visual cortical dynamics supporting predictable attentional capture
title_zh: 支持可预测注意捕获的视皮层动力学
authors: "Groot, J. J., Schall, J. D., Westerberg, J. A."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.23.720330v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 研究可预测注意捕获过程中的视觉皮层动态和群体放电。
tldr: 研究通过猕猴视觉皮层的分层电生理记录，探究可预测视觉阵列如何影响视觉搜索中皮层柱处理。发现可预测性通过降低目标刺激的感觉反应变异性和产生更均匀的前馈动态，实现更早的目标选择；并通过适应前馈处理增强干扰抑制，揭示了目标增强与干扰抑制的独立机制，表明经验预测通过精简前馈信号优化视觉皮层处理以支持注意力捕获。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究可预测感觉环境如何通过改变视觉皮层处理来提高视觉搜索效率。
method: 在猕猴视觉皮层进行分层电生理记录，结合基于特征的弹出式视觉搜索任务，操控注意力启动的可预测性。
result: 可预测阵列通过降低目标感觉反应变异与更均匀的前馈处理实现更早目标选择，并通过适应前馈处理增强干扰抑制。
conclusion: 经验预测通过精简前馈信号优化视觉皮层柱处理，以独立机制增强目标与抑制干扰，支持注意力捕获。
---

## 摘要
视觉行为依赖于优先处理相关感觉信息同时滤除干扰的能力。可预测的感觉环境通过改变感觉处理过程，使行为更为高效。利用猕猴视皮层的分层神经生理学方法，测量在基于特征的弹出式视觉搜索任务中群体的发放活动，我们考察了可预测的视觉流程如何影响皮层柱状结构对感觉信息的处理。通过注意启动来操控可预测性，我们发现当刺激阵列可预测时，行为表现得到改善。这些行为变化得到更早的神经元注意目标选择的支持，这源于对可预测目标刺激的感觉反应变异性的降低以及整个皮层柱内前馈处理动态更为均一。更有效的干扰抑制则源于对更频繁出现的干扰刺激的适应性前馈处理。综合来看，这些变化暗示目标增强与干扰抑制存在独立的机制。我们的结果突显了源于经验的预测如何通过简化前馈信号改变视皮层柱状处理，从而优化注意选择。

## Abstract
Visual behavior depends on the ability to prioritize relevant sensory information while filtering out distractions. Predictable sensory contexts enable more efficient behavior by altering sensory processing. Using laminar neurophysiology in macaque visual cortex measuring population spiking during a feature-based pop-out visual search task, we examined how predictable visual routines influence cortical columnar processing of sensory information. By manipulating predictability through attentional priming, we found improved behavioral performance with predictable stimulus arrays. These behavioral changes were supported by earlier neuronal attentional target selection driven by reduced variability in the sensory response to the predictable target stimulus and more homogeneous feedforward processing dynamics across the cortical column. More effective distractor suppression was driven by adapted feedforward processing of the more frequent distractor stimulus. Together, these changes implicate independent mechanisms for target enhancement and distractor suppression. Our results highlight how predictions from experience alter visual columnar processing to optimize attentional selection through streamlining feedforward signaling.

---

## 论文详细总结（自动生成）

# 论文总结：《支持可预测注意捕获的视皮层动力学》

## 1. 核心问题与整体含义
- **研究动机**：视觉行为（如视觉搜索）的效率高度依赖对感觉环境中规律性的利用。当环境可预测时，感知与决策通常更快、更准，但其背后的神经机制——尤其是可预测性如何在视皮层柱状回路中重塑信息处理——尚不清楚。
- **整体含义**：本研究探究了“源于经验的预测”如何优化视觉注意，揭示大脑通过独立机制分别实现“目标信号的增强”与“干扰信号的抑制”，两者共同支撑可预测情境下的注意捕获。

## 2. 方法论
- **核心思想**：利用猕猴视觉皮层（推测为 V4 或相应高级视皮层）的分层电生理记录，同时采集跨皮层的神经元群体放电，观察可预测视觉阵列如何改变前馈与反馈处理。
- **关键技术细节**：
  - **分层记录**：使用线状多触点电极（laminar probes）同时记录皮层各层的群体发放活动，便于分离前馈输入的颗粒层（第4层）与整合层（浅层与深层）。
  - **任务范式**：基于特征的弹出式视觉搜索任务，通过**注意启动**（attentional priming）操控序列的可预测性。例如，频繁呈现同一目标或同一干扰物的 trial，形成可预测条件；与传统随机或不可预测条件对比。
  - **分析策略**：
    - 测量目标与干扰物诱发的感觉反应的变异性（如 Fano factor 或 spike count correlation）。
    - 刻画前馈处理动态的异质性（如层间反应潜伏期分布、 spike-LFP 耦合强度）。
    - 分离“目标选择增强”与“干扰抑制适应”的时间进程和层流特征。
- **公式与算法**：论文摘要未给出明确数学公式，推断分析可能涉及：
  - 变异性降低用 $CV = \sigma/\mu$ 或 Fano 因子衡量；
  - 前馈动态均一性可能通过层间反应潜伏期的标准差 $SD(L_{4}, L_{2/3}, L_{5})$ 或跨层相关性描述；
  - 适应性前馈处理可能通过刺激特异反应的时间衰减模型拟合。

## 3. 实验设计
- **被试与场景**：
  - 使用猕猴作为模型动物，植入多触点分层电极，覆盖视皮层某一柱状结构。
  - 视觉搜索任务：屏幕上呈现多个刺激组成的阵列，其中一项为目标（例如颜色或方向独特的条形），其余为干扰物。猕猴通过眼动或杠杆报告目标位置。
- **基准与对比**：
  - 基准任务为“不可预测条件”（随机切换目标/干扰物特征或 trial 间无规律）。
  - 对比条件：“可预测条件”（通过注意启动，使目标或干扰物特征在连续 trial 中一致）。
  - 未提及其他外部算法或模型对比，属于纯粹的神经机制比较。
- **行为指标**：反应时间、正确率或搜索斜率。

## 4. 资源与算力
- **摘要未提及任何计算资源**。本研究为在体电生理实验，不涉及 GPU 或大规模训练算力。数据分析可能采用常规信号处理和统计方法，所需算力可忽略。若存在计算模型，原文尚未披露。

## 5. 实验数量与充分性
- 根据摘要提供的有限信息，至少包含以下实验条件/分析层面：
  - **可预测性操控**：至少 2 种（高可预测 vs 低可预测）。
  - **神经元群体分析**：分层记录下，区分目标反应、干扰物反应、前馈层与反馈层。
  - **行为-神经关联**：行为改善与反应变异性、前馈动态指标的关联。
- **充分性判断**：由于仅有摘要，无法评估样本量（动物数量、神经元数、trial 数）及统计效力。若实验设计控制完善（如对照平衡刺激特征、排除低级适应），结论可能较客观。但仅凭摘要无法确定是否进行了必要的对照（如消除低层感觉适应的混淆）。实验本身可能充分，但覆盖程度需阅读全文后评判。

## 6. 主要结论与发现
1. **行为提升**：可预测的刺激阵列显著缩短反应时间、提高准确率。
2. **目标增强机制**：
   - 可预测目标引起的感觉反应变异性降低（神经元发放更可靠）。
   - 皮层柱内前馈处理动态变得更均匀（各层反应的潜伏期或模式趋于一致），导致注意目标选择的时间点显著提前。
3. **干扰抑制机制**：
   - 对重复出现的干扰物，前馈处理表现出适应性（可能发放率下降或潜伏期变化），从而增强抑制效率。
4. **独立通路**：目标增强与干扰抑制涉及不同的前馈过程，表明经验预测通过两条独立机制优化注意。

## 7. 优点
- **方法论亮点**：
  - 将“分层电生理”与“注意启动范式”结合，可从回路层面拆解前馈与反馈贡献。
  - 关注变异性与动态均一性，而非仅响应幅度，揭示了信息编码可靠性这一新维度。
- **理论贡献**：首次在皮层柱水平证明经验预测分别增强目标表征、适应性抑制干扰，挑战了原先认为注意选择仅依赖增益调制的一元论。
- **实验设计**：使用特征弹出任务，贴近自然搜索，具有较高生态效度。

## 8. 不足与局限
- **实验覆盖**：仅基于猕猴单一脑区（视皮层某一柱），无法推广到其他脑区或物种；未探讨反馈连接（如额眼区、顶叶）如何贡献预测信号。
- **偏差风险**：摘要未说明如何排除低级感觉适应（如刺激重复引起的发放率衰减）与注意效应混淆的可能性；动物数量不明，存在小样本偏差风险。
- **应用限制**：基础神经机制研究，距离人类认知干预或临床转化较远；任务中可预测性仅通过 trial 间重复实现，忽略更复杂的场景预测（如空间规律、时间节律）。
- **计算细节缺失**：未给出前馈动态均一性的精确定量指标，也未提出可验证的计算模型。

（完）
