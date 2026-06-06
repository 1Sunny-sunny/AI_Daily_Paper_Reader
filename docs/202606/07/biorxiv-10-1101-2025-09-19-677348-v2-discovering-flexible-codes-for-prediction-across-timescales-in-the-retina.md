---
title: Discovering flexible codes for prediction across timescales in the retina
title_zh: 发现视网膜中跨时间尺度的灵活预测编码
authors: "Bojanek, K., Lefebvre, B., Salisbury, J. M., Marre, O., Palmer, S."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.19.677348v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 视网膜神经群体编码与时序动态解码
tldr: 视网膜需快速预测视觉信息，但编码如何适应时间统计变化尚不明确。本研究记录蝾螈视网膜神经节细胞对五类时间相关刺激的反应，以信息瓶颈推断最优预测时域，发现视网膜灵活调整预测时间尺度以适应刺激结构，并保持最优效率。这证明信息瓶颈框架可揭示感觉系统计算目标。
source: biorxiv
selection_source: fresh_fetch
motivation: 研究视网膜在视觉输入时间统计变化时如何调整预测编码。
method: 记录蝾螈视网膜神经节细胞群对随机移动条刺激的反应，利用信息瓶颈框架从数据中推断最优预测时域。
result: 随着刺激时间常数增加，预测时限延长，速度信息编码和运动预期增强，且种群响应保持近最优预测效率。
conclusion: 视网膜种群编码可根据输入时间结构灵活调整预测时间尺度，信息瓶颈框架能有效发现感觉系统的计算目标。
---

## 摘要
视网膜必须编码视觉信息，以支持快速、预测性行为，尽管存在显著的传输延迟。在视觉输入的时间统计特性发生变化这一不断变化的世界中，这种编码如何适应，仍是一个悬而未决的问题。我们在此记录了美西螈视网膜神经节细胞群在五种不同时间相关尺度下对随机移动条状刺激的响应。利用信息瓶颈框架，并将预测时域视为从数据推断的自由参数，我们探究在每种刺激条件下，视网膜被优化以预测未来运动的哪个时间尺度。我们发现，视网膜会根据变化的刺激统计特性调整其预测编码：随着刺激动力学时间常数的增加，推断的预测时域延长。细胞群转向编码更多的速度信息，运动预期增强，同时保持接近最优的预测效率。通过视网膜响应分布的玻尔兹曼机模型量化的群体惊奇度，在推断的最优压缩下追踪刺激的惊奇度。这揭示了视网膜的反转响应与高效预测编码之间的联系。这些结果表明，视网膜群体编码能灵活地将其预测时间尺度调整到输入的时间结构上。更广泛地，它们证明信息瓶颈框架不仅可用于检验，还可用于发现感觉群体中的计算目标。

## Abstract
The retina must encode visual information in a way that supports fast, predictive behavior despite significant processing delays. How this encoding adapts in an ever-changing world, when the temporal statistics of visual input shift, remains an open question. Here we record from populations of retinal ganglion cells in the axolotl as they respond to a stochastic moving bar stimulus across five different temporal correlation scales. Using the information bottleneck (IB) framework, and treating the prediction horizon as a free parameter inferred from the data, we ask what timescale of future motion the retina is optimized to predict under each stimulus condition. We find that the retina adapts its predictive encoding to the changing stimulus statistics: as the time constant of the stimulus dynamics increases, the inferred prediction horizon lengthens. The population shifts toward encoding more velocity information, and motion anticipation grows, all the while maintaining near-optimal prediction efficiency. Population surprise, quantified through a Boltzmann machine model of the retinal response distribution, tracks stimulus surprise under the inferred optimal compression. This connects the retina's reversal response to efficient predictive encoding. These results show that retinal population codes flexibly adjust their predictive timescale to the temporal structure of their inputs. More broadly, they demonstrate that the IB framework can be used to discover, not just test for, computational objectives in sensory populations.

---

## 论文详细总结（自动生成）

# 论文总结：发现视网膜中跨时间尺度的灵活预测编码

## 1. 论文的核心问题与整体含义
- **核心问题**：视网膜需在有限传输延迟下快速编码视觉信息以支持预测性行为。当环境中视觉输入的时间统计特性发生变化时，视网膜如何适应这种塔顶？目前仍不清楚。
- **研究动机**：理解感觉系统如何在动态变化的世界中自适应地调整其计算目标，尤其关注编码的预测时域是否、以及如何随输入统计结构而改变。
- **整体含义**：揭示视网膜群体编码能够灵活地将其预测时间尺度匹配到输入的时间结构上，并证明信息瓶颈框架不仅可用于检验，也可用于从数据中发现感觉系统的计算目标。

## 2. 方法论
- **核心思想**：将信息瓶颈（IB）框架应用于视网膜群体响应，把预测时域（prediction horizon）视为一个**从数据推断的自由参数**，而非预设的固定值。通过寻找最优压缩下刺激与响应的互信息与响应复杂度之间的权衡，来确定每种刺激条件下视网膜被优化用于预测未来的哪个时间尺度。
- **关键技术细节**：
  - 信息瓶颈目标：最大化关于未来刺激（预测目标）的互信息 $I(R; S_{future})$，同时约束关于过去刺激的互信息 $I(R; S_{past})$，通过拉格朗日乘子 $\beta$ 平衡压缩与预测。
  - 将预测时域 $\tau$ 作为可调节参数，针对每种刺激条件，寻找能解释响应最佳压缩特性的 $\tau$。
  - 使用**玻尔兹曼机模型**对响应分布建模，量化群体响应的“惊奇度”（surprise），并将其与刺激的惊奇度进行比较，建立反转响应与高效预测编码之间的联系。
- **算法流程（文字描述）**：
  1. 呈现不同时间相关尺度的随机移动条刺激，记录视网膜神经节细胞群体响应。
  2. 对每种刺激条件，在多个候选预测时域下拟合 IB 模型，评估模型对响应分布的描述能力。
  3. 通过模型选择或拟合优度，推断使 IB 压缩最优的预测时域 $\tau_{opt}$。
  4. 分析群体响应编码的信息内容（如位置、速度、运动预期）与效率，并关联到惊奇度匹配结果。

## 3. 实验设计
- **数据与刺激**：使用**蝾螈（axolotl）**视网膜，记录神经节细胞群体对**随机移动条状刺激**的反应。刺激在**五种不同时间相关尺度**下呈现（即改变了刺激动力学的时间常数），覆盖从快到慢的统计变化。
- **基准与对比对象**：
  - 并不传统意义上的 baseline 对比，而是采用 IB 框架作为理论基准，将实际群体响应与 IB 最优压缩的理论边界进行对比。
  - 通过变化预测时域，观察在哪种设定下响应统计最接近理论最优，从而“发现”视网膜的计算目标。
- **分析指标**：互信息、预测效率、群体惊奇度、速度信息编码强度、运动预期程度等。

## 4. 资源与算力
- 文中**未明确提及**所使用的 GPU 型号、数量或训练时长。
- 实验涉及生理学记录与计算建模，但无公开的算力细节。需推断计算负载集中在 IB 模型拟合与玻尔兹曼机训练上，但无具体硬件说明。

## 5. 实验数量与充分性
- **实验组数**：包含 **5 种时间相关尺度**的刺激条件，每种条件下记录群体细胞响应。
- **分析深度**：在每种条件下推断最优预测时域、编码效率、速度信息、惊奇度等，并比较不同条件的趋势，形成完整的结论链。
- **充分性与公平性**：
  - 实验设计覆盖了从快到慢的动力学变化，能有效揭示预测时域与时间常数的关系。
  - 分析以自身数据驱动为主，未与其它编码模型广泛对比，但内部一致性较高。
  - 使用同一视网膜群体、相同分析流程，保证了不同条件间的可比性。

## 6. 主要结论与发现
- **预测时域适应**：随着刺激动力学时间常数增加（运动变慢、可预测性增强），推断出的最优预测时域**延长**。
- **编码内容转变**：群体向编码更多**速度信息**转变，**运动预期**增强。
- **保持最优效率**：尽管有自适应调整，群体响应始终维持**接近最优的预测效率**。
- **惊奇度匹配**：在推断的最优压缩下，群体响应的惊奇度（玻尔兹曼机模型）追踪了刺激的惊奇度，揭示了**反转响应与高效预测编码**之间的关联。
- **方法论贡献**：证明 IB 框架可用于从神经数据中**发现未知的计算目标**（预测时域），而不仅是事后检验已知假设。

## 7. 优点
- **新颖的方法论应用**：首次将 IB 框架中的预测时域作为自由参数，从数据中直接推断感觉系统的预测目标，实现了从“检验假设”到“发现假设”的跃迁。
- **揭示灵活编码机制**：定量展示了预测编码如何随输入统计动态调整，深化了对适应性预测处理的理解。
- **理论与实验紧密结合**：通过惊奇度匹配将理论预测与生理响应（如反转响应）联系起来，提供了高效编码的生理证据。
- **群体水平分析**：从单个神经元扩展到群体编码，揭示了群体层面如何整合运动信息以实现多尺度预测。

## 8. 不足与局限
- **刺激类型单一**：仅使用了随机移动条，缺乏对更复杂、自然场景下时间统计变化的验证。
- **物种限制**：实验仅在蝾螈视网膜上进行，其结果在其他物种（如哺乳动物）中的推广性未经验证。
- **算力细节缺失**：未提供计算资源信息，难以评估模型的可复现性和规模。
- **对比实验较少**：未与其他编码假说（如纯速度编码、延迟线模型等）进行系统的比较，IB 框架的优越性更多是解释性而非竞争性。
- **预测时域推断的确定性**：未详细讨论置信区间或模型不确定性，单一最优值的推断可能过于简化。

（完）
