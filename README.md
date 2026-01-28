# 🛰️ Satellite Land Cover Classification

<div align="center">
  <img src="https://img.shields.io/badge/Google%20Colab-Ready-orange?style=for-the-badge&logo=googlecolab" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
</div>

---

## 📋 Project Overview
This project focuses on **Automated Land Cover Classification (LCC)** using Deep Learning. By implementing a **ResNet-50** Convolutional Neural Network, the model successfully classifies high-resolution satellite imagery into 10 distinct environmental categories. This mirrors industry-standard workflows used by organizations such as **NRSC/ISRO** for geospatial analysis.

## 🏗️ Technical Architecture
* **Backbone:** ResNet-50 (Transfer Learning from ImageNet)
* **Data Pipeline:** Customized `torchvision` transforms including normalization and random flips.
* **Classification Head:** Fully connected layers with Dropout (0.3) to prevent overfitting.
* **Optimization:** Adam Optimizer with Negative Log-Likelihood Loss (NLLLoss).

## 📊 Dataset Details
The model was trained on the **EuroSAT (RGB)** dataset, derived from Sentinel-2 satellite imagery.
**Classes include:** *Annual Crop, Forest, Herbaceous Vegetation, Highway, Industrial, Pasture, Permanent Crop, Residential, River, Sea Lake.*

## 📈 Key Performance Results
* **Accuracy:** ~96% on Validation Set.
* **Efficiency:** Leveraged GPU acceleration (T4) in Colab for fast convergence.
* **Evaluation:** Performance verified via Confusion Matrix and F1-score analysis.

## 🛠️ How to Run
1. **Install the required libraries:**
   ```bash
   pip install torch torchvision matplotlib seaborn scikit-learn tqdm
