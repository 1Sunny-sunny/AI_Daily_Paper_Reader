---
title: Direction and orientation preferences in mouse superior colliculus and its retinal inputs align with topographic axes atop locally mixed tuning
title_zh: 小鼠上丘及其视网膜输入中的方向和朝向偏好与拓扑轴对齐并叠加于局部混合调谐
authors: "He, Z., Gonzalez Fleitas, M. F., Gabdrashova, R., Schroeder, S."
date: 2026-07-03
pdf: "https://www.biorxiv.org/content/10.64898/2025.12.21.695778v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 检查上丘神经元和视网膜输入的方向和朝向调谐
tldr: 小鼠上丘（SC）神经元对运动方向和朝向的调谐偏好是否存在空间组织以及如何与视网膜输入对应一直存在争议。本研究结合双光子钙成像和Neuropixels记录，发现视网膜输入的偏好与先前描述的视网膜拓扑轴一致，即每个视野位置同时表征多个方向/朝向，而非单一偏好。随着SC深度增加，神经元的调谐逐渐偏离此组织，且局部聚类微弱。这表明SC为每个视野位置提供多样化的方向/朝向编码，以支持灵活的视觉引导行为。
source: biorxiv
selection_source: fresh_fetch
motivation: 探讨小鼠上丘方向与朝向偏好的空间组织及其与视网膜输入的关系，以解决该领域存在的争议。
method: 结合双光子钙成像（记录视网膜boutons和浅层SC神经元）与Neuropixels探针（覆盖SC全深度），分析调谐特性与空间距离的关系。
result: 视网膜boutons的偏好与视网膜的拓扑轴对齐，呈现局部混合调谐；随SC深度增加，神经元逐渐偏离此组织，且局部聚类仅限于极小的空间尺度。
conclusion: 小鼠SC的视网膜输入和神经元在每个视野位置表征多个方向和朝向，为多样化的视觉引导行为提供灵活的信息读出。
---

## 摘要
在小鼠上丘（SC）中，神经元对运动方向和朝向有强烈的调谐，但这些偏好是否具有空间组织性，以及这种组织如何与上丘的视网膜输入中所发现的相联系，仍然存在争议。我们通过结合对视网膜boutons和浅层SC神经元的双光子钙成像，以及跨SC全深度的Neuropixels记录，来解决这些问题。然后我们探究了方向和朝向偏好如何依赖于视野位置，以及单元间的调谐相似性如何依赖于SC中的横向和垂直距离。视网膜boutons表现出强烈的调谐，它们的偏好与先前在视网膜中描述的四种运动方向和朝向的视网膜拓扑组织紧密匹配，而不是一种在每个视野位置单一方向或朝向占主导的全局地图。随着深度增加，SC神经元逐渐偏离这一组织。叠加在已识别的拓扑结构上，视网膜boutons和SC神经元中调谐偏好的局部聚类较弱，且局限于非常小的空间尺度。总之，这些结果表明，小鼠上丘中的视网膜输入和神经元为视野中的每个位置表征了多个方向和朝向，可能支持多样视觉引导行为的灵活读取。

## Abstract
In mouse superior colliculus (SC), neurons are robustly tuned to motion direction and orientation, but it remains controversial whether these preferences are spatially organized, and how this organization relates to that found in the retinal input to the SC. We addressed these questions by combining two-photon calcium imaging of retinal boutons and SC neurons in superficial SC with Neuropixels recordings across the full depth of SC. We then asked how direction and orientation preferences depend on visual-field location and how tuning similarity among units depends on lateral and vertical distance in the SC. Retinal boutons were strongly tuned, and their preferences closely matched the retinal topographic organization of four motion directions and orientations previously described in the retina, rather than a global map in which a single direction or orientation dominates each visual-field location. With increasing depth, SC neurons progressively deviated from this organization. Superimposed on the identified topography, local clustering of tuning preferences in retinal boutons and SC neurons was weak and confined to very small spatial scales. Together, these results show that retinal inputs and neurons in mouse SC represent multiple directions and orientations for each location in the visual field, likely supporting flexible readout for diverse visually guided behaviors.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的结构化、深入的总结。

### 1. 论文的核心问题与整体含义

- **核心问题**：本文旨在解决小鼠上丘（SC）中方向和朝向偏好的空间组织这一长期争议。具体来说，研究者探究了SC神经元及其视网膜输入中的方向与朝向调谐是否存在全局地图（每个视野位置由单一偏好主导）、“盐和胡椒”式的随机分布，或是遵循一种新的组织形式。
- **研究背景与争议**：先前的研究结果相互矛盾，有的发现SC中存在明显的方向和朝向功能柱或全局地图，有的则报告几乎没有聚类。这些分歧表明，SC的功能组织可能取决于特定的实验条件，且可能超越“全局地图”与“盐和胡椒”的二分法。
- **整体含义**：该研究提出并验证了一种基于视网膜拓扑的“第三种组织形式”，即SC的视网膜输入为每个视野位置同时编码四种方向偏好和四种朝向偏好。这种局部混合调谐可能为支持多样化的视觉引导行为提供了灵活的信息读出基础，并随着SC环路逐级处理而发生转化。

### 2. 论文提出的方法论

本研究的技术核心在于结合多种高通量神经活动记录手段，并将记录的神经元的偏好与一个基于视网膜的几何预测模型进行定量比较。

- **核心思想**：将神经元的功能特性（方向/朝向偏好）与其在视觉空间中的精确位置（感受野）联系起来，检验其是否符合视网膜中已发现的特定拓扑规律，而不是寻找一个独立的SC图谱。
- **关键技术细节**：
    - **双光子钙成像**：
        - **视网膜Boutons（突触扣结）成像**：通过向眼球玻璃体注射表达突触靶向钙指示剂（AAV2-SyGCaMP6f）的病毒，特异性标记来自视网膜神经节细胞（RGC）的突触前末梢，实现对SC接收的直接视网膜输入的功能性记录。
        - **SC神经元成像**：直接向SC注射表达胞质钙指示剂（AAV1-GCaMP6f）的病毒来标记SC神经元。
    - **Neuropixels 电生理记录**：使用高密度硅探针，垂直贯穿SC全层进行记录，获取深部SC神经元的单细胞放电活动，弥补了双光子成像深度有限的缺点。
    - **视觉刺激与感受野映射**：
        - 使用覆盖大范围视野（如方位角 -135° 至 135°）的**移动正弦光栅**测量方向和朝向调谐。
        - 使用**稀疏噪声**（黑白棋盘格或圆点）精确映射每个单元的感受野（RF）在视觉空间中的位置。
    - **量化与分析模型**：
        - **调谐参数提取**：通过拟合一个包含时间核和独立试次幅值的模型来提取对每个刺激方向的反应，然后计算向量和。偏好方向和朝向为向量和的角度，选择性指数为其长度。
        - **视网膜几何预测模型**：基于 Sabbah et al. (2017) 和 Laniado et al. (2025) 的工作，该模型预测在任何给定的RF位置，RGC会偏好特定的4个运动方向（分别对齐身体/重力轴定义的四条经线）和4个朝向（分别对齐由两个极点定义的两套经纬线）。
        $$ \text{预测偏好} = f(\text{RF位置}, \text{几何模型}) $$
        - **模型匹配度分析**：对于每个记录单元，计算其实际偏好与最近预测向量之间的角度差。将此角度差的中位数与两种零假设分布（随机排列RF位置、均匀分布偏好）进行比较。

### 3. 实验设计

- **数据集与场景**：
    - **动物模型**：成年清醒、头部固定的C57Bl/6J品系及相关转基因品系小鼠。
    - **脑区**：聚焦于小鼠右侧SC。
    - **视网膜Boutons成像**：在8只小鼠的后部SC（代表左上象限外周视野）进行了17次记录，获得3,677个单元，其中2,391个对视觉刺激有反应。
    - **SC神经元成像**：在5只小鼠的后部SC进行了12次记录，获得4,769个单元，其中2,378个有反应。
    - **SC神经元电生理记录**：在7只小鼠的前部SC（代表前方中央视野）使用Neuropixels进行了23次记录，获得1,474个单细胞，其中1,120个有反应。
- **对比的基准与假设**：
    - **主要对比基准**：视网膜几何预测模型。
    - **零假设**：
        1.  **置换控制**：随机打乱RF位置，用以判断偏好与位置的关联是否显著高于随机水平。
        2.  **均匀分布控制**：从均匀分布中随机抽取偏好角度，用以判断数据是否比纯随机分布更集中。
    - **概念性对比**：对比“局部混合调谐”与“单一偏好全局地图”这两种组织模式。通过绘制平滑后的偏好地图、量化局部一致性、并分析成对调谐差异与距离的关系来进行。

### 4. 资源与算力

论文中未提及使用GPU进行模型训练，也未明确说明图像或数据分析所消耗的具体计算资源（如CPU型号、核心数、内存、分析总时长等）。

### 5. 实验数量与充分性

- **实验组数**：研究涉及 **3个主要实验组**：视网膜Boutons成像、SC神经元成像、SC神经元电生理记录。此外，在一个SC神经元子集中，还额外进行了移动光条和静态光栅的刺激作为对照实验。
- **实验充分性与客观性评估**：实验设计较为全面和客观。
    - **多模态交叉验证**：利用双光子成像的高空间分辨率和对特定结构（boutons vs 胞体）的靶向性，结合电生理的高时间分辨率和深层记录能力，从多个角度支撑同一结论，增强了可靠性。
    - **明确的对照**：所有关键的统计分析都包含了严格的置换检验等零假设模型，为判断结果的显著性提供了客观基准。
    - **偏差控制**：研究者系统排查了多种可能产生混淆的因素，包括眼球运动、感受野靠近监视器边缘、成像视野大小、以及不同刺激类型（光栅、光条）对结果的影响，并证实这些因素未能解释其主要发现。

### 6. 论文的主要结论与发现

1.  **强健的调谐与共同的偏差**：视网膜boutons和SC神经元都表现出对运动方向和朝向的强健调谐，并且对主方向（0°, 90°, 180°, 270°）存在共同的偏好。
2.  **视网膜拓扑在SC输入中被保留**：视网膜boutons的偏好与视网膜几何模型所预测的位置依赖性偏好高度一致，证实了SC的视网膜输入保留了4种方向和4种朝向的拓扑组织，**支持第三种组织形式**：每个视野位置同时存在多种偏好，而非单一偏好主导。
3.  **拓扑组织在SC内被逐级转化**：
    - SC浅层神经元对朝向偏好的拓扑对齐度弱于视网膜boutons，但方向对齐度依然存在。
    - 深层SC神经元的方向和朝向偏好与视网膜模型的预测几乎无一致性，表明SC内部环路对输入进行了显著的整合与转化。
4.  **局部聚类微弱**：无论是在视网膜boutons还是在SC神经元中，相似调谐偏好的局部聚类都非常弱，仅限于极小的空间尺度（约10-20微米），大部分区域表现出“局部混合”的特征，而非形成清晰的功能柱。
5.  **反对全局单一偏好地图**：全视野的平滑偏好地图中未发现系统性的梯度或同心圆模式，表明不存在一个稳定的、在特定视野区域由单一方向或朝向主导的全局地图。

### 7. 优点

- **整合性实验设计**：论文的一大亮点是将两种互补的记录技术（双光子成像和Neuropixels）应用于同一个科学问题，并直接比较了输入（boutons）和输出（神经元）以及浅层和深层的功能组织。
- **全新的分析视角**：跳出“地图 vs. 无地图”的二分法，引入了基于已知视网膜组织的“多重偏好拓扑”这一几何框架，为理解SC的组织提供了一个更精细、更具预测性的模型。
- **系统性的混淆因素排查**：作者非常细致地分析并排除了眼球运动、刺激边界效应、记录视野大小、刺激类型和不同动物品系等多种可能影响结论的变量，显著增强了结果的可信度。
- **定量化的逐级转化描述**：清晰地展示了从输入到输出的功能转化梯度，为理解SC内部的环路计算机制提供了重要线索。

### 8. 不足与局限

- **大脑皮层覆盖的影响**：双光子成像需要对SC上方的大脑皮层进行物理移除或植入透镜，这一手术过程可能损伤浅层SC或改变来自皮层的输入，从而影响所观察到的功能组织，尤其在活体成像的长期影响方面。
- **记录区域的局限性**：双光子成像主要集中于后部单眼区SC，而电生理记录则在前部双眼区。虽然这覆盖了不同区域，但同一技术未能覆盖SC全域，为直接进行区域间比较带来了变量。神经元调谐类型分布（图3 vs. 图7）的差异可能部分由此导致。
- **视觉刺激的简化**：研究主要使用移动光栅这一相对简单的刺激。自然场景下的复杂运动、不同对比度或运动速度可能会揭示出简单光栅未能调动的更丰富的功能组织结构。
- **个体差异问题**：作者在讨论中指出先前的研究显示出巨大的个体间差异，本文虽然量化了组间平均，但并未深入探讨或展示不同个体小鼠之间拓扑地图的一致性程度或变异范围。
- **行为相关性未验证**：论文在功能含义部分提出了该组织原则可能支持灵活行为读取的假设，但并未将神经活动与任何特定的视觉引导行为决策直接关联起来进行因果验证。

（完）
