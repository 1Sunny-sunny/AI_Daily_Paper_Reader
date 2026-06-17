---
title: "Functional Templates in fMRI: Building Accurate and Interpretable Group-Level Decoders"
title_zh: fMRI 中的功能模板：构建准确且可解释的组级解码器
authors: "Barbarant, P.-L., Meyniel, F., Thirion, B."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.21.726781v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: fMRI解码与功能对齐构建组级解码器
tldr: fMRI跨被试解码面临个体功能变异性挑战，功能模板可构建共享空间，但缺乏实用指南。本研究在任务解码框架下系统比较多种功能对齐方法（最优传输、普鲁克分析、岭回归、共享响应模型）与模板构建策略，发现基于最优传输的群体模板解码准确率最高、不偏倚于个体、利于泛化且保留皮层信号拓扑，为功能模板推广提供了依据。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有功能模板评估局限于电影观看范式，缺乏在一般任务解码中的系统比较，阻碍其实际应用。
method: 在多个任务和数据集上，比较四种功能对齐方法与三种模板构建策略在跨被试解码中的表现。
result: 最优传输构建的群体模板解码准确率最高，且无显著个体偏倚，泛化能力强，并保持皮层拓扑。
conclusion: 基于最优传输的功能模板能有效克服个体间功能变异性，是构建群体解码器的优选方法。
---

## 摘要
个体间差异为跨被试解码大脑活动带来了重大挑战。标准的解剖配准方法虽然能减少形态学差异，但无法捕捉被试之间的功能差异。功能对齐方法通过在个体之间建立体素对应关系，从而构建一个共享的功能空间。该共享空间可以在组水平上通过生成功能模板进行扩展。然而，尽管存在相关工具箱，功能模板在 fMRI 分析中仍然未被充分利用。由于现有方法的多样性和缺乏明确的指南，目前采用这种方法较为困难。对功能模板的全面评估仅限于观看电影范式。在此，我们在任务解码的更一般框架内广泛比较了功能对齐方法（最优传输、Procrustes、岭回归和共享响应模型）和模板构建策略（样本内、样本外、成对）。在该框架中，解码准确度衡量了个体激活模式的对齐程度。通过多个任务和数据集，我们证明使用最优传输构建的群体模板（a）能产生最高的解码准确度，（b）不会因单个被试而产生显著偏差，从而有助于泛化到新被试，以及（c）能保留皮层信号的拓扑结构。

## Abstract
Inter-individual variability poses a significant challenge in decoding brain activity across subjects. While standard anatomical registration procedures reduce morphological differences, they fail to capture functional variability between subjects. Functional alignment methods address this issue by establishing voxel-to-voxel correspondences between pairs of individuals, thereby constructing a shared functional space. This shared space can be extended at the group level by generating a functional template. However, despite the availability of toolboxes, functional templates remain underused in fMRI analysis. Adopting this approach is currently difficult due to the diversity of existing methods and the lack of clear guidelines. Comprehensive evaluations of functional templates are limited to movie-watching paradigms. Here, we extensively compare functional alignment methods (Optimal Transport, Procrustes, Ridge regression, and Shared Response Model) and template construction strategies (in-sample, out-of-sample, pairwise) within the more general framework of task decoding. In this framework, decoding accuracy measures how well individual activation patterns align. Across multiple tasks and datasets, we demonstrate that population templates built using Optimal Transport (a) yield the highest decoding accuracy, (b) are not significantly biased by individual subjects, which facilitates generalization to new subjects, and (c) preserve the cortical signal topography.