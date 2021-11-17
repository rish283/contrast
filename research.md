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

<center> <h1> <ins>RKHS based Physical Interpretation of Model Uncertainty: The QIPF</ins> </h1> </center>
<!-- <center>
<ins>RKHS based Physical Interpretation of Model Uncertainty: The QIPF</ins>
</center>
=== -->

<figure>
<img style="float: center" src="/kk1.jpg">
<figcaption align = "center"><b>Approach: Moments extracted from the local interaction of the model output with the RKHS potential field of the weights quantify the output uncertainty.</b></figcaption>
</figure>

We combine the expressive power of the Gaussian reproducing kernel Hilbert space (RKHS) and the high local resolution provided by quantum physics to create a moment decomposition framework for quantifying the predictive uncertainty of neural network models. The framework, called the quantum information potential field (QIPF), replaces the convention Bayesian notion of weight PDF with a physics based potential field representation of the models weights in a Gaussian RKHS. The QIPF moments quantify predictive uncertainty of a model by measuring the local interaction of the model prediction with its weight potential field. We show that the QIPF uncertainty measures are much more precise and better calibrated than Bayesian methods, especially in presence of distributional shifts in test-set, while being much cheaper to compute. 
<br />
<!-- <br /> -->
<!-- <br /> -->
<!-- <br /> -->
    
[Click here to read more!](/model_uq.md)

---
    
<center> <h1> <ins>Transfer Learning Uncertainty Quantification using QIPF (ongoing)</ins> </h1> </center>

<figure>
<img style="float: center" src="/tffm1.jpg">
<figcaption align = "center"><b>Approach: Moments extracted from the local interaction of the fine-tuned layer weights with the RKHS potential field created by source layer weights quantify the overall uncertainty in modeling target dataset.</b></figcaption>
</figure>
    
We extend the application of QIPF for quantifying transfer learning uncertainty. Here, we utilize the QIPF to quantify the overall predictive uncertainty of a model originally trained on a source dataset and then fine-tuned on a target dataset by evaluating the weights of the fine-tuned layers on the RKHS potential field created by source layer weights. This gives the discrepancy (with respect ot the model) between source and target datasets.
    
[Click here to read more!](/model_tf_uq.md)
    
---
    
<center> <h1> <ins>Time Series Data Analysis using Kernel Uncertainty Framework</ins> </h1> </center>
    
<figure>
<img style="float: center" src="/frmm.jpg">
<figcaption align = "center"><b>Decomposition of time series signal using QIPF uncertainty framework.</b></figcaption>
</figure>
    
In this work, we utilize the QIPF, an RKHS based uncertainty decomposition framework, to obtain a physical viewpoint of time series signal dynamics. More concretely, we leverage the QIPF as a dynamic potential field (embedding space) that automatically and sensitively adapts its local structure according to data, for the analysis of time series signals. We consequently arrive at an energy-based formulation of the time series signal that is now represented in terms of multiple moments of uncertainty at each data sample. Preliminary experiments show that QIPF features of time series data can be very useful for applications like anomaly detection and clustering.
    
[Click here to read more!](/timeseries_uq.md)
    
---
    
<center> <h1> <ins>Hierarchical Linear Dynamical System</ins> </h1> </center>
The Hierarchical Linear Dynamical System (HLDS) is a modified Kalman filter based topology of linear dynamical system (LDS) where we impose prior structural constraints of systematically varying proportions on the states. This induces unsupervised clustering of signal dynamics (being modeled by the LDS) at its most constrained states, thereby naturally improving its ability to model complex data sequences. I made the following contributions in the development and application of this algorithm. 
     <br />
    1. Demonstrated a better ability of the HLDS in modeling layered dynamic textures (a complex multi-dimensional and multi-dynamical data sequence where one or more texture videos are imposed over another) when compared with LDS: [click here to visit paper for details](/https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9054084)
    <br />
    2. Introduced Correntropy cost function for the HLDS to further improve its localization ability of the signal in its constrained states. This made it possible for the HLDS (despite being a linear algorithm) to cluster different speech phonemes. [click here to visit paper for details](/https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8489775)
    <br />
