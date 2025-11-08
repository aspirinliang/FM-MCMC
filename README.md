# Flow-Matching MCMC (FM-MCMC) for EMRI Inference

This repository provides the implementation of **Flow-Matching Markov Chain Monte Carlo (FM-MCMC)**, a novel Bayesian framework designed for **Extreme Mass-Ratio Inspiral (EMRI)** gravitational wave parameter estimation. The method integrates **continuous normalizing flows (CNFs)** with **parallel tempering MCMC (PT-MCMC)**, achieving both efficiency and statistical reliability.  

The code accompanies our paper:  
> **Unlocking New Paths for Science with Extreme-Mass-Ratio Inspirals: Machine Learning-Enhanced MCMC for Accurate Parameter Inversion**  
> Bo Liang, Chang Liu, Hanlin Song, Zhenwei Lyu, Minghui Du, Peng Xu, et al.

---

## 🔍 Background
- **EMRI signals** are prime sources for space-based gravitational-wave detectors (Taiji, LISA).  
- Traditional **MCMC methods** face severe challenges:  
  - prohibitively high computational costs,  
  - highly multimodal likelihoods with many local maxima,  
  - sensitivity to initialization.  

---

## 🚀 Method
**FM-MCMC** addresses these challenges by combining:  
1. **Flow Matching (FMPE):**  
   - Uses continuous normalizing flows to learn high-likelihood regions efficiently.  
   - Provides informed initialization to reduce the chance of trapping in local maxima.  

2. **Parallel Tempering MCMC (PT-MCMC):**  
   - Performs fine-grained posterior sampling starting from FMPE proposals.  
   - Ensures unbiased exploration of the parameter space.  

Together, FM-MCMC achieves **orders-of-magnitude speed-up** while maintaining **accurate and unbiased posterior estimation**.

---

## 📊 Key Results
- Tested on simulated EMRI signals (Taiji noise model).  
- **Intrinsic parameters** ($M, \mu, a, e_0$) recovered within 1σ posterior intervals for bright EMRI sources ($\text{SNR} > 60$).  
- Compared with **Eryn** (a state-of-the-art PT-MCMC sampler):  
  - FM-MCMC converges faster and avoids local maxima,  
  - Provides statistically reliable results under realistic noise conditions.  

---

## 🛠 Installation


---

## ▶️ Usage


---

## 📖 Citation
If you use this code, please cite our paper:
```bibtex
@misc{liang2025estimatingorbitalparametersdirect,
      title={Estimating Orbital Parameters of Direct Imaging Exoplanet Using Neural Network}, 
      author={Bo Liang and Hanlin Song and Chang Liu and Tianyu Zhao and Yuxiang Xu and Zihao Xiao and Manjia Liang and Minghui Du and Wei-Liang Qian and Li-e Qiang and Peng Xu and Ziren Luo},
      year={2025},
      eprint={2510.17459},
      archivePrefix={arXiv},
      primaryClass={astro-ph.EP},
      url={https://arxiv.org/abs/2510.17459}, 
}
```

---

