---
title: Connectome wiring shapes population-level neural geometry in the Drosophila visual system
title_zh: 连接组布线塑造果蝇视觉系统中的群体神经几何
authors: "Zhou, M. G., Hasler, J. O."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731214v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 果蝇视觉系统中的群体神经几何结构
tldr: 本研究探讨生物连接组对神经计算的贡献，提出采用表征几何学作为衡量群体级神经表征保真度的新指标。通过对比基于真实果蝇视觉连接组（FlyWire）和随机重连的网络，发现连接组约束的网络形成平滑的方向选择几何结构，且与活体记录的T4/T5神经元方向调谐高度一致，随机网络无法复现。该框架无需行为解码器或单细胞记录，为连接组规模模拟提供了一种可验证的保真度度量。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基于行为输出的验证无法保证模型内部表征的生物真实性，亟需能区分真实与任意连接组的群体级度量。
method: 对固定于FlyWire连接组架构的50个网络与稳定性约束的随机对照网络，使用表征相似性分析和中心核对齐比较群体响应的几何结构。
result: 连接组网络产生了随机网络无法复制的平滑圆形方向几何，并与活体T4/T5方向调谐高度匹配（r=0.930），同时揭示了ON通路比OFF通路有更强的方向几何分离。
conclusion: 表征几何学能有效区分生物与任意连接组，可作为连接组模拟的群体级保真度度量，无需依赖行为解码器，为未来大规模模拟提供验证路径。
---

## 摘要
生物连接究竟对神经计算有何贡献？行为实验可以检验模型是否产生正确输出，但无法确定其内部表征是否在生物学上忠实。Brunton 等人（2026）将此具体化：用深度强化学习训练的一个线虫连接组，产生了逼真的果蝇行走行为——然而该模型在生物学上毫无意义，因为行为保真度无需生物保真度即可实现。我们需要一种群体水平的度量，能够区分真实的生物连接与任意连接，而不依赖于行为解码器。我们提出表征几何作为该度量。表征几何——群体对不同刺激响应之间的成对距离结构——捕捉了神经回路如何组织其表征空间，独立于它所驱动的行为。我们将表征相似性分析（RSA）和中心核对齐（CKA）应用于 Flyvis 预训练的黑腹果蝇视觉系统集成（Lappalainen 等人，2024）：50个网络，其架构固定为 FlyWire 连接组，与受稳定性约束的随机基线（保持符号的权重打乱，经拒绝采样确保动态稳定性，n = 50）进行比较。连接组约束的网络产生了平滑的圆形方向几何，这是随机网络无法复现的：对于 ON 边缘刺激，RSA Spearman r = 0.686（p < 0.0001），对于 ON+OFF 边缘刺激，r = 0.846（p < 0.0001），CKA 也证实了这一点（两个实验中 p < 0.05）。该几何还追踪了在活体果蝇中记录到的生物 T4/T5 方向调谐（Maisak 等人，2013）：连接组约束的几何与生物学的匹配程度显著优于随机几何（r = 0.930 对比 r = 0.603，差距 Δr = 0.327，p < 0.0001）。在每个刺激极性内，ON 通路编码方向时的几何分离强于 OFF 通路（Δr = 0.138，95% CI [0.091, 0.236]），这与已知的 T4/T5 方向选择性强度不对称性一致。这些结果确立了表征几何作为候选保真度度量，能够在群体水平区分生物连接与任意连接。该框架无需行为解码器，也无需单神经元记录——仅需群体对结构化刺激集的响应——为连接组规模仿真在向哺乳动物皮层扩展时，提供了一条通向可验证保真度度量的可行路径。

## Abstract
What does biological wiring actually contribute to neural computation? Behavioral experiments can test whether a model produces the right outputs, but they cannot determine whether its internal representations are biologically faithful. Brunton et al. (2026) made this concrete: a C. elegans worm connectome trained with deep reinforcement learning produces realistic Drosophila fly walking -- yet the model is biologically meaningless, because behavioral fidelity is achievable without biological fidelity. We need a population-level metric that discriminates real biological wiring from arbitrary wiring, without requiring a behavioral decoder. We propose representational geometry as that metric. Representational geometry -- the structure of pairwise distances between population responses to different stimuli -- captures how a neural circuit organizes its representational space, independently of what behavior it drives. We apply representational similarity analysis (RSA) and centered kernel alignment (CKA) to the Flyvis pretrained Drosophila melanogaster visual system ensemble (Lappalainen et al. 2024): 50 networks whose architecture is fixed to the FlyWire connectome, compared against stability-constrained random baselines (sign-preserving weight shuffles, rejection-sampled for dynamic stability, n = 50). Connectome-constrained networks produce a smooth circular direction geometry that random networks cannot replicate: RSA Spearman r = 0.686 (p < 0.0001) for ON edge stimuli and r = 0.846 (p < 0.0001) for ON+OFF edge stimuli, corroborated by CKA (p < 0.05 in both experiments). The geometry also tracks biological T4/T5 direction tuning recorded in living flies (Maisak et al. 2013): connectome-constrained geometry matches biology substantially better than random geometry (r = 0.930 vs. r = 0.603, gap {Delta}r = 0.327, p < 0.0001). Within each stimulus polarity, the ON pathway encodes direction with stronger geometric separation than the OFF pathway ({Delta}r = 0.138, 95% CI [0.091, 0.236]), consistent with known T4/T5 asymmetries in direction selectivity strength. These results establish representational geometry as a candidate fidelity metric that discriminates biological from arbitrary wiring at the population level. The framework requires no behavioral decoder and no single-unit recordings -- only population responses to a structured stimulus set -- suggesting a practical path toward verifiable fidelity metrics for connectome-scale emulations as they scale toward mammalian cortex.