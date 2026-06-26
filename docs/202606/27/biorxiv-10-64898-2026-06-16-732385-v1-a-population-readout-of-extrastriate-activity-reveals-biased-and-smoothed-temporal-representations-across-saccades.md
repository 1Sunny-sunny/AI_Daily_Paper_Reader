---
title: A population readout of extrastriate activity reveals biased and smoothed temporal representations across saccades
title_zh: 纹外观皮层群体活动的读出揭示跨眼跳偏倚且平滑的时间表征
authors: "Poursadegh, A., Zekri, M., Weng, G., Akbarian Aghdam, A., Clark, K., Rabbani, H., Noudoost, B., Nategh, N."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.16.732385v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 纹外皮层时间表征的群体读出
tldr: 扫视期间视觉时间感知暂扭曲，机制未知。本研究用猕猴纹外皮层V4/MT群体电生理记录、高时空刺激和单试次建模，发现神经元偏置前扫视刺激的时间表征，降低时间敏感性；建模揭示该偏置因果导致敏感性下降，表明皮层通过偏好新近可靠输入平衡时间精度与鲁棒性，支持扫视间连续视觉感知。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究扫视期间纹外皮层如何编码和读出时间信息。
method: 结合猕猴V4/MT神经元群体电生理记录、高时空分辨率视觉刺激和单试次精度统计建模。
result: 神经元反应使前扫视刺激时间表征向前偏移并降低时间敏感性，建模显示表征偏置是敏感性降低的因果因素。
conclusion: 纹外皮层通过主动编码策略偏好新近可靠输入，实现时间精度与鲁棒性的权衡，维持跨扫视的连续视觉感知。
---

## 摘要
视觉时间的知觉在眼跳前后短暂失真，然而构建眼跳前后时间表征的神经元机制尚不清楚。在此，我们通过结合猕猴V4和MT区神经元群体的电生理记录（采用高时空分辨率视觉刺激）与统计建模框架（在单试次精度上捕获眼跳前后反应调制），探究了眼跳前后时间信息如何在纹外观皮层中编码和读出。我们的分析表明，眼跳前后神经元反应系统性地改变了感受野内对眼跳前刺激的时间表征——使其偏向更早的时间，并降低了对眼跳前刺激的时间敏感性——损害了对刺激出现时间的辨别能力。利用神经元群体中时变时空敏感性图进行的基于模型的读出，能够定量表征这些效应，并在毫秒级分辨率下识别出特定的神经元反应成分。计算机模拟操作进一步证明了表征偏差在降低时间敏感性中的因果作用。这些发现表明，纹外观皮层实施了一种主动编码策略，通过优先选择最近可靠的输入来稳定眼跳前的时间信息，揭示了时间精度与稳健性之间的基本权衡，这种权衡支持了跨眼跳的连续视觉感知。该发现也确立了纹外观皮层群体在构建视觉时间感知中的一般性作用。

## Abstract
Perception of visual time is transiently distorted around saccadic eye movements, yet the neuronal mechanisms constructing perisaccadic representations of time remain unclear. Here, we investigate how perisaccadic temporal information is encoded and read out in extrastriate cortex, by combining electrophysiological recordings in V4 and MT neuronal population in macaque monkeys under high spatiotemporal resolution visual stimulation, and a statistical modeling framework capturing perisaccadic response modulations at single-trial precision. Our analyses show that perisaccadic neuronal responses systematically shift the temporal representation of presaccadic stimuli within receptive fields-biasing them toward earlier times, and also reduce temporal sensitivity for presaccadic stimuli-impairing discrimination of stimulus onset times. Model-based readout using time-varying spatiotemporal sensitivity maps in neuronal ensembles enables quantitative characterization of these effects and identifies their specific neuronal response components at millisecond resolution. In silico manipulations further demonstrate a causal role of representational bias in reducing temporal sensitivity. These findings suggest that extrastriate cortex implements an active encoding strategy to stabilize presaccadic temporal information by favoring the most recent reliable input, revealing a fundamental tradeoff between temporal precision and robustness that supports a continuous visual percept across saccades. This finding also establishes a general role for extrastriate populations in constructing the perception of visual time.

---

## 论文详细总结（自动生成）

### 1. 论文核心问题与整体含义
- **研究背景与动机**：眼跳（saccade）期间，视觉时间知觉会出现瞬时失真（如时间压缩、时序倒置、停表错觉）。但纹外观皮层（如V4、MT）如何在神经元群体层面编码和读出眼跳前后的时间信息，其机制尚不明确。
- **核心问题**：眼跳前后纹外皮层的时间表征发生了怎样的系统性变化？这些神经变化能否解释行为上的时间知觉扭曲？
- **整体含义**：揭示大脑如何主动调整时间编码策略，在时间精度（灵敏性）与感知稳健性（连续性）之间进行权衡，从而跨眼跳维持稳定的视觉体验。

### 2. 方法论
- **核心思想**：利用高时空分辨率的白噪声视觉探针，结合时变广义线性模型（SVGLM）对单神经元反应进行精密建模，并通过群体核矩阵的读出分析，量化眼跳前后时间表征的偏差和灵敏性变化。
- **关键技术细节与流程**：
  - **刺激与记录**：在视觉引导眼跳任务中，于9×9网格内随机快速闪现7ms白色方块探针，同时记录猕猴V4、MT区神经元锋电位。
  - **编码模型（SVGLM）**：将神经反应建模为泊松过程，其条件强度函数为：
    $$ \lambda^{(l)}(t) = f\left( \eta^{(l)}(t) \right) $$
    线性预测器 $\eta^{(l)}(t)$ 包含：
    $$ \eta^{(l)}(t) = \sum_{x,y,\tau} k_{x,y}(t,\tau) s^{(l)}_{x,y}(t-\tau) + \sum_{\tau} h(\tau) r^{(l)}(t-\tau) + b(t) + b_0 $$
    其中 $k_{x,y}(t,\tau)$ 是时变时空敏感性核（stimulus kernels），$t$ 为相对眼跳时间，$\tau$ 为相对刺激延迟。通过稀疏化选择显著时空单元（STU），用最大惩罚似然估计参数，得到毫秒级时变核。
  - **时间敏感性分析**：在群体水平上，计算各个延迟下的群体核矩阵之间的相关性，对相关值曲线拟合S形函数，以真延迟与拐点延迟之差作为“时间差”指标（时间差越大敏感性越低）。
  - **时间偏差分析**：计算每个眼跳时刻的群体核与注视期核在延迟维度的相关性图，然后在300ms滑动窗中，用图间相关作为权重对各时刻加权求和，得到“感知时间”对“真实时间”的映射，以此量化时间偏差。
  - **因果操控（in silico）**：识别出“偏差相关STU”和“噪声相关STU”，分别用注视期权重替换，重新计算模型预测的反应，并再次评估时间敏感性与偏差，从而推断因果关系。

### 3. 实验设计
- **数据集/场景**：4只成年雄性猕猴，执行视觉引导眼跳任务。探针覆盖注视点、眼跳目标和感受野的9×9网格位置，7ms持续时间。共108个记录session，获得300个MT神经元和147个V4神经元。
- **分组与分析单元**：将感受野、眼跳目标、探针网格配置相似的神经元组成15个集合（6个V4，9个MT），每个集合至少10个神经元。
- **对比方法与基准**：
  - **模型对比**：全模型 vs 去除偏差相关STU的模型 vs 去除噪声相关STU的模型。
  - **数据来源对比**：模型预测的核分析与直接基于神经锋电位响应的分析相互印证（如Fig.2/3, Fig.4/5）。
  - **统计基准**：以注视期窗口（如 -500:-300 ms 或 -700:-400 ms）作为基线，校正和统计比较。

### 4. 资源与算力
- **算力说明**：文章未提及所使用的GPU型号、数量或训练时长等算力细节。
- **技术推断**：分析主要涉及电生理数据处理、SVGLM最大似然估计和基于相关性的读出计算，属于统计优化范畴，可能不需要大规模GPU集群。文中未作明确说明，此处为信息缺失。

### 5. 实验数量与充分性
- **实验规模**：
  - 4只猴子、300 MT/147 V4神经元、15个ensemble。
  - 主分析包含时间敏感性图（归一化平均）、时间偏差曲线（平均±SEM）。
  - 关键消融实验：识别并移除偏差相关STU、噪声相关STU各一次，并分别在模型核水平和模型预测发放水平重新度量效应。
  - 两种数据源（核与发放）均进行了相同分析。
- **充分性与客观性**：实验组数虽不算庞大，但通过ensemble层面分析增加统计效力。消融实验设计针对两种对立假说（偏差驱动 vs 噪声驱动），结果对比清晰，支持主要结论。采用基于单试次的统计模型和严格的统计检验（Wilcoxon签名秩检验），客观性较好。

### 6. 主要结论与发现
- **时间表征向前偏倚**：眼跳前（约-50:50 ms窗口），神经群的时间表征被系统性地映射到更早的时间点，平均偏倚约-18.54 ms（模型）和-17.3 ms（发放数据）。
- **时间敏感性下降**：眼跳前约-45:0 ms窗口，时间差指标显著升高，表明区分刺激出现时刻的能力降低。
- **因果机制**：时间敏感性下降由表征偏倚导致，而非神经反应变异性（噪声）增加。移除偏差相关STU可同时消除时间偏倚和敏感性下降；移除噪声相关STU则无此效果。
- **功能意义**：纹外皮层采用主动编码策略，将眼跳前刺激的表征平滑并移向最近稳定时刻，牺牲时间精度以换取跨眼跳感知的连续性与稳健性。

### 7. 优点
- **高时空精度**：7ms探针与毫秒级时变核，精细刻画了眼跳前后敏感性的快速动态。
- **群体层面读出**：利用ensemble核矩阵捕获群体表征特性，超越单神经元分析。
- **因果验证**：通过in silico识别和操控特定STU，明确区分了偏差与噪声的贡献，提供了因果性证据。
- **模型-数据双重验证**：将模型分析结果与直接神经反应分析进行平行比较，结果高度一致，增强了结论可靠性。
- **明确的计算框架**：SVGLM提供了可解释的神经处理成分（时空核），便于分离不同的调制效应。

### 8. 不足与局限
- **缺乏直接行为测量**：研究中定义的时间偏倚和敏感度下降基于神经群体读出，并未与猴子实际的行为时间知觉（如等时判断）直接关联，仅作了机制推断。
- **注意力干扰不能完全排除**：眼跳前注意资源向眼跳目标转移，可能部分影响感受野区域的加工，但文章未直接控制或量化注意对时间表征的独立贡献。
- **脑区与刺激范式局限**：仅涵盖V4与MT区，未探讨额叶眼动区（FEF）等可能与时间压缩/眼跳计划相关的上游结构；白噪声闪块刺激生态效度有限，可能与自然场景的时间加工不同。
- **因果操控的局限性**：in silico操控依赖模型假设，是对真实神经回路的简化，且替换为注视期核是一种静态干预，未考虑动态补偿机制。

（完）
