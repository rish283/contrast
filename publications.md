---
layout: page
title: "Publications"
---

2021:
===
Singh, R. and Principe, J.C., 2021. **Quantifying Model Predictive Uncertainty with Perturbation Theory**. [(Paper Link)](https://arxiv.org/abs/2109.10888)
<details>
<summary> Abstract </summary>
<br>
We propose a framework for predictive uncertainty quantification of a neural network that replaces the conventional Bayesian notion of weight probability density function (PDF) with a physics based potential field representation of the model weights in a Gaussian reproducing kernel Hilbert space (RKHS) embedding. This allows us to use perturbation theory from quantum physics to formulate a moment decomposition problem over the model weight-output relationship. The extracted moments reveal successive degrees of regularization of the weight potential field around the local neighborhood of the model output. Such localized moments represent well the PDF tails and provide significantly greater accuracy of the model's predictive uncertainty than the central moments characterized by Bayesian and ensemble methods or their variants. We show that this consequently leads to a better ability to detect false model predictions of test data that has undergone a covariate shift away from the training PDF learned by the model. We evaluate our approach against baseline uncertainty quantification methods on several benchmark datasets that are corrupted using common distortion techniques. Our approach provides fast model predictive uncertainty estimates with much greater precision and calibration.
</details>

Singh, R. and Principe, J.C., 2021. **Toward a Kernel-Based Uncertainty Decomposition Framework for Data and Models**. Neural Computation, 33(5), pp.1164-1198. [(Paper Link)](https://arxiv.org/abs/2001.11495) 
<details>
<summary> Abstract </summary>
<br>
This letter introduces a new framework for quantifying predictive uncertainty for both data and models that relies on projecting the data into a gaussian reproducing kernel Hilbert space (RKHS) and transforming the data probability density function (PDF) in a way that quantifies the flow of its gradient as a topological potential field (quantified at all points in the sample space). This enables the decomposition of the PDF gradient flow by formulating it as a moment decomposition problem using operators from quantum physics, specifically Schrödinger's formulation. We experimentally show that the higher-order moments systematically cluster the different tail regions of the PDF, thereby providing unprecedented discriminative resolution of data regions having high epistemic uncertainty. In essence, this approach decomposes local realizations of the data PDF in terms of uncertainty moments. We apply this framework as a surrogate tool for predictive uncertainty quantification of point-prediction neural network models, overcoming various limitations of conventional Bayesian-based uncertainty quantification methods. Experimental comparisons with some established methods illustrate performance advantages that our framework exhibits.
</details>


2020:
===

Singh, R. and Principe, J., 2020, August. **Time Series Analysis using a Kernel based Multi-Modal Uncertainty Decomposition Framework**. In Conference on Uncertainty in Artificial Intelligence (pp. 1368-1377). PMLR. [(Paper Link)](http://proceedings.mlr.press/v124/singh20a.html)
<details>
<summary> Abstract </summary>
<br>
This paper proposes a kernel based information theoretic framework with quantum physical underpinnings for data characterization that is relevant to online time series applications such as unsupervised change point detection and whole sequence clustering. In this framework, we utilize the Gaussian kernel mean embedding metric for universal characterization of data PDF. We then utilize concepts of quantum physics to impart a local dynamical structure to characterized data PDF, resulting in a new energy based formulation. This facilitates a multi-modal physics based uncertainty representation of the signal PDF at each sample using Hermite polynomial projections. We demonstrate in this paper using synthesized datasets that such uncertainty features provide a better ability for online detection of statistical change points in time series data when compared to existing non-parametric and unsupervised methods. We also demonstrate a better ability of the framework in clustering time series sequences when compared to discrete wavelet transform features on a subset of VidTIMIT speaker recognition corpus.
</details>


R. Singh, S. Yu and J. C. Principe. **Composite Dynamic Texture Synthesis Using Hierarchical Linear Dynamical System**. ICASSP 2020 - 2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2020, pp. 2757-2761, doi: 10.1109/ICASSP40776.2020.9054084. [(Paper Link)](https://ieeexplore.ieee.org/abstract/document/9054084)
<details>
<summary> Abstract </summary>
<br>
We demonstrate that a systematic inclusion of prior structural constraints on the states of a linear dynamical system significantly improves its ability to model complex multidimensional sequences. This constrained LDS, typically termed as the hierarchical linear dynamical system (HLDS), is a Kalman filter based topology that extracts relevant self-segmenting information from the input signal in an unsupervised manner by hierarchically constraining its information representing state subspaces thereby slowing down the signal dynamics. We highlight some of its practical advantages over the existing methods in real-world video applications. As a concrete application, we show that the HLDS, despite being a linear model trained in an unsupervised setting, is able to capture the dynamics of complex texture sequences consisting of multiple co-occurring textures. We compare its performance with a similarly trained LDS model in the reconstruction and synthesis of such signals.
 </details>
  
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
