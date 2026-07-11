---
title: "BCCWJ-Brain: A Multi-Modal fMRI, MEG, and EEG Dataset of Naturalistic Japanese Reading"
title_zh: BCCWJ-Brain：一个自然日语阅读的多模态fMRI、MEG和EEG数据集
authors: "Sugimoto, Y., Asahara, M., Jeong, H., Kanno, A., Koizumi, M., Oseki, Y."
date: 2026-07-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.05.736621v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 多模态神经影像数据集，用于自然阅读
tldr: 该研究发布了BCCWJ-Brain多模态神经影像数据集，包含112名日语母语者在自然阅读报纸文章时的fMRI、MEG和EEG数据，旨在为大型语言模型等计算模型提供认知基准，数据集公开于OpenNeuro，是神经科学和自然语言处理领域的宝贵资源。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-004.webp\", \"caption\": \"Table 1: Recent multimodal neuroimaging datasets for language processing research.\", \"page\": 3, \"index\": 4, \"width\": 936, \"height\": 761}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-008.webp\", \"caption\": \"Table 2: Participants’ information\", \"page\": 5, \"index\": 8, \"width\": 921, \"height\": 998}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-005.webp\", \"caption\": \"Figure 1: Directory structure of the BCCWJ-Brain datasets (BCCWJ-fMRI, BCCWJ-MEG, and BCCWJ-EEG, which use BIDS structures (v 1.9.0)). XX = subject ID; N = run number (1–4); * = sub-XX_task-BCCWJreading.\", \"page\": 8, \"index\": 5, \"width\": 1030, \"height\": 742}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-006.webp\", \"caption\": \"Figure 2: Inter-subject correlation (ISC) results.\", \"page\": 9, \"index\": 6, \"width\": 952, \"height\": 206}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-007.webp\", \"caption\": \"Figure 3: GLM analysis results. Top: word-rate contrast (FWE p < 0.05, Bonferroni, k > 50 voxels). Bottom: word-length contrast (FWE p < 0.05, Bonferroni, k > 50 voxels). Color bar indicates t-statistic values. L = left hemisphere; R = right hemisphere.\", \"page\": 9, \"index\": 7, \"width\": 922, \"height\": 306}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-002.webp\", \"caption\": \"Figure 4: Average evoked response to all words across subjects (MEG).\", \"page\": 10, \"index\": 2, \"width\": 914, \"height\": 489}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-003.webp\", \"caption\": \"Table 5: Word length — FWE (p < 0.05, Bonferroni, k > 50 voxels, t > 6.53).\", \"page\": 10, \"index\": 3, \"width\": 936, \"height\": 190}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-001.webp\", \"caption\": \"Figure 5: Average evoked response to all words across subjects (EEG).\", \"page\": 11, \"index\": 1, \"width\": 914, \"height\": 490}]"
motivation: 构建一个多模态、同刺激条件下的自然阅读脑成像数据集，以探索大脑语言处理机制并为语言模型提供评估基准。
method: 采用快速序列视觉呈现范式，采集112名日本人阅读BCCWJ报纸文章时的fMRI、MEG和EEG信号。
result: 成功构建并共享了BCCWJ-Brain数据集，涵盖三种模态的脑功能数据。
conclusion: 该数据集为神经科学和NLP研究提供了独特的跨模态认知基准。
---

## 摘要
我们介绍了BCCWJ-Brain数据集，这是一个多模态神经影像资源，包含功能性磁共振成像（fMRI）、脑磁图（MEG）和脑电图（EEG）数据，这些数据采集自母语为日语的受试者在阅读《现代日语书面语均衡语料库》（BCCWJ）中的报纸文章时的神经活动。神经数据来自112名参与者（36名fMRI，35名MEG，41名EEG），他们阅读了以快速序列视觉呈现（RSVP）范式呈现的二十篇报纸文章。通过提供在相同自然阅读刺激下采集的三种互补神经影像模态，该数据集为大型语言模型等计算模型提供了认知基准。该数据集在OpenNeuro平台上公开提供，为神经科学、自然语言处理和相关研究领域提供了宝贵的资源。

## Abstract
We present the BCCWJ-Brain dataset, a multi-modal neuroimaging resource comprising functional magnetic resonance imaging (fMRI), magnetoencephalography (MEG), and electroencephalography (EEG) data recorded from native Japanese speakers reading newspaper articles from the Balanced Corpus of Contemporary Written Japanese (BCCWJ). Neural data were collected from 112 participants (36 fMRI, 35 MEG, and 41 EEG) as they read twenty newspaper articles presented in a Rapid Serial Visual Presentation (RSVP) paradigm. By providing three complementary neuroimaging modalities collected under identical naturalistic reading stimuli, this dataset provides a cognitive benchmark for computational models such as large language models. The dataset is publicly available on the OpenNeuro platform, offering a valuable resource for neuroscience, natural language processing, and related research fields.