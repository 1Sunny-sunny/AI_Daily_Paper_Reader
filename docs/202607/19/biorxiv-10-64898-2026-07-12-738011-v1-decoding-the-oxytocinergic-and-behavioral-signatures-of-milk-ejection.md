---
title: Decoding the oxytocinergic and behavioral signatures of milk ejection
title_zh: 解码泌乳的催产素能和行为标志
authors: "Xiao, W., Zheng, Q., Wang, Y., Yuan, Y., Chen, Y., Zheng, T., Gao, Y., Song, B., Zhang, B., Qiu, L., Zeng, L., Huan, M., Brown, C. H., Duan, S., Pan, G., Gao, Z."
date: 2026-07-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.12.738011v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 解码催产素神经元活动和射乳行为特征
tldr: 排乳对哺乳和生殖健康至关重要，但其神经机制和行为解码仍具挑战。本研究结合钙成像和乳腺内压记录，揭示催产素神经元活动与排乳的时间联系，开发机器学习框架ME Decoder，定义母幼互动行为特征ADPI。应用该框架发现，阻断催产素受体后排乳减少但神经元活动未变，提供了可推广的分析方法。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-001.webp\", \"caption\": \"\", \"page\": 39, \"index\": 1, \"width\": 3087, \"height\": 2815}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-002.webp\", \"caption\": \"\", \"page\": 40, \"index\": 2, \"width\": 3723, \"height\": 2371}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-003.webp\", \"caption\": \"\", \"page\": 41, \"index\": 3, \"width\": 3210, \"height\": 2621}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-004.webp\", \"caption\": \"\", \"page\": 42, \"index\": 4, \"width\": 3207, \"height\": 2483}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-005.webp\", \"caption\": \"\", \"page\": 43, \"index\": 5, \"width\": 3460, \"height\": 3286}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-006.webp\", \"caption\": \"\", \"page\": 44, \"index\": 6, \"width\": 3302, \"height\": 3232}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-007.webp\", \"caption\": \"\", \"page\": 45, \"index\": 7, \"width\": 3162, \"height\": 3098}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-12-738011-v1/fig-008.webp\", \"caption\": \"\", \"page\": 46, \"index\": 8, \"width\": 3346, \"height\": 2320}]"
motivation: 排乳行为的催产素能神经机制尚不明确，需要解码其行为与神经活动特征。
method: 结合体内钙成像与乳腺内压记录，开发监督机器学习框架ME Decoder，关联神经元活动与母幼互动。
result: 发现催产素神经元偶发性活动与排乳同步，定义了行为特征ADPI；阻断催产素受体仅减少排乳而不影响神经元活动。
conclusion: 研究揭示了排乳的催产素能和行为特征，为母乳喂养研究提供了新的分析工具。
---

## 摘要
催产素介导的泌乳（ME）对有效母乳喂养和生殖健康至关重要，然而从行为上解码并揭示泌乳的神经机制仍然具有挑战性。在此，我们结合体内钙成像和乳腺内压记录，揭示了清醒哺乳大鼠中催产素神经元的阶段性活动与泌乳之间的时间联系。利用母鼠和幼崽的关联和行为反应，我们开发了一个监督机器学习框架（ME解码器），以实现对泌乳的自动化分析。受其可解释特征的启发，我们定义了活动耦合的母幼互动（ADPI），表现为母鼠高度驼背随后幼崽踩踏和伸展，作为泌乳的行为标志。通过ME解码器和ADPI分析，我们在全身阻断催产素受体后检测到泌乳减少但催产素能神经元活动未受影响。我们的研究揭示了泌乳的催产素能和行为标志，并为进一步研究提供了一种普适的方法。

## Abstract
Oxytocin-mediated milk ejection (ME) is pivotal to effective breastfeeding and productive health, yet behaviorally decoding and revealing neural mechanisms of ME remains challenging. Here, we combined in vivo calcium imaging and intramammary pressure recording to uncover the temporal connections between episodic activity of oxytocin neurons and ME in conscious lactating rats. Leveraging the association and behavioral responses in dam and pup, we developed a supervised machine learning framework (ME Decoder) to enable automated analyses of ME. Inspired by its interpretable features, we defined the activity-coupled dam-pup interactions (ADPI), manifested by high kyphosis of the dam followed by pup treading and stretch, as the behavioral signatures of ME. By ME Decoder and ADPI analyses, we detected reduced ME but unaffected activity of oxytocinergic neurons after systemic blockade of oxytocin receptor. Our study uncovers the oxytocinergic and behavioral signatures of ME and provides a generalizable approach for further investigation.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
*   **核心问题**：哺乳过程中的排乳是一个由催产素脉冲式释放驱动的神经内分泌反射，其神经机制与行为表现之间的精确对应关系尚不清晰。如何从行为学角度解码排乳事件，并建立一套自动化、非侵入性的检测方法，是该领域的一个重大挑战。
*   **整体含义**：本研究旨在揭示哺乳期大鼠排乳过程中的**催产素能神经活动特征**和**母幼互动的行为特征**，并开发一个通用的机器学习框架，以实现对排乳事件的自动化、精准识别与量化分析。这为研究哺乳相关的生理、心理及病理过程提供了新的工具和视角。

### 2. 方法论
论文提出了一套整合神经记录、行为分析与深度学习框架的研究方法。

*   **核心思想**：通过同步记录催产素神经元的活动与排乳的生理指标（乳腺内压），建立起神经活动与排乳事件的精确时间联系。随后，利用该联系作为“金标准”，训练一个监督学习模型，从行为视频中自动识别排乳事件，并从中解析出可解释的行为学标志。
*   **关键技术细节**：
    *   **神经活动记录**：使用光纤光度测量技术，在清醒哺乳期大鼠的视上核中记录催产素神经元群体的钙信号。
    *   **生理指标验证**：在麻醉大鼠中，同步记录催产素神经元钙信号和乳腺内压，证实钙波与排乳事件的滞后时间关系（~15秒）。
    *   **深度学习框架 (ME解码器)**：
        *   **结构**：一个两阶段的监督学习框架。
        *   **第一阶段 - ME检测器**：由**时序移位模块**和**边界匹配网络**组成。TSM从视频帧中提取动态时空特征，BMN则基于这些特征定位候选排乳片段的起止时间。
        *   **第二阶段 - ME精炼器**：包含另一个TSM，作为分类器对第一阶段提出的候选片段进行筛选，以减少误报。
        *   **训练数据**：正样本为钙波开始后约10秒起的9秒视频片段，负样本为其余时段的视频片段。
*   **关键算法流程**：
    *   输入一段哺乳视频。
    *   `ME Detector (TSM+BMN)`：提取每帧的行为表征，并生成候选排乳片段。
    *   `ME Refiner (TSM)`：对候选片段进行分类，判断是否为真正的排乳片段。
    *   输出：视频中自动识别的排乳事件片段。

### 3. 实验设计
*   **数据集/场景**：
    *   **动物模型**：Sprague Dawley和OXT-Cre转基因哺乳期大鼠（产后第5-18天）。
    *   **行为场景**：母鼠与幼崽在测试箱内自由哺乳，由顶部摄像头记录视频。
    *   **训练/验证/测试**：视频数据被划分为训练集、验证集和测试集。测试集1包含9.58小时视频中的87次排乳事件。
*   **基准比较**：
    *   **金标准 (Ground Truth)**：与催产素神经元钙波时间耦合的排乳事件。
    *   **方法对比**
        *   **骨架法 (DeepLabCut)**：尝试追踪母鼠关键点，但未能发现与排乳相关的位移或角度变化，验证了其局限性。
        *   **手动行为学评分 (ADPI)**：由经验丰富和初次接触的实验者分别基于定义的行为序列（ADPI）进行人工识别，其结果作为高精度基准，并与`ME解码器`和`GT-ME`进行比较。
*   **对比的干扰条件**：
    *   **清醒 vs. 麻醉**：比较两种状态下催产素神经元的反应与排乳时程。
    *   **生理盐水 vs. 催产素受体拮抗剂 (L-368,899)**：通过腹腔注射阻断外周催产素受体，验证`ME解码器`和`ADPI分析法`能否检测到排乳事件数量的减少，并观察对中枢催产素神经元活动的影响。

### 4. 资源与算力
论文正文和方法部分**未明确提及**所使用的GPU型号、数量或具体的模型训练时长。

### 5. 实验数量与充分性
*   **实验组别与数量**：论文设计了多组实验，数量较充分。
    *   **基础活动记录**：清醒哺乳期大鼠的钙信号记录（n=8只母鼠）。
    *   **麻醉状态对比**：同步记录钙信号和乳腺内压（n=5只母鼠），并进行清醒与麻醉状态的对比分析。
    *   **模型验证**：在训练集、验证集上优化后，在一个独立的测试集（7个视频，含87次排乳事件）上进行性能评估。
    *   **可解释性分析**：通过Grad-CAM++可视化、区域贡献度分析（n=7个视频）和精细行为序列分析（n=6个视频，77次试验）来解析模型决策。
    *   **功能验证与干扰实验**：
        *   阻断外周催产素受体，并用`ME解码器`和`ADPI`检测排乳变化（n=9只母鼠）。
        *   在OXT-Cre大鼠上重复阻断实验，同步记录催产素神经元活动（n=5只母鼠）。
*   **充分性与客观性**：
    *   **充分性**：实验设计层层递进，从确立金标准，到模型开发验证，再到应用模型进行药理学干预下的现象发现，逻辑链条完整。
    *   **客观性与公平性**：关键的行为学手动评分由双盲实验者独立完成，且一致性高（>90%），确保了数据分析的客观性。与骨架法的对比也公平地展示了图像法的优势。

### 6. 主要结论与发现
*   **神经活动特征**：哺乳期母鼠在持续吸吮期间，催产素神经元呈现出**偶发性、大幅度、同步化**的钙波，且该波动的数量与幼崽体重增加呈正相关。
*   **行为学标志**：排乳期间存在一个高度固定且可解释的母幼互动行为序列，即**活动耦合的母幼互动**，表现为：母鼠高度驼背 -> 幼崽踩踏 -> 幼崽伸展 -> 幼崽交换乳头。
*   **自动化工具**：开发的`ME解码器`能够基于俯拍视频自动、准确地检测排乳事件，其识别正确率超过75%，准确率约90%。
*   **机制洞察**：全身性阻断催产素受体显著减少了排乳事件，但不影响中枢催产素神经元的脉冲式放电活动，表明外周阻断药物并未反馈抑制该神经元的同步化爆发。

### 7. 优点
*   **方法创新性**：首次建立了清醒动物中结合神经活动、精细行为和深度学习的自动化排乳分析框架，克服了传统需要在麻醉下测量乳腺内压的限制。
*   **可解释性强**：不仅提供了一个“黑箱”模型，还通过可视化技术和行为学分析，定义了一个明确的、可被人类观察者可靠使用的行为学指标`ADPI`。
*   **多维度验证**：将自动化分析的结果，同时与生理金标准（钙活动）和行为金标准（双盲人工评分）进行交叉验证，结论坚实。
*   **应用前景广阔**：该方法成本效益高、非侵入性，仅需普通摄像设备，为研究哺乳的神经环路、社会行为及药物影响提供了强大且普适的工具。

### 8. 不足与局限
*   **记录技术的局限**：光纤光度测量虽然能反映群体神经元活动，但可能降低检测的敏感性和特异性，无法揭示单细胞水平的同步化机制。
*   **模型泛化性边界**：`ME解码器`的训练数据主要来自哺乳中晚期（产后第7-20天），其在哺乳早期（产后第1-6天）的应用效果可能需要进一步优化和验证。
*   **行为检测的潜在偏差**：顶部摄像头视角下，部分幼崽可能被母鼠完全遮挡，`ADPI`和模型虽然能处理多数情况，但对完全不可见个体的行为解读仍存在信息缺失。
*   **环境与场景限制**：模型的性能在改变环境设置（如垫料、光线、笼具）或不同动物品系中的鲁棒性，虽然文中提及已验证，但其详细数据和边界未充分展开。

（完）
