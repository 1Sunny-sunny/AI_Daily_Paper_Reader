---
title: Rank dependency of rescaled pruning in recurrent neural networks
title_zh: 递归神经网络中重缩放剪枝的秩依赖性
authors: "Wang, A. Q., Kim, S. H., Choi, H."
date: 2026-06-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.30.728930v1.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 循环神经网络中剪枝对低维动力学的影响
tldr: 神经网络在发育中经历大规模突触修剪，但如何保持低维群体计算仍不清楚。本研究探讨不同修剪规则与递归神经网络秩的相互作用，发现带突触重缩放的修剪在低秩网络中能有效保持低维动态，而在高秩网络中会导致性能退化，揭示了低秩结构与重缩放对于稀疏网络维持稳定动态的关键作用。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究突触修剪如何影响递归神经网络的低维动态和任务表现，理解其秩依赖特性。
method: 结合数学分析与数值模拟，系统评估受生物学启发的修剪规则与网络秩的相互作用。
result: 修剪后的动态与任务表现高度依赖初始网络秩，重缩放修剪在低秩网络表现良好，但在高秩网络退化。
conclusion: 低秩结构配合突触重缩放是稀疏网络中保持稳定低维动态的关键。
---

## 摘要
在发育与成熟过程中，神经回路经历大规模的突触剪枝，从而产生高度稀疏的连接，同时保持稳健的群体级计算。这些群体动力学通常是低维的，使得任务相关的计算可以被形式化为潜子空间内的轨迹。如何在广泛的网络稀疏化过程中保持这种低维动力学，目前仍不清楚。在此，我们研究不同的突触剪枝规则如何塑造递归神经网络中的低维动力学和任务性能。不同于以往专注于低秩网络或具有严格约束结构的网络的随机稀疏化方法，我们系统地评估了基于生物启发的剪枝规则如何与网络的底层秩相互作用。我们表明，剪枝后的动力学和任务性能关键取决于网络的初始秩，这是因为不同秩区域的谱特征不同。结合数学分析与模拟，我们证明，在低秩RNN中，带有突触重缩放的剪枝能以最小的失真保持低维动力学，但在高秩区域则性能下降。我们的发现表明，低秩结构结合稳态突触重缩放对于在稀疏网络中维持稳定的低维动力学至关重要。

## Abstract
Throughout development and maturity, neural circuits undergo massive synaptic pruning, yielding highly sparse connectivity while preserving robust population-level computations. These population dynamics are often low-dimensional, allowing task-related computations to be formalized as trajectories within latent subspaces. How such low-dimensional dynamics are preserved amid widespread network sparsification remains unclear. Here, we investigate how different synaptic pruning rules shape low-dimensional dynamics and task performance in recurrent neural networks (RNNs). Moving beyond previous approaches focused on random sparsification of low-rank networks or networks with strictly constrained structures, we systematically evaluate how biologically motivated pruning rules interact with a network's underlying rank. We show that post-pruning dynamics and task performance depend critically on the network's initial rank due to distinct eigenspectral characteristics across rank regimes. Combining mathematical analysis with simulations, we demonstrate that pruning with synaptic rescaling preserves low-dimensional dynamics with minimal distortion in low-rank RNNs, but degrades in the high-rank regime. Our findings suggest that low-rank structure, combined with homeostatic synaptic rescaling, is essential for maintaining stable, low-dimensional dynamics in sparse networks.