---
title: "BiXformer: A Bidirectional Cross Attention Transformer for Disentangling Inter-Regional Neural Dynamics"
title_zh: BiXformer：一种用于解耦脑区间神经动态的双向交叉注意力Transformer
authors: "El Sayed, O., Han, Y., Dragoi, T., Economo, M. N., DePasquale, B."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.05.730511v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 利用时间约束解耦前馈和反馈神经动力学
tldr: 为解析多脑区神经信号中交叠的前馈与反馈成分，本文提出BiXformer，一种双向交叉注意力Transformer。该模型通过方向掩码注意力将跨区通信分解为因果与反因果流，恢复低维定向潜变量动态并估计通信延迟，无需线性或平稳性假设。合成数据验证了其精确恢复能力，在运动任务神经记录中揭示出感觉反馈与运动信号的共存，为复杂神经回路中定向动态的解析提供了灵活框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法难以从高维多脑区神经记录中分离双向、时间偏移的跨区通信信号。
method: 提出BiXformer，利用方向掩码交叉注意力分解前馈与反馈流，并学习低维定向动态与延迟。
result: 在合成数据上准确恢复潜结构和延迟，在真实数据中提取出与感觉反馈和运动相关信号一致的成分。
conclusion: BiXformer能有效解析神经回路中的定向动态通信，适用于复杂多脑区交互研究。
---

## 摘要
高通量神经记录技术的进步使得能够在行为动物中同时测量多个脑区的活动，产生了规模和丰富性前所未有的数据集。由于脑区间通信的双向性质和时间偏移特性，解释这些数据仍然具有挑战性，其中前馈和反馈信号叠加在神经群体中。我们提出了BiXformer，一种双向交叉注意力Transformer，通过使用方向性掩码注意力将脑区间通信分解为因果和非因果流，从而解耦这些相互作用。通过在注意力头中施加时间约束，BiXformer恢复了低维的、有向的潜在动态，并估计通信延迟，不依赖于线性或平稳性假设。我们在具有已知真实延迟的合成数据集上验证了该模型，证明了潜在结构和脑区间时间能够被准确恢复。将BiXformer应用于同时记录的神经-行为数据和运动任务期间的多脑区神经记录，揭示了可解释的、时间结构化的成分，与感觉反馈和运动相关信号共存相一致。这些结果确立了BiXformer作为一个灵活的框架，用于揭示复杂神经回路中动态的、有向的通信。

## Abstract
Advances in high-throughput neural recording technologies enable simultaneous measurement of activity across multiple brain regions in behaving animals, producing datasets of unprecedented scale and richness. Interpreting these data remains challenging due to the bidirectional and temporally offset nature of inter-regional communication, where feedforward and feedback signals are superimposed within neural populations. We introduce BiXformer, a bidirectional cross-attention transformer that disentangles these interactions by decomposing inter-regional communication into causal and acausal streams using directionally masked attention. By enforcing temporal constraints within attention heads, BiXformer recovers low-dimensional, directed latent dynamics and estimates communication delays without relying on linearity or stationarity assumptions. We validate the model on synthetic datasets with known ground-truth delays, demonstrating accurate recovery of both latent structure and inter-regional timing. Applied to simultaneous neural-behavioral recordings and multi-region neural recordings during a movement task, BiXformer reveals interpretable, temporally structured components consistent with the coexistence of sensory feedback and motor-related signals. These results establish BiXformer as a flexible framework for uncovering dynamic, directed communication in complex neural circuits.