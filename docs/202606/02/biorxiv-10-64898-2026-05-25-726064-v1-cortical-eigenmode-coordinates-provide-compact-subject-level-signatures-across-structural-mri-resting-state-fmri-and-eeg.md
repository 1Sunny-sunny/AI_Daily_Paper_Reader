---
title: "Cortical eigenmode coordinates provide compact subject-level signatures across structural MRI, resting-state fMRI, and EEG"
title_zh: 皮层本征模坐标为结构MRI、静息态fMRI和EEG提供紧凑的个体水平特征
authors: "Park, H. G., Tarpey, T."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.726064v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 多模态脑信号共有的特征模态坐标框架
tldr: 本研究评估了皮层拉普拉斯-贝尔特拉米特征模态坐标作为跨结构MRI、静息态fMRI和EEG的统一几何语言，以构建紧凑、可解释的个体大脑特征。通过单模态与多模态分析（包括多模态PCA和几何特征模态多视角分解GEMF），特征模态坐标表示在预测年龄和认知表现上表现出色，多模态PCA性能最优，GEMF以更低维度提供可解释的共享与模态特异性因子，为多模态神经影像整合提供了实用基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 多模态神经影像分析常局限于模态特定空间或粗粒度汇总，缺乏共享的、可解释的个体水平大脑特征表示。
method: 采用皮层特征模态坐标统一表示sMRI、rs-fMRI和EEG数据，并比较单模态系数、多模态PCA、传统图谱/传感器PCA及几何特征模态多视角分解（GEMF）的性能。
result: 多模态特征模态坐标PCA在适中维度下实现高年龄预测精度，且始终优于传统低维PCA；GEMF以更少维度提供竞争性性能及清晰的共享与模态特异性解释。
conclusion: 皮层特征模态坐标可作为多模态对齐、紧凑且可解释的个体大脑标志，有助于推动多模态影像整合研究。
---

## 摘要
多模态神经影像的一个实际障碍是，结构MRI、fMRI和EEG通常分别在模态特定空间进行分析，或被简化为基于图谱和传感器的汇总，这限制了构建通用的、可解释的个体水平大脑特征。我们将皮层拉普拉斯-贝尔特拉米本征模坐标评估为结构MRI（sMRI）、静息态fMRI（rs-fMRI）和EEG的一种共享的几何对齐语言。在这个框架中，sMRI形态测量场由皮层本征模系数表示，rs-fMRI由本征模时间序列系数之间的协方差表示，EEG由模态-频率条件汇总表示。

使用莱比锡马克斯·普朗克研究所心-脑-体数据集（MPI-LEMON），我们比较了单模态本征模坐标汇总、多模态皮层本征模坐标PCA、基于图谱/传感器的传统PCA和岭表示，以及几何本征模多视角因子分解（GEMF）。GEMF是一种结构化分解，它保留了数据对象的模态原生组织，同时将共享变异与模态特异性变异分离开。本征模坐标表示产生了紧凑的个体水平特征，对实际年龄和次要认知结果具有强大的外部有效性。多模态本征模坐标PCA是性能最强的方法之一，在中等维度下达到了较高的年龄预测性能，并始终优于传统的低维PCA。GEMF选择了更低维度的共享表示，并保持竞争力，其优势在于提供可解释的共享和模态特异性因子。

这些发现支持皮层本征模坐标作为构建紧凑、可解释且多模态对齐的个体水平大脑特征的实用基础。

## Abstract
A practical barrier in multimodal neuroimaging is that structural MRI, fMRI, and EEG are often analyzed in modality-specific spaces or reduced to atlas- and sensor-based summaries, limiting the construction of common, interpretable subject-level brain signatures. We evaluate cortical Laplace-Beltrami eigenmode coordinates as a shared geometry-aligned language for structural MRI (sMRI), resting-state fMRI (rs-fMRI), and EEG. In this framework, sMRI morphometric fields are represented by cortical eigenmode coefficients, rs-fMRI by covariance among eigenmode time-series coefficients, and EEG by mode-frequency-condition summaries.

Using the Max Planck Institute Leipzig Mind-Brain-Body dataset (MPI-LEMON), we compared unimodal eigenmode-coordinate summaries, multimodal cortical eigenmode-coordinate PCA, conventional atlas/sensor-based PCA and ridge representations, and geometric eigenmode multiview factorization (GEMF). GEMF is a structured decomposition that preserves the modality-native organization of the data objects while separating shared from modality-specific variation. Eigenmode-coordinate representations yielded compact subject-level signatures with strong external validity for chronological age and a secondary cognitive outcome. Multimodal eigenmode-coordinate PCA was among the strongest-performing approaches, reached high age-prediction performance at moderate dimension, and consistently outperformed conventional low-dimensional PCA. GEMF selected an even lower-dimensional shared representation and remained competitive with the benefit of providing interpretable shared and modality-specific factors.

These findings support cortical eigenmode coordinates as a practical foundation for compact, interpretable, and multimodally aligned subject-level brain signatures.