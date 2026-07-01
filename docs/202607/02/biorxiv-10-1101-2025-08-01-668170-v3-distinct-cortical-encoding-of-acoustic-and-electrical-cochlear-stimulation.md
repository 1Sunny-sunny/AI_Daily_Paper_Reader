---
title: Distinct cortical encoding of acoustic and electrical cochlear stimulation
title_zh: 听觉与电刺激耳蜗在大脑皮层的不同编码
authors: "Hight, A. E., Insanally, M. N., Scarpa, J. K., Tamaoki, Y., Makol, R., Cheng, Y.-S., Trumpis, M., Viventi, J., Svirsky, M., Froemke, R. C."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.1101/2025.08.01.668170v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 声学和电学耳蜗刺激的皮层编码
tldr: 人工耳蜗神经编码机制不明，本研究用微皮质电图记录失聪大鼠皮层活动，发现电刺激虽可解码但时空动态与声学刺激迥异，声学解码器无法跨模态泛化，提示两种刺激感知表征可能不同。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究人工耳蜗电刺激与正常声学刺激在听觉皮层神经表征上的差异。
method: 使用微皮质电图记录失聪大鼠在声学与人工耳蜗电刺激下的皮层群体活动。
result: 电刺激引发粗糙耳蜗拓扑结构，刺激身份可解码，但时空反应模式与声学刺激显著不同，且声学训练的解码器对电刺激无效。
conclusion: 电刺激引发的皮层网络动态与声学刺激本质不同，可能影响人工耳蜗的感知质量。
---

## 摘要
人工耳蜗是一种神经假体装置，能够帮助极重度耳聋患者恢复听力和言语理解能力，是生物医学工程与研究应用于临床状况的典范。然而，由于对植入刺激所引起的神经环路反应缺乏了解，该装置在许多受试者中的效用受到限制。近期我们证实，失聪大鼠能够利用人工耳蜗识别声音，且这种训练会精细化初级听觉皮层中单个神经元的反应。在此，我们探究了皮层神经元局部集群如何表征急性植入刺激，为此使用了我们开发的用于皮层表面记录的电极阵列，即微皮层脑电图（micro-ECoG），这是一种颅内脑电图（iEEG）形式。我们发现，与听力正常大鼠中更清晰的音调拓扑空间表征相比，人工耳蜗刺激所引发的空间组织粗略且非随机，但各记录位点之间缺乏一致的、陡峭分级的耳蜗拓扑证据。尽管在两种情况下刺激身份均可被成功解码，但对声学输入的单试次iEEG反应比人工耳蜗刺激的反应更可靠。然而，声学与人工耳蜗刺激的时空反应图谱存在显著差异。在同一动物致聋并接受人工耳蜗刺激后，以声学反应训练的译码器在电刺激反应测试中显示几乎为零的信息传递。因此，尽管急性人工耳蜗刺激诱发了具有粗略耳蜗拓扑结构的空间非随机皮层活动，但其网络活动动态与声学刺激诱发的动态存在显著差异，这可能对尚未测试的感知相似性产生影响。

## Abstract
Cochlear implants are neuroprosthetic devices that restore hearing and speech comprehension to profoundly deaf humans and represent an exemplar application of biomedical engineering and research to clinical conditions. However, the utility of these devices in many subjects is limited, largely due to lack of information about how neural circuits respond to implant stimulation. Recently we showed that deafened rats can use cochlear implants to recognize sounds, and that this training refined the responses of single neurons in the primary auditory cortex. Here we asked how local populations of cortical neurons represent acute implant stimuli, using electrode arrays we developed for cortical surface recordings for micro-electrocorticography (micro-ECoG), a form of intracranial electroencephalography (iEEG). We found that there was a coarse, non-random spatial organization with limited evidence for consistent, sharply graded cochleotopy across recording sites, relative to a clearer tonotopic spatial representation in normal-hearing rats. Single-trial iEEG responses to acoustic inputs were more reliable than responses to cochlear implant stimulation, although stimulus identity could be successfully decoded in both cases. However, the spatio-temporal response profiles to acoustic vs cochlear implant stimulation were substantially different. Decoders trained on acoustic responses showed essentially zero information transfer when tested on electrical stimulation responses in the same animals after deafening and cochlear implant stimulation. Thus, while acute cochlear implant stimulation evoked spatially non-random cortical activity with coarse cochleotopic structure, the dynamics of network activity were substantially different from those evoked by acoustic stimulation, with possible implications for perceptual similarity that remain to be tested.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义  
- **核心问题**：人工耳蜗通过电刺激耳蜗内电极恢复听力，但其刺激在听觉皮层中所引发的神经集群表征是否与正常声学刺激相同或可迁移，尚不清楚。  
- **整体含义**：本研究旨在直接比较同一动物在急性条件下，声学刺激与人工耳蜗电刺激在初级听觉皮层诱发的群体编码差异，以揭示为何人工耳蜗用户的感知体验可能与自然听觉有本质不同，并为神经假体设计和编程提供神经生理学依据。

### 2. 论文提出的方法论  
- **核心思想**：利用高密度微皮层脑电图（μECoG）阵列，同时记录大鼠听觉皮层60个位点的诱发电位，提取事件相关电位（ERP）和高γ振荡（HG），分别从空间组织、单试次变异性和可解码性三个层次对比两种刺激模态的神经表征。  
- **关键技术细节**：  
  - **信号处理**：原始信号经2-150 Hz带通滤波，去除工频干扰，降采样至2 kHz，再经2-100 Hz（ERP）或70-140 Hz（HG）滤波；ERP幅度取刺激后50 ms内最大值减去基线，HG经整流、平滑后取同样方式幅度。  
  - **空间组织量化**：计算最佳频率/通道，构建空间相关曲线，并用局部梯度向量平均的“全局拓朴向量”和随机置换检验统计其非随机性。  
  - **单试次解码**：  
    * **PCA‑LDA**：将时空特征展平为试次×（位点·时间点）矩阵，用主成分分析（PCA）降至15维，训练线性判别分析（LDA）分类器，通过1000次bootstrap随机划分训练/测试集评估解码准确率和误差距离。  
    * **TCA‑LDA**：采用规范多元分解（CP分解），将数据构造成 $R \times S \times T$ 三维张量（$R$ 为时间点、$S$ 为空间位点、$T$ 为试次），分解出15个潜在因子，每个因子包含正交的空间、时间和试次成分；仅用试次因子训练LDA，实现解码。  
  - **跨模态信息传递**：用声学数据训练TCA模型并固定空间、时间因子，仅重拟合电刺激数据的试次因子，再用声学训练的LDA解码器对电刺激试次因子进行分类，计算互信息与最大可能信息的比值，从而量化两种模态表征的可迁移性。

### 3. 实验设计  
- **数据集与场景**：  
  - 大鼠模型：7只正常听力（normal‑hearing, NH）大鼠，7只双侧机械性致聋并单侧植入8通道人工耳蜗（cochlear implant, CI）的大鼠。其中NH组4只、CI组3只经过行为训练（听觉go/no‑go任务）。  
  - 刺激：NH组给予纯音（0.5~32 kHz，半倍频程间隔，70 dB SPL）；CI组给予单通道双相电荷平衡电脉冲（900 Hz，单极配置），通过临床言语处理器或直接编程控制。  
  - 记录：自制的61电极μECoG阵列（有效60通道，间距406 μm）硬膜外置于左半球核心听觉皮层。  
- **Benchmark 与对比**：  
  - 在同一动物内进行声学反应与CI反应的前后对比（4只接受两种记录）。  
  - 对比ERP与HG信号在不同分析中的表现。  
  - 解码分析中，对比使用全部时空信息、仅空间信息、仅时间信息的解码准确率。  
  - 跨模态测试中，以声学模型对电刺激数据进行解码，并与打乱基线进行比较。

### 4. 资源与算力  
- 文中未提及所使用的GPU型号、数量或训练时长。所有信号处理和解码分析均通过MATLAB自定义脚本完成，未报告大规模深度学习或需要特定算力的计算。

### 5. 实验数量与充分性  
- **总体实验组数**：  
  - 直接对比两组动物（NH vs CI）在空间组织、变异性、解码等方面的实验至少包含4类分析（空间相关性、拓朴向量、单试次变异性、分类）。  
  - 每种分析又分为ERP和HG两个子型，部分还拆分为空间、时间单独分析。  
  - 跨模态传递分析单独作为一个严格实验，包含正对照（声学→声学）和跨模态测试。  
- **充分性与公平性**：  
  - 样本量有限（每组7只），但利用前后对照（4只）增强了统计效力，且所有比较均采用线性混合效应模型控制个体差异。  
  - 刺激自身差异（纯音vs电流）不可避免，但跨模态传递实验设计本身已经规避了直接配对问题，通过信息传递比值来评估，较为公平。  
  - 行为训练对结果无显著影响，因此合并分析具有合理性。  
  - 总体实验设计较系统，覆盖了从宏观组织到单试次编码再到跨模态泛化的完整证据链，判断较充分。

### 6. 论文的主要结论与发现  
- **空间组织**：CI电刺激诱发的皮层活动具有粗尺度、非随机的空间结构，但与声学刺激相比，缺乏精细、梯度陡峭的耳蜗拓扑（cochleotopy）；ERP比HG信号能更明显地区分CI和NH的空间组织差异。  
- **单试次变异性**：CI刺激的空间反应模式在试次间更具变性（尤其在ERP中显著），而时间反应变异性两组无显著差异。  
- **刺激身份解码**：无论是PCA‑LDA还是TCA‑LDA，均可从单试次iEEG信号中解码刺激身份；CI的解码性能略低于NH（ERP尤为明显）；解码可通过空间特征或时间特征单独实现。  
- **跨模态信息传递**：在声学反应上训练的TCA‑LDA译码器无法泛化到CI电刺激反应，信息传递率接近0%甚至低于随机基线，表明两种模态的皮层群体表征本质不同。

### 7. 优点  
- **记录技术**：采用高密度μECoG阵列，兼顾较高空间分辨率和良好信噪比，对临床应用具有潜在的转化价值。  
- **双重分析维度**：同时分析ERP（低频）和HG（高频）信号，揭示二者在编码刺激身份和空间组织中的不同角色。  
- **前后自身对照**：部分动物在致聋前后记录，消除个体差异干扰，使得跨模态比较更具说服力。  
- **解码方法先进**：将TCA引入iEEG分析，能够分离空间、时间和试次因子，并直接检验跨模态的可迁移性，比单纯PCA‑LDA更具解释力。  
- **实验控制**：使用临床级植入体和言语处理器，电刺激参数和编程接近现实应用。

### 8. 不足与局限  
- **急性麻醉条件**：所有记录均在麻醉下进行，且为急性激活，未观察长期适应或行为反馈下的可塑性变化，不能排除长期使用后表征趋同的可能。  
- **样本量有限**：NH和CI各7只，部分分析仅4只前后对照，统计效力受限，跨模态传递不显著的结果可能反映真实效应或样本不足。  
- **刺激可比性**：电刺激通道间距与纯音频率间隔在感知意义上不一致，且单极电刺激的电流扩散效应可能模糊空间分辨率，使cochleotopy表现粗糙。  
- **种属差异**：大鼠耳蜗较小，听觉皮层拓扑与人差异较大，临床应用推断需谨慎。  
- **记录覆盖范围**：μECoG虽空间分辨率优于头皮EEG，但仍反映数千神经元的平均活动，无法完全替代单细胞记录，可能低估精细的空间组织。  
- **缺乏直接感知关联**：未结合行为感知实验或主观等价性比较，无法直接证实表征差异是否导致感知差异。

（完）
