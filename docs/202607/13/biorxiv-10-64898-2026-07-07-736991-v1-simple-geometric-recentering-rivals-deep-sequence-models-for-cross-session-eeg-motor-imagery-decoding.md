---
title: Simple Geometric Recentering Rivals Deep Sequence Models for Cross-Session EEG Motor-Imagery Decoding
title_zh: 简单的几何重中心化方法在跨会话脑电运动想象解码中媲美深度序列模型
authors: "Rahimipour, M., Van Hulle, M."
date: 2026-07-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.07.736991v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 用于跨session EEG运动想象解码的几何重定心方法，一种脑机接口应用
tldr: 现有大量EEG运动想象解码研究采用复杂深度架构，但很少在同条件下与简单几何基线对比。本文在8个公开数据集上固定协方差特征，对比基于SPD流形的无监督测试时重新居中切线空间方法与经典黎曼及深度模型。结果显示，跨会话中Geometry-Aware显著优于所有竞争者，证明简单几何方法结合重新居中可有效应对分布偏移，而深度模型未体现优势。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-001.webp\", \"caption\": \"Table 1: The eight benchmark datasets. Cross-session evaluation requires ≥ 2 sessions (last column).\", \"page\": 6, \"index\": 1, \"width\": 535, \"height\": 293}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-004.webp\", \"caption\": \"Figure 1: Cross-session balanced accuracy per dataset. Geometry-Aware (ours) is highest on every dataset.\", \"page\": 7, \"index\": 4, \"width\": 939, \"height\": 394}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-005.webp\", \"caption\": \"Figure 2: Within-session balanced accuracy per dataset. The Geometry-Aware lead over TS+SVM collapses to near zero.\", \"page\": 7, \"index\": 5, \"width\": 940, \"height\": 367}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-011.webp\", \"caption\": \"Table 2: Cross-session: Geometry-Aware vs. the best competing method, per dataset.\", \"page\": 8, \"index\": 11, \"width\": 656, \"height\": 204}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-010.webp\", \"caption\": \"Table 3: Within-session: Geometry-Aware vs. TS+SVM (its recentering-free twin), per dataset.\", \"page\": 8, \"index\": 10, \"width\": 621, \"height\": 291}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-015.webp\", \"caption\": \"Figure 3: Mean balanced accuracy with 95% bootstrap confidence intervals. Left: cross-session (clean separation of Geometry-Aware). Right: within-session (Geometry-Aware and TS+SVM overlap).\", \"page\": 9, \"index\": 15, \"width\": 940, \"height\": 357}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-014.webp\", \"caption\": \"Table 5: Mean balanced accuracy (%) with 95% bootstrap confidence intervals (2000 resamples). Methods ordered by cross-session mean; the Geometry-Aware row is highlighted. Note the identical within-session values for Geometry-Aware and TS+SVM.\", \"page\": 9, \"index\": 14, \"width\": 846, \"height\": 333}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-007.webp\", \"caption\": \"Table 6: Cross-session pairwise comparisons. Upper triangle: paired Cohen’s d (row vs. column; positive = row better). Lower triangle: FDR-corrected p-value. Green = row significantly better; red = significantly worse; grey = not significant after FDR.\", \"page\": 10, \"index\": 7, \"width\": 791, \"height\": 296}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-006.webp\", \"caption\": \"Table 7: Within-session pairwise comparisons, same layout as Table 6. The decisive cell — GeometryAware vs. TS+SVM — is now not significant (d = −0.00, grey), in contrast to cross-session.\", \"page\": 10, \"index\": 6, \"width\": 777, \"height\": 296}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-002.webp\", \"caption\": \"Table 9: Geometry-Aware vs. every other method, both protocols. Effect sizes (Cohen’s d, positive = Geometry-Aware better) and FDR-corrected significance. Codes: *** p < 0.001, ** p < 0.01, * p < 0.05, ns = not significant. Note the single ns cell: within-session vs. TS+SVM.\", \"page\": 11, \"index\": 2, \"width\": 841, \"height\": 356}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-003.webp\", \"caption\": \"Table 10: Average ranks (1 = best) across subject-level observations. Lower is better.\", \"page\": 11, \"index\": 3, \"width\": 735, \"height\": 291}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-012.webp\", \"caption\": \"Figure 4: The mechanism, visualised. From within- to cross-session, Geometry-Aware loses far less accuracy (−2.4 points) than the other strong tangent-space methods (TS+SVM −9.3, FgMDM −6.9), because only Geometry-Aware recenters to correct the between-session drift. The deep Mamba models change little across the gap, but from a much lower overall level.\", \"page\": 12, \"index\": 12, \"width\": 665, \"height\": 452}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-013.webp\", \"caption\": \"Figure 5: Critical Difference diagram, cross-session (N = 88). Geometry-Aware is significantly ahead of every other method.\", \"page\": 12, \"index\": 13, \"width\": 669, \"height\": 354}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-008.webp\", \"caption\": \"Figure 6: Critical Difference diagram, within-session (N = 120). Geometry-Aware and TS+SVM are statistically tied for first.\", \"page\": 13, \"index\": 8, \"width\": 710, \"height\": 354}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-009.webp\", \"caption\": \"Figure 7: Per-dataset margin of Geometry-Aware over the best competitor. Green = win, red = loss. Cross-session: wins everywhere, by +2.1 to +9.0 points. Within-session: small (between −1.2 and +2.7 points) and slightly negative on two datasets, as expected when there is no between-session drift to correct.\", \"page\": 13, \"index\": 9, \"width\": 943, \"height\": 342}]"
motivation: EEG运动想象解码领域深度模型盛行，但缺乏与简单几何基线的公平比较，需验证架构复杂度是否真正必要。
method: 在8个公开MI数据集上，固定协方差特征，比较基于SPD流形的无监督重新居中切线空间方法与经典黎曼及多种深度模型。
result: "跨会话中Geometry-Aware显著优于所有竞争者（Cohen's d=1.06-1.50），会话内与TS+SVM无差异，深度模型均不及经典方法。"
conclusion: 测试时重新居中是关键机制，简单几何解码器在受控条件下可超越复杂深度模型，质疑了架构复杂度的必要性。
---

## 摘要
大量且不断增长的工作将越来越复杂的深度架构应用于脑电运动想象（MI）解码，但很少在相同条件下测试这种复杂性相对于强大的简单几何基线的合理性。我们报告了一项在八个公开MI数据集（3-128通道，2-3类，单会话和多会话）上进行的受控基准测试，该测试固定特征表示，仅改变解码器。核心方法——一种在SPD流形上的紧凑切空间流程，具有无监督测试时重中心化，在此称为Geometry-Aware——与三种经典黎曼基线（TS+SVM、FgMDM、MDM）和一系列基于我们先前架构构建的深度模型（双向Mamba专家混合模型BiMamba+MoE，带有两个缩减的消融变体，以及一个SPDNet风格网络）进行比较，均使用相同的单频带协方差特征。在N=88个跨会话的受试者级观测和N=120个会话内的观测中，Geometry-Aware在跨会话中取得了最佳平均排名，并在会话内统计上与最佳方法并列（原始排名第二，但在临界差异检验下与TS+SVM无区别）。其跨会话优势很大且具有统计决定性——在多重比较校正后，它以大的效应量击败了每个竞争对手（Cohen's d=1.06-1.50；所有p_FDR<1.1x10^-12）——然而在会话内，它相对于无重中心化的孪生方法（TS+SVM）的优势在统计上无法区分（d=-0.00，p=0.54）。这种跨/内双重分离表明重中心化是起作用的机制，而非通用能力。深度序列模型（Mamba变体）尽管特征匹配且训练预算公平固定，但在两种方案下均大幅落后于每种经典黎曼方法；SPDNet基线表现较好——击败了MDM——但在相同特征上仍从未击败简单的切空间流程。我们认为这是一个积极的、控制良好的结果，直接回答了审稿人风格的问题，即架构复杂性是否有必要。我们说明了局限性——深度模型比较的公平性、缺乏直接的机制探究以及数据集范围——并概述了如何将每个局限性转化为具体的下一步工作。

## Abstract
A large and growing body of work applies increasingly complex deep architectures to EEG motor-imagery (MI) decoding, yet rarely tests whether that complexity is justified against a strong, simple geometric baseline under identical conditions. We report a controlled benchmark across eight public MI datasets (3-128 channels, 2-3 classes, single- and multi-session) that holds the feature representation fixed and varies only the decoder. The central method - a compact tangent-space pipeline on the SPD manifold with unsupervised test-time recentering, here called Geometry-Aware - is compared against three classical Riemannian baselines (TS+SVM, FgMDM, MDM) and a family of deep models built from our own prior architecture (a bidirectional Mamba mixture-of-experts, BiMamba+MoE, with two reduced ablation variants, and an SPDNet-style network), all consuming the same single-band covariance features. Across N=88 subject-level observations cross-session and N=120 within-session, Geometry-Aware achieves the best average rank cross-session and is statistically tied for the best within-session (second by raw rank but indistinguishable from TS+SVM under the critical-difference test). Its cross-session advantage is large and statistically decisive - it beats every competitor after multiple-comparison correction with large effect sizes (Cohen's d=1.06-1.50; all p_FDR<1.1x10^-12) - yet within session its advantage over its recentering-free twin (TS+SVM) is statistically indistinguishable (d=-0.00, p=0.54). This cross/within double dissociation points to recentering as the operative mechanism rather than generic capacity. The deep sequence models (the Mamba variants), despite matched features and a fair, fixed training budget, underperform every classical Riemannian method in both protocols by wide margins; the SPDNet baseline fares better - beating MDM - but still never beats the simple tangent-space pipeline on identical features. We argue this is a positive, well-controlled result that directly answers the reviewer-style question of whether architectural complexity is warranted. We state the limitations - fairness of the deep-model comparison, the absence of a direct mechanistic probe, and dataset scope - and outline how each becomes a concrete next step.

---

## 论文详细总结（自动生成）

好的，我将根据论文全文内容，以 Markdown 格式进行结构化总结。

## 论文核心问题与整体含义
- **核心问题**：跨会话的脑电（EEG）运动想象（MI）解码因协方差结构漂移（电极位置、阻抗变化、疲劳等）导致严重性能下降。当前研究主流通过加深模型复杂度（注意力、状态空间模型等）来应对，但很少在相同条件下与强大且简单的几何基线进行公平对比，审视架构复杂度是否真正必要。
- **整体含义**：本文通过严格控制实验，证明一个极简的、带有无监督测试时重中心化的切空间流程（Geometry-Aware）在跨会话场景下大幅超越经典黎曼方法和自研的深度序列模型。该结果并非否定深度学习，而是指出在样本量有限、特征固定的 MI 解码中，正确的几何先验（重中心化）比增加模型容量更有效，提示领域应重视机制而非盲目追逐复杂度。

## 论文提出的方法论
- **核心思想**：在固定特征的前提下，仅改变解码器，以测试无监督重中心化是否能解释跨会话增益。方法名为 **Geometry-Aware**，是一个极简的黎曼几何解码流程。
- **关键技术细节**：
  - **预处理**：每个试次使用 OAS 收缩估计计算空间协方差矩阵（单频带 8–32 Hz，重采样至 250 Hz）。
  - **流形映射**：将协方差矩阵投影到对称正定（SPD）流形的切空间（仿射不变黎曼度量），得到切向量。
  - **分类**：对切向量使用 $L_2$ 正则化的逻辑回归进行分类。
  - **重中心化机制（核心）**：在**跨会话协议**下，启用 `tsupdate=True`，即**测试时**利用无标签测试会话数据重新估计切空间的参考点（几何均值），从而刚性校正会话间的整体几何漂移。该步骤完全无监督。会话内协议则关闭重中心化（`tsupdate=False`），作为机制控制的消融实验。
  - **算法流程**：
    $$
    \text{Covariances}(\text{estimator}=\text{"oas"}) \rightarrow \text{TangentSpace}(\text{metric}=\text{"riemann"}, \text{tsupdate}=\text{True/False}) \rightarrow \text{LogisticRegression}
    $$

## 实验设计
- **数据集与场景**：使用 **8 个公开 MI 数据集**（来自 MOABB），覆盖 3–128 通道，2–3 类（取前三类），包括单会话（3个）和多会话（5个）两种场景。多会话数据集用于跨会话评估，所有 8 个数据集均参与会话内评估。
- **Benchmark 与协议**：
  - **特征固定**：所有方法输入完全相同的 OAS 协方差特征，消除特征工程差异。
  - **跨会话协议**：留一会话法（leave-one-session-out），训练于保留会话，测试于目标会话，要求至少 2 个会话。
  - **会话内协议**：5 折分层交叉验证（无重中心化，作为对照）。
  - **对比方法**：
    1.  **经典黎曼基线**：`TS+SVM`（无重中心化的孪生方法，仅分类器不同）；`FgMDM`；`MDM`。
    2.  **深度序列模型**（基于作者先前架构，输入相同协方差特征）：`BiMamba+MoE`（双向 Mamba 专家混合）、`BiMamba no-MoE`、`Mamba uni`（单向）。
    3.  **SPDNet风格**：批归一化 MLP 直接作用于切向量，隔离“深层 vs. 线性”对比。
- **统计验证**：使用 Friedman 检验、配对 Wilcoxon 检验（FDR 及 Holm 校正）、Cohen's d 效应量、2000 次 Bootstrap 置信区间及 Nemenyi 临界差异图（CD 图），确保所有结论均有严格统计支持。

## 资源与算力
- 论文提及实验在 **KU Leuven VSC 集群**上无人值守运行，并配有自动存档与恢复。
- 深度模型训练配置固定：**20 个 epoch，batch size 128**，Adam 优化器，余弦退火学习率，梯度裁剪，seed=42。模型参数规模在**数十万级别**，刻意设计为轻量模型以适应小样本。
- **未明确说明**具体使用了何种型号的 GPU 及数量，训练耗时也未提及。

## 实验数量与充分性
- **实验数量**：共进行 **N=88 次跨会话受试者级评测**和 **N=120 次会话内评测**。每个协议下，所有 8 种方法在所有数据集上均得到测评，构成了 `8 方法 × 88/120 观测值` 的完全配对矩阵。
- **消融与稳健性**：
  - 跨会话与会话内的**双重分离对照**：通过切换 `tsupdate` 精确归因重中心化的贡献。
  - 深度模型的**内部消融**（MoE、双向性）。
  - **稳健性检查**：移除样本最多的 Lee2019_MI（54/88），跨会话核心效果不变（d=1.10）；使用保守的**数据集级别符号检验**（N=5）也得到一致方向。
- **公平性**：所有方法共享完全相同的输入、评估协议和随机种子；深度模型使用固定、标准的训练预算且无逐数据集调参，确保了比较的客观性。实验设计从统计层面到机制层面均具有高度充分性。

## 论文的主要结论与发现
1.  **跨会话优势分明**：Geometry-Aware 跨会话平均准确率最高（78.5%），在所有 5 个多会话数据集上均战胜最佳竞争对手，平均排名第一，且经 FDR 校正后显著优于全部对手（$d=1.06-1.50, p_{\text{FDR}}<1.1\times10^{-12}$）。
2.  **会话内优势消失**：会话内 Geometry-Aware 与 TS+SVM 准确率几乎相同（均为 78.3%，$d=-0.00, p=0.54$），在 CD 图上统计绑定并列第一。
3.  **重中心化是关键机制**：跨会话大幅领先、会话内无差别的双重分离表明，性能提升并非来自模型容量或分类器差异，而是具体归因于无监督重中心化对会话间几何漂移的校正。
4.  **深度模型未能匹敌**：在相同特征和公平训练下，所有 Mamba 变体均显著弱于所有经典黎曼方法；SPDNet 虽优于 MDM，但仍从未超过简单的切空间+SVM/逻辑回归。这提供了复杂度在此问题设定下不被支持的证据。

## 优点
- **控制极佳的基准测试**：唯一变量是解码器，排除了特征工程这一最通常的混淆因素。
- **精密的机制归因**：通过“跨/会内双重分离”设计，将性能提升精准锁定于重中心化，是可证伪的实验逻辑。
- **全面的统计严谨性**：采用非参数检验、多重比较校正、效应量、bootstrap 和 CD 图，结论可信度高。
- **负责任的自我对标**：深度比较对象为作者自己的架构，并坦然报告其未优于简单基线，该态度增强了研究诚信。

## 不足与局限
- **深度模型比较的公平性边界**：虽然训练过程固定且合理，但未进行大规模的超参/架构搜索，因此不排除另一种深度模型设计或巨量调参可缩小差距。这留下了一个“更优深度模型”的可能性，但论文本身已明确其目的并非寻找最优深度模型。
- **缺乏直接机制探针**：重中心化的作用仅通过间接统计证据（双重分离）推断，未直接测量并展示校正前后会话间的黎曼距离或漂移量，缺少可视化定量验证。
- **表示限制单一**：固定单频带、单协方差特征，若使用更丰富特征（如多频带、CSD），结果是否变化未知。
- **数据集覆盖与类别裁剪**：数据集整体偏向中低通道数，且被统一裁剪为前三类并使用平衡准确率，与原始多类设定下的结果不完全可比。

（完）
