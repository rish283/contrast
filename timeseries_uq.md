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
    
We leverage a Gaussian RKHS based uncertainty decomposition framework (the QIPF) as a "dynamic potential field" for the analysis of time series data. This leads to an energy-based formulation of the time series signal that is now represented in terms of multiple moments of uncertainty at each data sample. Preliminary experiments show that QIPF features of time series data can be very useful for applications like anomaly detection and clustering.
  
<br />
<!-- <br /> -->
<!-- <br /> -->
<!-- <br /> -->
    
## Goal:

<br />
<br />
The problem is further made challenging by covariate shift of the test-set so that underlying distribution of input test data changes from $p(x|\lambda)$ during training to $p(x^*|\gamma)$ during testing (where $\lambda$ and $\gamma$ are parameters of the underlying distributions), while the target conditional distribution remains the same, i.e. $$p(y|x) = p(y^*|x^*)$$.
    
<br />
