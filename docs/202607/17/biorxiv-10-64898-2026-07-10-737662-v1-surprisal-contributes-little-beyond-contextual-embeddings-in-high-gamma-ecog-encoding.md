---
title: Surprisal contributes little beyond contextual embeddings in high-gamma ECoG encoding
title_zh: 高伽马ECoG编码中，意外性在上下文嵌入之外贡献甚微
authors: "Sakuma, T."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737662v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 测试惊奇度是否在预测ECoG响应中对上下文嵌入有额外贡献，探究神经编码模型内部
tldr: 本研究探讨了基于大语言模型的词惊异度在预测大脑语言理解神经活动时，是否在上下文嵌入之外提供额外信息。通过分析公开的自然语音ECoG数据，在包含GPT-2 XL嵌入后加入惊异度预测器，发现其并未显著提升高伽马响应的预测准确度，且差异在等价边界内。结果表明，惊异度并非独立预测因子，而仅是嵌入已捕获预测状态的压缩表示。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-004.webp\", \"caption\": \"Figure 1: Main model comparison across all electrodes. Bars show mean held-out Pearson correlation between predicted and observed high-gamma responses, averaged within participant and then across participants, for the prespecified center lag, index 80. The key comparison is Memb+surp versus Memb: contextual embeddings substantially improved prediction relative to Mbase, whereas adding St to Memb did not improve prediction. Consequently, the Mbase bar is visibly shorter than the other four, which cluster close together; the informative contrasts among Memb, Memb+surp, Memb+rot, and Memb+step are small differences within that cluster, reported precisely in Table 1.\", \"page\": 4, \"index\": 4, \"width\": 932, \"height\": 375}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-006.webp\", \"caption\": \"Figure 2: Region-specific model comparisons. Each panel repeats the main model comparison after restricting the response electrodes to the indicated region. Bars show held-out prediction accuracy averaged across electrodes within participant and then across participants at the center lag. Memb improved prediction accuracy relative to Mbase, whereas Memb+surp did not improve performance relative to Memb.\", \"page\": 5, \"index\": 6, \"width\": 976, \"height\": 214}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-001.webp\", \"caption\": \"Figure 3: Participant-level incremental effect of adding surprisal. For each participant, the surprisal increment was computed at the center lag for each electrode and then averaged across electrodes. Each point shows ∆r = r(Memb+surp) − r(Memb) for one participant. The dashed line indicates the sample mean, and all observed increments were small relative to the prespecified equivalence margin of ±0.001 correlation units.\", \"page\": 6, \"index\": 1, \"width\": 932, \"height\": 402}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-003.webp\", \"caption\": \"Figure 4: Incremental performance of candidate update measures. Bars show mean participant-level changes in held-out correlation relative to Memb. Embedding rotation and embedding step size yielded small positive gains relative to Memb.\", \"page\": 8, \"index\": 3, \"width\": 932, \"height\": 372}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-005.webp\", \"caption\": \"Figure 5: Model comparison under the public Podcast tutorial implementation. Using the released tutorial code on 3 participants, Memb outperformed surprisal-only and other feature spaces in mean prediction accuracy across channels. This analysis used the public tutorial implementation; all headline results used the 8-participant processed all_data.pkl file.\", \"page\": 9, \"index\": 5, \"width\": 932, \"height\": 334}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-002.webp\", \"caption\": \"Figure 7: Sensitivity analyses of the main surprisal comparison. Panel (a) shows the 3-participant public tutorial implementation for alternative scalar surprisal measures. Panel (b) shows the same ∆r after replacing the neural target with high-gamma, beta-envelope, or theta-envelope responses. Panel (c) compares shared-ridge and banded-ridge regularization. Panel (d) shows the recovered surprisal increment after injecting a controlled surprisal-shaped signal into the neural response matrix. The common scale is ∆r = r(Memb+surp) − r(Memb), the change in held-out correlation from adding St to Memb.\", \"page\": 11, \"index\": 2, \"width\": 979, \"height\": 735}]"
motivation: 尚不明确词惊异度是否在上下文嵌入基础上为神经预测提供增量信息。
method: 利用自然语音ECoG记录，构建包含基线特征、GPT-2 XL嵌入和惊异度的词对齐岭回归编码模型。
result: 加入惊异度后，留出相关度在中心滞后期基本不变，且在不同滞后和分析中均处于等价边界内。
conclusion: 惊异度不是独立的预测因子，而可视为嵌入所编码更广泛预测状态的压缩读出。
---

## 摘要
意外性和上下文嵌入均源自大型语言模型，被广泛用于预测语言理解过程中的神经响应，但意外性是否在嵌入之外提供了额外信息尚不清楚。我们直接检验了这一问题：在已纳入GPT-2 XL上下文嵌入的情况下，词汇意外性是否能改善对高伽马ECoG响应的样本外预测？利用公开的自然语音ECoG记录，我们使用基线刺激特征、GPT-2 XL嵌入和GPT-2 XL意外性拟合了单词对齐的岭回归编码模型。加入一个意外性预测因子后，在中心滞后点，留出的相关性基本不变，且在不同滞后点和敏感性分析中，效应均保持在预设的等效边界内。这一近乎为零的增益表明，意外性并非作为独立预测因子发挥作用，而更适合被理解为一种对嵌入已捕捉到的相同广泛预测状态的压缩读出。

## Abstract
Surprisal and contextual embeddings are both derived from large language models and are widely used to predict neural responses during language comprehension, but it is unclear whether surprisal adds information beyond embeddings. We test this directly: does word surprisal improve out-of-sample prediction of high-gamma ECoG responses after GPT-2 XL contextual embeddings are included? Using public ECoG recordings from natural speech, we fit word-aligned ridge encoding models with baseline stimulus features, GPT-2 XL embeddings, and GPT-2 XL surprisal. Adding one surprisal predictor left held-out correlation essentially unchanged at the center lag, and the effect remained within a prespecified equivalence margin across alternative lags and sensitivity analyses. This near-zero increment suggests that surprisal does not act as an independent predictor. It is better understood as a compressed readout of the same broader predictive state that the embeddings already capture.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究背景**：意外性（surprisal）和上下文嵌入均从大型语言模型（如 GPT‑2 XL）中提取，已被广泛用于预测人类语言理解时的神经响应（如 ECoG 高伽马活动）。  
- **核心问题**：在编码模型中，当上下文嵌入已经作为预测因子时，意外性（标量，词级累积负对数概率）能否额外提高对神经响应的样本外预测能力？即意外性是否在嵌入之外贡献了独立的信息？  
- **整体含义**：研究旨在区分“边缘关联”与“增量预测价值”，若意外性无额外贡献，则它更适合被理解为一种对嵌入已编码的更丰富预测状态的压缩读出，而非独立的神经预测变量。

## 2. 论文提出的方法论

### 2.1 核心思想
- 使用岭回归建立线性编码模型，预测高伽马 ECoG 响应。基准模型包含传统声学‑语言特征（Mel 谱功率、语音、句法、静态词嵌入）。在此基础上分别加入 GPT‑2 XL 上下文嵌入（1600 维）和词级意外性（标量），通过交叉验证比较加入意外性后留出相关性的变化 $\Delta r = r(M_{emb+surp}) - r(M_{emb})$，并采用两个单侧检验（TOST）与预设等效边界（±0.001 相关性单位）进行等效性检验。

### 2.2 关键技术细节
- **神经响应**：70–200 Hz 高伽马带通滤波后取 Hilbert 包络，在词事件周围按 161 个滞后点采样。  
- **意外性计算**：对每个词的子词 token 计算 $-\log p(\text{token}|\text{context})$，然后在词内求和得到词级意外性 $S_t$。  
- **编码模型**：对于电极‑滞后对，回归模型为 $y_t = \alpha + \mathbf{x}_t^\top \beta + \varepsilon_t$。M_emb 的特征向量 $\mathbf{x}_t$ 包含基线特征和 1600 维嵌入；M_emb+surp 再加入标量 $S_t$。  
- **交叉验证与预处理**：5 折连续分块交叉验证（25 词间隔），每折内对训练数据进行标准化，对高维特征块（频谱、句法、静态嵌入、上下文嵌入）分别进行 PCA 降维（例如上下文嵌入降至 100 维），标量特征不降维。岭回归的惩罚系数从 $\{1,10,10^2,\dots,10^6\}$ 内网格搜索。

### 2.3 评估与统计
- 主指标：留出数据上预测与观测值的 Pearson 相关系数，先在各电极内计算，然后按参与者平均，再跨参与者平均。  
- 增量 $\Delta r$ 通过 TOST 与 ±0.001 边界检验等效性。还报告了唯一解释方差 $R^2_{unique}$。

## 3. 实验设计

### 3.1 数据集与基线
- **主要数据**：公开的 “Podcast” ECoG 数据集（OpenNeuro ds005574），参与者聆听一段 30 分钟的自然叙述。主要分析使用经预处理的 all_data.pkl（8 名参与者，5013 个词事件，161 个滞后点，最多 43 个电极通道；实际有效电极数因参与者而异）。  
- **对比模型**：
  - $M_{base}$：仅基线特征（Mel 谱、语音、句法、静态词嵌入）
  - $M_{emb}$：$M_{base}$ + GPT‑2 XL 上下文嵌入
  - $M_{emb+surp}$：$M_{emb}$ + 词级意外性
  - $M_{emb+rot}$、$M_{emb+step}$：$M_{emb}$ + 上下文嵌入的旋转（$1-\cos(e_t,e_{t-1})$）或步长（$\|\Delta e_t\|_2$）
  - 用于敏感性分析时，还测试了预测熵、熵降等标量特征。

### 3.2 实验场景与多维度验证
- **全电极分析**：对比所有模型在全电极以及特定感兴趣区（颞上回中部、额下回）的预测表现。
- **滞后点分析**：在中心滞后（index 80）外，根据嵌入响应峰值、频谱特征峰值、意外性单独峰值等不同规则选择滞后点重复比较。
- **特征块重叠分析**：计算 $e_t$ 对 $S_t$ 的唯一解释方差和 $S_t$ 对 $e_t$ 的唯一解释方差。
- **替代实现检查**：使用数据集作者公开的教程代码，对 3 名可获取衍生数据的参与者重复主比较，并测试加入意外性、熵或同时加入两者的效果。
- **频带特异性**：将神经靶标从高伽马替换为 theta（4–8 Hz）和 beta（13–30 Hz）包络。
- **正则化方案**：除共享岭惩罚外，使用带状岭回归（banded‑ridge），允许嵌入块和意外性特征块有不同的有效正则化。
- **Spike‑in 校准**：向真实神经响应注入已知幅度的意外性成型信号，验证方法能够检测出接近等效边界的效果（约 5% 响应标准差时达到 0.001 的相关性变化）。

## 4. 资源与算力

- 论文未提及任何 GPU 型号、数量或训练时长。分析依赖于已公开的 GPT‑2 XL 特征（嵌入和意外性），编码模型本身为线性岭回归，计算量较小，因此未特别说明所用计算资源。

## 5. 实验数量与充分性

- **实验组数**：包含主模型比较、区域特异性比较、4 种滞后规则比较、特征块唯一方差分析、3 种上下文更新度量测试、3 名参与者的教程实现验证、3 种频带靶标测试、2 种正则化方案比较、spike‑in 校准（多个注入强度）。总计约十余种不同维度下的对比。
- **充分性与公平性**：实验设计非常系统，通过等效性检验、多种控制条件和敏感性分析验证了结果的稳定性。对比基线全面，交叉验证和 PCA 降维等预处理在每折训练集内进行，避免了数据泄漏。spike‑in 分析证明方法具备足够的灵敏度，增强了结论的可靠性。所有数据和处理代码公开可用，确保了可重复性。

## 6. 论文的主要结论与发现

- **嵌入的核心作用**：$M_{emb}$ 相较于 $M_{base}$ 将留出相关性从接近于零提升至约 $r=0.169$（全电极），在语言相关区域（如颞上回）提升更明显。上下文嵌入捕获了高伽马响应中大部分可预测的方差。
- **意外性的增量为零**：在所有主要和敏感性分析中，$\Delta r = r(M_{emb+surp}) - r(M_{emb})$ 均保持在 ±0.001 等效边界内（中心滞后时约为 $-6.6\times10^{-5}$），TOST 检验支持等效于零。即使选择意外性单独响应最强的滞后点，增量仍低于边界。
- **上下文更新特征的微小增益**：嵌入旋转和步长作为标量特征加入 $M_{emb}$ 后，产生方向一致的小幅正向增量（约 $+2\times10^{-4}$），而意外性无此效果。暗示预测相关的神经活动更可能与上下文状态更新而非纯粹的概率意外性有关。
- **意外性的本质**：意外性在编码模型中不是一个独立预测因子，而是对嵌入已包含的预测状态的一种极度压缩总结。因此，在脑编码研究中宜直接用完整嵌入，意外性本身不应被解释为独立的神经计算信号。

## 7. 优点

- **直接检验增量预测价值**：突破以往仅报告意外性与神经响应的边缘相关或单独比较的做法，回答了“意外性是否在嵌入之上提供新信息”这一关键问题。
- **严格的统计框架**：采用交叉验证、岭回归降维、等效性检验（TOST）和预设实用边界，从假设检验转向等效性评估，结论更保守可靠。
- **全面的敏感性分析**：通过不同的滞后选择、频带、正则化、实现方式和 spike‑in 校准，验证了零结果的稳健性和方法的灵敏度。
- **公开数据与可重复性**：使用标准化开放数据集，提供分析代码，有利于他人复现和拓展。
- **明确的实践建议**：指出在预测神经响应时应优先使用完整的上下文嵌入，并提示标量意外性可带来的局限性。

## 8. 不足与局限

- **模型和特征的线性与词级限制**：编码模型为线性，且时间对齐在词级。可能无法捕捉非线性映射或亚词级别的神经动态，以及错误信号可能以分布、多维、更细时间尺度的方式存在。
- **神经靶标的特异性**：仅分析高伽马、theta、beta 振幅包络，未考虑相位信息、层间分离或不同脑区间的功能连接。
- **语言模型单一**：仅使用了 GPT‑2 XL 一种模型，结论是否可推广至其他架构（如不同层数、注意力机制）或更大的语言模型需进一步研究。
- **参与者数量与刺激多样性**：主要结果基于 8 名参与者，仅聆听一种口语叙事材料。虽然样本量尚可，但能否泛化到更大人群、不同语言材料（如文学性叙事）尚待考察。
- **意外性的定义**：采用词内子词求和的方式计算意外性，可能与某些认知模型（如增量处理的子词方案）有所差异。
- **未触及叙事层级**：分析单位停留在单词，未探讨叙事层面的预测（如角色状态更新、事件边界），这些可能是意外性或上下文更新更有意义的应用场景。

（完）
