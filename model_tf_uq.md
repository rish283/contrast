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

<br />

## Transfer Learning
For transfer learning, a model is first pre-trained on a source dataset, and then then fine tuned on the target dataset on which predictions are to be made. All layers are frozen after pre-training, except for the last layer which is trained on the target dataset.

<br />

## Results (UCI Datasets)
We used a 1-D Fully Convolutional Network (FCN) architecture that achieves state-of-the-art results on UCI times series classification datasets. Transfer learning was implemented using different UCI datasets as source and the rest of datasets as targets. MC Dropout and QIPF methods were implemented on the network (at each source-target example) for quantifying overall predictive uncertainties of the network on the test-sets of the target dataset (after pre-training and fine-tuning).

<figure>
<img style="float: center" src="/tfres.jpg">
<figcaption align = "center"><b>Correlations between Test Errors and UQ Values: The QIPF uncertainties (for all source-target pairs) can be seen to be highly correlated with the corresponding model test-set errors.</b></figcaption>
</figure>    

Correlation coefficient between errors and uncertainty estimates:
<br />
MC Dropout: 0.71
<br />
QIPF: 0.85
    
<br />
    
## Results (ImageNet - KMNIST)
A VGG-16 network was pre-trained on ImageNet dataset finetuned on kuzushiji-MNIST data. Uncertainty was quantified by decomposing QIPF of finutuned layer weights in the field created by pretrained layer weights.
    
<figure>
<img style="float: center" src="/tfres1.jpg">
<figcaption align = "center"><b>Transfer Learning Uncertainty Quantification Example (ImageNet - KMNIST): Left - depiction of model architecture and method for quantifying performance of UQ techniques. Right - AUROC results of MC-dropout and QIPF in test-set error detection.</b></figcaption>
</figure> 
