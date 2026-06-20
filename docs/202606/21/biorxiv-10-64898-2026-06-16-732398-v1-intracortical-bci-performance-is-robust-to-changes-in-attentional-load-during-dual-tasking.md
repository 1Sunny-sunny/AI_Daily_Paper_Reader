---
title: Intracortical BCI Performance is Robust to Changes in Attentional Load During Dual-Tasking
title_zh: 皮层内脑机接口性能在双重任务中对注意力负荷变化具有鲁棒性
authors: "Canario, E., Shearer, C., Akcakaya, M., Weber, D., Chase, S. M., Collinger, J. L."
date: 2026-06-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.16.732398v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 双任务下脑机接口性能
tldr: 本研究通过双任务实验（iBCI光标控制与N-back工作记忆）结合颅内/头皮脑电，评估注意力负荷对四肢瘫痪患者颅内脑机接口性能的影响。结果显示，尽管注意力负荷增加，iBCI性能总体稳健，仅低信号质量者轻微下降，表明iBCI对注意力变化具有鲁棒性。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索注意力负荷如何影响脑机接口性能，以提升真实多任务环境下的稳定性。
method: 两位四肢瘫痪患者同时执行2D光标iBCI任务和N-back工作记忆任务，记录颅内信号和头皮EEG。
result: EEG显示注意力负荷增加，但iBCI性能总体稳健，仅一名低信号质量参与者出现轻微完成时间和路径长度增加。
conclusion: iBCI性能对注意力负荷具有稳健性，但信号质量差异可能影响结果，需进一步研究认知状态的影响。
---

## 摘要
高性能的皮层内脑机接口（iBCI）控制已在研究环境中得到证实，但其性能在会话内和会话间仍可能有所变化。这种变异性一个潜在来源是注意力负荷的变化，这种变化源于处理自然发生的干扰因素，如思绪、声音、疲劳或疼痛。为了提高iBCI在现实世界环境中表现的一致性，而在此类环境中多任务处理是不可避免的，我们必须了解注意力的转移如何影响性能。在此，我们通过一项2D光标平移加点击的iBCI任务，并结合一项N-Back工作记忆任务来增加双重任务期间的注意力负荷，以检测注意力负荷对iBCI性能和运动相关神经活动的影响。两名患有四肢瘫痪的参与者（P2和P4）在参加一项iBCI设备的长期临床试验（NCT1894802）期间完成了这项研究。通过同步记录头皮脑电图（EEG），测量了注意力的常见神经相关性（θ和α频带功率）。尽管EEG记录和难度评分表明双重任务期间注意力负荷有所增加，但iBCI性能在各种双重任务条件下表现相当稳健。其中一名参与者P2在轻度注意力负荷条件下，试验完成时间和归一化路径长度出现了小幅但显著的增加。两名参与者之间的信号质量差异可能影响了结果，因为P2的信号质量较低，因此可能更容易受到注意力负荷的影响。而P4较高的信号质量可能使他能够在注意力负荷增加的情况下仍保持性能不下降。总体而言，iBCI性能对注意力负荷似乎具有鲁棒性，但在此观察到的复杂趋势反映需要继续研究在不同认知状态下使用BCI的情况，以阐明不同参与者可能面临的潜在挑战和补偿机制。

## Abstract
High performance intracortical brain-computer interface (iBCI) control has been demonstrated in research settings, but performance can still vary within and between sessions. One potential source of this variability is the change in attentional load that comes from processing naturally occurring distractors such as thoughts, sounds, fatigue, or pain. To improve the consistency of iBCI performance in real-world environments where this sort of multi-tasking is inevitable, we must understand how shifts in attention can impact performance. Here we examined the effect of attentional load on iBCI performance and movement-related neural activity using a 2D cursor translation + click iBCI task paired with an N-Back working memory task to increase attentional load during dual-task performance. Two participants (P2 and P4) with tetraplegia completed the study while enrolled in a long-term clinical trial of an iBCI device (NCT1894802). Common neural correlates of attention (theta and alpha band power) were measured with simultaneously recorded scalp electroencephalography (EEG). While the EEG recordings and difficulty ratings suggested increased attentional load during dual tasking, iBCI performance was quite robust across the various dual tasking conditions. One participant, P2, experienced a small but significant increase in trial completion time and normalized path length during the mild attentional load condition. Signal quality differences between the two participants may have impacted the results, as P2 had lower signal quality and was therefore likely more vulnerable to attentional load. P4's higher signal quality likely allowed him to accommodate increased attentional load without a drop in performance. Overall, iBCI performance appears to be robust to attentional load, but the complex trends observed here reflect a need for continued investigation of BCI use under different cognitive states to elucidate potential challenges and compensatory mechanisms across participants.

---

## 论文详细总结（自动生成）

## 1. 论文核心问题与整体含义
本研究关注**皮层内脑机接口（iBCI）在真实多任务场景下的鲁棒性**。  
- 现有研究已证明 iBCI 可在控制环境中实现高性能操作，但**会话内与跨会话的性能波动仍然存在**，其中注意力负荷的变化被视为一个可能的扰动源。  
- 在实际应用中，使用者不可避免地要处理分心刺激（如思绪、声音、疲劳或疼痛），这会增加额外的认知负担，可能干扰脑信号解码。  
- 论文旨在**系统量化注意力负荷对 iBCI 控制性能的影响**，为提升脑机接口在日常环境中的可靠性和可用性提供依据。

## 2. 方法论
核心思路是通过**双任务实验范式**操纵注意力需求，同步记录颅内信号与头皮脑电（EEG），从行为与神经两个层面评估注意力对 iBCI 的影响。  

- **主要任务（iBCI 控制）**：要求被试执行 **2D 光标平移 + 点击任务**，解码算法将颅内神经信号映射为光标移动。  
- **次要任务（注意力负荷操纵）**：引入 **N-Back 工作记忆任务**，通过不同难度（如 0-back, 1-back, 2-back）改变注意力负荷，构建双重任务条件。  
- **注意力装载的神经量化**：同时采集 **头皮 EEG**，提取 **θ 频带功率** 和 **α 频带功率** 作为注意力的已知神经关联物，用于验证注意力负荷是否确实被成功操纵。  
- **分析策略**：对比单任务（仅 iBCI）与不同难度双任务条件下 iBCI 的性能指标，如试验完成时间、归一化路径长度等，并结合 EEG 证据进行推断。  

论文中未出现显式的数理公式或新解码算法，主要依赖统计检验比较条件间的行为与神经信号差异。

## 3. 实验设计
- **被试与设备**：两名四肢瘫痪患者（P2 和 P4），均参与一项长期 iBCI 设备临床试验（NCT1894802）。  
- **任务与场景**：在 2D 屏幕中控制光标进行平移与点击，次级任务采用听觉/视觉 N‑Back 任务，构成不同注意力负荷的**双任务场景**。  
- **条件对比**：实验设置多个条件，至少包括单任务基线、轻度负荷双任务、较重度负荷双任务。不涉及与其他解码方法或模型的横向对比，属于**同一系统在不同认知状态下的自身对照实验**。  
- **测量指标**：  
  - **iBCI 指标**：试验完成时间、归一化路径长度（反映控制效率与平滑性）。  
  - **注意力指标**：头皮 EEG 的 θ/α 频带功率、主观难度评分。  

## 4. 资源与算力
论文中所描述的研究不涉及大规模模型训练或高性能计算需求，因此**未提及 GPU 型号、数量或训练时长**。所用的计算资源可能仅限于标准的信号处理与统计软件（如 MATLAB、Python 等），无需特别说明算力消耗。

## 5. 实验数量与充分性评估
- **实验规模**：以两名被试（P2 和 P4）为基础，每人完成多个双任务条件与试次。尽管未给出精确试次数，但已涵盖单任务与多个注意负荷水平，并进行了 EEG 同步验证。  
- **消融与分析**：除主要的行为绩效对比外，还针对**信号质量**差异做了解释性分析，试图区分个体差异的干扰。  
- **充分性评价**：  
  - **优势**：实验范式内在逻辑清晰，同时从主观评分和 EEG 神经标记物两方面确认注意力操纵有效，结论具有一定的内部效度。  
  - **局限**：被试数量极少（N=2），结论普遍性受限；条件数量或重复次数在摘要中未详细披露，可能影响统计功效。整体而言，作为一项以被试内比较为主的探索性研究，实验设计基本客观公平，但**外部推广性较弱**。

## 6. 主要结论与发现
- **注意力负荷确实增加**：头皮 EEG 的 θ 和 α 频带功率变化趋势、以及被试主观难度评分，均证实双任务期间注意力负荷被有效提高。  
- **iBCI 性能总体稳健**：在大多数双任务条件下，光标控制绩效未出现显著恶化。  
- **个体差异显现**：仅信号质量较低的参与者 P2 在轻度注意力负荷下，出现了**试验完成时间和归一化路径长度的轻微但统计显著增加**；信号质量较高的 P4 则完全不受影响。  
- **推断**：高信号质量可能为神经系统提供了足够的“冗余”，使解码在注意力被部分占用时仍保持稳定；低信号质量环境则可能暴露脆弱性。iBCI 性能对注意力负荷具有鲁棒性，但仍需关注个体认知状态与信号质量之间的相互作用。

## 7. 优点
- **双重验证注意力负荷**：同时使用行为学评分和 EEG 神经标记物，避免仅凭主观报告或任务参数假设置信度不足。  
- **贴近实际使用场景**：采用双任务范式模拟日常必需的多任务处理，提升了研究结果的生态效度。  
- **对个体差异的重视**：主动对比两位参与者的信号质量并解释绩效差异，为未来个性化 BCI 参数调整提供思路。  
- **长期植入临床试验被试**：数据取自真实慢性四肢瘫痪患者且处于在线控制状态，比离线模拟或健康被试更接近目标应用人群。

## 8. 不足与局限
- **样本量极小**：仅 2 名被试，结论无法直接推广到更广泛的 iBCI 用户群体，异质性来源未能充分发掘。  
- **注意力操纵范围较窄**：仅通过 N‑Back 任务增加工作记忆负荷，未涵盖其他类型的分心（如情绪扰动、持续性疼痛或视觉杂乱场景），注意力概念覆盖不全面。  
- **信号质量差异可能遗漏变量**：虽然作者提出信号质量解释，但未通过系统操控质量或对比更多维度（如解码器类型）来排除混淆。  
- **缺乏长期稳定性证据**：实验在一个或少数几次会话内完成，未考察注意力对跨天、跨会话性能漂移的贡献。  
- **未明确解码器适应机制**：未分析解码器权重是否在负荷条件下发生动态调整，也未测试闭环系统本身对注意力变化的补偿能力。  
- **算力与重复性信息缺失**：若涉及离线重分析或高计算量预处理，文中未提供相关细节，不利于完全复现。

（完）
