---
title: "FASTIMAGES: Validating replay detection methods in human Neuroimaging using a combined MEG and fMRI dataset"
title_zh: "FASTIMAGES: 使用联合MEG和fMRI数据集验证人类神经影像中的重放检测方法"
authors: "Kern, S., Wittkuhn, L., Buss, E., Schuck, N., Feld, G. B."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.26.727586v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 验证随时间检测神经重放模式的方法
tldr: 神经重放是一种与记忆、规划等认知功能相关的脑活动模式，但非侵入性检测方法缺乏可靠验证。本研究提出FASTIMAGES数据集，包含70名参与者的fMRI和MEG记录，其中含有快速视觉刺激诱发的已知神经序列。通过该基准，检验了TDLM和SODA两种序列检测方法，发现它们在各自模态中表现优异但跨模态有限，该数据集可为未来方法提供验证基准。
source: biorxiv
selection_source: fresh_fetch
motivation: 缺乏对现有非侵入性神经序列检测方法与已知真实信号的比较验证。
method: 构建包含快速视觉刺激诱发的已知神经序列的fMRI和MEG数据集（FASTIMAGES），并应用TDLM和SODA方法进行检测对比。
result: TDLM在MEG中、SODA在fMRI中效果显著且效果量相当，但跨模态应用效果受限。
conclusion: FASTIMAGES数据集可作为验证未来神经序列检测方法的基准，促进该方法的发展。
---

## 摘要
利用侵入性电生理学在啮齿动物和人类中进行的研究已经证实，神经重放是大脑中广泛存在的一种现象，与包括记忆、规划和决策在内的多种认知功能相关。然而，在人类中进行侵入性记录仍然很困难，因此关于人类神经重放的知识仍然匮乏。因此，为了全面理解人类的神经重放，我们需要能够非侵入性地检测它的可靠方法。目前已经提出了几种主要的非侵入性方法，但我们缺乏针对已知真实信号的全面的比较验证。在这项研究中，我们提出了FASTIMAGES数据集，这是一个来自70名参与者的基准数据集，包含并行的fMRI（n=40，先前已发表）和MEG（n=30）记录，其中包含由快速视觉刺激诱发的已知神经序列以及功能定位实验。这些神经序列由五种不同的视觉刺激诱发，这些刺激以132、164、228和612毫秒的起始间隔按顺序呈现。利用该数据集，我们研究了两种现有的序列检测统计方法，即时间延迟线性建模（TDLM，由Liu等人于2021年为MEG开发）和斜率阶动态分析（SODA，由Wittkuhn和Schuck于2021年为fMRI开发）。我们检查了每种方法的基本假设，分析了它们在MEG和fMRI应用中的优缺点。我们证明，两种方法在其原生模态中表现出色（TDLM用于MEG，SODA用于fMRI），在该基准的理想条件下，效应量相当。跨模态迁移仍然具有挑战性。最后，FASTIMAGES数据集提供了已知且清晰明确的序列数据，可用于在理想条件下对未来的序列检测方法进行基准测试和验证。

## Abstract
Studies in rodents and humans using invasive electrophysiology have established that neural replay is a ubiquitous phenomenon in the brain that is associated with a wide range of cognitive functions, including memory, planning and decision making. Yet, invasively recording in humans remains difficult, and hence knowledge about replay in humans remains scarce. Hence, to comprehensively understand replay in humans, we need reliable approaches that can detect it non-invasively. Several main non-invasive approaches have been proposed, but we lack a full comparative validation against known ground truth signals. In this study, we present FASTIMAGES, a benchmark dataset from seventy participants with parallel fMRI (n = 40, previously published) and MEG (n=30) recordings containing known neural sequences evoked by fast visual stimulation as well as functional localizer trials. The neural sequences were elicited by five different visual stimuli shown in sequences at speeds of 132, 164, 228 and 612 milliseconds onset-to-onset intervals. Using this dataset, we investigate two existing statistical methods for sequence detection, namely Temporally Delayed Linear Modelling (TDLM, developed for MEG by Liu et al., 2021) and Slope Order Dynamic Analysis (SODA, developed for fMRI by Wittkuhn & Schuck, 2021). We examine the underlying assumptions of each method, analyse their resulting strengths and weaknesses in application to MEG and fMRI. We demonstrate that both approaches excel in their native modality (TDLM for MEG and SODA for fMRI), with comparable effect sizes given idealized conditions in this benchmark. Cross-modality transfer remains challenging. Finally, the FASTIMAGES dataset provides data with known and clearly expressed sequences and can be used to benchmark and validate future sequence detection methods under idealized conditions.