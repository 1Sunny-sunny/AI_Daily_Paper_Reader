---
title: Optimizing MR-based gaze-decoding for eyes-closed eye-tracking in fMRI
title_zh: 优化基于磁共振的注视解码以实现fMRI中的闭眼眼动追踪
authors: "Kling, S. M., Lascombes, U., Nau, M., Masson, G. S., Szinte, M."
date: 2026-07-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.07.736972v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 基于深度学习的眼MR信号注视解码
tldr: 功能性磁共振成像中眼动追踪重要，但闭眼时摄像头不可用。本研究利用DeepMReye框架从眼部MR信号解码凝视行为，通过睁眼校准数据微调，并加入闭眼注视数据优化模型，实现了闭眼状态下可靠的凝视监测，推动了fMRI眼动追踪整合与认知研究。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736972-v1/fig-001.webp\", \"caption\": \"Figure 1. A. Visuomotor calibration tasks. Participants completed three consecutive parts (see Material and methods): 9 guided fixation, guided pursuit, and free viewing of natural images. B. DeepMReye CNN architecture and fine-tuning 10 procedure. DeepMReye takes eye mask voxels from BOLD images as input and predicts 2D gaze position through a series 11 of convolutional layers, trained using two loss functions: Euclidean Error (EE) and the discrepancy between EE and a 12 predicted error (PE). Fine-tuning was performed by retraining the network on new participant-specific input data and gaze 13 labels. C. Visual/eyes state tasks. Participants fixated on a bull’s eye target across five consecutive screen positions 14 (central and four corners of a virtual square) forming four triangle patterns with their gaze trajectories. D. The eye movement 15 sequence was completed over four parts varying in visual input (vision/no vision) and eye state (open, blinked, closed), in 16 which they followed a bull's eye target guided by auditory tone sequences. Here is shown a single triangle sequence, 17 forming a triangle pointing upwards. 18 19 Fine-tuning improves DeepMReye performance when the eyes are open 20 To evaluate whether DeepMReye’s decoding performance for eyes-open parts could be adjusted to 21 the experimental setup, we used a visuomotor calibration tasks composed of three parts: guided 22 fixation, guided pursuit, and free viewing (Figure 1A). We then compared two model configurations: 23 “DeepMReye” (the original pre-trained model, see Figure 2A) and “DeepMReye & visuomotor 24 calibration” (fine-tuned on the visuomotor calibration tasks, see Figure 2B). Decoding accuracy was 25 quantified in comparison to camera-based eye-tracking data using both Pearson correlation, tracking 26 temporal dynamics, and Euclidean errors, quantifying the spatial distance between decoded and 27 eye-tracking gaze position. 28 When considering temporal Pearson correlation “DeepMReye & visuomotor calibration” significantly 29 outperformed the pretrained version of “DeepMReye” in the fixation part (Figure 2C, “DeepMReye & 30 visuomotor calibration”: r = 0.87, [0.84; 0.91]; –mean Pearson and bootstrapped 95 confidence 31 interval across participants– vs. “DeepMReye”: r = 0.84, [0.79; 0.88]; p < 0.05), the guided pursuit 32\", \"page\": 3, \"index\": 1, \"width\": 1052, \"height\": 423}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736972-v1/fig-002.webp\", \"caption\": \"Figure 3. A. Classification accuracy for “DeepMReye”, “DeepMReye & visuomotor calibration”, and “DeepMReye & 10 visual/eyes state” models using temporally-ordered gaze coordinates, shown for the “Vision and eyes-open” and “No vision 11 and eyes-closed” parts. Example segments (triangle-up trial from sub-04) illustrate the temporally-ordered or temporally-12 shuffled gaze coordinate inputs used by each model configuration. B. Classification accuracy for the same model 13 configurations and parts following temporally-shuffled coordinates. Error bars represent bootstrapped 95% confidence 14 intervals across participants; asterisk shows significant comparison (p < 0.05). C. Timeseries of one triangle sequence of 15 a representative participant (sub-04) of the proportion of eyelid-closed per sample during “Vision and eyes-blink” part, as 16 decoded by “DeepMReye” (top panel), “DeepMReye & visuomotor calibration” (middle pannel), and “DeepMReye & 17 visual/eyes state” (bottom panel), compared to the ground-truth training labels. 18 19 Eyelid-state decoding 20 Beyond gaze position, we asked whether fine-tuning also improves decoding of eyelid-state, 21 specifically whether the model can accurately distinguish between open and closed eyelids. 22 Importantly, this analysis also addresses a more practical question: does eyelid-state decoding 23 require task-specific fine-tuning with eyes-closed data, or is fine-tuning with eyes-open visuomotor 24 calibration data sufficient? 25 To evaluate this, we compared three model configurations using eye-tracking pupil size as ground-26 truth. Because other parts of the visual/eyes state tasks were heavily imbalanced toward either open 27 or closed eyelids periods, we focused our analysis on the \\\"Vision and eyes-blink\\\" part, which 28 provided the most balanced distribution of eyelid-state periods and therefore the most sensitive test 29 of decoding performance. 30 Classification accuracy was computed by converting both the continuous model predictions and the 31 eye-tracking ground truth into binary labels using a 30% threshold: any sample with an eye-closure 32\", \"page\": 8, \"index\": 2, \"width\": 1057, \"height\": 419}]"
motivation: 解决fMRI中闭眼状态下缺乏有效眼动追踪方法的问题。
method: 采用DeepMReye框架，使用睁眼校准和闭眼注视数据进行微调，从MR信号解码眼动。
result: 微调显著提升解码性能，且模型成功泛化至闭眼数据，闭眼微调进一步改善。
conclusion: 闭眼期间可靠的MR-based凝视监测可行，有助于更有效整合眼动追踪到fMRI研究。
---

## 摘要
眼动为人类认知提供了宝贵见解，也是众多功能性磁共振成像（fMRI）研究中的关键变量。然而，当眼睛闭合时，基于摄像头的眼动追踪便无法使用，这使得闭眼状态的研究面临挑战。在此，我们通过基于磁共振的注视解码，利用DeepMReye这一深度学习框架从眼部磁共振信号中无摄像头重建注视行为，来弥补这一空白。我们首先表明，利用睁眼时获取的视觉运动校准数据对DeepMReye进行微调，能显著提升注视解码效果，且这种微调不需要同步的摄像头数据。接着，我们评估了纳入参与者在睁眼和闭眼状态下注视已知位置的数据是否能进一步提升模型性能。值得注意的是，尽管DeepMReye最初仅使用睁眼数据进行训练，该网络成功推广到了闭眼时期，且通过闭眼数据的微调，性能显著提高。这些发现表明，在闭眼期间进行可靠的注视监测是可行的，从而能够在fMRI研究中更有效地整合眼动追踪，进而推动我们对人类认知的理解。

## Abstract
Eye movements provide valuable insights into human cognition and are a critical variable in numerous functional magnetic resonance imaging (fMRI) studies. Yet, when the eyes are closed, camera-based eye-tracking is unavailable, making studies of eyes-closed states challenging. Here, we address this gap through MR-based gaze decoding with DeepMReye, a deep learning framework for camera-free reconstruction of gaze behavior from the MR-signal of the eyes. We first show that fine-tuning DeepMReye using visuomotor calibration data acquired when the eyes were open significantly improves gaze decoding, and that this fine-tuning does not require simultaneous camera-based data. We next assessed whether model performance could be further improved by incorporating data acquired while participants gazed at known positions with both eyes open and closed. Notably, while DeepMReye was originally trained exclusively on eyes-open data, the network successfully generalized eyes-closed periods, with performance improving significantly through fine-tuning on the eyes-closed data. These findings demonstrate that reliable gaze monitoring during eyes-closed periods is feasible, enabling a more effective integration of eye-tracking in fMRI research and, consequently, advancing our understanding of human cognition.

---

## 论文详细总结（自动生成）

## 论文核心问题与整体含义

- **研究背景**：眼动追踪在功能性磁共振成像（fMRI）研究中至关重要，它能协助验证被试是否按照要求观看刺激，并降低非预期注视行为的混淆效应。然而，传统的基于红外摄像头的眼动仪成本高昂，且在 MRI 环境中存在安装限制、信号丢失、运动伪影等问题。
- **核心问题**：最关键的局限性在于，当被试的眼睛处于闭合或遮挡状态（例如睡眠、闭眼静息态、视觉想象等实验）时，基于摄像头的眼动追踪完全无法工作。这导致fMRI研究中一个重要的实验状态——闭眼状态——在眼动监测上存在显著空白。
- **研究目标**：本研究旨在利用并优化一种无摄像头的磁共振（MR）注视解码技术，使其能够在被试睁眼和闭眼两种状态下，可靠地从功能性磁共振信号中重建注视位置。
- **整体含义**：该研究旨在为推动“无摄像头眼动追踪”技术在更多 fMRI 研究场景（尤其是传统方法无法触及的闭眼实验）中的实际应用提供了方法论和工具，从而促进对人类全意识状态下眼动行为的理解。

## 论文提出的方法论

- **核心框架**：研究基于 DeepMReye，这是一个使用卷积神经网络（CNN）从眼球及周边组织的 BOLD 信号中解码出二维注视位置的深度学习框架。

- **关键技术流程与思想**：
    - **基础模型**：使用 DeepMReye 的预训练模型作为起点，该模型能将眼球区域掩模（mask）内的体素信号作为输入，输出连续的 $X$ 和 $Y$ 注视坐标。
    - **微调策略**：针对本地实验设备和特定任务进行模型微调，使模型适应新的数据分布，这是提高解码性能的核心方法。
        - **睁眼数据微调（Visuomotor Calibration）**：使用一套标准化的视觉运动校准任务（包含引导注视、引导追随、自由观看）收集的睁眼BOLD数据和眼部追踪标签，对预训练模型进行再训练。
        - **闭眼数据微调（Visual/Eyes State）**：开发了一项新颖的听觉引导眼动任务。被试在睁眼或闭眼状态下，跟随不同的听觉音调组合，依次注视构成三角形的四个角的五个屏幕位置。此任务产生的数据（特别是在“无视+闭眼”部分）可用于进一步微调模型，以提升闭眼状态下的解码能力。
    - **损失函数**：训练中使用了两个损失函数：欧几里得误差（Euclidean Error, $EE$）和 $EE$ 与预测误差（Predicted Error, $PE$）之间的差异。微调时，模型权重基于原始预训练模型参数进行初始化。
    - **无需摄像头标签的训练**：研究证明，在引导注视和引导追随等结构化的任务中，可以直接使用目标位置（Target Position）作为训练标签进行微调，其效果与使用真实眼动数据相当。

## 实验设计

- **参与者与数据集**：17名健康成人参与实验，其中15人完成全部扫描，数据被用于分析。数据包含结构像、功能像及同步采集的摄像头眼动数据。
- **任务范式与场景**：
    - **视觉运动校准任务（Visuomotor Calibration Tasks）**：
        - **引导注视（Guided Fixation）**：被试注视在18°视场角（dva）正方形范围内25个固定位置之一。
        - **引导追随（Guided Pursuit）**：被试追踪平滑移动的目标点。
        - **自由观看（Free Viewing）**：被试自由观看自然图像。
    - **视觉/眼睛状态任务（Visual/Eyes State Tasks）**：一个交叉设计的任务，操纵了视感觉输入（有/无）和眼睑状态（睁/闭/眨眼）两个因素。被试需在听觉引导下，通过注视完成四种方向的三角形轨迹。
- **基准模型与对比方法**：本研究主要对比了四种模型配置的解码表现：
    - **DeepMReye**：原始的仅使用预训练权重的模型，作为基线。
    - **DeepMReye & Visuomotor Calibration**：在视觉运动校准任务上微调后的模型。
    - **Scaled DeepMReye**：对原始模型的输出进行线性缩放，以匹配当前更大的屏幕尺寸（18 dva），用于检验微调是否仅等同于简单的尺度变换。
    - **DeepMReye & Visual/Eyes State**：在视觉/眼睛状态任务上微调后的模型。
- **评价指标**：
    - **睁眼性能**：将模型解码的注视坐标与同步采集的摄像头眼动数据进行对比，计算时间序列的皮尔逊相关系数（$r$）和空间欧几里得误差（单位：度）。
    - **闭眼性能**：由于缺乏真实注视坐标，使用逻辑回归分类器从解码出的注视轨迹中识别三角形方向，以分类准确率作为间接评价指标。此分析分别在保持坐标时间顺序和打乱顺序（`Temporally-shuffled`）两种条件下进行。
    - **眼睑状态解码**：使用30%的阈值将连续的眼睑闭合信号二值化为“开/闭”，并与摄像头数据的地面真值进行比较，计算分类准确率。

## 资源与算力

- 论文中**未明确提及**进行模型微调和推理所使用的**GPU型号、数量或具体的训练时长**。文中仅列出了微调的超参数，如学习率（$2 \times 10^{-6}$）、批次大小（15个被试）、训练步数（5000步）和训练轮次（1轮）。

## 实验数量与充分性

- **实验组数**：研究进行了多组对比实验，覆盖了多个层面。
    - **校准效果验证**：分别评估了是否有视觉运动校准任务微调的模型（2种配置）在三个子任务（引导注视、追随、自由观看）上的表现，并额外比较了与线性缩放模型的差异，验证了微调的必要性。
    - **数据依赖性分析**：比较了使用真实眼动标签和目标位置标签进行微调的效果，验证了对摄像头数据的依赖程度。
    - **闭眼解码能力**：在视觉/眼状态任务的四个不同条件下，对三种模型配置的解码轨迹进行了方向分类准确率的评估，并使用时间打乱的方式排除了时间结构的影响。
    - **眼睑状态解码**：专门评估了三种模型配置在解码眼睑开闭状态上的性能。
- **实验充分性与公平性**：实验设计较为充分和系统。通过层层递进的对比实验，不仅验证了方法有效性，还深入探究了性能提升的来源（例如，适应屏幕尺寸vs学习动态）、训练数据的依赖性以及在不同视觉/眼睑状态下的泛化能力。采用了留一被试交叉验证（leave-one-subject-out）和非参数置换检验，保证了统计评估的严谨性和公平性。

## 论文的主要结论与发现

- **微调显著提升性能**：使用专有视觉运动校准数据对DeepMReye进行微调，能显著提升睁眼条件下的注视解码性能。
- **微调超越简单缩放**：微调带来的提升不仅仅是补偿模型输出与当前屏幕尺寸不匹配的问题，而是让模型学习到了更本质的注视动态。
- **不依赖摄像头数据**：在结构化任务中，使用屏幕坐标作为标签即可达到与真实眼动标签相当的解码效果，降低了应用门槛。
- **成功泛化至闭眼状态**：仅用睁眼数据训练的原始DeepMReye模型已经表现出对闭眼注视解码的一定泛化能力。当使用包含闭眼数据的专用任务进行微调后，**闭眼状态下的解码准确率得到了最显著的提升**。
- **眼睑状态可解码**：模型能够可靠地区分睁眼和闭眼状态。但值得注意的是，仅使用睁眼视觉运动校准数据进行微调便足以显著提升眼睑状态解码的性能，额外的闭眼数据微调并未带来更多增益。

## 优点

- **填补重要空白**：该方法直接解决了传统眼动追踪在fMRI闭眼研究中的盲点，为睡眠、静息态等多种范式打开了新的研究窗口。
- **实用性强**：研究提供了完整的“任务范式-微调方法-性能评估”解决方案，并证明了训练过程可以不依赖昂贵的眼动仪，这大大降低了该技术的应用门槛，尤其有利于资源有限的实验室以及对已有无眼动数据的回顾性分析。
- **实验设计精巧**：听觉引导的眼动范式设计巧妙，它使得在完全没有视觉反馈和摄像头验证的情况下，也能对模型的解码能力进行客观的定量评估。
- **分析透彻**：通过一系列详尽的对比和消融实验，揭示了微调效果背后的原理，如对空间范围的适应和对动态行为的捕捉，而不仅仅是简单的输出缩放。

## 不足与局限

- **缺乏绝对的闭眼基准真值**：闭眼状态下解码性能的核心评价是基于间接的分类方法，而非精确的坐标比较。这使得无法衡量单点注视位置的解码精度或轨迹的保真度，模型解码出的可能是其基于睁眼数据“想象”的闭眼运动模式，而非真实的、质量上不同的闭眼固视行为。
- **任务依赖性**：用于闭眼微调的听觉引导范式要求被试能够理解并稳定地执行结构化眼动序列，这可能不适用于某些临床人群（如意识障碍、儿童），而这类人群恰恰是该方法最希望服务的对象。
- **泛化性限制**：虽然证明了微调的优势，但在特定小样本上微调后模型的性能否稳定泛化到完全不同的新任务或新被试群体中，仍有待验证。特别是自由观看任务的解码性能改善有限，是未来一大挑战。
- **时间精度有限**：模型预测基于每个TR（本实验中为1.2秒）的单点或多点平均，这使得它非常适合监测持续的注视状态，但无法替代高时间精度的摄像头眼动仪进行传统意义上的眨眼检测或细微的眼跳分析。

（完）
