---
title: Design of a Low-Latency sEMG Real-Time Correction System Based on High CMRR and EMRMS Mathematical Modeling
title_zh: 基于高CMRR与EMRMS数学模型的低延迟sEMG实时校正系统设计
authors: "Lo, H. U., Gao, Z., Loi, H. F., Cheng, S. K."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.724714v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 用于假肢控制的低延迟表面肌电校正系统
tldr: "针对sEMG中电力线干扰和数字延迟问题，设计了一种模拟-数字协同校正系统，融合高CMRR前端、指数窗口RMS包络估计与递归单音干扰消除。建立了电极-皮肤失衡的CMRR模型，并分析LMS稳定性。EMRMS算法将复杂度降至O(1)，实现确定性实时处理，适配无浮点单元微控制器。在Ninapro DB2上验证，SNR平均提升13.9 dB，包络误差70 μV，端到端延迟约30 ms，CPU占用仅1.6%，形态相关性0.993，算法开源。"
source: biorxiv
selection_source: fresh_fetch
motivation: sEMG信号易受电力线干扰且传统数字处理延迟高，限制了假肢和外骨骼的实时控制应用。
method: 提出基于高CMRR前端与EMRMS包络模型的自适应数字校正系统，结合递归单音消除器降低延迟和计算开销。
result: "在Ninapro DB2数据集上实现平均13.9 dB SNR提升、70 μV包络误差，延迟仅30 ms且CPU占用1.6%，形态保真度达0.993。"
conclusion: 该低延迟系统以极少计算资源有效抑制干扰，保持信号形态，为嵌入式实时肌电控制提供了高效且开源的解决方案。
---

## 摘要
表面肌电(sEMG)是肌电假肢、外骨骼和康复系统最实用的非侵入接口，但电力线干扰(PLI)污染和过度的数字流水线群延迟仍限制其临床采用。本文提出了一种协同设计的模拟-数字校正系统，该系统结合了高CMRR前端、指数窗均方根(EMRMS)包络估计器和递归单音PLI消除器。我们提出了一个捕捉电极-皮肤不平衡的闭式CMRR模型，并提供了LMS消除器的完整稳定性分析。EMRMS估计器将时间和空间复杂度从O(L)严格降低到O(1)。该算法无数据依赖分支，实现了确定性的算法执行时间（RTOS环境下零抖动），并原生兼容缺乏硬件浮点单元(FPU)的微控制器上的定点运算。参考实现达到每样本中位延迟8.2 μs，端到端延迟约30 ms，为机电驱动留下了充裕的>90 ms预算，同时仅需1.6%的CPU工作周期，可实现长时间深度睡眠。在公共Ninapro DB2数据集上的验证表明，相比长度为200的矩形参考，平均信噪比提升13.9 dB（12通道平均；单通道比较：9.7 dB，表3），包络RMSE为70.0 μV。配对Wilcoxon符号秩检验确认了相对于静态基线的统计显著性(p < 0.001)，Pearson相关性分析(ρ = 0.993 ± 0.0002)证实了严格的形态保真度。完整的开源代码库和基准测试已公开发布。

O_TBL 查看此表:
org.highwire.dtl.DTLVardef@113eac0org.highwire.dtl.DTLVardef@9910f0org.highwire.dtl.DTLVardef@1271269org.highwire.dtl.DTLVardef@29bf93org.highwire.dtl.DTLVardef@e08880_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNO表3:C_FLOATNO O_TABLECAPTION在Ninapro类似合成sEMG（单通道）的60 s公共片段上的定量比较，包含一个3 mV 50.3 Hz的主音，该主音略微偏离了静态陷波器设计中心50.0 Hz，在频率失配下对自适应校正器进行压力测试。第3.4节报告的Ninapro多通道聚合(13.9 dB)使用恰好50 Hz（匹配陷波）的主电源，因此获得了更高的Δ SNR。"MAC/样本"不包含EMRMS平方根和预先计算的LMS正弦/余弦。

C_TABLECAPTION C_TBL

## Abstract
Surface electromyography (sEMG) is the most practical non-invasive interface for myoelectric prostheses, exoskeletons, and rehabilitation systems, but power-line interference (PLI) contamination and excessive digital pipeline group delay still limit its clinical adoption. This paper proposes a co-designed analog-digital correction system combining a high-CMRR front-end with an exponentially-windowed RMS (EMRMS) envelope estimator and a recursive single-tone PLI canceller. We present a closed-form CMRR model capturing the electrode-skin imbalance, and provide a complete stability analysis of the LMS canceller. The EMRMS estimator reduces the computational overhead from[O] (L) to strictly[O] (1) in both time and space complexities. Featuring no data-dependent branching, the algorithm achieves deterministic algorithmic execution time (zero jitter under an RTOS environment) and is natively compatible with fixed-point arithmetic on microcontrollers lacking a hardware Floating-Point Unit (FPU). A reference implementation reaches an 8.2 {micro}s median per-sample latency, yielding an end-to-end delay of[~] 30 ms -- leaving a generous >90 ms budget for electromechanical actuation -- while requiring an active CPU duty cycle of merely 1.6%, enabling prolonged deep-sleep intervals. Validation on the public Ninapro DB2 dataset demonstrates a 13.9 dB mean SNR improvement (averaged across 12 channels; single-channel comparison: 9.7 dB, Table 3) and a 70.0 {micro}V envelope RMSE against a length-200 rectangular reference. Paired Wilcoxon signed-rank tests confirm statistical significance (p < 0.001) over static baselines, and Pearson correlation analysis ({rho} = 0.993 {+/-} 0.0002) confirms strict morphological fidelity. The full open-source codebase and benchmarks are publicly released.

O_TBL View this table:
org.highwire.dtl.DTLVardef@113eac0org.highwire.dtl.DTLVardef@9910f0org.highwire.dtl.DTLVardef@1271269org.highwire.dtl.DTLVardef@29bf93org.highwire.dtl.DTLVardef@e08880_HPS_FORMAT_FIGEXP  M_TBL O_FLOATNOTable 3:C_FLOATNO O_TABLECAPTIONQuantitative comparison on a common 60 s segment of Ninapro-like synthetic sEMG (single channel) with a 3 mV 50.3 Hz mains tone  slightly drifted from the static notchs design centre at 50.0 Hz, stress-testing the adaptive corrector under a frequency mismatch. The Ninapro multi-channel aggregate (13.9 dB) reported in Section 3.4 uses mains exactly at 50 Hz (matched notch) and so achieves a higher {Delta} SNR. "MAC/sample" excludes the EMRMS square root and the pre-computed LMS sine/cosine.

C_TABLECAPTION C_TBL

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **背景与动机**：表面肌电信号（sEMG）是肌电假肢、外骨骼及人机接口的主流非侵入式输入模态。然而，其实际部署面临两大核心挑战：
    - **电力线干扰（PLI）污染**：50/60 Hz 工频干扰在共模幅度可达数伏，而肌电信号仅为毫伏级，要求模拟前端提供超过 100 dB 的共模抑制比（CMRR）。
    - **数字流水线群延迟过高**：传统矩形窗 RMS 包络提取等环节引入显著延迟，超过约 125 ms 即被用户感知为系统迟钝，严重影响控制实时性。
- **研究意义**：现有研究往往只侧重其中一轴，或在低延迟实现上依赖 FPGA、深度学习加速器等重型硬件。本文旨在构建一个统一的、软硬件协同设计的低延迟校正系统，使其能在通用微控制器上同时满足高 CMRR 与低延迟的需求，推动低成本可穿戴设备走向临床实用。

## 2. 论文提出的方法论

系统采用“模拟前端 + 数字流水线”的串行架构，核心创新包括三点。

- **高 CMRR 闭式数学模型**
    - 将有效 CMRR 建模为三个误差源的级联：（i）仪表放大器（INA）的固有 CMRR $(\text{CMRR}_{\text{INA}})$；（ii）电极-皮肤阻抗失配 $\Delta Z$ 造成的分压效应，其决定被动上限 $\text{CMRR}_{\text{div}} = 20\log_{10}(Z_{in}/\Delta Z)$；（iii）右腿驱动（DRL）反馈环路的开环增益 $A_{\text{DRL}}$。
    - 总有效 CMRR 由下式给出：
        $$\text{CMRR}_{\text{eff}} = \min(\text{CMRR}_{\text{INA}}, \text{CMRR}_{\text{div}}) + A_{\text{DRL}}$$
    - 该模型可量化电极状态（湿/干）与 DRL 增益对最终抗干扰能力的影响，用于指导参数选取。

- **指数窗均方根（EMRMS）包络估计器**
    - 用一阶 IIR 递归替代传统的 $L$ 点矩形窗 RMS：
        $$P[n] = (1-\alpha)P[n-1] + \alpha x[n]^2,\quad y[n] = \sqrt{P[n]}$$
    - 平滑因子 $\alpha = 1 - \exp(-1/(\tau f_s))$，其中 $\tau$ 为时间常数，亦为等效群延迟。
    - **复杂度与实时性优势**：将时间和空间复杂度从 $\mathcal{O}(L)$ 降至严格的 $\mathcal{O}(1)$，仅需两次乘累加和一次开方，无数据依赖分支，可实现确定性的执行时间，原生兼容定点运算。

- **自适应单音 PLI 消除器**
    - 使用一个单频点（$\omega=2\pi f_{\text{PLI}}/f_s$）的 LMS 自适应滤波器来跟踪残余 PLI 的幅度和相位：
        $$e[n] = x[n] - \hat{A}[n]\cos(\omega n) - \hat{B}[n]\sin(\omega n)$$
        $$\hat{A}[n+1] = \hat{A}[n] + \mu e[n]\cos(\omega n)$$
        $$\hat{B}[n+1] = \hat{B}[n] + \mu e[n]\sin(\omega n)$$
    - 论文给出了完整的收敛性分析。收敛条件为 $0<\mu<4$，选定步长 $\mu=10^{-3}$，在 $f_s=2\text{ kHz}$ 下收敛时间常数 $\tau_{\text{LMS}}=2/\mu = 1\text{ s}$，稳态失调 $M = \mu/2 \approx 0.05\%$，在速度与精度间取得平衡。

## 3. 实验设计

- **合成信号与延迟基准**：
    - 生成 30 秒含高斯脉冲的合成 sEMG 信号，叠加 3 mV/50 Hz PLI 和 0.1 mV 慢漂移。在通用四核笔记本 CPU 上运行流水线，测量每样本延迟，观察包络提取质量（图 2、3、5）。
- **公共数据集验证**：
    - **数据集**：Ninapro DB2，使用受试者 1 的练习 B（手部基本动作），包含 12 通道、$f_s=2\text{ kHz}$ 的 sEMG 记录。为可重复验证，人为叠加 3 mV 的 50 Hz 主音及其二次谐波。
    - **基准对比**：将所提议流水线与以下方案对比：
        - 静态陷波 + 矩形窗 RMS（$L=200$）
        - 静态陷波 + EMRMS（无自适应消除）
        - 文献中的 FPGA 实现（Belkhiria et al.）和微控制器系统（Gao et al.）
    - **评价指标**：信噪比改善（$\Delta \text{SNR}$）、包络均方根误差（RMSE）、皮尔逊相关系数 $\rho$（评估形态保真度），以及配对 Wilcoxon 符号秩检验的统计显著性。
- **参数灵敏度与鲁棒性分析**：
    - 扫描 CMRR 随 $\Delta Z$ 和 DRL 增益的变化（图 1）。
    - LMS 步长 $\mu$ 从 $10^{-4}$ 到 $10^{-1}$ 进行扫描（图 8a–b）。
    - 固定校正器频率，测试主电源频率以 $0.1/0.2/0.5\text{ Hz/s}$ 线性漂移时的追踪性能（图 8c–d）。

## 4. 资源与算力

- 论文并未提及使用 GPU 或进行任何神经网络训练。
- 所有信号处理算法和流水线均以 Python 实现，在“通用 4 核笔记本 CPU”上进行延迟基准测试，但未给出具体 CPU 型号。
- 算法计算量极低：中位执行时间 $8.2\ \mu\text{s}$/样本，对应 $2\text{ kHz}$ 采样率下的 CPU 工作周期仅为 $1.6\%$，为深度睡眠模式留出大量空闲。全部管线仅需约 11 次乘加运算和 1 次开方，内存占用约 13 个状态字。
- 论文提出未来计划移植到 STM32F4 微控制器，并预估在该平台上每样本延迟 $\le 40\ \mu\text{s}$。

## 5. 实验数量与充分性

- **实验覆盖**：包含合成信号测试、CMRR 参数扫描、自适应算法步长与漂移响应、公共数据集（1 个受试者，12 通道）上的多指标定量评估。设计较为全面，验证了模型的预测能力、算法的静态与动态性能。
- **对比公平性**：在 Ninapro 验证中，与不采用自适应消除的静态陷波 + 矩形/指数 RMS 方案直接对比，量化了每一步的增益（表 3）。同时引用文献中异构平台（FPGA、MCU）的实现作为外部参考。
- **局限性**：数据集验证仅局限于 Ninapro DB2 的单一受试者（subject 1），虽符合算法概念验证的惯例，但结果的普适性有待多受试者、多运动模式检验。文中已明确指出此局限，并列为未来工作。总体而言，实验设计严谨，定量评估透明，且开源了代码以保证可复现性。

## 6. 论文的主要结论与发现

- **统一框架有效性**：通过协同设计模拟 CMRR 模型与数字低延迟处理，可为低成本嵌入式平台同时提供高抗噪能力和满足实时控制需求的短延迟。
- **性能量化**：
    - 在 $40\text{ dB}$ DRL 增益下，干电极条件也能将有效 CMRR 维持在 $120\text{ dB}$ 以上。
    - EMRMS 以 $\mathcal{O}(1)$ 开销提供了与 $L=200$ 矩形窗相当的平滑度，但群延迟仅为其约 $1/5$（$25\text{ ms}$ vs $125\text{ ms}$ 级）。
    - 自适应消除器在主频匹配时能额外提供约 $50\text{ dB}$ 的 PLI 抑制。
    - 在 Ninapro DB2 上，全流水线实现 $13.9\text{ dB}$ 平均信噪比提升，包络 RMSE 为 $70.0\ \mu\text{V}$，形态相关性 $\rho=0.993$，端到端延迟约 $30\text{ ms}$，CPU 工作周期仅 $1.6\%$。

## 7. 优点

- **理论-实践闭环**：为模拟 CMRR 和数字自适应滤波均提供了闭式或收敛性分析，为参数选择提供了理论依据，而非经验调试。
- **极致的计算效率**：EMRMS 实现了严格 $\mathcal{O}(1)$ 复杂度、确定性执行时间，无需硬件 FPU，极大降低了对嵌入式硬件的门槛。
- **系统级低延迟**：端到端约 $30\text{ ms}$ 的延迟远优于 $125\text{ ms}$ 感知阈值，且留给机电驱动和分类器充足预算。
- **高保真度与鲁棒性**：在有效去噪的同时，皮尔逊系数证实包络形态几乎无损，利于下游分类或控制任务。
- **可复现性与开放性**：提供开源代码、单元测试和基准，并在公共数据集上进行验证。

## 8. 不足与局限

- **单通道处理**：当前的自适应消除和包络估计均为逐通道独立进行，未利用多通道间的共模成分做空间滤波，可能留下性能提升空间。
- **频率漂移鲁棒性**：LMS 消除器假定工频固定。实验表明当主电源频率漂移速率超过 $0.1\text{ Hz/s}$ 时，残余噪声迅速升至毫伏级。文中将此作为重要局限并提出应引入锁相环。
- **运动伪迹假设**：系统假定宽带运动伪迹已由模拟高通环节充分衰减，未考虑剧烈运动导致电极-皮肤相对位移时的基线漂移问题。
- **实验覆盖有限**：Ninapro 验证仅用了单一受试者的数据，延迟基准在非实时操作系统上测得，未完全反映嵌入式 RTOS 环境下的实际抖动和行为。
- **硬件验证缺失**：CMRR 模型和嵌入式移植仍属于计划工作，当前缺乏物理硬件实测数据的直接支撑。

（完）
