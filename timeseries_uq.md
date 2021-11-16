---
header-includes:
  - \usepackage{algorithm}
  - \usepackage{algpseudocode}
  - \usepackage{algorithmic}
  - \usepackage{algorithm2e}
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
  
<center> <h1> <ins>Time Series Data Analysis using Kernel Uncertainty Framework</ins> </h1> </center>
    
<figure>
<img style="float: center" src="/frmm.jpg">
<figcaption align = "center"><b>Proposed decomposition of time series signal using QIPF uncertainty framework.</b></figcaption>
</figure>
 
In this work, we utilize the QIPF, an RKHS based uncertainty decomposition framework, to obtain a physical viewpoint of time series signal dynamics. More concretely, we leverage the QIPF as a dynamic potential field (embedding space) that automatically and sensitively adapts its local structure according to data, for the analysis of time series signals. We consequently arrive at an energy-based formulation of the time series signal that is now represented in terms of multiple moments of uncertainty at each data sample. Preliminary experiments show that QIPF features of time series data can be very useful for applications like anomaly detection and clustering.

<br />
<!-- <br /> -->
<!-- <br /> -->
<!-- <br /> -->

## Goal:
Our conjecture is that the best way to model non-stationary features of a time series signal is to use a dynamic embedding space that changes its local structure based on the evolution of the signal. To this end, we propose to utilize the QIPF uncertainty framework that, through its multiple uncertainty modes at each sample, is able to quantify local data dynamics relative to the signal's PDF in an unsupervised manner with high sensitivity and specificity. Through the use of the QIPF, we utilize concepts of quantum physics (which provides a principled quantification of particle-particle dynamics in a physical system) to interpret data. Consequently we introduce a new information theoretic framework to accomplish pattern recognition tasks associated with time series data that quantifies sample-by-sample dynamics of the signal (important in online time series analysi, which is not achievable by conventional methods.
<br />
<!-- <br />
The problem is further made challenging by covariate shift of the test-set so that underlying distribution of input test data changes from $p(x|\lambda)$ during training to $p(x^*|\gamma)$ during testing (where $\lambda$ and $\gamma$ are parameters of the underlying distributions), while the target conditional distribution remains the same, i.e. $$p(y|x) = p(y^*|x^*)$$. -->
## Approach:
Our approach consists of three main steps:
 <br />
 <br />
($$\mathbf{1}$$). Estimation of PDF at a sample at time $$t$$ using information potential field (empirical estimate of kernel mean embedding): 
 <br />
 <br />
 $$p(x^t|x^0, x^1 ... x^{t-1}) \approx \psi_{\mathbf{x}}(x^t) = \frac{1}{n}\sum_{k=1}^{t-1}G_\sigma(x_k, x^t)$$.
    
---
    
($$\mathbf{2}$$). A Schrödinger's equation formulation over data PDF by assuming the IFP, $$\psi_{\mathbf{x}}(x^t)$$, to be a wave-function. This transforms the static PDF measure (the IPF) into a dynamic embedding that measures the local changes in the PDF at $$x^t$$: 
<br />
<br />
$$H_(x^t) = E_\mathbf{w}(x^t) + (\sigma^2/2)\frac{\nabla_y^2\psi_\mathbf{w}(x^t)}{\psi_\mathbf{w}(x^t)}$$ 
    
---
    
($$\mathbf{3}$$). Moment decomposition of $$H$$ to extract various uncertainty modes at $$x^t$$ which serve as dynamical features of the time-series at time t:
<br />
<br />
$$H^k(x^t) = E_\mathbf{w}^k(x^t) + (\sigma^2/2)\frac{\nabla_y^2\psi_\mathbf{w}^k(x^t)}{\psi_\mathbf{w}^k(x^t)}$$.
<br />
<br />
These stochastic features $$H^0(x^t), H^1(x^t), H^2(x^t) ...$$ are then utilized for applications like clustering or detection of change points in the time-series.

---
    
<figure>
<img style="float: center" src="/qspd7.jpg">
<figcaption align = "center"><b>Detailed depiction of approach: QIPF uncertainty decomposition of a time series.</b></figcaption>
</figure>
    
---

##Algorithm:
A pseudo-code for QIPF implementation is as follows:
<!-- \begin{algorithm}[H]
\caption{Quantum decomposition of IPF}\label{euclid}
\begin{algorithmic}
\State \textbf{Input:}
\State $x$: Signal
\State $\sigma$: Kernel width
\State $m$: Number of quantum modes
\State \textbf{Initialization:}
\State $\psi$: Wave-function
\State $\psi^1, \psi^2, ... , \psi^m$: Wave-function Hermitian embeddings
\State $V_s^1, V_s^2, ... , V_s^m$: QIPF modes
\State $E^1, E^2, ... , E^m$: Eigenvalue of each mode
\State \textbf{Computations:}
\For {$i = $ 1 to length($x$)}
\State $\psi=0$
\For {$j = $ 1 to i}
\State $\psi \gets \psi + e^{-\frac{(x_i - x_j)^2}{2\sigma^2}}$
\EndFor
\State $\psi_i \gets \sqrt{mean(\psi)}$
\State 
\State $[\psi_i^1, \psi_i^2, ... , \psi_i^m] \gets Hermite  Projections(\psi_i)$
\State $[{\nabla^2}\psi_i^1, ... , {\nabla^2}\psi_i^m] \gets Laplacians$ %_\psi(\psi_i^2\psi_i^4...\psi_i^m)
\State 
\For {each mode $k$}
\State $E_i^k = -\min_{q=1...i}\frac{\sigma^2/2{\nabla^2}\psi_q^k}{\psi_q^k}$
\State
\State $V_{s(i)}^k = E_i^k + \frac{\sigma^2/2{\nabla^2}\psi^k}{\psi^k}$
\EndFor
\EndFor
\end{algorithmic}
\end{algorithm} -->

    
    
<figure>
<img style="float: center" src="/alg.jpg">
<figcaption align = "center"><b>Detailed depiction of approach: QIPF uncertainty decomposition of a time series.</b></figcaption>
</figure>

[Return to research page](https://singhrish.com/research/)
