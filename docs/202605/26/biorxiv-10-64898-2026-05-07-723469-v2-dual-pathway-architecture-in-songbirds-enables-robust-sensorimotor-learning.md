---
title: Dual pathway architecture in songbirds enables robust sensorimotor learning
title_zh: 鸣禽中的双通路架构实现稳健的感觉运动学习
authors: "Sankar, R., Suryawanshi, A., Rougier, N. P., Leblois, A."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.07.723469v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 鸣鸟基底节计算模型通过神经表征解释感觉运动学习
tldr: 本研究针对强化学习在非凸性能景观中易陷入局部最优的问题，以鸣禽为模型，提出了受斑胸草雀鸣唱系统解剖与发育约束的双通路计算架构。该架构结合基底节驱动的强化学习通路和通过赫布可塑性巩固模式的皮层运动通路，并引入突触波动以产生结构化变异。模拟表明，该模型可靠收敛至全局最优，优于标准方法，并复现了非单调学习轨迹等实验现象，揭示了回路架构对高效学习的关键作用，为人工强化学习系统提供了仿生设计原则。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有强化学习理论在非凸性能景观中易陷入局部最优，难以解释鸣禽等动物的鲁棒感觉运动学习。
method: 构建受斑胸草雀鸣唱系统约束的双通路神经网络模型，集成基底节驱动的强化学习通路与皮层运动通路，并引入突触波动。
result: 模型在模拟中可靠收敛至全局最优，优于标准与噪声退火强化学习，并复现了非单调学习、变异减少及控制权转移等实验特征。
conclusion: 双通路架构通过皮层延迟成熟内隐调节探索-利用平衡，而突触波动助力逃离局部最优，实现了高效鲁棒学习，为人工系统提出了新设计原则。
---

## 摘要
感觉运动技能的获取关键依赖于基底神经节（BG）-丘脑-皮层回路。主流理论认为，基底神经节通过强化学习（RL），利用内部表现评估来近似随机梯度上升，从而优化运动输出。然而，该框架在非凸表现景观中面临困境，局部最优会阻碍高效学习。鸣禽提供了一个稳健感觉运动学习的典型生物学实例，它们通过试错在专门的BG-丘脑-皮层架构中掌握复杂发声。在此，我们提出了一个受斑胸草雀鸣叫系统的解剖学、生理学和发育轨迹约束的计算模型。该模型将BG驱动的强化学习通路与并行的皮层运动通路相结合，后者通过赫布可塑性逐步巩固成功的运动模式。此外，我们在BG通路中引入了突触波动性，从而在学习过程中引入结构化变异。通过使用生物物理鸣管模型和合成表现景观模拟发声学习，我们证明这种双通路架构能够可靠地收敛到全局最优，并优于标准及噪声退火的强化学习方法。该模型再现了鸣叫学习的关键实验特征，包括非单调的学习轨迹、运动变异性的逐渐降低，以及运动控制从皮层下回路到皮层回路的发育性转移。从机制上讲，皮层通路的延迟成熟提供了对探索-利用权衡的隐式调节，而突触波动性则使系统能够逃离局部最优。这些结果突显了神经回路架构和动态在高效学习中的重要性，并提出了受生物学启发的设计原则，以提高复杂感觉运动领域中人工强化学习系统的鲁棒性和样本效率。

## Abstract
The acquisition of sensorimotor skills critically depends on basal ganglia (BG)-thalamo-cortical circuits. Prevailing theories propose that the BG optimize motor output through reinforcement learning (RL), using internal performance evaluations to approximate stochastic gradient ascent. However, this framework struggles in non-convex performance landscapes, where local optima hinder efficient learning. Songbirds provide a compelling biological example of robust sensorimotor learning, mastering complex vocalizations through trial-and-error within a specialized BG-thalamo-cortical architecture. Here, we present a computational model constrained by the anatomy, physiology, and developmental trajectory of the zebra finch song system. The model combines a BG-driven RL pathway with a parallel cortical motor pathway that progressively consolidates successful motor patterns via Hebbian plasticity. In addition, we incorporate synaptic volatility within the BG pathway, introducing structured variability across learning. Through simulations of vocal learning using both a biophysical syrinx model and synthetic performance landscapes, we demonstrate that this dual-pathway architecture reliably converges to global optima and outperforms standard and noise-annealed RL approaches. The model reproduces key experimental features of song learning, including non-monotonic learning trajectories, a gradual reduction in motor variability, and the developmental transfer of motor control from subcortical to cortical circuits. Mechanistically, delayed maturation of the cortical pathway provides an implicit regulation of the exploration-exploitation trade-off, while synaptic volatility enables escape from local optima. These results highlight the importance of neural circuit architecture and dynamics in efficient learning, and suggest biologically inspired design principles for improving the robustness and sample efficiency of artificial RL systems in complex sensorimotor domains.