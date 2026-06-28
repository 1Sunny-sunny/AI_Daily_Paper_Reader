---
title: Task-optimized models of sensory uncertainty reproduce human confidence judgments
title_zh: 任务优化的感官不确定性模型再现人类信心判断
authors: "Govindarajan, L. N., Alavilli, S., McDermott, J. H."
date: 2026-06-24
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.31.685933v3.full.pdf"
tags: ["query:sr"]
score: 6.0
evidence: 任务优化模型关联感官输入与不确定性估计
tldr: 为探究人类在自然感知中的不确定性表征是否准确，研究开发了任务优化模型来生成感知概率分布并计算信心，通过声音定位和音高感知实验比较人类信心判断。结果显示人类信心与模型信心高度一致，表明人类不确定性表征准确反映实际感知变异性，该模型框架可推广至其他感知领域。
source: biorxiv
selection_source: fresh_fetch
motivation: 缺乏可计算刺激的不确定性模型，限制了对人类感知不确定性表征的研究。
method: 提出任务优化模型估计不确定性，将模型信心与人类信心判断进行跨条件对比。
result: 在两项听觉任务中，人类信心随刺激变异性系统性变化，并与模型信心显著相关。
conclusion: 人类能够准确表征感知不确定性，任务优化模型可作为研究该能力的有效工具。
---

## 摘要
感官输入常常模糊不清，导致对外部世界的解释充满不确定性。对感知不确定性的估计可能有助于指导行为，但尚不清楚人类在自然情境中是否明确表征不确定性，以及这种表征是否规范正确。由于缺乏能够计算不确定性且适用于刺激的模型，研究进展受阻。我们开发了一类任务优化模型，可生成感知估计的概率分布。为评估人类的不确定性表征是否与模型一致，我们将人类信心判断（可能间接反映不确定性表征）与从模型不确定性中提取的信心判断进行比较。在声音定位和音高感知任务中，人类信心系统性地变化，对于在不同试次中产生更变异估计的刺激，信心更低。人类信心在不同条件下跟踪模型信心，表明人类的不确定性表征准确地反映了感知估计的实际不确定性。该建模框架可扩展到其他感知领域。

## Abstract
Sensory input is often ambiguous, leading to uncertain interpretations of the external world. Estimates of perceptual uncertainty might be useful in guiding behavior, but it remains unclear whether humans explicitly represent uncertainty in naturalistic settings, and whether any such representations are normatively correct. Progress has been hindered by the absence of stimulus-computable models that estimate uncertainty. We developed a class of task-optimized models that generate probability distributions over perceptual estimates. To assess whether human uncertainty representations align with the models, we compared human confidence judgments, which might indirectly reflect uncertainty representations, to confidence judgments extracted from the models uncertainty. In both sound localization and pitch perception, human confidence varied systematically, being lower for stimuli that produced more variable estimates across trials. Human confidence tracked model confidence across conditions, suggesting that human uncertainty representations accurately reflect the actual uncertainty of perceptual estimation. The modeling framework is extensible to other perceptual domains.