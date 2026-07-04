---
title: Modelling individual ampullary afferents in two species of gymnotiform fish using simulation-based inference
title_zh: 使用基于模拟的推断对两种裸背电鳗的壶腹电感受器传入神经进行建模
authors: "Mayer, S., Benda, J., Grewe, J."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.24.734418v1.full.pdf"
tags: ["query:sr"]
score: 8.0
evidence: 将刺激与尖峰活动相关联的神经编码数学模型
tldr: 针对两种弱电鱼壶腹电感受器编码机制不明的问题，本文构建了扩展的泄露整合发放模型，引入低通滤波和两种噪声源（白噪声和粉红噪声），并采用仿真推断训练神经网络根据反应特征估计参数。该模型能准确复现感器自发放电和刺激驱动的频谱特性，并生成异质的生物学合理模型种群，为电感觉外周提供统一机制模型及更高阶神经处理研究基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 壶腹电感受器编码机制跨物种保守但实现不同，需建立统一的跨物种电感觉外周模型。
method: 使用仿真推断训练神经网络，将扩展的泄露整合发放模型参数映射到神经元反应特征上，模型增加低通预滤波和活动依赖的适应噪声。
result: 模型成功复现了两种鱼壶腹传入神经的自发放电和刺激响应频谱，低频编码需粉红噪声，高频编码需低通滤波。
conclusion: 提出了统一的壶腹电感受器编码机制模型，并可利用仿真推断网络生成生物学合理的感觉神经元种群，用于上级神经加工研究。
---

## 摘要
壶腹电感受器广泛存在于水生脊椎动物中。感知外源电场的目的在不同物种间是保守的，但实现方式各异，且编码机制仍未完全理解。我们比较了弱电鱼线翎电鳗（Apteronotus leptorhynchus）和青色埃氏电鳗（Eigenmannia virescens）的壶腹电感受器传入神经在基线状态和刺激驱动下的响应特性。我们发现，一个扩展的漏电整合发放模型能够很好地捕捉它们的活动，并且该模型可泛化至这两个物种。该模型与之前的一个结节状电感受器传入神经模型有相似之处，但进一步加入了低通预滤波和额外的噪声源，以重现观测到的频谱响应特征。低通滤波对于在高频范围内塑造刺激编码至关重要。准确预测低频刺激编码还需要两种不同的噪声源：与刺激无关的白电流噪声以及适应电流中活动依赖的噪声，后者由适应时间常数塑造，产生粉红噪声动态。利用基于模拟的推断，我们训练了一个神经网络，将模型参数映射到神经元响应特征。该方法能够生成异质的、生物学上合理的模型群体，可作为研究下一级神经处理的真实输入层。由此，我们为这些物种乃至可能更广泛的物种提供了一个统一且机制性的壶腹电感受器编码模型。所提模型是朝着这些动物的电感受外周系统完整模型迈出的又一步。

作者摘要感知外源电场（即被动电感受）的能力在水生动物中很普遍。它在猎物探测中起着核心作用，在某些物种中也参与交流。要理解高阶脑功能，我们还需要掌握感觉外周，并且最好拥有能提供自然外周响应的模型。利用基于模拟的推断（SBI），我们在此开发了一个被动电感受的机制模型，该模型至少对两种电鱼有效。通过详细分析，我们确定了模型组件，例如粉红噪声源，这些组件对于使模型频谱响应特性与记录细胞的频谱响应特性相匹配至关重要。这项工作的主要成果是模型本身和训练好的推断网络（这里称为SBI网络），该网络现在可用于创建人工但生物学上合理的感觉神经元群体，可作为研究高阶神经处理的真实输入层。我们的工作补充了现有的主动电感受模型，是朝着这些动物电感受外周系统完整模型迈出的一大步。

## Abstract
Ampullary electroreceptors are widespread across aquatic vertebrates. The purpose of sensing exogeneous electric fields is conserved across species but the implementations differ and the encoding mechanisms remain incompletely understood. We compared baseline and stimulus-driven response properties of ampullary electroreceptor afferents in the weakly electric fish Apteronotus leptorhynchus and Eigenmannia virescens. We find that their activity is very well captured by an extended leaky integrate-and-fire model that generalizes across both species. The model shares similarities to a previous model of the tuberous electroreceptor afferents but further incorporates a low-pass pre-filtering and additional noise sources to reproduce the observed spectral response characteristics. The low-pass is essential to shape stimulus encoding in the high-frequency range. Accurate prediction of low-frequency stimulus encoding further requires two distinct noise sources: stimulus-independent white current noise and activity-dependent noise in the adaptation current, which is shaped by the adaptation time constant to yield pink noise dynamics. Using simulation-based inference, we trained a neural network to map model parameters to neuronal response features. This approach enables the generation of heterogeneous, biologically plausible model populations that may serve as a realistic input layer for studying neuronal processing on the next level. With this, we provide a unified and mechanistic model of ampullary electroreceptor encoding in these species and possibly beyond. The proposed model is another step towards a full model of the electrosensory periphery in these animals.

Author summaryThe ability to sense exogenous electric fields, i.e. passive electroreception, is widespread among aquatic animals. It plays a central role in prey detection and, in some species, also contributes to communication. To understand higher-order brain function, we also need to grasp the sensory periphery and ideally have models that provide naturalistic peripheral responses. Using simulation-based inference (SBI), we here develop a mechanistic model of passive electroreception that is valid for at least two species of electric fish. Through detailed analyses, we identify model components, such as a source of pink noise, that are essential for matching the models spectral response properties to those of the recorded cells. The main results of this work are the model itself and the trained inference network (here called the SBI network), which can now be used to create artificial but biologically plausible populations of sensory neurons that may serve as a realistic input layer for studying higher-order neuronal processing. Our work complements the existing models of the active electric sense and is a big step towards a full model of the electrosensory periphery in these animals.