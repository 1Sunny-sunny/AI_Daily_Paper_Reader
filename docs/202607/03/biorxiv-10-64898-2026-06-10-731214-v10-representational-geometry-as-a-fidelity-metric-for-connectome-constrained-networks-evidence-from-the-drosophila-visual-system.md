---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
title_zh: 表征几何作为连接组约束网络的保真度度量：来自果蝇视觉系统的证据
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v10.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 表征几何作为连接网络活动与生物布线的度量
tldr: 生物连接组如何贡献神经计算？行为忠实不代表生物忠实，亟需不依赖解码器的群体度量。本文提出表征几何作为忠实度量，对果蝇视觉系统连接组约束模型与随机基线进行RSA/CKA分析，发现连接组网络呈现平滑方向几何并显著匹配生物调谐，且连接组先验于训练前已塑造几何。表征几何可区分生物与任意连接，为连接组仿真提供候选度量。
source: biorxiv
selection_source: fresh_fetch
motivation: 行为忠实不等于生物忠实，需要不依赖行为解码器的群体度量来判别神经回路。
method: 对果蝇视觉系统连接组约束网络与稳定性约束随机网络，计算表征几何（RSA/CKA）并比较方向表示与生物T4/T5调谐。
result: 连接组网络形成平滑方向几何，与生物匹配度显著高于随机网络（r=0.930 vs 0.603），且连接组先验在无训练时即存在。
conclusion: 表征几何可作为仅需群体响应的忠实度量，为大规模脑仿真提供验证工具。
---

## 摘要
生物布线对神经计算到底贡献了什么？行为实验可以测试一个模型是否产生正确的输出，但它们无法确定其内部表征是否在生物学上保真。Brunton等人（2026）将这一点具体化：使用深度强化学习训练的秀丽隐杆线虫连接组产生了逼真的果蝇行走——然而该模型在生物学上毫无意义，因为行为保真度可以在没有生物保真度的情况下实现。我们需要一种群体水平的度量，能够区分真实的生物布线与任意布线，而无需行为解码器。我们提出表征几何作为该度量。表征几何——即对不同刺激的群体反应之间的成对距离结构——捕捉了神经回路如何组织其表征空间，独立于它所驱动的行为。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于Flyvis预训练的黑腹果蝇视觉系统集成（Lappalainen等人，2024）：50个网络，其架构固定为Flyvis连接组（从部分电子显微镜来源重建），与稳定性约束的随机基线（符号保持的权重洗牌，通过动态稳定性拒绝采样，n=50）进行比较。连接组约束的网络产生了随机网络无法复制的平滑圆形方向几何：对于ON边缘刺激，RSA Spearman r=0.686（p<0.0001），对于ON+OFF边缘刺激，r=0.846（p<0.0001），并由CKA（两者p<0.05）证实。该几何还追踪了在活体果蝇中记录到的生物T4/T5方向调谐（Maisak等人，2013）：连接组约束的几何与生物学的匹配显著优于随机几何（r=0.930 vs. r=0.603，差距Δr=0.327，p<0.0001）。在每个刺激极性内，ON通路编码方向时的几何分离强于OFF通路（Δr=0.138，95% CI [0.091, 0.236]）；我们将此报告为模型集成表征的一个属性，而非已确立的生物学差异：Maisak等人（2013）发现T4和T5除了对比极性外功能等效。为了解决训练混淆，我们将未训练的网络与洗牌基线进行比较：在任何任务训练之前，连接组先验在集成水平上塑造了方向几何（r=0.260，p=0.041和r=0.215，p=0.048；两者均为边际的，未校正），这表明布线编码了一个几何先验，而训练将其放大。这些结果确立了表征几何作为一种候选保真度度量，它仅使用对结构化刺激集的群体反应就能区分生物布线与任意布线，并提出了一条通往接近哺乳动物皮层的连接组尺度模拟的保真度度量的实用途径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder. We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. (2024)): 50 networks whose architecture is fixed to the Flyvis connectome (reconstructed from partial electron-microscopy sources), compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]); we report this as a property of the model ensembles representations rather than an established biological difference: Maisak et al. (2013) find T4 and T5 functionally equivalent except in contrast polarity. To address the training confound, we compared untrained networks against shuffled baselines: the connectome prior shapes directional geometry at the ensemble level before any task training (r = 0.260, p = 0.041 and r = 0.215, p = 0.048; both marginal, uncorrected), suggesting wiring encodes a geometric prior that training amplifies.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring using only population responses to a structured stimulus set, and suggest a practical path toward fidelity metrics for connectome-scale emulations approaching mammalian cortex.