---
title: Efficient and reproducible pipelines for spike sorting large-scale electrophysiology data
title_zh: 用于大规模电生理数据棘波分选的高效且可复现的流程
authors: "Buccino, A. P., Sridhar, A., Feng, D., Svoboda, K., Siegle, J. H."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.12.687966v2.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: 大规模电生理数据的尖峰排序流程
tldr: 针对大规模电生理记录带来的计算瓶颈和算法验证不足问题，本文开发了一个端到端并行化spike sorting管线，可在单机、集群或云端高可重复运行，并引入基准测试管线系统性比较算法。结果显示Kilosort4优于Kilosort2.5，且7倍有损压缩几乎不影响性能，为实现数千通道实验的透明、可扩展分析奠定了基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 大规模电生理数据激增，spike sorting耗时且缺乏严格验证，成为主要瓶颈。
method: 提出并行化端到端spike sorting管线和基准测试管线，适配不同计算环境并优化资源。
result: Kilosort4算法表现优于Kilosort2.5，7x有损压缩对spike sorting精度影响极小。
conclusion: 这些管线满足了大规模电生理数据可扩展、透明和高效处理的需求，为高通道实验洪流做好了准备。
---

## 摘要
近年来，体内电生理学的规模不断扩大，同时记录数千个电极的数据已逐渐成为常规操作。这些进展促成了诸多发现，但也带来了巨大的计算需求。棘波分选，即从细胞外电压测量中提取棘波的过程，仍是一个主要瓶颈：几小时内收集的数据集在一台机器上可能需要数天才能完成分选，并且该领域缺乏对众多使用的棘波分选算法和预处理步骤的严格验证。提升棘波分选的速度和准确性对于充分发挥大规模电生理学的潜力至关重要。在此，我们提出了一种端到端的棘波分选流程，利用并行处理来扩展至大规模数据集。同一工作流程可在个人工作站、高性能计算集群或云环境中可复现地运行，且计算资源可根据每个处理步骤进行定制，以降低成本并缩短执行时间。此外，我们引入了一个基准测试流程，同样针对并行处理进行了优化，可系统地比较多种分选流程。利用这一框架，我们展示了广泛使用的棘波分选算法 Kilosort4 优于 Kilosort2.5（Pachitariu 等，2024）。我们还发现，能大幅降低数据存储成本的 7 倍有损压缩对棘波分选性能的影响极小。这些流程共同解决了电生理数据可扩展与透明棘波分选的迫切需求，为该领域即将涌现的数千通道实验做好准备。

## Abstract
The scale of in vivo electrophysiology has expanded in recent years, with simultaneous recordings across thousands of electrodes now becoming routine. These advances have enabled a wide range of discoveries, but they also impose substantial computational demands. Spike sorting, the procedure that extracts spikes from extracellular voltage measurements, remains a major bottleneck: a dataset collected in a few hours can take days to spike sort on a single machine, and the field lacks rigorous validation of the many spike sorting algorithms and preprocessing steps that are in use. Advancing the speed and accuracy of spike sorting is essential to fully realize the potential of large-scale electrophysiology. Here, we present an end-to-end spike sorting pipeline that leverages parallelization to scale to large datasets. The same workflow can run reproducibly on individual workstations, high-performance computing clusters, or cloud environments, with computing resources tailored to each processing step to reduce costs and execution times. In addition, we introduce a benchmarking pipeline, also optimized for parallel processing, that enables systematic comparison of multiple sorting pipelines. Using this framework, we show that Kilosort4, a widely used spike sorting algorithm, outperforms Kilosort2.5 (Pachitariu et al. 2024). We also show that 7x lossy compression, which substantially reduces the cost of data storage, has minimal impact on spike sorting performance. Together, these pipelines address the urgent need for scalable and transparent spike sorting of electrophysiology data, preparing the field for the coming flood of multi-thousand-channel experiments.