---
title: Dynamic Reversal of IT-PFC Information Flow Orchestrates Visual Categorization Under Perceptual Uncertainty
title_zh: IT-PFC信息流的动态逆转协调感知不确定性下的视觉分类
authors: "Abouhadi, Z., Karimi-Rouzbahani, H."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2025.12.17.695044v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 颅内记录和连接性分析以解码随时间的信息流
tldr: 本研究通过记录猴子执行延迟匹配类别任务时的颅内神经活动，并结合新开发的基于模型的表征连接分析框架，揭示了IT-PFC信息流方向受知觉确定性动态调节：高确定性时维持经典前馈，低确定性时出现早期PFC至IT的反馈流，携带内容特异性信息，挑战了固定层次模型，证明大脑动态重构交互以适应知觉难度。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究知觉确定性是否动态调节IT至PFC的信息流方向。
method: 开发了基于模型的表征连接分析（RCA），同时追踪猴猴延迟匹配类别任务中IT与PFC的信息流内容、时间和方向。
result: 低确定性下信息流方向反转，出现早期PFC至IT的反馈流，携带刺激特异性信息。
conclusion: 大脑根据感知不确定性动态重构IT-PFC交互，PFC在模糊时提供自上而下偏置以优化分类。
---

## 摘要
分类依赖于感觉表征与认知控制之间的动态相互作用，但经典观点认为存在从颞下皮层（IT）到前额叶皮层（PFC）的固定前馈信息流。这种层级方向性是否适应认知情境（如感知确定性），仍是系统神经科学的一个基本问题。我们通过记录猴子执行延迟匹配类别任务时的颅内神经活动来研究此问题。我们开发了一种新颖的连接框架——基于模型的表征连接分析（RCA），以同时追踪IT和PFC之间信息流的内容、时间和方向，同时控制常见的任务一般表征。我们的结果显示，虽然两个脑区都快速编码了任务相关信息，但信息流的方向性受到刺激确定性的高度调节。对于高确定性刺激（远离类别边界），我们观察到经典的从IT到PFC的前馈流。然而，对于低确定性刺激（靠近类别边界），这一层级动态逆转，出现从PFC到IT的主导性早期反馈流，先于前馈扫荡。这种反馈信号携带与模糊刺激相关的特定内容信息，提示采用了一种自上而下的机制来优化感觉表征。这些发现挑战了视觉处理的固定层级模型，提供了机制性证据，表明大脑根据感知难度动态重新配置感觉与执行区域之间的相互作用。我们提出，当感觉证据模糊时，PFC向IT皮层启动自上而下的偏向信号，作为一种适应性的、情境驱动的控制机制。

## Abstract
Categorization relies on a dynamic interplay between sensory representation and cognitive control, yet the classical view posits a fixed, feed-forward information flow from the inferotemporal (IT) cortex to the prefrontal cortex (PFC). Whether this hierarchical directionality adapts to cognitive context, such as perceptual certainty, remains a fundamental question in systems neuroscience. We investigated this by recording intracranial neural activity in monkeys performing a delayed match-to-category task. We developed a novel connectivity framework, Model-Based Representational Connectivity Analysis (RCA), to simultaneously track the content, timing, and directionality of information flow between IT and PFC while controlling for common task-general representations. Our results revealed that while both areas rapidly encoded task-relevant information, the directionality of information flow was highly modulated by stimulus certainty. For high-certainty stimuli (far from the category boundary), we observed the classical feed-forward flow from IT to PFC. However, for low-certainty stimuli (near the category boundary), this hierarchy dynamically reversed, with a dominant, early feedback flow from PFC to IT preceding the feed-forward sweep. This feedback signal carried content-specific information related to the ambiguous stimuli, suggesting a top-down mechanism recruited to refine sensory representations. These findings challenge fixed-hierarchy models of visual processing, providing mechanistic evidence that the brain dynamically reconfigures the interactions between sensory and executive areas as a function of perceptual difficulty. We propose that the PFC initiates a top-down biasing signal to the IT cortex when sensory evidence is ambiguous, serving as an adaptive, context-driven control mechanism.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义
- **研究动机**：传统观点认为，视觉分类依赖颞下皮层（IT）到前额叶皮层（PFC）的固定前馈信息流，但这种层级方向是否随认知情境（尤其是感知不确定性）动态调整，仍是一个基本未解的问题。
- **整体含义**：论文挑战了经典的固定层级处理模型，旨在揭示大脑在面对模糊刺激时，是否通过重新配置感觉与执行脑区间的交互（如信息流方向的反转），实现适应性的认知控制，从而优化分类决策。

## 2. 论文提出的方法论
- **核心思想**：开发一种新型连接分析框架——**基于模型的表征连接分析（Model-Based Representational Connectivity Analysis, RCA）**，同步追踪IT与PFC之间信息流的方向、内容和时序，同时剔除任务通用的、非特异性的表征混淆。
- **关键技术细节**：
  - RCA框架通过构建模型驱动的表征相似性度量，分离出信息流中携带的**内容特异性信息**（即与刺激特征或类别相关的表征）。
  - 能够控制常见的任务一般表征（如运动准备、决策阈值等），从而更纯净地提取脑区间方向性的信息传递。
  - 结合高时间分辨率的颅内神经记录，可在毫秒级解析前馈扫荡与反馈信号的先后顺序，推断信息流的方向性（IT→PFC 或 PFC→IT）。

## 3. 实验设计
- **数据与场景**：采用清醒猕猴执行**延迟匹配类别任务**，同时记录IT与PFC区域的颅内神经活动。刺激被分为两类：远离类别边界的**高确定性刺激**，以及靠近类别边界的**低确定性（模糊）刺激**。
- **比较基准与方法**：
  - 基准为经典固定前馈层级模型，并隐含对比了不同刺激确定性条件下的信息流方向。
  - 研究本质上通过操纵感知确定性水平，比较了高、低确定下信息流方向的时间动态，而非直接与其他连接方法（如Granger因果）进行系统benchmark对比（摘要未提及对比其他方法）。
- **实验设计亮点**：通过刺激类别边界的精确定义，确保了对感知不确定性的强力操控；延迟匹配任务设计分离了感觉编码与决策阶段，有助于解析时序。

## 4. 资源与算力
- **算力说明**：论文未提及使用GPU、训练深度学习模型等信息。主要实验依赖电生理数据采集与分析，所需计算资源集中在神经信号处理和统计建模上，未明确说明算力配置。

## 5. 实验数量与充分性
- **实验组设置**：至少包含两类确定性条件（高 vs. 低）下信息流方向的对比，可能还含有不同脑区间、不同刺激类别边界的操作。由于基于摘要和元数据，具体试次数、猴子数量、刺激类别数等细节未知，尚无法评判其统计充分性。
- **充分性评估**：从方法设计看，RCA框架同时考察方向、内容与时间，结合了实验操纵与模型推断，逻辑链条自洽，但具体样本量和统计效力需查看原文确认。

## 6. 论文的主要结论与发现
- **方向性逆转**：对于高确定性刺激，再现了经典的从IT到PFC的前馈信息流；对于低确定性刺激，层级方向发生动态反转，出现**早期的、主导性的PFC→IT反馈流**，且该反馈流先于前馈扫荡。
- **内容特异性**：反馈信号携带了与模糊刺激相关的特定内容信息，提示PFC向IT发送自上而下的偏向信号，用以优化感觉表征。
- **理论贡献**：实验证据表明，视觉处理并不遵循固定层级，大脑能根据感知难度动态重构感觉与执行区域的交互，PFC在感觉证据模糊时主动介入，扮演适应性控制角色。

## 7. 优点
- **方法创新**：RCA框架实现了信息流内容、时间和方向的同步解耦，并控制了任务通用表征，提供了比传统连接分析更精细的视角。
- **因果推论潜力**：通过线索化时间先后（反馈先于前馈）来推断方向性，增强了结果的说服力。
- **理论突破**：有力挑战了视觉系统中固定层级的前馈经典，揭示了感知不确定下自上而下控制的动态机制，对理解大脑的适应性认知具有重要启示。

## 8. 不足与局限
- **信息不完整**：仅基于摘要和元数据，无法获知实验的样本数量、统计细节、重复性以及可能的数据变异性，难以全面评估结论的稳健性。
- **相关性证据**：颅内记录揭示的是相关性顺序，虽然通过精细时序可推断方向，但缺少因果干扰实验（如微刺激或短暂失活PFC）的直接验证。
- **任务与物种泛化**：结论基于猕猴的延迟匹配类别任务，向其他任务范式、其他物种或人类大脑的推广有待验证。
- **方法敏感性**：RCA方法依赖先验表征模型，模型的选取可能影响对“内容特异性”的定义，且对不同噪声水平和时间分辨率的敏感性未在摘要中讨论。

（完）
