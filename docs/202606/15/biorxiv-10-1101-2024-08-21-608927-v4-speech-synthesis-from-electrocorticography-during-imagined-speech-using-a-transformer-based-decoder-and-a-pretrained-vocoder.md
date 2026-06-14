---
title: Speech Synthesis from Electrocorticography during Imagined Speech Using a Transformer-Based Decoder and a Pretrained Vocoder
title_zh: 基于Transformer解码器和预训练声码器的想象语音皮层脑电图语音合成
authors: "Komeiji, S., Shigemi, K., Mitsuhashi, T., Iimura, Y., Suzuki, H., Sugano, H., Shinoda, K., Yatabe, K., Tanaka, T."
date: 2026-06-13
pdf: "https://www.biorxiv.org/content/10.1101/2024.08.21.608927v4.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 想象语音ECoG到语音合成的脑机接口
tldr: 针对想象言语脑电图（ECoG）信号因缺乏同步音频而难以训练语音合成模型的问题，本研究提出利用朗读言语音频作为想象言语的替代训练目标，基于语言内容一致性，采用Transformer解码器从ECoG生成对数梅尔谱图，再通过预训练Parallel WaveGAN合成波形语音。13名被试的实验取得合成语音与代理目标之间动态时间规整对齐的皮尔逊相关系数0.74-0.84，验证了该框架的有效性。
source: biorxiv
selection_source: fresh_fetch
motivation: 想象言语ECoG信号缺乏同步音频训练数据，致使语音合成极具挑战。
method: 利用朗读言语音频作为代理真实目标，使用Transformer解码器从ECoG生成对数梅尔谱图，再经预训练Parallel WaveGAN转换为语音波形。
result: 合成语音与代理目标的动态时间规整对齐皮尔逊相关系数达到0.74至0.84。
conclusion: 朗读言语音频能作为想象言语重建的有效训练目标，为无行为输出情况下解码器的训练提供了可行方案。
---

## 摘要
从想象语音期间记录的皮层脑电图（ECoG）信号合成语音仍然是一个挑战，因为缺乏同步的音频信号用于训练。为了解决这个问题，我们提出了一种训练框架，利用在出声语音任务中记录的音频作为想象语音信号的替代真实标签，这是基于语言内容的一致性。我们使用了一个基于Transformer的解码器从想象语音ECoG生成对数梅尔频谱图，然后使用预训练的Parallel WaveGAN将其转换为波形音频。在涉及13名参与者的ECoG记录实验中，合成的语音与代理目标之间的动态时间规整对齐的皮尔逊相关系数范围在0.74到0.84之间。这些结果表明，出声语音音频可以作为重建想象语音的有效训练目标，为在缺乏行为输出的情况下训练解码器提供了一种可行的解决方案。

## Abstract
Synthesizing speech from Electrocorticogram (ECoG) signals recorded during imagined speech remains a challenge due to the absence of synchronized audio signals for training. To address this, we propose a training framework that utilizes audio recorded during overt speech tasks as a surrogate ground truth for imagined speech signals, based on the consistency of the linguistic content. We employed a Transformer-based decoder to generate log-mel spectrograms from imagined speech ECoG, which were then converted into waveform audio using a pre-trained Parallel WaveGAN. In experiments involving ECoG recordings from 13 participants, the synthesized speech achieved dynamic time warping-aligned Pearson correlation coefficients ranging from $0.74$ to $0.84$ with the proxy targets. These results demonstrate that overt speech audio can serve as an effective training target for reconstructing imagined speech, offering a viable solution for training decoders in the absence of behavioral output.

---

## 论文详细总结（自动生成）

# 论文深度分析：《基于Transformer解码器和预训练声码器的想象语音皮层脑电图语音合成》

## 1. 研究动机与核心问题

*   **核心问题**：如何从想象语音（Imagined Speech）期间记录的皮层脑电图（ECoG）信号中合成出可听懂的语音波形。
*   **根本挑战**：想象语音过程中**不存在同步的声学音频信号**作为训练目标。传统基于有监督学习的神经解码模型，严重依赖于成对的“神经信号—音频”数据，而想象语音天然缺乏这种对应关系，导致模型训练极度困难。
*   **研究意义**：解决该问题对于开发面向失语症患者或闭锁综合征患者的“无声脑机接口”至关重要，旨在直接从大脑意图中恢复交流能力。

## 2. 方法论核心

论文的核心思想是**利用替代训练目标（Proxy Surrogate Target）** 巧妙地绕开想象语音缺少同步音频的困境。

*   **核心假设**：假设**出声语音（Overt Speech）** 与**想象语音**在语言内容一致的前提下，共享相似的神经表达和声学特征。因此，出声语音的音频信号可作为想象语音ECoG的“代理真实标签”。
*   **两阶段流水线架构**：
    1.  **ECoG到声学特征解码器**：
        *   **输入**：想象语音期间的ECoG高频神经信号。
        *   **架构**：采用 **Transformer 解码器** 结构进行时间序列建模，负责从ECoG特征映射到声学中间表征。
        *   **输出**：**对数梅尔频谱图（Log-mel Spectrograms）**。这是语音合成领域常用的二维时频表征。
    2.  **声学特征到语音波形生成**：
        *   **模型**：使用预训练好的 **Parallel WaveGAN** 声码器。
        *   **输入**：第一步生成的对数梅尔频谱图。
        *   **输出**：最终的 **合成语音波形**。

*   **训练与评估的对齐策略**：
    *   由于想象语音和代理音频在时间尺度上存在非线性扭曲（语速不同），论文在计算客观质量指标时，采用了 **动态时间规整（Dynamic Time Warping, DTW）** 算法，将合成语音的频谱与代理目标音频的频谱在时间轴上强制对齐，然后计算 **皮尔逊相关系数（Pearson Correlation Coefficient）** $r$。

## 3. 实验设计

*   **被试数据**：实验涉及 **13名参与者** 的ECoG颅内记录数据。数据集包含想象语音任务下的ECoG信号，以及出声语音任务下同步记录的ECoG和音频信号。
*   **任务范式**：出声语音与想象语音对应的语言内容（词汇/短语）需保持一致，以构建配对训练数据。
*   **评估基准（Benchmark）**：
    *   **主要指标**：合成语音与代理音频经 DTW 对齐后的皮尔逊相关系数，用于客观衡量频谱包络的重建准确度。
    *   **对比方法/基线**：摘要中未明确提及与其他具体模型的对比实验（如LSTM、CNN基线），侧重于验证“出声代理想象”这一框架的可行性本身。

## 4. 资源与算力

*   **文中说明情况**：在提供的摘要与元数据中，**未明确提及**训练所使用的GPU型号、显卡数量、显存大小或具体的训练耗时。
*   **推断**：考虑到使用了 Transformer 架构和 Parallel WaveGAN，且数据为多被试ECoG信号，训练通常需要中高端的单卡或多卡 GPU（如 NVIDIA V100 或 A100 系列），但确切的算力开销需查阅完整论文的实验设置部分。

## 5. 实验数量与充分性

*   **实验规模**：基于摘要，实验覆盖了 **13名被试** 的宏观验证，这在植入式脑机接口研究中属于中大规模的样本量。
*   **量化结果**：报告了 DTW 对齐后的皮尔逊相关系数范围，跨被试结果在 **$0.74$ 至 $0.84$** 之间。
*   **充分性评估**：
    *   **客观公平性**：使用皮尔逊相关系数作为物理层面的频谱相似度指标是客观的。不过，摘要未提及主观听力测试（如人工可懂度打分），无法评估合成的语音人类是否能真正听懂。
    *   **消融实验**：摘要中**未体现**消融实验（例如：验证Transformer是否优于RNN、验证对齐损失函数的作用、验证不同频段的ECoG特征贡献等）。若缺少这些，方法的内部有效性论证可能不够饱满。

## 6. 主要结论与发现

1.  **框架有效性验证**：出声语音音频**能够作为**想象语音重建的高质量代理训练目标。
2.  **定量表现**：Transformer解码器成功将想象语音ECoG转化为对数梅尔谱，经声码器导出后，客观声学指标与真实（代理）音频高度相关。
3.  **应用前景**：提供了一种在无法获取行为输出（如说话、动作）的情况下训练神经解码器的**可行替代方案**，为“无声交流”脑机接口的发展迈出了重要一步。

## 7. 论文优点与亮点

*   **巧妙的训练策略**：最大的亮点是提出了“**利用出声语音音频作为想象语音的代理监督信号**”。这解决了脑机接口语音合成领域一个极其头疼的数据缺失问题，极具工程实用价值。
*   **端到端可控生成**：结合 Transformer 解码器与 Parallel WaveGAN，实现了从高维神经信号直接到可播放语音波形的完整通路。
*   **客观指标较高**：在未经大量数据清洗的情况下，频谱重建的相关系数能达到 0.74-0.84，说明神经信源保留了相当丰富的声学特征信息。

## 8. 不足与局限性

*   **“想象”与“出声”的鸿沟**：代理假设是该方法的生命线，也是最大风险。出声语音涉及听觉反馈和嘴部肌肉的本体感觉反馈，而想象语音缺乏这些。强行对齐两者的特征可能会引入系统性噪声，限制合成语音的精细度（如语调、情感）。
*   **评估维度的单一性**：目前仅报告了 **DTW-皮尔逊相关系数**。该指标更关注频谱形状的数学拟合，**无法等同于人耳的实际可懂度**。论文缺少主观听力测试（如MOS分或词错误率），我们不知道合成出来的“声音”人类是否能辨别出具体的字句。
*   **时间对齐的局限性**：DTW 虽然解决了非线性的语速同步问题，但它本质上是一种数据操纵。在实际的实时闭环系统中，语音合成必须流式输出，无法使用未来的信息进行 DTW 对齐，因此该评估得分可能高估了实时场景下的实际性能。
*   **侵入式设备的限制**：使用 ECoG（需开颅手术植入电极阵列）属于侵入式方案，临床应用门槛高、风险大，难以像非侵入式（头皮脑电）那样快速普及。
*   **信息缺失**：摘要未提及具体的词汇量大小（开放词汇还是孤立词）、解码的延迟以及跨时间（不同日期）的模型泛化能力，这些都是限制其实际可用性的关键因素。

（完）
