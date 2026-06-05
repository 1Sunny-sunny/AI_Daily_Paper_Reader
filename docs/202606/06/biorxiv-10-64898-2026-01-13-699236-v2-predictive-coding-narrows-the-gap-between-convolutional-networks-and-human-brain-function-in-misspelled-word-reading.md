---
title: Predictive coding narrows the gap between convolutional networks and human brain function in misspelled-word reading
title_zh: 预测编码缩小了卷积网络与人脑在拼写错误单词阅读中的功能差距
authors: "You, J., Salmelin, R., van Vliet, M."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.13.699236v2.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 利用预测编码解释CNN中类脑处理机制
tldr: 本研究探索预测编码能否解释人脑识别拼错词的鲁棒性及延迟。将预测编码动态融入卷积神经网络，用1000个芬兰语单词训练，并在真假拼错词刺激上评估，与人类脑磁图数据比较。结果表明，预测编码提升了模型对拼错词的表现，缩小了行为差距，且模型激活与大脑响应更一致，证实了预测编码作为大脑处理拼错词的生物学合理机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究预测编码是否可作为计算机制，解释人脑对拼错词的稳健识别及额外处理时间。
method: 将预测编码动态加入CNN，先监督训练分类，再无监督训练反馈重建，最后用拼错词刺激评估并与人类MEG数据对比。
result: 预测编码提升模型对拼错词性能，缩小真实词与拼错词准确率差距，并使模型激活与大脑MEG响应更相关。
conclusion: 预测编码动力学是大脑应对拼错词的生物学合理计算机制，验证了预测编码在词阅读中的作用。
---

## 摘要
人类能轻松识别拼写错误的单词，尽管反应会变慢。我们研究了预测编码是否可能作为一种可行的计算机制来解释这种鲁棒性及额外的处理时间。通过将受大脑启发的预测编码动力学引入卷积神经网络（CNN），我们评估了反馈预测与前馈误差之间的交互是否增强了模型在拼写错误单词阅读中与大脑的相似度。初始CNN通过监督学习训练，对1000个芬兰语单词的渲染文本图像进行分类，然后加入反馈预测编码连接，并以重建前一层活动的学习目标进行无监督训练。随后，用与人类参与者在脑磁图（MEG）记录中相同的真实和拼写错误单词刺激，对启用和未启用预测编码动力学的模型进行评估。预测编码动力学提高了模型在拼写错误单词上的表现，尤其缩小了真实单词与类似单词的拼写错误之间的准确率差距，从而使整体表现更接近人类行为模式。此外，表征相似性分析（RSA）和多元回归表明，当启用预测编码动力学时，模型激活与人类MEG响应之间的对应关系更强。这些发现为预测编码动力学作为一种生物学上合理的计算机制提供了多重证据，解释了大脑处理拼写错误单词的能力。

## Abstract
Humans can readily recognize words even when they are misspelled, though with slower responses. We investigated whether predictive coding could be a feasible computational mechanism to explain both the robustness and the additional processing time. By incorporating brain-inspired predictive coding dynamics into a convolutional neural network (CNN), we assessed whether the resulting interplay between feed-back predictions and feed-forward errors enhanced the model's brain-likeness in misspelled-word reading. The initial CNN was trained to classify images of rendered text from a 1000-word Finnish vocabulary (supervised), and then enhanced with feedback predictive coding connections, which were trained with the learning objective of reconstructing the activity in the previous layer (unsupervised). The model, with and without the predictive coding dynamics enabled, was then evaluated using the same real and misspelled word stimuli that were presented to human participants during a magnetoencephalography (MEG) recording. The predictive coding dynamics improved model performance on misspelled words, particularly reducing the accuracy gap between real and word-like misspelled words, thereby aligning overall performance more closely with human behavioral patterns. Furthermore, representational similarity analysis (RSA) and multivariate regression showed a stronger correspondence between model activations and human MEG responses when predictive coding dynamics were enabled. These findings provide converging evidence for predictive coding dynamics as a biologically plausible computational mechanism for the brain's ability to cope with misspelled words.