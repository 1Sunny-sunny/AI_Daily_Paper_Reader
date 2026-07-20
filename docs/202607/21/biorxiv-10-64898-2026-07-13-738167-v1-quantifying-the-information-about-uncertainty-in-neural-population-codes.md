---
title: Quantifying the information about uncertainty in neural population codes
title_zh: 量化神经群体编码中关于不确定性的信息
authors: "Wang, X., Dayan, P., Bays, P."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.13.738167v1.full.pdf"
tags: ["query:sr"]
score: 9.0
evidence: 量化神经群体编码中的不确定性信息
tldr: 本文研究神经群体编码如何编码感觉变量及其不确定性。作者提出两种量化辅助信息的方法，并揭示估计误差的非高斯性与不确定性信息的内在联系，为理解元认知提供理论框架。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-006.webp\", \"caption\": \"Figure 1: Marginal distribution of the estimation error in the MLE for translation-symmetric population codes. An example of maximum likelihood (ML) decoding: for a given stimulus (orientation θ), stochasticity in neural activity r leads to variability in likelihood width, shape and location of the peak (the MLE θ̂r). Among the different likelihood functions (left), the same estimation error ε (red curves; same θ̂r as indicated by the dotted red line) can be associated with different ar (different shapes), whereas the same ar (orange curves; same shape) can be associated with different values of ε. The marginal estimation error (blue curve; far right) is a mixture of the normalized, reflected (around the MLE) and re-centred likelihood components (grey curves; right).\", \"page\": 4, \"index\": 6, \"width\": 923, \"height\": 419}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-002.webp\", \"caption\": \"Figure 2: Geometric views of statistical inference for MLE. (a) In the boules example (see text) two different landing points (x1 and x2, blue dots) yield the same MLE θ̂x (black cross) of the direction of the jack, and thus the same angular error ε relative to the true direction (black unfilled dot), but the likelihoods differ in width, with the farther landing point having a narrower likelihood. The statistical model is equivalent to Fisher’s circle model (inset): likelihood functions are von Mises with concentration equal to the distance D from the centre of the unit circle. This is also the value of the Observed FI, which quantifies certainty in the estimate. The marginal error distribution is a scale mixture of von Mises with concentrations distributed identically to the distances. (b) Statistical inference based on high-dimensional neural activity r and exponential family noise: The mean response of M neurons forms a one-dimensional curved submanifold M ⊂ R. All observations r (blue dots) that yield the same MLE θ̂r (black cross) lie in an (M−1)-dimensional ancillary subspace Aθ̂. This ancillary subspace intersects with M at θ̂r. The critical point C is now an (M − 2)-dimensional subspace containing responses that are equiprobable for all values of the stimulus θ. Within the ancillary subspace corresponding to a particular MLE, the Observed FI Jθ̂(r) increases linearly with distance measured orthogonally from C in the direction of r̄(θ̂r), i.e. parallel to the vector λθ̂ (unfilled dots correspond to observations with less uncertainty, as measured by Observed FI, than filled dots). Variation orthogonal to this line (e.g. differently coloured dots) corresponds to observations that are matched in estimation error and Observed FI, but differ in other aspects of the shape of the likelihood function (insets).\", \"page\": 7, \"index\": 2, \"width\": 735, \"height\": 809}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-005.webp\", \"caption\": \"Table 1: A summary of the key statistical and information-theoretic quantities\", \"page\": 8, \"index\": 5, \"width\": 944, \"height\": 334}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-007.webp\", \"caption\": \"Figure 3: Marginal error as a mixture of circular normal (von Mises) distributions, with likelihood precision following a Gamma distribution. (a) The probability density of the Observed FI (Gamma distributed) and the corresponding marginal error distribution (insets), shown for fixed Expected FI (I = 1, 2, 4). Colours indicate different levels of I∞ loss. For a fixed I, increasing I∞ loss leads to heavier tails in the marginal error distribution. (b) Higher I∞ loss implies greater variability in the Observed FI, resulting in heavier tails in the marginal error distribution. (c) The information loss as a function of scale (s), which is related to the shape parameter α by α = I/s. For a fixed I, the asymptotic loss (I∞ loss, dashed lines) depends solely on s and increases linearly with it (corresponding to decreasing α). The information loss in a single observation (Iloss, solid lines) increases monotonically with s, plateaus at large s (with higher asymptote for larger I), and converges to I∞ loss as α → ∞. (d) MIe as a function of Iloss and I∞ loss for fixed I. Results obtained using Monte Carlo simulations with 107 samples on a uniform grid of 201 points spanning θ ∈ [−π, π). Unless otherwise indicated, these simulation settings are used throughout the paper.\", \"page\": 9, \"index\": 7, \"width\": 746, \"height\": 634}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-003.webp\", \"caption\": \"Table 2: FI and the asymptotic loss of FI in the MLE for some statistical models\", \"page\": 10, \"index\": 3, \"width\": 846, \"height\": 229}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-001.webp\", \"caption\": \"Figure 4: The neural population coding framework. (a) Assuming idealized identically shaped tuning functions densely and evenly distributed over a circular stimulus space, noise in the neural response leads to insufficiency of the MLE, manifested in variation of likelihood width and shape and yielding heavy tails in the marginal error distribution. With a fixed value of Expected FI, for small Iloss, the marginal error distribution is approximately a circular normal distribution (dark blue curves). As Iloss increases, the error distribution deviates more from normality (light yellow curves). Error distributions are normalized by peak probability. (b) In the Poisson noise model, spike counts are discrete and non-negative, resulting in normal (von Mises) likelihoods. (c) In the Gaussian noise model, response amplitudes are continuous and can include negative responses, and likelihoods are nonnormal and may be multimodal. (d) For the modulated Poisson model with overdispersed Poisson firing, larger σ2 G leads to greater overdispersion in the neural response, resulting in heavier tails in the marginal error distribution and stronger interneuronal correlations. The interneuronal correlation matrix is shown with each off-diagonal entry representing the activity correlation between a pair of neurons; diagonal elements (autocorrelations) are omitted for illustrative purpose. Simulations use parameters of κ = 1, ξ = 2 for the (modulated) Poisson models, and equivalents for the Gaussian model based on the variance-stabilizing reparametrization. Results obtained with a population of M = 200 simulated neurons; the same setting is used throughout unless otherwise indicated.\", \"page\": 11, \"index\": 1, \"width\": 733, \"height\": 865}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-004.webp\", \"caption\": \"Figure 5: Ancillary information in different noise models. (a) A Gaussian approximation to Poisson variability (green curves) based on a variance-stabilizing transformation yields similar error distribution pattern to the standard Poisson model (black curves). (b) Ancillary information as a function of parameters κ and ξ, with the Expected FI held fixed (I = 2). Under this constraint, increasing κ is accompanied by decreasing ξ. With matched parameters, the Gaussian approximation has the same Expected FI as the Poisson but less ancillary information in terms of MIe (solid curves), Iloss (dashed curves) and asymptotically as I∞ loss (dotted curves). (c-d) Similar to (a-b) but with varying Poisson modulation parameter σ2 G. Modulation increases ancillary information (e) The relationship between MIe and Iloss in different noise models, with fixed Expected FI (I = 2). The standard Poisson model corresponds to the black line. (f) Ancillary information dependent on parameters κ and ξ in terms of Iloss (upper panel) and MIe (lower panel). White contour lines indicate I = 2.\", \"page\": 13, \"index\": 4, \"width\": 941, \"height\": 737}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738167-v1/fig-008.webp\", \"caption\": \"Figure 6: Effects of increasing external noise versus weakening activity. (a) Increasing external noise σ2 E (with fixed κ = 2 and ξ = 5) and (b) decreasing population gain ξ (with fixed κ = 2) both produce increased error variability (vertically aligned panels are matched for circular s.d.). Decreasing ξ leads to heavy tails in the marginal error distribution. (c) Changes in the error variability (circular s.d.) dependent on σ2 E and ξ. (d) Ancillary information (i.e. Iloss, I∞ loss and MIe) as a function of changes to circular s.d. induced by external noise (blue curves) or weakening activity (green curves). Dashed curves represent the values of I∞ loss. The theoretical value of I∞ loss = 1.87 is calculated as κI2(κ)/I1(κ)+1 (Table. 2, the Poisson model). (e) The relationship between the two ancillary information measures with respect to changes in external noise (increasing σ2 E , blue curve) or weakening activity (decreasing ξ, green curve). All simulations are based on the standard Poisson noise model. Coloured open circles in (c–e) correspond to the error distributions shown in (a,b).\", \"page\": 16, \"index\": 8, \"width\": 893, \"height\": 465}]"
motivation: 神经群体活动包含超出点估计的丰富信息，但如何量化这种关于不确定性的辅助信息及其与行为的关系尚不清晰。
method: 提出并比较两种量化方法：活动与估计误差的互信息，以及基于信息几何的Fisher信息损失。
result: 发现估计误差的非高斯性（如长尾）是辅助信息的自然结果；相同误差分布的群体可能因噪声特性不同而辅助信息含量迥异；给出了仅从群体活动获取不确定性信息的上限。
conclusion: 本研究将关于不确定性的知识与感知估计的非高斯性直接关联，为探究元认知在神经群体活动中的基础提供了坚实的理论依据。
---

## 摘要
神经群体的活动通常编码了关于感觉或运动变量的更多信息，这些信息无法仅通过变量的点估计来捕获。我们提出并比较了两种量化这种附加或辅助信息及其与不确定性关系的方法：活动与估计误差之间的互信息，以及可以借助信息几何中的曲率来解释的Fisher信息损失。我们表明，估计误差偏离高斯性，包括在人类行为任务中经常观察到的长尾分布，是存在辅助信息的预期推论。然而，具有相似估计误差分布的群体，其辅助信息含量可能因噪声特性而大相径庭。对于给定的群体调谐和噪声模型，我们的结果量化了仅从群体活动中可以获得的不确定性信息的上界：行为显示出的知识若超出此上界，则表明还获取了其他关于不确定性的信息源。最后，我们对比了外部噪声和内部信号强度下降对辅助信息和误差高斯性的影响。我们的工作将关于不确定性的知识与感觉估计中的非高斯性直接联系起来，并为研究神经群体活动中元认知的基础建立了一个一致的理论框架。

## Abstract
The activity of neural populations typically encodes more information about sensory or motor variables than can be captured by point estimates of the variables. We present and compare two approaches to quantifying this additional or ancillary information and its relationship to uncertainty: the mutual information between activity and estimation error, and the Fisher information loss, which can be interpreted in terms of curvature in information geometry. We show that deviations from Gaussianity of estimation errors, including the long tails frequently observed in human behavioural tasks, are an expected corollary of the presence of ancillary information. However, populations with similar distributions of estimation error can differ substantially in their ancillary information content depending on the noise characteristics. For a given population tuning and noise model, our results quantify an upper bound on the information about uncertainty that can be obtained from population activity alone: behaviour demonstrating knowledge in excess of this bound would indicate access to a separate source of information about uncertainty. Finally, we contrast the effects of external noise and decreasing internal signal strength on ancillary information and the Gaussianity of errors. Our work directly relates knowledge about uncertainty to non-Gaussianity in sensory estimates, and establishes a coherent theoretical foundation for investigating the basis of metacognition in neural population activity.

---

## 论文详细总结（自动生成）

好的，这是对论文《量化神经群体编码中关于不确定性的信息》的结构化总结。

### 1. 论文的核心问题与整体含义
*   **核心问题**：大脑在利用带有噪声的神经活动进行感知决策时，是如何同时获得关于决策本身可靠性（即不确定性）的信息的？在连续的刺激估计任务中，神经群体活动不仅包含对刺激变量的最佳估计（点估计），还包含关于该估计值不确定性的“辅助信息”。如何从理论框架上量化和理解这种辅助信息？
*   **整体含义**：本研究建立了一个统一的理论框架，将神经编码原理、估计误差的非高斯性（长尾分布）以及元认知敏感性（对自身决策正确性的评估）联系起来，并量化了从群体活动中能获取的不确定性信息的上限。

### 2. 论文提出的方法论
论文基于平移对称的神经群体编码模型（编码一个连续刺激 $\theta$），提出了两种互补的辅助信息量化方法，并探讨了它们与信息几何的联系。

*   **核心思想与关键公式**：
    *   **模型设定**：神经群体的随机活动 $r$ 编码刺激 $\theta$，其最大似然估计（MLE）为 $\hat{\theta}_r$。该模型为平移类型，因此可以将总体信息分解为与 $\hat{\theta}_r$ 相关的信息和辅助统计量 $a_r$ 相关的信息。估计误差定义为 $\varepsilon = \hat{\theta}_r - \theta$。边缘误差分布 $p(\varepsilon)$ 本质上是一系列归一化、反射并重新中心化的似然函数的混合分布，这是产生非高斯误差的根本原因。
    *   **基于互信息的量化指标 $MI_e$**：该指标衡量的是神经活动 $r$ 对估计误差 $\varepsilon$ 的信息量，定义为 $MI_e = MI(\varepsilon; r) = MI(\varepsilon; a_r)$。它可以表示为误差分布的熵与给定辅助统计量后误差条件熵之差。
        $$MI_e = H(\varepsilon) - H(\varepsilon|a_r) = H(\mathbb{E}_r[L^*_r]) - \mathbb{E}_r[H(L^*_r)]$$
        该公式可以看作是Jensen-Shannon散度（JSD）的推广，量化了似然函数形状的多样性。
    *   **基于费雪信息的量化指标 $I_{loss}$**：该指标衡量当用MLE $\hat{\theta}_r$ 代替全部观察 $r$ 时所损失的信息。它被定义为总体观察的费雪信息 $I$ 与 MLE 所包含的费雪信息 $I_{\hat{\theta}}$ 之差。
        $$I_{loss} = I - I_{\hat{\theta}} = \mathcal{F}(\mathbb{E}_r[L^*_r]) - \mathbb{E}_r[\mathcal{F}(L^*_r)]$$
        其中 $\mathcal{F}(f)$ 是基于Fisher信息计算分布散度的泛函。该公式是Jensen-Fisher散度（JFD）的推广。
    *   **信息几何视角**：在信息几何框架下，辅助信息的产生源于编码流形在神经活动空间中的曲率。被称为“统计曲率”（$\gamma_\theta$）的量与费雪信息损失的渐近形式（$I_{loss}^\infty$）直接相关：$I_{loss}^\infty = I \cdot \gamma_\theta^2$，其中 $\gamma_\theta = \frac{\sqrt{\text{Var}[J_\theta(r)]}}{I}$，而 $J_\theta(r)$ 是观测费雪信息。

### 3. 实验设计
本研究主要通过理论分析和计算仿真进行，未使用生物学或行为学真实数据集。其“场景”和基准对比如下：

*   **仿真场景与模型**:
    *   **神经群体模型**：一个密集且均匀覆盖圆形刺激空间的理想化神经元群体，使用冯·米塞斯调谐函数。
    *   **对比的噪声模型**:
        1.  **标准泊松噪声模型**：响应离散、非负，似然函数为冯·米塞斯分布。
        2.  **高斯噪声模型**：连续响应，可能产生负值，似然函数非标准，通常作为泊松模型的简化近似。
        3.  **调制泊松模型**：具有共享增益调制的泊松模型，能产生过度离散和相关噪声，更接近生物神经元特性。
*   **对比与基准**:
    *   **高斯近似与泊松模型的对比**：通过方差稳定化变换匹配两者参数，使其产生相似的估计误差分布。在此基础上，对比两者在辅助信息量（$MI_e$, $I_{loss}$）上的差异，以检验近似模型的保真度。
    *   **噪声类型与活动强度的对比**：对比“增加外部噪声”（在 $\theta$ 上叠加高斯噪声）与“减弱内部信号强度”（降低群体增益 $\xi$）这两种操作对辅助信息量和误差分布高斯性的不同影响。这是为了区分不同的不确定性来源如何影响元认知潜力。

### 4. 资源与算力
*   论文为理论性和计算仿真研究，没有提及大规模神经网络训练。文中提到的仿真（如使用 $10^7$ 样本的蒙特卡洛模拟）是标准的统计计算，**未明确说明**使用的具体CPU/GPU型号、数量或计算时长。因此，不涉及典型的“算力”成本评估。

### 5. 实验数量与充分性
*   **实验数量与类型**：
    1.  **理论推导**：严格从统计学和信息论角度推导出 $MI_e$ 和 $I_{loss}$ 的表达式，并建立其与信息几何曲率和渐近信息损失的联系。
    2.  **合成模型验证 (Fig. 3)**：在似然精度服从Gamma分布的混合高斯/冯·米塞斯分布这一简化模型中，系统测试了不同参数（$I$, $I_{loss}^\infty$）对误差分布形状和两种辅助信息指标关系的影响。
    3.  **多种噪声模型扫描 (Fig. 5, S2)**：在固定模型下，扫描了调谐浓度 $\kappa$ 和增益 $\xi$ 的参数空间，并观察辅助信息的变化。
    4.  **模型间对比分析 (Fig. 5a-d)**：在参数匹配条件下，系统对比了三种噪声模型的误差分布和辅助信息量。
    5.  **特定效应探究 (Fig. 6)**：设计了对比实验探究外部噪声与内部活动衰减对结果的影响。
*   **充分性与公平性**：实验设计在方法学上是公平和充分的。模型对比建立在参数匹配（如等检验费雪信息 $I$ 或等误差分布）的公平基础上，清晰揭示了不同模型的内在差异。参数空间扫描全面展示了指标的行为模式。

### 6. 论文的主要结论与发现
1.  **误差非高斯性与辅助信息直接相关**：估计误差分布是由不同宽度的似然函数混合而成，似然函数形状的多样性（即辅助信息）自然导致了误差分布的长尾。辅助信息 $I_{loss}$ 越大，误差分布尾部越重。
2.  **量化了不确定性信息的上限**：$MI_e$ 是一个可量化的理论界限，代表了仅从用于生成感知估计的同一神经表征中能获得的最高元认知敏感性。若行为学上测得的敏感性超过 $MI_e$，则意味着大脑可能采用了其他独立的信息源。
3.  **噪声特性至关重要，而非仅看误差模式**：具有相似估计误差分布的神经群体，其辅助信息含量可能因噪声模型（如泊松 vs. 高斯）不同而存在显著差异。将泊松噪声近似为高斯噪声会系统性地低估辅助信息量。
4.  **共享增益调制增强辅助信息**：在调制泊松模型中，引入共享增益调制（增加神经元间相关性）在总信息 $I$ 不变的情况下，能显著增加辅助信息 $I_{loss}$ 和 $MI_e$。
5.  **区分了外部噪声与内部信号衰减的影响**：增加外部噪声和降低内部活动增益都会增大误差变异，但对辅助信息的影响迥异：前者单调降低 $MI_e$，而后者会导致 $MI_e$ 呈现先升后降的倒U型。

### 7. 优点
*   **理论框架统一**：巧妙地将神经群体编码、概率估计理论（MLE）、信息论（$MI_e$）和信息几何（$I_{loss}$, 曲率）联系起来，为理解元认知的神经基础提供了连贯一致的理论基础。
*   **指标互补且解释性强**：提出了 $MI_e$ 和 $I_{loss}$ 两个互补的量化指标，并指出其本质上是JSD和JFD的推广。$MI_e$ 提供了与行为元认知敏感性直接对比的桥梁，$I_{loss}$ 则揭示了背后的几何本质。
*   **揭示关键差异**：一个核心且有力的发现是，即使行为（误差分布）相似，背后神经编码机制可能根本不同（如不同噪声模型），而这会极大影响信息的可用性。这对于模型选择和解释有重要意义。
*   **量化理论界限**：明确提出了 $MI_e$ 作为基于感知信号的元认知敏感性理论上限，为检验行为实验结果是否超出编码所能提供的信息提供了强有力的工具。

### 8. 不足与局限
*   **理想化模型假设**：理论框架建立在一系列理想化假设之上，如平移对称性（均匀调谐曲线覆盖）、独立噪声（部分模型）、以及使用MLE作为解码器。这些在生物神经网络中不一定严格成立。
*   **未建模动态与高阶结构**：未考虑神经元调谐的动态变化、复杂的神经元间协方差结构（除共享增益外）以及更复杂的解码策略（如贝叶斯解码、采样）。
*   **解码器特定**：分析建立在特定点估计器（MLE）之上。如果大脑使用不同的、非最优的读出机制，辅助信息的量化可能会有所不同。
*   **行为连接待验证**：虽然提出了 $MI_e$ 是元认知敏感性的理论上限，但论文停留在理论和仿真层面，并未将其与实际的动物行为或人类心理物理学数据进行直接拟合和比较。
*   **省略证明细节**：正文省略了关键公式的详细推导，核心证明放在附录中，可能影响阅读流畅性。

（完）
