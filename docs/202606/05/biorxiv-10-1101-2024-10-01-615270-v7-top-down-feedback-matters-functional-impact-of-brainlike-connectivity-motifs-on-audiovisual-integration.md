---
title: "Top-down feedback matters: Functional impact of brainlike connectivity motifs on audiovisual integration"
title_zh: 自上而下反馈的重要性：类脑连接模式对视听整合的功能影响
authors: "Tugsbayar, M., Li, M., Muller, E., Richards, B. A."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.1101/2024.10.01.615270v7.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 建模自上而下反馈以解释神经编码
tldr: 人工神经网络常缺乏自上而下反馈，本研究开发了捕获新皮层反馈特性的深度模型，构建层次递归网络用于视听整合任务。发现模仿人脑的层次结构赋予模型类似人类的轻微视觉偏差，且不同反馈配置使相同连接模型功能异于传统模型，证明自上而下反馈具有计算重要性。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索自上而下反馈在大脑中的计算角色，解决标准人工神经网络模型缺少该特征的问题。
method: 开发了捕获新皮层自上而下反馈核心功能特性的深度神经网络模型，构建层次递归人工神经网络进行视听整合任务。
result: 模仿人脑层次的模型产生无损性能的轻微视觉偏差，不同反馈配置使模型功能区别于传统前馈和横向递归模型。
conclusion: 自上而下反馈是生物大脑的计算相关特征，将其纳入人工神经网络会影响模型行为并约束解决方案。
---

## 摘要
人工神经网络是研究神经计算的重要工具，但标准ANN架构并未捕捉到大脑的许多特征。大多数ANN模型缺少的一个显著特征是自上而下的反馈，即网络中从高阶层到低阶层的投射。自上而下的反馈在大脑中普遍存在，并且对新皮层锥体神经元的活动具有独特的调节作用。然而，我们仍然不理解其计算作用。在此，我们开发了一个深度神经网络模型，该模型捕捉了新皮层自上而下反馈的核心功能特性，使我们能够构建更贴近大脑架构的层次化循环ANN模型。我们利用该模型探索了不同层次化循环架构对视听整合任务的影响。我们发现某些层次结构，特别是那些模仿人脑架构的结构，赋予了ANN模型轻微的视觉偏好，类似于在人类中观察到的现象。这种偏好并未损害视听任务的表现。结果进一步表明，不同配置的自上而下反馈使得原本连接相同的模型在功能上彼此不同，也与传统的前馈和横向循环模型有所区别。总之，我们的发现证明调节性自上而下反馈是生物脑在计算上相关的特征，将其纳入ANN会影响其行为并限制其可能发现的解决方案。

## Abstract
Artificial neural networks (ANNs) are an important tool for studying neural computation, but many features of the brain are not captured by standard ANN architectures. One notable missing feature in most ANN models is top-down feedback, i.e. projections from higher-order layers to lower-order layers in the network. Top-down feedback is ubiquitous in the brain, and it has a unique modulatory impact on activity in neocortical pyramidal neurons. However, we still do not understand its computational role. Here we develop a deep neural network model that captures the core functional properties of top-down feedback in the neocortex, allowing us to construct hierarchical recurrent ANN models that more closely reflect the architecture of the brain. We use this to explore the impact of different hierarchical recurrent architectures on an audiovisual integration task. We find that certain hierarchies, namely those that mimic the architecture of the human brain, impart ANN models with a light visual bias similar to that seen in humans. This bias does not impair performance on the audiovisual tasks. The results further suggest that different configurations of top-down feedback make otherwise identically connected models functionally distinct from each other, and from traditional feedforward and laterally recurrent models. Altogether our findings demonstrate that modulatory top-down feedback is a computationally relevant feature of biological brains, and that incorporating it into ANNs affects their behavior and constrains the solutions it's likely to discover.