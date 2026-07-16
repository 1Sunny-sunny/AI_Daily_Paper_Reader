---
title: Generating whole-brain neural activity and behavior through unified latent dynamics
title_zh: 通过统一潜在动力学生成全脑神经活动与行为
authors: "Nuzzi, D., Mattia, M., Pezzulo, G."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.05.730482v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 从潜在动力学生成全脑神经活动和行为
tldr: 为理解高维神经活动与行为如何从共享潜在动力学中涌现，本文提出生成式框架NEBULA，基于线虫全脑记录学习统一潜在动力学，实现长时程神经与行为轨迹生成、真实行为模拟及靶向虚拟干预，揭示了行为相关过渡点并支持无重训练的状态操控，为脑-行为数字孪生和可扩展虚拟实验奠定了基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-001.webp\", \"caption\": \"Figure 1: Characterization of empirical data and virtual kinematic reconstruction. a) Calcium signals recorded in (Kato et al., 2015) for each single neurons (109 rows). b) Trace of the AVA neuron colored according to the behavioral state labelled in (Kato et al., 2015). c) PCA of the neural signals. Only the first three components are shown. Each point is colored by the corresponding behavioral state. The percentage of explained variance is shown near each axis label. d) Postural reconstruction from discrete behavioral states. The bottom plot shows the temporal evolution of the first three postural components (eigenworm amplitudes): first (black), second (blue), and third (red). Shaded regions denote discrete behavioral states over a 25 seconds window. Top panels display representative reconstructed body shapes at t = 10, 220, 500 and 740, with red circles indicating the head position. e) Kymogram of body curvature. Postural dynamics reconstructed from the eigenworm amplitudes over the same period as panel d. The heatmap illustrates the relative angle (radians) between 25 adjacent body segments from head (top) to tail (bottom). Blue and red colors denote dorsal and ventral bending, respectively. f) Simulated spatial trajectory. The path of the worm in the xy-plane reconstructed from the sequence of behavioral states over the full 18-minute recording. The trace is colored by elapsed time (seconds), as indicated by the colorbar.\", \"page\": 4, \"index\": 1, \"width\": 932, \"height\": 957}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-002.webp\", \"caption\": \"Figure 2: Neural and behavioral modeling through NEBULA. a) Encoded latent manifold. The training dataset represented within the three-dimensional latent space of the encoder. Each point is colored according to its ground-truth behavioral label. b) Latent transition rates. Arrows indicate the direction and magnitude (color) of the vector field corresponding to the transition rates, visualized only at points on the manifold from panel a for clarity. c) Encoder standard deviation. Manifold points colored by the standard deviation of the encoder’s output distribution. d) Transition standard deviation. Manifold points colored by the standard deviation of the transition rates. e) Generative rollout. Latent trajectories produced by the transition module over 30000 timesteps within the three-dimensional manifold. Points are colored by the decoded behavioral state. f) Decoded neural activity. Heatmap showing the activity across all neural channels decoded from the generative rollout trajectories over the first 15000 timesteps (≈ 85 minutes). Color indicates simulated activity magnitude.\", \"page\": 6, \"index\": 2, \"width\": 932, \"height\": 858}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-003.webp\", \"caption\": \"Figure 3: Quantitative validation of generated neural and behavioral dynamics. a) Behavioral state frequencies. Comparison between the true distribution of behaviors from the training set and the distribution decoded from the 30000 timesteps generative rollout visualized in Figure 2e. b) Behavioral transition matrices. Comparison of transition probabilities between states in the training data (left) and the decoded generative rollout (right). Values denote non-zero probabilities. c) Functional connectivity matrices. Pairwise linear correlations between all neural channels for the original data (left) and those decoded from the generative rollout (right). d) Correlation between real and generated functional connectivity. Comparison of functional connectivity (computed via pairwise linear correlations) between the original neural timeseries and that decoded from generated latent trajectories. Each point represents a unique pair of neural channels. Black points include all channel pairs, while red points denote a subset of consistent neurons identifiable across all worms (see text and (Kato et al., 2015)). The data for the comparisons are illustrated in the functional connectivity matrices of panel c. e) Stochastic divergent trajectories. Snapshots at four time points (t = 12.5, 25, 37.5, 50 s) showing the spatial dispersal of 500 simulated worms. All simulations begin from the same latent state and spatial origin. The diversity in trajectory and body posture is driven by the stochasticity of the latent transition rates.\", \"page\": 9, \"index\": 3, \"width\": 932, \"height\": 917}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-004.webp\", \"caption\": \"Figure 4: Robustness to latent perturbations and targeted steering of behavioral dynamics. a) Behavioral distribution robustness. KL divergence between the behavioral state frequencies of a baseline (noise-free) generative rollout and those subjected to varying intensities of white Gaussian noise. The red shaded region indicates the standard deviation range associated with the learned transition rates. Error bars represent the standard deviation across 20 independent generative samples per intensity level. b) Functional connectivity robustness. MSE between the functional connectivity matrices of the baseline generative rollout and those generated under varying intensities of latent noise. The red shaded region indicates the standard deviation range natively expressed by the learned transition rates. Error bars represent the standard deviation across 20 independent generative samples per intensity level. c) Behavioral sensitivity to localized noise. KL divergence between the behavioral distributions of a baseline generative rollout and trajectories subjected to localized latent perturbations (σ = 5 within radius 1). Color indicates the discrepancy resulting from noise applied at each manifold location. d) Connectivity sensitivity to localized noise. MSE between functional connectivity matrices of baseline and locally perturbed rollouts. Color maps represent the local impact of noise on the accuracy of decoded neural interactions. e-h) Steering toward ventral turns. Targeted intervention on the transition rates to modulate behavioral priors, specifically to increase the frequency of ventral turns. In panel e, baseline manifold is shown in grey, while the steered trajectory is colored by its decoded behavioral state. White arrows represent the learned steering field vectors (magnitude > 0.05). Panel f shows the behavioral state frequencies, providing a comparison between the distribution of behaviors from the baseline generative rollout and the distribution decoded from the steered generative rollout. Panel g shows the spatial dispersal of simulated worms driven by the steered latent transition rates. All simulations begin from the same latent state and spatial origin. Panel h shows the activity across all neural channels decoded from the steered generative rollout trajectories over 18 minutes. Color indicates simulated activity magnitude. i-l) Steering toward forward and slow locomotion. A second targeted intervention on the transition rates designed to incentivize forward and slow behaviors while suppressing reversals and turns. Panels i through l mirror the data modalities of panels e through h, respectively illustrating the steered latent manifold, the corresponding shift in behavioral state frequencies, the resulting spatial dispersal of simulated worms, and the decoded neural activity under this alternative steering policy.\", \"page\": 11, \"index\": 4, \"width\": 979, \"height\": 672}]"
motivation: 解决高维神经活动与行为如何从共享潜在动力学中涌现这一根本挑战，以构建可预测多尺度脑-行为动态的数字孪生。
method: 提出NEBULA框架，利用线虫全脑记录联合学习神经与行为的统一潜在动力学结构。
result: 模型能生成长时程真实神经与行为轨迹，虚拟干预揭示行为过渡点并实现无需重训练的神经与行为状态操控。
conclusion: 该工作建立了连接脑动力学与行为的框架，为神经科学的可扩展虚拟实验提供了新范式。
---

## 摘要
理解高维神经活动与行为如何从共享的底层动力学中涌现，仍然是神经科学的一个根本挑战。解决这一问题对于构建能够忠实再现和预测生命系统多尺度脑-行为动力学的数字孪生至关重要。在此，我们提出 NEBULA（通过统一潜在动力学进行神经与行为建模），一个联合建模全脑神经活动与行为的生成框架。利用线虫的全脑记录，该模型学习到一个统一的潜在动力学结构，能够支持神经和行为轨迹的长时程生成、逼真的行为模拟以及有针对性的虚拟干预。对所学动力学的扰动揭示了与行为相关的转换点，而引导干预则能够在不重新训练的情况下实现对神经和行为状态的受控操纵。这些结果建立了一个将大脑动力学与活体生物行为联系起来的框架，并为神经科学的可扩展虚拟实验奠定了基础。

## Abstract
Understanding how high-dimensional neural activity and behavior emerge from shared underlying dynamics remains a fundamental challenge in neuroscience. Addressing this problem is key to enabling digital twins that can faithfully reproduce and predict the multiscale brain-behavior dynamics of living systems. Here we present NEBULA (NEural and Behavioral modeling through Unified LAtent dynamics), a generative framework that jointly models whole-brain neural activity and behavior. Using brain-wide recordings from C. elegans, the model learns a unified latent dynamical structure that supports long-horizon generation of neural and behavioral trajectories, realistic simulations of behavior, and targeted virtual interventions. Perturbations of the learned dynamics reveal behaviorally relevant transition points, whereas steering interventions enable controlled manipulation of neural and behavioral states without retraining. These results establish a framework for linking brain dynamics to behavior in a living organism and provide a foundation for scalable virtual experimentation in neuroscience.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：大脑如何从高维神经活动中产生丰富的行为？揭示神经活动与行为共享的底层动力学是神经科学的一项根本挑战。理解这种涌现机制对构建能够预测多尺度脑–行为动态的数字孪生至关重要。
- **整体含义**：本文旨在构建一个统一的生成框架，从线虫全脑记录中同时学习神经活动与行为的潜在动力学，从而能够生成长时间、逼真的神经和行为轨迹，并支持虚拟干预实验，为神经科学中的可扩展虚拟实验奠定基础。

### 2. 论文提出的方法论
- **框架名称**：NEBULA（NEural and Behavioral modeling through Unified LAtent dynamics）
- **核心思想**：
  - 通过一个统一潜在空间，将高维神经活动（钙成像信号）和离散行为状态（如前进、转向等）映射到低维连续流形。
  - 在该潜在空间中学习一个概率动力系统（过渡模块），刻画状态演化的向量场。
  - 从潜在轨迹解码出神经活动和行为，实现神经–行为的闭环生成。
- **关键技术细节**（基于图和摘要推断）：
  - **编码器**：将原始神经和行为数据映射到潜在变量 $z$ 的分布 $q(z|x)$，其标准差体现编码不确定性。
  - **过渡模块**：建模潜在状态间的转移率，形成向量场 $f(z)$，支持随机微分方程式的推演；转移过程带有可学习的标准差，赋予生成多样性。
  - **解码器**：从潜在状态 $z$ 重建神经活动和行为标签 $p(x|z)$，包括神经发放序列和离散行为分类。
  - 训练目标极可能结合了重建损失（神经与行为）以及潜在动力学的正则化（如变分下界或对比散度），从而保证潜在空间既紧凑又能捕捉时序结构。
- **干预方式**：
  - **无重训练干预**：通过对潜在过渡率施加外部引导场（steering field），直接操纵行为偏好（如增加“腹转弯”频率），无需重新训练网络。

### 3. 实验设计
- **数据集**：
  - 线虫（C. elegans）全脑钙成像记录，来自 Kato et al., 2015。
  - 包含 109 个神经元的信号，以及人工标注的行为离散状态（如前进、后退、转弯等）。
  - 同时从行为状态重建了线虫的姿态（特征蠕虫振幅）和二维运动轨迹。
- **基准与评价指标**：
  - **行为分布匹配**：生成行为的状态频率与真实训练集分布的 KL 散度。
  - **行为转换矩阵**：比较生成轨迹与真实数据的状态转移概率。
  - **功能连接矩阵**：计算所有神经元对之间的线性相关系数，比较生成数据与真实数据矩阵的一致性，并计算逐对通道的相关性。
- **对比方法**：
  - 文内未提及与其他现有模型（如 LEADS、LFADS 等）的定量对比，主要通过生成质量与真实统计量的吻合度来验证。
- **实验操控**：
  - **噪声扰动**：在潜在状态或过渡率上施加不同强度的白噪声或局部噪声，测量行为分布和功能连接的变化。
  - **靶向引导**：设计两种引导策略：（i）增加“腹转弯”行为频率；（ii）促进缓慢前向运动并抑制后退和转弯。通过修改向量场实现，无需重新训练。

### 4. 资源与算力
- 论文提供的摘要及元数据中**未明确提及**所用 GPU 型号、数量、训练时长等算力信息。从实验规模（单个线虫数据集，较短时间内完成 30 000 步生成）推测，训练可以在普通单 GPU 工作站完成，但缺乏具体佐证。

### 5. 实验数量与充分性
- **主要实验组数**：
  - 长时程生成评估（1 组，30 000 步，约 85 分钟）。
  - 行为分布、转移矩阵、功能连接与真实数据对比（3 项定量分析）。
  - 噪声鲁棒性测试（多个噪声强度，每个强度 20 次独立采样；计算 KL 和 MSE）。
  - 局部扰动敏感性分析（在流形不同位置施加固定强度噪声，绘制 KL 和 MSE 地形图）。
  - 靶向引导实验（2 种行为策略，每种展示潜空间轨迹、行为频率、空间疏散、解码神经活动）。
- **充分性与公平性**：
  - 验证覆盖较全面，同时评估了潜在动力学、行为模拟和神经连接保持。
  - 缺乏与其他生成模型或动力学模型的横向比较，也未见消融研究（如去掉行为模态、只用神经数据的基线），因此方法的相对优势未被充分证明。
  - 仅在单一线虫个体数据上测试，样本多样性不足。

### 6. 论文的主要结论与发现
- NEBULA 框架能够从全脑记录中学习出统一的潜在动力学，忠实复现长时间神经活动与行为轨迹。
- 生成的行为统计量（频率、转移矩阵、功能连接）与真实数据高度吻合。
- 对潜在动力学的扰动揭示了与行为转换相关的关键区域，表明潜在流形的结构直接编码了行为决策边界。
- 通过引导过渡向量场，可在不重训的情况下精确调控合成生物的行为偏好与神经状态，验证了模型作为“虚拟实验平台”的潜力。
- 整体上，该工作搭建了从脑动力学到活体行为连接的桥梁，为构建脑–行为数字孪生和快速、低成本的虚拟实验提供了基础。

### 7. 优点
- **统一联合建模**：将神经与行为整合到单一概率动力学框架，避免了传统两步法中信息的割裂。
- **端到端长时程生成**：潜在动力学支持超过 85 分钟的自洽推演，远超诸多已有模型。
- **虚拟干预能力**：无需重训练即可施加外部引导，模拟靶向神经调控后果，提供了一种计算神经行为学的新工具。
- **可解释的潜在结构**：过渡率的几何结构与行为的转换边界相关联，增强了生物学可解释性。
- **多模态输出**：同时生成全脑神经活动、离散行为状态、连续姿态和空间轨迹，覆盖了从微观到宏观的表征。

### 8. 不足与局限
- **数据与泛化局限**：仅测试一条线虫的全脑记录，样本量和个体差异性均未被检验，推广到其他个体或物种的能力未知。
- **比较基准缺失**：未与流行的神经动力学模型（如 LFADS、autoregressive 隐变量模型等）或纯行为生成模型进行比较，难以判断增量优势。
- **行为离散化假设**：使用人工标注的离散状态而非从运动原语联合学习，可能简化了真实行为连续谱。
- **虚拟干预缺少生物学验证**：引导实验仅在模型内进行，没有对应的真实光遗传或扰动实验来佐证模型预测。
- **细节信息不足**：网络架构、损失函数的具体形式、训练超参数均未在摘要/元数据中披露，再现性和透明度受限；算力要求也不明确。
- **潜在可解释性仍有限**：虽然展示了过渡率场与行为的对应，但并未深入解释单个神经元或回路层面的贡献。

（完）
