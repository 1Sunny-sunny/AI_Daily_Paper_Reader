---
title: Predictive Neural Signals during Natural Mandarin Speech Comprehension
title_zh: 自然普通话言语理解中的预测性神经信号
authors: "Wang, Q., Szewczyk, J., Fazekas, J., Berlot, E., de Lange, F."
date: 2026-08-20
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.23.690006v2.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 言语理解中的预测神经信号涉及从时间神经活动模式中解码语言信息
tldr: 本研究利用汉语普通话和脑磁图（MEG）考察自然语音理解中预测加工是否同时涉及音素、亚音节、汉字、词等多个粒度。通过对34名母语者的神经活动进行线性回归建模，发现惊异度在亚音节、汉字和词层级同时调制响应，但缺少音素层独特效应，且声调惊异需与音系成分整合。研究揭示语言特定结构影响预测加工的实施，为跨语言比较提供了重要证据。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-11-23-690006-v2/fig-001.webp\", \"caption\": \"Figure 1. Experimental paradigm and analysis pipeline. Participants listened to a Chinese audiobook 124 while their brain activity was recorded using magnetoencephalography (MEG). The linguistic structure 125 of Mandarin is illustrated: words comprise one or more characters; each character maps to a single 126 syllable, which is composed of sub-syllabic units—an optional initial (consonant) and a final (vowel(s), 127 sometimes with a nasal consonant). The final also carries a lexical tone (indicated by numbers 1-4). 128 Sub-syllabic units are further composed of one or more phonemes. The audiobook transcript was 129 analyzed using a Chinese GPT-2 model to quantify contextual surprisal for each character. Temporal 130 response function (TRF) modelling was used to estimate the linear relationship between linguistic 131 features and MEG signal. As illustrated for character-level surprisal, the regressor was time-shifted 132\", \"page\": 6, \"index\": 1, \"width\": 963, \"height\": 308}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-11-23-690006-v2/fig-002.webp\", \"caption\": \"Figure 2. Onset effects at different linguistic levels. (A) Model performance when adding regressors 417 with different onset types. The upper panel shows cumulative prediction accuracy for models including 418 different onset regressors. The baseline model included acoustic regressors (envelope, spectrogram, 419 acoustic edges, and pitch). Each ‘+’ model included one onset regressor on top of the previous model. 420 For example, the + sub-syllabic model contains acoustics + phoneme onset + sub-syllabic onset. The 421 order of the added regressors was determined based on their individual contribution to model 422 performance. Dots with connecting lines represent individual participants (averaged over all temporal 423 sensors). The lower panel shows the incremental improvement in model performance (Δr) produced by 424 adding each new onset regressor, providing a clearer visualization of the contribution of each regressor. 425 For instance, the first violin indicates the difference of the +phoneme model compared to the baseline 426 model. (B) Temporal profiles of the global field power (GFP) of the beta coefficients from the full onset 427 model (i.e., the + character model), plotted separately for each onset type. Shaded area represents 428 standard deviation. (C) Topographic maps of beta coefficients at two peak time windows, shown 429 separately for phoneme, sub-syllabic, character, and word onsets. 430 431 Surprisal effect occurs at multiple levels of granularity 432\", \"page\": 20, \"index\": 2, \"width\": 1017, \"height\": 540}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-11-23-690006-v2/fig-003.webp\", \"caption\": \"Figure 3. Surprisal effects at different levels of granularity. (A) Model performance across different 490 surprisal regressor conditions. The upper panel shows cumulative prediction accuracy for models 491 including different surprisal regressors. The baseline (onset) model included acoustic features, all onset 492 regressors, and character frequency. Each ‘+’ model included one surprisal regressor on top of the 493 previous model, for instance, the + character model contains baseline (onset) + sub-syllabic surprisal 494 + character surprisal. The order of the added regressors is determined based on their individual 495 contribution to model performance. The lower panel shows the incremental improvement in model 496 performance (Δr) produced by adding each new surprisal regressor, providing a clearer visualization of 497 the contribution of each regressor. (B) Temporal profiles of the global field power (GFP) of the beta 498 coefficients from the full surprisal model (i.e., + word model), plotted separately for each surprisal 499 regressor. Shaded area represents standard deviation. (C) Topographic maps of beta coefficients in the 500 200-400 ms time window, shown separately for phoneme, sub-syllabic, character, and word surprisal. 501\", \"page\": 23, \"index\": 3, \"width\": 1019, \"height\": 447}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-11-23-690006-v2/fig-004.webp\", \"caption\": \"Figure 4. Surprisal effects for tone and rhyme. (A) Illustration of probability estimation for 531 different phonological components. GPT-2 generated predictions for upcoming characters with 532 varying probabilities; the target character is marked in red. Each character corresponds to a syllable 533 comprising an initial (green), rhyme (dark purple), and tone (light purple). Initial probability was 534 computed by summing the probabilities of all characters sharing the same initial (e.g., all ‘ch’ 535 characters). Rhyme and tone probabilities were calculated by summing probabilities of characters that 536 share either both the same initial and rhyme (e.g. ch–i) or the same initial and tone (e.g. ch–1), then 537 normalized by the initial probability. Integrated probability was computed by summing probabilities 538 of characters that match the target in initial, rhyme, and tone (e.g. ch–i1), normalized by the 539 probability of the initial. (B) Model performance across different surprisal regressor conditions. The 540 tone + rhyme model contained tone and rhyme surprisal, whereas + tone x rhyme model included tone 541 surprisal, rhyme surprisal and integrated tone and rhyme surprisal. Shaded area represents standard 542 deviation. (C) Temporal profiles of the global field power (GFP) of the beta coefficients from the full 543 model (i.e., the + tone x rhyme model), plotted separately for each surprisal type. (D) Topographic 544 maps of beta coefficients in different time windows, shown separately for tone, rhyme and integrated 545 surprisal. 546\", \"page\": 25, \"index\": 4, \"width\": 1019, \"height\": 394}]"
motivation: 已有研究多基于印欧语言，预测加工是否在音节、短语等层级同时发生尚不清楚，而汉语独特的亚音节词汇约束可能改变预测权重的分配。
method: 34名普通话母语者聆听自然有声读物并记录脑磁图，利用线性回归模型分析各语言层级惊异度对神经活动的调制。
result: 惊异度在亚音节、汉字和词层级同时调制脑活动，但未发现音素层的独特效应，声调惊异仅在与其音系成分整合时产生调制。
conclusion: 汉语语音理解中的预测加工同时跨多个（但非所有）语言粒度层级运作，其实施受语言特定结构特性的塑造。
---

## 摘要
语言理解需要将言语持续转化为语言单位的层级结构，从音位到音节再到词汇。由于言语展开速度很快，听者被认为会预测即将出现的内容以跟上节奏。先前研究已为自然聆听中在多个语言层级上运作的预测过程提供了经验证据，包括词汇和音位层级。然而，预测是否也在其他层级（如音节和短语表征）上同时运作，仍不清楚。在此，我们使用汉语普通话来考察自然言语理解中跨多个语言粒度层级的预测加工的神经特征。普通话包含四个表征层级：音位、亚音节、汉字和词，其词汇身份在很大程度上受限于亚音节层级，这可能会在不同语言表征之间重新分配预测权重。我们记录了34名以普通话为母语的被试（21名女性）在聆听自然有声书时的脑磁图（MEG）数据，并应用线性回归模型考察语言特征如何调节神经活动。我们发现，听者的大脑活动将言语切分为层级性单元，且惊讶度同时调节了亚音节、汉字和词层级上的反应。然而，与印欧语系语言中的发现不同，我们未在最低的音位层级观察到独特的惊讶度效应。此外，普通话声调的惊讶度仅在与音系成分整合时才调节大脑活动。这些发现表明，普通话言语理解中的预测加工在多个（尽管不一定所有）语言粒度层级上同时运作，其实现方式受到语言特定结构特性的塑造。

## Abstract
Language comprehension requires the continuous transformation of speech into a hierarchy of linguistic units, from phonemes to syllables to words. Because speech unfolds rapidly, listeners are thought to predict upcoming content to keep pace. Previous research has provided empirical evidence for predictive processes operating at multiple linguistic levels during naturalistic listening, including words and phonemes. However, it remains unclear whether prediction also operates concurrently at other levels, such as syllabic and phrasal representation. Here we use Mandarin Chinese to examine the neural signatures of predictive processing across multiple levels of linguistic granularity during natural speech comprehension. Mandarin comprises four representational levels: phoneme, sub-syllabic, character and word, and its lexical identity is largely constrained at the sub-syllabic level, potentially redistributing predictive weight across linguistic representations. We recorded magnetoencephalography (MEG) data while 34 native Mandarin speakers (21 females) listened to a naturalistic audiobook and applied linear regression modeling to examine how linguistic features modulated neural activity. We found that the brain activity of listeners segmented speech into hierarchical units, and that surprisal modulated responses simultaneously across sub-syllabic, character and word levels. In contrast to findings from Indo-European languages, however, we did not observe unique surprisal effects at the lowest, phonemic level. Furthermore, the surprisal of lexical tone in Mandarin modulated brain activity only when integrated with its phonological components. These findings suggest that predictive processing during Mandarin speech comprehension operates concurrently across multiple (though not necessarily all) levels of linguistic granularity, with its implementation shaped by language-specific structural properties.

---

## 论文详细总结（自动生成）

# 论文总结：自然普通话言语理解中的预测性神经信号

## 1. 核心问题与整体含义

- **研究动机与背景**  
  语言理解需要听者将快速展开的语音流实时切分为多层语言单元，如音位、音节、词和短语。由于语速很快，预测加工被认为是理解的关键机制。已有研究主要在印欧语系语言中发现，自然聆听时预测加工可以在**词汇层**和**音位层**同时发生。

- **尚未解决的关键问题**  
  目前尚不清楚预测加工是否也在**音节层、短语层**等其他语言粒度上同时运作。尤其是汉语普通话具有独特的语言结构：词由汉字组成，每个汉字对应一个音节，音节下又分为声母、韵母和声调等**亚音节单元**。这种结构可能使听者将预测权重更多地放在亚音节层，而不是音位层。

- **整体含义**  
  本研究试图利用汉语普通话的层级特性，考察自然言语理解中预测加工是否跨多个粒度层级同时进行，并揭示语言特定结构如何塑造预测加工的实现方式。其意义在于：如果预测加工在不同语言中表现出不同的层级权重，那么“预测是通用认知机制”这一观点就需要结合语言类型学进行修正。

## 2. 方法论

- **核心思想**  
  利用**自然有声书聆听范式**，结合**脑磁图（MEG）**和**线性回归建模**，考察不同语言层级特征如何调节神经活动。核心预测变量是各层级单元的**惊异度（surprisal）**，即该单元在当前上下文中出现的意外程度。

- **关键技术细节**
  - **语言特征量化**：使用**中文 GPT-2 模型**对有声书文本进行逐字概率估计，为每个汉字计算上下文惊异度。
  - **语言层级划分**：将普通话划分为四个表征层级：**音位（phoneme）**、**亚音节（sub-syllabic）**、**汉字（character）**和**词（word）**。
  - **时间响应函数（TRF）建模**：采用线性回归估计语言特征与 MEG 信号之间的关系。回归器在不同时间偏移上构建，以捕捉神经响应的时程变化。
  - **声学基线控制**：基线模型包含声学包络、频谱、声学边缘和音高特征，以排除低层声学加工的影响。
  - **模型比较指标**：通过预测准确率和增量预测准确率 $\Delta r$ 来评估每个语言层级回归器的贡献。

- **分析流程**
  1. 构建声学基线模型。
  2. 在基线模型上逐步添加不同层级的 **onset 回归器**（音位、亚音节、汉字、词），观察模型性能提升。
  3. 在 onset 基线模型基础上添加**字符频率**，再逐步加入各层级的 **surprisal 回归器**，考察惊讶度的增量贡献。
  4. 提取各回归器的 beta 系数，计算**全局场功率（GFP）**的时间剖面和地形图。
  5. 进一步对**声调、韵母及二者的整合惊异度**进行专门分析，构建如下概率条件：
     - tone（声调）条件：目标声调与上下文预测之间的惊异度。
     - rhyme（韵母）条件：目标韵母与上下文预测之间的惊异度。
     - integrated（整合）条件：声调与韵母共同匹配时的惊异度。

## 3. 实验设计

- **被试与数据采集场景**
  - **被试**：34 名以普通话为母语的被试，其中 21 名为女性。
  - **任务**：被试聆听一段自然有声书。
  - **神经记录**：使用脑磁图（MEG）全程记录脑活动。
  - **材料**：汉语普通话有声书及其文本转写。

- **Baseline 与比较方法**
  - **声学基线模型**：包含包络、频谱、声学边缘和音高四个声学回归器。
  - **onset 模型比较**：在声学基线之上，逐步加入音位 onset、亚音节 onset、汉字 onset、词 onset，比较不同语言单元边界对神经响应的调制。
  - **surprisal 模型比较**：在 onset 基线和字符频率基础上，逐步加入亚音节惊异度、汉字惊异度、词惊异度、音位惊异度，观察哪些层级的惊异度能可靠提升模型预测。
  - **音系成分模型**：比较 tone、rhyme 模型与加入整合 tone×rhyme 惊异度的模型，考察声调与韵母的交互/整合效应。

- **Benchmark 设置**  
  没有使用传统的外部 benchmark，而是采用**内部模型比较**：以声学基线为基准，通过增量 $\Delta r$ 衡量各语言特征的神经解释力。这在本类自然言语神经成像研究中是常见做法。

## 4. 资源与算力

- 论文提供的文本中**未明确报告** GPU 型号、数量、训练时长或具体算力消耗。
- 虽然使用了中文 GPT-2 模型进行语言特征提取，但未说明该模型是自己训练、微调还是直接使用预训练权重，也未说明推理阶段的硬件环境。
- 因此，无法评估该研究的算力需求；在算力披露方面存在明显不足。

## 5. 实验数量与充分性

- **主要实验组数**
  根据图表和文字描述，研究可大致分为三组核心分析：
  1. **onset 层级效应分析**：比较声学基线、+音位、+亚音节、+汉字、+词等多层模型。
  2. **多粒度 surprisal 效应分析**：比较 onset 基线+字符频率、+亚音节惊异度、+汉字惊异度、+词惊异度等模型。
  3. **声调与韵母音系成分分析**：比较 tone、rhyme、integrated tone×rhyme 等条件。

- **多层级验证**
  每种分析不仅报告了模型性能，还提供了 beta 系数的 GFP 时间剖面和地形图。例如，onset 分析给出了音位、亚音节、汉字和词 onset 的两个峰值时间窗地形图；surprisal 分析给出了 200–400 ms 时间窗的地形图；声调/韵母分析给出了不同时间窗的地形图。

- **充分性与客观性评价**
  - **优点**：实验设计系统，涵盖了多个语言层级和多类语言特征；样本量在 MEG 研究中属于中等偏大；模型比较采用逐步加入回归器的方式，能够区分各层级的增量贡献。
  - **潜在问题**：
    - 实验主要基于**单一有声书材料**，缺少跨语料验证，可能受到特定文本特性的影响。
    - 模型中加入回归器的顺序是**根据单个回归器对模型性能的贡献确定**的，这可能引入顺序偏差。
    - 论文未明确报告**统计显著性检验**的细节（如多重比较校正、效应量置信区间等）。
    - 研究只包含普通话母语者，未直接与印欧语言数据做统计比较，所得“与印欧语言不同”的结论依赖于间接文献对照。

## 6. 主要结论与发现

- 听者的大脑活动能够将连续言语**切分为层级性语言单元**。
- **惊异度同时调制亚音节、汉字和词层级的神经响应**，表明预测加工在多个语言粒度层级上并行运作。
- **未发现音位层的独特惊异度效应**，这与印欧语系语言中的发现不同，提示普通话听者可能不将音位作为独立的预测层级。
- **普通话声调的惊异度**只有在与其音系成分（韵母）整合时才调制神经活动；单独的声调或韵母预测信息不足以产生显著效应。
- 总体而言，预测加工在普通话言语理解中跨多个语言层级同时运作，但并非覆盖所有层级，其实现方式受到语言特定结构特性的塑造。

## 7. 优点

- **语言选择具有理论针对性**：汉语普通话的音节、亚音节和汉字层级具有明确的边界和独特的词汇约束，非常适合研究预测加工在多粒度层级的分配。
- **自然聆听范式**：采用自然有声书而非人为设计的刺激，生态效度较高，能够揭示真实语言理解中的神经过程。
- **多层回归器系统比较**：研究不仅考察词汇和音位层，还引入了亚音节层、汉字层以及声调/韵母的整合分析，分析粒度细致。
- **声学基线控制**：模型中纳入多种声学特征，有助于将语言层面的效应与低层声学效应分离。
- **神经信号时空分析**：同时报告 GFP 时间剖面和地形图，可以观察不同语言特征的时间动态和空间分布。

## 8. 不足与局限

- **算力与可复现性披露不足**：未报告 GPT-2 模型的具体版本、计算环境和训练/推理细节，降低了方法可复现性。
- **材料单一性**：仅使用一段有声书文本，语言特征分布可能受文本类型和叙事风格影响，结论未必能推广到其他语体。
- **语言层级覆盖不完整**：虽然讨论了音位、亚音节、汉字和词，但未系统考察**短语/句法层级的预测效应**，而这正是引言中提到的开放问题之一。
- **缺少跨语言直接比较**：研究仅基于普通话数据，未直接比较英语或其他印欧语言被试在同一范式下的表现，因此“与印欧语言不同”的结论仍属间接推断。
- **统计检验细节不足**：文中未清晰展示模型比较的统计方法、多重比较校正和效应稳定性，可能影响结果的可靠性判断。
- **音位效应的缺失解释**：未充分排除音位层缺乏独特效应的替代解释，例如音位信息可能被亚音节或声学特征吸收，而非真实不存在预测加工。
- **语言模型偏差**：中文 GPT-2 对普通话的建模可能不如专门的中文语言模型精确，惊异度估计的准确性会影响神经模型的结果。

（完）
