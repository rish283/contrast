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
  
<center> <h1> <ins>Transfer Learning Uncertainty Quantification using QIPF (ongoing)</ins> </h1> </center>

<figure>
<img style="float: center" src="/tffm1.jpg">
<figcaption align = "center"><b>Proposed approach: Moments extracted from the local interaction of the fine-tuned layer weights with the RKHS potential field created by source layer weights quantify the overall uncertainty in modeling target dataset.</b></figcaption>
</figure>

We extend the application of QIPF for quantifying transfer learning uncertainty. Here, we utilize the QIPF to quantify the overall predictive uncertainty of a model originally trained on a source dataset and then fine-tuned on a target dataset by evaluating the weights of the fine-tuned layers on the RKHS potential field created by source layer weights. This gives the discrepancy (with respect ot the model) between source and target datasets.
