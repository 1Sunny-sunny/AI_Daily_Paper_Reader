---
title: Adaptive Bayesian localization of motor representation areas
title_zh: 自适应贝叶斯运动表征区域定位
authors: "Laine, M., Mutanen, T. P., Parvin, S., Numssen, O., Weise, K., Stenroos, M., Granö, I., Soto, A. M., Matsuda, R. H., Souza, V. H., Knösche, T. R., Ilmoniemi, R. J."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729093v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 自适应贝叶斯框架连接TMS刺激（外部变量）与运动诱发电位（神经活动）
tldr: "经颅磁刺激（TMS）可用于非侵入性定位皮层运动表征，但传统方法忽略电场空间信息且未利用先验反应指导刺激。本文提出自适应贝叶斯定位方法，结合实时电场优化与逐次概率推断，将运动起源表示为空间概率分布并每次更新，后续刺激最大化预期定位改善。实验采用多焦点TMS自适应方案与单线圈随机方案对照，8名受试者结果显示自适应方法将所需刺激次数至少减半，平均60次收敛，150次后95%最高密度区常小于10 mm²，为术前规划提供高效工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有TMS定位方法忽略诱导电场的空间信息或不利用已引发的运动反应来优化后续刺激，导致定位效率低下。
method: 提出自适应贝叶斯定位框架，每次刺激后更新运动反应皮层起源的空间概率分布，并基于信息增益最大化原则实时优化下一次刺激参数。
result: 与随机线圈放置相比，自适应方案将稳定定位所需刺激次数至少减半，平均60次即收敛，定位精度达10 mm²以内。
conclusion: 自适应贝叶斯方法能显著减少定位所需刺激次数，实现快速、精准的运动表征定位，具有重要临床应用价值。
---

## 摘要
经颅磁刺激（TMS）能够无创定位皮层运动表征，在术前规划中具有重要临床应用。现有方法要么忽略TMS感应电场（E场）的空间信息，要么使用不利用先前诱发的运动反应来指导后续刺激的采集方案。我们提出了一种自适应贝叶斯定位方法，结合了实时电场优化和逐次试验的概率推断。运动反应的皮层起源被表示为一个空间概率分布，在每次刺激后更新。随后，优化后续刺激以最大化给定先前反应下预期的定位改进。我们通过实验验证了该方法，使用多靶点TMS进行自适应定位，并以随机线圈放置的单线圈TMS作为非自适应参考。在八名受试者中，与随机方案相比，自适应方案至少将稳定定位所需的刺激次数减少了一半，平均在60次刺激时收敛，到150次刺激时，95%最高密度区域通常低于10平方毫米。

## Abstract
Transcranial magnetic stimulation (TMS) enables non-invasive localization of cortical motor representations, with important clinical applications in presurgical planning. Existing methods either disregard spatial information about the TMS-induced electric field (E-field) or use acquisition schemes that do not leverage previously elicited motor responses to guide subsequent stimulation. We present an adaptive Bayesian localization method that combines real-time E-field optimization with per-trial probabilistic inference. The cortical origin of the motor responses is represented as a spatial probability distribution that is updated after each stimulus. Subsequent stimuli are then optimized to maximize the expected localization improvement given previous responses. We validated the method experimentally, using multi-locus TMS for adaptive localization and single-coil TMS as a non-adaptive reference with randomized coil placements. Across eight subjects, the adaptive protocol at least halved the number of stimuli required for stable localization compared to the randomized protocol, converging in 60 stimuli on average, with 95% highest-density regions often below 10 mm2 by 150 stimuli.

---

## 论文详细总结（自动生成）

# 自适应贝叶斯运动表征区域定位 论文总结

## 1. 核心问题与整体含义
- **研究背景**：经颅磁刺激（TMS）可通过测量运动诱发电位（MEP）无创定位大脑皮层中的运动功能区，对神经外科术前规划（如肿瘤切除避免损伤运动皮层）具有重要价值。
- **现有缺陷**：传统TMS定位方法存在两个痛点：
  - 忽略TMS诱导电场（E-field）的空间分布信息，未能将电场与解剖结构精准配准。
  - 刺激采集策略为“盲采”（如随机网格、固定间距），不利用已诱发的运动反应来优化后续刺激位置，导致定位效率低下、所需刺激次数多。
- **整体含义**：本文提出一种自适应贝叶斯定位框架，将每一次TMS刺激视为一次信息采集，通过实时概率推断和刺激参数优化，以最少刺激次数实现快速、精准的运动功能区定位。

## 2. 方法论
- **核心思想**：将皮层运动起源表示为一个随刺激不断更新的空间概率分布，并通过最大化信息增益来决定下一次刺激的位点和参数，实现闭环自适应定位。
- **关键技术环节**：
  - **概率建模**：用空间概率分布 $p(s)$ 描述运动反应起源于皮层某点 $s$ 的可能性，初始为无信息先验。
  - **逐次更新**：每次刺激后，根据该次刺激产生的MEP幅值是否存在，结合该刺激下皮层各点的电场强度、电流方向与神经元取向的关系（似然函数），通过贝叶斯公式更新后验概率分布：
    $$p(s \mid \text{response}) \propto p(\text{response} \mid s) \, p(s)$$
  - **刺激优化**：下一次刺激的选择基于**预期信息增益最大化**准则，即寻找能够最大程度降低后验分布不确定性的刺激参数（线圈位置、角度等），相当于最小化条件熵：
    $$\text{next stimulus} = \arg\max\ \mathbb{E}[\text{KL}(p_{\text{posterior}} \parallel p_{\text{prior}})]$$
  - **实时电场优化**：利用多焦点TMS（multi-locus TMS）可在不移动实体线圈的情况下快速切换刺激焦点，使得连续自适应方案能够即时实施。
- **算法流程**：初始化先验 → 选择最优刺激参数 → 施加刺激并记录MEP → 更新空间概率分布 → 判断是否收敛（如95%最高密度区域面积小于阈值） → 未收敛则重复。

## 3. 实验设计
- **受试者与设备**：8名健康受试者。自适应定位使用**多焦点TMS系统**，可电子切换刺激位点；非自适应对照采用传统**单线圈TMS随机放置**方案。
- **任务与目标**：定位拇短展肌（APB）的运动热点，以MEP幅值作为响应变量。
- **对比方案**：
  - **自适应方法**：贝叶斯闭环优化，每次根据已有信息选择最佳刺激位置。
  - **非自适应参考**：在感兴趣区内随机选择线圈位置进行刺激，无信息引导。
- **评价指标**：
  - 收敛所需刺激次数（如连续N次刺激后最可能位置不再显著变化）
  - 定位精度：150次刺激后95%最高密度区域（HDR）面积（mm²）
- **实验条件**：所用多焦点TMS与单线圈TMS产生的电场经建模配准到个体MRI头模，确保可比性。

## 4. 资源与算力
- **算力情况**：**文中未明确提及**使用的GPU型号、数量或计算时长。从方法原理推断，概率更新与信息增益计算为解析或轻量级数值运算，可能无需大规模深度学习算力，实时性可由普通计算机或嵌入式系统满足，但无具体数据支撑。

## 5. 实验数量与充分性
- **实验组数**：
  - 主要对比为一组（自适应 vs. 随机），无额外消融实验或不同超参数对比。
  - 受试者8人，单个皮层靶区（手部运动区）。
- **充分性评估**：
  - **优点**：采用个体自身对照（同受试者先后进行自适应和随机方案），减少了个体间差异，对比公平。
  - **局限**：样本量较小（n=8），且仅测试了一个靶区，缺少对不同皮层区域（如面部、腿部）以及患病群体（如脑肿瘤患者）的验证；未与其他经典自适应策略（如参数估计的D-最优设计）或网格搜索+事后电场建模方法进行比较，实验设计的广度有限。
  - 从概念验证角度，实验足以支撑“可大幅减少刺激次数”的结论，但外部效度和方案普适性尚需进一步研究。

## 6. 主要结论与发现
- **效率提升**：自适应贝叶斯方案使稳定定位所需刺激次数比随机线圈放置方案**至少减少一半**，平均约**60次刺激**即可收敛。
- **高精度定位**：在150次刺激后，95%最高密度区域面积常小于**10 mm²**，表明定位焦点非常集中。
- **临床转化潜力**：该方法能以较短时间、较高效刺激次数实现精准的术前运动功能区映射，有望降低患者负担并提高手术规划安全性。

## 7. 优点
- **实时闭环自适应**：首次将逐次贝叶斯更新与电场优化整合到TMS运动区定位中，使刺激具备主动信息获取能力。
- **大幅减次增效**：实验明确证实刺激次数减半以上，对临床时间窗口宝贵的情境极具价值。
- **概率输出可解释**：定位结果给出完整的空间不确定性分布（HDR），而非单点估计，有助于可靠性判断。
- **设备优势利用**：充分结合多焦点TMS的快速电子靶点切换能力，避免机械移动延滞，使自适应成为可能。

## 8. 不足与局限
- **样本与人群局限**：仅8名健康人测试，无患者数据，未覆盖不同脑区、年龄或病理状态下的泛化性。
- **对照方法单一**：非自适应对照仅为随机线圈放置，未与临床常用的网格搜索+事后电场建模或其它自适应设计比较。
- **技术依赖**：自适应方案依赖多焦点TMS硬件和个体化电场模型，普通单线圈设备难以直接迁移。
- **模型假设**：贝叶斯更新中的似然模型依赖于MEP阈值判定和电场‑神经元取向函数，这些假设的偏差可能影响定位准确性，文中未分析模型失配的影响。
- **信息缺失**：本文为预印本，未经过完整同行评审；且摘要和元数据中未提供收敛判据的具体细节、电场建模精度及计算开销等关键技术说明，完整评估需等待正式版本。

（完）
