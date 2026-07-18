---
title: Evidence of predictive information compression in latent space in humans during speech listening
title_zh: 人类言语聆听中潜在空间预测信息压缩的证据
authors: "Corsini, A., Schneider, S., Tomassini, A., Pedani, L., Fadiga, L., D'Ausilio, A."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738305v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 潜在空间中的预测信息压缩
tldr: 研究通过比较三类言语处理模型（最优压缩、预测性重构和潜在空间预测信息表征）与脑电图活动及行为表现的关系，探讨了言语感知的神经计算原理。结果发现，只有潜在空间预测信息模型既能解释神经活动又能预测行为，表明大脑在言语聆听中优先编码预测信息，而非简单压缩输入或预测重构。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 1277, \"height\": 1098}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 1274, \"height\": 857}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 1273, \"height\": 890}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-004.webp\", \"caption\": \"\", \"page\": 9, \"index\": 4, \"width\": 1271, \"height\": 1194}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-005.webp\", \"caption\": \"\", \"page\": 23, \"index\": 5, \"width\": 1276, \"height\": 1018}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-006.webp\", \"caption\": \"\", \"page\": 24, \"index\": 6, \"width\": 1273, \"height\": 1248}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-007.webp\", \"caption\": \"\", \"page\": 25, \"index\": 7, \"width\": 1270, \"height\": 781}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-008.webp\", \"caption\": \"\", \"page\": 26, \"index\": 8, \"width\": 1270, \"height\": 583}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738305-v1/fig-009.webp\", \"caption\": \"\", \"page\": 27, \"index\": 9, \"width\": 1276, \"height\": 1158}]"
motivation: 探究言语感知的神经计算原理，以区分高效压缩与预测编码假说。
method: 构建自编码器压缩、预测自编码器重构和对比学习潜在预测三种模型，将其表征与听言语时的脑电图数据拟合，并检验对行为表现的预测力。
result: 潜在空间预测信息模型最匹配神经信号，且唯有该模型能显著预测行为表现。
conclusion: 人脑在言语聆听中于潜在空间选择性压缩预测信息，支持预测性信息表征理论。
---

## 摘要
言语感知需要将声学输入转化为支持语言理解的神经表征，但其底层计算原理仍不清楚。经典有效编码理论主张对感觉输入进行最优压缩，而替代性解释则认为神经系统优先编码支持预测的信息。一个关键未决问题是这种预测编码是作用于固定输入还是灵活的内部表征。我们实例化了三种言语处理假设模型：(i) 使用深度自编码器的最优压缩，(ii) 使用预测自编码器的预测重建，以及 (iii) 使用对比学习在潜在空间进行预测的信息表征。我们将得到的言语潜在表征与言语聆听期间的脑电图(EEG)活动进行比较。在预测信息目标下学习的表征最能解释神经潜在变量。关键的是，只有选择性压缩预测信息的表征才能预测行为表现，这表明神经言语表征的结构是在潜在空间中对预测信息进行编码，而非最大化压缩或输入预测。

## Abstract
Speech perception requires transforming acoustic input into neural representations that support linguistic understanding, yet its underlying computational principles remain unclear. Classical efficient coding theories posit optimal compression of sensory input, whereas alternative accounts propose that neural systems preferentially encode information that supports prediction. A key open question is whether such predictive encoding operates on fixed inputs or on flexible internal representations. We instantiated three hypothesis models of speech processing: (i) optimal compression with deep autoencoders, (ii) predictive reconstruction with predictive autoencoders, and (iii) predictive information representation via latent-space prediction using contrastive learning. We compared resulting speech latent representations to electroencephalographic (EEG) activity during speech listening. Representations learned under the predictive information objective best explained neural latents. Crucially, only representations that selectively compressed predictive information predicted behavioral performance, suggesting that neural speech representations are structured to encode predictive information in latent space rather than to maximize compression or input prediction.