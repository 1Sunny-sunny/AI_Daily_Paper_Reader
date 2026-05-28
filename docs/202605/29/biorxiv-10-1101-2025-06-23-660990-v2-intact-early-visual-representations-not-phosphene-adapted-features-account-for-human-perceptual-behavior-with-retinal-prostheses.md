---
title: "Intact early visual representations, not phosphene-adapted features, account for human perceptual behavior with retinal prostheses"
title_zh: 完整的早期视觉表征，而非适应光幻视的特征，决定了使用视网膜假体的人类感知行为
authors: "Skaza, J., Murlidaran, S., Varshney, A., Wen, Z., Eckstein, M. P., Beyeler, M."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.1101/2025.06.23.660990v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 视网膜假体脑机接口系统
tldr: 视网膜假体植入后患者感知难以预测，缺乏术前规划工具。本研究提出计算虚拟患者（CVP）流程，结合基于解剖的光幻视模拟与任务优化的深度神经网络，在多种任务和电极配置上预测感知能力。发现保留自然图像表征比适应光幻视特征更符合人类行为，且模型预测与患者实际表现及正常视力者心理物理数据吻合，为术前评估提供了可扩展框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 视网膜假体发展超前于感知预测能力，临床缺乏可靠的手术规划和设备选择工具。
method: 构建整合光幻视模拟与深度神经网络的计算虚拟患者（CVP）流程，在六种视觉任务、六种电极配置下评估，并比较冻结自然特征与微调光幻视特征的效果。
result: CVP预测与患者FLORA评估及正常视力者心理物理数据高度一致，且保留自然图像表征的策略更贴合人类感知行为。
conclusion: CVP可作为探索假体视觉的科学工具、设备开发引擎和术前预测框架，强调了早期视觉表征保留的重要性。
---

## 摘要
通过神经植入物恢复视觉的努力已经超越了预测使用者感知内容的能力，使患者和临床医生缺乏可靠的手术规划或设备选择工具。为弥合这一关键差距，我们引入了一个计算虚拟患者（CVP）流程，该流程将基于解剖学的光幻视模拟与任务优化的深度神经网络（DNNs）相结合，以预测患者在不同假体设计和任务中的感知能力。我们评估了六种视觉任务、六种电极配置和两种人工视觉模型的表现，确立了我们的CVP方法作为一种可扩展的植入前评估方法。所选任务中有几项与功能性低视力观察者评级评估（FLORA）一致，揭示了模型预测的难度与现实世界患者预后之间的对应关系。此外，CVP范式与从正常视力受试者观看光幻视模拟时收集的心理物理数据高度一致，既捕捉了总体任务难度，也反映了不同植入配置的性能变化。将冻结特征线性探测与完整端到端微调进行比较表明，保留自然图像表征——而不是使它们适应光幻视特定的统计特性——能更好地再现人类感知行为，这与成人视觉皮层有限的可塑性相一致。这些发现将CVP定位为探测假体视觉下感知的科学工具、指导设备开发的引擎以及用于术前预测的临床相关框架。

## Abstract
Efforts to restore vision via neural implants have outpaced the ability to predict what users will perceive, leaving patients and clinicians without reliable tools for surgical planning or device selection. To bridge this critical gap, we introduce a computational virtual patient (CVP) pipeline that integrates anatomically grounded phosphene simulation with task-optimized deep neural networks (DNNs) to forecast patient perceptual capabilities across diverse prosthetic designs and tasks. We evaluate performance across six visual tasks, six electrode configurations, and two artificial vision models, establishing our CVP approach as a scalable pre-implantation method. Several chosen tasks align with the Functional Low-Vision Observer Rated Assessment (FLORA), revealing correspondence between model-predicted difficulty and real-world patient outcomes. Further, the CVP paradigm exhibited strong correspondence with psychophysical data collected from normally sighted subjects viewing phosphene simulations, capturing both overall task difficulty and performance variation across implant configurations. Comparing frozen-feature linear probing with full end-to-end fine-tuning reveals that preserving natural-image representations--rather than adapting them to phosphene-specific statistics--better reproduces human perceptual behavior, consistent with the constrained plasticity of adult visual cortex. The findings position CVP as a scientific tool for probing perception under prosthetic vision, an engine to inform device development, and a clinically relevant framework for pre-surgical forecasting.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义
- **研究背景**：视网膜假体（如视网膜植入物）技术发展迅速，但临床中缺乏能预先预测患者植入后实际感知效果的工具，导致手术规划和设备选择缺乏客观依据。
- **核心问题**：如何构建一个计算框架，在术前就能准确预测不同假体设计和视觉任务下患者的感知能力，从而弥合技术能力与临床需求之间的差距。
- **整体含义**：提出“计算虚拟患者”（CVP）概念，不仅为假体视觉下的感知机制研究提供科学工具，也为设备开发迭代和临床术前评估建立可扩展的框架。

## 2. 方法论
- **核心思想**：将基于解剖学的光幻视模拟与任务优化的深度神经网络（DNN）相结合，构建能预测患者感知行为的虚拟患者。
- **关键技术流程（CVP 流程）**：
  - 利用基于解剖结构的光幻视模拟，生成特定电极配置下的人工视觉输入图像。
  - 使用深度神经网络对该模拟视觉输入进行任务优化训练或特征提取。
  - 通过在不同任务和配置上评估模型性能，映射出患者的潜在感知能力。
- **两种视觉表征策略对比**：
  - **冻结特征线性探测**：保留在自然图像上预训练的 DNN 特征，仅训练线性分类头。
  - **端到端微调**：使 DNN 整体适应光幻视特有的统计特性。
- **评估维度**：在六种视觉任务和六种电极配置下测试，并与实际患者数据和心理物理实验数据进行校准。

## 3. 实验设计
- **任务与数据集**：
  - 六种视觉任务，其中数项与功能性低视力观察者评级评估（FLORA）中的项目对齐，以建立与现实世界患者预后的联系。
  - 光幻视模拟输入涵盖六种不同的电极配置（即不同假体设计方案）。
- **基准与对比方法**：
  - **临床基准**：真实视网膜假体植入患者的 FLORA 评估结果。
  - **人类感知基准**：正常视力受试者观看相同光幻视模拟时的心理物理学行为数据。
  - **模型对比**：冻结自然特征线性探测 vs. 端到端光幻视特征微调，以确定哪种策略更符合人类行为。
- **评估目标**：检验 CVP 能否同时再现总体任务难度和不同植入配置间的性能变化。

## 4. 资源与算力
- 文中未明确提及所使用的 GPU 型号、数量、训练时长或算力规模。该信息从现有摘要和元数据中无法获取。

## 5. 实验数量与充分性
- **实验组数**：至少覆盖 6（任务）× 6（电极配置）× 2（表征策略）的组合，共计 72 种基础实验条件，外加与两组外部基准（患者 FLORA 数据、视力正常者心理物理数据）的对比验证。
- **充分性与客观性**：
  - 任务类型和配置维度较丰富，且选择了有临床对应物的评估项目，提高了生态效度。
  - 同时引入患者实际结局与人类受试者行为数据作为外部参考，形成了“模型-临床-行为”三角验证，实验设计客观且较为充分。
  - 对比策略（冻结 vs. 微调）直接回应了核心假说，避免了单一模型偏差。

## 6. 主要结论与发现
- **模型预测与人类行为高度一致**：CVP 预测的任务难度和配置间差异，与视网膜假体患者的 FLORA 评估结果、以及正常视力个体在光幻视模拟下的心理物理表现均显著吻合。
- **自然表征优于光幻视适应**：保留冻结的自然图像表征比经过端到端微调、适应光幻视特征的表征更能复现人类感知行为。
- **理论启示**：这一结果支持了成年视觉皮层可塑性有限的生物学观点，即遗传或发育形成的自然视觉表征在假体视觉下仍起主导作用。
- **框架定位**：CVP 可同时作为探索假体视觉感知的科学工具、指导假体设备开发的工程引擎，以及用于术前预测的临床相关框架。

## 7. 优点
- **解剖与学习的深度整合**：将解剖学指导的逼真光幻视模拟与任务优化 DNN 有机结合，提升了模拟的生理合理性与预测能力。
- **多维度、跨层次验证**：同时使用任务性能、临床结局（FLORA）和人类心理物理数据进行校准，证据链完整。
- **关键机制洞见**：通过冻结与微调的对比实验，明确揭示了自然表征保留的重要性，为假体编码策略和康复训练提供了理论指导。
- **可扩展性**：流程标准化，能够快速应用于新的电极设计、新任务或新模型，具备成为术前规划通用工具的可能性。

## 8. 不足与局限
- **模拟真实性的局限**：光幻视模拟虽基于解剖，仍可能与个体间真实的神经激活感受存在偏差，且未深入探讨感知质量、扭曲等主观维度。
- **任务和配置覆盖有限**：六种视觉任务和六种电极配置虽满足初步验证，但距离覆盖所有日常视觉需求和新型电极拓扑尚有距离，泛化性需进一步检验。
- **个体差异未建模**：现框架可能主要反映群体平均行为，尚未考虑患者间解剖结构、病程、神经可塑性等方面的异质性。
- **术前到术后的转化鸿沟**：预测结果与实际手术植入后患者的长期感知变化之间的对应关系，仍需前瞻性临床研究证实。
- **算力与部署细节缺失**：未提供所需计算资源的规模和训练效率数据，不利于评估其临床落地的硬件成本与可行性。
- **跨假体类型限制**：模型基于视网膜假体机制构建，推广到皮层假体等其他视觉植入物时可能需大幅调整。

（完）
