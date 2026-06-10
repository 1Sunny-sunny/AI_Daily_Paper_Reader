---
title: "Beyond the Canonical HRF: Flexible Temporal Modeling Reveals Unconstrained BOLD Profiles During Naturalistic Viewing"
title_zh: 超越经典HRF：灵活的时间建模揭示自然观看下无约束的BOLD响应曲线
authors: "Di, X., Hanna, G. B., Biswal, B. B."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.07.687226v3.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: BOLD信号的灵活时间建模
tldr: 自然观影fMRI研究中，特征与BOLD响应的时间延迟多变，标准HRF可能引入错位。本研究利用互相关和FIR反卷积分析三个数据集，发现标准HRF对瞳孔大小和心智理论等延迟信号产生双重延迟，而FIR模型揭示了跨皮层的时间层级，强调了灵活时间建模对准确映射复杂处理动态的必要性。
source: biorxiv
selection_source: fresh_fetch
motivation: 标准HRF无法充分捕获自然刺激中特征与BOLD响应之间多变的时间延迟。
method: 使用互相关与有限脉冲响应（FIR）反卷积分析三个电影观看数据集的视觉、听觉、瞳孔和心智理论特征的时间动态。
result: 标准HRF对生理延迟信号引入双重延迟，而FIR模型揭示了跨皮层区域的时间层级。
conclusion: 灵活的时间建模对准确映射自然观看过程中的复杂时间尺度至关重要。
---

## 摘要
自然刺激，如电影和叙事，越来越多地被用于认知神经科学，以将认知和情感过程映射到功能磁共振成像（fMRI）测量的大脑活动上。从电影中提取的特征跨越多个层次，从计算视觉和听觉输入到生理信号和主观评分。然而，这些特征与血氧水平依赖（BOLD）响应之间的时间对齐差异很大，常用的带有时间导数的经典血流动力学响应函数（HRF）可能无法充分捕捉这些延迟。在本研究中，我们使用互相关和有限脉冲响应（FIR）反卷积分析了三个观影数据集，以绘制视觉、听觉、瞳孔和心理理论（ToM）特征在整个大脑中无约束的时间动态。我们的结果表明，虽然经典HRF能有效捕捉基本感觉特征，但对于固有延迟的信号会引入系统性的错位。由于生理标记（瞳孔大小）和受试者报告（ToM）本身滞后于潜在的神经事件，标准的HRF卷积过度补偿了它们的生物延迟，引入了冗余的相位不匹配或“双重延迟”。此外，我们的无约束FIR模型揭示了皮层间明显的区域间时间层次。认识到现实世界刺激固有的共线性，这些估计的曲线捕捉了自然主义处理中捆绑的多维动态，而非完美隔离的特征效应。最终，这些发现强调了采用灵活、经过可靠性检验的时间建模对于准确绘制自然观看过程中涉及的复杂处理时间尺度的必要性。

## Abstract
Naturalistic stimuli, such as movies and narratives, are increasingly used in cognitive neuroscience to map cognitive and affective processes onto brain activity measured with functional MRI (fMRI). Features extracted from movies span multiple levels, from computational visual and auditory inputs to physiological signals and subjective ratings. However, the temporal alignment between these features and the blood-oxygen-level-dependent (BOLD) response varies considerably, and the commonly used canonical hemodynamic response function (HRF) with temporal derivatives may not adequately capture these delays. In this study, we analyzed three movie-watching datasets using cross-correlation and finite impulse response (FIR) deconvolution to map the unconstrained temporal dynamics of visual, auditory, pupillary, and Theory of Mind (ToM) features across the brain. Our results demonstrate that while the canonical HRF effectively captures basic sensory features, it introduces systematic misalignments for inherently delayed signals. Because physiological markers (pupil size) and subject reports (ToM) intrinsically lag the underlying neural events, standard HRF convolution overcompensates for their biological latency, introducing a redundant phase mismatch or "double-delay." Furthermore, our unconstrained FIR models revealed distinct inter-regional temporal hierarchies across the cortex. Recognizing the inherent collinearity of real-world stimuli, these estimated profiles capture the bundled, multi-dimensional dynamics of naturalistic processing rather than perfectly isolated feature effects. Ultimately, these findings highlight the necessity of flexible, reliability-tested temporal modeling to accurately map the complex processing timescales engaged during naturalistic viewing.