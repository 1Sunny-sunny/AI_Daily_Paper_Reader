---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
title_zh: 表征几何作为连接组约束网络的保真度指标：来自果蝇视觉系统的证据
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-24
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v5.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 表征几何作为生物网络保真度度量
tldr: 神经连接组对计算的实际贡献尚不明确，仅靠行为保真可能掩盖生物失真的内部表征。本文提出表征几何学作为群体级保真度度量，在果蝇视觉系统中通过比较连接组约束网络与随机网络的群体响应几何，发现连接组网络呈现与生物T4/T5方向调谐高度一致的平滑圆形几何，且训练前已存在方向几何先验，证明表征几何学能有效区分生物与任意布线，为连接组尺度模拟提供新指标。
source: biorxiv
selection_source: fresh_fetch
motivation: 当前缺乏仅凭群体响应即可区分生物真实连接与任意连接的群体级度量，行为输出相似并不能保证内部表征的生物保真。
method: 对连接组约束的Flyvis网络和稳定性约束的随机网络施加定向边缘刺激，利用表征相似性分析(RSA)和中心核对齐(CKA)量化群体响应几何，并与生物T4/T5记录对比。
result: 连接组网络的方向几何与生物数据相关度达r=0.930，显著高于随机网络的r=0.603；未训练网络中已存在方向几何先验，训练会放大该倾向。
conclusion: 表征几何学可作为区分生物与任意布线的有效保真度量，为构建高保真连接组尺度神经模拟提供了可行路径。
---

## 摘要
生物连接究竟对神经计算有何贡献？行为实验可以检验模型是否产生正确的输出，但无法确定其内部表征是否在生物学上忠实。Brunton 等人（2026）将这一点具体化：一个用深度强化学习训练的秀丽隐杆线虫连接组产生了逼真的果蝇行走行为——然而该模型在生物学上毫无意义，因为行为保真度可以在没有生物学保真度的情况下实现。我们需要一个群体水平的指标，能够区分真正的生物连接与任意连接，而无需求助于行为解码器。

我们提出将表征几何作为这一指标。表征几何——即不同刺激引发的群体反应之间的成对距离结构——刻画了神经回路如何组织其表征空间，而独立于它所驱动的行为。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于 Flyvis 预训练的果蝇视觉系统集成（Lappalainen 等人，2024）：50 个网络，其架构固定为 Flyvis 连接组（由部分电子显微镜来源重建），并与稳定性约束的随机基线（符号保持的权重打乱，经拒绝采样以满足动态稳定性，n = 50）进行比较。

连接组约束网络产生了一种平滑的圆形方向几何，随机网络无法复现：对于 ON 边缘刺激，RSA Spearman r = 0.686（p < 0.0001）；对于 ON+OFF 边缘刺激，r = 0.846（p < 0.0001），这一结果得到 CKA 的佐证（两项实验中 p < 0.05）。该几何还追踪了在活体果蝇中记录到的生物 T4/T5 方向调谐（Maisak 等人，2013）：连接组约束几何与生物几何的匹配程度远优于随机几何（r = 0.930 vs. r = 0.603，差距 Δr = 0.327，p < 0.0001）。在每个刺激极性内，ON 通路对方向的编码在几何上比 OFF 通路有更强的分离（Δr = 0.138，95% CI [0.091, 0.236]）；我们将此报告为模型集成表征的一种属性，而非已确立的生物学差异：Maisak 等人（2013）发现 T4 和 T5 除对比极性外在功能上等效。为解决训练带来的混淆，我们将未训练网络与打乱基线进行比较：在任何任务训练之前，连接组先验在集成水平上塑造了方向几何（r = 0.260，p = 0.041；r = 0.215，p = 0.048；均为边际显著，未经校正），这表明连接编码了一种几何先验，而训练将其放大。

这些结果确立了表征几何作为一种候选保真度指标，仅利用群体对结构化刺激集的响应即可区分生物连接与任意连接，并为逼近哺乳动物皮层规模的连接组仿真提供了一条通往保真度指标的实用路径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder.

We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. (2024)): 50 networks whose architecture is fixed to the Flyvis connectome (reconstructed from partial electron-microscopy sources), compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]); we report this as a property of the model ensembles representations rather than an established biological difference: Maisak et al. (2013) find T4 and T5 functionally equivalent except in contrast polarity. To address the training confound, we compared untrained networks against shuffled baselines: the connectome prior shapes directional geometry at the ensemble level before any task training (r = 0.260, p = 0.041 and r = 0.215, p = 0.048; both marginal, uncorrected), suggesting wiring encodes a geometric prior that training amplifies.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring using only population responses to a structured stimulus set, and suggest a practical path toward fidelity metrics for connectome-scale emulations approaching mammalian cortex.