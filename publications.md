---
layout: page
title: "Publications"
---

2021:
===
1. Singh, R. and Principe, J.C., 2021. **Quantifying Model Predictive Uncertainty with Perturbation Theory**. (Under Review) [(Paper Link)](https://arxiv.org/abs/2109.10888)
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

Singh, R. and Principe, J.C., 2019. **A New Uncertainty Framework for Stochastic Signal Processing**. [(Paper Link)](https://arxiv.org/abs/1904.13038)
<details>
<summary> Abstract </summary>
<br>
The fields of signal processing and information theory have evolved with the goal of developing formulations to extract intrinsic information from limited amount of data. When one considers the modeling of unpredictably varying processes and complex dynamical signals with a large number of unknowns (such as those encountered in the fields of finance, NLP, communications, etc.), there is a need for algorithms to have increased sensitivity with short spans of data, while maintaining stochastic generalization ability. This naturally calls for an increased focus on localized stochastic representation. So far, most metrics developed for characterizing signals envision data from entropic and probabilistic points of view that lack sensitivity towards quick changes in signal dynamics. We hypothesize that models that work with the intrinsic uncertainties associated with local data induced metric spaces would be significantly more sensitive towards signal characterization. To this end, we develop a new framework for stochastic signal processing that is based on decomposing the local metric space of the signal in a Gaussian Reproducing Kernel Hilbert Space (RKHS). A major advantage of our framework is that we are able to implement this decomposition on a sample-by-sample basis. The key aspects of our framework are the following: (1) We use a data defined metric related to Parzen density estimation for quantifying the local structure of data in the Gaussian RKHS. (2) We use a quantum description of this metric which consequently introduces uncertainty in the structure of the local kernel space. Since the RKHS has been well established and known for providing universal data fitting capabilities, we submit that local quantifiers of the kernel space data projection could significantly improve acquisition of signal information.
</details>

2018:
===

Singh, R. and Principe, J.C., 2018, July. **Correntropy based hierarchical linear dynamical system for speech recognition**. In 2018 International Joint Conference on Neural Networks (IJCNN) (pp. 1-7). IEEE. [(Paper Link)](https://ieeexplore.ieee.org/abstract/document/8489775)
<details>
<summary> Abstract </summary>
<br>
Hierarchical Linear Dynamical System (HLDS) is a recently introduced Kalman filter based generative state model that extracts relevant self-segmenting information from input time series signal by hierarchically constraining the information representing subspaces of its states thus slowing down the dynamics of the input signal. Despite the simplicity of its nested architecture and its dependance on linear Kalman update rules, the HLDS has been shown to have state-of-the-art performance in the classification of musical notes. However, it was observed that the application scope of this state based model was only limited to linearly separable signals since the representations of non-linear and non-stationary signals (such as speech) in the state space of the HLDS was highly intermingled and hence, non-discriminative. This paper proposes a kernel based extension of the HLDS that shows promising results in the sparse and discriminative representation of speech phonemes in its information representing state spaces. Specifically, we use correntropy as an additional non-linear constraint on top of the linear constraints already provided by the nested architecture of the states. We show that by using correntropy as the cost function in the Kalman update equations, we are able to adaptively restrict the different phonemes of a speech signal into localized areas of the top state space. Our training results, along with their authentication through top-down inference of the states, provide valid credibility to the use of HLDS as a promising speech recognition model.
 </details>

2015:
===

Singh, R., Sekhsaria, S. and Kulandhaivelu, S., **Novel Rotor Position Estimation Technique For Switched Reluctance Motor Using Vibration Signature Analysis**. National Power Electronics Conference (NPEC) 2013. [(Paper Link - PDF)](https://www.ee.iitb.ac.in/npec/Papers/Program/NPEC_2015_paper_62.pdf)
<details>
<summary> Abstract </summary>
<br>
In this paper, we present a novel technique to estimate the position of the rotor of a switched reluctance motor by observing the characteristics of the vibration of the stator during the motor operation. This removes the need of the shaft position sensor which is known for its unreliability and problems associated with its application. Vibration in switched reluctance motors is generated mainly due to stator deformation as a result of radial forces caused by the magnetic flux. The magnetic flux density varies significantly with the rotor position depending upon the alignment of the poles of the rotor and the stator. Thus, at different rotor positions, the vibration amplitude recorded at a particular point on the stator lamination varies. This makes it possible to correlate rotor position with the stator vibration pulses. We have carried out simulations on a 6/4 SR motor to demonstrate this position estimation technique. Initially, we generate vibration pulses separately in the simulation with respect to the flux density keeping the point above a particular stator pole as the frame of reference. This is done to closely approximate and simulate the data recorded by an accelerometer imagined to be installed at that point. We have used the characteristics determined and the analysis made on the vibration of SR motors by previous research experiments to generate the vibration pulses with respect to the flux. We then estimate the rotor position by detecting the regular spikes in vibration and then compare it with the actual position of the rotor. We find that although the resolution of the rotor position measurement using our technique is not very high at low speeds, this method is highly efficient at high rotor speeds and it requires less computational power thereby saving costs. We analyze our technique in detail and outline its several key advantages when compared to other position estimation schemes for SR motors.
 </details>

2013:
===
Singh, R., Umashankar, S., Vijaykumar, D. and Kothari, D.P., 2013, April. **Dynamic braking of induction motor-Analysis of conventional methods and an efficient multistage braking model**. In 2013 International Conference on Energy Efficient Technologies for Sustainability (pp. 197-206). IEEE. [(Paper Link)](https://ieeexplore.ieee.org/abstract/document/6533382)
<details>
<summary> Abstract </summary>
<br>
In this paper, a detailed analysis is made on capacitor self excitation and DC injection methods of dynamic braking of induction motor through MATLAB/SIMULINK simulations. The effectiveness of these conventional dynamic braking methods is carefully analyzed while changing various parameters. The speed range and time duration for which these methods are the most effective is carefully observed during changing load conditions. The effects of changing capacitor values and DC injection voltage levels on the effective speed range have been studied and the time durations in which these methods are most effective are also analyzed. Using the analysis data obtained, the parameters of a reliable fast multistage dynamic braking model are arrived upon for its best possible performance. The performance of this model, which efficiently dissipates the kinetic energy of the motor in a very short duration of time, is checked through simulations.
</details>
