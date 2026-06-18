---
title: Stimulus identity rather than emotion drives EEG classification on the FACED dataset
title_zh: 在FACED数据集上，刺激身份而非情绪驱动EEG分类
authors: "Gerster, M., Sirotina, E., Orlovskii, A., Hertz, A., Champaud, J., Guarino, D., Tulli, S."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.12.731889v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: EEG解码刺激身份而非情绪
tldr: 该研究针对FACED数据集，通过线性分类器和深度学习模型分析发现，其脑电图情绪分类性能主要由刺激身份而非情绪驱动。原因包括每个情绪类别刺激少、使用刺激预设标签以及时域分割导致的自相关。分类准确率在使用自评标签时下降，且减少视频数反而提升。文章最后提出了五项避免此类混淆的实验设计建议。
source: biorxiv
selection_source: fresh_fetch
motivation: 推动EEG情绪识别需要可靠基准，但FACED数据集可能存在混淆因素。
method: 使用LinearSVC和CLISA模型，从受试者感受、标签替换和视频缩减三个角度验证分类驱动因素。
result: 分类表现相近于感受与否情绪，自评标签降低准确率，减少视频数提升准确率，表明分类依赖刺激身份。
conclusion: FACED设计缺陷导致分类混淆，未来研究应遵循五项建议避免类似问题。
---

## 摘要
可靠的基准数据集对于推进基于EEG的情绪识别至关重要。细粒度情感计算EEG数据集（FACED）是最大的公开可用EEG情绪数据集（123名受试者，九种情绪类别），并被广泛用作基准。我们证明，在FACED上的被试内和跨被试分类主要反映了刺激身份而非情绪。使用线性分类器（LinearSVC）和深度学习模型（CLISA），我们表明：（1）在受试者报告感受到与未感受到指定情绪的试次中，分类性能相当；（2）当用个体自我报告替代刺激指定标签时，准确率下降；（3）尽管丢弃了三分之二的数据，每个情绪减少到一个视频时准确率反而提高。这些结果反映了FACED中的三个设计选择：每个类别的刺激数量少、刺激指定标签以及用于交叉验证的视频内时间分割。这些共同使得数据集容易受到时间自相关和刺激身份混淆的影响。为了指导未来的工作，我们提出五项建议——涵盖刺激多样性、时间独立性和标签验证——以减轻这些混淆的情绪解码研究设计。

## Abstract
Reliable benchmark datasets are critical for advancing EEG-based emotion recognition. The Finer-grained Affective Computing EEG Dataset (FACED) is the largest publicly available EEG emotion dataset (123 subjects, nine emotion categories) and a widely adopted benchmark. We demonstrate that both intra-subject and cross-subject classification on FACED primarily reflects stimulus identity rather than emotion. Using a linear classifier (LinearSVC) and a deep learning model (CLISA), we show that (1) classification performance is comparable for trials where subjects reported feeling versus not feeling the assigned emotion; (2) accuracy drops when stimulus-assigned labels are replaced with individual self-reports; and (3) accuracy increases when reducing to one video per emotion despite discarding two-thirds of the data. These results reflect three design choices in FACED: few stimuli per category, stimulus-assigned labels, and within-video temporal splits for cross-validation. Together, these make the dataset susceptible to temporal autocorrelation and stimulus-identity confounds. To guide future work, we propose five recommendations -- spanning stimulus diversity, temporal independence, and label validation -- for emotion-decoding study designs that mitigate these confounds.