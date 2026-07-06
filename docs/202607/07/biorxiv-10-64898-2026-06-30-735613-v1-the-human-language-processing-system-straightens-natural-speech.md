---
title: The human language processing system straightens natural speech
title_zh: 人类语言处理系统拉直自然语音
authors: "Xu, J., Nguyen, T. D., Tang, J., Huth, A. G., Goris, R. L. T."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.30.735613v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 测量言语处理中表征轨迹曲率的方法
tldr: 本研究探究时间预测目标如何塑造人脑语音表征。通过开发基于fMRI的轨迹曲率测量方法，结合单细胞与群体神经活动的时间尺度联系，发现听自然语音时脑响应轨迹在低级听觉区域最弯曲，并沿皮层层次逐渐拉直；wavLM模型验证了自然语音刺激的拉直效应最强。结果表明，预测目标促使神经表征轨迹平滑化，建立了预测目标、表征几何与皮层时间尺度层次间的直接联系。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究预测目标如何影响人脑语音表征的结构，检验表征轨迹沿语音处理层次被拉直的假说。
method: 开发基于fMRI的轨迹曲率测量方法，利用单细胞反应时间尺度与群体轨迹曲率的联系，分析听自然语音时的脑响应。
result: 人类听觉皮层响应轨迹沿层次逐渐拉直，且wavLM模型显示自然语音刺激的层次拉直效应最强。
conclusion: 时间预测目标促进神经语音表征的几何平滑化，建立了预测目标、表征几何与皮层时间尺度层次之间的直接关联。
---

## 摘要
在预测下一个词的任务上训练的大型语言模型具有令人印象深刻的语言能力。这表明时间预测的目标对语言处理至关重要，但这一目标如何影响人脑中语音表征的结构仍不清楚。在这里，我们检验了以下假设：预测通过沿语音处理层级对表征轨迹进行时间拉直而得到促进。我们开发了一种使用功能磁共振成像（fMRI）来测量这些轨迹曲率的方法。我们的方法利用了单细胞反应的时间尺度与群体轨迹曲率之间前所未知的联系。我们检查了被试在聆听自然语音时的大脑反应。反应轨迹在较低级听觉区域弯曲度最大，并沿皮层层级逐渐被拉直。我们将相同的语音刺激及其扰动版本呈现给wavLM——一个与人类大脑反应高度一致的语言表征模型——并发现，对于统计结构类似自然语音的刺激，层级拉直效应最强。综上所述，我们的结果在时间预测的目标、神经语音表征的几何结构以及表征时间尺度的皮层层级之间建立了直接的联系。

## Abstract
Large language models trained on next-word prediction have impressive linguistic capabilities. This suggests that the goal of temporal prediction is essential to language processing, but how this goal impacts the structure of speech representations in the human brain remains unknown. Here, we test the hypothesis that prediction is facilitated by the temporal straightening of representational trajectories along the speech processing hierarchy. We developed a methodology for measuring the curvature of these trajectories using fMRI. Our method exploits a previously unknown connection between the timescale of single-unit responses and the curvature of population trajectories. We examined brain responses of subjects listening to natural speech. Response trajectories were most curved in lower-level auditory areas and progressively straightened along the cortical hierarchy. We presented the same speech stimuli and perturbed versions thereof to wavLM--a speech representation model that is well aligned with human brain responses--and found that hierarchical straightening effects are strongest for stimuli whose statistical structure resembles natural speech. Together, our results establish a direct connection between the goal of temporal prediction, the geometry of neural speech representations, and the cortical hierarchy of representational timescales.