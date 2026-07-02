---
title: Within-electrode temporal envelope processing predicts multi-channel speech outcomes across cochlear implant pulse rates
title_zh: 单电极内时间包络处理预测不同脉冲速率下人工耳蜗多通道语音感知结果
authors: "Azadpour, M., Neukam, J., Capach, N., Svirsky, M."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.734273v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 人工耳蜗时间包络处理预测言语效果
tldr: 本研究探讨人工耳蜗刺激脉冲率如何限制时域包络处理与言语感知。对10名语后聋CI用户，在不同脉冲率下评估调幅检测和辅音识别，发现低脉冲率(125pps)导致表现显著下降，高脉冲率(4000pps)轻微降低，临床常用脉冲率(250-2000pps)保持稳定。单通道与多通道表现显著相关，表明电极内时域包络处理对多通道言语感知至关重要，且脉冲率效果存在个体差异，具有临床意义。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究刺激脉冲率如何约束时域包络处理和言语线索感知，以理解人工耳蜗的编码机制。
method: 在10名语后聋CI用户中，使用临床多通道和单通道策略，测量不同脉冲率下的调幅检测阈值和辅音识别能力。
result: 最低脉冲率(125pps)导致调幅检测和辅音识别显著下降，最高脉冲率(4000pps)出现非显著降低，临床脉冲率(250-2000pps)下表现稳定，且单通道与多通道性能显著相关。
conclusion: 电极内时域包络处理对多通道言语感知有重要贡献，不同脉冲率效应存在个体差异，具有临床相关性。
---

## 摘要
人工耳蜗通过刺激听觉神经元来编码各频段的幅度包络，从而恢复听力，为语音识别提供基本线索。本研究通过评估不同脉冲速率下的幅度调制（AM）检测阈值和辅音识别表现，探讨了刺激脉冲速率如何限制十名语后聋人工耳蜗用户的时间包络处理和语音线索感知。采用标准临床多通道策略和旨在分离通道内包络表征的单通道策略，考察了脉冲速率对时间处理和言语感知的影响。结果表明，在测试的最低脉冲速率125脉冲/秒（pps）下，AM检测和辅音识别表现显著下降，这符合低载波速率下时间处理的感知限制，而非包络采样不足。在最高脉冲速率4000pps下，观察到AM检测的非显著下降，这可能与先前报道的高脉冲速率下幅度辨别能力下降一致。在临床相关的脉冲速率范围（250-2000pps）内，辅音识别表现保持稳定，但观察到听者特异性的脉冲速率效应。值得注意的是，在AM检测和辅音识别任务中，单通道与多通道表现之间存在显著相关性。这些发现支持电极内时间包络处理对多通道言语知觉的重要贡献，并强调了个体差异在脉冲速率效应中的临床相关性。

## Abstract
Cochlear implants (CIs) restore hearing by stimulating auditory neurons to encode amplitude envelopes across frequency bands, providing essential cues for speech recognition. This study investigated how stimulation pulse rate constrains temporal envelope processing and speech cue perception in ten post-lingually deaf CI users by evaluating amplitude modulation (AM) detection thresholds and consonant identification performance across pulse rates. The effects of pulse rate on temporal processing and speech perception were examined using both standard clinical multi-channel strategies and single-channel strategies designed to isolate within-channel envelope representations. Results revealed a significant decline in AM detection and consonant recognition performance at the lowest tested pulse rate of 125 pulses per second (pps), consistent with perceptual constraints on temporal processing at low carrier rates, rather than inadequate envelope sampling. At the highest pulse rate of 4000pps, a non-significant reduction in AM detection was observed which may be consistent with previously reported reductions in amplitude discrimination at high pulse rates. Consonant recognition performance remained stable across clinically relevant pulse rates (250-2000pps), though listener-specific pulse rate effects were observed. Notably, significant correlations were found between single-channel and multi-channel performance in AM detection and consonant recognition tasks. These findings support an important contribution of within-electrode temporal envelope processing to multi-channel speech perception and highlight the clinical relevance of individual variability in pulse rate effects.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

*   **核心问题**：人工耳蜗（CI）通过电刺激听觉神经元来编码不同频段的幅度包络，从而恢复听力。刺激脉冲速率（pulse rate）是编码策略中的关键参数，但既往研究关于脉冲率对言语感知的影响结果不一致：一些研究发现较高脉冲率有益，另一些则未观察到优势或发现低脉冲率更有益，还有研究指出最优脉冲率存在个体差异。该研究旨在直接探究脉冲率对声学包络灵敏度（AM检测）和言语感知（辅音识别）的影响，并检验“单电极内的时间包络处理能预测多通道言语结果”这一假设。
*   **整体含义**：研究希望通过分离通道内和跨通道线索，揭示脉冲率约束时间包络处理的底层机制，从而解释临床上脉冲率效应的不一致性，并为个性化 CI 编程提供依据。

### 2. 论文提出的方法论

*   **核心思想**：通过比较不同脉冲率下的心理物理表现，并利用单通道策略（single-channel）隔离出电极内的时间包络处理，排除跨通道频谱线索的干扰，从而评估“电极内时域处理”对“多通道言语感知”的贡献。
*   **关键技术细节**：
    *   **刺激处理平台**：使用 CCi-MOBILE 研究平台绕过受试者自己的临床言语处理器，实时处理音频并通过 Cochlear Nucleus 植入体传输。
    *   **编码策略**：采用标准临床多通道 ACE（Advanced Combination Encoder）策略和自定义的单通道策略。多通道测试使用 $125, 250, 500, 1000, 2000$ pps（脉冲/秒）五种通道速率，单通道额外增加了 $4000$ pps 条件。单通道策略使用电极阵列中间位置的一个电极（12号或最近可用电极）来编码整个信号的包络。
    *   **响度平衡**：为防止不同脉冲率导致的响度增长差异成为混淆因素，在每种脉冲率下单独测量了受试者的阈值（T-level）和舒适级（C-level），并通过自适应强迫选择法将各速率下的 C-level 响度平衡到一个 $1000$ pps 的参考脉冲串。
    *   **任务指标**：
        *   **辅音识别**：使用 16 个辅音的 `/aCa/` 音节（6 个说话人），计算正确率和基于 Miller & Nicely（1955）方法的发音特征（发音方式、发音部位、清浊）信息传递。
        *   **AM 检测**：使用 25 Hz 正弦调幅的宽带噪声，在 3 间隔 3 选迫选范式中，通过 2下1上的自适应规则测量 AM 深度觉察阈。加了 $\pm 3$ dB 的响度扰动以消除响度线索。

### 3. 实验设计

*   **数据集/场景**：本研究不是计算模型，不涉及典型数据集。被试为 10 名语后聋成人 CI 使用者，均佩戴 Cochlear Nucleus 设备及弯电极阵列，使用 CI 至少 1 年。
*   **对比的“方法”/条件**：
    *   不同脉冲速率条件：$125$, $250$, $500$, $1000$, $2000$, $4000$ pps（多通道仅至 2000 pps）。
    *   策略类型：单通道策略 vs. 多通道ACE策略。
*   **Benchmark**：没有第三方基准模型。该研究将不同脉冲率下的表现进行组内比较，并将多通道表现作为临床参考，分析单通道指标与多通道指标之间的相关性。

### 4. 资源与算力

*   论文是基于心理物理实验和统计分析的研究，不涉及深度学习模型训练或大量计算。文中未提到使用任何 GPU 或训练时长。所有刺激使用 CCi-MOBILE 平台生成与播放，数据分析使用重复测量方差分析（ANOVA）、Pearson 相关等常规统计方法。**没有明确说明算力资源。**

### 5. 实验数量与充分性

*   **实验组数**：
    *   对每个被试，进行了 T、C 级测量（所有电极/脉冲率）。
    *   辅音识别实验：多通道策略（5 种脉冲率）×（最多 288 试次/条件），单通道策略（6 种脉冲率）×（最多 288 试次/条件）。
    *   AM 检测实验：同样对多通道（5 种脉冲率）和单通道（6 种脉冲率）进行了阈限测量。
    *   总计大概完成了 $10$ 名被试 $\times$ ($5$ 种多通道率 $+ 6$ 种单通道率) $\times$ 两项任务的大量数据点。
*   **充分性与公平性**：
    *   实验设计通过单独测量各速率下的电刺激阈值和舒适级，并做响度平衡，控制了不同脉冲率可能带来的响度知觉差异，保证了对比的公平性。
    *   样本量较小（$n=10$），统计功效有限，尤其是进行相关分析和检测高脉冲率下的微弱效应时。作者也承认，$4000$ pps 下 AM 检测的下降未达显著，可能需更大样本验证。
    *   实验排除了跨通道频谱差异（通过单通道）和响度线索（通过平衡与扰动），较为严谨地分离出了脉冲率对通道内时域处理的影响。

### 6. 论文的主要结论与发现

1.  **脉冲率对基本电刺激水平的影响**：T-level 和 C-level 随脉冲率升高而降低，T-level 下降更显著，导致动态范围在高脉冲率下增大。
2.  **辅音识别**：在 $250$–$2000$ pps 的临床相关范围内，平均辅音得分保持稳定。但在 $125$ pps（最低测试率）时，无论是多通道还是单通道策略，识别率均显著下降；$4000$ pps 下个别受试者出现下降，但组平均不显著。信息传递分析显示，发音方式的传递受低脉冲率影响最明显。
3.  **AM 检测**：AM 检测阈限随脉冲率呈倒 U 型趋势。在多通道和单通道中，$125$ pps 下 AM 检测均显著劣于更高脉冲率；$4000$ pps 下观察到非显著下降，部分支持了高脉冲率损害调制灵敏度的假设。AM 检测在单通道策略下显著优于多通道策略，可能因单通道的电流波动更小且有效刺激水平更高。
4.  **单通道与多通道表现的关系**：
    *   单通道和多通道的 AM 检测阈限之间呈强相关（$r = 0.89$）。
    *   单通道和多通道的辅音识别得分之间呈中等显著相关（$r = 0.64$），单通道的包络处理可解释约 40% 的多通道言语得分变异。
    *   这支持“电极内时间包络处理对多通道言语感知有重要贡献”的论点。
5.  **个体差异**：脉冲率效应在个体间变化很大，且同一被试内，不同语音特征的最优脉冲率也可能不同，强调了脉冲率选择的个性化。

### 7. 优点

*   **设计精巧**：使用单通道策略成功分离了“通道内时间包络处理”，排除了跨通道频谱信息的影响，直接回答了研究的核心问题。
*   **控制严格**：为每种脉冲率单独测量 T/C 级并进行响度平衡，有效控制了响度变化这一关键混淆变量。AM 检测中还增加了响度扰动。
*   **分析深入**：不仅报告了总正确率，还分析了发音特征的信息传递，能更细致地揭示脉冲率对特定言语线索（如发音方式）的影响。
*   **与临床关联强**：发现单通道表现可预测多通道结果，提示未来可开发基于单个电极的客观测量方法，用于评估和优化 CI 编程。

### 8. 不足与局限

*   **样本局限**：样本量小（$n=10$），且全为佩戴单一品牌（Cochlear Nucleus）、弯电极阵列的语后聋成人，结果可能无法推广到其他植入体品牌、电极类型或儿童人群。
*   **参数局限**：
    *   多通道策略中固定使用 $N_{\text{max}} = 6$，可能与部分受试者的临床设置不同，轻微限制了总刺激速率。
    *   单通道测试仅使用了中间位置的一个电极，结论无法代表蜗顶或蜗底区域。
    *   只测试了一个 AM 频率（25 Hz），可能高估或低估了调制检测与言语知觉的关系（既往有研究发现更高频的 AM 检测与言语得分相关性更高）。
*   **统计功效**：因样本量小，未能得出 $4000$ pps 下 AM 检测下降的显著结论；AM 检测与辅音识别之间未发现显著相关，也可能受统计功效所限。
*   **残留混淆**：即使进行了响度平衡，不同脉冲率引起的响度增长非线性可能仍有微小的残留效应无法完全排除。

（完）
