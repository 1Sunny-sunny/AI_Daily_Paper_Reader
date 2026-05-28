---
title: Random network structure stabilizes neural manifolds
title_zh: 随机网络结构稳定神经流形
authors: "Eppler, J.-B., Galella, S., Mel, G. C., Roxin, A."
date: 2026-05-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.21.726949v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 研究神经群体表征在漂移中的稳定性
tldr: 神经活动模式持续变化（表征漂移），但群体表征的相似结构却保持稳定。本研究发现，这种稳定性是随机连接网络的内在特性：输出相似性仅取决于输入相似性，与具体连接无关。漂移动态仅驱动网络在不同随机实例间切换，从而保持几何结构。该机制适用于循环网络和深度网络，且训练后的网络连接具有类似随机投影的统计特性，可解释生物脑中的表征稳定性。
source: biorxiv
selection_source: fresh_fetch
motivation: 解释神经表征漂移与群体相似结构稳定性之间的矛盾。
method: 分析随机连接网络中输入输出相似性的单调关系，并模拟漂移动态下的网络切换。
result: 随机网络中输出相似性是输入相似性的单调函数，漂移不改变表征相似结构。
conclusion: 表征稳定性是随机连接网络的通用结果，训练网络可表现出类似特性，为生物神经回路提供解释。
---

## 摘要
神经元活动模式在数天至数周内持续变化，这一现象称为表征漂移。尽管如此，群体表征的几何结构，即刺激诱发活动模式之间的成对相似性，仍保持显著稳定。持续的活动变化如何与稳定的表征相似性保持一致？我们证明这是随机连接的一般结果：在具有随机连接的网络中，输出相似性是输入相似性的单调递增函数，与特定的连接模式无关。无论是随机突触更替还是赫布可塑性驱动的漂移，仅使网络在不同随机实例间转换，而保持相似性不变。这扩展至循环架构和深度神经网络，在性能饱和后继续训练会产生活动漂移，同时保留表征相似性。尽管大脑中的连接并非随机，但在高维输入上训练的网络获得的连接在统计上行为类似随机投影，使得这些结果广泛适用于生物神经回路。

## Abstract
Neuronal activity patterns change continuously over days and weeks, a phenomenon known as representational drift. Despite this, the geometric structure of population representations, namely the pairwise similarities between stimulus-evoked activity patterns, remains remarkably stable. How can ongoing changes in activity be consistent with stable representational similarity? We show that this is a generic consequence of random connectivity: in networks with random connectivity, output similarity is a monotonically increasing function of input similarity, independent of the specific connectivity pattern. Drift, whether driven by random synaptic turnover or Hebbian plasticity, merely transitions the network between random instantiations, leaving similarity intact. This extends to recurrent architectures and to deep neural networks, where continued training beyond performance saturation produces activity drift while preserving representational similarity. Although connectivity in the brain is not random, networks trained on high-dimensional inputs acquire connectivity that behaves statistically like a random projection, making these results broadly applicable to biological neural circuits.