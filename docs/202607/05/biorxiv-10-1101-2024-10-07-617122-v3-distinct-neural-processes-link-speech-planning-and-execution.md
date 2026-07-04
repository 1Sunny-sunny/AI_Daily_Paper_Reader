---
title: Distinct neural processes link speech planning and execution
title_zh: 独特的神经过程连接言语规划与执行
authors: "Duraivel, K., Rahimpour, S., Barth, K., Chiang, C.-H., Wang, C., Harward, S., Lad, N., Sexton, D., Friedman, A., Sinha, S., Hickok, G., Southwell, D., Viventi, J., Cogan, G. B."
date: 2026-07-03
pdf: "https://www.biorxiv.org/content/10.1101/2024.10.07.617122v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 颅内记录解码言语计划和执行中不同的神经过程
tldr: 本研究利用高时空分辨率颅内记录，揭示言语计划与执行的不同神经过程：前额叶离散编码语音单元，运动区将其整合为连续序列，两者间存在快速神经转换，解释了说话如何从计划无缝过渡到执行。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究大脑如何协调言语计划与执行以产生有意义的声音。
method: 借助不同空间尺度的颅内电生理记录，以高时空分辨率捕获神经活动。
result: 计划时前额叶离散表征语音单元，执行时运动区生成反映单元及过渡特性的连续序列。
conclusion: 从离散语音单元到运动序列的快速神经转换是连接计划与执行的关键机制。
---

## 摘要
说话是人类交流的主要方式。这一交流得益于一个能够规划和执行独特语音组合的产生系统。尽管分布式脑区网络已与说话有关，但言语句的规划和执行如何协调以产生有意义的声音尚不清楚。借助不同空间尺度下颅内记录的高时空分辨率，我们展示了促进言语规划和执行的独特神经机制。在规划阶段，不同层次的言语单元在各自的前额叶位点被离散编码。这些规划好的单元随后在皮层不同层面动态整合，以指导随后的执行。在言语执行阶段，言语运动区产生连续序列，既反映离散的语音单元，也反映单元之间的过渡特性。这种从离散言语单元到运动序列的快速神经转换，将言语规划与执行联系起来，并使我们能够毫不费力地说话。

## Abstract
Speaking is the primary way that humans communicate. This communication is enabled by a production system that can plan and execute unique combinations of speech sounds. Although a distributed network of brain regions has been implicated in speaking, it is unclear how planning and execution of speech are coordinated to produce meaningful sounds. Leveraging the high spatio-temporal resolution of intracranial recordings at different spatial scales, we show distinct neural mechanisms that facilitate speech planning and execution. During planning, different levels of speech units are coded discretely at distinct prefrontal sites. These planned units are then dynamically integrated at various cortical levels to guide subsequent execution. During speech execution, speech motor regions generate continuous sequences that reflect both discrete speech sound units and their transitional properties between units. This rapid neural transition from discrete speech units to motor sequences links speech planning with execution and enables our effortless ability to speak.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **核心问题**：言语产生涉及从意图到发音的复杂转换，但口语规划（planning）与运动执行（execution）在大脑中如何协调、各自的神经表征是什么，以及它们如何衔接以产生流畅的语音，仍不明确。具体而言，音节（syllable）和音素（phoneme）这两级语音单元在规划与执行阶段的时空组织机制是什么？
- **整体含义**：通过高时空分辨率的颅内脑电图（iEEG）和微电极阵列（μECoG），揭示规划网络（前额叶）离散地编码语音单元（先音节后音素），执行网络（感觉运动皮层）则将这些离散表征转换为包含单元及其之间过渡信息的连续运动序列。这一从离散到序列的快速神经转换是流畅说话的基础，为言语产生模型和脑机接口提供实证依据。

### 2. 方法论

- **核心思想**：利用颅内脑电信号（尤其是高γ频段 70–150 Hz）作为局部神经活动的指标，通过对比不同言语条件下的高γ功率，来分离规划与执行阶段的神经表征，并借助解码模型量化语音单元的时间进程。
- **关键技术细节**：
  - **信号提取**：对经过预处理（陷波滤波、共平均参考）的iEEG信号，提取8个对数分布频带（70–150 Hz）的包络，平均得到高γ功率，降采样至200 Hz，并进行z-score基线校正。
  - **音节/音素对比分析**：计算音节对比 ΔHG（VCV vs. CVC 伪词试次的功率差异），在感兴趣区（ROI）内平均，通过置换检验和聚类校正评估时间上的显著性。
  - **解码分析**：使用奇异值分解（SVD）降维，保留解释80%方差的成分，再以线性判别分析（LDA）进行10折交叉验证，解码音节（2类）、音素（9类）或音位过渡概率（3类）。通过滑动窗（200 ms，步长10 ms）获得时间分辨的解码准确率。
  - **功能连接**：计算成对跨网络的高γ净互相关（减去自相关），获得峰值滞后，通过循环移位零分布检验时序显著性。
  - **非负矩阵分解（NNMF）**：数据驱动地将全脑高γ活动分解为5个时间成分，验证预先定义的三网络（规划、执行、监测）时序。

### 3. 实验设计

- **数据集/被试**：
  - **临床监测单元**：52名药物难治性癫痫患者，植入临床iEEG电极（ECoG 2例，SEEG 50例）。总计8106个电极，其中3534个在说话时高γ显著激活。
  - **术中微型电极**：3名清醒开颅或深部脑刺激（DBS）手术患者，植入高密度μECoG阵列（128或256通道，间距1.33 mm或1.72 mm）。
- **任务范式**：延迟伪词复述任务，听觉呈现52个构造的伪词（均为CVC或VCV结构，包含9个音素），延迟1.2–1.6秒后视觉提示“Speak”。术中任务为简化版（无延迟直接复述）。此外有部分被试完成了CVCVC伪词作为控制。
- **对比的层级/网络**：
  - **规划网络**：IFG、rMFG、cMFG
  - **执行网络**：PrCG、PoCG、IPC
  - **监测网络**：aSTG、pSTG、STS、PAC
- **对比内容**：不同ROI间高γ峰值时间、音节对比ΔHG的时间进程、音节与音素解码的时间差异、音素位置解码（P1→P2→P3）、音位过渡概率解码。

### 4. 资源与算力

- 文中未明确提及使用的GPU类型、数量或训练时长。所采用的分析（置换检验、线性解码等）计算复杂度不高，通常可在标准CPU上完成。无直接报告算力资源。

### 5. 实验数量与充分性

- **主要实验组别与分析数**：
  1. 行为分析：以线性混合效应模型检验音节结构对反应时和持续时长的影响。
  2. 全脑iEEG高γ激活：对比响应期与基线，筛选显著电极。
  3. ROI时序分析：计算各ROI高γ峰值时间，比较规划–执行–监测网络的时序。
  4. 功能连接：计算三网络间高γ净互相关滞后。
  5. 数据驱动分解：NNMF验证三网络。
  6. 音节编码分析（ΔHG）：对三网络及各ROI进行音节对比的时间显著性检验，并利用μECoG分析空间梯度。
  7. 降噪控制分析：比较CVCVC vs CVC来排除首音素辅/元音的影响。
  8. 音节与音素解码时间进程：全脑及分网络分析，μECoG微尺度解码。
  9. 音素位置顺序解码：分网络检验P1、P2、P3的时序。
  10. 过渡概率解码：μECoG水平上对CVC伪词解码前向过渡概率，并嵌入音素序列中。
- **充分性与公正性**：实验覆盖多规模、多模态颅内记录，被试数量较多（52+3），采用严格的统计检验（置换检验、多重比较校正、聚类校正）和交叉验证。控制分析（排除首音素干扰、不同音节结构）增强了结论的稳健性。整体实验设计严谨、全面。

### 6. 主要结论与发现

- **三网络时序分离**：左半球前额叶规划网络激活最早，比执行网络早约180 ms，执行网络又比监测网络早约398 ms，存在级联式的信息流。
- **音节编码始于规划**：音节（CVC vs VCV）的神经编码在规划网络最早出现，然后向执行和监测网络传播，且在高密度μECoG上呈现前部（规划）→后部（执行）的空间梯度。
- **层级化的音节-音素时序**：音节解码早于音素解码，两者的时间差在规划网络最大（约250–350 ms），到执行网络压缩（110–130 ms），至监测网络几乎同步（17–25 ms），表明层级压缩是网络间通信的体现。
- **音素序列仅在执行阶段出现**：规划网络解不出音素位置顺序，执行网络和监测网络则能准确解码P1→P2→P3的时序，意味着音素顺序是在运动执行中实时生成，而非预先规划。
- **连续过渡信息嵌入离散顺序**：在感觉运动皮层，不仅解码出离散的音素身份，还解码出音素间的前向过渡概率（如P(C|V)），且这些过渡信息恰好嵌入两个音素之间，显示运动皮层以连续方式组织整个序列。

### 7. 优点

- **高时空分辨率的结合**：运用大规模iEEG和高密度μECoG，在毫秒级和毫米级尺度上捕捉神经活动，精确分离规划与执行的时间进程。
- **层级框架的实证支撑**：通过解码时间差、空间梯度及时序压缩直接为言语产生的层级状态反馈控制（HSFC）模型提供了电生理证据。
- **控制分析严谨**：设计CVCVC伪词任务排除首音素辅/元音的混淆，利用混合效应模型控制被试间差异，数据驱动NNMF验证网络分组，增强了结论的可信度。
- **揭示了从离散到连续执行的关键转换**：首次在微尺度上同时展示音素序列的音素身份和过渡概率编码，解释了流畅发音的神经基础。

### 8. 不足与局限

- **相关性而非因果性**：研究为观察性相关分析，无法确定网络间的因果关系或方向性信息流（如规划→执行是否必须），未来需用刺激或扰动实验验证。
- **工作记忆的贡献未分离**：延迟复述任务中维持语音工作记忆的成分可能与规划过程交织，难以完全剥离记忆维持与规划本身的神经活动。
- **语言材料受限**：仅限于少数英语伪词（CVC、VCV）及有限音素集，缺乏对词汇、语义和更复杂音系结构的研究，结论推广至自然语言产生需谨慎。
- **受试群体特殊性**：患者均为癫痫或运动障碍患者，尽管为常规神经外科手术，仍可能在一定程度上影响神经活动模式（如癫痫活动的潜在干扰）。此外，部分右侧半球结果不一致（规划区域延迟）可能受限于癫痫偏侧性。
- **覆盖范围限制**：iEEG植入由临床需要决定，部分相关区域（如前额叶下部等）可能未充分覆盖，影响ROI分析的代表性。
- **分析方法依赖高γ功率**：高γ是局部场电位的频带，虽然与多单元放电相关，但并非直接测量神经元发放，可能受多种因素影响。

（完）
