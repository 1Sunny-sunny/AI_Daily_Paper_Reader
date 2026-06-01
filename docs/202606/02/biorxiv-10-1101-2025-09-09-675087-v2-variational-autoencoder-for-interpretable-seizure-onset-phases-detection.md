---
title: Variational autoencoder for interpretable seizure onset phases detection
title_zh: 用于可解释的癫痫发作期检测的变分自编码器
authors: "Capallera, I., Mercadal, B., Bartolomei, F., Ruffini, G."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.09.675087v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 可解释的VAE用于SEEG癫痫发作检测
tldr: "本研究针对局灶性癫痫患者的立体脑电图（SEEG）记录，首次提出基于变分自编码器的深度学习框架，实现自动、时间分辨的逐通道发作期与低电压快活动（LVFA）起始检测。方法使用一维VAE编码2秒片段至60维潜在空间，经线性分类及后处理输出0.5秒分辨率标记，在37例患者上验证。结果显示片段级平均召回0.88，通道级发作召回0.84、LVFA召回0.74，发作检测召回99.1%且假阳性仅1%。潜在维度与生理特征高度关联，消融实验证实VAE重建目标提升了检测性能与可解释性。该平台为SEEG自动化分析提供稳健解决方案，有望减轻临床负担。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法未能在连续单通道SEEG记录上联合进行发作期与LVFA的时间分辨注释。
method: 采用一维变分自编码器将2秒SEEG片段编码为60维潜在表示，通过线性分类器区分三类状态，并结合后处理算法生成逐通道0.5秒分辨率的发作标记。
result: "片段级三类平均召回率达0.88，通道级发作召回0.84（发作起始区达0.91），LVFA召回0.74；作为检测器召回99.1%且假阳性1%；潜在维度与振幅、频带功率等可解释特征高度相关。"
conclusion: 该框架首次实现SEEG记录的联合发作与LVFA自动标注，性能优异且具有可解释性，有望大幅减少临床癫痫评估中的手工工作量。
---

## 摘要
目的：我们提出了首个深度学习框架，用于局灶性癫痫患者立体脑电图（SEEG）记录中发作期和低电压快活动起始的自动化、时间分辨的每通道标注。据我们所知，之前没有系统在连续单通道记录上同时处理这些任务。方法：一个一维变分自编码器（VAE）将2秒的SEEG片段编码到一个60维的潜在空间中，并通过线性分类器将它们分类为发作间期、发作期或LVFA。一个后处理算法将片段级概率转换成分辨率为0.5秒的每通道起始标记。该系统在37名具有人工发作期和LVFA标注的患者上使用受试者级别的5折交叉验证进行训练和评估。主要结果：在片段级别，VAE以平均0.88的召回率对三个类别进行了分类。在通道级别，它的发作期召回率达到0.84（在癫痫发作起始区通道上为0.91），LVFA召回率为0.74，中位起始延迟分别为5.0秒和0.86秒。作为癫痫检测器，该系统实现了99.1%的召回率和1%的误报率。潜在维度与生理上可解释的特征（振幅、频带功率、频谱平坦度、能量比）相关。消融研究表明，与仅使用判别式编码器的基线相比，VAE的重建目标提供了双重好处：提高了检测性能，并增强了潜在维度与这些临床有意义特征之间的对齐。意义：通过提供首个用于联合发作期和LVFA标注的时间分辨每通道框架，这项工作为自动化SEEG分析建立了一个稳健且可解释的平台，有可能在术前癫痫评估期间大幅减少临床医生的工作量。

## Abstract
ObjectiveWe present the first deep learning framework for automated, time-resolved, per-channel annotation of ictal and Low-Voltage Fast Activity (LVFA) onsets in stereo electroencephalography (SEEG) recordings of patients with focal epilepsy. To our knowledge, no prior system jointly addresses these tasks on continuous single-channel recordings.

ApproachA one-dimensional Variational Autoencoder (VAE) encodes 2-second SEEG segments into a 60-dimensional latent space and classifies them as interictal, ictal, or LVFA via a linear classifier. A postprocessing algorithm converts segment-level probabilities into per-channel onset markers at 0.5-second resolution. The system was trained and evaluated using subject-wise 5-fold cross-validation on 37 patients with manual ictal and LVFA annotations.

Main resultsAt the segment level, the VAE classified the three classes with an average recall of 0.88. At the channel level, it reached an ictal recall of 0.84 (0.91 on Seizure Onset Zone channels) and LVFA recall of 0.74, with median onset latencies of 5.0 s and 0.86 s, respectively. As a seizure detector, the system achieved 99.1 % recall with 1 % false positives. Latent dimensions correlated with physiologically interpretable features (amplitude, band powers, spectral flatness, energy ratio). An ablation study showed that the VAEs reconstruction objective provides dual benefits over a discriminative encoder-only baseline: improved detection performance and stronger alignment between latent dimensions and these clinically meaningful features.

SignificanceBy providing the first time-resolved per-channel framework for joint ictal and LVFA annotation, this work establishes a robust and explainable platform for automated SEEG analysis with potential to substantially reduce clinician workload during presurgical epilepsy evaluation.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **核心问题**：在局灶性癫痫患者的立体脑电图（SEEG）评估中，临床医生需要手动标注每个通道的发作起始与低电压快活动（LVFA）起始时刻，这一过程极其耗时且依赖经验。现有自动化方法要么仅做发作检测，要么缺乏时间分辨、逐通道的联合标注能力。
- **研究动机**：提出首个能够对连续单通道 SEEG 信号同时进行发作期与 LVFA 起始时间分辨标注的深度学习框架，以大幅降低术前评估的人工负担，并为解释模型决策提供生理可解释性。
- **整体含义**：将变分自编码器（VAE）用于这一临床序列标注任务，既实现了高召回率的自动标注，又通过潜在空间与可解释特征的对齐，增强了模型的透明度和临床可信度。

## 2. 方法论

- **核心思想**：利用一维 VAE 的无监督重构任务作为辅助目标，引导编码器学习到对判别任务有利且可解释的潜在表示，再通过轻量的线性分类器与后处理算法实现逐通道、高时间分辨率的发作起始标记。
- **关键技术细节**：
  - 输入：将 SEEG 原始信号切分为 2 秒长的片段。
  - 编码器：一维卷积（或类似架构）将片段映射到 60 维潜在空间的均值与方差参数，经重参数化得到潜在变量 $z$。
  - 分类器：在潜在变量 $z$ 上接一个线性层，输出三类概率（发作间期、发作期、LVFA）。
  - 训练目标：包含重构损失（如均方误差）与 KL 散度正则项的 VAE 目标，加上分类交叉熵损失，联合优化。
  - 后处理：将片段级概率序列转换为每个通道上 0.5 秒分辨率的发作起始标记，可能包含阈值判断、持续时间约束或平滑等规则。
- **算法流程**（文字概括）：
  1. 滑动窗口截取各通道 2 秒片段，送入 VAE 编码器得到 $z$；
  2. 线性分类器输出片段属于每一类的概率；
  3. 将片段概率拼接为时间序列，利用后处理算法剔除孤立误检并定位起始时刻；
  4. 最终给出每通道的发作期起始和 LVFA 起始时间。

## 3. 实验设计

- **数据集**：37 名局灶性癫痫患者的 SEEG 记录，每名患者均有人工标注的发作期和 LVFA 起始标签。
- **验证策略**：采用受试者级别的 5 折交叉验证，确保训练与测试患者不重叠。
- **评估基准与对比方法**：
  - 主要性能指标：片段级三类召回率、通道级发作召回率和 LVFA 召回率、检测延迟（中位起始延迟）、作为发作检测器时的召回率和假阳性率。
  - 消融研究对比了“仅使用判别式编码器”（无重构目标的纯监督基线），用以验证 VAE 重构目标的贡献。

## 4. 资源与算力

- 论文元数据及所给摘要中未明确提及所使用的 GPU 型号、数量或训练时长等算力信息。
- 因此，无法推断所需的计算资源规模，这是所提供文本信息的局限。

## 5. 实验数量与充分性

- **实验组数**：
  - 主要实验：37 名患者的 5 折交叉验证，提供了片段级和通道级的全面指标。
  - 消融实验：至少包含 VAE 与仅判别式编码器的对比，验证重构目标的作用。
  - 可解释性分析：潜在维度与若干生理特征（振幅、频带功率、频谱平坦度、能量比）的相关性计算。
- **充分性与客观性**：
  - 使用严格的受试者独立交叉验证，避免了数据泄露，比较客观。
  - 数据集规模（37 例）对于交叉验证尚可，但并非大规模多中心数据，结论泛化性需更多验证。
  - 消融实验清晰回答了重构目标是否带来增益，实验设计合理但较简洁，未与其他已有发作检测方法（如传统机器学习或其它深度模型）直接对比，公平性仅体现在与自身基线的比较。

## 6. 主要结论与发现

- **片段级表现**：三类平均召回率达 0.88。
- **通道级表现**：发作期召回 0.84，其中癫痫发作起始区（SOZ）通道召回高达 0.91；LVFA 召回 0.74。中位检测延迟分别为 5.0 秒与 0.86 秒。
- **发作检测器**：全局发作召回率 99.1%，假阳性率仅 1%。
- **可解释性**：潜在维度与振幅、频带功率、频谱平坦度等临床可解释特征显著相关；VAE 的重构目标同时提升了检测性能与潜在维度-特征的对齐程度。
- **消融结论**：去除重构目标会降低性能并削弱可解释性，说明生成式建模在本任务中带来的双重收益。

## 7. 优点

- **首创性**：首次在连续单通道 SEEG 上联合进行发作期与 LVFA 的时间分辨标注。
- **VAE 的巧妙应用**：利用重构任务增强特征学习，并通过潜在空间分析提供了模型的可解释性，而非单纯追求黑箱性能。
- **临床实用性**：后处理算法输出 0.5 秒时间分辨率的标记，可直接辅助临床报告生成，且作为发作检测器时异常低的假阳性率极具实用价值。
- **验证可靠**：受试者级交叉验证避免了信息泄露，指标维度全面，覆盖片段级和通道级。

## 8. 不足与局限

- **数据集局限**：仅来自单中心 37 例患者，未在外部独立队列上验证，泛化性存疑；患者样本量不大，可能无法充分代表各种癫痫发作类型或电极植入方案。
- **对比方法有限**：消融实验仅对比了自身无重构的基线，未与已有的 SEEG 发作检测算法（如传统信号处理或其它深度学习模型）进行标杆比较，难以判断其相对现有方法的确切优势。
- **信息缺失**：缺乏计算资源及训练时间说明；后处理算法的具体细节未在摘要中交代，可复现性可能受影响。
- **延迟指标**：中位发作检测延迟 5.0 秒，在实时预警场景下可能稍高，但用于离线评估可接受。
- **仅针对起始标注**：模型专注于起始时刻检测，未对发作演化过程进行分段，临床应用需进一步扩展。

（完）
