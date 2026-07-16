---
title: Diffusion Latent Representations for Neural Decoding
title_zh: 神经解码的扩散潜在表示
authors: "Wong, B., Laschowski, B."
date: 2026-07-13
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.08.737343v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 用于神经语音解码的扩散潜在表示
tldr: "神经解码需将神经活动映射到中间表示以进行重建，但中间表示的选择影响性能。本文提出新框架研究该影响，并以扩散模型潜在表示为证，应用于语音解码。实验发现不同扩散时间步的潜在表示导致解码性能差异显著（词错误率44.7%至3.5%），表明扩散潜在表示有效但依赖时间步选择，该框架为系统研究中间表示效应奠定了基础。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/fig-001.webp\", \"caption\": \"Fig. 1. Overview of our framework for studying how representation choice influences downstream learning and reconstruction. A pretrained diffusion model performs reverse diffusion using the ground-truth conditioning factor M to generate target latent variables zi, which are tokenized into Vi. The latent model maps neural activity onto tokenized latent representations, which are then untokenized into z′i. Simultaneously, the conditioning factor model predicts M ′ using the ground-truth conditioning factor M as the target. During inference, z′i and M ′ are injected into the pretrained diffusion model to reconstruct the target stimulus.\", \"page\": 2, \"index\": 1, \"width\": 1076, \"height\": 592}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/fig-002.webp\", \"caption\": \"Fig. 2. Training dynamics for the conditioning factor and latent models. The top row shows training and validation losses and the bottom row shows validation Word Error Rate (WER) under teacher-forced generation. Although all models showed stable optimization, downstream reconstruction performance depended on the intermediate representation.\", \"page\": 5, \"index\": 2, \"width\": 1076, \"height\": 642}]"
motivation: 探究神经解码中不同中间表示如何影响下游学习与重建性能。
method: 提出分析框架，并采用不同扩散时间步的潜在表示进行神经语音解码实验。
result: "不同时间步的潜在表示导致教师强制词错误率从44.7%骤降至3.5%。"
conclusion: 扩散潜在表示能作为有效中间表示，但其成功强烈依赖于扩散时间步的选择；框架为系统研究提供了基础。
---

## 摘要
神经解码可以看作一个表示学习问题，其中神经活动被映射到一个中间表示，再进行下游重建。中间表示的选择会影响性能和学习难度。在此，我们提出了一个新框架，用于研究中间表示的选择如何影响下游学习和重建。作为概念验证，我们以扩散潜在表示为例，从不同的扩散时间步提取表示用于神经语音解码。逐成分评估显示，重建性能在不同扩散时间步间差异显著，不同潜在模型的强制教师词错误率分别为44.7%、7.5%和3.5%。这些结果表明，扩散潜在表示可以作为从神经活动中学习的有效中间表示，但其有效性强烈依赖于所选的扩散时间步。更广泛地说，我们的框架为系统性地研究中间表示选择如何影响下游学习和重建提供了基础。

## Abstract
Neural decoding can be viewed as a representation learning problem in which neural activity is mapped into an intermediate representation before downstream reconstruction. The choice of intermediate representation influences both performance and learning difficulty. Here we developed a novel framework for studying how intermediate representation choice influences downstream learning and reconstruction. As a proof-of-concept, we instantiated our framework using diffusion latent representations extracted from different diffusion timesteps for neural speech decoding. Component-wise evaluation showed that reconstruction performance differed substantially across diffusion timesteps, with teacher-forced Word Error Rates of 44.7%, 7.5%, and 3.5% for different latent models. These results demonstrate that diffusion latent representations can serve as effective intermediate representations for learning from neural activity, but that their effectiveness depends strongly on the selected diffusion timestep. More broadly, our framework provides a basis for systematically studying how intermediate representation choice influences downstream learning and reconstruction.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **问题**：神经解码通常需要将高维、嘈杂的神经活动映射为中间表示，再交由解码器重建（例如语音）。但不同中间表示的选择会如何影响下游学习的难度和重建质量，缺少系统性的研究。
- **动机**：现有工作大多针对单一任务挑选一种固定表示，很少比较“不同中间表示”带来的影响，尤其在数据有限、维度高的神经解码中，表示的选择尤为关键。
- **整体含义**：本文的目标不是提出一种新的解码器，而是提供一个通用框架来**衡量和对比不同中间表示对于从神经活动学习及最终重建的影响**。作为概念验证，作者选用扩散模型在不同去噪时间步的潜在变量作为中间表示，并通过神经语音解码任务来展示框架的能力。

### 2. 方法论
- **核心思想**：将中间表示学习看作一个“神经活动 → 中间表示 → 下游重建”的流水线，并让中间表示可通过**冻结的预训练扩散模型**来生成和评估，从而隔离表示本身的影响。
- **框架三阶段**：
  1. **生成训练目标**：用预训练的 DiffWave 条件扩散模型，从合成语音中提取不同扩散时间步 $i$ 的潜在变量 $z_k^i$，并用 EnCodec 的残差向量量化（RVQ）将其 token 化为 $V_k^i$；同时生成条件因子（梅尔谱图 $M_k$）。
  2. **编码器预测**：用共享编码器的两个 Transformer 解码器，分别自回归地预测 token 化潜在序列 $V_k^i$（潜在模型）和梅尔谱图 $M_k$（条件因子模型）。潜在模型在每个自回归步骤同时预测所有 $J=4$ 个 RVQ 码本的索引；条件因子模型用线性层直接回归。
  3. **冻结扩散解码**：将预测的潜在 token 反量化为连续表示 $z'_i$，与预测的条件因子 $M'$ 一同输入冻结的 DiffWave，完成从噪声到清晰语音的反向扩散。
- **关键公式**：反向扩散一步更新为  
  $$z'_{k_{i-1}} = \frac{1}{\sqrt{\alpha_i}}\left(z'_{k_i} - \frac{\beta_i}{\sqrt{1-\bar\alpha_i}} \epsilon_\theta(z'_{k_i}, i, M'_k)\right) + \sigma_i z,$$
  其中 $z\sim\mathcal{N}(0,I)$，$\sigma_i$ 是 DiffWave 的超参数。
- **训练细节**：仅优化编码器部分（潜在模型和条件因子模型），冻结扩散模型。损失函数：潜在模型为所有 $J$ 个码本的交叉熵之和，条件因子模型为均方误差，停止概率头为二元交叉熵。优化器 Adam，学习率 $5\times10^{-4}$，批次 128，训练 100 个 epoch，无学习率调度和 dropout。

### 3. 实验设计
- **数据集**：一名受试者的 256 通道微电极阵列（颅内记录），神经活动按时长 20 ms 分箱，提取阈值穿越和锋电位频带功率，得到 512 维特征。预定义训练集 7,879 个神经-句子对，验证集 1,409 对。
- **Benchmark**：
  - **组件评估**（教师强制）：分别评估条件因子模型（给定真实条件因子）和三个不同扩散时间步的潜在模型（给定真实梅尔谱图），用**词错误率（WER）** 衡量。
  - **端到端评估**：将最佳潜在模型与条件因子模型组合，比较教师强制生成和完全自回归生成的 WER，并引用先前研究［10］在相同数据上的自回归结果（6.3%）。
- **对比方法**：对比三个扩散时间步 $i\in\{1,2,3\}$ 的潜在模型，以及条件因子模型，观察不同“中间表示”带来的性能差异。

### 4. 资源与算力
- 训练使用 **四块 NVIDIA H100 GPU**，采用 PyTorch 的 DistributedDataParallel。
- 文中未提供具体训练耗时，但给出了模型大小（隐藏维度 128、4 层 Transformer、2 注意力头）和训练 epoch 数（100），可间接估算计算量。

### 5. 实验数量与充分性
- **实验组数**：共训练了 **4 个编码器模型**（1 个条件因子模型 + 3 个不同时间步的潜在模型），并进行两类评估（组件和端到端）。此外展示了训练 loss 和验证 WER 随 epoch 变化的曲线。
- **充分性**：
  - **优点**：组件评估将条件因子和潜在表示的贡献分离，能清晰观察到不同时间步的表示对下游重建的影响，设计干净、目标明确。
  - **局限**：仅在一个受试者、一种神经信号（微电极阵列）、一种扩散架构（DiffWave）和一种 token 化方法（EnCodec）上进行了验证。未对比其它中间表示（如自编码器特征或手工特征），也缺少对不同编码器结构、训练样本量、扩散模型种类的消融研究。因此实验结论的普适性有限，但作为概念验证是足够的。

### 6. 论文的主要结论与发现
- **表示选择影响显著**：不同扩散时间步的潜在表示导致教师强制 WER 差异巨大：模型 1（i=1）44.7%，模型 2（i=2）7.5%，模型 3（i=3）3.5%，其中模型 3 与条件因子模型持平。
- **表示质量不等同于优化难度**：尽管所有模型训练 loss 均稳定收敛，但下游 WER 仍存在显著差异，说明低训练损失不保证中间表示适合下游重建。
- **自回归误差积累是主要瓶颈**：完整框架在教师强制下达到 4.6% WER，但在完全自回归下飙升至 125.3%，表明性能退化主要源于序列生成时的误差传播，而非表示本身的信息不足。

### 7. 优点
- **框架的系统性**：提出可通用的“表示选择影响研究”框架，将表示预测和重建解耦，便于更换不同的生成模型、token 化方法和预测架构。
- **组件隔离分析**：通过教师强制分别评估条件因子和潜在模型，清晰揭示了性能瓶颈所在，避免了混叠误差。
- **量化扩散时间步的影响**：首次在神经解码场景下量化了扩散模型中不同去噪阶段潜在表示的“可学性”和“重建保真度”，对后续表示选择有指导意义。

### 8. 不足与局限
- **实验覆盖范围窄**：仅基于单受试者、单种神经记录、单种扩散模型和声码器，结论泛化性有待在其他受试者、任务（如图像解码）和模型上验证。
- **方法对比缺失**：未将扩散潜在表示与其他常用的中间表示（如 Mel 谱图、自编码器瓶颈特征）进行直接比较，难以证明扩散表示具有相对优势。
- **自回归生成脆弱性**：完全自回归下性能崩溃，说明当前简单的自回归解码器无法有效应对长序列的累积误差，限制了该框架在实时神经假体中的应用。
- **训练细节不完整**：未说明具体训练耗时，以及不同扩散时间步下所需解码步数的计算开销差异。

（完）
