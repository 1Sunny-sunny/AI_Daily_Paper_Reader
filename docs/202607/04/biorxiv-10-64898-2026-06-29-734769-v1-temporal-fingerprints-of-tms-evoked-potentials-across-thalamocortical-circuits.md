---
title: Temporal fingerprints of TMS-evoked potentials across thalamocortical circuits
title_zh: 丘脑皮质回路中经颅磁刺激诱发电位的时间指纹
authors: "Hassan, G., Gaglioti, G., Furregoni, G., Focacci, E., Porro, M., Bernardelli, L., Calcagno, A., Massimini, M., Sarasso, S., Rosanova, M., Casarotto, S."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.29.734769v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: TMS诱发电位的时间特征分析
tldr: 本研究系统探索了经颅磁刺激诱发电位（TEPs）在额、顶、枕叶的形态特征，通过自动分析40名被试的峰-峰振幅、潜伏期和峰间间隔，发现TEP形态反映刺激网络的区域特异性：枕叶早期振幅最大且潜伏期长，后期成分沿后-前轴递减，顶叶居中。结论是早期振幅反映局部招募，后期时间特征追踪循环节律，并提供Python工具表征皮层反应性。
source: biorxiv
selection_source: fresh_fetch
motivation: 系统探索非运动皮层TEPs的形态特征及其与局部网络特性的关联。
method: 对40名被试在左枕、顶、额叶刺激下记录的TEPs，自动计算峰-峰振幅、峰潜伏期和峰间间隔。
result: 枕叶TEPs早期振幅最大、潜伏期最长；后期潜伏期和峰间间隔沿后-前轴递减；顶叶呈中间模式。
conclusion: TEP形态受刺激网络属性影响，早期振幅反映局部招募程度，后期时间特征反映循环活动节律，可作为皮层反应性标记。
---

## 摘要
背景：经颅磁刺激（TMS）诱发的脑电图（EEG）电位为了解皮层动力学提供了一个直接窗口。然而，类似于感觉诱发电位，对其形态特征的系统探索尚付阙如，尤其是对于运动皮层以外的刺激。目的：从TMS诱发电位（TEPs）的时间过程中获取额叶、顶叶和枕叶网络的区域特异性属性。材料与方法：我们实现并应用了一种自动程序，计算了40名神经典型受试者在左侧枕叶（n=25）、顶叶（n=25）和额叶（n=25）皮层区域接受刺激后记录的TEPs的峰峰值振幅、峰值潜伏期和峰间间隔。结果：枕叶TEPs显示出最大的峰峰值振幅和最长的第一波形成分潜伏期，与刺激强度无关，这与招募一大片密集连接的神经元一致。关于后期成分，潜伏期和峰间间隔沿后-前轴系统性降低，反映出从以α振荡为主的枕叶回路到额叶皮层与皮层下结构之间的紧密耦合环路的逐步加快的循环动力学。顶叶TEPs表现出中等的振幅和潜伏期测量值，这与顶上小叶皮层异质的细胞构筑和连接组织一致。结论：我们的发现表明，TEP形态受刺激网络的独特属性塑造，早期振幅反映局部招募的程度，而后期时间特征追踪循环活动的节律。这项工作提供了一种机制上有据且实用易行的方法，并以Python工具的形式发布，可用于表征不同脑状态和人群的皮层反应性。

## Abstract
Background: Electroencephalographic (EEG) potentials evoked by transcranial magnetic stimulation (TMS) offer a direct window into cortical dynamics. Yet, a systematic exploration of their morphological features, analogous to sensory-evoked potentials, is lacking, especially for stimulation outside the motor cortex. Aim: To obtain region-specific properties of frontal, parietal and occipital networks from the time course of TMS-evoked potentials (TEPs). Materials and Methods: We implemented and applied an automatic procedure to compute peak-to-peak amplitude, peak latency, and inter-peak interval of TEPs recorded from 40 neurotypical subjects stimulated over left occipital (n=25), parietal (n=25), and frontal (n=25) cortices. Results: Occipital TEPs showed the largest peak-to-peak amplitude and longest latency of the first waveform component, independently of stimulation intensity and consistent with the recruitment of a large patch of densely interconnected neurons. Concerning later components, both latency and inter-peak interval systematically decreased along the posterior-to-anterior axis, reflecting progressively faster recurrent dynamics from the alpha-dominated occipital circuitry to the tightly coupled loops between frontal cortex and subcortical structures. Parietal TEPs showed intermediate amplitude and latency measures, consistent with the heterogeneous cytoarchitectonic and connectional organization of the superior parietal cortex. Conclusions: Our findings suggest that TEP morphology is shaped by the distinct properties of the stimulated networks, with early amplitude reflecting the extent of local recruitment and later temporal features tracking the rhythm of recurrent activity. This work offers a mechanistically grounded and practically accessible approach, also released as a Python-based tool, that allows to characterize cortical reactivity across different brain-states and populations.