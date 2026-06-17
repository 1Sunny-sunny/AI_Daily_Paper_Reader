---
title: EEG-based classification models reveal differential neural processing of words and images
title_zh: 基于EEG的分类模型揭示字词与图像的差异性神经处理
authors: "Morakabati, N. R., Thiha, A. S., Schechtman, E."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.16.712233v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: EEG分类模型解码视觉类别信息
tldr: 本研究利用脑电图（EEG）和机器学习方法，探索词语和图像刺激下类别表征的神经处理差异。通过让被试观看五类物体的图像或词语并进行分类任务，训练支持向量机对EEG数据进行解码。结果表明，图像诱发的类别分类准确率显著高于词语，且所有类别对在图像条件下可区分，顶叶和左颞电极贡献更大，模式还能跨被试泛化。该流程为研究意识及离线状态下类别神经表征的激活与再激活提供了有效工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 为了探索不同输入模态（图像与词语）下类别信息在神经层面的处理差异，并验证EEG在神经解码中的有效性。
method: 被试执行五类别（动物、工具、食物、场景、车辆）的图像和词语分类任务，同时记录EEG数据，用支持向量机进行多变量模式分析。
result: 图像试验的分类准确率显著高于词语试验，所有类别对在图像条件下可区分，而词语条件仅有一对可区分，且顶叶和左颞电极贡献更大，图像分类模式还能跨被试泛化。
conclusion: 该EEG分析管道对图像类别解码表现出高准确率，证实了EEG在探讨类别表征及跨状态神经再激活研究中的潜力。
---

## 摘要
背景：利用神经影像数据的机器学习方法可用于监测神经表征的激活。具体而言，它们可用于识别参与处理特定类别项目的脑网络。该方法已应用于神经影像数据，包括功能磁共振成像数据和脑电图（EEG）数据。

新方法：在此，我们提出了一项任务和一个分析流程，用于利用EEG研究类别表征。参与者（N=30）观看一系列属于五个类别（动物、工具、食物、场景和车辆）的物体的图像和字词，并在同一类别的项目连续呈现时做出反应。

结果：我们在参与者的EEG数据上训练支持向量机，发现图像试次和字词试次均产生了显著的类别分类准确率，图像试次的准确率高于字词试次。当以成对方式比较类别时，对于图像试次，所有对在统计上均可区分，而对于字词试次，仅有一对是可区分的。顶叶和左颞叶电极对图像分类的贡献大于额叶和右颞叶电极。类别特异性活动模式也在参与者之间对图像试次泛化。

与现有方法的比较：我们的数据和分析流程取得了高分类准确率，主要针对图像试次，为EEG数据在神经解码中的实用性提供了支持。

结论：这些方法可用于探索在清醒状态下以及可能在离线状态下类别层次神经表征的激活和再激活。

## Abstract
BackgroundMachine learning methods employing neuroimaging data are useful for monitoring the activation of neural representations. Specifically, they can be used to discern the brain networks engaged in processing specific categories of items. This approach has been employed on neuroimaging data, including functional magnetic resonance imaging data and electroencephalography (EEG) data.

New methodHere, we present a task and an analytical pipeline for investigating category representations using EEG. Participants (N = 30) viewed a series of images and words of objects belonging to five categories (Animals, Tools, Food, Scenes, and Vehicles) and responded when items from the same category were presented consecutively.

ResultsWe trained support vector machines on EEG data within participants and found that both image trials and word trials yielded significant category classification accuracy, with image trials achieving higher accuracy than word trials. When comparing categories in a pair-wise fashion, all pairs were statistically distinguishable for image trials, whereas only one pair was distinguishable for word trials. Parietal and Left Temporal electrodes contributed more to image classification than Frontal and Right Temporal electrodes. Category-specific activity patterns also generalized across participants for image trials.

Comparison with existing methodsOur data and analytic pipeline yielded high classification accuracies, primarily for image trials, providing support for the utility of EEG data for neural decoding.

ConclusionsThese methods can be instrumental for exploring the activation and reactivation of neural representations at the category level during wakefulness and, potentially, during offline states.