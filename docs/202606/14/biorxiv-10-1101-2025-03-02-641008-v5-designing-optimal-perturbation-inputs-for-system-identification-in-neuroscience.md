---
title: Designing optimal perturbation inputs for system identification in neuroscience
title_zh: 为神经科学中的系统辨识设计最优扰动输入
authors: "Ogino, M., Sekizawa, D., Kitazono, J., Oizumi, M."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.1101/2025.03.02.641008v5.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 使用控制理论进行神经系统的优化扰动设计
tldr: 为准确估计神经网络连接，本研究提出基于控制理论的扰动输入优化框架。传统扰动依赖经验，而本方法将神经模型视为控制系统，通过最小化系统识别误差来设计最优扰动，并揭示其与常见刺激模式的关系。模拟结果表明，该框架设计的扰动显著优于传统输入，为神经状态分类和控制提供了理论依据。
source: biorxiv
selection_source: fresh_fetch
motivation: 被动神经活动信息有限，传统扰动设计缺乏理论指导，难以精确估计神经连接。
method: 将神经模型构建为控制系统，基于最小化估计误差推导最优扰动输入的理论，并关联常见刺激模式。
result: 该框架设计的扰动在模拟中实现了比传统直觉输入更准确的神经动力学估计。
conclusion: 研究为扰动输入设计提供了理论支撑，有助于可靠区分神经状态并精准控制其恢复。
---

## 摘要
探究由神经元间连接支配的神经动力学是神经科学中的一项根本性挑战。由于被动（自发）活动仅为估计连接性提供有限的信息，基于扰动的方法在神经科学中被广泛应用，因为它们能唤起潜在的隐藏动力学。然而，这类扰动的特性通常基于经验或生物学直觉来设计。为了实现更准确的连接性估计，我们提出一种数据驱动且理论上有据的框架，通过将神经模型表述为控制系统来最优地设计扰动输入。支撑我们方法的核心理论见解是：在被动状态下观察到的神经信号缺乏足够的潜在信息，这导致系统辨识失败。扰动揭示了这些隐藏的动力学，并带来估计的改进。在这些见解的指导下，我们推导出优化扰动输入的理论基础，以最小化神经系统辨识的估计误差。在此基础上，我们进一步探索了这一理论与神经科学中常用刺激模式（如频率、脉冲和阶跃输入）的关系。我们通过基于实验范式（如神经状态分类和神经状态的最优控制）的模拟，证明了该框架对神经科学的有效性。我们的理论分析与多项模拟一致表明，与传统基于直觉的输入相比，根据我们框架设计的扰动能实现显著更准确的系统辨识。本研究为设计扰动输入以实现神经动力学的精确估计提供了理论基础。这进而能够可靠地区分神经状态（如意识水平和病理状况），并有助于精确控制其向从异常状态恢复的转变。

## Abstract
Investigating the dynamics of neural networks, which are governed by connectivity between neurons, is a fundamental challenge in neuroscience. Because passive (spontaneous) activity provides only limited information for estimating connectivity, perturbation-based approaches are widely applied in neuroscience, as they can evoke underlying hidden dynamics. However, the characteristics of such perturbations have typically been designed based on empirical or biological intuition. To enable more accurate estimation of connectivity, we propose a data-driven and theoretically grounded framework for optimally designing perturbation inputs, based on formulating the neural model as a control system. The core theoretical insight underlying our approach is that neural signals observed in the passive state lack sufficient latent information, which leads to failures in the system identification. Perturbations reveal these hidden dynamics and lead to improved estimation. Guided by these insights, we derive a theoretical basis for optimizing perturbation inputs that minimize estimation errors in neural system identification. Building upon this, we further explore the relationship of this theory with stimulation patterns commonly used in neuroscience, such as frequency, impulse, and step inputs. We demonstrate the effectiveness of this framework for neuroscience through simulations grounded in experimental paradigms such as neural state classification and optimal control of neural states. Our theoretical analysis, together with multiple simulations, consistently shows that perturbations designed according to our framework achieve substantially more accurate system identification compared to the conventional, intuition-based inputs. This study provides a theoretical foundation for designing perturbation inputs to achieve accurate estimation of neural dynamics. This, in turn, enables reliable discrimination of neural states such as levels of consciousness and pathological conditions, and facilitates precise control of their transitions toward recovery from abnormal states.