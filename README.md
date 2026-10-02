# 🌾 Resource-Constrained CNN for Edge Image Classification

![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Enabled-red.svg)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Project Overview
This project focuses on the automated classification of agricultural rice grains (5 varieties) using Convolutional Neural Networks (CNNs) optimized for **extreme edge devices**. We built a custom **Depthwise-Separable CNN (Model B)** strictly constrained to under 100,000 parameters to simulate real-world microcontroller deployments (e.g., an automated agricultural sorting machine).

### 🚀 Key Achievements
* **Model Size on Disk:** 0.99 MB (94% reduction compared to SOTA EfficientNet-B0)
* **Trainable Parameters:** 79,168 (Satisfies the <100k constraint)
* **Test Accuracy:** 96.73%
* **Features:** Depthwise-Separable Convolutions, Global Average Pooling, Deterministic Random Seed Locking for 100% reproducibility.

## 📂 Repository Structure
```text
├── notebook/
│   └── EN3150_Assignment_03_GalTricals.ipynb  # Main Jupyter Notebook
├── report/
│   ├── EN3150_Assignment_03.pdf               # Final Project Report
│   └── latex_source/                          # LaTeX source code and image assets
├── results/
│   └── figures/                               # Training curves and confusion matrices
├── EN3150_Assignment_03_In23.pdf              # Original Assignment Guidelines
├── requirements.txt                           # Python dependencies
└── README.md                                  # Project documentation