---
title: Exploring the functionality of market-available tools for neural recording
title_zh: 探索市面上可用的神经记录工具的功能性
authors: "Esmaeilzadeh, K., Hosseini, M., Etghani, S. A., Vahabie, A., Yekani, M."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.20.720337v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 模块化神经记录平台
tldr: 该研究针对神经电生理记录系统依赖于专用硬件、灵活性不足的问题，开发并评估了一个完全由市售组件构建的模块化神经记录平台。通过与地面真值对比，平台在多数配置下成功恢复局部场电位波形，并在直接连接记录中检测到尖峰活动；主成分分析与k均值聚类可区分模拟尖峰波形。尽管存在采样率和噪声方面的局限，该工作验证了利用通用硬件构建低成本、模块化神经记录系统的可行性，为未来定制化开源方案提供了基础框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 为降低神经电生理研究的门槛，需开发低成本、开源且高度模块化的记录系统，以克服现有平台对专用硬件的依赖和灵活性不足的问题。
method: 构建一个完全由市售组件组成的模块化神经记录平台，并通过与地面真值信号对比，评估其在局部场电位和尖峰记录中的性能。
result: 平台在多数条件下可恢复局部场电位样波形，直接连接时能检测尖峰活动，PCA和k均值聚类可区分多个模拟尖峰，但盐水和前置放大器配置会引入额外噪声、降低信号质量。
conclusion: 该平台证明了使用通用硬件搭建可定制神经记录系统的可行性，虽在采样率和噪声等指标上仍有不足，但为未来开源神经记录研究提供了实用基础。
---

## 摘要
低成本且开源的神经记录系统对于扩大电生理学研究的可及性日益重要。然而，许多现有平台仍然依赖专用硬件或模块化程度有限，限制了寻求可定制解决方案的实验室的灵活性。在此，我们开发并评估了一个完全由市售组件构建的模块化神经记录平台。我们将记录数据与真实信号进行了对比。该平台在大多数条件下成功恢复了类似局部场电位（LFP）的波形，并在直接连接记录中检测到锋电位样活动。主成分分析和 k 均值聚类进一步证明了区分多个模拟锋电位波形的能力。信号质量因配置而异，盐水记录和前置放大器集成会引入更多噪声并降低可检测性。这些发现证明了使用广泛可得的硬件构建经济实惠且模块化的电生理学系统的可行性。尽管当前实现在采样率、噪声性能和体内验证方面存在局限性，但所提出的框架为未来可定制的开源神经记录提供了实用基础。

## Abstract
Low-cost and open-source neural recording systems are increasingly important for expanding access to electrophysiological research. However, many existing platforms still rely on specialized hardware or limited modularity, restricting flexibility for laboratories seeking customizable solutions. Here, we developed and evaluated a modular neural recording platform constructed entirely from commercially available components. Recordings were compared against the ground truth. The platform successfully recovered local field potential (LFP)-like waveforms in most conditions and detected spike-like activity during direct connection recordings. Principal component analysis and k-means clustering further demonstrated the ability to distinguish multiple simulated spike waveforms. Signal quality varied across configurations, with saline recordings and preamplifier integration introducing increased noise and reduced detectability. These findings demonstrate the feasibility of building affordable and modular electrophysiology systems using widely accessible hardware. Although the current implementation has limitations in sampling rate, noise performance, and in vivo validation, the presented framework provides a practical foundation for future customizable open-source neural recording.