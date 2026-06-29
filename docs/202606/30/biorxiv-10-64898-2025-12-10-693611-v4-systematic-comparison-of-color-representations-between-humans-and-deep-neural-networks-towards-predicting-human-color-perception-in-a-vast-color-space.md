---
title: "Systematic comparison of color representations between humans and deep neural networks: towards predicting human color perception in a vast color space"
title_zh: 人类与深度神经网络颜色表征的系统性比较：迈向在广阔色彩空间中预测人类颜色感知
authors: "Wickramanayaka, N. R., Oizumi, M."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2025.12.10.693611v4.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 比较深度神经网络与人类颜色表征以理解编码
tldr: 人类大规模颜色感知表征难以通过实验获取，深度神经网络可能提供预测。本研究系统比较自监督、监督和CLIP范式，运用GWOT对比嵌入与人类93色相似性，发现仅CLIP在输出层维持对齐。探索4096色表征，早期层及CLIP输出形成稳定结构，为未来实验提供预测。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示大规模人类颜色感知的完整表征结构，并确定哪种DNN学习范式能产生与人类感知对齐的颜色表示。
method: 采用Gromov-Wasserstein最优传输无监督比较自监督、监督和CLIP学习的DNN嵌入与93种颜色的人类相似性判断。
result: 所有范式早期层均与人类数据精细对齐，但仅CLIP在输出层维持一致表征；4096色分析显示早期层和CLIP输出各自收敛于稳定结构。
conclusion: CLIP能最好地模拟人类颜色感知，该框架可预测大规模未知颜色表征，为未来心理物理实验提供方向。
---

## 摘要
大规模人类颜色感知的表征结构仍未完全了解。尽管经典研究测量了大量颜色对，但这些测量仅比较了相似颜色，而由于心理物理学实验的时间成本，探索数千种颜色间的整体关系一直不可行。鉴于这些限制，深度神经网络（DNNs）作为提供人类感知代理或预测的有前景工具，已引起关注，其范围可超越心理物理学实验。然而，仍不清楚哪些 DNN 具有与人类颜色感知几何对齐的嵌入。此外，也不清楚何种学习范式能使 DNN 获得与人类一致的颜色表征。在此，我们系统性地研究了何种学习范式能使 DNN 产生与人类在结构上一致的颜色表征，重点关注三种类型：仅训练图像的自监督学习（SSL）、训练带有类别标签图像的监督学习（SL），以及训练图像-文本对的对比语言-图像预训练（CLIP）。我们使用一种严格的非监督方法——Gromov-Wasserstein 最优传输（GWOT），将 DNN 的嵌入与人类对 93 种颜色的相似性判断进行比较。结果表明，尽管每种学习范式在早期层中在细粒度水平上获得了与人类数据高度一致的颜色表征，但只有 CLIP 在输出层保持了这种表征。此外，我们利用 DNN 的关键优势，研究了 4096 种颜色的表征结构，发现每种学习范式的早期层和 CLIP 的输出层均一致收敛于各自特有的结构。这些结构为大规模人类颜色表征提供了合理的预测。我们的工作展示了一种方法，即通过在有限经验空间中验证的计算模型来探索人类感知的未知领域，并为未来大规模心理物理学实验提供了预测。

## Abstract
The representational structure of large-scale human color perception remains incompletely understood. While classical studies measured numerous color pairs, these measurements compared only similar colors, and exploring the global relationships among thousands of colors has been infeasible due to the time costs of psychophysical experiments. Given these constraints, deep neural networks (DNNs) have attracted attention as a promising tool for providing proxies or predictions of human perception beyond the scope of psychophysical experiments. However, it remains unclear which DNNs possess embeddings that geometrically align with human color perception. Furthermore, it is unclear which learning paradigm enables DNNs to acquire a color representation that aligns with that of humans. Here, we systematically investigate which learning paradigm enables DNNs to produce a color representation that is structurally congruent with that of humans, with a focus on three types: self-supervised learning (SSL) that trains on images alone, supervised learning (SL) that trains on images with category labels, and contrastive language-image pre-training (CLIP) that trains on image-text pairs. We compared the embeddings of DNNs with the human similarity judgments of 93 colors using a rigorous unsupervised method termed Gromov-Wasserstein Optimal Transport (GWOT). Our results show that , while each learning paradigm acquires color representations that strongly align with human data at the fine-item level in early layers, only CLIP sustains such a representation at the output. Furthermore, when we leveraged a key advantage of DNNs and investigated the representational structure of 4096 colors, the early layers of each learning paradigm and the output of CLIP consistently converged on their own characteristic structures. These structures present plausible predictions for the large-scale human color representation. Our work demonstrates an approach for exploring unknown territories of human perception through the use of computational models validated in a limited empirical space, and provides predictions for future large-scale psychophysical experiments.