# 🌾 Resource-Constrained CNN for Edge Image Classification

![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Enabled-red.svg)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Project Overview
This project focuses on the automated classification of agricultural rice grains (5 varieties: Arborio, Basmati, Ipsala, Jasmine, and Karacadag) using Convolutional Neural Networks (CNNs) optimized for **extreme edge devices**. We designed and evaluated a custom **Depthwise-Separable CNN (Model B)** strictly constrained to under 100,000 trainable parameters to simulate real-world low-resource microcontroller deployments (e.g., an automated agricultural sorting machine).

### 🚀 Key Achievements
* **Model Size on Disk:** 0.99 MB (A massive 94% reduction compared to SOTA EfficientNet-B0)
* **Trainable Parameters:** 79,168 (Successfully satisfies the <100k constraint)
* **Test Accuracy:** 96.73%
* **Architectural Features:** Depthwise-Separable Convolutions, Global Average Pooling, and Deterministic Random Seed Locking for 100% reproducibility.


## 📂 Repository Structure
```text
├── models/                                    # Saved pre-trained models (.h5 / .keras)
├── notebook/
│   └── EN3150_Assignment_03_GalTricals.ipynb  # Main Jupyter Notebook containing the code
├── report/
│   ├── EN3150_Assignment_03.pdf               # Final Compiled Project Report
│   └── latex_source/                          # LaTeX source code and image assets
├── results/
│   └── figures/                               # Exported training curves and confusion matrices
├── EN3150_Assignment_03_In23.pdf              # Original Assignment Guidelines
├── requirements.txt                           # Python dependencies required to run the code
└── README.md                                  # Project documentation
```

## 📊 View Notebook Online
Click the badge below to view the fully rendered Jupyter Notebook online:

[![View Jupyter Notebook](https://img.shields.io/badge/View%20Notebook-nbviewer-orange?logo=jupyter&style=for-the-badge)](https://nbviewer.jupyter.org/github/senuja-dilmith/EN3150_A03_GalTricals/blob/main/notebook/EN3150_Assignment_03_GalTricals.ipynb)

## 👥 Team GalTricals (University of Moratuwa)
This project was completed as part of the **EN3150 - Pattern Recognition** module.

| Name | Index Number |
| :--- | :--- |
| **CHINTHAKA M.K.M.G.** | 230105H |
| **DILMITH G.S.** | 230149U |
| **KAUSHAL S.V.** | 230326K |
| **RAJAPAKSHA J.S.W.** | 230511A |
```
