---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
title_zh: 表征几何作为连接组约束网络的保真度度量：来自果蝇视觉系统的证据
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 提出表征几何作为神经网络生物保真度度量
tldr: 本研究针对仅靠行为输出无法判断神经网络是否真正具备生物保真度的问题，提出表征几何学作为度量内部表征生物相似性的指标。通过分析果蝇视觉系统的连接组约束网络与随机对照，发现连接组约束网络产生平滑的圆形方向几何，与生物数据高度匹配，显著优于随机网络，且未训练时亦存在几何先验，表明表征几何学可有效区分生物与任意连接，为连接组仿真提供实用保真度度量。
source: biorxiv
selection_source: fresh_fetch
motivation: 需要一种不依赖行为解码、能区分真实生物连接与任意连接的表征级保真度度量。
method: 对果蝇视觉系统连接组约束网络集与稳定性受限的随机基线，采用表征相似性分析和中心核对齐，比较其表征几何并与生物T4/T5方向调谐数据对比。
result: 连接组约束网络呈现平滑圆形方向几何，与生物数据匹配度(r=0.930)远高于随机网络(r=0.603)，且未训练连接组即具几何先验，训练后进一步增强。
conclusion: 表征几何学可作为有效保真度度量，能鉴定内部表征是否源于真实生物连接，为连接组规模仿真提供评估手段。
---

## 摘要
生物连接到底为神经计算贡献了什么？行为实验可以测试模型是否产生正确的输出，但无法确定其内部表征是否在生物学上忠实。Brunton等人（2026）将这一点具体化：一个用深度强化学习训练的秀丽隐杆线虫连接组模型，产生了逼真的果蝇行走行为——然而该模型在生物学上毫无意义，因为行为保真度可以在没有生物保真度的情况下实现。我们需要一个人群层面的度量标准，能够区分真实的生物连接和任意连接，而不需要行为解码器。

我们提出将表征几何作为这一度量标准。表征几何——即不同刺激引起的人群反应之间的成对距离结构——捕捉了神经回路如何组织其表征空间，而不依赖于它驱动何种行为。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于Flyvis预训练的果蝇视觉系统集成（Lappalainen等人，2024）：50个架构固定为Flyvis连接组（从部分电子显微镜来源重建）的网络，与受稳定性约束的随机基线（符号保持的权重洗牌，并经过拒绝采样以确保动态稳定性，n=50）进行比较。

连接组约束的网络产生了一个平滑的圆形方向几何，而随机网络无法复制：对于ON边缘刺激，RSA斯皮尔曼相关系数r=0.686（p<0.0001），对于ON+OFF边缘刺激，r=0.846（p<0.0001），CKA结果也证实了这一点（两个实验中p<0.05）。该几何也追踪了在活体果蝇中记录的生物T4/T5方向调谐（Maisak等人，2013）：连接组约束几何比随机几何更匹配生物学（r=0.930对比r=0.603，差距Δr=0.327，p<0.0001）。在每个刺激极性内，ON通路编码方向时的几何分离比OFF通路更强（Δr=0.138，95%置信区间[0.091, 0.236]）；我们将此报告为模型集成表征的一个属性，而非已确立的生物学差异：Maisak等人（2013）发现T4和T5在功能上除对比极性外是等效的。为了排除训练混杂因素，我们比较了未训练的网络与洗牌基线：在任何任务训练之前，连接组先验在集成层面上塑造了方向几何（r=0.260, p=0.041和r=0.215, p=0.048；均为边际显著性，未经多重比较校正），这表明连接编码了一种几何先验，训练将其放大。

这些结果确立了表征几何作为一种候选保真度度量，仅使用对结构化刺激集的人群反应即可区分生物连接和任意连接，并为接近哺乳动物皮层尺度的连接组仿真提供了一条通往保真度度量的实用路径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder.

We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. (2024)): 50 networks whose architecture is fixed to the Flyvis connectome (reconstructed from partial electron-microscopy sources), compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]); we report this as a property of the model ensembles representations rather than an established biological difference: Maisak et al. (2013) find T4 and T5 functionally equivalent except in contrast polarity. To address the training confound, we compared untrained networks against shuffled baselines: the connectome prior shapes directional geometry at the ensemble level before any task training (r = 0.260, p = 0.041 and r = 0.215, p = 0.048; both marginal, uncorrected), suggesting wiring encodes a geometric prior that training amplifies.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring using only population responses to a structured stimulus set, and suggest a practical path toward fidelity metrics for connectome-scale emulations approaching mammalian cortex.