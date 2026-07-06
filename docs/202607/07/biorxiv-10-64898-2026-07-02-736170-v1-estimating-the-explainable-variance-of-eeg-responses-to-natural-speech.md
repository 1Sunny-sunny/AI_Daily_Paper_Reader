---
title: Estimating the Explainable Variance of EEG Responses to Natural Speech
title_zh: 估计自然语音 EEG 响应的可解释方差
authors: "Dou, J., Lalor, E."
date: 2026-07-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736170v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 将脑电反应与语音特征关联的数学框架（可解释方差）
tldr: 理解大脑如何处理自然语音中，EEG建模进展显著，但缺乏衡量模型解释力的标准。本研究假设最佳模型为他人听同样语音的EEG，通过构建19名被试的被试间模型，估计EEG反应的总可解释方差。发现基于声学与语言特征的线性模型能解释大部分但非全部方差，为语音神经处理研究提供了基准。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究EEG对自然语音的反应中有多少方差源自语音输入，以定义好模型的标准。
method: 假设最优模型为其他被试的EEG，利用被试间预测和外推估计总可解释方差。
result: 常用特征模型可预测大部分但非全部可解释方差，存在未解释成分。
conclusion: 现有模型虽有效，但仍有改进空间，需考虑额外因素以完全解释EEG对语音的反应。
---

## 摘要
近年来，人们在理解人脑如何解析和处理自然语音方面取得了实质性进展。这些进展很大程度上建立在脑活动与语音不同声学和语言特征之间关系的建模之上。通过基于这些特征拟合和测试模型，可以检验关于大脑将语音转化为理解所使用的计算和表征类型的假设。尽管大多数工作集中在使用功能性神经影像或颅内记录的电生理信号来建模 BOLD 活动，但该方法也被证明对 MEG 和 EEG 有效。事实上，无创 EEG 在转化研究和应用方面，对研究语音处理具有某些优势。过去十年左右的研究表明，EEG 可以基于大量声学、语言和副语言语音特征成功建模。然而，一个重要的未解问题笼罩着所有这些工作：即什么构成了自然语音 EEG 响应的良好模型？或者，换句话说，在自然语音聆听过程中记录的 EEG 中，有多大比例的方差可解释为源自该语音输入？本研究旨在解决这一问题。我们基于这样的假设进行：对一个人自然语音 EEG 响应的最佳模型，是其他聆听相同语音的个体的 EEG 响应集合。利用这一假设，我们使用 19 名健康成人英语母语者（均聆听同一本有声书）的 EEG，构建了受试者间模型。每个受试者的模型涉及使用来自不同数量其他受试者的（降维后）EEG 来预测其自身 EEG 数据，然后通过外推来估计目标个体对语音响应的总可解释方差。随后，我们表明，基于几个常用声学和语言语音特征的线性模型（时间响应函数）可以预测受试者间 EEG 响应估计总可解释方差的大部分——但重要的是，并非全部。

## Abstract
Substantial progress has been made in recent years on understanding how the human brain parses and processes natural speech. Much of this progress has been based on modeling how brain activity relates to the different acoustic and linguistic features of speech. By fitting and testing models based on those features, one can test hypotheses about the kinds of computations and representations the brain uses to convert speech sounds into understanding. While much of this work has focused on modeling BOLD activity using functional neuroimaging or intracranially recorded electrophysiological signals, the approach has also proven useful with MEG and EEG. Indeed, noninvasive EEG has certain advantages for studying speech processing in terms of translational research and application. Research over the last decade or so has shown that EEG can be successfully modeled based on numerous acoustic, linguistic, and paralinguistic speech features. However, an important unanswered question hangs over all of this work: namely, what constitutes a good model of EEG responses to natural speech? Or, to put it another way, how much variance in EEG recorded during natural speech listening is explainable as having derived from that speech input? The present study aims to tackle this issue. We do so under the assumption that the best model for a person's EEG response to natural speech is a set of EEG responses from other people listening to the same speech. Using this assumption, we construct inter-subject models using EEG from 19 healthy adult native speakers of English who all listened to the same audiobook. The model for each subject involves predicting their EEG data using (dimensionality-reduced) EEG from different numbers of other subjects and then extrapolating to estimate the total explainable variance in the target individual's response to speech. Following this, we show that linear models (temporal response functions) based on several commonly used acoustic and linguistic speech features can predict most - but importantly not all - of the estimated total explainable variance in EEG responses across subjects.