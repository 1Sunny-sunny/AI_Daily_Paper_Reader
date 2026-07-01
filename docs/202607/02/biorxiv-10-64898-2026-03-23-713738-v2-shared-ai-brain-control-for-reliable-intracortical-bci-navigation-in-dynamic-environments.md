---
title: Shared AI-brain control for reliable intracortical BCI navigation in dynamic environments
title_zh: 共享AI-大脑控制实现动态环境中可靠的皮质内脑机接口导航
authors: "Saussus, O., Song, P., De Schrijver, S., Caprara, I., Detry, R., Janssen, P."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.23.713738v2.full.pdf"
tags: ["query:sr"]
score: 10.0
evidence: 带有AI副驾驶的皮层内脑机接口共享控制
tldr: 为解决脑机接口在动态环境中因神经指令波动导致的可靠性问题，研究开发了信心调制的AI-大脑共享控制框架，通过自适应整合解码指令与概率时间先验来稳定执行，同时保持用户意图。在猕猴虚拟导航实验中，该框架几乎消除了碰撞和过冲等执行失败，但目标突变时会出现短暂延迟。重置时间先验可恢复性能，表明限制源于算法而非解码。该工作为神经假体的安全控制提供了设计原则。
source: biorxiv
selection_source: fresh_fetch
motivation: 脑机接口在动态环境中因解码神经指令的波动而可靠性受限。
method: 提出信心调制的AI-大脑共享控制框架，自适应整合解码神经指令与概率时间先验以稳定执行。
result: 共享控制几乎消除了执行失败，但突然目标变化时短暂延迟，重置时间先验可恢复性能。
conclusion: 该框架揭示了连续脑机接口导航的机制，并为动态环境中的神经假体控制确立了更安全可靠的设计原则。
---

## 摘要
皮质内脑机接口(iBCIs)可以帮助瘫痪患者控制辅助设备，但在动态环境中的可靠操作仍受限于神经解码命令的波动。本文开发了一种置信度调制的AI-大脑共享控制框架，其中人工智能副驾驶通过概率时间先验自适应地整合解码的神经命令，以在保留用户意图的同时稳定执行。在两只猕猴执行的复杂环境闭环虚拟导航任务中，共享控制几乎消除了执行层面的失败，包括障碍物碰撞和目标超调，同时保持了神经命令的方向结构。目标的突然变化揭示了一个边界条件：当近期历史不再具有预测性时，时间稳定性会暂时延迟响应能力。离线回放显示，重置时间先验可消除这一滞后并恢复性能，表明该障碍是算法性问题而非神经解码失败。这些结果提供了对置信度调制的AI-大脑共享控制用于连续皮质内BCI导航的机制性表征，并确定了在动态环境中更安全、更可靠的神经假体控制的设计原则。

## Abstract
Intracortical brain-computer interfaces (iBCIs) can enable people with paralysis to control assistive devices, but reliable operation in dynamic environments remains limited by fluctuations in decoded neural commands. Here we develop a confidence-modulated AI-brain shared-control framework in which an artificial intelligence copilot adaptively integrates the decoded neural commands with a probabilistic temporal prior to stabilize execution while preserving user intent. In two macaques performing closed-loop virtual navigation tasks in complex environments, shared-control nearly eliminated execution-level failures, including obstacle collisions and target overshoot, while maintaining the directional structure of neural commands. Abrupt target changes revealed a boundary condition: temporal stabilization transiently delays responsiveness when recent history was no longer predictive. Offline replay showed that resetting the temporal prior eliminated this lag and restored performance, demonstrating that the impairment was algorithmic rather than a failure of neural decoding. These results provide a mechanistic characterization of confidence-modulated AI-brain shared control for continuous intracortical BCI navigation and identify design principles for safer and more reliable neuroprosthetic control in dynamic environments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景与动机**：皮质内脑机接口（iBCI）可将瘫痪患者的神经活动转化为控制信号，以驱动外部辅助设备。然而，解码出的神经命令（速度指令）在短时间尺度上存在固有波动，这些波动并非总是反映用户真实意图的变化，却会直接导致设备运动不稳定，在杂乱环境中累积为碰撞、轨迹不稳定或目标失败。
- **核心问题**：如何在动态、有约束的环境中，既稳定不可靠的神经命令执行，又保留对用户真实意图变化的快速响应性。现有共享控制方法要么过度依赖自主规划，稀释用户控制感，要么采用固定混合策略，难以自适应解码可靠性波动。
- **整体含义**：论文提出“置信度调制的AI-大脑共享控制”不仅是一个解码后处理策略，更是一个使能层，其意义在于将不稳定的、但包含目标信息的神经控制转化为稳定可用的执行动作，而非替代用户决策。

### 2. 论文提出的方法论
- **核心思想**：将解码神经命令视为对用户意图的含噪观测，通过一个概率化的“时间先验”（temporal prior）建模近期运动历史与环境的协同关系，在线性推理中动态仲裁“AI先验”（稳定化）与“BCI命令”（响应性）的权重。仲裁权重由先验置信度（$\alpha$，基于先验熵）自适应调整，实现“当命令一致且可预测时增大稳定化，当命令混乱或突变时增大响应性”。
- **关键技术细节与算法流程**（文字说明）：
  - **意图先验建模**：使用一个轨迹高斯混合模型，预测候选未来速度轨迹 $\xi$ 的条件分布 $p(\xi|\zeta, c)$，其中 $\zeta$ 为近8步（400毫秒）解码速度历史，$c$ 为环境上下文（目标候选位置、障碍物）。模型通过模拟轨迹和监督微调（使用BCI控制轨迹）预训练。
  - **贝叶斯融合与执行**：在每一个50ms更新步，将当前解码速度 $v$ 作为似然 $p(v|\xi)$，计算后验分布 $p(\xi|\zeta, c, v) \propto p(v|\xi)p(\xi|\zeta, c)$。从后验中采样轨迹并利用成本函数（惩罚碰撞，奖励接近目标）选优，执行其所含瞬时速度。
  - **置信度仲裁与安全优先**：仲裁强度由时间先验熵 $H(p(\cdot|\zeta, c))$ 决定。定义置信度指数 $\alpha = 1 - \text{归一化熵}$。$\alpha$ 高时输出偏向平滑、目标导向；$\alpha$ 低时紧密跟随BCI命令。若当前BCI命令判定为“即将碰撞”，则触发150毫秒的完全先验覆盖（安全覆盖），强行避障后立即返回共享模式。
  - **方法定位**：该控制器（RT-V2）位于解码器下游，仅使用解码运动学和任务环境，不直接接收原始神经信号。

### 3. 实验设计
- **实验平台与场景**：两只植入96通道Utah阵列的猕猴，执行三维虚拟环境下的二维修道球导航任务。运动控制完全由解码的神经速度信号驱动，无实体动作。
- **任务与对比基准**：
  - **固定障碍物任务**：起点与目标之间存在固定障碍物（基准：BCI-only控制）。
  - **障碍物出现任务**：行进中意外出现障碍物（基准：BCI-only控制）。
  - **目标重生任务**：行进中目标突然跳跃至相邻位置（基准：BCI-only控制）。
- **对比方法**：本文未直接对比其他共享控制算法，核心对比为同一解码器下的“共享控制”与“BCI-only”控制模式，以量化共享控制相对于直接解码执行的增益。

### 4. 资源与算力
- **文中提及**：论文未明确说明AI共享控制模块训练或推理所需的具体计算资源，如GPU型号、数量或训练时长。推断共享控制模型（RT-V2）可实时运行于50ms的闭环更新频率中。

### 5. 实验数量与充分性
- **实验数量**：实验覆盖了两种动物，三种具有互补挑战性的任务范型，总计跨越多个会话和数月时间。每个任务每只猴均完成了9-12个有效会话。分析包括了跨会话的平均性能、逐目标增益、失败模式分类、事件相关先验置信度动态，以及一个关键的离线回放消融实验（重置时间先验）。
- **实验充分性与客观性**：实验设计具有高度充分性和对比公平性。固定障碍任务作为基准，障碍物出现任务测试对突发环境的稳定，目标重生任务专门测试对意图突变的响应——构成对算法的系统压力测试。离线回放实验直接拆除了时间先验的干扰，明确了响应滞后的算法性来源，避免了解码信号质量改变的干扰。逐目标增益与基线性能关系的二次拟合分析，揭示了算法在何种条件下最有效。

### 6. 论文的主要结论与发现
- **显著提升执行可靠性**：在障碍物任务中，共享控制大幅提升成功率（约30个百分点），显著降低或消除了碰撞和目标超调等执行层面失败，使障碍物避障轨迹更平滑、裕度更大。
- **选择性稳定而非意图修正**：共享控制将“解码方向正确”（即含有部分正确目标信息）的噪杂命令转化为成功执行，但无法拯救解码方向系统错误（指向错误目标）的试次。成功概率由解码状态决定。
- **揭示仲裁边界条件**：目标突变时，共享控制的成功率反低于纯BCI控制。表现为执行速度滞后于解码意图，且时间先验衰减慢。离线回放重置先验后性能即刻恢复，证明限制根源于算法的时间惯性，非神经网络解码失效。
- **事件相关的仲裁动态**：仲裁置信度 $\alpha$ 对环境突变（障碍出现、目标重生）呈现瞬态下降再恢复的特征，解释了共享控制在突发变化下的灵活性受限现象。

### 7. 优点
- **机制性的仲裁设计**：以时间先验的归一化熵为驱动的自适应仲裁机制，简洁且提供了在线可控的量化的置信度指标（$\alpha$），优于固定融合。
- **目标明确的执行稳定器定位**：清晰将共享控制功能界定为“稳定含噪声的正确意图”，而非“自主规划与纠正错误”，在哲学和工程上更适合高带宽侵入式BCI。
- **严谨的边界条件探究**：通过特意设计的目标重跳任务和富有洞见的离线“重置先验”实验，系统、客观地展示了方法当前的缺陷及原因，为其改进指出了方向。
- **解码器普适性**：系统作为解码器下游模块，原则上可耦合至任何产生连续命令的BCI系统。

### 8. 不足与局限
- **实验覆盖**：
  - **对比基线有限**：仅与纯BCI控制对比，未与其他共享控制策略（如固定混合、预测性目标推断）进行横向比较。
  - **环境与对象限制**：在结构化的恒河猴虚拟导航任务中完成，目标预定义且数量有限。未覆盖真实物理环境、更自由度的末端器操作及人类临床对象。
- **偏差风险**：
  - **先验对准确度依赖**：该方法不能纠正解码器根本性错误，其有效运行边界取决于解码器提供信息的基本正确性。
  - **突变响应缺陷依赖外部检测**：当前框架在未收到目标变化的明确信号时无法主动重置先验。对 $\alpha$ 骤降的检测可能成为触发先验重置的在线机制，但文内未深入开发。
- **应用限制**：需要预先获取或在线感知密集的环境信息与候选目标，这在实际动态场景（如轮椅导航）中会引入环境感知与目标预测的级联误差。对防止碰撞的绝对安全覆盖打断了用户连续控制，过度触发可能损害用户控制感。

（完）
