---
title: "APpar: automated action potential parameter analysis software for reproducible electrophysiological measurements in neurons"
title_zh: APpar：用于神经元中可重复电生理测量的自动化动作电位参数分析软件
authors: "Vasylyev, D. V., Waxman, S. G."
date: 2026-06-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.10.731446v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 自动从神经记录中提取动作电位参数
tldr: APpar是一款免费开源的神经元动作电位参数自动分析软件，基于OriginLab环境，通过导数阈值检测动作电位并计算静息膜电位、阈值、幅度、时长等全面兴奋性参数。其核心创新是TRUE-threshold验证算法，从波峰回溯至最近局部导数最大值再至阈值点重算参数，减少人为误差，提升可重复性。软件在背根神经节神经元重复及自发放电记录中验证，提供透明、可定制的分析框架，助力神经电生理研究。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统动作电位分析多依赖手动或专有软件，可重复性、透明度和通量受限，亟需自动化、标准化的开源工具。
method: 在OriginLab中开发APpar，通过用户定义导数阈值自动检测动作电位，并采用TRUE-threshold算法验证阈值点以重算参数，涵盖全面波形指标。
result: APpar对背根神经节神经元的相同波形、重复放电和自发放电均给出稳定测量，能提取动态参数变化，经实验验证有效。
conclusion: APpar为神经电生理提供了可重复、可定制的动作电位分析方案，其阈值验证算法提高了阈值检测的可靠性，具有广泛应用前景。
---

## 摘要
对动作电位(AP)波形的定量分析是神经元兴奋性、离子通道功能、疾病机制和药理调节研究的核心。然而，AP分析通常仍采用部分手动工作流程、实验室专用电子表格或专有软件环境，这可能限制可重复性、透明度和通量。本文介绍APpar，一个免费的、开源的AP参数提取软件工具，专为OriginLab软件包Origin/OriginPro开发。

APpar利用用户定义的导数标准从膜电压记录中检测AP，并计算一套全面的兴奋性参数，包括静息膜电位、AP阈值、阈值处的dV/dt、超射、下射、AP幅度、AP半幅值、上升时间、衰减时间、AP持续时间、AP半宽、0 mV处的AP宽度、电压阈值以上的AP面积、dV/dtMAX、dV/dtMIN以及相应AP的锋电位间期。由于AP阈值是一个特别敏感且依赖方法的测量，APpar包括一个TRUE阈值验证算法。在识别初始前向dV/dt阈值交叉后，该软件找到AP超射，向后搜索最近的前一个局部dV/dt最大值，然后向后搜索到用户定义的dV/dt交叉点，并从这个已验证的阈值点重新计算AP参数。

我们使用来自背根神经节神经元电流钳记录的APs验证了APpar，包括复制相同的AP、电流诱发的重复放电和长时间的自发放电。该软件对相同的复制AP产生了稳定的测量结果，并提取了重复和自发放电序列中AP参数的动态变化。APpar为神经元电生理学中的可重复AP分析提供了一个透明、可定制且与Origin兼容的框架。

意义声明: 动作电位波形分析对于解释神经元兴奋性至关重要，但许多AP测量仍然容易受到用户依赖的阈值放置、手动光标选择和不一致的参数定义的影响。APpar是一个免费、开源软件工具，通过在电生理学实验室广泛使用的OriginLab环境中自动化AP检测和参数提取来解决这个问题。该软件规范化了AP阈值、幅度、持续时间、半宽、后超极化、基于导数的参数和放电指标的定义，并引入了一种TRUE阈值验证算法，该算法从导数验证的阈值点重新计算AP参数。此工作流程减少了操作员依赖的可变性，同时保留了用户对生理上有意义的检测标准的控制。

亮点: 在OriginLab Origin环境中自动分析动作电位波形；AP阈值验证提高了基于导数的阈值检测的可重复性；提取动作电位动力学、幅度、宽度和dV/dt测量；开源工作流程支持可重复的神经元电生理数据分析；使用DRG神经元的重复和自发放电进行了验证。

## Abstract
Quantitative analysis of action potential (AP) waveforms is central to studies of neuronal excitability, ion channel function, disease mechanisms, and pharmacological modulation. However, AP analysis is still often performed using partially manual workflows, laboratory-specific spreadsheets, or proprietary software environments that can limit reproducibility, transparency, and throughput. Here we present APpar, a freely available, open-source software tool for extracting AP parameters, developed for use with the OriginLab software package Origin/OriginPro.

APpar detects APs from membrane voltage recordings using a user-defined derivative criterion and calculates a comprehensive set of excitability parameters, including resting membrane potential, AP threshold, dV/dt at threshold, overshoot, undershoot, AP amplitude, AP half-amplitude, rise time, decay time, AP duration, AP half-width, AP width at 0 mV, AP area above voltage threshold, dV/dtMAX, dV/dtMIN, interspike interval for the respective AP. Because AP threshold is a particularly sensitive and method-dependent measurement, APpar includes a TRUE-threshold validation algorithm. After the initial forward dV/dt threshold crossing is identified, the software finds AP overshoot, searches backward to the closest preceding local dV/dt maximum, then searches backward to the user-defined dV/dt crossing and recalculates AP parameters from this validated threshold point.

We validated APpar using APs from dorsal root ganglion neurons current-clamp recordings, including copied identical APs, current-evoked repetitive firing, and long-duration spontaneous firing. The software produced stable measurements from identical copied APs and extracted dynamic changes in AP parameters across repetitive and spontaneous firing sequences. APpar provides a transparent, customizable, and Origin-compatible framework for reproducible AP analysis in neuronal electrophysiology.

Significance statementAction potential waveform analysis is essential for interpreting neuronal excitability, but many AP measurements remain vulnerable to user-dependent threshold placement, manual cursor selection, and inconsistent parameter definitions. APpar, a freely available, open-source software tool, addresses this problem by automating AP detection and parameter extraction within the OriginLab environment widely available to electrophysiology laboratories. The software formalizes definitions of AP threshold, amplitude, duration, half-width, afterhyperpolarization, derivative-based parameters, and firing metrics, and introduces a TRUE-threshold validation algorithm that recalculates AP parameters from a derivative-validated threshold point. This workflow reduces operator-dependent variability while preserving user control over physiologically meaningful detection criteria.

HighlightsAutomated action potential waveform analysis within OriginLab Origin environments AP threshold validation improves reproducibility of derivative-based threshold detection Extracts action potential kinetics, amplitudes, widths, and dV/dt measurements Open-source workflow supports reproducible neuronal electrophysiology data analysis Validated using repetitive and spontaneous firing in DRG neurons