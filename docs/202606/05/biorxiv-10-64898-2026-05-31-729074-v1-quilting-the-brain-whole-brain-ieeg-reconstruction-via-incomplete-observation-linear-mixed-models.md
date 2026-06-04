---
title: "Quilting the Brain: Whole-Brain iEEG Reconstruction via Incomplete Observation Linear Mixed Models"
title_zh: 拼缀大脑：基于不完全观测线性混合模型的全脑iEEG重建
authors: "Wang, Y., Li, M., Bringas Vega, M. L., Valdes-Sosa, P. A."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.31.729074v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 全脑iEEG重建的统计框架
tldr: 颅内脑电图（iEEG）受限于碎片化观测，无法获得全脑连续活动。本研究提出不完全观测线性混合效应模型（IOLMM），结合Sure Independence Screening筛选真实信号和分层混合效应解耦个体差异，将稀疏iEEG记录拼接为全脑皮层源活动图。在106名患者数据上，重建了睡眠各期功率分布，揭示了NREM慢波的额叶优势，构建了首个基于iEEG的皮层电生理规范图谱，为癫痫病灶检测提供定量参考。
source: biorxiv
selection_source: fresh_fetch
motivation: iEEG临床植入导致观测碎片化，难以实现全脑水平的功能整合和组分析。
method: 提出IOLMM框架，整合Sure Independence Screening识别生理信号和层次线性混合模型解耦固定与随机效应。
result: 成功恢复睡眠分期依赖的全脑皮层源功率，再现NREM慢波额叶主导和电生理层级。
conclusion: 建立首个来自iEEG的皮层表面电生理规范图谱，桥接微观电生理与宏观系统神经科学，助力癫痫病灶定量预测。
---

## 摘要
高时空分辨率地绘制人脑功能受限于非侵入成像的物理局限和侵入性电生理的稀疏采样。虽然颅内脑电图（iEEG）能以毫米精度捕捉局部场电位，但临床植入策略导致了“覆盖悖论”：观测仅限于不相连的、患者特异性的小片区域，大部分皮层未被观测。本研究引入不完全观测线性混合效应模型（IOLMM），通过将碎片化观测“拼缀”成连续的全脑源活动图，解决了这一悖论。我们的方法整合了两项创新：（1）从超高维统计改编而来的确定性独立筛选（SIS），用于区分真实生理信号与容积传导的“幽灵源”；（2）分层IOLMM，将组水平生理固定效应与受试者特异性仪器随机效应解耦，解决了困扰iEEG组分析的尺度模糊性。在MNI开放iEEG图谱上的应用，通过清醒、N2、N3和快速眼动睡眠状态下依赖睡眠阶段的皮层源功率重建，验证了该框架，从106名患者的碎片化记录中恢复了非快速眼动慢波活动的额叶优势和层级化电生理等级。本工作建立了首个源自iEEG的皮层表面水平规范性电生理图谱，为检测和预测致痫病变提供了定量参考，弥合了电生理学微观精度与系统神经科学宏观视野之间的鸿沟。

## Abstract
Mapping human brain function at high spatiotemporal resolution is constrained by the physical limitations of non-invasive imaging and the sparse sampling of invasive electrophysiology. While intracranial electroencephalography (iEEG) captures local field potentials with millimeter precision, clinical implantation strategies result in a ``coverage paradox'': observations are restricted to disjoint, patient-specific patches, leaving most of the cortex unobserved. This study introduces the Incomplete Observation Linear Mixed-Effect Model (IOLMM), a statistical framework that resolves this paradox by ``quilting'' fragmented observations into continuous, whole-brain source activity maps. Our approach integrates two innovations: (1) Sure Independence Screening (SIS) adapted from ultra-high-dimensional statistics to distinguish true physiological signals from volume-conducted ``ghost sources''; (2) a hierarchical IOLMM that decouples group-level physiological fixed effects from subject-specific instrumental random effects, solving the scaling ambiguities that plague iEEG group analyses. Applied to the MNI Open iEEG Atlas, the framework is validated through sleep stage-dependent cortical source power reconstruction across Wake, N2, N3, and REM states, recovering the frontal predominance of NREM slow-wave activity and the graded electrophysiological hierarchy from fragmented recordings of 106 patients. This work establishes the first cortical surface-level normative electrophysiological atlas derived from iEEG, providing a quantitative reference for detecting and predicting epileptogenic lesions and bridging the gap between the microscopic precision of electrophysiology and the macroscopic scope of systems neuroscience.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：人脑功能的高时空分辨率成像面临两难：非侵入技术（如 fMRI、脑电图）空间或时间分辨率有限，而侵入性颅内脑电图（iEEG）虽能以毫米精度捕捉局部场电位，但其临床植入策略造成“覆盖悖论”——电极仅覆盖少量不连续的患者特异性皮层区域，大脑绝大部分皮层未被观测。
- **核心问题**：如何将来自多位患者的碎片化、异质的稀疏 iEEG 记录整合为连续的全脑皮层源活动图像，以实现组水平的统计推断和定量比较。
- **整体意义**：该工作旨在弥合电生理微观精度与系统神经科学宏观尺度之间的鸿沟，建立首个基于 iEEG 的皮层表面电生理规范图谱，为癫痫等脑疾病的病灶检测与预测提供定量参考。

## 2. 论文提出的方法论

- **框架名称**：不完全观测线性混合效应模型（IOLMM）。
- **核心思想**：将 iEEG 的碎片化观测视作从全脑源空间中抽取的不完全样本，通过解耦生理信号与仪器／个体效应，实现全脑源活动的“拼缀”重建。
- **关键技术细节**：
    - **确定性独立筛选（SIS）**：从超高维统计中引入，用于识别真实生理信号并剔除因容积传导而产生的“幽灵源”（虚源），克服源重构中的模糊性。
    - **分层线性混合效应模型**：将组水平的生理固定效应（如睡眠阶段相关的功率地形）与受试者特异性的仪器随机效应（个体基线、电极灵敏度差异）解耦，解决传统 iEEG 组分析中的尺度混淆问题。
    - **整体流程**：先通过 SIS 筛选出可靠源，再利用分层 IOLMM 估计固定效应系数，从而在每个皮层顶点上获得群体规范值及置信区间，最终生成连续的全脑源活动图（如跨睡眠状态的功率分布）。

## 3. 实验设计

- **使用数据集**：MNI 开放 iEEG 图谱（MNI Open iEEG Atlas），包含 106 名患者的临床 iEEG 记录。
- **实验场景／验证任务**：在不同警觉状态（清醒、N2、N3、快速眼动睡眠）下，重建全脑皮层源功率分布。
- **验证基准**：以已知的神经生理知识作为“金标准”——例如，非快速眼动（NREM）睡眠期慢波活动的额叶优势、皮层电生理层级（由感觉皮层到高级联合皮层的渐变）。
- **对比方法**：摘要中未提及与特定基线方法（如简单组平均、传统源成像）的量化比较，主要通过恢复经典电生理空间模式来验证框架的合理性。

## 4. 资源与算力

- **文中未明确说明**：提供的论文内容中，没有提及 GPU 型号、数量、训练时长或任何计算基础设施的具体信息。因仅见摘要与元数据，无法确认正文是否包含此类细节；就现有信息而言，资源与算力需求未知。

## 5. 实验数量与充分性

- **实验数量**：基于现有描述，主要展示了一类验证实验——在 4 种睡眠状态下进行全脑源功率重建，并观察结果是否与已知电生理规律一致。未提及消融实验（如移除 SIS 或分层效应的影响）、不同参数敏感性分析、跨数据集泛化测试或与其它重建方法的定量比较。
- **充分性与客观性**：实验能够证明 IOLMM 可以恢复预期的宏观地形图，验证了概念可行性。但缺乏消融研究、定量基准对比及统计显著性检验的报告，因此难以全面评估各组件贡献，实验的充分性和客观性在已知信息范围内较为有限。

## 6. 论文的主要结论与发现

- 成功将 106 名患者的碎片化 iEEG 记录“拼缀”为连续的全脑皮层源活动图。
- 从恢复的睡眠期功率地形中再现了已知的生理规律：NREM 慢波活动的额叶占优，以及从初级感觉皮层到高级联合皮层的层级化电生理梯度。
- 建立了首个来自 iEEG 的皮层表面电生理规范图谱，可作为定量参考用于检测和预测致痫病灶。

## 7. 优点

- **创新的统计框架**：将超高维变量筛选（SIS）与分层混合效应模型巧妙结合，系统性地解决了 iEEG 组分析中的容积传导假象和个体差异混淆两大难题。
- **临床与科学价值**：首次从稀缺的临床数据中构建出全脑尺度的电生理规范参考，为个性化病灶定位和大脑功能组织的研究提供新工具。
- **概念优雅**：用“拼缀”的比喻直观体现了将不相连的观察拼接为连续全脑图谱的核心思想，框架具有推广到其他模态和认知状态的潜力。

## 8. 不足与局限

- **实验验证有限**：仅以内源性睡眠状态作为验证场景，未在任务态、刺激诱发活动或独立临床预测任务中检验图谱的准确性与泛化能力。
- **缺乏定量比较**：未见到与现有 iEEG 组分析方法（如基于体积的插值、单变量元分析）或非侵入源成像技术的系统对比，难以评估改进幅度。
- **假设与偏差风险**：线性混合效应模型依赖线性假设；SIS 的筛选效能可能受信噪比影响；数据仅源自癫痫患者植入点，可能存在取样偏倚，规范图谱对健康大脑的代表性存疑。
- **未报告计算成本与可复现细节**：缺失算法复杂度、软件实现、算力需求等信息，限制了他人的复现与大规模应用评估。

（完）
