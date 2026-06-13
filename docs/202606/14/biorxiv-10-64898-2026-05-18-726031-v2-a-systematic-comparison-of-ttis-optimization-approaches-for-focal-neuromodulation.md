---
title: A Systematic Comparison of tTIS Optimization Approaches for Focal Neuromodulation
title_zh: 针对聚焦神经调控的tTIS优化方法的系统性比较
authors: "ghanem, p., Rampersad, S., Yarossi, M., Dorval, A., Brooks, D., Moharrer, A."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.18.726031v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 比较了非侵入性脑刺激（tTIS）的优化方法，实现局灶性神经调控
tldr: 颞叶干扰刺激（tTIS）利用高频电流干涉实现深部脑区聚焦调控，但寻找高效、安全且聚焦的电极模式是非凸优化难题。本研究首次系统比较了文献中7种近期优化方法，在5个头部模型的250个脑目标上评估聚焦性与刺激强度，按组织类型和深度分层揭示性能差异，最终提供基于证据的方法选择指南并公开代码，为研究者建立明确的决策框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 不同tTIS优化方法缺乏在多样脑目标上的系统比较，导致实践者无从选择最适合特定实验的优化策略。
method: 在五套有限元头模型中定义250个皮质和皮质下目标，以靶区平均电场和靶外激活体积为指标，全面基准测试七种优化方法（涵盖穷举搜索到无监督神经网络等）。
result: 各方法性能随组织类型和靶点深度呈现系统性差异，揭示了不同场景下的最优选择依据。
conclusion: 研究为科研和临床提供了一个基于证据的框架，可根据靶区位置、组织特性和计算资源选择最合适的tTIS优化方法。
---

## 摘要
经颅干涉电刺激(tTIS)是一种有前景的非侵入性脑刺激技术，它通过施加两路高频交流电在目标区域产生低频调幅包络，从而可能选择性地调控深部脑区。部署tTIS的关键挑战在于寻找同时具备有效、聚焦和安全特性的电极电流模式。这是一个本质上的非凸优化问题，近年来已有多项方法被提出。然而，尚未有研究对大量且多样的脑目标进行系统比较，这导致实践者缺乏针对特定实验设置优化方法的明确指导。本文中，我们进行了一项全面的基准测试研究，比较近年来文献中出现的七种tTIS优化方法：穷举搜索、遗传算法、多目标进化算法(MOVEA)、最小-最大优化、凸TI(CVXTI)、基于凸松弛的非凸优化以及无监督神经网络。所有方法在五个有限元头部模型中的250个跨越皮层、皮层下灰质和白质区域的脑目标上进行评估。每种方法通过两个关键指标衡量：目标区域内的平均电场强度，以及靶外受刺激脑体积。结果按组织类型和目标深度分层，以识别系统性的性能差异。基于这些结果，我们根据目标位置、组织类型和可用计算时间，为这七种方法的选择提供了实用的循证建议。此外，我们提供了代码库，使其他研究者能够将这些方法用于他们自己的应用。我们的目标是为研究人员和临床医生提供一个清晰、循证的框架，以选择适合其特定目标和应用的tTIS优化方法。

## Abstract
stimulation (tTIS) is a promising non-invasive brain stimulation technique that has the potential to selectively modulate deep brain regions by delivering two high-frequency alternating currents that interfere to produce a low-frequency amplitude-modulated envelope at the target. A key challenge in deploying tTIS is finding electrode current patterns that are simultaneously effective, focal, and safe. This is a fundamentally non-convex optimization problem for which a number of methods have recently been proposed. However, no systematic comparison of these methods across a large and diverse set of brain targets has been performed, leaving practitioners without clear guidance on how best to optimize for a particular experimental setting. In this work, we present a comprehensive benchmarking study comparing seven tTIS optimization methods that have appeared in the literature in recent years: exhaustive search, genetic algorithm, multi-objective evolutionary algorithm (MOVEA), min-max optimization, convex TI (CVXTI), non-convex optimization with convex relaxations, and an unsupervised neural network. All methods were evaluated across 250 brain targets spanning cortical and subcortical gray matter and white matter regions in five finite element head models. Each method was evaluated on two key metrics: mean electric field strength within the target region of interest, and off-target stimulated brain volume. Results were stratified by tissue type and target depth to identify systematic performance differences. Based on these results, we provide practical evidence-based recommendations for optimization method selection among these seven methods depending on target location, tissue type, and available computation time. Moreover we provide the code base that will allow other investigators to use these methods for their own applications. Our goal is to provide researchers and clinicians with a clear, evidence-based framework for choosing a tTIS optimization method suited to their specific target and application.