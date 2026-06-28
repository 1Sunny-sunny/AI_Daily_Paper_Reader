---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
title_zh: 表征几何作为连接组约束网络的保真度指标：来自果蝇视觉系统的证据
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v6.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 表征几何作为生物网络保真度度量
tldr: 连接组对神经计算的实际贡献尚不明确，因行为保真度不等于生物保真度。本研究提出表征几何学作为候选度量，通过对果蝇视觉系统连接组约束网络与随机网络进行表征相似性分析，发现连接组网络呈现平滑的圆形方向几何，且与生物神经元调谐高度匹配，即使未训练网络也具备几何先验，表明表征几何学能有效区分生物与任意线路。
source: biorxiv
selection_source: fresh_fetch
motivation: 仅有行为保真度无法保证模型的生物忠实性，需开发基于群体表征的指标来判别真实生物连接。
method: 使用表征相似性分析(RSA)和中心核对齐(CKA)，比较果蝇视觉系统连接组约束网络与稳定性随机网络的表征几何。
result: 连接组网络产生独特的圆形方向几何，与生物T4/T5方向调谐高度一致(r=0.930)，且ON通路几何分离强于OFF通路，未训练网络即展现几何先验。
conclusion: 表征几何学可作为区分生物与任意连接的有效保真度指标，为连接组规模仿真提供新路径。
---

## 摘要
生物连接对神经计算的真正贡献是什么？行为实验可以测试模型是否产生正确的输出，但无法确定其内部表征是否在生物学上忠实。Brunton等人（2026）将这一问题具体化：一个用深度强化学习训练的秀丽隐杆线虫连接组产生了逼真的果蝇行走行为——然而该模型在生物学上毫无意义，因为行为保真度可以在没有生物保真度的情况下实现。我们需要一种群体水平的指标，能够区分真实的生物连接和任意连接，而不需要行为解码器。

我们提出将表征几何作为这一指标。表征几何——对不同刺激的群体反应之间的成对距离结构——捕捉了神经回路如何组织其表征空间，而与它驱动何种行为无关。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于Flyvis预训练的黑腹果蝇视觉系统集成模型（Lappalainen等人，2024）：50个网络，其架构固定于Flyvis连接组（由部分电子显微镜来源重建），并与受稳定性约束的随机基线（保号权重打乱，并通过动力学稳定性拒绝采样，n=50）进行比较。

连接组约束的网络产生了一种平滑的圆形方向几何结构，而随机网络无法复制：对于ON边缘刺激，RSA Spearman r = 0.686（p < 0.0001）；对于ON+OFF边缘刺激，r = 0.846（p < 0.0001），并得到CKA的验证（两者实验中p < 0.05）。该几何结构还追踪了在活体果蝇中记录的生物T4/T5方向调谐（Maisak等人，2013）：连接组约束的几何结构与生物数据的匹配程度显著优于随机几何结构（r = 0.930 vs. r = 0.603，差值Δr = 0.327，p < 0.0001）。在每个刺激极性内，ON通路编码方向的几何分离比OFF通路更强（Δr = 0.138，95% CI [0.091, 0.236]）；我们报告这是模型集成表征的一个属性，而不是已确立的生物学差异：Maisak等人（2013）发现T4和T5在除了对比度极性之外的功能上等价。为了解决训练带来的混淆，我们将未经训练的网络与打乱基线进行比较：在集成水平上，连接组先验在任何任务训练之前就已经塑造了方向几何结构（r = 0.260, p = 0.041 和 r = 0.215, p = 0.048；两者均为边缘显著，未经校正），这表明连接编码了一种几何先验，而训练将其放大。

这些结果确立了表征几何作为一个候选保真度指标，它仅使用对结构化刺激集的群体反应就能区分生物连接和任意连接，并为接近哺乳动物皮层的连接组规模仿真的保真度指标提供了一条实用路径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder.

We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. (2024)): 50 networks whose architecture is fixed to the Flyvis connectome (reconstructed from partial electron-microscopy sources), compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]); we report this as a property of the model ensembles representations rather than an established biological difference: Maisak et al. (2013) find T4 and T5 functionally equivalent except in contrast polarity. To address the training confound, we compared untrained networks against shuffled baselines: the connectome prior shapes directional geometry at the ensemble level before any task training (r = 0.260, p = 0.041 and r = 0.215, p = 0.048; both marginal, uncorrected), suggesting wiring encodes a geometric prior that training amplifies.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring using only population responses to a structured stimulus set, and suggest a practical path toward fidelity metrics for connectome-scale emulations approaching mammalian cortex.