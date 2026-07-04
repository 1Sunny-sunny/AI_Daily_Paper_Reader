---
title: Machine learning on magnetoencephalography data yields generalizable low-dimensional neural fingerprints that distinguish individuals across task conditions
title_zh: 基于脑磁图数据的机器学习产生可泛化的低维神经指纹，能够在不同任务条件下区分个体
authors: "Karhula, J., Ojanperä, A., Yılmaz, E., Merz, S., Kaski, S., Salmelin, R."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.26.734424v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 利用脑磁图数据通过机器学习提取低维神经指纹
tldr: 本研究采用隐噪声贝叶斯降秩回归从MEG数据中学习低维神经指纹，在少量训练样本下即可实现个体区分，且指纹跨任务条件保持稳定，表明功率谱密度的个体差异具有内在性，为神经影像分析提供了高效工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 全功能连接组维度高导致计算负担重，需要一种低维但能保留个体特征的神经指纹替代方案。
method: 使用隐噪声贝叶斯降秩回归对MEG功能连接和功率谱密度数据降维，并与PCA、LDA对比，同时在不同任务条件下测试泛化能力。
result: 模型在仅20个样本时已可捕捉可推广的个体模式，30-35样本达最优；任务态指纹与静息态性能相当，且功率谱密度指纹在不同任务间高度相似。
conclusion: 隐噪声贝叶斯降秩回归是神经影像数据分析的有效方法，功率谱密度的个体差异本质上是内源的，不受认知任务改变。
---

## 摘要
个体大脑在结构和功能上都是独一无二的。功能差异由神经指纹捕捉，这些指纹反映了行为和认知上的个体差异以及与神经退行性疾病相关的群体水平变化。迄今为止，大多数研究都集中在由完整功能连接组构成的指纹上。然而，连接组的高维性会增加计算负荷并阻碍机器学习方法在潜在应用中的性能。因此，一种能保留完整连接组个体特征的低维替代方案将是有益的。本研究采用潜在噪声贝叶斯降秩回归（lnBRRR）来学习低维潜在空间，该空间能够捕捉来自脑磁图记录的功能连接和功率谱密度数据中的个体特征。我们评估了 lnBRRR 在低训练集大小（N=20-44）下的性能，并与主成分分析和线性判别分析进行了比较。还使用任务数据评估了模型性能，并通过余弦相似度比较了不同任务条件下的解，以确定不同的认知过程是否改变了个体特征。lnBRRR 在 N=20 时就已经捕捉到了可泛化的个体模式，但需要 N=30-35 才能达到最佳测试精度并防止潜在的过拟合。该模型也达到了与其他替代模型相当的性能。从任务数据中得出的潜在指纹获得了与静息态潜在指纹相当的性能，并且 lnBRRR 的解被证明可以跨条件泛化。此外，发现不同任务条件下功率谱密度数据的模型解非常相似，但旋转方向不同，这表明无论任务条件如何，模型都能捕捉到相似的个体特征模式。总之，目前的结果突出了 lnBRRR 作为神经影像数据分析的潜在工具，并证明功率谱密度中的个体差异在很大程度上是内在的，不受不同认知过程的影响。

## Abstract
Individual brains are unique in structure and function. Functional differences are captured by neural fingerprints, which reflect individual differences in behavior and cognition as well as group-level changes related to neurodegenerative diseases. Most research efforts so far have focused on fingerprints com-prising full functional connectomes. However, the high dimensionality of the connectomes can increase computational load and impede performance of machine learning methods in potential applications. A low-dimensional alternative that retains individual features of the full connectomes would thus be beneficial. The present study employed latent-noise Bayesian Reduced Rank Regression (lnBRRR) to learn low-dimensional latent spaces that capture individual features in functional connectivity and power spectral density data derived from MEG recordings. LnBRRR performance was assessed with low training set sizes (N=20-44), and against principal component analysis and linear discriminant analysis. Model performance was also assessed with task data, and the solutions were compared across task conditions with cosine similarity to establish whether individual features are altered by different cognitive processes. LnBRRR captured generalizable individual patterns already at N=20 but N=30-35 was needed to reach optimal test accuracies and to prevent potential overfitting. The model also achieved comparable performance to the alternative models. Latent fingerprints derived from task data attained comparable performance to resting-state latent fingerprints, and lnBRRR solutions were shown to generalize across conditions. Additionally, the model solutions for power spectral density data were discovered to be notably similar, yet differently rotated, over task conditions, suggesting that similar patterns of individual features were captured by the model regardless of the task condition. Altogether, the present results highlight lnBRRR as a potential tool for neuroimaging data analysis and demonstrate that individual differences in power spectral density are largely intrinsic and unaffected by varying cognitive processes.