---
title: Conjunctive coding of letter pairs emerges in segregated human medial temporal lobe neurons during working memory
title_zh: 工作记忆期间人类内侧颞叶分离神经元中字母对联合编码的出现
authors: "Felez Martinez, E., Costa, F., Ledergerber, D., Imbach, L., Sarnthein, J., Proix, T."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.729179v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 单神经元记录揭示字母对的连接编码
tldr: 工作记忆中组合表征的神经机制存在争论：是混合选择性还是专门的联合编码？本研究从11名癫痫患者内侧颞叶记录996个单神经元，执行字母串任务，发现字母对由稀疏的、不响应单个字母的神经元编码，表明存在分离的神经元群体专门组合项目，为联合编码假说提供了单神经元水平的直接神经生理支持。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究工作记忆中组合表征的神经编码是依赖混合选择性还是专门的联合编码神经元。
method: 记录癫痫患者内侧颞叶单神经元活动，执行字母串工作记忆任务。
result: 字母对编码出现在稀疏的、不对组成字母反应的神经元群中。
conclusion: 人类内侧颞叶通过分离的神经元独立编码组合信息，支持联合编码假说。
---

## 摘要
将个体记忆痕迹组合成统一表征是结构关系编码和灵活认知的基础。神经科学中一个核心争论涉及这些组合的神经机制：这些组合是通过混合选择性（同一神经元同时表征个体和组合项目）编码，还是通过一个独特且特化的神经元群体内的联合编码？本研究通过记录11名癫痫患者在字母串工作记忆任务中的996个内侧颞叶单个单元，检验了这些竞争性假设。我们发现，在任务相关时期，单个字母和字母对均存在神经编码，后者在维持阶段达到峰值。关键的是，字母对由一个稀疏的神经元子集编码，这些神经元对其组成字母未显示出显著的选择性。这表明存在一个被招募来组合项目的分离神经元群体，独立于单字母的神经编码。这些发现提供证据表明，人类内侧颞叶在分离的神经元中分别编码组合，在单神经元水平上为联合编码提供了直接的神经生理学支持。

## Abstract
Composing individual memory traces into unified representations is fundamental to encoding of structured relationships and flexible cognition. A central debate in neuroscience concerns the neural mechanisms of these compositions: are these compositions encoded through mixed selectivity, where the same neurons simultaneously represent individual and composed items, or through conjunctive coding within a distinct and specialized neuronal population? Here, we tested these competing hypotheses by recording 996 single units from the medial temporal lobe of 11 epilepsy patients performing a letter-string working memory task. We found neural encoding of both single letters and letter pairs during task related periods, with the latter peaking during the maintenance phase. Crucially, letter pairs were encoded by a sparse subset of neurons that did not show significant selectivity for their constituent letters. This suggests the existence of a segregated population of neurons recruited to compose items independently of single letter neural encoding. These findings provide evidence that the human medial temporal lobe separately encodes compositions within segregated neurons, offering direct neurophysiological support for conjunctive coding at the single-neuron level.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：大脑如何将离散的符号元素（如字母）组合成统一的结构化表征，是灵活认知（如推理、语言、记忆）的基础。神经科学的核心争论在于，这种组合是通过**混合选择性**（H2：同一神经元同时编码单个项目和组合），还是通过**联合编码**（H1：分离的神经元群体专门编码组合）实现。  
- **整体含义**：论文旨在利用人类内侧颞叶（MTL）单神经元记录，直接检验上述竞争性假说。理解这一机制有助于阐明大脑实施“思想语言”（Language of Thought）的神经计算原理，为记忆与高级认知提供神经基础。

### 2. 论文提出的方法论
- **核心思想**：采用**点过程广义线性模型（PPGLM）** 量化和分离神经元对单个字母及字母对的响应，通过**信息论指标BPS**（每尖峰比特数）评估编码强度，并利用统计检验区分假说。  
- **关键技术细节**（均用文字说明）：
  - **单字母分析**：对每个神经元、字母和任务阶段，比较空模型（仅含混杂因素：任务阶段、试次集大小、放电历史）和全模型（额外添加字母身份二元回归元$L_p$）。模型预测力的增益以BPS衡量，公式为  
    $$BP S_{n,L,p} = \frac{\log\text{Likelihood}(\text{Full Model}) - \log\text{Likelihood}(\text{Null Model})}{\log 2 \cdot n_{\text{spikes}}}$$  
    值越高表示字母身份带来的预测改进越大。
  - **字母对分析**：空模型包含两个组成字母的身份，全模型新增二者的交互项，从而剥离组合效应（即BPS的增益反映字母对的特异信息，而非单字母的简单叠加）。
  - **显著性检验与假说对立**：  
    - 对单字母或字母对模型，通过**置换检验**（重复200次打乱标签）生成BPS零分布，经FDR校正（$\alpha=0.05$）判定显著性。  
    - 为识别**维持特异性联合编码神经元**，将每个神经元在维持期的最大字母对BPS回归到固定期（基线）的BPS上，选取残差超过2倍标准差的神经元（共14个）。  
    - 假说检验：若这些字母对编码神经元对组成字母无显著选择性，则支持H1（联合编码）；反之支持H2（混合编码）。

### 3. 实验设计
- **数据集与场景**：  
  - 11名药物难治性癫痫患者，因临床需要植入深部电极至MTL（海马、杏仁核、内嗅皮层），共分离出996个**单神经元**（海马559、杏仁核239、内嗅皮层198）。  
  - 行为范式：**改良的Sternberg工作记忆任务**。每个试次包含固定（1 s）、编码（2 s，同时呈现4/6/8个辅音字母字符串）、维持（3 s，字母消失，被试默念复述）、检索（最大2 s，判断探针是否在之前字符串中）阶段，共15个辅音字母。
- **基准与对比**：  
  - 行为基准：正确率约92%，反应时间随集大小线性增加（63 ms/项），证实任务执行有效。  
  - 神经编码对比：  
    - 纵向对比：比较各任务阶段的BPS，以固定期为噪音基线。  
    - 假说对比：检验**H1（联合编码）** 与**H2（混合编码）**，通过同一神经元的单字母与字母对编码模式直接判定。  
    - 对照分析：重复回归分析并打乱标签以评估虚报概率；筛选最大单字母编码神经元，观察其是否出现字母对编码。

### 4. 资源与算力
- **文中未明确说明**使用任何GPU型号、数量或训练时长。研究本质为离线神经数据分析，基于Julia的`GLM.jl`库对每个神经元拟合线性模型，计算量适中，但不涉及大规模深度学习训练，故无法提供传统意义上的算力信息。

### 5. 实验数量与充分性
- **主要实验组**：  
  1. 单字母编码分析：996个神经元 × 15个字母 × 4个任务阶段，共数万次模型拟合，并伴随200次置换检验。  
  2. 字母对编码分析：同上，但针对字母对组合（如C(15,2)=105对），生成最大BPS矩阵。  
  3. 维持特异性神经元分离：回归分析筛选14个神经元，并辅以1000次打乱标签的对照。  
  4. 假说检验：追踪14个神经元的组成字母BPS，并与随机挑选的最大单字母编码神经元对比。  
- **充分性与公平性**：  
  - 实验设计层次分明，从全局编码模式逐步聚焦到特异神经元亚群，统计检验严格（多重比较校正、置换检验、回归去基线）。  
  - 然而，维持特异性联合编码神经元数量极少（14/996），可能不够充分以进行亚区（如海马前后部）统计；且患者群体的临床异质性引入潜在偏差。总体而言，实验序列足以支撑假说检验，但结论的普适性受限于样本量。

### 6. 论文的主要结论与发现
- **单字母编码**在任务相关期（编码、维持、检索）显著增强，具有阶段特异性，维持期信息量最高。  
- **字母对编码**在**维持期**达到峰值，且编码模式与基线期负相关，表明其随任务动态涌现，而非静态噪音。  
- **关键发现**：维持期字母对编码由**稀疏、分离的神经元子集**驱动（14个细胞）。这些神经元对组成字母几乎无选择性，统计上符合**H1联合编码假说**，即MTL内存在专门组合项目的神经元群体，独立于单字母表征。  
- 对照实验证实，强单字母选择性神经元不自动产生字母对编码，排除混合编码主因。

### 7. 优点
- **直接证据**：采用人类单神经元活动，提供迄今最直接的联合编码神经生理证据。  
- **方法严谨**：  
  - 使用PPGLM剥离单项目与组合效应，BPS提供无偏的信息论度量。  
  - 回归去基线策略有效分离维持期特异性信号，减少自发活动混淆。  
  - 多重对照分析排除替代解释（如标签打乱、反向回归、最大单字母神经元对照）。  
- **任务设计巧妙**：控制外显刺激、记忆负荷和阶段分离，突显内部维持期的组合表征。

### 8. 不足与局限
- **样本局限性**：  
  - 数据来自**癫痫患者**，可能受病理放电（如发作间期棘波）或药物影响，不一定完全代表健康大脑。  
  - 电极植入由临床需求决定，采样区域和神经元数量（尤其维持编码细胞仅14个）存在**偏差**，统计效力不足，并可能遗漏真正的H2神经元。  
- **实验范式**：  
  - 刺激集限于**辅音字母**，且任务为言语工作记忆，未验证非言语、更抽象或更高阶组合（如多字母序列）的泛化性。  
  - 模型**未考虑字母位置**顺序，错失了顺序编码的潜在维度。  
- **资源未报**：未提供计算资源细节，复现分析环境不透明。

（完）
