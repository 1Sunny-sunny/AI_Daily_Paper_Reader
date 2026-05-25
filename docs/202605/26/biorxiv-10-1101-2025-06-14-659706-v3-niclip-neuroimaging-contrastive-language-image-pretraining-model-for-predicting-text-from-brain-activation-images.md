---
title: "NiCLIP: Neuroimaging contrastive language-image pretraining model for predicting text from brain activation images"
title_zh: NiCLIP：用于从脑激活图像预测文本的神经影像对比语言-图像预训练模型
authors: "Peraza, J. A., Kent, J. D., Nichols, T. E., Poline, J.-B., de la Vega, A., Laird, A. R."
date: 2026-05-23
pdf: "https://www.biorxiv.org/content/10.1101/2025.06.14.659706v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用对比学习从脑激活预测文本
tldr: 神经影像功能解码长期面临文本信息语义整合困难。本研究提出NiCLIP，一种对比语言-图像预训练模型，通过逾23000篇神经科学文章训练文本与脑激活图的关联，实现从脑激活模式预测认知任务。使用全文和策展认知本体可优化性能，微调大语言模型进一步提升。NiCLIP在组级激活图上预测准确，可表征脑区功能角色，但受限于个体级噪声图，为功能解码带来重大进展。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有元分析功能解码方法无法捕捉文本的语义上下文，限制了对脑激活模式的准确认知预测。
method: 利用23000多篇神经科学文章训练CLIP模型进行文本-大脑激活图的对比学习，结合全文和策展认知本体，并微调大语言模型。
result: NiCLIP在组级激活图上准确预测跨领域认知任务和脑区功能角色，但对个体级噪声图性能有限。
conclusion: NiCLIP代表了神经影像定量功能解码的重大进步，为假设生成和科学发现提供了强大工具。
---

## 摘要
从脑激活图预测认知过程多年来一直是神经科学领域的一个开放性问题。元分析功能解码方法旨在通过提供与特定脑区相关的行为特征的定量估计来解决这一问题。现有方法在神经影像元分析中面临固有挑战，尤其是在整合出版物中的文本信息方面，因为它们依赖于有限的度量标准，未能捕捉文本的语义上下文。大型语言模型（LLMs）与先进的深度对比学习模型（如CLIP）相结合以对齐文本和图像，已经彻底改变了神经影像元分析，可能为功能解码挑战提供解决方案。在这项工作中，我们提出了NiCLIP，一个对比语言-图像预训练模型，能够从脑激活模式预测认知任务、概念和领域。我们利用超过23,000篇神经科学文章来训练一个用于文本-大脑关联的CLIP模型。对NiCLIP预测的评估表明，当使用全文文章而非摘要，以及采用具有精确任务-概念-领域映射的精选认知本体时，性能达到最优。此外，微调后的大型语言模型（如BrainGPT模型）略优于其基础LLM版本。我们的结果表明，NiCLIP能够从人类连接组计划提供的组水平激活图准确预测跨多个领域（如情绪、语言、运动）的认知任务，并精确表征特定脑区（包括杏仁核、海马体和颞顶联合区）的功能角色。然而，NiCLIP在处理噪声较大的个体受试者水平激活图时表现出局限性。NiCLIP代表了神经影像定量功能解码的重大进展，为研究人员提供了假设生成和科学发现的强大工具。

## Abstract
Predicting cognitive processes from brain activation maps has remained an open question within the neuroscience community for many years. Meta-analytic functional decoding methods aim to tackle this issue by providing a quantitative estimation of behavioral profiles associated with specific brain regions. Existing methods face intrinsic challenges in neuroimaging meta-analysis, particularly in consolidating textual information from publications, as they rely on limited metrics that do not capture the semantic context of the text. The combination of large language models (LLMs) with advanced deep contrastive learning models (e.g., CLIP) for aligning text with images has revolutionized neuroimaging meta-analysis, potentially offering solutions to functional decoding challenges. In this work, we present NiCLIP, a contrastive language-image pretrained model that predicts cognitive tasks, concepts, and domains from brain activation patterns. We leveraged over 23,000 neuroscientific articles to train a CLIP model for text-to-brain association. Evaluation of NiCLIP predictions revealed that performance is optimized when using full-text articles instead of abstracts, as well as a curated cognitive ontology with precise task-concept-domain mappings. Furthermore, fine-tuned LLMs (e.g., BrainGPT models) modestly outperform their base LLM counterparts. Our results indicated that NiCLIP accurately predicts cognitive tasks from group-level activation maps provided by the Human Connectome Project across multiple domains (e.g., emotion, language, motor) and precisely characterizes the functional roles of specific brain regions, including the amygdala, hippocampus, and temporoparietal junction. However, NiCLIP showed limitations with noisy subject-level activation maps. NiCLIP represents a significant advancement in quantitative functional decoding for neuroimaging, offering researchers a powerful tool for hypothesis generation and scientific discovery.