---
title: Cortical encoding of probabilistic temporal predictions during speech perception
title_zh: 言语感知过程中概率性时间预测的皮层编码
authors: "Deyna, L., Albouy, P., Trebuchon, A., Schon, D., Morillon, B., Guilleminot, P. H."
date: 2026-08-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.08.16.745095v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 通过预测模型将语音的时间统计与皮层编码联系起来
tldr: 该研究超越传统以平均速率描述语音时间结构的视角，利用大型语料训练模型预测音素、音节和词的起始，发现RNN能捕捉上下文相关的概率时间结构。结合53名患者颅内记录，模型输出的连续起始概率在声学和语言内容之外显著解释神经活动，且与内容编码分离，涉及广泛皮层网络。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统语音时间结构仅以平均速率概括，忽略了上下文依赖的精细概率时间结构及其在听觉预测编码中的作用。
method: 使用英法语大型语音语料训练不同复杂度模型预测语言单位起始，并在53名患者颅内电极记录中检验模型概率对神经活动的额外解释力。
result: RNN优于平均速率和风险率模型，其输出的起始概率在声学和语言内容特征之外解释神经活动，且时间预测与内容编码依赖不同脑区。
conclusion: 语音中的时间预测是一个动态、上下文依赖且概率性的独立过程，由分布式皮层网络支持。
---

## 摘要
言语的时间结构传统上通过其规范语言单位（音素、音节、词）的节律性来刻画，每种单位以平均出现率来概括。这一观点虽合理，却忽视了言语是否携带更精细、依赖语境且具概率性的时间结构，从而能在聆听过程中支持时间预测编码。利用大型法语和英语语音语料库，我们训练了复杂度递增的模型来预测语言单位的起始点。循环神经网络（RNN）优于平均率模型和风险率模型，表明围绕这些率的变异并非噪声，而是由局部语境塑造的时间结构，可在音素、音节和词层面被统计预测。接下来，通过记录53名神经外科患者在聆听自然言语时的7698个颅内电极信号，我们表明模型的输出——即将到来的起始点的连续概率（何时）——在声学和语言内容（什么）特征之外解释神经活动，且RNN的效果显著强于平均率或风险率模型。这种关于起始点何时发生的动态神经预测与语言内容的编码可分离，依赖大致不同的通道群体。时间预测涉及一个分布式的皮层网络，从双侧颞叶皮层延伸至左侧额叶和感觉运动区域。总之，这些结果确立了言语中的时间预测本身就是一个动态、依赖语境且具概率性的过程。

## Abstract
The temporal structure of speech has traditionally been characterized by the rhythmicity of its canonical linguistic units (phonemes, syllables, words), each summarized by a mean occurrence rate. While valid, this view overlooks whether speech carries a finer, context-dependent and probabilistic temporal structure that could support temporal predictive coding during listening. Using large French and English speech corpora, we trained models of increasing complexity to predict the onsets of linguistic units. Recurrent neural networks (RNNs) outperform mean-rate and hazard-rate models, showing that the variability around these rates is not noise but a temporal structure shaped by local context, statistically predictable across phonemes, syllables and words. Recording from 7,698 intracerebral electrodes in 53 neurosurgical patients listening to natural speech, we next show that the models' output), the continuous probability of an upcoming onset (when), explains neural activity beyond acoustic and linguistic content (what) features, with markedly stronger effects for RNNs than for mean- or hazard-rate models. This dynamic neural prediction of when an onset will occur is dissociable from the encoding of linguistic content, relying on largely distinct channel populations. Temporal predictions engage a distributed cortical network extending from bilateral temporal cortex into left frontal and sensorimotor regions. Together, these results establish temporal prediction in speech as a dynamic, context-dependent and probabilistic process in its own right.