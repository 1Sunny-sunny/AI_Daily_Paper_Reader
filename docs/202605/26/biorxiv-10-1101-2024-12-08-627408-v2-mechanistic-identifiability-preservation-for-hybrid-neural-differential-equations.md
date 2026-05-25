---
title: Mechanistic Identifiability Preservation for Hybrid Neural Differential Equations
title_zh: 混合神经微分方程的机理可辨识性保持
authors: "Whipple, B., Hernandez-Vargas, E. A."
date: 2026-05-23
pdf: "https://www.biorxiv.org/content/10.1101/2024.12.08.627408v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 确保混合神经微分方程机制可解释性的理论框架
tldr: 本文研究混合神经常微分方程中神经增强对机械模型可识别性的影响，通过建立有界神经校正形式化体系，推导误差界限和可识别性保持的充分条件，实验揭示了表达性与可识别性之间的权衡，为科学计算中HNDEs的部署提供了理论指导。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经增强可能损害机械模型的可识别性，亟需理论框架指导模型表达性与可解释性的平衡。
method: 形式化有界神经校正类，推导Gronwall型轨迹与观测差异界限，建立近似机械参数可恢复性的充分条件。
result: 实验证实神经增强系统性削弱但不消除机械可识别性，揭示基本的表达性-可识别性权衡。
conclusion: 本文为在科学智能计算中部署混合神经微分方程提供了理论基础和可操作指导。
---

## 摘要
混合神经微分方程（HNDEs）将神经网络组件嵌入机理骨架，结合了领域导出模型的结构可解释性与神经动力学的逼近能力。尽管在生物学和工程学中得到越来越多的采用，神经增强可能引入观测退化，从而损害机理可辨识性和科学可解释性。本文为HNDEs中机理可辨识性的实用保持建立了一个理论框架。我们形式化了有界神经修正类，并推导了将神经扰动与机理参数模糊性联系起来的Gronwall型轨迹和观测差异界。我们进一步建立了充分条件，在此条件下混合神经修正能保持近似的机理参数可恢复性，直到显式量化的容差。对基准系统的经验似然曲线分析证实，神经增强系统性地削弱——但不消除——机理可辨识性，揭示了一种基本的表达能力-可辨识性权衡。这些结果为在科学智能计算中部署HNDEs提供了理论基础和可操作的指导。

## Abstract
Hybrid neural differential equations (HNDEs) embed neural network components within mechanistic scaffolds, combining the structural interpretability of domain-derived models with the approximation power of neural dynamics. Despite their growing adoption in biology and engineering, neural augmentation can introduce observational degeneracies that compromise mechanistic identifiability and scientific interpretability. In this paper, we develop a theoretical framework for practical preservation of mechanistic identifiability in HNDEs. We formalize bounded neural correction classes and derive Gronwall-type trajectory and observational discrepancy bounds linking neural perturbations to mechanistic parameter ambiguity. We further establish sufficient conditions under which hybrid neural corrections preserve approximate mechanistic parameter recoverability up to explicitly quantifiable tolerances. Empirical likelihood profile analyses on benchmark systems confirm that neural augmentation systematically weakens---but does not eliminate---mechanistic identifiability, revealing a fundamental expressiveness--identifiability trade-off. These results provide theoretical foundations and actionable guidance for deploying HNDEs in scientific intelligent computing.