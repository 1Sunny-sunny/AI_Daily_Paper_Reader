---
title: Stimulus and circuit contributions to the information geometry of neural manifolds
title_zh: 刺激和回路对神经流形信息几何的贡献
authors: "Goedeke, S., Kautz, J. K., Leibold, C."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.21.733384v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 将输入调谐与流形几何和Fisher信息联系的微分几何框架
tldr: 系统神经科学中，降维方法发现神经流形但缺乏与网络机制联系。本研究提出微分几何方法，推导拉回度量与费舍尔信息矩阵，表明前馈连接决定表征几何，慢噪声下递归无影响；前馈可生成网格细胞等距表征，递归仅快速降噪。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有降维方法无法将神经流形几何与网络机制及信息编码联系起来，需要严格框架。
method: 采用微分几何分析速率递归网络，推导稳态下流形拉回度量与费舍尔信息矩阵的关系。
result: 发现前馈连接决定信息几何，慢噪声下递归贡献抵消；演示前馈可生成网格细胞环面流形，递归在快速噪声下改善编码。
conclusion: 揭示了前馈连接对表征几何的关键作用，递归选择性降噪，为理解网络构建神经表征提供新见解。
---

## 摘要
理解网络连接如何塑造神经表征是系统神经科学的核心。虽然降维方法揭示了群体记录中的低维流形结构，但将流形几何与网络机制和信息编码联系起来的严格框架仍然缺乏。我们开发了一种微分几何方法来分析接收调谐前馈输入的发放率递归网络中的神经流形。我们推导了神经流形的拉回度规表达式，展示了输入调谐曲线、前馈和递归突触连接如何塑造流形几何。关键的是，我们建立了稳态下的费舍尔信息矩阵也具有拉回度规的结构，直接将内蕴流形几何与刺激可辨别性和信息编码联系起来。对于通过网络传播的慢时间相关性噪声，我们表明递归效应对信息几何的影响相互抵消：费舍尔信息仅依赖于前馈连接。因此，前馈连接关键性地决定了表征几何。作为一个例子，我们证明了一个六边形网格细胞模块对空间网格相位随机分布的表征近似等距。此外，线性前馈变换可以将空间随机的输入调谐曲线映射为六边形网格细胞群，形成环面流形。因此，仅有前馈连接就可以产生结构化的空间表征，而不需要精细调谐的递归连接或连续吸引子动力学。然而，递归连接在快速噪声下被证明可以改善刺激编码，从而实施选择性降噪。

## Abstract
Understanding how network connectivity shapes neural representations is central to systems neuroscience. While dimensionality reduction methods uncover low-dimensional manifold structure in population recordings, a rigorous framework connecting manifold geometry to network mechanisms and information encoding remains lacking. We develop a differential geometric approach for analyzing neural manifolds in rate-based recurrent networks receiving tuned feedforward inputs. We derive expressions for the pullback metric of neural manifolds, showing how input tuning curves, feedforward and recurrent synaptic connectivity shape manifold geometry. Critically, we establish that the Fisher information matrix at steady states also has the structure of a pullback metric, directly linking intrinsic manifold geometry to stimulus discriminability and information encoding. For noise with slow temporal correlations propagated through the network, we show that recurrent effects on information geometry cancel: Fisher information depends only on the feedforward connectivity. Thus, feedforward connectivity critically determines representational geometry. As an example, we demonstrate that the representation of space by a module of hexagonal grid cells is approximately isometric for random distribution of grid phases. Moreover, a linear feedforward transformation can map spatially random input tuning curves into a population of hexagonal grid cells, forming a toroidal manifold. Thus, feedforward connectivity alone can generate structured spatial representations without requiring carefully tuned recurrent connectivity or continuous attractor dynamics. Recurrent connectivity, however, is shown to improve stimulus encoding under fast noise, thereby implementing a selective noise reduction.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：系统神经科学中，利用群体记录降维常能发现“神经流形”，但当前缺乏一个将流形几何与底层网络机制（如前馈、递归连接）以及信息编码联系起来的严格理论框架。
- **整体含义**：本文试图填补这一空白，通过微分几何工具解释网络连接如何塑造神经表征的几何结构，并阐明表征几何如何决定刺激编码效率，为理解“网络结构→流形几何→信息编码”这一链条提供统一视角。

### 2. 论文提出的方法论
- **核心思想**：将稳态发放率递归网络所张成的神经流形视为一个黎曼流形，其上的“拉回度量”（pullback metric）直接连接了输入调谐、突触权重与内在几何。
- **关键技术细节**：
  – 模型：发放率网络接收具有调谐曲线的前馈输入，包含前馈权重 $W^{\text{ff}}$ 和递归权重 $W^{\text{rec}}$。
  – 流形几何：推导出流形上由刺激参数 $\theta$ 诱导的拉回度量 $g(\theta)$，该度量由输入调谐的雅可比矩阵与前馈、递归权重组装而成。
  – 信息联系：证明稳态下费舍尔信息矩阵 $\mathcal{I}(\theta)$ 具备相同的拉回度量结构，从而将刺激可辨别性直接映射为流形的内在距离。
  – 噪声分析：考虑经网络传播的慢时间相关性噪声，发现递归对信息几何的贡献相互抵消，费舍尔信息仅取决于前馈连接；只有快速噪声下递归才能提升编码。
- **公式与算法流程**（概念描述）：
  – 反应动力学方程：$\tau \dot{\mathbf{r}} = -\mathbf{r} + f(W^{\text{ff}}\mathbf{h}(\theta) + W^{\text{rec}}\mathbf{r} + \boldsymbol{\xi})$，其中 $\mathbf{h}(\theta)$ 为输入调谐，$\boldsymbol{\xi}$ 为噪声。
  – 稳态 $\mathbf{r}^*(\theta)$ 定义流形，嵌入诱导的度量为 $g_{ij} = \left(\frac{\partial \mathbf{r}^*}{\partial \theta_i}\right)^\top \left(\frac{\partial \mathbf{r}^*}{\partial \theta_j}\right)$，并可显式表达为权重的函数。
  – 费舍尔信息 $\mathcal{I}(\theta)$ 在慢噪声极限下与 $g(\theta)$ 成比例；快噪声下递归通过调整稳态增益改变度量，实现选择性降噪。

### 3. 实验设计
- **验证场景**：论文主要依赖理论推导，并辅以概念性示例进行验证，并非基于传统基准数据集。
- **主要示例**：六边形网格细胞模块。
  – 展示随机分布的网格相位所对应的群体表征近似构成等距环面流形。
  – 演示一个线性前馈变换即可将空间随机的输入调谐映射为六边形网格细胞群，无需精细调节的递归。
- **对比方法**：未与其它降维或流形分析方法进行系统对比，重点在于建立新框架并说明其解释力。

### 4. 资源与算力
- 全文为理论分析与数值示意，**未提及任何 GPU 型号、数量或训练时长**，推算算力需求极小，仅为普通数值仿真。

### 5. 实验数量与充分性
- **实验数量**：文中仅提供一个核心仿真示例（网格细胞），以及对噪声效应的分析性推导与简单数值验证。
- **充分性**：作为一篇偏理论的论文，该示例足以支撑主要论点（前馈足以生成结构化环面流形；递归在慢噪声下无贡献）。但从实证角度看，缺少在不同网络规模、非线性类型、高维刺激下的系统比较，实验覆盖度有限，无法全面评估框架的普适性。

### 6. 论文的主要结论与发现
- **前馈主导几何**：在慢噪声场景下，信息几何（费舍尔信息）完全由前馈连接决定，递归的贡献在稳态中消失。
- **前馈即可生成结构化表征**：简单的线性前馈变换足以将随机调谐输入转化为具有六边形网格细胞特性的环面流形，无需连续吸引子或精细调谐的递归突触。
- **递归实现选择性降噪**：虽然递归不影响慢噪声下的表征几何，但可抑制快速噪声，改善刺激编码。
- **表征几何与信息编码统一**：拉回度量与费舍尔信息矩阵的同构关系，为“神经流形的内蕴距离直接衡量刺激可辨别性”提供了严格数学基础。

### 7. 优点
- **框架严谨**：将微分几何、网络动力学与信息论有机结合，给出了从权重到表征几何再到信息编码的完整形式化链条。
- **结论简洁有力**：“前馈决定几何，递归只管降噪”的结论对理解网络结构与功能关系具有启发性，并指出了网格细胞等空间表征形成的一种节约网络资源的可能机制。
- **范例直观**：网格细胞的构造性示例直观展示了理论如何解释已知神经现象，增强了方法的可解释性。

### 8. 不足与局限
- **实验验证薄弱**：仅含单一概念性示例，未在实测神经数据或多样的任务条件下检验框架的适用性与鲁棒性。
- **模型假设简化**：基于稳态、线性化及特定噪声假设，未探讨强非线性动力学、尖峰噪声、时间依赖性等现实因素对结论的影响。
- **对比缺失**：未与其他流形分析或表征相似性度量（如 CKA、Procrustes 变换）进行对比，难以判断该方法在分析真实数据时的增益与代价。
- **适用范围待拓展**：当前结论主要由慢噪声极限导出，对于介于快慢之间的噪声时域，递归的贡献如何变化尚不明确。

（完）
