---
title: A Thin Film Transistor Backplane for Scalable Chronic Neural Interfaces
title_zh: 一种用于可扩展慢性神经接口的薄膜晶体管背板
authors: "Bourhis, A. M., Vatsyayan, R., Tonsfeldt, K. J., Galton, I., Dayeh, S. A."
date: 2026-06-24
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.23.733868v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 直接脑机通信硬件
tldr: 为了应对神经接口高通道数扩展需求，本研究提出一种受有源矩阵显示技术启发的柔性薄膜集成电路平台。该平台在聚酰亚胺基底上集成双栅非晶铟镓锌氧化物晶体管，实现像素内跨导放大与行列时分复用，并通过混合陶瓷-聚合物封装实现超38年寿命。在大鼠急慢性实验中，系统热负担低、记录稳定，30天后仍保持功能，为下一代可扩展神经接口奠定了基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经接口向高通道数发展中，无源阵列面临互连瓶颈，需要集成有源电子器件以减少互连、提高通道密度。
method: 基于显示技术，在柔性聚酰亚胺基底上制造双栅非晶IGZO晶体管，实现像素内放大和行列复用，并采用混合薄膜封装。
result: 封装后器件加速老化测试表明寿命超过38年，动物实验显示热负担小，能稳健记录感觉诱发信号，并在植入30天后保持稳定功能。
conclusion: 受显示技术启发的柔性薄膜电子器件可作为可扩展的神经接口基础，提供高通道数、长期稳定性。
---

## 摘要
随着薄膜制造、光刻和连接技术的进步，将神经接口扩展到更高的通道数已迅速加速，使得无源阵列能够达到数千个通道，并为走向更大的格式规划了可信的路径。将有源电子器件直接集成在感应位点为提高通道密度提供了一种补充途径，因为它减少了访问大型阵列所需的互连数量。在此，我们受有源矩阵显示技术的启发，推出了一种用于有源神经传感的单片柔性薄膜集成电路平台。该系统在聚酰亚胺衬底上集成双栅非晶氧化铟镓锌晶体管，以实现像素内跨导放大和行列时分复用，从而提高了高通道数应用的可扩展性。通过器件架构、接触工程和混合陶瓷-聚合物薄膜封装的协同优化，实现了稳定运行，在加速老化条件下预测寿命超过38年。在急性和慢性体内大鼠研究中，该平台表现出可忽略的热负担、稳健的感觉诱发电位记录，并且尽管存在组织包裹，在30天内功能稳定。这些结果确立了受显示启发的柔性薄膜电子学作为下一代神经接口可扩展构件的地位。

## Abstract
Scaling neural interfaces to ever-higher channel counts has accelerated rapidly with advances in thin-film fabrication, lithography, and connectorization, enabling passive arrays to reach thousands of channels and chart credible pathways to much larger formats. Integrating active electronics directly at the sensing sites offers a complementary route to higher channel density by reducing the number of interconnects required to access large arrays. Here we introduce a monolithic flexible thin-film integrated circuit platform for active neural sensing, inspired by active-matrix display technology. The system integrates dual-gate amorphous indium gallium zinc oxide transistors on polyimide substrates to implement in-pixel transconductance amplification and row-column time-division multiplexing, improving scability for high-channel-count applications. Co-optimization of device architecture, contact engineering, and a hybrid ceramic-polymer thin-film encapsulation yields stable operation with projected lifetimes exceeding 38 years under accelerated aging. In acute and chronic in vivo rat studies, the platform exhibits negligible thermal burden, robust sensory-evoked recordings, and stable functionality over 30 days despite tissue encapsulation. These results establish display-inspired flexible thin-film electronics as a scalable building block for next-generation neural interfaces.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义
- **研究动机**：神经接口正在向数千乃至数万通道规模演进，但传统的无源电极阵列面临互连导线急剧增多的物理瓶颈，导致通道密度难以继续提升。
- **解决思路**：借鉴有源矩阵显示技术（如 AMOLED）的思想，将信号放大与寻址电路直接集成在柔性传感位点附近，通过“像素内”有源电子器件实现行列复用，从而大幅减少引出导线数量，为高通道可扩展神经接口提供新的硬件范式。

## 2. 方法论
- **核心思想**：在柔性聚酰亚胺衬底上，单片集成双栅非晶氧化铟镓锌（a‑IGZO）薄膜晶体管，构建一个类似于显示屏有源像素的“有源传感像素”平台。
- **关键电路功能**：
  - **像素内跨导放大**：每个传感位点均配置基于双栅 IGZO 晶体管的跨导放大器，将微弱的神经电信号在源端直接转换为可读的电流或电压信号，降低长线传输噪声。
  - **行列时分复用**：通过行选通和列读出的方式，以 $m+n$ 条总线访问 $m \times n$ 个通道，显著降低互连复杂度。
- **器件与封装优化**：
  - **接触工程**：对源/漏电极接触进行工程化处理，以提升器件稳定性和性能。
  - **混合陶瓷‑聚合物薄膜封装**：在柔性芯片上叠加无机/有机多层封装膜，经加速老化测试推算，器件在生理环境下的工作寿命超过 38 年。

## 3. 实验设计
- **实验对象与场景**：
  - **急性大鼠实验**：验证平台在植入早期的热安全性和感觉诱发信号记录能力。
  - **慢性大鼠实验**：评估持续 30 天的功能稳定性及组织反应。
- **评估指标与基准**：
  - **热负担**：测试芯片运行时的温升，以确保其在脑组织中的生物安全性。
  - **信号质量**：记录感觉诱发电位（如躯体感觉刺激下的神经响应），检验信噪比和波形保真度。
  - **长期可靠性**：通过加速老化实验外推实际体内寿命，并以 30 天慢性植入后是否仍能稳定记录作为有效性判据。
- **对比方法**：文中未明确提出与特定有源或无源神经接口的对照实验，主要聚焦于平台本身的性能验证与寿命预测。

## 4. 资源与算力
- 本研究为硬件制备、封装与动物电生理实验，不涉及大规模神经网络训练或高性能计算。文中未提及 GPU 型号、数量或训练时长等算力信息。

## 5. 实验数量与充分性
- **实验组别**：
  - 加速老化封装实验（推算寿命）。
  - 急性体内热测量与电生理记录。
  - 慢性 30 天植入后的连续功能验证。
- **充分性与客观性**：
  - 实验覆盖了从材料稳定性到体内功能的完整验证链条，成果具有较强的说服力。
  - 然而，缺乏与现有高密度无源阵列或其它有源阵列（如硅基 CMOS 阵列）的直接并行对比，难以量化其在通道密度、功耗、信噪比等方面的具体优势。实验动物数量、植入位点数量等统计细节在摘要和元数据中未披露，严谨性尚待全文验证。

## 6. 主要结论与发现
- 基于双栅 a‑IGZO 晶体管和混合薄膜封装的柔性集成电路平台，可在体内稳定工作，预测寿命 >38 年。
- 平台在急性和慢性大鼠实验中展现出极低的热负担，能高质量记录感觉诱发信号；即使经过 30 天植入并出现组织包裹，仍能保持功能稳定。
- 这种受显示技术启发的柔性薄膜电子学，是构建下一代可扩展、高通道数神经接口的可行基础构件。

## 7. 优点
- **高可扩展性**：通过行列寻址将互连导线数从 $O(n)$ 降为 $O(\sqrt{n})$，为数千乃至数万通道阵列的布线提供解决思路。
- **芯片级集成**：单片集成放大与复用功能，避免多芯片键合带来的复杂度和失效点。
- **超长期稳定性**：混合封装方案使器件在加速老化中的寿命外推超过 38 年，远超当前植入式器件的常见封装寿命。
- **体内验证**：同时进行急性和慢性动物实验，证明了生物相容性和实际信号采集能力。

## 8. 不足与局限
- **对比缺失**：未与现有高密度神经接口（如 Neuropixels、柔性硅纳米线阵列等）在关键指标上进行并排比较，难以定位其相对竞争力。
- **通道规模局限**：论文摘要未透露实际阵列尺寸，仅展示了概念和单像素/小阵列功能，尚未验证数千通道下的版图面积、功耗、散热与信号串扰等系统级挑战。
- **体内周期与统计**：慢性实验仅报告 30 天，虽能初步证明稳定性，但距离临床所需的数年仍相距甚远；实验动物数量和行为学评估细节未公开。
- **组织包裹**：文中提到存在组织包裹现象，虽暂未影响功能，但更长时间的包裹演变是否会加速器件失效或降低信号质量尚不明确。
- **材料与工艺限制**：a‑IGZO 具有光敏性和偏压应力不稳定性，文中虽通过双栅结构和封装缓解，但在长期植入中的电学漂移仍需监测。

（完）
