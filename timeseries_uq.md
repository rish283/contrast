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
  
<center> <h1> <ins>Time Series Data Analysis using Kernel Uncertainty Framework</ins> </h1> </center>
    
<figure>
<img style="float: center" src="/frmm.jpg">
<figcaption align = "center"><b>Proposed decomposition of time series signal using QIPF uncertainty framework.</b></figcaption>
</figure>
In this work, we utilize the QIPF, an RKHS based uncertainty decomposition framework, to obtain a physical viewpoint of time series signal dynamics. More concretely, we leverage the QIPF as a dynamic potential field (embedding space) that automatically and sensitively adapts its local structure according to data, for the analysis of time series signals. We consequently arrive at an energy-based formulation of the time series signal that is now represented in terms of multiple moments of uncertainty at each data sample. Preliminary experiments show that QIPF features of time series data can be very useful for applications like anomaly detection and clustering. The main idea here is to introduce a new information theoretic framework to accomplish pattern recognition tasks associated with time series data that is usually not achievable by classical information theoretic methods due to their inability to quantify sample-by-sample dynamics of the signal (important in online time series analysis). It is for this reason that we look towards quantum physics, which provides a principled quantification of particle-particle dynamics in a physical system, to interpret data.

<br />
<!-- <br /> -->
<!-- <br /> -->
<!-- <br /> -->

## Goal:
Our conjecture is that the best way to model non-stationary features of a time series signal is to use a dynamic embedding space that changes its local structure based on the evolution of the signal. To this end, we propose to utilize the QIPF uncertainty framework that, through its multiple uncertainty modes at each sample, is able to quantify local data dynamics relative to the signal's PDF in an unsupervised manner with high sensitivity and specificity.
<br />
<!-- <br />
The problem is further made challenging by covariate shift of the test-set so that underlying distribution of input test data changes from $p(x|\lambda)$ during training to $p(x^*|\gamma)$ during testing (where $\lambda$ and $\gamma$ are parameters of the underlying distributions), while the target conditional distribution remains the same, i.e. $$p(y|x) = p(y^*|x^*)$$. -->
## Approach:


<br />
