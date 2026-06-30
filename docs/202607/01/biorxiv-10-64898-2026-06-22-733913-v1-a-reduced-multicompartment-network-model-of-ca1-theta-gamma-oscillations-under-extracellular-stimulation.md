---
title: A reduced multicompartment network model of CA1 theta-gamma oscillations under extracellular stimulation
title_zh: 细胞外刺激下CA1 theta-gamma振荡的简化多室网络模型
authors: "Andriantsoamberomanga, M., Rougier, N. P., Wagner, F. B., Aussel, A."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733913v1.full.pdf"
tags: ["query:sr"]
score: 7.0
evidence: CA1神经活动在刺激下的数学模型
tldr: 针对深部脑刺激治疗记忆障碍效果不一且机制不明的问题，本文开发了一个简化海马CA1多室网络模型。该模型包含锥体细胞、篮状细胞和OLM细胞及CA3到CA1的轴突投射，能够再现theta嵌套gamma振荡。通过在细胞外施加刺激，系统探究电极位置、刺激幅度和频率的影响，发现兴奋性反应主要由Schaffer侧支投射驱动。该模型计算高效，为探索神经调控策略提供有力模板。
source: biorxiv
selection_source: fresh_fetch
motivation: 深部脑刺激治疗记忆障碍效果不一致，需理解其对海马theta-gamma振荡的调控机制。
method: 构建含锥体、篮状、OLM细胞及CA3投射的简化多室CA1网络模型，施加细胞外刺激。
result: 模型再现theta-gamma振荡，刺激引起的CA1兴奋主要源于Schaffer侧支投射的募集。
conclusion: 该计算高效模型可系统研究刺激参数对海马动力学的影响，助力优化记忆障碍的神经调控策略。
---

## 摘要
深部脑刺激已显示出调节与帕金森病和癫痫相关的病理性振荡的治疗潜力。然而，其在治疗记忆相关疾病（如阿尔茨海默病）中出现的theta-gamma相位-振幅耦合紊乱方面的疗效仍知之甚少。虽然近期研究已针对内嗅-海马回路，但结果仍不一致。这种差异源于对刺激方案如何影响该回路的机制缺乏理解。在本工作中，我们提出了一个海马CA1区的简化多室模型，该模型能重现记忆任务期间健康神经活动的特征——theta嵌套的gamma振荡。模型包含形态简化的锥体细胞、篮状细胞和OLM细胞。我们还加入了CA3到CA1的轴突投射，为研究刺激诱导的传入通路募集如何调节CA1动力学提供了基础框架。通过平衡计算效率与解剖精度，我们的模型能够系统性地研究电极位置和方向，以及刺激幅度和频率对CA1神经活动的影响。我们证明，CA1的兴奋性反应主要由Schaffer侧支投射的募集所驱动。总体而言，这项工作为探索不同的刺激配置提供了一个计算效率高的模板，并可扩展用于开发恢复生理网络动力学的神经调控策略。

作者摘要：深部脑刺激已通过抑制导致运动障碍的异常神经活动，在治疗帕金森病方面取得了成功。然而，当应用于记忆相关病理（如阿尔茨海默病）时，治疗效果仍不可预测，范围从认知改善到损害。这一差异凸显了我们对刺激方案如何与目标回路的神经动力学相互作用的机制理解存在关键缺口。为了解决这一问题，我们开发了一个计算高效的海马模型（海马参与记忆过程），以理解深部脑刺激如何影响其活动。我们的模型保持了足够的生物准确性，以捕捉与记忆相关的重要神经活动，同时保持轻量化，以便快速执行和系统探索不同的刺激方案。这种计算效率使我们能够系统研究多种刺激配置对海马动力学的影响。总体而言，该模型可为探索深部脑刺激机制提供一个有用且计算成本效益高的工具，并有助于优化旨在缓解记忆障碍的刺激方案。

## Abstract
Deep brain stimulation has demonstrated its therapeutic potential in modulating pathological oscillations associated with Parkinsons disease and epilepsy. However, its efficacy in treating disrupted theta-gamma phase-amplitude coupling seen in memory-related disorders, such as Alzheimers disease, remains poorly understood. While recent studies have targeted the entorhinal-hippocampal circuit, results remain inconsistent. This discrepancy stems from a lack of mechanistic understanding regarding how stimulation protocols affect this circuit. In this work, we present a reduced multicompartment model of the hippocampal CA1 area that reproduces theta-nested gamma oscillations characteristic of healthy neural activity during memory performance. The model comprises pyramidal, basket and OLM cells with simplified morphologies. We also incorporated CA3-to-CA1 axonal projections, providing a foundational framework for studying how stimulation-induced recruitment of afferent pathways modulates CA1 dynamics. By balancing computational efficiency with anatomical accuracy, our model enables systematic investigation of the effects of electrode placement and orientation, as well as stimulation amplitude and frequency on CA1 neural activity. We demonstrate that the excitatory response in CA1 is primarily driven by the recruitment of Schaffer collateral projections. Overall, this work provides a computationally efficient template for exploring diverse stimulation configurations and could be expanded for developing neuromodulatory strategies to restore physiological network dynamics.

Author summaryDeep brain stimulation has shown success in treating Parkinsons disease by suppressing abnormal neural activity responsible for movement disorders. However, when applied to memory-related pathologies, such as Alzheimers disease, the therapeutic outcomes remain unpredictable, ranging from cognitive improvement to impairment. This discrepancy highlights a critical gap in our understanding of how stimulation protocols interact with neural dynamics of the targeted circuits. To address this, we developed a computationally efficient model of the hippocampus, which is involved in memory processes, in order to understand how deep brain stimulation might influence its activity. Our model maintains enough biological accuracy to capture essential memory-related neural activity while remaining lightweight enough for rapid execution and systematic exploration of different protocols. This computational efficiency allowed us to conduct systematic investigations of several stimulation configurations to study their effects on hippocampal dynamics. Overall, this model could provide a useful and computationally cost-efficient tool for exploring the mechanisms of deep brain stimulation and help optimize stimulation protocols aimed at alleviating memory disorders.