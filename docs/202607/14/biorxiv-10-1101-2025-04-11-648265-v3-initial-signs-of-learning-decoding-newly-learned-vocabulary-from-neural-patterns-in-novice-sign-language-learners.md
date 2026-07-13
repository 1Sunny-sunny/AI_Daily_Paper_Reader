---
title: "Initial signs of learning: Decoding newly-learned vocabulary from neural patterns in novice sign language learners"
title_zh: 学习的最初迹象：从新手手语学习者的神经模式解码新学词汇
authors: "Hillis, M. E., Kraemer, D. J. M."
date: 2026-07-13
pdf: "https://www.biorxiv.org/content/10.1101/2025.04.11.648265v3.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 从手语学习者的神经模式解码新学词汇
tldr: 本研究探讨新手手语学习者（听力正常的非手语者）在学习第一课后如何在大脑中表征新语言的语义。通过fMRI分析，发现群体神经活动模式与所学手语词的语义特征相关，且个体对新词的理解程度可通过神经表征与已知英语对应词的相似性解码。结果表明，早期学习使新获取的手语名词表征向熟悉的英语表征靠拢，涉及广泛分布的脑区（包括语言区和右顶叶），揭示了跨语言、跨模态语义整合的初期机制。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-04-11-648265-v3/fig-001.webp\", \"caption\": \"Table 1. Linear Mixed Model Results for ASL RSA Regions Model β CI Marginal R2 p-adj\", \"page\": 13, \"index\": 1, \"width\": 945, \"height\": 379}]"
motivation: 探索新手二语学习者在初次接触后如何将新语言的语义信息融入已有知识网络，尤其关注感官模态差异巨大的手语。
method: 使用功能性磁共振成像（fMRI）记录40名听力正常非手语者在首次ASL课程后的脑活动，比较已学与未学手语词的神经表征。
result: 群体神经模式与已学手语词的语义特征相关，且个体层面的理解程度可通过跨语言（ASL-英语）神经相似性预测，相关脑区包括perisylvian语言区和右顶叶。
conclusion: 新学手语词汇的神经表征快速向母语对应词靠拢，分布式脑区共同支持跨语言、跨模态的语义整合，即便在学习的早期阶段。
---

## 摘要
新手语言学习者如何在他们的新语言中表示语义信息？双语者对不同语言的神经表征是截然不同的还是重叠的，这一点已有充分研究，但对于新知识如何在习得的最初阶段整合到已建立的表征网络中的了解较少。除了本身就是一个未被充分研究的案例外，手语还允许我们在目标语言的感觉特征与学习者先前经验最大程度不相似的情况下研究语言学习。利用40名听力正常的非手语者在上第一堂美国手语（ASL）课后的功能磁共振成像数据，我们表明，群体层面的神经活动模式与已学过（但未学过的）ASL手语的语义特征相关。此外，语义等价名词之间的跨语言神经相似性反映了个体对ASL的理解水平。在表示ASL内部语义关系的脑区中，项目水平的理解可以被解码，这表明早期学习使新获得的ASL名词的神经表征与熟知的英语对应词的神经表征变得更加相似。这些结果证明了分布式神经区域（包括外侧裂周围语言区以及右侧顶叶区域）在新手跨语言和跨模态地表征语义内容中的作用。

## Abstract
How do novice language learners represent semantic information in their new language? Whether bilinguals' neural representations of different languages are distinct or overlapping has been well-studied, but less is known about how new knowledge is integrated into established representational networks at the earliest stages of acquisition. In addition to being an understudied case in their own right, signed languages allow the study of language learning when the sensory features of the target language are maximally dissimilar from the learners' prior experience. Using fMRI data from 40 hearing non-signers following their first lesson in American Sign Language (ASL), we show that group-level patterns of neural representation correlate with semantic features for studied (but not unstudied) ASL signs. Furthermore, cross-language neural similarity between semantically equivalent nouns reflects individual-level comprehension of ASL. Item-level comprehension was decodable in regions that represent semantic relationships within ASL, suggesting that representations of newly acquired ASL nouns become more similar to well-known English counterparts as a result of early-stage learning. These results demonstrate the role of distributed neural regions, including perisylvian language areas as well as right parietal areas, in representing semantic content across language and modality in novice learners.

---

## 论文详细总结（自动生成）

## 论文核心问题与整体含义
- **研究动机**：探究新手外语学习者（尤其是成人）在初次接触一门新语言后，如何在神经层面表征其语义信息。现有研究多关注熟练双语者，对极其早期的学习阶段，特别是当新语言的感觉模态（如手语）与母语（口语）截然不同时，新知识如何整合到已有的概念网络中缺乏了解。
- **整体含义**：本研究旨在揭示，在仅仅一节手语课（约 45 分钟）后，听力正常的非手语者大脑中已学手语词汇的神经表征是否已与对应的母语（英语）表征产生共享或相似。这类跨语言神经相似性是否能够预测个体的实际学习成效（回忆准确率），从而为“新手利用母语作为支架辅助新语言学习”的假说提供神经层面的直接证据。

## 方法论
- **核心思想**：通过功能磁共振成像（fMRI）记录被试观看手语和英语名词视频时的脑活动，先利用表征相似性分析（RSA）定位对单一语言内部语义关系敏感的脑区，再在这些区域内计算同一名词跨语言（手语-英语）的神经模式相似性，最后用线性混合效应模型检验该相似性是否能预测词汇是否被学习过以及个体的回忆成绩。
- **关键技术细节与算法流程**：
  1. **神经活动估计**：使用一般线性模型（GLM）为每个刺激视频逐试次估计 beta 值，并对跨 run 项进行项目级固定效应合并，得到每个项目在每种语言下的神经活动向量。
  2. **神经不相似矩阵构建**：在被试个体层面，在每个 Schaefer 500 脑区分别计算项目间的相关距离（1 - 相关系数），得到每个脑区的神经不相似矩阵（DM）。
  3. **语义与形式模型**：
     - 语义模型：基于预训练 Word2Vec 英文维基百科嵌入，计算每对名词的余弦不相似度，形成语义 DM。
     - 形式模型：为排除音韵/形式特征的混淆，分别为 ASL（手形、位置、运动等特征）和英语（Metaphone 音韵编码的 Levenshtein 距离）构建形式 DM。
     - 在 RSA 前，通过线性回归将语义 DM 对相应的形式 DM 进行正交化，得到纯净的语义距离。
  4. **脑区选择（组水平 RSA）**：将当前 40 名被试数据与先前 10 名经过充分训练、学习达到天花板水平的被试数据合并（共 50 人），在每个脑区计算正交化后语义模型与神经 DM 的 Spearman 秩相关（经 Fisher z 变换），并与随机置换产生的零分布比较。经符号翻转置换检验校正后，选出显著相关的脑区（ASL 任务保留 54 个脑区，英语任务保留 24 个）。
  5. **层次聚类与神经分数**：对入选脑区，依据其跨语言（每对手语-英语等价词）神经相似性的模式进行层次聚类，使用加速度法确定最佳簇数为 4。对每个被试、每个词汇、每个簇，计算簇内所有脑区跨语言相似性的平均值，作为“神经分数”。
  6. **混合效应建模**：使用逻辑（预测是否学过）和高斯（预测回忆分数）线性混合效应模型，以神经分数为固定效应，被试、项目、簇为随机效应（含随机截距），采用 Satterthwaite 近似估计自由度和 p 值，并对簇级分析进行 FDR 校正。

## 实验设计
- **数据集与被试**：40 名听力正常的英语母语成年志愿者（平均 20.3 岁，28 名女性），均无任何手语经验。
- **学习材料与分组**：从 ASL-LEX 数据库中挑选 64 个低透明度的具体名词，分为两个列表（各 32 个）。将被试随机分为两组，各学习一个列表的 32 个词，另一列表作为未学对照。采用远程在线课程，约 45 分钟，包括观看视频、模仿、选择题和录像练习。
- **fMRI 任务**：在扫描中进行 ASL 和英语两个 run。ASL run 中呈现 24 个名词（12 个已学，12 个未学，来自上述列表），每个视频呈现 6 次；英语 run 中呈现对应的英语名词视听片段。英语 run 放在最后以避免提前泄露词汇含义。扫描中穿插 10% 的注意力检查试次。
- **行为测量**：在三个时间点（学习当天、扫描前、三周后）进行自由回忆测验，要求写出每个手语词的英语翻译。每个项目的最终回忆分数取三次测验的平均正确率。
- **对比基准**：研究未采用多种算法直接对比，主要的对比是**已学词 vs. 未学词**（内部对照），以及**跨语言神经相似性在 ASL 语义敏感脑区 vs. 英语语义敏感脑区**的预测效力差异。同时，研究结果与先前熟练双语手语者的发现（如 Evans 等，2019）进行了理论对比。

## 资源与算力
- 论文中未提及任何 GPU 型号、数量或具体训练时长。实验采用 3 特斯拉西门子 PRISMA 扫描仪进行数据采集，预处理使用 fMRIPrep，后续分析使用 Nilearn、Pymer4 等 Python 工具。由于是传统的 fMRI 分析，未涉及深度学习模型的训练，故无算力消耗说明。

## 实验数量与充分性
- **主要实验组次**：
  - 基于 ASL 语义敏感脑区（54 个）的整体模型和 4 个簇级模型，分别预测“是否学过”（逻辑回归）和“回忆分数”（线性回归）。
  - 基于英语语义敏感脑区（24 个）的同样两套模型。
  - 辅助分析：组水平 RSA 的置换检验、脑区选择用到了额外的 10 人数据作为“学习基准”。
- **实验充分性与公平性**：
  - 实验设计严谨，采用了被试内已学-未学对照、列表抵消、透明度和形式特征控制、交叉验证性质的脑区选择（部分数据用于脑区定义，部分用于假设检验）。
  - 统计方法先进，混合效应模型能有效控制被试、项目、脑区簇的随机变异，并进行多重比较校正。
  - 总共生成 4（ASL 簇 + 英语簇） × 2（任务类型）= 8 组主要对比，加上整体模型，共约 10 余组分析，覆盖了主要假设，规模尚可。但属于单次研究，未进行独立样本复现，且样本量中等（N=40），未来仍需更大样本验证。

## 主要结论与发现
1. **跨语言相似性反映学习**：在手语语义敏感脑区中，单个手语词与其英语等价词之间的神经表征相似性（神经分数），可以有效预测该手语词是否被被试学习过，并且对于已学词，还能预测个体准确回忆其含义的几率。
2. **脑区特异性**：这种学习相关的预测效应在由 ASL 语义敏感区定义的脑网络中最为显著（包含多个簇），尤其在左侧顶内沟、角回、楔前叶构成的簇中效应最强。而由英语语义敏感区定义的脑网络预测力较弱，且无法预测回忆表现，暗示新手早期语义整合更多地借助了正在形成的手语加工相关脑区。
3. **极早期学习痕迹**：仅约 45 分钟的训练就能引起特定脑区中跨语言神经表征的系统性变化，且这种变化与行为学习成效直接挂钩。
4. **分布式网络参与**：结果支持包括外侧裂周围经典语言区（如缘上回、颞上沟）和右顶叶在内的分布式脑网络共同支持新手跨语言、跨模态的语义整合，并非局限于某个单一区域。

## 优点
- **选题新颖**：聚焦于极其早期的手语学习阶段，填补了二语习得神经机制研究的时间空白。
- **实验控制严密**：通过未学词对照、列表抵消、手语透明度预筛选、形式特征正交化等方法，有效排除了多项潜在混淆。
- **方法论先进**：将 RSA、层次聚类与混合效应模型相结合，从群体脑区选择到个体行为预测，实现了多层次的“神经分数”建模，分析思路清晰且说服力较强。
- **结论具启发意义**：首次在项目水平上证明极早期跨语言神经相似性与个体学习结果的对应关系，为“母语支架”理论提供了直接的多变量神经证据。

## 不足与局限
- **样本与可推广性**：样本量 40 人，均为年轻成年人且来自单一学术机构，结论在外推至其他年龄、教育背景或语言组合时需谨慎。
- **学习深度与生态效度**：学习内容为 32 个孤立的名词，缺乏句法、语境和真实交际互动，其结果可能无法直接推广至更复杂的自然语言学习场景。
- **因果推断限制**：研究为观察性设计，仅能揭示神经相似性与学习表现之间的相关性，无法证实神经相似性的增长是导致学习成功的直接原因。
- **时间动态缺失**：仅有一个扫描时间点，无法刻画学习过程中神经表征变化的动态轨迹，也无法判断这些早期变化是暂时性还是长期稳定的。
- **技术依赖**：脑区选择依赖于特定皮层图谱、语义模型和额外样本，不同预处理和分析参数可能对结果产生一定影响。

（完）
