# 🌾 Resource-Constrained CNN for Edge Image Classification

![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Enabled-red.svg)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Project Overview
This project focuses on the automated classification of agricultural rice grains (5 varieties: *Arborio, Basmati, Ipsala, Jasmine, and Karacadag*) using Convolutional Neural Networks (CNNs) optimized for **extreme edge devices**. 

Targeted for deployment on an **automated agricultural sorting machine** running on resource-constrained microcontrollers, we designed and evaluated a custom **Depthwise-Separable CNN (Model B)** strictly constrained to under 100,000 trainable parameters, benchmarked against a standard baseline CNN (Model A) and fine-tuned lightweight SOTA architectures (MobileNetV2 and EfficientNetB0).

---

### 🚀 Key Achievements & Benchmark Results
All models were evaluated on a held-out test set of **11,250 images** (downscaled to $64 \times 64 \times 3$ resolution from the 75,000-image Kaggle Rice Dataset):

| Model | Architecture Type | Total Params | Model Size (.h5) | MACs | Test Accuracy |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Model A** | Standard CNN Baseline | 1,142,597 | 13.12 MB | 42.6 M | **99.55%** |
| **Model B (Ours)** | **Depthwise-Separable CNN** | **79,168** (<100k) | **0.97 MB (994 KB)** | **7.6 M** | **97.99%** |
| **MobileNetV2** | SOTA Transfer Learning | 2,422,597 | 10.85 MB | 25.2 M | 98.41% |
| **EfficientNetB0** | SOTA Transfer Learning | 4,214,184 | 17.79 MB | 33.5 M | 99.45% |

* **Ultra-Low Memory Footprint:** Model B achieves a massive **94.5% reduction** in size on disk compared to EfficientNetB0, successfully fitting within a sub-1 MB budget (**0.99 MB**).
* **Rigorous Constraint Satisfaction:** With **79,168 trainable parameters**, Model B easily clears the `< 100,000` competition constraint with a 20.8% safety headroom.
* **Inference Efficiency:** Requires only **7.6M MACs**, reducing forward-pass compute by **5.6x** compared to Model A.
* **Deterministic Reproducibility:** Global random seeds locked at 42 with deterministic TensorFlow operations enabled.

---

## 📂 Repository Structure
```text
├── models/                                    # Saved pre-trained models (.h5 / .keras)
│   ├── model_a.h5                             # Standard CNN weights
│   ├── model_b.h5                             # Optimized Depthwise Separable CNN weights
│   ├── sota_mn.h5                             # Fine-tuned MobileNetV2
│   └── sota_en.h5                             # Fine-tuned EfficientNetB0
├── notebook/
│   └── EN3150_Assignment_03_GalTricals.ipynb  # Main fully executed Jupyter Notebook
├── report/
│   ├── EN3150_Assignment_03.pdf               # Final compiled IEEE-style Project Report
│   └── latex_source/                          # LaTeX source files (.tex, diagrams, assets)
├── results/
│   └── figures/                               # Training loss/accuracy curves & confusion matrices
├── EN3150_Assignment_03_In23.pdf              # Assignment Rubric and Guidelines
├── requirements.txt                           # Python environment dependencies
└── README.md                                  # Project documentation
```

---

## 📊 View Notebook Online
Click the badge below to inspect the fully executed notebook including all interactive plots and training logs:

[![View Jupyter Notebook](https://img.shields.io/badge/View%20Notebook-nbviewer-orange?logo=jupyter&style=for-the-badge)](https://nbviewer.jupyter.org/github/senuja-dilmith/EN3150_A03_GalTricals/blob/main/notebook/EN3150_Assignment_03_GalTricals.ipynb)

---

## 👥 Team GalTricals (University of Moratuwa)
This project was carried out for the module **EN3150 – Pattern Recognition**, Department of Electronic and Telecommunication Engineering.

| Name | Index Number |
| :--- | :---: |
| **CHINTHAKA M.K.M.G.** | 230105H |
| **DILMITH G.S.** | 230149U |
| **KAUSHAL S.V.** | 230326K |
| **RAJAPAKSHA J.S.W.** | 230511A |
