---
title: Low-latency neuromorphic closed-loop control of hippocampal ripples in vivo
title_zh: 低延迟神经形态闭环控制活体海马尖波涟漪
authors: "Alves, P., Jurado-Parras, M.-T., Freitas, J., Ventura, J., de la Prida, L. M., Aguiar, P."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.09.737518v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 神经形态闭环系统实现海马尖波涟漪的实时检测与调控
tldr: "针对实时闭环神经调控中高带宽信号处理的低延迟与能效挑战，本文利用神经形态计算实现体内海马涟漪的快速检测与控制。通过训练紧凑脉冲神经网络（41神经元、530参数），在SpiNNaker硬件上部署，与Open Ephys集成达到约50毫秒闭环延迟，可在高达80%的涟漪中进行事件内刺激。清醒小鼠实验验证了该框架可有效抑制涟漪动态，为体内快速脑振荡的闭环操控提供了实用、低功耗的方案。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-001.webp\", \"caption\": \"Figure 1 - Spike-based encoding and SNN architecture for neuromorphic ripple detection. A, Hippocampal local field potentials (LFPs) were bandpass filtered in the ripple range (100-250 Hz) and converted into sparse UP and DN spike trains using asynchronous delta modulation. Encoded spike trains were downsampled from 30 kHz to 1 kHz to match the 1 ms timestep used for SNN simulation and neuromorphic deployment. B, Representative reconstruction of the ripple-band signal from UP/DN spike events, illustrating preservation of high-frequency ripple structure after spike-based encoding. C, Encoding metrics comparing ripple and non-ripple baseline segments. Average firing rate (AFR) was markedly higher during ripples than during baseline activity, and reconstructed signals showed higher signal-to-noise ratio (SNR) during ripple segments, indicating preferential encoding of event-relevant dynamics. Data are shown across channels/sessions as indicated in Methods; statistical comparisons were performed using two-sided Wilcoxon signed-rank tests. D, Continuous spike trains were segmented into overlapping windows for supervised training, with ground-truth labels assigned according to the temporal alignment between each window and annotated ripple events. E, SNN architecture used for ripple detection. The network receives two input streams corresponding to UP and DN events and comprises two fully connected hidden layers of leaky integrate-and-fire neurons, with 24 and 16 units, followed by a single output neuron that signals ripple detections. Networks were trained by backpropagation through time using surrogate-gradient learning.\", \"page\": 6, \"index\": 1, \"width\": 943, \"height\": 627}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-005.webp\", \"caption\": \"Figure 2 - SNN ripple detection performance in continuous LFPs and comparison with established detectors. A, Representative SNN detection over 300 s of continuous hippocampal LFPs, with a 10 s zoomed segment. Ripple-band LFPs, manually annotated ground-truth (GT) ripples, SNN output spikes and event classifications are shown. TP, true positive; FP, false positive; FN, false negative. B, Representative raster plot showing UP/DN input events, GT ripples, ripple-band LFPs, hiddenlayer spiking activity and output spikes during continuous SNN processing. Output spikes correspond to putative ripple detections. C, Distribution of precision, recall and F1-score across recording sessions (n = 23), aggregated as the median performance of the selected SNN configurations. The SNNs showed high recall and lower precision, reflecting the precisionrecall trade-off observed across sessions. D, Relationship between ripple rate and detection performance. Ripple rate was strongly correlated with precision and F1-score (Spearman’s ρ = 0.85, p < 0.01 for both), whereas recall remained stable across sessions (ρ = −0.15, p = 0.48). E, Benchmark comparison against conventional filter-based detectors and deep-learning models: Buzsáki-style RMS detector (Fernández-Ruiz et al., 2019), Dutta filter-based detector (Dutta et al., 2018), RippleNet (Hagen et al., 2021), 1D-CNN (Navas-Olive et al., 2022), and LSTM model (Navas-Olive et al., 2024). Models were evaluated using standard out-of-the-box parameters and parameters optimized for maximum F1-score on this dataset. The SNN achieved\", \"page\": 9, \"index\": 5, \"width\": 877, \"height\": 1043}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-004.webp\", \"caption\": \"Figure 3 - Feature structure of SNN-detected, missed and false-positive ripple-band events. A, Representative 400 ms LFP snippets filtered in the ripple band (100-250 Hz), illustrating true positives (TPs), false positives (FPs) and false negatives (FNs). Manually annotated ground-truth ripples and SNN output spikes are indicated. B, Event-triggered ripple-band power centered on the event peak (±50 ms). TPs showed higher ripple-band power, whereas FPs and FNs exhibited similar lower-amplitude profiles. Data are shown as mean ± 95% confidence interval for events detected or missed by the best-performing network. C, Feature profiles of TP, FP and FN events. Radar plots show median and interquartile range across events for peak power, mean power, average UP/DN firing rate (AFR), spectral entropy, peak frequency and skewness of the curvature. Features were normalized for visualization. TPs showed higher power, AFR, peak frequency and curvature skewness than both FPs and FNs. Direct comparison between FPs and FNs showed that FPs had lower peak frequency (Mann-Whitney test, p < 0.001, Cliff’s δ = 0.2) and higher AFR (p < 0.001, Cliff’s δ = −0.3). Differences in entropy and peak power reached statistical significance but had negligible effect sizes (Cliff’s δ ≤ 0.1). D, Uniform Manifold Approximation and Projection (UMAP) visualization of the eventfeature space. E, Principal Component Analysis (PCA) visualization of the same feature space. Both projections revealed a continuous distribution without clear separation between event classes, with substantial overlap between FP and FN events.\", \"page\": 12, \"index\": 4, \"width\": 943, \"height\": 700}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-002.webp\", \"caption\": \"Figure 4 - Neuromorphic deployment preserves online ripple detection and enables energy-efficient operation. A, Open Ephys signal chain used for online in silico validation. Pre-recorded LFPs were streamed through the Open Ephys File Reader and ZMQ Interface plugins to an external Python bridge, encoded into UP/DN spikes and processed by the SNN running on SpiNNaker hardware. Feedback events generated by the output neuron were returned to Open Ephys through Network Events and logged for post-hoc analysis. B, Precision-recall trade-off across output-neuron firing thresholds during SpiNNaker operation using 6 ms buffers. Data points show median performance across recording sessions (n = 23), with error bars indicating interquartile range. C, F1-score as a function of firing threshold. Thresholds between 0.8 and 1.0 produced the highest overall performance and significantly outperformed the remaining tested thresholds after Holm-Bonferroni correction (Wilcoxon signed-rank tests, p < 0.01). Within this range, threshold 0.9 achieved higher F1-score than threshold 0.8 (p < 0.01). D, Performance impact of deployment from software simulation to SpiNNaker hardware and transition from offline continuous processing to online buffered processing. The software-to-hardware transition produced a modest but significant reduction in F1-score at thresholds 0.8 (p < 0.001), 0.9 (p < 0.001) and 1.0 (p < 0.05). In contrast, online buffered processing preserved performance relative to offline SpiNNaker processing at the most balanced operating thresholds. E, False positive and false negative rates as a function of firing threshold. Increasing the threshold reduced false positives per minute while increasing missed detections, illustrating the operational trade-off between stimulation specificity and detection sensitivity. F, Power consumption (Watts) associated with SNN simulation and inference using a regular GPU, CPU, and the SpiNNaker neuromorphic board (total power and power dedicated to simulation), n=14 sessions. SpiNNaker shows a 16/20-fold reduction in power consumption compared to CPU/GPU, that can go up to 170/200-fold when considering only the power consumed by the actual simulation (disregarding background processes).\", \"page\": 15, \"index\": 2, \"width\": 943, \"height\": 395}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-003.webp\", \"caption\": \"Figure 5 - Hardware-in-the-loop validation of closed-loop latency and intervention timing. A, Hardware validation setup. Prerecorded hippocampal LFPs were generated by a National Instruments NI-9264 data acquisition board (1), routed through the Open Ephys I/O board (2) and acquired by the Open Ephys Acquisition Board (3). Signals were streamed to the host computer (4), encoded into UP/DN spikes and sent through a Python bridge to the SNN running on SpiNNaker hardware (5). SNN detections triggered an Arduino MEGA 2560 output (6), which was looped back to the Open Ephys I/O board for round-trip latency measurement. B, Effect of feedback-triggering pathway on round-trip latency. Latency was compared using the Open Ephys Arduino Output plugin, direct Python control of the Arduino output and the offline simulation baseline, with buffer size fixed at 3 ms and firing threshold fixed at 0.8. Direct Python control significantly reduced latency relative to the Open Ephys plugin (Mann-Whitney U, p < 0.001). Data is shown as median with 5th-95th percentiles. C, Relationship between buffer size, round-trip latency and ripple duration. Latency increased approximately linearly with buffer size, as quantified by a linear mixed-effects model (slope = 0.84 ms per 1 ms buffer increase, p < 0.001). Relative latency analysis showed that stimulation before ripple termination was consistently achieved only with short buffers. D, Latency-performance trade-off across buffer sizes. Median F1-score and latency are shown as a function of buffer size. Larger buffers modestly improved detection performance but imposed a substantial latency cost. F1-score was strongly correlated with buffer size (Spearman’s ρ = 0.93, p < 0.01; linear mixed-effects model predictor = 0.002, p < 0.001). Data are shown as median ± interquartile range. E, Effect of firing threshold on latency using the two shortest buffer configurations, 3 ms and 6 ms. Higher thresholds increased latency, although all tested configurations maintained median relative latencies below ripple duration. F, Joint latency-performance trade-off across buffer size and firing threshold. Increasing the buffer from 3 to 6 ms improved F1-score across thresholds (Wilcoxon signed-rank test, p < 0.01). Threshold 0.9 yielded the highest median F1-score and significantly outperformed threshold 1.0 (Wilcoxon signed-rank test, p < 0.001), but was not statistically superior to threshold 0.8, which provided lower latency and higher intra-event intervention probability.\", \"page\": 18, \"index\": 3, \"width\": 796, \"height\": 770}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737518-v1/fig-006.webp\", \"caption\": \"Figure 6 - In vivo closed-loop ripple manipulation using the neuromorphic framework. A. Schematic of the closed-loop optogenetics setup. Neural signals from the CA1 hippocampus of a head-fixed mouse (1) are acquired via µLED optoelectrodes connected to an Open Ephys Acquisition Board (2). Data is streamed to the host computer (3), and spike-encoded for processing by the SNNs running on the SpiNNaker board (4). Detections trigger an Arduino MEGA 2560 (5) to drive a 100 ms inhibitory optogenetic pulse via the light stimulator (6). B. In vivo detection performance. Post-hoc evaluation of performance across sessions (n=12) displays wide inter-session variability. C. Round-trip latency versus event duration. Utilizing a preliminary unoptimized configuration (20 ms buffer), the median detection latency exceeded the median event duration (median relative latency = 126%). D. Peri-detection power profile. Average ripple-band power (mean ± SEM) centered on detection time (t=0), normalized per window. Comparison of mean power in the post-detection window (+50 ms) reveals a nonsignificant but large magnitude reduction in \\\"ON\\\" sessions (4 sessions OFF, 8 sessions ON, Mann-Whitney U, p=0.07, δ=0.69). E. Radar Plot characterizing the impact of light stimulation on ripple features (top 25% longest events per session). Data is shown as the median and interquartile range across sessions. Features include: Peak and Mean Power (z-scored), Duration (ms), Spectral Entropy, Peak Frequency (H_Freq, Hz), ratio of long ripples (R>80 ms, calculated across all ripples), low frequency contribution (L_Freq) and Energy. Values are normalized between the minimum and the 3rd quartile for visualization. Optogenetic inhibition seems to have significantly altered ripple dynamics, as \\\"ON\\\" sessions exhibit significantly lower energy (𝑝 = 0.048*, δ=0.75), and also higher spectral entropy (δ=-0.56), lower peak frequency (δ=0.56), a reduced fraction of long-duration ripples (δ=0.56), and a higher low frequency contribution (δ=-0.69).\", \"page\": 20, \"index\": 6, \"width\": 943, \"height\": 571}]"
motivation: 实时闭环操控快速脑动态面临延迟和能效瓶颈，神经形态计算虽具潜力，但缺乏对体内瞬时振荡的验证。
method: 采用替代梯度反向传播训练小型脉冲神经网络，部署于SpiNNaker神经形态硬件，并与Open Ephys平台集成构建闭环系统。
result: "在清醒小鼠中实现约50毫秒总延迟，80%涟漪获事件内刺激，且神经形态触发的光遗传抑制显著改变涟漪动态并降低振荡能量。"
conclusion: 该神经形态框架实现了体内快速脑动态的低延迟闭环控制，为记忆相关节律的研究与干预提供了高效、可及的工具。
---

## 摘要
实时闭环神经调控，即根据进行中的脑动态精确定时施加刺激，对于治疗神经系统疾病和探究神经环路功能具有变革性潜力。然而，这需要低延迟、高能效地处理高带宽神经信号，传统计算架构难以满足。神经形态计算模仿生物神经环路的事件驱动和大规模并行操作，提供了一种有吸引力的替代方案。但其在体内经验证的、针对快速瞬态振荡的闭环框架中的整合尚未得到展示。在此，我们提出一个完全集成的神经形态框架，用于实时检测和操控海马尖波涟漪：短暂（30-100毫秒）、高频（100-250赫兹）的振荡，对记忆巩固至关重要，并与神经系统疾病有关。我们使用替代梯度反向传播训练了包含41个神经元和530个参数的紧凑型脉冲神经网络，在23个记录会话中取得了与深度学习模型相媲美的检测性能，同时在SpiNNaker神经形态硬件上部署时能耗降低多达200倍。与开源Open Ephys平台的整合实现了约50毫秒的总闭环延迟，使得在高达80%的涟漪中能够进行事件内刺激。在清醒、头部固定的清醒小鼠中验证完整的感知-处理-刺激通路，我们证明神经形态触发的光遗传抑制显著改变涟漪动态并降低振荡能量。这项工作为活体快速脑动态的低延迟闭环控制建立了一个实用且易于使用的神经形态框架。

## Abstract
Real-time closed-loop neuromodulation, in which stimulation is precisely timed to ongoing brain dynamics, holds transformative potential for treating neurological disorders and probing neural circuit function. However, it requires low-latency, energy-efficient processing of high-bandwidth neural signals that conventional computing architectures struggle to deliver. Neuromorphic computing, which emulates the event-driven and massively parallel operation of biological neural circuits, offers a compelling alternative. Yet, its integration into closed-loop frameworks validated in vivo for fast, transient oscillations has not been demonstrated. Here, we present a fully integrated neuromorphic framework for real-time detection and manipulation of hippocampal ripples: brief (30-100 ms), high-frequency (100-250 Hz) oscillations that are critical for memory consolidation and implicated in neurological disorders. We train compact spiking neural networks comprising 41 neurons and 530 parameters using surrogate-gradient backpropagation, achieving detection performance competitive with deep learning models across 23 recording sessions while consuming up to 200-fold less energy when deployed on SpiNNaker neuromorphic hardware. Integration with the open-source Open Ephys platform yields total closed-loop latencies of approximately 50 ms, enabling intra-event stimulation in up to 80% of ripples. Validating the complete sensing-processing-stimulation pipeline in awake, head-fixed mice, we demonstrate that neuromorphic-triggered optogenetic inhibition significantly alters ripple dynamics and reduces oscillatory energy. This work establishes a practical and accessible neuromorphic framework for low-latency closed-loop control of fast brain dynamics in vivo.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **核心问题**：实时闭环神经调控要求对高带宽神经信号进行**低延迟、高能效**处理，但传统冯·诺伊曼架构难以同时满足。神经形态计算（事件驱动、大规模并行）在理论上极具优势，却一直缺少可在活体（in vivo）中操控**快速瞬态振荡**的完整闭环验证。
- **整体含义**：本文以**海马尖波涟漪**（100–250 Hz，30–100 ms）这一记忆巩固关键且病理相关的快速节律作为严苛测试场景，首次实现了一个**完全集成的神经形态闭环框架**，从活体信号采集、脉冲神经网络（SNN）实时检测到光遗传反馈刺激，验证了用低功耗神经形态硬件在数十毫秒内干预脑动态的可行性。

## 2. 方法论

- **信号编码与预处理**  
  - 将原始 LFP 带通滤波至涟漪频段（100–250 Hz），使用**异步差分调制**（step-forward encoding）将连续信号转换为 UP 和 DN 两路稀疏脉冲序列。  
  - 编码基线阈值 $T_{\mathrm{base}}$ 每 10 s 自适应更新；脉冲序列从 30 kHz 降采样至 1 kHz，以匹配神经形态硬件的 1 ms 仿真步长。

- **SNN 架构与训练**  
  - **网络结构**：前馈全连接，两个输入通道（UP/DN），两个隐藏层（分别 24 和 16 个 LIF 神经元），1 个输出 LIF 神经元作为涟漪检测器（共 41 神经元、530 可训练参数）。  
  - **学习算法**：基于替代梯度的时间反向传播（SG-BPTT），优化**首脉冲时间均方误差（TTFS-MSE）损失**，并引入对假阳性、假阴性的额外惩罚。  
  - **训练细节**：窗口长度 180 ms，对无涟漪窗口欠采样以缓解类失衡；用 snnTorch + PyTorch 训练，Adam 优化器，学习率 $10^{-5}$，权重更新速率 5 倍于偏置。

- **神经形态硬件部署**  
  - 部署到 **SpiNNaker SpiNN‑3 板**。模型从 snnTorch （离散时间）翻译至 PyNN/SpiNNaker （连续时间），需要将突触时间常数 $\tau_{\mathrm{syn}}$、膜时间常数 $\tau_{\mathrm{m}}$ 等参数进行等效转换（$\tau = -1/\ln(x)$），并补偿膜电阻 $R_{\mathrm{m}}$ 的影响。  
  - 为保持输入缓冲区的精确时间结构，构建了**延迟线输入架构**，使得同一缓冲区的脉冲虽同时注入但按突触延迟依次到达 LIF 层。

- **闭环系统集成**  
  - 完整流水线：Intan 头阶段 → Open Ephys 采集板 → 主机 Python 桥（滤波、编码）→ 以太网传输 → SpiNNaker 上 SNN 实时推理 → 检测触发 → Arduino 输出 TTL 脉冲驱动光刺激。

## 3. 实验设计

- **数据集**  
  - 公开的海马 CA1 纹波 LFP 数据集（Figshare:117897）及额外提供的新会话，共 **23 个记录会话**（来自 5 只小鼠），包含 **2719 个人工标注的涟漪事件**。  
  - 体内验证使用 **2 只转基因小鼠**（PV‑Cre、SST‑Cre），共 12 个会话（4 OFF, 8 ON）。

- **基准对比（Benchmark）**  
  - 传统方法：Buzsáki‑style RMS 检测器、Dutta 滤波检测器；  
  - 深度学习方法：RippleNet（RNN）、1D‑CNN、LSTM（RipplAI）。  
  所有方法均采用**标准参数**和**针对该数据集优化至最大 F1 的配置**进行评估。

- **评估指标**  
  - 检测性能：精确率、召回率、F1 分数，以及假阳性/假阴性率（事件/分钟）。  
  - 闭环性能：往返延迟（round‑trip latency）、涟漪内刺激比例、功耗。  
  - 效应分析：纹波能量、谱熵、峰值频率、长涟漪比例等。

## 4. 资源与算力

- **训练资源**：文中未提及训练所使用的 GPU 型号、数量及训练时长，仅说明使用 snnTorch + PyTorch 进行 SG‑BPTT 训练。  
- **推理能耗对比**（14 个会话）：
  - GPU 约 **70 W**，CPU 约 **53 W**（均无法满足实时性）；
  - SpiNNaker 板总功耗约 **3.6 W**，其中模拟实际只占 **≈0.35 W**；
  - 相比 CPU/GPU 降低了 **16/20 倍**（若仅计仿真功耗可达 **170/200 倍**）。

## 5. 实验数量与充分性

- **离线性能评估**：在 23 个会话上对 SNN 进行系统评估，并与 5 种基准检测器（分别用标准、优化参数）对比，**全面且公平**。
- **硬件部署与参数扫描**：在 SpiNNaker 上扫描了阈值（0.8–1.0）、缓冲大小（3–40 ms）与触发通路对延迟‑性能的影响，统计检验充分（线性混合效应模型、Cliff’s δ、Holm‑Bonferroni 校正等）。
- **错误分析**：利用 UMAP、PCA 和辐射图对 TP、FP、FN 事件的多维特征进行深入分析，揭示了错误主要来自低振幅模糊事件。
- **体内验证**：在清醒固定小鼠中实现完整的感知‑处理‑刺激闭环，但样本量较小（2 只小鼠，12 个会话，且使用的是未优化的 20 ms 缓冲和旧触发通路，导致延迟较高）。
- **总体**：离线与硬件在环实验**数量充足、设计合理**，体内实验虽证明了概念，但受限于初步配置，尚未在最优延迟参数下进行大规模验证，**体内部分充分性稍弱**。

## 6. 主要结论与发现

- **紧凑 SNN 检测有效**：仅 41 神经元、530 参数的 SNN 达到中位 F1=0.56，与更大规模的深度学习模型（1D‑CNN、LSTM）性能相当，且在标准参数下超越经典滤波器。
- **神经形态部署保持性能并显著降耗**：从软件到 SpiNNaker 硬件的迁移带来轻微 F1 下降（≈5–16%），但整体在线检测能力依然保持，功耗降低至 1/20–1/200。
- **闭环延迟低至约 50 ms**：通过直接 Python 控制 Arduino 输出、短缓冲（3 ms）和适当阈值，往返延迟中值 ≈48.5 ms，使**多达 80% 的涟漪可在结束前被刺激**。
- **体内操控有效**：在清醒小鼠中，神经形态触发的光遗传抑制显著降低了长时间涟漪的能量，并产生更高的谱熵、更低的峰值频率等去同步化特征，证明系统能即时调制快速脑动态。
- **可调权衡空间**：缓冲大小和阈值可灵活调整检测灵敏度、精确率与延迟，以适应不同实验需求。

## 7. 优点

- **首次实现**面向快速振荡的完整神经形态闭环在体验证，填补了领域空白。
- **极简模型 + 低功耗硬件**，显著优于传统 CPU/GPU 方案，为可穿戴/可植入边缘接口提供可行路径。
- **系统全面集成**开源 Open Ephys 和 SpiNNaker，降低了技术壁垒，提升了可复现性与可扩展性。
- **细致的系统分析**：量化了软件‑硬件转换损失、缓冲‑阈值‑延迟的定量关系，给出了实用的参数选择指南。
- **错误分析透明**：通过特征分析证明检测模糊源于神经信号本身的内在不确定性，而非模型缺陷，解释合理。

## 8. 不足与局限

- **检测精确率有限**：虽然召回率高，但假阳性率会带来不必要的刺激，需要引入多通道共识、运动状态门控等进一步降低。
- **体内样本量小**：仅 2 只小鼠、12 个会话，且使用未优化的硬件配置（20 ms 缓冲、Open Ephys 插件触发）导致延迟远高于 50 ms，最优延迟配置下的体内效果尚未展示。
- **平台局限**：SpiNNaker 本身并非可植入器件，直接将管线移植到专用 SoC 仍需进一步工作。
- **泛化性待考**：训练和测试数据来源有限，不同实验室、行为状态和标注标准下的性能需额外验证。
- **绝对检测精度不占优**：精细调参的传统检测器（Buzsáki 优化）仍能达到更高 F1，SNN 的核心优势在于**硬件友好、低功耗、可实时部署**，而非精度的彻底超越。
- **软件‑硬件转换仍有损失**：模型翻译后的性能小幅下降有待进一步降低。

（完）
