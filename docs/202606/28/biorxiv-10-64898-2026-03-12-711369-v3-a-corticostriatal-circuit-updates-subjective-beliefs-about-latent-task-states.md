---
title: A corticostriatal circuit updates subjective beliefs about latent task states
title_zh: 皮质纹状体回路更新关于潜在任务状态的主观信念
authors: "DeMaegd, M. L., Hocker, D., Gurnani, H., Adler-Wachter, M., Schindler, J., Schiereck, S. S., Savin, C., Constantinople, C. M."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.12.711369v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 记录并解码皮层纹状体环路中的信念神经表征
tldr: 信念影响决策与学习，但其神经回路机制尚不清楚。本研究在大鼠隐藏奖励状态任务中，记录并扰动眶额皮层（OFC）到中间/吻侧尾壳核（CPi/CPr）的特异性投射，发现OFC-CPi神经元编码高奖励状态的类别证据并呈饱和非线性；刺激该回路使信念偏向高奖励，扰动干扰隐藏状态编码，揭示了更新主观信念的皮质-纹状体回路。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索大脑如何表示和更新关于环境隐藏状态的主观信念。
method: 记录和扰动大鼠眶额皮层至尾壳核的特异性投射，结合隐藏奖励状态任务。
result: 刺激OFC-CPi神经元偏向高奖励信念，记录显示编码类别证据且具饱和非线性，可解码完整信念，扰动破坏状态编码。
conclusion: OFC-CPi回路是实现更新抽象环境状态主观信念的核心神经机制。
---

## 摘要
关于世界状态的信念深刻影响决策和学习，但人们对神经回路如何表征和更新信念知之甚少。我们对大鼠在执行具有隐藏奖励状态的任务时，从眶额皮层（OFC）投射到中间或前部尾状壳核（CPi/CPr）的神经元进行了投射特异性的记录和扰动。刺激OFC-CPi神经元使大鼠的信念偏向高奖励状态。对光遗传学标记的OFC-CPi神经元的记录显示，它们编码了高奖励状态的分类证据，这受到神经反应中饱和非线性的影响。下游神经元原则上可以解码大鼠在决策考虑期间关于奖励状态的完整信念分布。最后，投射特异性的扰动破坏了OFC内隐藏状态的编码。这些发现揭示了一个核心认知计算的回路实现，即更新关于环境抽象潜在状态的主观信念。

## Abstract
Beliefs about states of the world profoundly impact decision-making and learning, but little is known about how neural circuits represent and update beliefs. We performed projection-specific recordings and perturbations from neurons in the orbitofrontal cortex (OFC) projecting to the intermediate or rostral caudate putamen (CPi/CPr) in rats performing a task with hidden reward states. Stimulating OFC-CPi neurons biased rats' beliefs towards high reward states. Recordings from optogenetically-tagged OFC-CPi neurons showed that they encoded categorical evidence for high reward states, shaped by a saturating nonlinearity in neural responses. Downstream neurons could, in principle, decode the full belief distribution over reward states as rats deliberated about decisions. Finally, projection-specific perturbations disrupted encoding of hidden states within OFC. These findings reveal the circuit implementation of a core cognitive computation, updating subjective beliefs about abstract latent states of the environment.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **核心问题**：大脑如何表征和动态更新关于环境隐藏状态的主观信念？尽管信念对决策与学习影响深远，但其神经回路机制尚不清楚。
- **研究动机**：以往研究发现眶额皮层（OFC）参与价值推断和部分可观测任务，但具体投射通路和下游纹状体如何协同实现"状态推断"这一抽象认知计算仍属空白。
- **整体含义**：揭示 OFC→CPi（中间尾状壳核）回路是实现信念更新的关键皮质-纹状体通路，为理解概率推理、精神疾病中异常信念提供神经机制层面的解释。

### 2. 论文的方法论

- **行为任务与模型**：
  - 大鼠执行**时间下注任务**，奖励为隐藏状态（高/低/混合块），通过等待时间来度量主观价值。
  - **贝叶斯推断模型**：$P(B_t|R_t) \propto P(R_t|B_t) P(B_t)$，结合先验和似然计算最可能块，选择对应机会成本 $\kappa$ 并确定退出阈值。
  - 模型用于生成行为预测、估计信念分布，并作为分析神经记录的参照。
- **神经回路扰动与记录**：
  - **光遗传学刺激/抑制**：利用逆行Cre病毒在CPi或CPr表达ChR2，在奖励时刻激活 OFC→CPi 或 OFC→CPr 轴突末梢，测量行为变化。
  - **投射特异性电生理记录**：在OFC植入Neuropixels探针，同时在CPi/CPr植入光纤，通过**碰撞测试（collision test）** 鉴定逆行标记的投射神经元，记录其任务相关活动。
  - **数据分析技术**：
    - 判别指数 $d'$ 衡量神经元对大小奖励的区分能力。
    - logistic 回归解码器，分析信念（最可能块和第二可能块）的可解码性。
    - **去混合主成分分析（demixed PCA）** 分离时间、奖励量、隐藏状态（块）的神经群体动态，评估扰动对状态表征的影响。
- **受控变量操控**：
  - 对比刺激 OFC→CPi 与 OFC→CPr，检验通路功能特异性。
  - 变化模型参数（机会成本、时间常数、奖励感知）进行模拟，确定行为效应最匹配“信念偏向高状态”这一解释。

### 3. 实验设计

- **实验对象**：593只Long-Evans大鼠（雌雄均有），水限制以驱动任务执行。
- **行为范式与数据集**：
  - 隐藏状态任务（高、低、混合块），块间转换规律性。
  - 行为记录：等待时间、选择，包含捕捉试验（15-25%试次无奖励以测量等待意愿）。
  - 每次实验包含控制会话和刺激会话（40%试次在奖励时给光）。
- **神经记录**：
  - 运用Neuropixels探针长时间记录OFC神经活动，共记录到95个通过碰撞测试的OFC→CPi/CPr投射神经元。
  - 还同时记录光遗传学标记神经元及未被标记的OFC群体作为对照。
- **比较条件与方法**：
  - **两通路对比**：OFC→CPi vs. OFC→CPr 在行为调制和神经编码上的差异。
  - **假刺激和对照组**：同只动物在不同会话中交替进行控制/刺激，采用Wilcoxon符号秩检验等统计。
  - **模型对照**：测试不同参数修改（增加机会成本、改变时间常数、引入奖励感知偏差）以排除其他解释。
  - **解码分析对照**：比较 OFC→CPi 神经元与相同数量的未标记OFC神经元的解码性能，评估信息专一性。
  - **双变量设计**：在去混合PCA中，分别比较高奖励量高/混合块、低奖励量低/混合块，确保公平对比。

### 4. 资源与算力

- **硬件**：文中未明确说明所用GPU、计算集群或训练时长。行为训练为自动化高通量系统，电生理数据采集使用Neuropix-PXI硬件和Open Ephys。数据分析采用MATLAB、Kilosort2.5进行spike sorting，dPCA采用公开软件，但**未提算力具体配置**。

### 5. 实验数量与充分性

- **行为实验**：11只 OFC→CPi 刺激大鼠，7只 OFC→CPr 刺激大鼠，每只大鼠均有控制和刺激会话的重复测量，统计效力尚可。
- **电生理记录**：5只大鼠贡献60个 OFC→CPi 神经元，35个 OFC→CPr 神经元（来自补充表），加上大量未标记神经元作为背景。同只大鼠多次记录，增加样本量。
- **功能性验证**：
  - 行为扰动与多模型模拟比较，确认效应特异性。
  - 记录与行为模型结合：解码信念分布、分析饱和非线性、快发放中间神经元参与证据。
  - 去混合PCA分析在3只动物中进行，但包括多次会话（15个session），结果有一致性。
- **消融/对照实验**：
  - 刺激通路与不刺激对比、不同通路对比、不同块类型对比。
  - 比较模型不同参数变化，排除其他可能性。
  - 解码分析中将OFC→CPi与未标记OFC对比。
- **评估**：实验设计较严谨，包含内部对照、行为模型验证、群体和单神经元分析，提供了多层面收敛证据。样本量中等，但效应显著且统计方法恰当，实验结果充分且客观公平。

### 6. 主要结论与发现

- **OFC→CPi通路特异性更新信念**：
  - 刺激OFC→CPi神经元使大鼠行为偏向高奖励状态，最大效应在低奖励块，延迟从混合块到低块的行为转变，而刺激OFC→CPr无此效应。
  - 行为效应与模型模拟的“先验偏向高状态”一致，排除了调节机会成本、时间常数或奖励感知偏差等解释。
- **OFC→CPi神经元编码类别性证据**：
  - 在奖励时刻，该群体平均放电率反映高块证据（40/80 μL相对于5/10 μL），且呈现饱和非线性：优选奖励之间区分度低，非优选奖励区分度高。
  - 该饱和性质可能由快发放中间神经元（FSI）的抑制性输入实现，特别是一类正 d' 的FSI在80 μL时发放更强。
- **群体可解码完整信念分布**：
  - 在决策等待期间，可从 OFC→CPi 群体解码出最可能块和第二可能块，证明其携带完整后验分布信息，但在奖励时刻则主要编码高块证据，呈现时间上的多路复用。
- **OFC→CPi扰动干扰皮层状态表征**：
  - 刺激 OFC→CPi 轴突末梢后，OFC中对隐藏块状态的群体级编码被显著削弱，但奖励量的编码基本不受影响，表明状态推断依赖于该投射维持的环路动态（可能通过皮质-基底节-丘脑环路反馈）。

### 7. 优点

- **因果机制明确**：结合细胞类型特异性光遗传扰动和电生理记录，在相同动物中揭示特定投射的功能。
- **计算建模驱动**：行为模型不仅解释行为，还用于估计隐含信念，从而将神经数据与认知变量关联，增强解释深度。
- **多水平分析**：从行为、单神经元调谐、非线性机制、群体解码到宏观电路动态，构建了层次清晰的证据链。
- **严谨对照**：对比不同通路（CPi vs. CPr）、不同模型参数、未标记神经元等，强化结论可靠性。
- **揭示非线性与微环路机制**：把神经网络中的饱和特性和抑制性中间神经元纳入信念计算，提供机制性解释。
- **时间动态观察**：发现OFC→CPi神经元在试次不同阶段编码不同变量（等待期信念分布，奖励期证据），提出时间多路复用模型。

### 8. 不足与局限

- **样本量与普适性**：记录到的投射神经元总数有限（95个），部分分析中数据分散，可能限制对异质性的深入刻画。结果基于大鼠，外推到灵长类或人类尚需验证。
- **扰动方式有限**：光遗传学刺激是单向增加活动，不能完全模拟自然信念更新，未来可采用抑制或双向操纵。
- **下游机制未直接验证**：虽然推测CPi整合跨试次证据并计算信念，但未记录下游CPi神经元活动，也未直接证明皮质-基底节-丘脑环路的作用。
- **计算模型简化**：模型假设固定块长和简单过渡概率，可能遗漏动物的真实内部模型复杂性。
- **抑制性中间神经元分析初步**：FSI参与的证据仅基于相关分析和正 d' 细胞，对其他中间神经元类型未探讨，且缺乏直接扰动。

（完）
