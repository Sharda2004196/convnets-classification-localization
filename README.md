# 🧠 ConvNets for Classification and Localization

> A dual-head Convolutional Neural Network that simultaneously classifies handwritten digits and predicts bounding box coordinates — built from scratch using TensorFlow and Keras.

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN-red)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Project Overview

This project builds a **multi-output CNN** that performs two tasks simultaneously:

| Task | Type | Output |
|------|------|--------|
| Digit Classification | Multi-class Classification | Class label (0–9) |
| Digit Localization | Bounding Box Regression | [x, y, width, height] |

Both tasks are handled by a **shared convolutional backbone** with two separate output heads — one for classification and one for bounding box regression. This is the foundational architecture behind real-world object detection systems.

| Detail | Info |
|--------|------|
| **Dataset** | MNIST — 70,000 grayscale handwritten digit images |
| **Input Shape** | 28 × 28 × 1 |
| **Classes** | 10 (digits 0–9) |
| **Architecture** | Dual-head CNN (Classification + Localization) |
| **Framework** | TensorFlow / Keras |
| **Environment** | Google Colab |

---

## 🏗️ Model Architecture

```
Input (28x28x1)
      │
Conv2D(32, 3x3, ReLU) + MaxPooling
      │
Conv2D(64, 3x3, ReLU) + MaxPooling
      │
Flatten → Dense(128, ReLU)
      │
   ┌──┴──┐
   │     │
Head 1   Head 2
Classification   Localization
Dense(10, Softmax)   Dense(4, Linear)
[class label]   [x, y, w, h]
```

---

## 📉 Loss Functions

| Head | Loss Function | Reason |
|------|--------------|--------|
| Classification | Categorical Cross-Entropy | Standard for multi-class classification |
| Localization | Mean Squared Error (MSE) | Standard for regression tasks |

---

## 🚀 How to Run

**1. Open in Google Colab**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1-N96UajrQYu3nWPcToBanU5CMy0mAm7t#scrollTo=PLo4JmmRmLln)

**2. Run all cells**

Go to **Runtime → Run All** — the dataset loads automatically, no manual downloads needed. ✅

---

## 📂 Project Structure

```
convnets-classification-localization/
├── ConvNets_for_Classification_and_Localization.ipynb  ← Main notebook
└── README.md                                           ← Project documentation
```

---

## 🗂️ Notebook Walkthrough

```
Step 1  → Import Libraries
Step 2  → Load and Preprocess MNIST Dataset
Step 3  → Visualize Sample Images
Step 4  → Generate Synthetic Bounding Boxes
Step 5  → Build Dual-Head CNN Model
Step 6  → Train the Model (5 epochs)
Step 7  → Plot Training Accuracy
Step 8  → Evaluate on Test Set
Step 9  → Visualize Predictions with Bounding Boxes
Step 10 → Final Summary
```

---

## ⚙️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10 | Core language |
| TensorFlow / Keras | Model building and training |
| NumPy | Numerical operations |
| Matplotlib | Training plots and visualizations |
| OpenCV (cv2) | Drawing bounding boxes on images |
| Google Colab | Development environment |

---

## 💡 Key Concepts Demonstrated

- Building a **multi-output model** using the Keras Functional API
- **Dual loss training** — combining classification and regression losses
- **Bounding box regression** using MSE loss
- Shared convolutional backbone for feature extraction
- Visualizing predictions with bounding boxes using OpenCV

---

## 🔗 Related Projects

- [House Price Prediction — ML Regression](https://github.com/Sharda2004196/house-price-prediction)
- [GitHub Portfolio Analyzer — AI Agent](https://github.com/Sharda2004196/github-portfolio-analyzer)
- [Xavier — AI Assistant (n8n Workflow)](https://github.com/Sharda2004196/Xavier-AI-Assistant)

---

## 👤 Author

**Sharda Vatsal Bhat**  
Aspiring AI/ML Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/sharda-vatsal-bhat-73b037295)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/Sharda2004196)
