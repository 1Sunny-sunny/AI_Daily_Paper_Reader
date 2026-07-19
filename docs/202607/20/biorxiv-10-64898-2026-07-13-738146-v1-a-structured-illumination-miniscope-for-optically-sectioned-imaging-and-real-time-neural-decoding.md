---
title: A structured-illumination miniscope for optically sectioned imaging and real-time neural decoding
title_zh: 一种用于光学层切成像和实时神经解码的结构光照明显微镜
authors: "Lin, H., Wang, S., Zhu, Y., Yin, Z., Guo, Q., Zhou, J."
date: 2026-07-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.13.738146v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 轻量级微型显微镜实现自由活动动物的神经解码
tldr: 单光子微型显微镜在自由行为动物成像中受离焦背景荧光困扰，本文提出一种轻量（<3g）、低成本的结构光照明显微镜，通过Ronchi光栅和时间复用激发实现HiLo光学切片，在保持宽场速度和视野的同时增强对比度与单细胞信号保真度，支持多平面成像并实现实时神经解码的闭环脑机接口，为高对比度钙成像提供实用方案。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738146-v1/fig-003.webp\", \"caption\": \"Figure 1. Design and performance of the HiLo miniscope. (A) Cross-sectional schematic of the HiLo miniscope. (B) Dimensions of the HiLo miniscope. (C) Time-division multiplexing scheme used to acquire uniformly illuminated and structured illumination images. The total acquisition frame rate is 30 frames per second. (D) Uniformly illuminated image and corresponding structured illumination image of a thin, uniform fluorescent plane. The Ronchi grating has a spatial period of approximately 28 𝜇m at the sample plane. (E) Uniformly illuminated image of a USAF 1951 resolution target. Inset shows a magnified view of the highlighted region; the finest resolvable feature corresponds to 256 lp/mm (Group 8, Element 1). (F) Comparison of uniformly illuminated widefield imaging and optical-sectioned HiLo miniscope imaging in a Thy1-GFP mouse brain slice. Intensity profiles along the blue and magenta line cuts illustrate the reduction of background fluorescence and the enhancement of image contrast achieved by the HiLo miniscope.\", \"page\": 3, \"index\": 3, \"width\": 1057, \"height\": 321}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738146-v1/fig-004.webp\", \"caption\": \"Figure 2. HiLo imaging improves signal fidelity and ROI-based calcium signal quality. (A) Schematic of simulated data generation. Each synthetic widefield frame was constructed as a weighted sum of three components: an in-focus neural activity signal (\\\"true signal\\\"), a spatially localized out-of-focus background (\\\"local background\\\"), and a global background signal (\\\"global background\\\"). (B) HiLo reconstruction of the simulated widefield image shown in (A). (C) Example fluorescence traces extracted from the simulated ROI indicated in (A) and (B). (D) Quantitative comparison of signal fidelity in simulations. Scatter plot shows the correlation coefficient between extracted signals and ground-truth activity for widefield imaging versus HiLo imaging. Each dot represents one simulated ROI; the green dot indicates the example ROI shown in (C). (E) In vivo calcium imaging from hippocampal CA1 in freely moving mice. Rows show raw widefield images, raw HiLo images, and CNMF-E-denoised signals. Left, maximum-intensity projections (MIPs) over 1000 frames; middle, representative single frames with example ROIs outlined; right, representative fluorescence traces from the same color-coded ROIs. (F) Comparison of mean Δ𝐹∕𝐹 between widefield and HiLo ROI signals across all ROIs (𝑛 = 1,513 ROIs from 5 mice). Each point represents one ROI. (G) Signal-to-noise ratio comparison across extraction methods, including ROI pixel-averaged signals from widefield and HiLo images and CNMF-E–extracted signals from widefield and HiLo data. Colored dots represent individual ROIs; white dots indicate medians; lines connect session-averaged values from individual mice. (H) Similarity between ROI-based and CNMF-E–extracted signals. Scatter plot shows the correlation between ROI-derived fluorescence traces from widefield or HiLo images and denoised CNMF-E fluorescence traces extracted from the corresponding widefield dataset. Black dots represent individual ROIs, and colored dots indicate session means. Statistical significance in (G and H) was assessed using paired 𝑡-tests on mouse-level mean values (𝑛 = 5 mice; *𝑝 < 0.05, ***𝑝 < 0.001; n.s., not significant).\", \"page\": 4, \"index\": 4, \"width\": 1046, \"height\": 1015}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738146-v1/fig-001.webp\", \"caption\": \"Figure 3. Optical-sectioned multi-plane imaging increases the yield of imaged neurons. (A) Color-coded composite image sampled from a Thy1-GFP mouse brain slice across multiple focal depths, illustrating volumetric coverage enabled by optical-sectioned HiLo imaging. Color indicates relative imaging depth. Scale bar, 100 𝜇m. (B) Schematic and representative maximum-intensity projection (MIP) images illustrating in vivo two-plane imaging. Example fluorescence images acquired at depths of 179 𝜇m and 212 𝜇m are shown, together with detected neurons color-coded by imaging plane and overlap (magenta, 212 𝜇m; green, 179 𝜇m; white, neurons detected in both planes). (C) Representative calcium activity traces (Δ𝐹∕𝐹 ) from neurons detected exclusively in the deeper plane (212 𝜇m), exclusively in the shallower plane (179 𝜇m), and in both planes (overlap), demonstrating reliable signal extraction across imaging depths. (D) Percentage of neurons detected in both imaging planes relative to the total number of neurons identified across planes. (E) Comparison of mean signal-to-noise ratio (SNR) between neurons detected in the deeper and shallower imaging planes. (F) Number of neurons detected in the deeper plane, the shallower plane, and after combining neurons from both planes. In (D)–(F), each dot represents one imaging session. In (E) and (F), paired lines indicate within-session comparisons. Boxes represent the median and interquartile range, and whiskers indicate the minimum and maximum values. Statistical significance was assessed using paired 𝑡-tests (𝑛 = 6mice; *𝑝 < 0.05, **𝑝 < 0.01, ***𝑝 < 0.001).\", \"page\": 6, \"index\": 1, \"width\": 1045, \"height\": 619}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738146-v1/fig-002.webp\", \"caption\": \"Figure 4. HiLo imaging enhances ROI-based spatial readout from hippocampal CA1. (A) Representative matched ROI from dorsal hippocampal CA1. Left: animal trajectory (gray) overlaid with calcium event locations (red); only events exceeding 3 standard deviations of Δ𝐹∕𝐹 are shown. Right: corresponding spatial tuning map, computed with 2.5 × 2.5 cm spatial bins and smoothed with a Gaussian kernel (𝜎 = 3.5 cm). (B) Cumulative distributions of spatial information for individually extracted ROI pixel-averaged signals from widefield and HiLo images. (C) Comparison of spatial information for matched ROIs identified in both widefield and HiLo images; each dot represents one ROI. (D) Summary of mean spatial information for matched ROIs across imaging modalities. (E)–(G) Same analyses as in (B)–(D), performed on signals extracted using the CNMF-E algorithm. (H) Bayesian decoding of animal position using ROI pixel-averaged signals from widefield and HiLo images. Actual trajectories are shown in black, and decoded positions are overlaid as colored dots for each imaging modality. (I) Decoding performance quantified as median decoding error. (J) Same decoding analyses as in (H) using CNMF-E–extracted signals. In (D), (G), and (I), paired lines indicate within-session comparisons; boxes show median and interquartile range; whiskers indicate extreme values; statistical significance was assessed using paired 𝑡-tests (𝑛 = 5mice; *𝑝 < 0.05, **𝑝 < 0.01, ****𝑝 < 0.0001; n.s., not significant).\", \"page\": 7, \"index\": 2, \"width\": 1057, \"height\": 745}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738146-v1/fig-005.webp\", \"caption\": \"Figure 5. Closed-loop hippocampal BMI training. (A) Experimental setup for a closed-loop BMI paradigm. The real-time decoding algorithm compares ongoing population vector activity to a pre-established odor-evoked template. If the correlation exceeds a threshold, a reward is triggered. Training consists of acquisition, extinction, and reacquisition phases, with rewards delivered during acquisition and reacquisition but not extinction. (B) Example session of real-time correlation of population vector activity with the template during training. Red dashed line represents correlation threshold. Vertical blue lines are reward delivery and gray bars are licks. (C) Threshold-crossing events (% of total) across the acquisition process. Gray lines indicate individual animals, with the bolded gray line showing the example mouse in (B), (E)–(H); green line shows the population average. Correlation between acquisition progress and threshold-crossing events is tested using Spearman correlation. (D) Frequency of crossing events per minute during the acquisition, extinction, and reacquisition phases. Bolded gray line corresponds to the example mouse. Paired lines indicate within-session comparisons; boxes show median and interquartile range; whiskers indicate extreme values. (E) Example behavioral session showing lick rasters aligned to threshold-crossing events (dashed line); shaded regions indicate training blocks. (F) Lick rate as a function of time relative to threshold-crossing events for the example session. (G) Lick rate preceding threshold-crossing events (−2 to −1 s), corrected by subtracting baseline lick rate (−4 to −3 s), across acquisition, extinction, and reacquisition blocks for the same session. Statistical significance was assessed using rank sum test (*𝑝 < 0.05, **𝑝 < 0.01; n.s., not significant). (H) Baseline (−6 to −3 s) and peri-crossing (−1 to 2 s) lick rates during extinction. Statistical significance was assessed using a paired 𝑡-test (𝑛 = 32 crossing events; ****𝑝 < 0.0001). In (G) and (H), colored dots represent individual crossing events; white dots indicate medians.\", \"page\": 9, \"index\": 5, \"width\": 1058, \"height\": 684}]"
motivation: 解决单光子微型显微镜的背景荧光问题，避免多光子方法的高成本和复杂性。
method: 采用Ronchi光栅和时间复用激发的结构光照明实现HiLo光学切片成像。
result: 显著抑制背景荧光，提升ROI信号质量，使简单平均信号接近离线算法提取性能，并实现实时神经解码。
conclusion: 结构照明是一种实用易行的策略，可增强微型显微镜成像对比度和神经信号读出。
---

## 摘要
单光子微型显微镜能够对自由活动动物进行大规模钙成像，但离焦背景荧光会降低图像对比度和单细胞信号保真度。多光子方法可解决这一局限，但成本高昂且结构复杂。在此，我们介绍一种轻量（<3克）、低成本的结构光照明显微镜，可在自由活动小鼠中实现光学层切。该系统采用简单的朗奇光栅和时间复用激发实现HiLo成像，在保持宽场微型显微镜的速度、视场和易用性的同时，强烈抑制背景荧光，并支持光学层切多平面成像以增加神经元采集量。利用海马体记录，我们展示了基于感兴趣区域（ROI）的信号质量和空间信息读取的增强，使简单的ROI平均信号能够接近离线算法提取信号的性能。我们进一步展示了由快速在线信号提取和实时神经解码实现的原理验证闭环脑机接口。总之，这些结果确立了结构光照明作为一种实用且易于实现的策略，用于通过微型化显微镜实现高对比度钙成像。

## Abstract
Single-photon miniscopes enable large-scale calcium imaging in freely behaving animals but are limited by out-of-focus background fluorescence that degrades image contrast and single-cell signal fidelity. Multiphoton approaches address this limitation but remain costly and complex. Here we introduce a lightweight (<3 g), low-cost structured illumination miniscope that achieves optical sectioning in freely behaving mice. Using HiLo imaging implemented with a simple Ronchi grating and time-multiplexed excitation, the system strongly suppresses background fluorescence while preserving the speed, field of view, and accessibility of widefield miniscopes, and supports optical-sectioned multi-plane imaging to increase neuronal yield. Using hippocampal recordings, we show enhanced region-of-interest (ROI)-based signal quality and spatial information readout, allowing simple ROI-averaged signals to approach the performance of offline algorithm-extracted signals. We further demonstrate a proof-of-principle closed-loop brain--machine interface enabled by rapid online signal extraction and real-time neural decoding. Together, these results establish structured illumination as a practical and accessible strategy for achieving high-contrast calcium imaging with miniaturized microscopes.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

*   **研究动机**：单光子宽场微型显微镜是自由活动动物神经活动群体成像的流行工具，但存在固有缺陷——缺乏光学层切能力，导致严重的离焦背景荧光。这会降低图像对比度，损害单细胞信号的保真度。
*   **现有解决途径的局限**：多光子显微镜可从源头提供光学层切，但成本高昂、系统复杂、技术门槛高，限制了其广泛应用。离线计算去混叠方法（如 CNMF-E）虽能部分缓解问题，但处理滞后，难以满足实时神经解码和闭环实验的需求。
*   **核心问题**：如何在不牺牲单光子微型显微镜的简易性、便携性和低成本优势的前提下，在成像采集阶段就实现对背景荧光的光学抑制，从而提升信号质量和实时应用潜力。
*   **整体含义**：本文提出一种新型结构光照明微型显微镜，作为连接传统宽场和多光子系统的补充方案，旨在以最低的硬件复杂度实现“采集端”的光学层切成像，为高对比度群体神经活动记录和实时闭环神经调控提供一个实用且易于推广的解决方案。

### 2. 论文提出的方法论

*   **核心思想**：采用 **HiLo 显微术** 原理，通过将均匀照明（Widefield）和结构光照明（Structured Illumination）下获取的两幅图像进行融合计算，重构出具有光学层切效果的图像，从而在剔除离焦背景信号的同时，保留焦面内的高频和低频细节。
*   **关键技术细节**：
    *   **硬件设计**：微型显微镜（<3g）内置 **Ronchi 光栅**，置于一路 LED 激发光路中产生正弦条纹图案。通过 **时间复用** 方式，交替点亮无光栅和有光栅的两路 LED，用 CMOS 相机分别采集 **均匀照明图像 $U(\vec{\rho})$** 和 **结构光照明图像 $S(\vec{\rho})$**。
    *   **系统集成**：集成了 **电润湿液体透镜**，通过电压控制实现快速、无机械运动的轴向焦点调制，支持多平面成像。
*   **算法流程**（HiLo重构）：
    1.  **获取高频焦内信号**：由于离焦信号 $I_{\text{out}}(\vec{\rho})$ 主要包含低频信息，对均匀照明图像 $U(\vec{\rho})$ 进行高通滤波（HP），即可直接提取焦内信号的高频分量： $HP[I_{\text{in}}(\vec{\rho})] \approx HP[U(\vec{\rho})]$。
    2.  **获取低频焦内信号**：构建一个差分图像 $D(\vec{\rho}) = |HP[U(\vec{\rho}) - 2S(\vec{\rho})]|$。该图像本质上是焦内信号 $I_{\text{in}}(\vec{\rho})$ 受到正弦调制的结果。对该图像进行低通滤波（LP），即可恢复焦内信号的低频分量： $LP[I_{\text{in}}(\vec{\rho})] \approx \frac{\pi}{2M} LP[D(\vec{\rho})]$，其中 $M$ 为调制对比度。
    3.  **合成光学切片图像**：将高低频分量加权求和，得到最终的无背景、焦内图像： $I_{\text{HiLo}}(\vec{\rho}) = HP[U(\vec{\rho})] + \eta LP[D(\vec{\rho})]$，其中 $\eta$ 为融合系数。

### 3. 实验设计

*   **数据集与场景**：
    *   **仿真数据**：人为合成包含焦内信号、局部离焦背景和全局背景的模拟图像，用于定量评估 HiLo 算法对已知“真值”神经活动的恢复保真度。
    *   **离体验证**：在 **Thy1-GFP 转基因小鼠的脑片** 上成像，直观展示 HiLo 显微镜对比宽场成像的背景抑制和对比度增强效果。
    *   **活体动物成像**：在自由活动的 **Thy1-GCaMP6f 小鼠** 上，通过植入 GRIN透镜，对 **海马 CA1 区** 神经元进行大规模钙信号记录。
        *   **静息/自由探索**：比较宽场与 HiLo 图像的信号质量和 ROI 信号信噪比（SNR）。
        *   **开放旷场任务**：检验 HiLo 成像对海马位置细胞空间信息读取和动物轨迹解码能力的提升。
    *   **闭环脑机接口**：在 **头部固定的小鼠** 上进行闭环训练，利用 HiLo 实时提取的神经群体活动信号解码状态，控制奖赏。
*   **Benchmark 与对比方法**：
    *   **主要对比基准**：同一系统采集的 **时间匹配的宽场（Widefield）图像**。
    *   **信号提取对比**：对比 **简单 ROI 像素平均信号** 与 **离线 CNMF-E 算法提取信号** 的质量。
    *   **分析维度**：信号信噪比（SNR）、空间信息含量、贝叶斯解码误差等行为学指标。

### 4. 资源与算力

*   论文全文未明确提及进行数据处理、模型训练或闭环解码时所使用的具体硬件算力信息（如 GPU 型号、数量、训练时长）。对于闭环 BMI 实现，文中仅说明其通过 Suite2p 进行快速 ROI 识别，并利用自定义 LabVIEW 脚本与 DAQ 系统进行数据采集和实时控制，但未详述实时计算的算力平台。

### 5. 实验数量与充分性

*   **实验规模**：
    *   **仿真实验**：生成含多个模拟 ROI 的数据，并与真实海马成像数据动态结合。
    *   **活体成像**：使用了 7 只 Thy1-GCaMP6f 小鼠和 1 只 Thy1-GFP 小鼠。
    *   **ROI 分析**：比较了来自 5 只小鼠的 **1513个 ROI** 的信号质量。
    *   **空间信息与解码**：分析了 5 只小鼠的 **965个神经元** 的空间信息。
    *   **多平面成像**：在 6 只小鼠上进行了体内双平面成像验证。
    *   **闭环脑机接口**：在 6 只小鼠上进行了原理论证，至少 1 只表现出与任务相关的连贯舔舐行为。
*   **充分性与客观性评价**：
    *   **充分性**：实验设计层层递进，从仿真、离体到多种活体任务范式，并比较了不同信号提取方法下的多维度指标，论证较为全面。
    *   **客观公平性**：对比公平，如使用相同的 ROI 空间足迹提取不同模态下的信号，并对活动水平等混杂因素进行了控制分析（如匹配事件率的空间信息比较）。闭环 BMI 实验证明系统可用于实时应用，但作为原理验证，其行为学结果（如仅 1 只动物表现出明显学习行为）尚属初步。

### 6. 论文的主要结论与发现

*   **硬件实现可行**：成功构建了一个轻量（<3g）、低成本的 HiLo 微型显微镜，可在自由活动小鼠上实现光学层切成像。
*   **信号质量显著提升**：HiLo 成像能有效抑制背景荧光，大幅提升 **ROI 像素平均信号** 的信噪比（SNR），使其质量接近计算量更大的离线 CNMF-E 算法提取的信号。与宽场 ROI 信号相比，HiLo ROI 信号与去噪后的 CNMF-E 信号的相似度更高。
*   **增强行为信息读取**：HiLo 提升了海马位置细胞的空间信息含量，使用 HiLo 的 ROI 信号进行贝叶斯解码的误差显著低于使用宽场 ROI 信号，解码性能接近了使用 CNMF-E 信号的性能。
*   **支持多平面与实时应用**：集成的电润湿透镜结合光学层切能力，可进行多平面成像，增加神经元产出。该系统成功应用于原理验证性的闭环脑机接口，证明了其进行快速在线信号提取和实时神经解码的潜力。

### 7. 优点

*   **实用性极强**：在保持单光子微型显微镜低成本、轻重量、易用等核心优势的基础上，仅在激发光路中增加简易 Ronchi 光栅等少量硬件，便实现了采集端的光学层切，是现有系统的理想补充方案。
*   **提升在线分析性能**：显著改善最简单、最快速的 ROI 平均信号的信号质量，使其性能逼近复杂的离线分析，这对需要低延迟的实时神经解码和闭环调控至关重要。
*   **功能扩展性**：设计中集成了电润湿液体透镜，在不显著增加系统复杂度的情况下实现了光学切片的多平面成像，增加了单次实验的神经元记录量。
*   **比较分析严谨**：实验设计考虑周全，不仅直接对比了宽场和 HiLo，还对比了简单 ROI 信号和 CNMF-E 信号，并通过控制神经活动率等分析方法，明确了 HiLo 增益的来源和范围，客观评价了其与计算方法的互补关系。

### 8. 不足与局限

*   **成像深度与散射限制**：作为单光子技术，其光学层切和成像深度潜力仍远不如多光子（双光子、三光子）显微镜，不适用于深层或高散射组织的高信噪比成像。
*   **无法分离重叠细胞**：HiLo 在成像层面清除了非焦面背景，但无法像计算去混叠方法（如 CNMF-E）那样分离焦平面内空间上重叠的神经元信号，因此在神经元密度极高的区域，后处理算法仍有必要。
*   **多平面成像速度**：体内多平面成像的帧率相对较低（2-plane 为 2.5 Hz），是由于液体透镜响应和为避免串扰而丢弃部分帧所导致的，这使其目前更适用于对时间分辨率要求不苛刻的实验。
*   **闭环 BMI 证据初步**：闭环脑机接口的实验结果主要作为系统实时性能的原理验证，行为学（舔舐行为）仅在部分动物中表现得显著，其训练效果和神经机制的解析尚不充分。
*   **环境光照敏感**：系统设计未提及对动物行为学环境中常见光源（如红外摄像头、屏幕光）的抗干扰措施，这在实际开放场实验中可能是潜在的噪声源。

（完）
