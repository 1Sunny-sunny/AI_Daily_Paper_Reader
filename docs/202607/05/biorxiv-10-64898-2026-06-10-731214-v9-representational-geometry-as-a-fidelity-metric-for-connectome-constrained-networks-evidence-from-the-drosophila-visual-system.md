---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
title_zh: 表征几何作为连接组约束网络的保真度指标：来自果蝇视觉系统的证据
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v9.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 表征几何作为神经编码保真度度量
tldr: 神经网络模型的行为逼真不等于内部表征的生物学真实性，需要不依赖行为解码器的群体水平度量。本文提出表征几何——群体响应对刺激的距离结构——作为保真度指标，并在果蝇视觉系统中验证：固定于真实连接组的网络产生平滑圆形方向几何，随机打乱权重的网络无法重现，且该几何与活体测得的方向调谐高度匹配（r=0.930），未训练网络也显示连线先验。结果为连接组规模仿真提供了可操作的保真度评估方法。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有行为测试无法判断模型内部表征是否生物学真实，需一种不依赖行为解码器的群体水平度量。
method: 对果蝇视觉系统连接组约束网络和随机打乱权重的基线网络，用表征相似性分析和中心核对齐比较群体响应几何，并与生物T4/T5方向调谐数据对比。
result: 连接组网络产生独特的平滑圆形方向几何，其与生物调谐的相关性（r=0.930）显著高于随机网络（r=0.603），且未训练网络已携带几何先验。
conclusion: 表征几何能有效区分生物连线与随机连线，可作为连接组尺度神经仿真保真度的候选度量。
---

## 摘要
生物连接实际上对神经计算有何贡献？行为实验可以测试模型是否产生正确的输出，但无法确定其内部表征在生物学上是否忠实。Brunton等人（2026）将这一点具体化：用深度强化学习训练的秀丽隐杆线虫连接组能产生逼真的果蝇行走——然而该模型在生物学上是无意义的，因为行为保真度可以在没有生物保真的情况下实现。我们需要一个人群层次的度量标准，能够区分真实的生物连接与任意连接，而无需行为解码器。我们提出以表征几何作为该度量标准。表征几何——群体对不同刺激反应之间的成对距离结构——捕获了神经回路如何组织其表征空间，独立于它所驱动的行为。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于Flyvis预训练的果蝇视觉系统集成（Lappalainen等人，2024）：50个网络，其架构固定为Flyvis连接组（通过部分电子显微镜来源重建），并与稳定性约束的随机基线进行比较（符号保留权重洗牌，为动态稳定性进行拒绝采样，n=50）。连接组约束的网络产生了随机网络无法复制的平滑圆形方向几何：对于ON边缘刺激，RSA Spearman r=0.686（p<0.0001），对于ON+OFF边缘刺激，r=0.846（p<0.0001），并由CKA证实（两个实验中p<0.05）。该几何还追踪了活体果蝇中记录到的生物T4/T5方向调谐（Maisak等人，2013）：连接组约束的几何与生物学的匹配度显著优于随机几何（r=0.930 vs. r=0.603，差距Δr=0.327，p<0.0001）。在每个刺激极性内，ON通路编码方向时具有比OFF通路更强的几何分离（Δr=0.138，95% CI [0.091, 0.236]）；我们将此报告为模型集成表征的特性，而非已确立的生物学差异：Maisak等人（2013）发现T4和T5除了对比极性外功能上是等效的。为解决训练混淆，我们将未训练的网络与打乱的基线进行了比较：连接组先验在任何任务训练之前，就在集成层面塑造了方向几何（r=0.260，p=0.041和r=0.215，p=0.048；两者均边缘显著，未校正），表明连接编码了一个几何先验，训练将其放大。这些结果确立了表征几何作为一个候选保真度指标，仅使用群体对结构化刺激集的反应就能区分生物连接与任意连接，并为接近哺乳动物皮层尺度的连接组仿真提供了一条通往保真度指标的实用路径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder. We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. (2024)): 50 networks whose architecture is fixed to the Flyvis connectome (reconstructed from partial electron-microscopy sources), compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {triangleup}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({triangleup}r = 0.138, 95% CI [0.091, 0.236]); we report this as a property of the model ensembles representations rather than an established biological difference: Maisak et al. (2013) find T4 and T5 functionally equivalent except in contrast polarity. To address the training confound, we compared untrained networks against shuffled baselines: the connectome prior shapes directional geometry at the ensemble level before any task training (r = 0.260, p = 0.041 and r = 0.215, p = 0.048; both marginal, uncorrected), suggesting wiring encodes a geometric prior that training amplifies.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring using only population responses to a structured stimulus set, and suggest a practical path toward fidelity metrics for connectome-scale emulations approaching mammalian cortex.