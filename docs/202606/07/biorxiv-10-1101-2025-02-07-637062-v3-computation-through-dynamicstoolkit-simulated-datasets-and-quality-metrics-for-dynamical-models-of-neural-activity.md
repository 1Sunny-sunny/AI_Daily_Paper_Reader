---
title: "Computation-through-DynamicsToolkit: Simulated datasets and quality metrics for dynamical models of neural activity"
title_zh: 计算通过动力学工具包：用于神经活动动力学模型的模拟数据集和质量指标
authors: "Versteeg, C., McCart, J. D., Ostrow, M., Zoltowski, D. M., Washington, C. B., Driscoll, L., Codol, O., Michaels, J. A., Linderman, S. W., Sussillo, D., Pandarinath, C."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.1101/2025.02.07.637062v3.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 用于验证神经活动动力学模型的模拟数据集和指标
tldr: 系统神经科学研究神经计算依赖动力学模型，但现有合成数据集与验证指标无法反映生物特征。CtDToolkit提供反映生物计算特性的合成数据集、可解释的性能指标及标准化训练评估流程，支持模型开发、调优与故障排除，为动力学视角理解神经计算提供必要框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有合成数据集和验证指标缺乏神经计算的基本特征，阻碍了神经动力学模型的可靠验证和发展。
method: CtDToolkit提供模拟生物神经计算特性的合成数据集、可解释的准确性指标及标准化训练评估流程。
result: 展示了CtDToolkit如何有效指导神经动力学模型的开发、参数调优与故障诊断。
conclusion: CtDToolkit为模型开发者提供了通过动力学透镜理解神经计算的关键工具和框架。
---

## 摘要
系统神经科学的一个主要目标是发现神经元群如何将输入转化为目标导向行为，这一过程称为神经计算。理解神经计算的一个有力框架是使用神经动力学——即控制神经活动随时间演化的规则——来解释目标导向的输入-输出转换是如何发生的。由于动力学规则不可直接观察，我们需要能够从记录的神经活动中推断出神经动力学的计算模型。我们通常使用具有已知真实动力学的合成数据集来验证这些模型，但不幸的是，现有的合成数据集并未反映神经计算的基本特征，因此可能无法很好地代表神经系统。此外，该领域缺乏经过验证的指标来量化模型推断出的动力学的准确性。计算通过动力学工具包（CtDToolkit）通过提供以下内容来弥补这些关键差距：1）反映生物神经回路计算特性的合成数据集；2）用于量化模型性能的可解释指标；以及3）在已知或未知外部输入的情况下训练和评估模型的标准化流程。在本文中，我们演示了CtDToolkit如何帮助指导神经动力学模型的开发、调整和故障排除。总之，CtDToolkit为模型开发者提供了一个必要的框架，使他们能够通过动力学的视角更好地理解和表征神经计算。

## Abstract
A primary goal of systems neuroscience is to discover how ensembles of neurons transform inputs into goal-directed behavior, a process known as neural computation. A powerful framework for understanding neural computation uses neural dynamics - the rules that govern how neural activity evolves over time - to explain how goal-directed input-output transformations occur. As dynamical rules are not directly observable, we need computational models that can infer neural dynamics from recorded neural activity. We typically validate such models using synthetic datasets with known ground-truth dynamics, but unfortunately existing synthetic datasets don't reflect fundamental features of neural computation and may therefore be poor proxies for neural systems. Further, the field lacks validated metrics for quantifying the accuracy of the dynamics inferred by models. The Computation- through-Dynamics Toolkit (CtDToolkit) addresses these critical gaps by providing: 1) synthetic datasets that reflect computational properties of biological neural circuits, 2) interpretable metrics for quantifying model performance, and 3) a standardized pipeline for training and evaluating models with or without known external inputs. In this manuscript, we demonstrate how CtDToolkit can help guide the development, tuning, and troubleshooting of neural dynamics models. In summary, CtDToolkit provides a necessary framework for model developers to better understand and characterize neural computation through the lens of dynamics.