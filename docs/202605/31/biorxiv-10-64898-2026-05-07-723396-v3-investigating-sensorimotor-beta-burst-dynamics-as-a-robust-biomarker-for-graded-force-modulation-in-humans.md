---
title: Investigating sensorimotor beta burst dynamics as a robust biomarker for graded force modulation in humans
title_zh: 研究感觉运动beta爆发动态作为人类分级力调制稳健生物标志物
authors: "Perwez, M. S., Bonaiuto, J. J., Suthar, B., Muralidharan, V."
date: 2026-05-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.07.723396v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: Beta爆发动力学用于脑机接口中的力解码
tldr: 该研究针对脑机接口中连续力解码难题，探究感觉运动beta爆发作为稳健生物标志物的潜力。通过16名受试者在四种力水平下执行运动执行与运动想象任务，发现beta爆发的幅度、谱宽等特征可区分不同力水平，且爆发波形与力调制相关，表明beta爆发可替代传统ERD/S，为实现精确力控提供新路径。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统ERD/S在连续力解码中不够稳健，需寻找更有效的生物标志物以实现精细的力调制脑机接口。
method: "记录16名受试者在执行四种力水平（10%、25%、50%、75%最大自主收缩）的运动执行和运动想象任务时的EEG，提取感觉运动beta爆发并分析其频谱与时间特征。"
result: 运动执行中beta爆发幅度和谱宽随力水平变化，且不同条件伴生不同爆发波形，而运动想象中的变化较弱。
conclusion: 感觉运动beta爆发的特征可有效编码力水平，有望成为实现脑机接口精确力控制的关键生物标志物。
---

## 摘要
与运动执行和运动想象相关的最显著特征是mu和beta频段（8-30 Hz）的事件相关去同步化和同步化（ERD/S）。在脑机接口（BCI）的背景下，这种ERD/S特征有助于二分类决策，如左右想象，但对于连续预测，如精确解码不同力度水平，它并不是一个稳健的生物标志物。这对于开发具有精确动态力输出的更好BCI应用至关重要。最近的研究表明，感觉运动beta爆发与运动控制的关系比beta频段功率更强，甚至可以在单次试验水平上观察到。因此，我们研究了beta爆发的瞬态特性是否能为BCI力解码提供一种替代但稳健的生物标志物。在此，我们设计了一个实验，16名人类受试者在记录脑电图的同时，执行了四个力度水平（最大自主收缩的10%、25%、50%和75%）的运动执行（ME）任务，并想象执行相同的力度，即运动想象（MI）任务。我们观察到在ME任务期间运动皮层有清晰且经典的ERD模式，而在MI任务期间则不太明显。在提取感觉运动beta爆发后，我们观察到运动执行和想象之间在频谱爆发特征上的差异，包括爆发幅度、频谱宽度和时间宽度。此外，不同力度水平与爆发幅度和爆发频谱宽度的变化相关，特别是在运动执行期间。有趣的是，我们发现不同的beta爆发波形与不同的力度水平和条件相关联。这表明爆发水平特征可能由潜在的beta爆发波形变化所驱动。总体而言，我们的研究表明，感觉运动beta爆发可以成为在基于脑机接口的假肢中实现精确力控制的重要一环。

## Abstract
The most prominent signature associated with motor execution and motor imagery is the event-related desynchronisation and synchronisation (ERD/S) in the mu and beta bands (8-30 Hz). In the context of brain-computer interfaces (BCI), this ERD/S signature is helpful for binary decisions, such as left vs. right imagery, but it is not a robust biomarker for continuous prediction, such as precisely decoding different levels of force application. This is essential for developing better BCI applications with precise dynamic force outputs. Recent studies have revealed that sensorimotor beta bursts have a stronger relationship with motor control, even at a single-trial level, than beta band power. We, therefore, investigated whether the transient nature of beta bursts provide an alternative, but robust biomarker for BCI force decoding. Here, we designed an experiment where human participants (N = 16) performed both motor execution (ME) at four force levels (10%, 25%, 50%, and 75% of maximum voluntary contraction) and imagined exerting the same, i.e. a motor imagery (MI) task, as their electroencephalogram was recorded. We observed a clear and classical ERD pattern in the motor cortex during the ME task, whereas it was less pronounced during the MI task. After extracting sensorimotor beta bursts, we observed differences in spectral burst features between motor execution and imagery including burst amplitude, spectral width, and temporal width. Moreover, different force levels were correlated with changes in the burst amplitude and burst spectral width, specifically during motor execution. Interestingly, we found that different beta burst waveforms are associated with the different force levels and conditions. This suggests that the bursts-level features could be driven by changes in the underlying beta burst waveforms. Overall, our study shows that sensorimotor beta burst can be an important piece of the puzzle to implementing precise force control in brain-computer interface-based prosthetics.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究背景**：脑机接口（BCI）中常用的运动相关神经信号是mu和beta频段的事件相关去同步/同步（ERD/S），它适合二分类（如左右手想象），但在连续力控制（如精确解码不同力度）上鲁棒性不足。
- **核心问题**：能否从感觉运动beta爆发的瞬态特性中找到一种鲁棒的生物标志物，用于BCI中分级力调制（连续力解码），从而突破传统ERD/S在动态力输出上的局限。
- **整体含义**：该研究试图将beta爆发动力学（而非传统频带功率）作为力编码的替代特征，为实现具有精确力控能力的假肢或BCI应用提供新的神经生理学依据。

## 2. 论文提出的方法论

- **核心思想**：以单试次可观测的beta爆发（瞬时振荡事件）替代平滑后的beta频段功率（ERD/S），提取其频谱‑时间特征来编码不同力水平。
- **关键技术细节**：
  - **信号采集**：16名受试者执行运动执行（ME）和运动想象（MI）任务，采用4种力水平（10%、25%、50%、75%最大自主收缩），同步记录头皮EEG。
  - **Beta爆发提取**：在感觉运动皮层通道上识别并提取beta爆发，定义爆发事件并计算其频谱特征（如幅度、谱宽、时间宽度）。
  - **特征分析**：比较不同条件（ME vs MI）、不同力水平下爆发幅度、谱宽等特征的变化；进一步分析爆发波形形态是否与力水平相关联。
- **算法流程**（文字描述）：  
  预处理EEG → 选择感觉运动区电极 → 时频分解 → 检测beta爆发（基于功率阈值） → 对每个爆发计算幅度、谱宽、时间宽度等特征 → 统计检验这些特征在不同力和任务下的差异 → 通过波形形状聚类或比较揭示潜在驱动因素。

## 3. 实验设计

- **数据集与场景**：
  - 自采集数据集：16名健康成人。
  - 两个任务场景：运动执行（真实握力）和运动想象（想象相同握力）。
  - 四种力条件：10%、25%、50%、75%最大自主收缩。
- **Benchmark与对比方法**：
  - 主要对比对象：传统的beta频段ERD/S模式（通过功率时间序列分析）。
  - 以ERD在ME和MI中的清晰度为性能参照，说明ERD在MI中变弱，而beta爆发特征可提供更细粒度的区分。
  - 文中并未明确列出其他计算模型作为benchmark，更多是神经特征层面的对比分析。

## 4. 资源与算力

- **算力资源**：原文未提及GPU、CPU型号或训练时长等算力信息。由于该研究主要是离线EEG分析和统计检验，未涉及深度学习模型训练，因此对算力的需求较低，作者也未声明具体硬件配置。

## 5. 实验数量与充分性

- **实验组别**：
  - 16名受试者 × 2种任务（ME, MI） × 4种力水平 = 共128组条件（每个受试者内部作为重复测量）。
  - 分析维度包括：
    1. ERD/S模式描绘（定性验证）；
    2. 任务间beta爆发特征对比（ME vs MI）；
    3. 力水平与爆发幅度、谱宽的关联分析（主要针对ME）；
    4. 爆发波形形态与力水平/条件的关联性探索。
- **充分性与公平性**：
  - 样本量较小（N=16），但采用受试者内设计，统计检验可控制个体差异。
  - 条件设置系统（4水平×2任务），能揭示力调制的主效应和任务间的交互。
  - 未涉多中心或跨数据集验证，外部泛化性待检验。整体实验设计合理，但作为初步探索，验证尚不算充分。

## 6. 论文的主要结论与发现

- **任务差异**：运动执行期间的ERD模式典型且清晰，运动想象期间的ERD较微弱；在beta爆发特征上同样观察到ME与MI的幅度、谱宽和时间宽度差异。
- **力水平编码**：在运动执行中，beta爆发的幅度和频谱宽度随力水平变化而改变，表明这些瞬态特征能够区分不同力度。
- **波形特异性**：不同力水平与不同的beta爆发波形相关联，暗示爆发级别的调制可能源于波形形态的变化，而不仅仅是功率增强或减弱。
- **应用潜力**：感觉运动beta爆发可作为BCI精确力控制的重要生物标志物，具有单试次、等级性解码的潜力。

## 7. 优点

- **创新思路**：从传统的持续性功率转向事件性爆发特征，更贴合运动控制的瞬态神经编码机制。
- **特征丰富性**：不仅考察幅度，还分析了谱宽和波形形态，为力编码提供了多维候选特征。
- **实验设计系统**：在同一个实验中同时对比真实运动与运动想象，并设置四级力度梯度，增强了结论的说服力。
- **关注BCI痛点**：直指连续力解码这一实用难题，具有较强的应用导向。

## 8. 不足与局限

- **样本量小、被试同质**：仅16名健康成人，未涵盖患者或大样本人群，个体差异和泛化能力未知。
- **离线分析**：未进行在线BCI力解码验证，爆发特征的实际解码精度、延迟等未量化评估。
- **运动想象效果弱**：MI任务中ERD不清晰，爆发特征的力调制效应也不如ME显著，实际应用于完全无法运动的患者时可能面临信噪比挑战。
- **方法细节缺失**：摘要中未详述beta爆发检测的阈值和伪迹控制方法，可能影响可重复性。
- **缺乏对比基线**：未与其他力解码特征（如Hjorth参数、协方差矩阵等）进行直接性能比较，难以判断beta爆发特征的相对优劣。
- **未提及算力**：虽离线分析算力需求低，但若向在线BCI转化，实时爆发检测的计算效率尚需评估。

（完）
