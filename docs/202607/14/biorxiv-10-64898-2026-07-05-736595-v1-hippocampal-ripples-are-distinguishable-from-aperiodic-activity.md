---
title: Hippocampal ripples are distinguishable from aperiodic activity
title_zh: 海马波纹与非周期性活动是可区分的
authors: "Kragel, J. E."
date: 2026-07-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.05.736595v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 改进海马尖波检测区分非周期性活动
tldr: 海马体高频涟漪振荡对学习记忆至关重要，但有观点认为清醒人类记录中检测到的涟漪可能是算法将无周期性（1/f）活动误判的假阳性。本研究通过模拟实验发现，该结论源于检测算法在仅含无周期性活动的替代数据上评估时阈值偏移导致误报率虚高。将真实涟漪事件添加回替代数据可纠正阈值并消除大多数误检。多变量分类器进一步表明无周期性活动能模拟涟漪的功率但无法模拟其时序和频谱特征。结果证明，在真实信号条件下，人类海马涟漪可与无周期性活动可靠区分，但需注意替代数据的正确使用。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736595-v1/fig-001.webp\", \"caption\": \"Figure 1. Excluding ripples from surrogate distributions inflates false detections. (A) Schematic illustrating ripple detection under 1/f-only (top) and mixed (bottom) regimes. In 1/f-only data, threshold crossings reflect aperiodic fluctuations, whereas in mixed data they reflect a combination of aperiodic fluctuations and ripples. (B) Representative hippocampal power spectrum (example contact from Study 1) showing localized ripple-band power above the fitted aperiodic (1/f) background in direct recordings (bottom) but not in matched aperiodic simulations (top). (C) Reduction in false detections when matched ripple-band events are restored to the surrogate, for each of the five detection algorithms. Points are individual channels (N = 99). Black markers show the median ±95% CIs. (D) Across channels, greater variability in ripple-band event amplitudes was associated with a larger shift in the detection threshold. (E) Larger threshold shifts removed a greater fraction of false detections. The fraction of surrogate detections surviving the inclusion of ripple-band events declined with the magnitude of the threshold shift. Points denote individual channels and shaded regions denote 95% CIs of predictions.\", \"page\": 2, \"index\": 1, \"width\": 1026, \"height\": 397}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736595-v1/fig-002.webp\", \"caption\": \"Figure 2. Detected ripple events are distinguishable from aperiodic surrogates. (A) Receiver operating characteristic curve for leave-one-subject-out cross-validation (detector 3). Shaded region shows the 95% CI (subject-level bootstrap). (B) Feature contribution, quantified as the drop in cross-subject AUC when each feature is removed. Error bars denote 95% CI. (C) Mean duration and peak frequency for real and surrogate events per channel (colored points). Black markers show group means, with lines denoting 95% CI.\", \"page\": 3, \"index\": 2, \"width\": 1023, \"height\": 309}]"
motivation: 验证清醒状态下检测到的海马涟漪是否仅为无周期性活动的误检产物。
method: 通过向替代数据中添加真实涟漪事件来纠正检测阈值，并结合多变量分类器比较涟漪与无周期性活动在功率、时序和频谱上的差异。
result: "仅有无周期性活动的替代数据导致误报率中位数达62%，加入真实事件后误检大幅减少；无周期性活动能再现功率谱但无法模拟时序和频谱特征。"
conclusion: 真实信号中人类海马涟漪确实可与无周期性活动区分，但在使用替代数据评估检测算法时需避免阈值偏移导致的误判。
---

## 摘要
高频“波纹”振荡在跨物种的学习和记忆中起支持作用，然而有观点认为，在清醒人类记录中检测到的所谓波纹是算法误将非周期性（1/f）波动识别为波纹频段振荡而产生的假阳性。我们证明，这一结论源于在仅含非周期性活动的替代数据上评估检测算法时产生的假象。波纹检测器具有自适应性，根据信号的幅度统计设定阈值，因此将其应用于仅含非周期性活动的替代数据会降低阈值并增加假阳性（中位数62%）。将真实的波纹频段事件重新加入替代数据可纠正这一阈值偏移，并在多个标准算法中消除大多数错误检测。通过多变量分类器，我们发现非周期性波动可以再现波纹的功率，但无法再现其时序或频谱内容。这些发现表明，在使用替代数据评估波纹检测算法时需要谨慎。因此，在现实的信号特性下，人类海马波纹仍可与非周期性活动区分开来。

## Abstract
High-frequency "ripple" oscillations support learning and memory across species, yet it has been argued that putative ripples in awake human recordings are false positives produced when algorithms misread aperiodic (1/f) fluctuations as ripple-band oscillations. We show that this conclusion arises from an artifact of evaluating detection algorithms on surrogate data containing only aperiodic activity. Ripple detectors are adaptive, setting their threshold from the amplitude statistics of the signal, so applying them to surrogate data that contains only aperiodic activity lowers the threshold and inflates false positives (median 62%). Adding real ripple-band events back to the surrogate corrects this threshold shift and eliminates most false detections across multiple standard algorithms. Using multi-variate classifiers, we show aperiodic fluctuations can reproduce the power of ripples but not their timing or spectral content. These findings indicate care needs to be taken when using surrogates to evalute ripple detection algorithms. Thus, under realistic signal properties, human hippocampal ripples remain distinguishable from aperiodic activity.