---
title: Electrolytic-Microbubble Dynamics Delineate Safety Thresholds During Intracortical Microstimulation with Flexible Neural Interfaces
title_zh: 电解微气泡动力学界定柔性神经接口皮层内微刺激的安全阈值
authors: "Iliasov, A., Ma, H., Li, F., Chen, Z., Xu, M., Yu, C., Li, R., Wu, J., He, F."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.733032v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 柔性神经界面的皮层内微刺激安全性研究
tldr: 本研究利用双光子活体成像与电生理学，在清醒小鼠中探究柔性神经电极皮层内微刺激时，气泡形成与血管损伤的电流依赖关系。发现气泡尺寸随电流平方增大，低电流（20-40 μA）下血管漏出有限可逆，高电流（≥60 μA）则引发广泛外渗和电极损坏，定义了安全阈值。多物理仿真揭示气泡通过电场重分布调控损伤模式，为脑机接口设计提供机制性安全窗口。
source: biorxiv
selection_source: fresh_fetch
motivation: 皮层内微刺激中安全有效电流范围的微观机制尚不明确，亟需厘清气泡动力学与神经血管损伤的关联。
method: 结合双光子活体成像、电生理记录和多物理仿真，在清醒小鼠中系统观测不同电流下柔性电极周围气泡生成与血管渗漏。
result: 低电流时气泡引发局部可逆渗漏，高电流下气泡尺寸剧增并导致场主导的广泛血管破坏和运动反应，仿真重现了非线性损伤转变。
conclusion: 研究明确了柔性电极微刺激的安全电流区间，并识别气泡辅助血管通透性升高为高电流下的关键失效模式，为神经假体设计提供依据。
---

## 摘要
采用超柔性神经电极的皮层内微刺激（ICMS）能够实现低阈值、长期稳定且高分辨率的神经回路调控，为感觉恢复和闭环神经调控提供了可行策略。然而，界定其安全有效电流范围的微观机制仍不清楚。在此，我们在清醒小鼠中结合活体双光子成像和电生理学技术，研究通过超柔性阵列施加电荷平衡刺激时的电流依赖性神经血管效应。我们在ICMS过程中观察到电极周围形成气泡，气泡尺寸随电流幅值呈二次方增长，符合法拉第气泡生长模型。活体双光子成像显示，在低至中等电流（20–40 μA）下，血管渗漏较小、空间局限且大多可逆，而较高电流（≥60 μA）则导致剧变性的大范围、电场主导的外渗及继发性血管破坏。这一转变与即时的、与刺激锁时的运动反应以及电极退化的发生相吻合。多物理场仿真通过纳入气泡引起的电场重分布和电压依赖的血管壁通透性，复现了所观察到的渗漏-电流非线性关系。模型表明，气泡作为局部电场调节器，在较低电流下将超阈值电场集中在气泡边界附近，同时屏蔽较远处的血管段；而在较高电流下，这种局限效应被打破，系统进入电场主导的损伤状态。总之，这些发现为柔性神经接口的ICMS设定了一个有机制依据的安全窗口，并确定了气泡辅助血管通透性增加是高电流下的关键失效模式，这对未来双向脑机接口和高精度神经假体方案的设计至关重要。

## Abstract
Intracortical microstimulation (ICMS) with ultraflexible neural electrodes enables low-threshold, chronically stable, and high-resolution modulation of neural circuits, providing a promising strategy for sensory restoration and closed-loop neuromodulation. However, the microscopic mechanisms delineating its safe and effective current range remain unclear. Here, we combine intravital two-photon (2P) imaging and electrophysiology in awake mice to examine the current-dependent neurovascular outcomes of charge-balanced stimulation via ultraflexible arrays. We observed gas bubbles formed along the electrode during ICMS, with bubble size increasing quadratically with current amplitude, consistent with a Faradaic bubble-growth model. Intravital 2P imaging reveals that at low-to-moderate currents (20-40 {micro}A), vascular leakage is small, spatially confined, and largely reversible, whereas higher currents ([&ge;]60 {micro}A) induce a sharp transition to extensive, field-dominated extravasation and secondary vessel disruption. This transition coincides with immediate, stimulus-locked motor responses and the onset of electrode degradation. Multiphysics simulations reproduce the observed nonlinear leakage-current relationship by incorporating gas bubble-induced electric field redistribution and voltage-dependent vessel wall permeability. The model indicates that gas bubbles act as local electric-field modulators, concentrating suprathreshold fields near the bubble boundary at lower currents while shielding more distant vessel segments; at higher currents, this confinement breaks down and the system enters a field-dominated damage regime. Collectively, these findings define a mechanistically informed safety window for ICMS with flexible neural interfaces and identify bubble-assisted vascular permeabilization as a key failure mode at high currents, crucial for the design of future bidirectional brain-computer interfaces and high-precision neuroprosthetic protocols.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：采用超柔性神经电极的皮层内微刺激（ICMS）能够实现低阈值、长期稳定且高分辨率的神经调控，在感觉重建和闭环神经假体中前景广阔。然而，如何界定刺激的安全电流范围、避免组织损伤，其微观机制尚不清楚。
- **核心问题**：厘清柔性电极上电荷平衡刺激所引起的神经血管效应与电流幅值之间的定量关系，并揭示控制损伤阈值的内在机制。
- **整体含义**：通过揭示气泡动力学介导的血管损伤模式，为双向脑机接口与高精度神经假体方案的设计提供具有机制依据的安全操作窗口。

## 2. 方法论

本研究构建了一个多模态、多尺度的分析框架，核心思想是“观察—建模—验证”，具体包含以下关键要素：

- **双光子活体成像与电生理同步记录**：在清醒小鼠中，利用活体双光子显微镜实时观测超柔性电极阵列周围血管结构、渗漏情况以及气泡形成过程，同时记录电生理信号。
- **气泡动力学分析**：依据法拉第气泡生长模型，建立气泡尺寸与刺激电流之间的定量关系：
  $$ r_{\text{bubble}} \propto I^2 $$
  即气泡尺寸随电流幅值呈二次方增长。
- **多物理场仿真**：构建包含电场、气泡以及血管壁通透性的有限元模型。模型纳入以下关键机制：
  - 气泡引起的局部电场重新分布；
  - 电压依赖性血管壁通透性（将跨壁电场强度与外渗程度挂钩）。
  仿真用于复现渗漏-电流间的非线性依赖关系，并检验气泡充当“电场调节器”的假说。

## 3. 实验设计

- **实验对象与场景**：以清醒小鼠为模型，在其皮层植入超柔性神经电极阵列，施加电荷平衡双相电流脉冲。
- **刺激参数条件**：系统性地改变电流幅值，典型组别包括低电流（20 μA）、中等电流（40 μA）及高电流（≥60 μA），以考察电流依赖性效应。
- **观测基准与对比方案**：
  - **微观血管损伤**：以血管荧光标记物的外渗范围、程度、可逆性作为损伤指标。
  - **宏观行为**：记录与刺激锁时的运动反应作为功能性损伤参考。
  - **电极状态**：评估电极退化程度。
  - **模型对照**：多物理场仿真结果与活体实测的渗漏-电流曲线进行对比，验证气泡调控电场假说的解释力。
  本研究未与其他电刺激模式或电极类型直接进行大量比较，属探索机制的自立型实验设计。

## 4. 资源与算力

- 原文及所提供的元数据中**未明确说明**使用的 GPU 型号、数量、训练时长等计算资源。多物理场仿真通常可在工作站或小型服务器上完成，不依赖大规模深度学习集群，因此未突出报道算力细节。

## 5. 实验数量与充分性

- **实验类型覆盖**：至少包括活体双光子成像实验、电生理记录、行为观察以及多物理场数值模拟四类实验/分析。
- **条件分组**：至少涵盖三个电流等级（低、中、高），并在部分条件下考察可逆性（刺激后恢复）和电极完整性，形成多维度损伤评估。
- **模型验证**：仿真不只是参数重现，而是通过包含气泡效应和电压依赖性通透性来复现非线性转折，内在构成一种“机制消融”验证。
- **充分性判断**：实验从微观细胞层面到整体行为、从现象描述到机制模拟，形成闭环证据链，具备较好的内部效度；但受限于动物数量、电流参数梯度、长期慢性观察等维度，客观性尚可，外部推广性需进一步验证。

## 6. 主要结论与发现

- **安全阈值界定**：低至中等电流（20–40 μA）下，气泡引发局部、可逆的血管渗漏；高电流（≥60 μA）则触发突变的、电场主导的大范围外渗、继发性血管破坏、即时运动反应和电极退化，由此明确了一个微刺激安全电流窗口。
- **气泡动力学作用**：气泡尺寸随电流平方增大，并充当局部电场调制器——低电流下将超阈值电场约束在气泡边界附近，屏蔽远处血管；高电流下这种限域效应崩溃，导致全场损伤。
- **失效模式识别**：气泡辅助的血管通透性升高被确立为高电流下的关键失效模式，为脑机接口安全性设计提供了直接干预靶点。

## 7. 优点

- **多模态融合**：将活体亚细胞成像、电生理、行为观察与多物理仿真有机结合，实现对同一现象的跨尺度解释，方法上具有创新性。
- **机制深度**：不止步于现象描述，而是通过法拉第气泡生长模型和电场重分布仿真，给出了非线性损伤转变的物理–生物耦合机制。
- **定量安全指导**：明确给出20–40 μA的安全电流区间，并定性指出气泡尺寸与电场限域–崩塌的转折点，对工程应用有直接参考价值。
- **清醒动物模型**：使用清醒小鼠避免麻醉对血管反应的干扰，提高了观测的生理相关性和转译可信度。

## 8. 不足与局限

- **实验覆盖范围**：
  - 仅在小鼠模型上验证，大脑尺寸、血管结构、电极间距等与人脑差异较大，推广到灵长类或人类应用需谨慎。
  - 刺激模式限于电荷平衡双相脉冲，频率、脉宽、脉冲间隔等参数的影响未展开。
  - 长期慢性刺激下组织反应、胶质疤痕形成对安全阈值的影响未被纳入。
- **偏差风险**：
  - 活体成像仅观测表层血管，皮层深部区域的气泡–血管交互可能不同。
  - 血管通透性的电压依赖性参数可能源自文献或简化的理论模型，存在不确定性。
  - 电极退化评价可能依赖间接指标，缺少系统的材料学表征。
- **应用限制**：安全阈值严格依赖于所用电极几何形状、材料、表面特性，直接迁移至其他神经界面需重新校准；气泡调控假说有待通过主动改变气泡行为（如超声）的实验进一步验证。

（完）
