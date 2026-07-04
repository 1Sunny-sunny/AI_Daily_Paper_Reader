---
title: Closed-loop optimization of a high-dimensional generative latent space for rhythmic visual response
title_zh: 针对节律性视觉反应的高维生成潜在空间的闭环优化
authors: "Livezey, J. A., Su, Y., Wolfer, S., Ingster, A., Klein, D. J., Hanina, A."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.27.734819v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用非侵入式EEG闭环比调制SSVEP以控制视觉神经反应
tldr: 神经振荡调制对认知和临床研究意义重大。本研究提出一种闭环优化方法，利用非侵入脑电图测量稳态视觉诱发电位（SSVEP），在生成模型的高维潜在空间中调节视觉刺激参数，成功实现对alpha和theta节律相对功率的调制。优化后的刺激可泛化至新被试，并揭示图像低频空间功率驱动两个频段呈相反方向变化。该工作证明闭环优化是可行的非侵入节律神经调制途径。
source: biorxiv
selection_source: fresh_fetch
motivation: 节律性神经振荡的闭环调制日益重要，但现有方法依赖侵入式记录且未聚焦节律调制。
method: 采用非侵入脑电图测量SSVEP，通过闭环优化生成式高维潜在空间中的图像刺激参数来调节节律响应。
result: 在10、20、40维潜在空间中实现SSVEP功率闭环调制，优化刺激可泛化，且低频空间功率驱动theta与alpha反向变化。
conclusion: 闭环刺激优化是一种使用非侵入神经成像进行节律神经调制的可行方法。
---

## 摘要
神经振荡伴随着广泛的认知状态和行为，包括感知、记忆和运动，对其进行调节在基础神经科学和临床研究中日益受到关注。以往关于视觉神经反应闭环调节的演示主要依赖于侵入性记录，并侧重于放电率最大化，而非节律性调节。这里，我们展示了稳态视觉诱发电位（SSVEP）的相对功率，通过易于获取的非侵入性脑电图测量，可以在单一会话内针对单个参与者，作为图像刺激参数的函数进行闭环调节。在alpha和theta频带的闪烁频率下，刺激优化在10维、20维和40维潜在空间中均取得成功。我们还表明，优化后的刺激在开环呈现时能够泛化到新的参与者。最后，我们表征了调节相对SSVEP功率的视觉特征，并发现图像中的低频空间功率驱动theta和alpha向相反方向变化。总之，我们的结果表明，闭环刺激优化是一种使用非侵入性神经成像方法进行节律性神经调节的可行方法。

## Abstract
Neural oscillations accompany a wide range of cognitive states and behaviors including perception, memory, and movement, and modulating them is of growing interest for both basic neuroscience and clinical research. Previous demonstrations of closed-loop modulation of visual neural responses mainly relied on invasive recordings and focused on firing-rate maximization rather than rhythmic modulation. Here, we show that the relative power of steady-state visual evoked response (SSVEP), measured with readily-available, non-invasive electroencephalography, can be modulated in closed-loop as a function of image stimulus parameters for single participants within a single session. Stimulus optimization with flicker frequencies in the alpha and theta bands was successful in 10, 20, and 40 dimensional latent spaces. We also show that optimized stimuli generalize to new participants when shown in open-loop. Finally, we characterize the visual features that modulate relative SSVEP power and find that low-frequency spatial power in the image drives theta and alpha in opposite directions. Together, our results show that closed-loop stimulus optimization is a viable method for rhythmic neural modulation using noninvasive neuroimaging methods.