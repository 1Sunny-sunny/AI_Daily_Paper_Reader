---
title: Next-Generation Neural Mass Models Reproduce Features of Speech Processing
title_zh: 新一代神经群模型再现语音处理特征
authors: "Shannon, A. J., Barton, D. A. W., Homer, M., Houghton, C. J."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.20.683434v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 神经群体模型复制语音处理特征，将外部刺激与神经活动联系起来
tldr: 语音分割为音节依赖于神经活动与语音节奏的同步，但其皮层回路机制尚不明确。本研究采用下一代生物物理神经群体模型，对比现象学模型，通过四项测试评估其再现语音追踪特征的能力。结果表明，该模型通过阈值相位重置对语音包络锐利起始的响应，产生跨频率嵌套振荡，自然再现了锐度调谐的追踪和事件间相位相干性的双峰特征，为从神经群体振荡到音节分割的认知计算提供了机制桥梁。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示语音音节分割背后的皮层神经回路机制。
method: 使用生物物理神经群体模型，以现象学模型为基线，通过四项计算测试（锐度-追踪相关性、相位集中度、音节速率影响、事件间相位相干性）评估模型动力学。
result: 神经群体模型通过阈值相位重置触发跨频率嵌套振荡，再现了锐度调谐的节奏追踪和实验观察的双峰相位相干性特征。
conclusion: 神经群体模型提供了连接听觉皮层振荡动力学与语音追踪认知计算的机制性解释，并解释了连续语音中离散事件表征的产生。
---

## 摘要
音节分离是神经语音处理的关键步骤，依赖于神经活动与语音节奏结构的对齐。两种竞争假说解释了这种神经语音追踪：相位重置和诱发反应。虽然对这些假说的现象学建模已取得成效，但我们仍缺乏对底层皮层回路机制的理解。为探索这些机制，我们以竞争假说的现象学模型为算法基线，评估了生物物理的新一代神经群模型是否能再现神经语音追踪的多种特征。我们通过四项测试考察模型动态：在计算机中重现了一项将追踪强度与音素锐度关联起来的脑电图实验，计算了相位集中度指标，测试了不同音节速率的效果，并评估了音素起始点间的跨事件相位相干性。我们研究的所有模型都再现了锐度调谐的节律性语音追踪，但诱发模型需要预处理的声学边缘脉冲刺激。我们证明，神经群模型是通过连续语音包络中尖锐起始点触发的阈值化相位重置来运作的。这产生了跨频率嵌套振荡，其在定性上匹配了实验观察到的跨事件相位相干性中的双峰特征。我们的结果表明，生物物理神经群模型在皮层群体的通用振荡动态与语音追踪的认知计算之间架设了一座机制桥梁。事实上，神经群模型的非线性动态解释了听觉皮层活动中如何响应连续声学输入而产生峰值率事件表征。意义陈述：音节分离至关重要但极具挑战性，因为自然语音缺乏明确边界，然而人类却能毫不费力地完成这一计算。语音将神经活动与音节节律对齐，从而预测音节时机，但底层皮层机制仍未知。将这种宏观行为与神经生物学联系起来颇具挑战，但新一代神经群模型有望解决这一问题。我们展示了这些模型能再现锐度调谐的追踪和声学边缘提取。动态分析表明这是通过对音素起始点进行阈值化相位重置，触发跨频率嵌套振荡来实现的。我们的结果既推进了对音节分离的生物物理学理解，也验证了该模型模拟宏观神经活动的能力。这些模型在听觉皮层神经生物学与语音处理动态之间架起了一座现象学模型无法提供的桥梁。

## Abstract
Segregation of speech into syllables is a key step in neural speech processing. It relies on the alignment of neural activity with the rhythmic structure of speech. Two competing hypotheses explain this  neural speech tracking, phase-resetting and evoked responses. While phenomenological modelling of these hypotheses has been successful, we still lack understanding of the underlying cortical circuits. To investigate these mechanisms, we evaluate whether a biophysical next-generation neural mass model can reproduce several features of neural speech tracking, using phenomenological models of the competing hypotheses as algorithmic baselines. We investigate the models dynamics with four tests: recreating in-silico an EEG experiment that identified a correlation between tracking strength and phoneme sharpness, computing the Phase Concentration Metric, testing the effect of varying syllabic rates, and evaluating the Inter Event Phase Coherence across phoneme onsets. While all of the models that we study reproduce the sharpness-tuned rhythmic speech tracking, the evoked model requires a pre-processed acoustic edge impulse stimulus. We demonstrate that the neural mass model is performing thresholded phase-resetting triggered by sharp onsets in the continuous speech envelope. This produces cross-frequency nested oscillations that qualitatively match an experimentally-observed dual-peak signature in the Inter Event Phase Coherence. Our results indicate that the biophysical neural mass model provides a mechanistic bridge between generic oscillatory dynamics in cortical populations and the cognitive computations of speech tracking. Indeed, the non-linear dynamics of the neural mass model offer an explanation for how peak-rate event representations in auditory cortex activity arise in response to continuous acoustic input.

Significance StatementSyllable segregation is crucial but challenging as natural speech lacks clear boundaries, yet humans perform this computation effortlessly. Speech aligns neural activity to syllabic rhythms, predicting syllable timing, but the underlying cortical mechanisms remain unknown. Relating this macroscopic behaviour to neurobiology is challenging; however, next-generation neural mass models promise to resolve this. We demonstrate that these models reproduce sharpness-tuned tracking and acoustic edge extraction. Dynamical analyses indicate this occurs through thresholded phase-resetting to phoneme onsets, triggering cross-frequency nested oscillations. Our results both advance biophysical understanding of syllable segregation and validate the models capacity for simulating macroscopic neural activity. These models offer a bridge between the neurobiology of the auditory cortex and speech processing dynamics that phenomenological models cannot provide.