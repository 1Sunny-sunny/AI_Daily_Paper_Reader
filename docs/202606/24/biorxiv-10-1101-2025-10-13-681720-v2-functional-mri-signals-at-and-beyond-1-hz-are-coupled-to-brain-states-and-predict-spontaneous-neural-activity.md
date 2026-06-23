---
title: Functional MRI signals at and beyond 1 Hz are coupled to brain states and predict spontaneous neural activity
title_zh: 1.3 Hz 及以上的功能性磁共振成像信号与脑状态耦合并可预测自发神经活动
authors: "Jacob, L. P. L., Bailes, S. M., Williams, S. D., Stringer, C., Rosen, B. R., Polimeni, J. R., Lewis, L. D."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.13.681720v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 快速fMRI信号预测自发神经活动和脑状态
tldr: 本研究利用快速fMRI（TR=378 ms）与同步EEG，探究高频fMRI信号与脑状态及自发神经活动的关系。发现NREM睡眠时，频率高达1.3 Hz的fMRI功率增强，且高频fMRI功率与EEG alpha和delta节律存在时空耦合。通过机器学习，可从高频fMRI信号跨个体解码EEG节律，表明高频fMRI包含神经耦合信息，快速fMRI能时间精确地量化自发神经动态。
source: biorxiv
selection_source: fresh_fetch
motivation: 理解快速fMRI血流动力学信号与静息态自发神经活动的关系，以推断神经过程。
method: 使用快速fMRI（TR=378 ms）和同时EEG记录27名在睡眠与清醒间转换的被试。
result: NREM睡眠期高频fMRI功率增强，并与EEG alpha/delta节律相关，且可被机器学习跨个体解码。
conclusion: 高频fMRI信号与动态脑状态耦合，快速fMRI可实现自发神经活动的时间精确量化。
---

## 摘要
技术进步使得高时间分辨率的功能性磁共振成像采集成为可能，从而能在短短几百毫秒内实现全脑成像。然而，静息态下快速血流动力学信号与自发神经活动之间的关系尚未被充分理解，这限制了我们从这些快速数据中推断神经过程的能力。我们假设高频fMRI信号与警觉状态相关的自发神经活动有关，并且这些高频信号可用于推断由脑电神经节律所表征的神经元活动的动态变化。利用快速fMRI（TR=378毫秒）和同步脑电图对27名在睡眠与觉醒之间漂移的受试者进行研究，我们发现非快速眼动睡眠期间（与觉醒时相比）频率高达1.3 Hz的fMRI功率增加。高频fMRI功率还与经典的觉醒相关脑电节律（α和δ波）相关，其时空互相关模式既反映了共享的觉醒动态，也反映了节律特异性特征。通过机器学习，我们发现在训练集中未包含的受试者中，可以从高频fMRI信号解码出脑电α和δ波功率，表明fMRI信号的高频成分包含与神经耦合的稳健信息，足以跨个体泛化。这些结果揭示高频fMRI信号与动态变化的脑状态耦合，并且快速fMRI能够实现对自发神经活动的时间精确量化。

## Abstract
Technological advances have enabled fMRI acquisition with high temporal resolution, enabling brainwide imaging in just a few hundreds of milliseconds. However, the relationship between fast hemodynamic signals and spontaneous neural activity in the resting state is not yet well understood, limiting our ability to infer neural processes from these fast data. We hypothesized that high-frequency fMRI signals are linked to spontaneous neural activity tied to vigilance states, and that these high-frequency signals could be used to infer the dynamic variations in neuronal activity indexed by EEG neural rhythms. Using fast fMRI (TR=378 ms) and simultaneous EEG in 27 humans drifting between sleep and wakefulness, we found that fMRI power increased during NREM sleep (compared to wakefulness) in frequencies up to 1.3 Hz. High-frequency fMRI power was also correlated to canonical arousal-linked EEG rhythms (alpha and delta), with spatiotemporal cross-correlation patterns reflecting both shared arousal dynamics and rhythm-specific signatures. Using machine learning, we found that EEG alpha and delta power can be decoded from high-frequency fMRI signals in subjects held-out from the training set, showing that the high-frequency components of fMRI signals contain neurally-coupled information robust enough to generalize across individuals. These results reveal that high-frequency fMRI signals are coupled to dynamically varying brain states, and that fast fMRI allows for temporally precise quantification of spontaneous neural activity.