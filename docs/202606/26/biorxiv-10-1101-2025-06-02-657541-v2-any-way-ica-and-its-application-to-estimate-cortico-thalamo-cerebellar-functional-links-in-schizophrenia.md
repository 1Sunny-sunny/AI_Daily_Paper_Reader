---
title: aNy-way ICA and its application to estimate cortico-thalamo-cerebellar functional links in schizophrenia
title_zh: aNy-way ICA及其在估计精神分裂症皮质-丘脑-小脑功能连接中的应用
authors: "Duan, K., Silva, R. F., Rahaman, M. A., Fu, Z., Liu, J., Kochunov, P., van Erp, T. G. M., Shultz, S., Calhoun, V. D."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.1101/2025.06.02.657541v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 通过任意方式ICA进行脑连接的数据融合
tldr: 针对多模态生物样本数据尺度不一、模型阶数各异的融合难题，研究提出一种灵活高效的aNy-way独立成分分析法。该方法结合高斯独立向量分析与独立成分分析，可优化跨模态载荷相关性并允许不同模态拥有不同阶数。仿真表明其准确性优于现有方法，在精神分裂症fMRI数据中成功识别出皮质-丘脑-小脑功能回路，该回路异常可区分患者与对照，并与认知缺陷相关。
source: biorxiv
selection_source: fresh_fetch
motivation: 多模态生物样本数据具有不同尺度和模型阶数，需开发灵活高效的数据融合方法以揭示疾病机制。
method: 提出aNy-way ICA，通过联合高斯独立向量分析和独立成分分析，优化载荷相关性与独立性，允许不同模态具有不同模型阶数。
result: 仿真显示方法准确性高，在精神分裂症fMRI中发现皮质-丘脑-小脑回路，其功能连接异常能区分患者并关联认知缺陷。
conclusion: 识别的皮质-丘脑-小脑回路可能构成精神分裂症中“认知协调障碍”的神经基础。
---

## 摘要
国际和国家生物样本库收集的多模态数据具有不同的尺度和模型阶数，并为疾病机制提供了独特且互补的见解。我们提出了一种新颖、灵活且高效的数据融合方法，任意路独立成分分析（aNy-way ICA）。aNy-way ICA通过高斯独立向量分析（IVA-G）优化链接成分的整个载荷相关结构，同时通过单独的ICA优化独立性，从而融合N路多模态或多域数据。这允许不同模态/域具有不同的模型阶数，并能在任意数量的模态或域中检测多个链接源，而无需对源施加正交性约束。仿真结果表明，aNy-way ICA能识别设计的源和载荷以及真实的协方差模式，与其他方法相比，尤其在噪声条件下，准确性有所提高。将aNy-way ICA应用于融合精神分裂症的四维多域fMRI数据，我们识别出一个皮质-丘脑-小脑回路，突出了高级丘脑核团、视觉皮层、默认模式网络和小脑后叶之间的功能连接。这些功能连接在两个独立数据集中得到了重复验证。高级丘脑核团、视觉皮层和默认模式网络之间的连接能够区分精神分裂症患者与对照人群，并且这种异常连接在发现和重复数据集中均与多种认知缺陷相关，表明所识别的皮质-丘脑-小脑回路可能是精神分裂症“认知协调不良”的基础。

## Abstract
Multimodal data collected by international and national biobanking efforts have distinct scales and model orders and provide unique and complementary insights into disease mechanisms. We propose a novel, flexible and efficient data fusion approach, aNy-way independent component analysis (aNy-way ICA). aNy-way ICA fuses N-way multimodal or multidomain data by optimizing the entire loading correlation structure of linked components via Gaussian independent vector analysis (IVA-G) and simultaneously optimizing independence via separate ICAs. This allows for distinct model orders for different modalities/domains and multiple linked sources detection across any number of modalities or domains without requiring orthogonality constraints on sources. Simulation results demonstrate that aNy-way ICA identifies the designed sources and loadings, as well as the true covariance patterns, with improved accuracy compared to other approaches, especially under noisy conditions. Applying aNy-way ICA to fuse 4D multi-domain fMRI data in schizophrenia, we identified a cortico-thalamo-cerebellar circuit, highlighting the functional linkages among higher order thalamic nuclei, the visual cortex, default mode network, and the posterior lobe of cerebellum. Their function links were replicated in two independent datasets. The connection among higher order thalamic nuclei, the visual cortex, and default mode network discriminates schizophrenia from controls and this aberrant connection is related to multiple cognitive deficits in both discovery and replication datasets, indicating the identified cortico-thalamo-cerebellar circuit may underlie "cognitive dysmetria" in schizophrenia.