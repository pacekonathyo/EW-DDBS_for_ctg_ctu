# EW-DDBS: Entropy-Weighted Dynamic Density-Based Sampling for Cardiotocographic Fetal Distress Classification

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=Jupyter)](https://jupyter.org/try)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.20+-FF6F00?logo=tensorflow)](https://tensorflow.org)

This repository contains the official implementation of the paper:

> **EW-DDBS: Latent-Guided Safe-Region Oversampling with Entropy Weighting for Cardiotocographic Fetal Distress Classification**  
> *Ahmad Ilham, Catur Supriyanto, Machmudah, Laelatul Khikmah*  
> Submitted to a Q1 journal (Elsevier)

The proposed framework addresses extreme class imbalance in fetal distress classification by coupling a lightweight 1D‑CNN latent topology guide with a safe‑region weighting mechanism and optional Tomek‑Link cleaning.

## 🔍 Abstract (brief)

Automated cardiotocography (CTG) interpretation is hampered by extreme class imbalance (pathological cases <10%). Conventional oversamplers often inject noise into overlapping decision regions. **EW‑DDBS** introduces a hybrid weighting function that combines:
- Shannon entropy from a 1D‑CNN softmax head (uncertainty),
- multi‑scale $k$‑NN Safe‑Ratio in the latent manifold (local consistency).

Synthesis is performed in the original input space to preserve clinical interpretability, followed by Tomek‑Link boundary cleaning. The framework is evaluated on two cohorts (UCI CTG and CTU‑UHB) across 15 downstream classifiers with leakage‑controlled cross‑validation.

## 🚀 Getting Started

### Prerequisites

- Python 3.9 or higher
- TensorFlow 2.20.0
- Other libraries: numpy, pandas, scikit-learn, imbalanced-learn, xgboost, scikit-posthocs, shap, wfdb, etc.

All dependencies can be installed using the provided `requirements.txt`:

```bash
pip install -r requirements.txt
