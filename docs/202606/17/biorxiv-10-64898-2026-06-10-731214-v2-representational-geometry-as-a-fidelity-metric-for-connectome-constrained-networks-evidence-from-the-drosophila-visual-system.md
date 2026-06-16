---
title: "Representational geometry as a fidelity metric for connectome-constrained networks: evidence from the Drosophila visual system"
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-13
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 表征几何作为神经模型生物保真度度量
tldr: 本文提出表征几何作为连接组约束网络的保真度度量，以解决行为测试无法区分生物连接与任意连接的问题。通过对果蝇视觉系统连接组约束网络与随机基线的表征相似性分析，发现前者产生与生物方向调谐高度匹配的平滑几何，证实该群体级度量无需行为解码器即可判别生物保真度，为连接组仿真扩展至哺乳动物皮层提供了可行路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 需要一种群体级度量来区分生物连接和任意连接，而不依赖行为解码器。
method: 对Flyvis果蝇视觉系统连接组约束网络应用RSA和CKA，与稳定性约束的随机网络进行比较。
result: 连接组约束网络生成平滑圆形方向几何，与活体T4/T5调谐相关达r=0.930，显著优于随机网络（r=0.603）。
conclusion: 表征几何能有效判别连接组的生物保真度，为可扩展的连接组仿真验证框架奠定基础。
---

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder. We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. 2024): 50 networks whose architecture is fixed to the FlyWire connectome, compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50).

Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]), consistent with known T4/T5 asymmetries in direction selectivity strength.

These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring at the population level. The framework requires no behavioral decoder and no single-unit recordings--only population responses to a structured stimulus set -- suggesting a practical path toward verifiable fidelity metrics for connectome-scale emulations as they scale toward mammalian cortex.