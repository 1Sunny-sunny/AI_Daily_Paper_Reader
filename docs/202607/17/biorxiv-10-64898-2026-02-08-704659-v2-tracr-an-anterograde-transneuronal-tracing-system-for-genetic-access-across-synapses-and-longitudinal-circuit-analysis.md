---
title: "TRACR: an anterograde transneuronal tracing system for genetic access across synapses and longitudinal circuit analysis"
title_zh: TRACR：一种用于跨突触遗传访问和纵向回路分析的顺行跨神经元示踪系统
authors: "Ibrahimi, M., Gray, M. T., Rochon, P.-L., Eiras, S. M., Lee, J. J., Pietraszkiewicz, P., Dabiri, S., Hicks, J. L., Salter, M. W., Boisvert, M., Paquet, M.-E., Josselyn, S. A., Martemyanov, K. A., Krishnaswamy, A., Wallace, V. A., Lefebvre, J. L."
date: 2026-07-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.08.704659v2.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 跨突触示踪系统揭示神经元如何通过回路连接表示信息
tldr: 现有顺行跨神经元示踪工具受限于细胞毒性和遗传控制不足，TRACR通过合成Notch设计，利用跨突触配体-受体结合诱导报告基因转录，实现对突触后神经元的遗传标记。该系统可分离标记突触前后群体，结合多种功能元件，在完整突触连接下发挥可逆信号，在小鼠视觉系统中成功标记多种突触后靶标，为回路纵向分析提供了AAV递送的新工具。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-08-704659-v2/fig-001.webp\", \"caption\": \"Figure 3. Functional recordings of TRACR-positive cells confirm direction-selective identity. (A) Schematic of TRACR strategy in ChAT-Cre retinas showing Sender-positive Starburst amacrine cells (green), Receiver+ ACs and RGCs (grey), and Reporter labelled DSGCs (RFP, magenta). Recorded RFP+ cells are predicted to show direction-selective responses to preferred direction (black). Mice received AAV intravitreal injections at 3-4 postnatal weeks and harvested at 2 months of age; AAV.TRE-mRuby and Ai63 mice were used for Reporters. (B) Wholemount retina stained with antibodies against RFP, isolectin to label blood vessels, and anti-myc to mark Receiver-labelled retinal neurons. Right: High power image shows a typical field. (C) Fraction of Reporter RFP-positive (RFP+, n = 32 RGCs) and RFP-negative (RFP-, n= 42 RGCs) with ON, OFF, and ON-OFF responses to full field flash stimuli. (D) Two-photon image of alexa488 filled electrode (A488) and RFP+ RGC (top) and its spike responses evoked by a full field flash (bottom). (E) Polar plot of RFP+ RGC firing evoked by a bright bar moving in 8 directions. ON responses evoked by the leading edge of the bars; OFF responses evoked by the trailing edge. Normalized firing vector showing direction selective index (DSI) and angular preference also shown. (F) Average ON and OFF DSIs computed from recordings from RFP+ (n=32 RGCs) and RFPcells (n=42 RGCs), like shown in E. Data show mean ± SEM. p < 0.05, t-test. (G) Polar plot showing angular preference from RFP+ ON-OFF RGCs. Data come from recordings in over 30 retinas from 25 mice. Scale bars: 1mm (B), 20 µm (D).\", \"page\": 43, \"index\": 1, \"width\": 710, \"height\": 486}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-08-704659-v2/fig-002.webp\", \"caption\": \"Figure 5. TRACR activation requires photoreceptor survival. (A) Predicted TRACR activation pattern following photoreceptor degeneration in rd1;Ai63 and MNU-treated Ai63 mice. Mice were infected at P5 with AAV.PhR-Sender and AAV.BP-Receiver (as in\", \"page\": 46, \"index\": 2, \"width\": 948, \"height\": 713}]"
motivation: 现有顺行示踪工具存在细胞毒性且缺乏对连接伙伴的完全遗传控制，急需一种安全、可控的跨突触标记方法。
method: 基于合成Notch系统设计TRACR，通过工程化配体-受体跨突触结合，触发TRE驱动的报告基因转录以标记突触后神经元。
result: 在小鼠视觉系统中，TRACR标记了感觉神经元的长程投射和局部抑制性中间神经元的突触后伙伴，且信号依赖于突触连接完整性，随突触丧失消失、随组装激活。
conclusion: TRACR是一种AAV可递送的顺行跨突触报告工具，适用于从回路组装到退化和修复的纵向分析，突破了现有示踪剂的局限。
---

## 摘要
追踪神经信号汇聚于单个神经元及从中发散的过程，对理解回路功能和疾病相关功能障碍至关重要。现有的顺行跨神经元示踪剂受限于细胞毒性和对连接伙伴不完全的遗传控制。为解决这些局限，我们改造了合成Notch设计，创建了跨突触顺行回路读出系统(TRACR)。工程化配体-受体跨突触结合后，诱导TRE驱动的报告基因转录，从而能够表征突触后神经元。TRACR为突触前和突触后群体提供了分离的遗传访问，并可与标记物、传感器或效应器结合以扩展回路分析。通过在小鼠视觉系统的多个突触中应用TRACR，我们展示了TRACR能标记感觉神经元的突触后伙伴、长程投射和局部抑制性中间神经元。TRACR信号是可逆的，并且在突触缺失或破坏时无法激活。总之，TRACR是一种可及的、AAV可递送的跨神经元报告工具，用于纵向分析回路组装、退化和修复。

亮点：
• TRACR改造了synNotch系统以跨突触传递信号，用于示踪突触后靶点。
• TRACR识别小鼠视觉系统中的局部和长程突触后靶点。
• TRACR的激活需要完整的突触连接而非邻近性。
• TRACR信号是可逆的，在突触丧失时减弱，并在组装后激活。

## Abstract
Following neural signals as they converge onto and diverge from individual neurons is central to understanding circuit function and disease-related dysfunction. Existing anterograde transneuronal tracers are limited by cytotoxicity and incomplete genetic control over connected partners. To address these limitations, we adapted synthetic Notch designs to create TRanssynaptic Anterograde Circuit Readout (TRACR). Binding of the engineered ligand-receptor across synapses induces TRE-driven reporter transcription, enabling characterization of postsynaptic neurons. TRACR provides segregated genetic access to pre- and postsynaptic populations, and can be combined with markers, sensors, or effectors to expand circuit analysis. By applying TRACR at multiple synapses in the mouse visual system, we show that TRACR labels postsynaptic partners of sensory neurons, long-range projections and local inhibitory interneurons. TRACR signaling is reversible and fails to activate when synapses are absent or disrupted. Together, TRACR is an accessible, AAV-deliverable transneuronal reporting tool for longitudinal analysis of circuit assembly, degeneration, and repair.

HIGHLIGHTSO_LITRACR adapts the synNotch system to signal across synapses for tracing postsynaptic targets.
C_LIO_LITRACR identifies local and long-range postsynaptic targets in the mouse visual system.
C_LIO_LITRACR activation requires intact synaptic connectivity rather than proximity.
C_LIO_LITRACR signals are reversible, diminishing upon synapse loss and activating following assembly.
C_LI