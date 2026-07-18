---
title: A geometric and dynamical theory of latent computations in biological neural networks
title_zh: 生物神经网络中潜在计算的几何与动力学理论
authors: "Dinc, F., Blanco-Pozo, M., Klindt, D., Acosta, F., Sylber, C., Jiang, Y., Ebrahimi, S., Shai, A., Tanaka, H., Yuan, P., Miolane, N., Schnitzer, M. J."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737763v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 引入潜在处理单元作为神经群体动力学的理论框架
tldr: 本文提出潜在处理单元（LPUs）的理论框架，通过六个定理统一解释生物神经网络中低维编码与高维动态的关系，揭示编码变量与下游影响分离、线性解码最优性及表征漂移下计算稳定等现象，为系统神经科学提供了因果性计算机制描述。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-002.webp\", \"caption\": \"Figure 1. (Theorem 1, Universal computing). Latent processing units (LPUs) are low-dimensional dynamical systems that have universal computing capabilities.\", \"page\": 39, \"index\": 2, \"width\": 970, \"height\": 998}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-001.webp\", \"caption\": \"Figure 2. (Theorem 2, Computing over extended timescales). Embedding LPUs in large networks allows reliable computations over timescales far slower than cellular time constants.\", \"page\": 43, \"index\": 1, \"width\": 983, \"height\": 619}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-006.webp\", \"caption\": \"Figure 3. (Theorem 3, Optimality of linear LPU readouts). Linear decoders of behaviorally relevant, latent dynamical variables attain performances comparable to nonlinear decoders.\", \"page\": 48, \"index\": 6, \"width\": 864, \"height\": 810}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-004.webp\", \"caption\": \"Figure 4. (Theorem 4, Intrinsic low-dimensional dynamics with extrinsic high-dimensional embeddings). Nonlinear embedding of LPUs with low-dimensional dynamics can lead to extrinsic high-dimensional representations.\", \"page\": 51, \"index\": 4, \"width\": 986, \"height\": 473}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-003.webp\", \"caption\": \"Figure 5. (Theorem 5, Neural coding without causal influence on behavior). Neurons with encoding weights allowing re-entrant influence on LPU dynamics causally shape neural computations, whereas cells lacking this property can merely code for behavioral variables.\", \"page\": 54, \"index\": 3, \"width\": 1002, \"height\": 927}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737763-v1/fig-005.webp\", \"caption\": \"Figure 6. (Theorem 6, Computational robustness to representational drift). LPU dynamics are robust to drift provided the synaptic changes are either purely random or orthogonal to the causally coding subspace.\", \"page\": 59, \"index\": 5, \"width\": 1002, \"height\": 1057}]"
motivation: 现有降维分析无法因果解释生物神经网络如何在单神经元高度变异性下稳定实现低维计算，且方法假设局限。
method: 引入架构无关的潜在处理单元（LPUs）概念，并通过六个定理对其编码与计算动力学进行形式化描述。
result: LPU理论成功解释低维编码产生高维动态、编码神经元对下游影响微弱、线性读出近似最优解码及表征漂移下计算鲁棒等常见实验发现。
conclusion: 该框架统一了几何与动力学观点，为生物神经网络的可信计算机制提供了因果理论。
---

## 摘要
许多神经记录揭示，在大规模的神经活动模式中编码着低维的行为相关变量集合。然而，仅靠降维分析无法因果地解释网络如何稳定执行计算，而使其不受单神经元动态的显著变异性影响。此外，现有的降维方法通常依赖于关于网络结构的简化假设，限制了其适用范围与解释力。为了提供描述高维神经网络中低维计算动态的理论框架，我们在此引入潜在处理单元（LPU）的概念，它们是操作于生物神经回路中的架构无关计算元件。关于 LPU 编码与计算的六条定理共同解释了一系列常见的生物学发现：低维编码变量集合可以产生高维神经动态；许多神经元具有代表行为相关变量的活动模式，但对下游回路影响甚微；神经群体活动的线性读取通常能实现近乎最优的解码；即使网络计算保持完整，神经表征的漂移往往也很显著。总体而言，我们对网络中动态实现的 LPU 的处理，将神经计算的几何视角与动力学视角统一在了一个联合框架之下，并为系统神经科学提供了大脑如何执行可靠计算的因果解释。

## Abstract
Many neural recordings have revealed low-dimensional sets of behaviorally relevant variables encoded within large-scale neural activity patterns. However, dimensionality reduction analyses alone cannot yield causal explanations for how networks stably implement computations that are resilient to the substantial variability of single neuron dynamics. Further, existing methods for dimensionality reduction often rely on simplifying assumptions about network structure that limit their applicability and explanatory power. To provide a theoretical framework describing the dynamics of low-dimensional computation in high-dimensional neural networks, here we introduce the concept of latent processing units (LPUs), which are architecture-agnostic computational elements operating within biological neural circuitry. Six theorems governing coding and computation by LPUs collectively provide explanations for a range of common biological findings: low-dimensional sets of coding variables can generate high-dimensional neural dynamics; many neurons have activity patterns that represent behaviorally relevant variables but exert little influence on downstream circuits; linear readouts of neural population activity commonly permit near-optimal decoding; the drift of neural representations is often substantial even while network computations remain intact. Overall, our treatment of LPUs, as enacted in network dynamics, unifies the geometric and dynamical views of neural computation under a joint framework and provides systems neuroscience with a causal account of how the brain executes reliable computations.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：如何解释生物神经网络在单神经元调谐特性持续漂移（representational drift）且其活动存在高噪声的背景下，仍能稳定实现可靠的低维计算。
- **背景与动机**：
  - 现有降维方法（如 PCA、张量分解）多聚焦于神经活动的几何结构（流形学习），无法提供因果机制。
  - 基于动力学模型的方法（如 rSLDS、低秩 RNN）虽能给出因果解释，但通常依赖强假设（如线性解码子空间、仿射流形），难以与丰富的生物实验证据（如非线性调谐曲线、高维神经流形、表征漂移）相容。
  - 需要一种统一的框架，将几何视角与动力学视角融合，并为神经计算提供因果性解释。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：引入 **潜在处理单元（Latent Processing Units, LPU）** 作为架构无关的神经计算基本元件。
- **四大原则**：
  - **P1 线性编码**：潜在变量 $\boldsymbol{\kappa}(t) \in \mathbb{R}^K$ 是神经活动 $\boldsymbol{r}(t) \in \mathbb{R}^N$ 的线性组合 $\boldsymbol{\kappa}(t) = \boldsymbol{N} \boldsymbol{r}(t)$。
  - **P2 非线性嵌入**：神经动态由非线性函数 $\boldsymbol{\varphi}$ 驱动 $\tau \dot{\boldsymbol{r}}(t) = -\boldsymbol{r}(t) + \boldsymbol{\varphi}(\boldsymbol{\kappa}(t), \boldsymbol{u}(t))$。
  - **P3 行为意义**：行为相关的计算由低维潜在动态系统 $\dot{\boldsymbol{\kappa}} = \boldsymbol{G}(\boldsymbol{\kappa}, \boldsymbol{u})$ 执行。
  - **P4 生物实现**：突触权重 $\boldsymbol{W} \approx \boldsymbol{M} \boldsymbol{N}$ 实现编码矩阵 $\boldsymbol{N}$ 和嵌入矩阵 $\boldsymbol{M}$。
- **LPU 定义**：满足上述原则且具备通用逼近能力的低维动力学系统。
- **六条核心定理**：
  - **定理1（通用计算）**：在神经元数量 $N\to\infty$ 且存在非多项式非线性时，LPU 可逼近任意连续 $K$ 维向量场。
  - **定理2（长时间尺度计算）**：若要实现比单神经元时间常数慢 $\beta$ 倍的计算，网络规模需满足 $N \sim O(\beta^2)$，否则有限尺寸误差会破坏长时间尺度稳定。
  - **定理3（线性读出最优性）**：通过扩展 LPU 维度，任何连续可微的潜在变量函数均可在 $N\to\infty$ 时由线性解码器读出一致逼近，无需显式识别潜在变量。
  - **定理4（神经流形）**：非线性的嵌入使神经活动落在弯曲的低维流形附近 $\boldsymbol{r}(\boldsymbol{\kappa}) \approx \boldsymbol{\varphi}(\boldsymbol{\kappa})$，即使内在维度 $K$ 很低，外在线性维度也可高达 $N$。
  - **定理5（无因果影响的编码）**：只有与编码矩阵 $\boldsymbol{N}$ 的行空间（因果编码子空间）对齐的扰动才能持续影响 LPU 动态；垂直于该子空间的变化（包括与潜在变量相关的）会指数衰减，不改变计算。
  - **定理6（表征漂移鲁棒性）**：若突触权重的漂移是纯随机的或正交于因果编码子空间，潜在动态在一阶近似下保持不变；漂移沿因果方向则会被破坏。
- **理论构建**：架构基本假设为 $\tau \dot{\boldsymbol{r}}(t) = -\boldsymbol{r}(t) + \boldsymbol{f}(\boldsymbol{z}^{(1)}(t), \dots, \boldsymbol{z}^{(L)}(t); \boldsymbol{\xi})$，其中 $\boldsymbol{z}^{(j)}$ 是第 $j$ 个树突隔间的突触前电流。通过低秩分解 $\boldsymbol{W}^{(j)} = \boldsymbol{M}^{(j)} \boldsymbol{N}^{(j)}$ 实现线性编码与非线性嵌入。

### 3. 实验设计：使用了哪些数据集/场景，它的 benchmark 是什么，对比了哪些方法
- **模拟实验场景**：
  - **K-bit flip-flop 任务**：训练基本 RNN（及增益调制 RNN）执行 $2^K$ 状态记忆任务，分析 LPU 的吸引子动力学和分岔实验。
  - **双稳动力学构建**：直接根据目标时间尺度采样 $\boldsymbol{m}, \boldsymbol{n}$ 参数分布，验证定理 2 给出的网络规模与时间尺度关系。
  - **静态流形分析**：将高维单位球通过 sin/tanh 等非线性嵌入，测量外在线性维度。
  - **序列排序任务 RNN**：训练低秩 RNN 做序列排序，观察高维动力学维度。
  - **随机连接低秩 RNN**：验证混沌状态下非线性嵌入同样产生高外在维度。
  - **扰动实验（定理5）**：在 2-bit flip-flop 网络中添加无因果影响的神经元，并添加随机遮掩连接，对比扰动因果与无因果神经元的效应。
  - **连续控制（延迟加法任务）**：训练秩-1 RNN 执行延迟加法，沿编码方向可实现近似线性的连续状态控制，沿读出方向无持久影响。
  - **表征漂移实验（定理6）**：在 flip-flop 任务网络上，对嵌入权重施加三种漂移（纯随机、正交于因果子空间、切向于因果子空间），测量状态估计准确率与漂移耐受力。
- **真实数据验证**：
  - 使用**小鼠全皮层钙成像数据**（视觉辨别任务，8 脑区、平均 3595 个神经元/场次），训练线性与非线性分类器（逻辑回归、LDA、随机森林、QDA）解码试次类型。结果在 PLS 降维到约 15 维时，线性解码器性能匹配甚至略优于非线性解码器，验证定理 3。
- **对比方法**：包括线性/非线性解码器的对比，不同漂移策略的对比，不同网络规模（几百到百万神经元）、不同网络架构（基本 RNN vs 增益调制 RNN）。

### 4. 资源与算力
- 论文**未明确提及** GPU 型号、数量或具体训练时长。
- 提及的训练细节：Adam 优化器，学习率 $10^{-3}$，权重衰减 $10^{-7}$，训练 epochs 在数千到两万之间。大规模网络（百万神经元）采用基于采样的参数生成而非 BPTT 训练，因此算力需求得到控制。整体算力消耗应处于模拟实验的正常范围，无超大规模计算要求。

### 5. 实验数量与充分性
- 实验覆盖了**6 个定理**的模拟验证和 1 个定理的真实数据验证，每一定理下包含多个子实验（不同参数、不同网络架构/规模、不同任务）。
- 涉及的任务包括 flip-flop（2-bit, 3-bit）、序列排序、双稳系统构建、静态流形嵌入、延迟加法等；网络规模从 100 到 1,000,000 神经元。
- 真实数据实验覆盖 6 只小鼠、30 个 session、21,570 个神经元。
- 大部分模拟实验使用至少 30-50 个不同随机种子，展示均值与误差线，评估指标（准确率、误差、维度）的统计稳定性良好。消融实验（如不同漂移类型、不同观测比例 $N_{\text{obs}}$）充分，且与理论推导的误差标度律一致，实验较为充分、客观和公平。

### 6. 论文的主要结论与发现
- LPU 框架成功统一了神经计算的**几何**与**动力学**视角，提供因果解释。
- 即便潜在变量维度很低，**非线性嵌入**也能产生外在高维的、弯曲的神经流形，解释现象中“高维神经活动可能对应于低维计算”。
- **线性读出**在足够大的网络中是近似最优的，不需要复杂的非线性解码器，且无需显式识别潜在变量。
- **神经元的编码权重**（重入连接）决定其对计算的因果影响力，而调谐曲线（由嵌入权重决定）可能与之无关，解释了为什么调谐于行为的神经元扰动可能不引起行为改变。
- LPU 动力学对**表征漂移**具有鲁棒性，只要漂移不沿因果编码方向；大规模网络可进一步增强此鲁棒性。
- 网络实现长时间尺度计算需要**足够大的神经元数量**，定量关系为 $N \sim \beta^2$，为大脑为何动用大量神经元提供新解释。

### 7. 优点：方法或实验设计上有哪些亮点
- **理论严谨且普适**：从最少假设出发推导出 6 个定理，覆盖了编码、计算时间尺度、读出最优性、流形、因果作用和漂移鲁棒性，构成完整理论体系。
- **编码-嵌入分离**：将编码矩阵（线性）和嵌入映射（非线性）明确区分，既保证了线性可识别性与因果子空间的不变性，又允许丰富的非线性表达。
- **与生物现象对齐**：多项结论直接解释了实验中的矛盾现象（如编码-因果分离、高维活动低维计算、漂移鲁棒性），并给出可验证的预测（如有效扰动应限于低维线性子空间）。
- **可扩展至多种架构**：框架覆盖基本 RNN、增益调制 RNN、树突计算模型，并可与低秩 RNN 和 rSLDS 等流行模型关联。
- **数值实验与理论紧密配合**：误差标度律（$\beta/\sqrt{N}$）的验证和漂移下的准确率变化严格支持定理，实验设计精细且系统。

### 8. 不足与局限
- **弱缩放假设限制**：主要分析基于 $\boldsymbol{W}_{ij} \sim O(N^{-1})$ 的自平均区域，未深入涵盖 $O(N^{-1/2})$ 引发的强波动、混沌动力学对计算的影响。
- **LPU 识别的实际困难**：尽管给出了 LPU 的数学定义，但从生物记录中直接估计编码权重 $\boldsymbol{N}$ 和重构潜在动态仍极具挑战性，尤其当记录仅为部分神经元时（定理2 表明需大量神经元才能精准重建长时间尺度 LPU）。
- **漂移模型过于抽象**：仅假设嵌入权重的变化，未映射到具体的生物可塑性过程（如突触周转、稳态可塑性）。
- **学习规则未涉及**：定理建立了 LPU 存在的结构条件，但未给出生物网络如何通过学习形成这些 LPU 的机制。
- **实验预测待检验**：提出的低维有效扰动、弯曲神经流形等预测需要高精度的多细胞干预技术，目前实验证据有限。

（完）
