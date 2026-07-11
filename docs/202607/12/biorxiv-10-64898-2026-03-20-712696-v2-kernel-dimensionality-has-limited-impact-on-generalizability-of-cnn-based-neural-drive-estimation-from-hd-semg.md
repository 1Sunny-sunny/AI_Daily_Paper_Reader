---
title: Kernel Dimensionality Has Limited Impact on Generalizability of CNN-Based Neural Drive Estimation from HD-sEMG
title_zh: 核维度对基于HD-sEMG的CNN神经驱动估计泛化能力影响有限
authors: "Fu, J., Huang, H. J., Wen, Y."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.20.712696v2.full.pdf"
tags: ["query:sr"]
score: 10.0
evidence: 基于CNN的高密度肌电神经驱动估计
tldr: "卷积神经网络常用于从高密度表面肌电信号估计神经驱动，但核维度（1D、2D、3D）对跨数据集泛化能力与计算效率的影响尚不明确。本研究比较了仅核维度不同的三种CNN架构，在单数据集训练后直接评估于两个独立数据集。结果表明，核维度对泛化性能影响微小，2D和3D CNN仅略优于1D CNN（R值高0.2%）；计算效率因平台而异，3D CNN在CPU上最慢。结论是2D CNN兼顾精度与效率，最适合部署。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-001.webp\", \"caption\": \"Fig. 1: Experimental protocols of the datasets used to train and evaluate the deep CNN models. (a) The training dataset was recorded from the VL and VM muscles during isometric knee extension in five participants on two separate days at 25% MVC. (b) The cross-intensity evaluation dataset was recorded during isometric ankle plantarflexion across three intensities (10%, 30%, and 50% MVC) from GM muscle in seven different participants on a single day. (c) The crossmuscle evaluation dataset was also recorded during isometric ankle plantarflexion across three muscles (GM, GL, and SOL) in six different participants on a single day at 30% MVC.\", \"page\": 2, \"index\": 1, \"width\": 524, \"height\": 595}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-004.webp\", \"caption\": \"Fig. 2: Architecture of the deep CNNs for neural drive decoding from HD-sEMG signals. All models consisted of two convolutional blocks, each comprising two convolutional layers, batch normalization, max pooling, and dropout. Features extracted from the convolutional blocks were flattened and passed to a multi-head dense architecture to decode neural drive as cumulative spike trains (CSTs). The 1D, 2D, and 3D CNNs shared the same network architecture and differed only in the dimensionality of the convolutional kernels, enabling the extraction of temporal, spatial, and spatiotemporal features, respectively.\", \"page\": 3, \"index\": 4, \"width\": 527, \"height\": 381}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-006.webp\", \"caption\": \"TABLE I: The structure of the 1D, 2D, and 3D CNNs used to decode neural drive from HD-sEMG signal. The abbreviations Conv, Act Fun, ReLU, MaxPool, and Fc denote a convolutional layer, Activation Function, Rectified Linear Unit, and a fully connected layer. Note that this table only includes one head of dense layers as all 4 heads are identical, and the output row indicates the concatenated dimension of the output from all 4 heads.\", \"page\": 4, \"index\": 6, \"width\": 1064, \"height\": 358}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-007.webp\", \"caption\": \"Fig. 4: (a) Six consecutive frames of the flattened HD-sEMG signal in which the time duration is about 68.4 ms. The red window shows the nth frame, which includes 40 samples, and the blue window shows the (n + 1)th frame. The nth and (n + 1)th frame has 20 samples overlapped; (b) The output of the deep CNN, which was the neural drive represented as CST; (c) The shape of the HD-sEMG signal for 1D CNN; (d) The shape of the HD-sEMG after padding and reshaping for 2D CNN; (e) The shape of a HD-sEMG frame for 3D CNN.\", \"page\": 5, \"index\": 7, \"width\": 522, \"height\": 366}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-008.webp\", \"caption\": \"Fig. 5: Nested cross-validation pipeline for training and validating the deep CNNs on the training dataset (5 subjects, 2 days, 2 muscles, 3 contractions). Outer split: a leave-onecondition-out scheme over the four day × muscle conditions, across four runs, each condition is held out once as the test set (green) while the remaining three form the training set (orange). Inner split: within each run, the three contractions (C1–C3) of the training conditions are divided by leave-onecontraction-out into three sub-folds, each sub-fold using two contractions for training (blue) and one for validating the model (red).\", \"page\": 5, \"index\": 8, \"width\": 522, \"height\": 533}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-002.webp\", \"caption\": \"Fig. 6: Generalizability of the deep CNNs evaluated on the cross-intensity dataset (recorded at 10%, 30%, and 50% MVC). (a) Correlation coefficient (R) and (b) normalized root-mean-square error (nRMSE) between the BSS-estimated neural drive and the neural drive mapped from the CNNestimated neural drive.\", \"page\": 7, \"index\": 2, \"width\": 501, \"height\": 713}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-003.webp\", \"caption\": \"Fig. 7: Cross-muscle generalizability of the 1D, 2D, and 3D CNNs evaluated on the independent testing dataset (recorded at GM, GL and SOL muscles). (a) Correlation coefficient and (b) normalized root-mean-square error between the BSSestimated neural drive and the neural drive mapped from the CNN-estimated neural drive, shown for each muscle.\", \"page\": 7, \"index\": 3, \"width\": 511, \"height\": 706}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-20-712696-v2/fig-005.webp\", \"caption\": \"Fig. 9: Average inference time per sample for the 1D, 2D, and 3D CNNs on CPU and CUDA-enabled GPU platforms. Bars and error bars denote the mean and standard deviation. On the CPU, inference time increased sharply with kernel dimensionality, the 3D CNN being the slowest; on the GPU, the three models converged to a similar range, as GPU execution reduced the cost of the 3D CNN but increased that of the 1D and 2D CNNs.\", \"page\": 8, \"index\": 5, \"width\": 484, \"height\": 388}]"
motivation: 探究不同核维度CNN在跨数据集神经驱动估计中的泛化能力与计算效率差异。
method: 构建三种仅核维度不同的CNN，在一个数据集上训练，直接在两个独立数据集上测试泛化性能与推理速度。
result: "所有架构均泛化成功，2D/3D CNN仅比1D CNN的R值高0.2%，而3D CNN在CPU上推理慢一倍。"
conclusion: 增加核维度未提升泛化性，2D CNN在精度与效率间取得最佳平衡，适用于资源受限平台。
---

## 摘要
卷积神经网络（CNN）因其实时性能而被广泛用于从高密度表面肌电图（HD-sEMG）信号中估计神经接口的神经驱动。根据核维度（1D、2D或3D），CNN可以提取时间、空间或时空特征。鉴于运动单位动作电位在空间和时间上传播，利用空间特征的架构可能为神经驱动估计提供优势。尽管核维度具有潜在重要性，但其对神经驱动估计的影响仍知之甚少。现有研究主要在同一HD-sEMG数据集内评估CNN在不同被试、收缩强度或肌肉之间的泛化能力，而很少考虑计算效率。因此，不同核维度是否影响跨数据集泛化能力和计算效率仍不清楚。在本研究中，我们实施了三种仅在核维度上有所不同的CNN架构，以探究利用运动单位动作电位的空间和时空特征是否提高从下肢等长收缩期间记录的HD-sEMG估计神经驱动的泛化能力和计算效率。我们在一个HD-sEMG数据集上训练CNN，并在没有重新训练的情况下，在两个独立、未见过的数据集上进行评估，这些数据集来自不同被试、不同时段和不同实验方案——一个包含三种收缩强度，另一个包含三块肌肉。所有三种架构都泛化到了两个未见过的数据集。2D和3D CNN略微优于1D CNN，R值增加了0.2%，而3D CNN相对于2D CNN没有优势。计算效率以平台依赖的方式取决于核维度。在CPU上，3D CNN显示出最慢的推理时间，比2D和1D CNN慢2倍，这是因为其时空卷积的算术成本更高。在GPU上，所有三种架构都实现了约1.36毫秒/采样的相似推理时间。这些发现表明，CNN架构复杂性的增加并不能提高神经驱动估计的泛化能力，而2D CNN在精确性和效率之间提供了最佳平衡，适用于可靠的、可部署的基于CNN的神经驱动估计器——特别是在仅使用CPU或资源受限的平台上。

## Abstract
Convolutional neural networks (CNNs) have been widely used to estimate neural drive from high-density surface electromyography (HD-sEMG) signals in neural machine interfaces owing to their real-time capability. Depending on kernel dimensionality (1D, 2D, or 3D), CNNs can extract temporal, spatial, or spatiotemporal features. Given that motor unit action potentials propagate across both space and time, architectures that exploit spatial features may offer advantages for neural drive estimation. Despite the potential importance of kernel dimensionality, its influence on neural drive estimation remains poorly understood. Existing studies have mainly evaluated CNN generalizability across participants, contraction intensities, or muscles within the same HD-sEMG dataset, while computational efficiency has seldom been considered. As a result, it remains unclear whether different kernel dimensionalities affect cross-dataset generalizability and computational efficiency. In this study, we implemented three CNN architectures -- differing only in kernel dimensionality -- to investigate whether exploiting the spatial and spatiotemporal features of motor unit action potentials improves the generalizability and computational efficiency of neural drive estimation from HD-sEMG recorded during lower-limb isometric contractions. We trained the CNNs on one HD-sEMG dataset and evaluated them, without retraining, on two independent, unseen datasets recorded from different participants, sessions, and protocols -- one spanning three contraction intensities and the other three muscles. All three architectures are generalized to both unseen datasets. The 2D and 3D CNNs marginally outperformed the 1D CNN with a 0.2% increase in R, while the 3D CNN showed no advantage over the 2D CNN. Computational efficiency depended on kernel dimensionality in a platform-dependent manner. On the CPU, the 3D CNN showed the slowest inference time, which was 2x slower than the 2D and 1D CNN, owing to the higher arithmetic cost of its spatiotemporal convolutions. On the GPU, all three architectures achieved similar inference times of about1.36 ms/sample. These findings indicate that increased architectural complexity of CNN does not improve generalizability for neural drive estimation, and that a 2D CNN offers the best balance of accuracy and efficiency for a reliable, deployable CNN-based neural drive estimator--particularly on CPU-only or resource-constrained platforms.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义
- **研究问题**：从高密度表面肌电（HD‑sEMG）信号中估计神经驱动（neural drive）时，CNN卷积核的维度（1D、2D、3D）是否会影响模型的**跨数据集泛化能力**与**计算效率**。
- **研究动机**：运动单位动作电位同时在空间（肌纤维传导）和时间维度上传播，利用空间特征的2D/3D CNN理论上可能比纯时序1D CNN更有利于神经驱动解码。然而现有工作仅在同一数据集内评估泛化性，且很少关注计算效率，核维度的实际作用尚不明确。
- **整体含义**：探究能否通过引入空间或时空特征提升神经驱动估计器的通用性和部署效率，为基于CNN的实时神经接口提供设计依据。

## 2. 论文提出的方法论
- **核心思想**：构建三种架构完全相同、**仅卷积核维度不同**的CNN，分别提取时间（1D）、空间（2D）、时空（3D）特征，以孤立核维度的影响。
- **网络结构**（三种模型共享）：
  - 两个卷积块，每个包含两层卷积、批归一化、ReLU激活、最大池化、Dropout。
  - 特征展平后，送入多头全连接层，输出为累计脉冲序列（CST）形式的神经驱动。
- **输入处理**：
  - 将HD‑sEMG分割为时长约68.4 ms的重叠帧（40采样点，滑动步长20采样点）。
  - **1D CNN**：直接使用原始二维信号（通道×时间），应用一维时间卷积。
  - **2D CNN**：先将电极信号填充并重塑为二维空间网格（电极阵列），然后应用二维卷积，捕获空间-时间局部特征。
  - **3D CNN**：将每一帧视为三维体（空间-空间-时间），使用三维卷积提取时空局部特征。
- **训练与验证**：
  - 在训练数据集上采用**嵌套交叉验证**：外层按“天×肌肉”组合留一，内层按“收缩次数”留一，用于超参数选择与模型选择。
  - ground truth神经驱动由盲源分离（BSS）方法估计得到，评估指标为相关系数 $R$ 和归一化均方根误差 $\mathrm{nRMSE}$。

## 3. 实验设计
- **数据集与场景**：
  - **训练集**：5名受试者，两天，两块肌肉（股外侧肌VL、股内侧肌VM），等长膝关节伸展，25% MVC，共12个条件（天×肌肉）。
  - **跨强度测试集**：7名不同受试者，踝关节跖屈，腓肠肌内侧头（GM），三种收缩强度（10%、30%、50% MVC），仅一天。
  - **跨肌肉测试集**：6名不同受试者，踝关节跖屈，30% MVC，三块肌肉（GM、腓肠肌外侧GL、比目鱼肌SOL），仅一天。
  - 所有测试集均完全未在训练阶段出现，且受试者、实验方案、肌肉均不同，构成严格的无重训练跨数据集泛化评估。
- **对比方法（benchmark）**：
  - 三种CNN架构：1D CNN、2D CNN、3D CNN。
  - 本质上是自身对照，比较不同核维度下的泛化性能和推理时间。
- **评估指标**：
  - 相关系数 $R$ 和 $\mathrm{nRMSE}$，衡量估计神经驱动与BSS参考驱动的一致性。
  - 推理时间（ms/样本），分别在CPU和CUDA GPU上测量。

## 4. 资源与算力
- 文中仅提及推理效率测试时使用**CPU**和**CUDA‑enabled GPU**，但**未明确给出GPU型号、数量、训练时长、显存占用或总FLOPs**等具体算力信息。
- 训练过程的硬件配置和耗时同样未作说明，无法从现有内容推断所需的计算资源规模。

## 5. 实验数量与充分性
- **实验数量**：
  - 训练阶段：嵌套交叉验证共4个外层折、每个外层3个内层折，产生12组训练/验证拆分。
  - 跨强度评估：3种强度 × 7名受试者 × 每种条件多次重复（具体次数未细述），得到多组 $R$ 与 $\mathrm{nRMSE}$。
  - 跨肌肉评估：3块肌肉 × 6名受试者，同样多组指标。
  - 推理效率测量：每种模型在CPU和GPU上分别多次推理，取均值与标准差。
- **充分性与公平性**：
  - 通过在同一训练流程、完全相同网络层数及参数量的条件下对比，仅改变核维度，实验设计**公平**。
  - 严格的多层交叉验证、完全独立的测试集，使得泛化结论可信。
  - 覆盖了不同肌肉、不同收缩强度、不同受试人群，实验维度**相对充分**，能反映核维度的主要影响。
  - 未进行消融实验（如不同网络深度、不同电极数），但鉴于研究目标聚焦于核维度，当前实验已足够回答核心问题。

## 6. 论文的主要结论与发现
- **泛化性**：三种架构均成功泛化到两个未见过的数据集，但核维度带来的性能提升极其微小。
- **精度差异**：2D和3D CNN仅比1D CNN的 $R$ 值高约**0.2%**，3D相对2D无额外优势，差异在统计上可能不显著。
- **计算效率**：
  - **CPU**：3D CNN推理时间最长，约为2D和1D CNN的**2倍**，原因是三维卷积计算开销大。
  - **GPU**：三种模型推理时间趋于一致（约1.36 ms/样本），GPU的并行能力抵消了3D卷积的额外成本，但1D和2D在GPU上的效率反而下降。
- **最终建议**：2D CNN在精确度和效率间达到**最佳平衡**，尤其适用于仅CPU或资源受限的部署场景。

## 7. 优点
- **问题聚焦，控制严格**：唯一变量是核维度，排除了其他架构差异的干扰，结论明确。
- **真实泛化评估**：采用完全独立的受试者、肌肉群、实验协议和数据集，避免在同一数据集内循环验证的伪泛化。
- **双维度评价**：同时考察精度和推理效率，为实际部署提供指导。
- **实验设计严谨**：多层级交叉验证、公开基准指标（BSS参考）、多种收缩条件和肌肉，可信度较高。
- **实用性取向**：明确推荐2D CNN为轻量、可靠的选择，对可穿戴神经接口有直接指导意义。

## 8. 不足与局限
- **动作范式单一**：仅评估了下肢等长收缩，未涉及动态运动或上肢肌肉，对其他动作模式的泛化性未知。
- **地面真值依赖**：神经驱动真值基于BSS分解，BSS本身存在分解不确定性和误差，可能影响结论的绝对定量精度。
- **训练数据规模有限**：仅使用5名受试者、两种肌肉的训练集，模型可能未充分学习更丰富的肌电模式，从而限制核维度差异的显现。
- **算力报告缺失**：未提供GPU型号、训练耗时等详细资源信息，使读者难以评估实际训练成本和扩展性。
- **模型结构单一**：仅比较核维度，未探讨网络深度、宽度、残差连接等其他设计要素的影响；推理效率分析局限于单样本延迟，未考虑吞吐量与内存占用。
- **环境假设**：实验室高质量HD‑sEMG信号，未测试在电极偏移、汗液干扰、运动伪迹等真实噪声条件下的鲁棒性。

（完）
