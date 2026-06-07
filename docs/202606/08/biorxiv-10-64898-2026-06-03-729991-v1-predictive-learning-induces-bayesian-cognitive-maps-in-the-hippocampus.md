---
title: Predictive learning induces Bayesian cognitive maps in the hippocampus
title_zh: 预测性学习在海马体中诱导贝叶斯认知地图
authors: "Kim, Y., Kang, Y. H."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729991v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 通过预测学习研究位置细胞活动和贝叶斯认知地图
tldr: 导航过程中位置感知存在不确定性，但经典空间表征模型常忽视这一问题。本研究提出贝叶斯理想观察者模型，将感知推理纳入位置信念，发现其更准确地复现海马位置细胞的活动特性。进一步，通过训练循环神经网络预测下一时刻的自我中心感觉输入，网络能学习类贝叶斯表征，并在不同环境中产生位置细胞样活动，优于自编码器。结果表明，海马可能通过预测性感知学习，从经验中构建贝叶斯认知地图。
source: biorxiv
selection_source: fresh_fetch
motivation: 经典空间表征模型忽略感知不确定性，无法解释位置细胞如何从模糊感觉输入中形成。
method: 比较直接可观察模型与贝叶斯理想观察者模型，并训练循环神经网络预测下一感觉输入来学习表征。
result: 贝叶斯模型更好复现位置野特性，预测性网络学习到类贝叶斯信念，并产生位置细胞样活动。
conclusion: 海马可能通过预测性感知学习构建贝叶斯认知地图。
---

## 摘要
导航需要感知：位置必须从嘈杂且模糊的自我中心感觉输入中推断出来，就像视觉估计距离一样。然而，许多经典的空间表征模型隐含地假设异我中心位置可以直接观测，从而忽略了感知不确定性。在此，我们将这样的模型与一个显式包含感知推断的贝叶斯理想观察者进行比较。我们发现，贝叶斯观察者关于位置的信念更准确地再现了位置细胞活动的关键属性，包括位置野的宽度、面积和密度，无论是在单个环境内还是跨环境。通过分析论证和数值模拟，我们展示了训练以预测下一个自我中心感觉输入的递归神经网络学习到了类似于贝叶斯信念的表征，并在熟悉和陌生环境中产生类似位置细胞的活动，其表现优于训练以再现当前输入的自编码器。总之，这些结果表明，海马回路可能通过预测性感知学习从经验中构建贝叶斯认知地图。

## Abstract
Navigation requires perception: location must be inferred from noisy and ambiguous egocentric sensory inputs, as in visual estimation of distance. However, many classical models of spatial representation implicitly assume that allocentric location is directly observable, thereby neglecting perceptual uncertainty. Here, we compare such a model with a Bayesian ideal observer that explicitly incorporates perceptual inference. We find that the Bayesian observer's beliefs over location more accurately reproduce key properties of place cell activity, including place field width, area, and density, within and across environments. Using analytic arguments and numerical simulations, we show that recurrent neural networks trained to predict the next egocentric sensory input learn representations resembling Bayesian beliefs and yield place cell-like activity in both familiar and unfamiliar environments, outperforming autoencoders trained to reproduce the current input. Together, these results suggest that hippocampal circuits may construct Bayesian cognitive maps from experience through predictive perceptual learning.