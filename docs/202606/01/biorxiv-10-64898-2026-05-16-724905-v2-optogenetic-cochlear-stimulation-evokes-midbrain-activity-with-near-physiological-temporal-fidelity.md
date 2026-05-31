---
title: Optogenetic cochlear stimulation evokes midbrain activity with near-physiological temporal fidelity
title_zh: 光遗传学耳蜗刺激以接近生理的时序保真度唤起中脑活动
authors: "Koert, E., Götz, J., Albrecht, N., Vavakou, A., Wolf, B. J., Moser, T."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.16.724905v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 评估光遗传耳蜗刺激在中脑的瞬时保真度
tldr: 为解决电耳蜗植入因电流扩散导致频率编码受限的问题，本研究在蒙古沙鼠中评估了快速关闭通道视紫红质 f-Chrimson 用于光遗传耳蜗刺激的时间编码能力。通过记录下丘神经活动，发现 f-Chrimson 能以低微焦能量阈值实现≥150 Hz 的高效刺激，动态范围和频率选择性均优于电刺激，且不损害时间编码。该结果表明快速门控 ChR 能兼顾频谱与时间保真度，为光学耳蜗植入提供生理级时间编码。
source: biorxiv
selection_source: fresh_fetch
motivation: 电耳蜗植入的电流扩散限制频率编码，而光遗传刺激中慢通道视紫红质可能损害时间编码，需要验证快速 ChR 能否兼具高频谱选择性与时间保真度。
method: 利用 f-Chrimson 介导的光遗传刺激蒙古沙鼠耳蜗，通过多电极阵列记录下丘神经响应，并与声刺激、CatCh/ChReef光刺激及电刺激比较。
result: f-Chrimson 在≥150 Hz 速率下实现能量高效刺激，动态范围和频率选择性与 CatCh 相当，并显著优于电刺激。
conclusion: 快速关闭的 f-Chrimson 实现了近生理的时间保真度，证明光学耳蜗植入可在不牺牲时间编码的情况下增强频谱编码。
---

## 摘要
当听力受损时，电人工耳蜗（eCI）对听神经的刺激可部分恢复听力，大多数eCI使用者能够实现开放式言语理解。然而，每个电极的电流扩散范围大，限制了频率编码和在背景噪声环境下的言语理解。未来光人工耳蜗（oCI）的空间受限光遗传学刺激可改善频率编码，但通道视紫红质（ChRs）毫秒级的关闭动力学会限制时间编码。本研究评估了快速关闭的f-Chrimson在蒙古沙鼠听觉系统中处理时间信息的效用。我们记录了下丘中由f-Chrimson介导的耳蜗光遗传学刺激所诱发的神经活动。f-Chrimson能够以≥150 Hz的速率高效节能地刺激听觉通路，优于较慢的ChR变体CatCh（蓝光）和ChReef（绿光）。激活听觉通路的能量阈值在低微焦范围，介于ChReef（亚微焦）和CatCh之间。动态范围和频率选择性与以往CatCh的观察结果相当，并优于电刺激。总之，采用快速门控的ChRs可在不降低时间编码的前提下实现改进的频谱编码。

论文解析

问题：电人工耳蜗（eCI）使大多数原本重度聋的百万患者部分恢复了言语理解能力。然而，大多数CI使用者在日常情境中面临听觉挑战。通过光人工耳蜗（oCI）对听神经进行频谱选择性更高的刺激有望克服这一局限性。但是，通道视紫红质（ChR）的关闭动力学会限制仿生声音编码的时间带宽。改进ChR特性并评估时间编码仍是发展oCI听力恢复的主要目标。

结果：本研究通过中脑多电极阵列（MEA）记录，评估了基于波导的oCI使用快速关闭ChR Chrimson（f-Chrimson）编码时间、频谱和强度信息的效用。我们将f-Chrimson介导的仿生编码与声学编码以及以往使用其他ChRs的光遗传学刺激和电刺激数据进行了比较。f-Chrimson能够以≥150 Hz的速率高效节能地刺激听觉通路，优于较慢的ChR变体CatCh（蓝光）和ChReef（绿光）。强度和频率编码与以往CatCh的观察结果相当，并优于电刺激。

影响：本研究展示了快速关闭ChR f-Chrimson接近生理的时间编码能力，表明oCI改进的频谱编码不会因时序保真度差而打折扣。

## Abstract
When hearing fails, stimulation of the auditory nerve by electrical cochlear implants (eCIs) partially restores hearing, with most eCI users achieving open speech understanding. However, the broad current spread from each electrode limits frequency coding and speech understanding in daily situations with background noise. Spatially confined optogenetic stimulation by future optical cochlear implants (oCIs) improves frequency coding but millisecond closing kinetics of channelrhodopsins (ChRs) might limit temporal coding. Here, we evaluated the utility of fast-closing f-Chrimson for processing temporal information in the auditory system of Mongolian gerbils. We recorded neural activity in the inferior colliculus evoked by f-Chrimson-mediated optogenetic stimulation of the cochlea. F-Chrimson enabled energy-efficient stimulation of the auditory pathway at rates [&ge;]150 Hz, outperforming the slower ChR variants CatCh (blue) and ChReef (green). Energy thresholds for activation of the auditory pathway were in the low {micro}J range, between ChReef (sub-{micro}J) and CatCh. Dynamic range and frequency selectivity were comparable to previous observations with CatCh and outperformed electrical stimulation. In conclusion, employing fast-gating ChRs harnesses improved spectral coding without degrading temporal coding.

The Paper Explained

ProblemElectrical cochlear implants (eCIs) partially restore speech comprehension in most of 1 million otherwise severely deaf people. However, most CI-users face challenges hearing in daily situations. Spectrally more selective stimulation of the auditory nerve by optical cochlear implants (oCIs) promises to overcome this limitation. However, the closing kinetics of channelrhodopsins (ChR) limit the temporal bandwidth of bionic sound coding. Improving the ChR properties and evaluating temporal coding remain major objectives for developing hearing restoration by oCI.

ResultsHere, we evaluate the utility of waveguide-based oCI using the fast-closing ChR Chrimson (f-Chrimson) for encoding of temporal, spectral and intensity information by multi-electrode-array (MEA) recordings from the midbrain. We compare f-Chrimson-mediated bionic coding to acoustic coding as well as to previous data acquired with optogenetic stimulation using other ChRs and with electrical stimulation. F-Chrimson enabled energy-efficient stimulation of the auditory pathway at rates [&ge;]150 Hz, outperforming the slower ChR variants CatCh (blue) and ChReef (green). Intensity and frequency coding were comparable to previous observations with CatCh and outperformed electrical stimulation.

ImpactThis study demonstrates near physiological temporal coding with the fast-closing ChR f-Chrimson, indicating that improved spectral coding by oCI is not traded off by poor temporal fidelity.