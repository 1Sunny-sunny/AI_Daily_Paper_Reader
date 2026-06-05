---
title: Efficient neural encoding of time intervals in speech and complex sound sequences
title_zh: 语音与复杂声音序列中时间间隔的高效神经编码
authors: "Chen, H., Wang, J., Gao, J., Zhang, H., Ding, N."
date: 2026-06-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729227v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 提出听觉皮层时间间隔的高效神经编码
tldr: 语音等复杂声音中的时间间隔编码需兼顾精确性与宽广动态范围。本研究提出听觉皮层采用高效编码策略，通过MEG和iEEG实验发现，皮层对音节时长的响应函数可自适应于时长分布的均值和方差，并呈现压缩非线性以最大化信息熵。计算模型进一步阐释了持续推断时长分布的高效编码算法，该机制在自然言语理解中亦得到验证，为神经高效处理可变时间间隔提供了新证据。
source: biorxiv
selection_source: fresh_fetch
motivation: 复杂声音中时间间隔的神经编码需要同时满足高精度和宽动态范围，但传统机制难以解释。
method: 结合MEG、iEEG记录与计算建模，分析受试者在不同音节时长分布下的神经响应函数及其自适应特性。
result: 听觉皮层的间隔反应函数随音节时长分布的均值和方差自适应调整，并展现出降低响应偏度的压缩非线性，符合最大熵高效编码。
conclusion: 大脑采用适应性高效编码机制，通过持续推断统计分布来实现对多变时间间隔的精确神经表征。
---

## 摘要
在复杂声音中编码时间间隔面临双重挑战：它必须精确并覆盖广泛的动态范围。例如，在语音中，音节延长十毫秒即可表示重音或短语边界，但音节的时长分布呈长尾状，超过500毫秒，且在不同说话者之间统计特性各异。在此，我们提出听觉皮层采用高效编码来表示时间间隔。当听者听到来自不同时长分布的音节序列时，颞叶皮层脑磁图（MEG）响应随音节时长缩放，这通过间隔响应函数来表征。关键的是，该间隔响应函数符合高效编码的预测。其截距和斜率分别适应音节时长的均值和方差，并且它始终表现出一种压缩非线性，降低了响应的偏度，这与最大熵编码一致。一个不断更新时长分布推断的计算模型提供了这种高效编码的算法解释，颅内脑电图（iEEG）数据证实了自然语音理解过程中的相同原理。综上所述，我们的发现揭示了一种高效的神经机制，它支持在复杂声音序列中对高度可变的时间间隔进行精确编码。

## Abstract
Encoding time intervals in complex sound faces dual challenges: it must be precise and cover a broad dynamic range. In speech, for example, a ten millisecond lengthening of a syllable can signal stress or phrasal boundaries, yet the syllable duration distribution is long tailed beyond 500 ms and has variable statistics across speakers. Here, we propose that the auditory cortex employs efficient coding to represent time intervals. When listeners heard syllable sequences drawn from different duration distributions, the magnetoencephalographic (MEG) response from the temporal cortex scaled with syllable duration, which is characterized using the interval response function. Crucially, this interval response function met predictions of efficient coding. Its intercept and slope adapted to the mean and variance of syllable duration, respectively, and it consistently exhibited a compressive nonlinearity that reduced response skewness, consistent with a maximum entropy code. A computational model that constantly updates the inference of duration distribution provided an algorithmic account of this efficient coding, and intracranial electroencephalogram (iEEG) data confirmed the same principles during natural speech comprehension. Together, our findings reveal an efficient neural mechanism that supports precise encoding of highly variable time intervals in complex sound sequences.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **核心问题**：复杂声学序列（尤其是语音）中的时间间隔（如音节时长）编码面临双重约束：一方面要**极其精确**（毫秒级差异即可改变语义或韵律边界），另一方面要覆盖**宽广的动态范围**（音节时长可从几十毫秒延伸至 500 毫秒以上，且不同说话人间的统计分布存在显著变异）。传统神经编码理论难以同时满足这两个要求。
- **整体含义**：本文提出并验证了听觉皮层采用**高效编码**策略来表征时间间隔，即神经响应会自适应地追踪当前输入的时长分布统计量，并以最大化信息熵的方式压缩非线性，从而在有限神经资源下同时实现高精度与宽动态范围。这一发现为脑如何处理时序多变信号提供了原则性解释。

### 2. 方法论
- **核心思想**：假设听觉皮层通过**间隔响应函数**将物理时长映射为神经活动量，该函数会根据环境（即音节的时长分布）的动态统计进行**适应性调整**，以逼近信息论上的最优编码——最大化响应的熵，同时降低响应分布的偏度。
- **关键技术细节/算法流程**：
  - **间隔响应函数刻画**：利用脑磁图（MEG）和颅内脑电图（iEEG）记录被试在被动聆听音节序列时颞叶皮层的诱发响应，提取响应幅度随音节时长变化的函数关系。
  - **自适应预测**：若为高效编码，则响应函数的**截距**应随时长分布的**均值**漂移，其**斜率**应随分布的**方差**缩放；且该函数必然呈**压缩非线性**，使得在长时长区间的响应增长变缓，从而降低整体响应分布的偏度，达成最大熵编码。
  - **计算模型**：建立不断**推断并更新时长分布先验**的算法模型，从原理上复现上述自适应压缩编码，为观测到的神经现象提供计算层次解释。
  - **验证推广**：在自然语音理解任务中，使用 iEEG 数据检验相同的高效编码规律是否成立。

### 3. 实验设计
- **数据集/场景**：
  - **主实验**：合成音节序列，将其分为具有不同**时长分布**（均值、方差不同）的条件。受试者聆听这些序列，同步记录 MEG。
  - **验证实验**：采用**自然连续语音**作为刺激，采集 iEEG 数据，考察自然语境下的编码机制。
- **基准与对比**：
  - 该研究属于神经机制的探索性实验，**无传统意义上的“基准模型”**。其比较逻辑内置在实验设计中：通过操控时长分布的统计量（如均值、方差），对比不同分布条件下测得的间隔响应函数的形状和参数，检验其是否符合**高效编码的理论预测**（即截距与均值的对应关系、斜率与方差的对应关系、以及压缩非线性的出现）。
  - 隐含对比的是“非适应性的固定编码”假设，即如果神经编码不随分布变化，则无法观察到上述自适应效应。

### 4. 资源与算力
- 文中提供的摘要和元数据**未提及任何 GPU 型号、数量或训练时长**。该研究以神经成像实验和计算建模为主，其算力消耗可能集中于 MEG/iEEG 数据的预处理和统计分析以及轻量级模型的模拟，但未给出具体算力描述。因此，**无法获取这方面的量化信息**。

### 5. 实验数量与充分性
- 从现有信息推断，实验至少包含两大组：
  - **MEG 主实验**：含多个时长分布操控条件，每个条件下需采集足够的试次以提取可靠的响应函数。
  - **iEEG 自然言语验证实验**。
  - **计算建模**：模拟不同分布下的编码过程，并与神经数据对照。
- **充分性评价**：研究同时采用了**无创高时间分辨率（MEG）和有创高空间/时间分辨率（iEEG）**两种互补的神经记录技术，并在严格控制的合成音节与生态效度更高的自然语音场景下交叉验证，实验设计严谨。加上计算模型为神经发现提供了算法层级的解释，整体证据链较为完整。然而，由于未见到全文，无法精确评估每个条件下的被试数量、试次数和条件平衡等细节是否充分，但就现有信息而言，实验设计在逻辑上对齐了核心假说，客观且维度丰富。

### 6. 论文的主要结论与发现
- 听觉皮层确实采用**高效编码**策略处理时间间隔：
  - 颞叶神经响应的间隔响应函数**自适应于音节时长的统计分布**：其截距随分布均值变化，斜率随分布方差变化。
  - 该响应函数**始终表现出压缩非线性**，有效降低了神经响应分布的偏度，符合**最大熵编码**原则（即在给定响应范围限制下最大化信息传输）。
  - 所提出的**持续推断时长分布的计算模型**能够重现上述自适应压缩编码行为，为算法提供了解释。
  - 在**自然语音理解**过程中，iEEG 数据同样印证了同一套高效编码原理，表明这是真实语言加工中的基本神经机制。

### 7. 优点
- **理论驱动，实验验证**：从信息论的高效编码假设出发，推导出可检验的量化预测（截距、斜率、压缩非线性），并通过操控分布参数进行直接测试，逻辑严密。
- **多模态交叉验证**：同时使用 MEG（无创、高时间分辨率）和 iEEG（有创、高空间精度）两种记录手段，并在合成序列与自然语音两种声学情境中复现效应，极大增强了结论的可靠性与推广性。
- **多层次解释**：从行为/生理现象（响应函数自适应）到计算原则（最大熵编码）再到算法模型（分布推断更新），提供了 Marr 三层级的完整解释框架。
- **生态效度高**：研究动机直接源于真实语音中音节时长的长尾分布和跨说话人变异，且最终在自然语音理解中证实，应用前景明确。

### 8. 不足与局限
- **统计分布操控的简洁性**：人工合成的音节序列可能仅变化了时长，而真实语音中时长变化往往与频谱、基频等高阶特征共变，简化环境下的结论能否完全泛化至所有自然场景仍需更多检验。
- **因果性未直接证实**：实验主要基于被动聆听的观测性证据（MEG/iEEG 响应与分布统计的相关），未通过神经调控（如经颅磁刺激）直接测试自适应编码的因果必要性。
- **个体差异与广义分布**：不同听者的先验经验、注意力状态会否影响分布推断速度或压缩函数形态，文中未涉及（根据现有摘要推断）。
- **技术细节缺失**：由于目前仅可获摘要，存在信息盲区——例如具体被试量、分布操控的精确范围、压缩非线性的数学模型拟合形式、计算模型的具体架构等，均无法评估其稳健性。实际论文可能有更详尽的限制说明，但在此无法呈现。

（完）
