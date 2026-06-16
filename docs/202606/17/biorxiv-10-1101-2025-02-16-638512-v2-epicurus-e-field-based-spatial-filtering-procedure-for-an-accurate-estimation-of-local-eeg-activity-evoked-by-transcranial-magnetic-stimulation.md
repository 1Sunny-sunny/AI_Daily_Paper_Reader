---
title: "EPICURUS: E-field-based spatial filtering procedure for an accurate estimation of local EEG activity evoked by Transcranial Magnetic Stimulation"
title_zh: EPICURUS：基于电场空间滤波的经颅磁刺激诱发局部脑电活动精确估计方法
authors: "Corominas-Teruel, X., Mutanen, T., Leto, C., Colomina, M. T., Gallea, C., Bracco, M., Cabre, A. V."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.1101/2025.02.16.638512v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 基于电场空间滤波从TMS中估计局部脑电
tldr: 经颅磁刺激联合脑电图（TMS-EEG）研究面临局部诱发反应难以可靠分离的挑战。本文提出EPICURUS空间滤波方法，利用个体化MRI模拟的TMS感应电场，精确界定局部活动的空间范围并重建源信号，有效抑制远源串扰。合成与真实数据验证表明，该方法能保留早期局部活动、衰减后期非局部成分，有望提升TMS-EEG的时空特异性。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决TMS-EEG中准确分离刺激灶局部诱发反应与非目标源干扰的难题。
method: 基于个体化MRI电场仿真，构建空间滤波器引导EEG源重建，最小化远源串扰。
result: 在合成模拟和人类数据中，EPICURUS保留早期诱发活动，同时大幅衰减后期非局部成分。
conclusion: 该方法通过电场建模增强EEG重建特异性，为提升TMS诱发的局部皮质反应时空间分辨率提供了新工具。
---

## 摘要
背景：经颅磁刺激与脑电图联用（TMS-EEG）正越来越多地整合到研究和临床方案中。然而，如何可靠地分离由TMS在目标皮层区域局部诱发的脑电反应，并避免污染源的影响，仍然具有挑战性。方法：本文介绍EPICURUS，一种新型TMS-EEG空间滤波方法，利用基于个体化MRI的TMS感应电场模拟来界定局部诱发活动的空间范围。该方法指导重建源自直接刺激部位的脑电信号，同时最大限度地减少远处非目标源的串扰。结果：在合成模拟和人类TMS-EEG数据集中，EPICURUS保留了早期潜伏期TMS诱发的局部活动，同时显著衰减了后期成分，这与抑制非局部活动相一致。结论：通过利用个体化电场模型的空间精度，EPICURUS可提高脑电信号重建的特异性，为改善TMS直接诱发的局部早期和晚期皮层反应时空分辨率提供了一种有前景的工具。

## Abstract
Background: The concurrent use of Transcranial magnetic stimulation and electroencephalography (TMS-EEG) is increasingly integrated into research and clinical protocols. However, a reliable isolation of EEG responses that are locally evoked by TMS at the targeted cortical sites independent from contaminating sources, remains challenging. Methods: Here we introduce EPICURUS, a novel spatial filtering approach for TMS-EEG that uses individualized MRI-based simulations of the TMS-induced electric field (E-field) to define the spatial extent of locally evoked activity. This method guides the reconstruction of EEG signals originating from the direct stimulation site while minimizing crosstalk from distant, non-targeted sources. Results: In synthetic simulations and a human TMS-EEG dataset, EPICURUS preserved early-latency TMS-evoked local activity while substantially attenuating later components, consistent with suppression of non-local activity. Conclusion: By leveraging the spatial precision of individualized E-field modeling, EPICURUS may enhance the specificity of EEG signal reconstruction, offering a promising tool for improving the spatiotemporal resolution of local early and late cortical local responses directly elicited by TMS.