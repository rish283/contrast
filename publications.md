---
layout: page
title: "Publications"
---

2021:
===
<details>
<summary>Singh, R. and Principe, J.C., 2021. **Quantifying Model Predictive Uncertainty with Perturbation Theory**.</summary> [arXiv preprint arXiv:2109.10888](https://arxiv.org/abs/2109.10888)
<br>
We propose a framework for predictive uncertainty quantification of a neural network that replaces the conventional Bayesian notion of weight probability density function (PDF) with a physics based potential field representation of the model weights in a Gaussian reproducing kernel Hilbert space (RKHS) embedding. This allows us to use perturbation theory from quantum physics to formulate a moment decomposition problem over the model weight-output relationship. The extracted moments reveal successive degrees of regularization of the weight potential field around the local neighborhood of the model output. Such localized moments represent well the PDF tails and provide significantly greater accuracy of the model's predictive uncertainty than the central moments characterized by Bayesian and ensemble methods or their variants. We show that this consequently leads to a better ability to detect false model predictions of test data that has undergone a covariate shift away from the training PDF learned by the model. We evaluate our approach against baseline uncertainty quantification methods on several benchmark datasets that are corrupted using common distortion techniques. Our approach provides fast model predictive uncertainty estimates with much greater precision and calibration.
</details>

<details>
<summary>Singh, R. and Principe, J.C., 2021. **Toward a Kernel-Based Uncertainty Decomposition Framework for Data and Models**. Neural Computation, 33(5), pp.1164-1198.</summary> (https://arxiv.org/abs/2001.11495)
<br>
This letter introduces a new framework for quantifying predictive uncertainty for both data and models that relies on projecting the data into a gaussian reproducing kernel Hilbert space (RKHS) and transforming the data probability density function (PDF) in a way that quantifies the flow of its gradient as a topological potential field (quantified at all points in the sample space). This enables the decomposition of the PDF gradient flow by formulating it as a moment decomposition problem using operators from quantum physics, specifically Schrödinger's formulation. We experimentally show that the higher-order moments systematically cluster the different tail regions of the PDF, thereby providing unprecedented discriminative resolution of data regions having high epistemic uncertainty. In essence, this approach decomposes local realizations of the data PDF in terms of uncertainty moments. We apply this framework as a surrogate tool for predictive uncertainty quantification of point-prediction neural network models, overcoming various limitations of conventional Bayesian-based uncertainty quantification methods. Experimental comparisons with some established methods illustrate performance advantages that our framework exhibits.
</details>


2020:
===

Singh, R. and Principe, J., 2020, August. **Time Series Analysis using a Kernel based Multi-Modal Uncertainty Decomposition Framework**. In Conference on Uncertainty in Artificial Intelligence (pp. 1368-1377). PMLR.

2019:
===

2018:
===

2017:
===

2015:
===

2013:
===
