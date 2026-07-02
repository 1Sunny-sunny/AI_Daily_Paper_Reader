---
title: "NeuroVLM: A generative vision-language framework for human neuroimaging"
title_zh: NeuroVLM：一个用于人类神经影像的生成式视觉-语言框架
authors: "Hammonds, R., Aguirre-Chavez, J., Omoma-Edosa, B., Patel, A., Voytek, B."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.06.704508v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 用于神经影像-文本对的生成式视觉语言模型
tldr: 随着神经影像研究积累了大量自然语言描述与激活坐标配对数据，本研究利用视觉语言模型（VLM）技术，提出NeuroVLM框架，从30826对神经影像-文本中学习，支持对比与生成目标，实现了文本到脑图生成、脑图到文本解读、网络标注及跨模态检索等功能，推动了神经影像的智能化理解与应用。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经影像领域存在大量图文配对数据，但缺乏有效的统一框架以实现跨模态交互，需要借助VLM的强大能力来打通文本与脑图之间的生成与理解。
method: 提出NeuroVLM架构，在30826个神经影像-文本对上同时训练对比学习和生成任务，包括文本生成脑图、脑图生成文本以及相似度排序。
result: 模型能根据文本生成脑图谱或统计图，自动解析神经影像的含义，标记网络，并能检索与图像或文本最相关的文献与脑图。
conclusion: NeuroVLM成功将VLM范式引入神经影像分析，展示了生成式跨模态框架在多任务上的潜力，为神经影像与自然语言的融合提供了新路径。
---

## 摘要
神经影像研究已产生数万篇将自然语言与激活坐标表配对的文章。视觉-语言模型的最新进展提供了同时建模文本与图像的方法。在本研究中，我们提出NeuroVLM，一种从30,826个人类神经影像-文本对中进行学习的模型架构。该架构支持对比学习与生成目标。对比模型对神经影像与文本之间的相似度进行排序。生成模型包括文本到神经影像和神经影像到文本的生成。这些模型在多种图谱的网络图像、不同出版物的统计图谱以及由坐标表生成的图像上进行了评估。这些模型能够根据文本语料生成相应的图谱或图像，生成神经影像的文本解释，标注脑网络，找出与特定神经影像查询最相关的文献，或找出与特定文本查询最相关的神经影像。

## Abstract
Neuroimaging research has produced tens-of-thousands of articles that pair natural language and activation coordinate tables. Recent advances in vision-language models (VLMs) have provided methods to model text and images simultaneously. In this work, we present NeuroVLM, a model architecture for learning from 30,826 human neuroimage-text pairs. The architecture supports contrastive and generative objectives. The contrastive model ranks similarity between neuroimages and text. The generative models include text-to-neuroimage and neuroimage-to-text. These models are evaluated on network images from a variety of atlases, statistical maps from diverse publications, and images created from coordinate tables. These models are capable of generating atlases or maps given a text corpus, generating text interpretations of neuroimages, labeling networks, finding publications most related to a neuroimage query, or finding neuroimages most related to a text query.