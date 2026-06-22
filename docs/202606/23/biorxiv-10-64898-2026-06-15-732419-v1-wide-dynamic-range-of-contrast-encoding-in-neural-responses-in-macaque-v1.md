---
title: Wide dynamic range of contrast-encoding in neural responses in macaque V1
title_zh: 猕猴V1神经响应中对比度编码的宽动态范围
authors: "Yoshida, H., Chen, Y., Geisler, W. S., Seidemann, E."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.15.732419v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 猕猴V1区对比度响应函数表征
tldr: "本研究探究了猕猴初级视觉皮层（V1）对非定向高斯刺激的对比度编码动态范围，韦伯对比度最高达900%，以匹配自然场景中常见的高对比度统计。通过电生理和钙成像，发现平均单神经元放电和群体反应在超过100%对比度后仍持续增强，仅少数神经元饱和。结果表明V1的对比度编码动态范围比先前预想的更宽，更符合自然环境需求。"
source: biorxiv
selection_source: fresh_fetch
motivation: "自然场景中存在大量超过100%韦伯对比度的情况，而现有研究多将对比度限制在100%以内，导致对比度编码理解不完整。"
method: "在注视猕猴的V1区，运用电生理记录单神经元放电和钙成像测量群体反应，并呈现韦伯对比度高达900%的高斯刺激。"
result: "平均神经元反应和群体活动在100%韦伯对比度以上仍显著增长，只有极少数神经元在100%以下饱和。"
conclusion: V1区的对比度编码动态范围比此前假设的更宽，与自然场景中的对比度统计特性更为一致。
---

## 摘要
早期视觉系统中对比度编码的动态范围已在单神经元和群体水平上使用定向刺激（如光栅和Gabor斑块）进行了动物研究。然而，非定向刺激（如高斯型）的对比度编码研究较少，尽管这类刺激能引发大量群体反应。在使用高斯刺激的研究中，初级视觉皮层神经元和神经群体的对比度响应函数通常仅在最高100%的韦伯对比度的有限范围内表征，这可能无法充分反映自然场景中的对比度统计。实际上，我们的分析显示，自然场景中远超100%韦伯对比度的区域无处不在。因此，在自然环境背景下，我们对对比度编码的理解仍不完整。在此，我们在注视的猕猴V1中，通过电生理测量单个神经元的放电活动，通过钙成像测量群体反应，同时呈现韦伯对比度高达900%的宽范围高斯刺激。平均放电反应和平均群体反应在超过100%韦伯对比度后仍持续强劲增长。仅少数神经元在100%韦伯对比度以下饱和。这些结果表明，V1中对比度编码的动态范围比以往假设的更宽，并与自然场景中的对比度统计更为一致。

## Abstract
The dynamic range of contrast-encoding in the early visual system has been investigated at both single-neuron and population levels in animals using oriented stimuli such as gratings and Gabor patches. However, contrast-encoding of unoriented stimuli such as Gaussians has been less explored, even though such stimuli can evoke a large population response. In studies that employ Gaussians, contrast response functions (CRFs) of neurons and neural populations in primary visual cortex are typically characterized across a limited range of Weber contrasts up to 100%, which may not adequately reflect the statistics of contrast in natural scenes. Indeed, our analysis shows that locations with contrasts far exceeding 100% Weber contrast are ubiquitous in natural scenes. Thus, our current understanding of contrast encoding remains incomplete in the context of natural environments. Here, we measured spiking activities of individual neurons using electrophysiology and population responses using calcium imaging in V1 of fixating macaques while Gaussian stimuli were presented over a wide range of Weber contrasts, up to 900%. Both the average spiking response and the average population response continued to increase robustly above 100% Weber contrast. Only a small minority of neurons saturate below 100% Weber contrast. These results demonstrate that the dynamic range of contrast-encoding in V1 is broader than previously assumed and aligns more closely with the statistics of contrast in natural scenes.

---

## 论文详细总结（自动生成）

# 猕猴 V1 神经响应中对比度编码的宽动态范围

## 1. 核心问题与整体含义（研究动机与背景）

- **研究现状与缺口**：早期视觉系统（尤其是初级视觉皮层 V1）的对比度响应函数（contrast response functions, CRFs）已在单神经元和神经群体水平上得到广泛研究，但大多数工作采用定向刺激（如光栅、Gabor 斑块），且将韦伯对比度（$C_{\text{W}}$）限制在 0–100% 的范围内。
- **自然场景中的对比度统计**：作者指出，自然环境中高对比度区域（$C_{\text{W}} \gg 100\%$）普遍存在，这意味着基于 ≤100% 对比度的传统实验范式可能遗漏了视觉系统处理自然信号的真实动态范围。
- **核心问题**：在非定向、大范围高斯刺激下，猕猴 V1 的单神经元与群体活动对超 100% 韦伯对比度的编码能力如何？响应是否在 100% 之后饱和，还是继续增强？
- **整体含义**：该研究旨在纠正对 V1 对比度编码动态范围的过低估计，使其更符合自然场景的统计特性，从而完善我们从生态学角度对早期视觉处理机制的理解。

## 2. 论文提出的方法论

- **核心思想**：突破以往仅研究 ≤100% 韦伯对比度的限制，将刺激范围扩展至高达 900%，并同时记录单细胞放电与群体钙信号，以揭示 V1 对自然高对比度的编码潜力。
- **技术路线与关键细节**：
  - **刺激设计**：采用非定向高斯光斑（unoriented Gaussian stimuli），韦伯对比度从低值延伸至 900%，覆盖自然场景中可能出现的高对比度区间。
  - **单神经元记录**：在清醒注视的猕猴 V1 区插入微电极，记录单个神经元的锋电位发放（spiking activity）。
  - **群体记录**：利用钙成像（calcium imaging）技术，记录更广泛皮层区域的神经群体反应。
  - **数据分析**：构建对比度响应函数，分析平均放电频率及钙荧光信号随韦伯对比度的变化趋势，重点观察在 >100% $C_{\text{W}}$ 区间是否出现饱和。
- **公式或量化指标（无具体方程细节，只有概念）**：
  - 韦伯对比度定义为 $C_{\text{W}} = \frac{L_{\text{stim}} - L_{\text{bg}}}{L_{\text{bg}}}$，其中 $L_{\text{stim}}$ 为刺激亮度，$L_{\text{bg}}$ 为背景亮度。
  - 对比度响应函数刻画神经反应（放电率或钙信号 ΔF/F）与 $C_{\text{W}}$ 的关系。

## 3. 实验设计

- **受试与场景**：清醒、注视状态下的猕猴（macaque），在其 V1 脑区进行记录。自然场景对比度统计用于论证研究动机，未作为实验条件操纵变量。
- **数据来源**：实验数据来自电生理与钙成像的双重记录；自然场景分析可能采用标准自然图像库（具体来源未在摘要中明确）。
- **模拟对比基准（Benchmark）**：并非传统意义上的算法基准，而是以**先前文献中 ≤100% 韦伯对比度下的 V1 响应特性**作为参照系，展示超 100% 范围的新发现。
- **对比维度**：
  - **记录方法之间比较**：单神经元锋电位 vs. 群体钙信号。
  - **对比度区间比较**：低/中等对比度（≤100%） vs. 高/超高对比度（>100% 至 900%）。
  - **自然场景统计**：自然图像中高对比度点的普遍性作为生态合理性基准。

## 4. 资源与算力

- 论文摘要及元数据中**未提及**使用的 GPU 型号、数量、训练时长或任何与深度学习/大规模计算相关的硬件配置。
- 实验主要依赖神经电生理记录系统、双光子钙成像设备及常规数据分析软件，不属于计算密集型 AI 训练任务，因此未披露算力信息。

## 5. 实验数量与充分性

- **实验组数概述**（基于摘要推断）：
  - 单神经元电生理实验：在至少一只猕猴的 V1 中进行了宽范围对比度刺激下的放电记录。
  - 群体钙成像实验：同样在注视猕猴上获取 V1 群体钙反应。
  - 自然场景统计分析：以独立数据集展示高对比度（>100% $C_{\text{W}}$）的普遍性，作为生态动因。
- **充分性评价**：
  - 实验同时覆盖了单细胞和群体两个层次，且对比度跨度远超既往研究，设计本身对研究问题具有针对性。
  - 然而，摘要未提供动物数量、神经元/成像样本量、重复次数等细节，难以评判统计效力是否足够稳健。
  - 未见明显的不公平对比：主要与已有文献中的有限范围数据进行定性比较，而非不同模型间的角逐。
- **客观性**：研究动机以自然统计为客观基础，实验结果通过直接测量获得，对比性强，但缺少定量模型拟合的交叉验证等细节。

## 6. 论文的主要结论与发现

- **平均响应持续增长**：无论是单神经元平均放电率还是群体钙信号，在韦伯对比度超过 100% 后仍继续大幅上升，未出现平台或下降。
- **少数神经元饱和**：仅有极小部分 V1 神经元在 100% 韦伯对比度以下达到饱和，绝大多数细胞对更高对比度依然敏感。
- **动态范围被低估**：V1 对比度编码的动态范围比以往普遍假设的更宽，传统实验中 100% 的上限人为压缩了这一范围。
- **与自然环境一致**：宽的动态范围与自然场景中普遍存在的高对比度统计特征相吻合，表明 V1 加工已经适应了生态视觉需求。

## 7. 优点：方法或实验设计上的亮点

- **跨越传统边界**：将韦伯对比度上限从惯常的 100% 拓展至 900%，是本文最显著的创新点，直接针对自然视觉输入的真实范围。
- **双重记录层面**：同时运用电生理和钙成像，既能捕捉单神经元的精准时序放电（电生理），又能观察大范围皮层群体活动（钙成像），提供了互补的神经证据。
- **生态效度驱动**：以自然场景统计分析作为出发点，使研究问题具有明确的生态学意义，超越单纯的神经生理学参数测量。
- **简单而有力的刺激**：使用非定向高斯光斑，避免方向选择性带来的复杂因素，更纯粹地检验对比度编码本身。

## 8. 不足与局限

- **信息不完整**：仅基于摘要分析，缺少方法细节（动物数量、细胞样本量、重复数、统计检验）和图表，无法评估结论的可重复性和统计显著性。
- **刺激类别局限**：仅使用非定向高斯刺激，而真实世界的对比度常伴随方向、空间频率、运动等特征，研究结论向自然复杂刺激的泛化需谨慎。
- **种群采样偏差**：单电极记录可能偏向于较大、活跃的神经元，钙成像在时间分辨率上有所牺牲，可能影响绝对响应幅度的比较。
- **未涉及行为相关性**：没有建立神经响应与知觉或行为之间的联系，未能说明宽动态范围如何影响视觉感知。
- **物种局限**：实验在猕猴 V1 上进行，虽与人类类似，但仍需小心推论至人脑。
- **计算模型缺失**：未提供解释宽动态范围的计算模型或规范化机制（如对比度增益控制），缺乏对潜在网络的机理解释。

（完）
