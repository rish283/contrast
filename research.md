---
layout: page
title: "PhD Research:"
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
<img style="float: left; padding-right:25px" src="/fm3.JPG" width="55%" height="55%">In this work, we combine the expressive power of the Gaussian reproducing kernel Hilbert space (RKHS) and accuracy of quantum physics to create a framework, called the quantum information potential field (QIPF), for quantifying the predictive uncertainty of a neural network model. We show that the QIPF is significantly more precise, better calibrated and much faster than typical Bayesian approaches, especially in situations involving distributional shifts in the test-set.
<br />
<!-- <br /> -->
<!-- <br />
<br /> -->

Goal: 
---
Consider a $k$-class classification problem with training dataset $\mathbf{D} = \{x_{i}, y_{i}\}_{i=1}^N$ consisting of $d$-dimensional input vectors $x_i \in \mathbb{R}^d$ and the corresponding target labels $y_i \in \{1...k\}$. Assume that a point-prediction neural network with weights $\mathbf{w}$ learns an implicit distribution $p(y|x, \mathbf{w})$ and its output corresponding to a test input $\hat{x}$ is $\hat{y}$. <ins>Our goal is to best estimate probability envelope $p(\hat{y}|\hat{x}, \mathbf{w})$ </ins>.
<br />
The problem is further made challenging by test-set covariate shift so that underlying distribution of input test data changes from $p(x|\lambda)$ during training to $p(\hat{x}|\gamma)$ during testing (where $\lambda$ and $\gamma$ are parameters of the underlying distribution), while the target conditional distribution remains the same, i.e. $p(y|x) = p(\hat{y}|\hat{x}).
