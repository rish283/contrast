---
layout: page
title: "Research Work:"
---

<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
    }
});
MathJax.Hub.Queue(function() {
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>

<ins>RKHS based Physical Interpretation of Model Uncertainty: The QIPF</ins>
===
<img style="float: left; padding-right:25px" src="/fm3.JPG" width="55%" height="55%">In this work, we combine the expressive power of the Gaussian reproducing kernel Hilbert space (RKHS) and high local resolution of quantum physics to create a framework, called the quantum information potential field (QIPF), for quantifying the predictive uncertainty of a neural network model. We show that the QIPF is significantly more precise, better calibrated and much faster than typical Bayesian approaches, especially in situations involving distributional shifts in the test-set.
<br />
<br />
<br />
<!-- <br /> -->
Goal:
---
Consider a $k$-class classification problem with training dataset $$\mathbf{D} = \{x_{i}, y_{i}\}_{i=1}^N$$ consisting of $d$-dimensional input vectors $x_i \in \mathbb{R}^d$ and the corresponding target labels $y_i \in \{1...k\}$. Assume that a point-prediction neural network with weights $\mathbf{w}$ learns an implicit distribution $p(y|x, \mathbf{w})$ and its output corresponding to a test input $$x^*$$ is $$y^*$$. **Our goal is to come up with a pseudo-probability (or uncertainty) measure for the true implicit posterior predictive PDF $$p(y^*|x^*, \mathbf{w})$$.**
<br />
<br />
The problem is further made challenging by covariate shift of the test-set so that underlying distribution of input test data changes from $p(x|\lambda)$ during training to $p(x^*|\gamma)$ during testing (where $\lambda$ and $\gamma$ are parameters of the underlying distributions), while the target conditional distribution remains the same, i.e. $$p(y|x) = p(y^*|x^*)$$.
    
Approach: 
---
A Bayesian approach to accomplish this involves methods for approximating the posterior predictive PDF of the model (a problem of marginalization over weights): $$p(y^*|x^*, \mathbf{D}) = \int{p(y^*|x^*, \mathbf{w})p(\mathbf{w}|\mathbf{D})d\mathbf{w}}$$.
<br />
<br />
Our approach: Quantify the local gradient flow (heterogeneity) of $$p(y^*|x^*, \mathbf{w})$$. In other words, quantify how optimized weight $\mathbf{w}$ are to make predictions in the vicinity of $$y^*$$. This is done in the three steps:
    <br />
    1. Projection (mean embedding) of weights in a Gaussian RKHS to estimate the implicit weight PDF: $$p(y^*|x^*, \mathbf{w}) \approx \psi_{\mathbf{w}}(y^*) = \frac{1}{n}\sum_{t=1}^{n}G_\sigma(w_t, y^*)$$.
    <br />
    2. Quantification of local gradient flow of $$p(y^*|x^*, \mathbf{w})$$ using Laplacian operator based formulation: $$\nabla_y^2\psi_\mathbf{w}(y^*) \approx p(y^* + \Delta{y^*}|x^*, \mathbf{w}) - p(y^*|x^*, \mathbf{w})$$.
    <br />
    3. Moment decomposition of $$\nabla_y^2\psi_\mathbf{w}(y^*)$$ for high resolution information extraction of heterogeneity: $$\nabla_y^2\psi_\mathbf{w}(y^*) = \psi_\mathbf{w}^0(y^*) + \lambda\psi_\mathbf{w}^1(y^*) + \lambda^2\psi_\mathbf{w}^2(y^*) + ...$$.
    <br />
Inspired by quantum mathematics we propose to use the Schrodinger’s equation, which includes the Laplacian of the wavefunction, to estimate the local gradient flow of $\psi_\mathbf{w}$. Unlike quantum mechanics that utilizes an Hilbert space, we will be estimating the solution in a RKHS, with the great advantage that we can use the kernel trick to compute the solution in the input space, directly from samples:
    <br />
       $$H_0^k = E_\mathbf{w}^k + (\sigma^2/2)\frac{\nabla_y^2\psi_\mathbf{w}^k}{\psi_\mathbf{w}^k}$$
    
Illustrative Results: 
---
    
Related Papers: 
---
Singh, R. and Principe, J.C., 2021. **Quantifying Model Predictive Uncertainty with Perturbation Theory**. (Under Review) [(Paper Link)](https://arxiv.org/abs/2109.10888)
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
    
    
