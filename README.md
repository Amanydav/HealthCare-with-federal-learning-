# 🏥 Decentralized Healthcare Prediction using Federated Learning

This repository implements a **privacy-preserving healthcare prediction system** using **Federated Learning (FL)**.  
The project focuses on **diabetes prediction** while ensuring that **patient data never leaves local clients**, making the system suitable for decentralized healthcare environments.

---

## 📌 Project Motivation
Traditional centralized machine learning requires aggregating sensitive healthcare data, raising privacy and regulatory concerns.  
Federated Learning enables collaborative model training **without sharing raw data**, making it a promising solution for healthcare analytics.

---

## 🎯 Objectives
- Build a **decentralized diabetes prediction model**
- Compare multiple **federated learning algorithms**
- Analyze performance trade-offs in healthcare settings
- Identify the most reliable federated approach for clinical prediction

---

## 🗂 Dataset
- **Source**: Kaggle Diabetes Dataset  
- **Target Variable**: `Outcome` (Diabetes: Yes / No)  
- **Features**: 8 clinical attributes (Glucose, BMI, Age, Blood Pressure, etc.)

---

## 🧠 Model Architecture
- **Multi-Layer Perceptron (MLP)**
  - Input Layer: 8 features
  - Hidden Layer 1: 128 neurons (ReLU)
  - Hidden Layer 2: 64 neurons (ReLU)
  - Output Layer: Sigmoid (Binary Classification)

---

## 🔄 Federated Learning Setup
- **Clients**: 3 (simulated healthcare institutions)
- **Data Distribution**: IID (used as a performance benchmark)
- **Training**:
  - Local model training at each client
  - Only model parameters shared with the server
- **Privacy**: Raw patient data never shared

---

## ⚙️ Algorithms Implemented
- **FedAvg** – Baseline federated averaging  
- **FedProx** – Handles client drift via proximal regularization  
- **FedAdam** – Adaptive server-side optimization  
- **FedAdagrad** – Adaptive learning-rate federated optimization  

---

## 📊 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  
- Accuracy vs Communication Rounds (Graph)

---

## ✅ Key Findings
- **FedAvg** achieved the best balance of accuracy and recall, making it most suitable for healthcare prediction.
- **FedProx** provided stable but slightly conservative performance.
- **FedAdam and FedAdagrad** achieved high recall but suffered from excessive false positives.
- Results confirm that **optimizer choice significantly impacts federated healthcare reliability**.

---

## 🧪 Centralized vs Federated Learning
- Centralized learning achieved higher accuracy.
- Federated learning provided competitive performance **while preserving privacy**.
- The goal of this project is **secure and decentralized learning**, not outperforming centralized models.

---

## 🚧 Limitations
- Public dataset used instead of real clinical data
- IID data distribution does not fully represent real-world hospitals
- No differential privacy or secure aggregation implemented

---

## 🔮 Future Work
- Evaluation under **Non-IID data distributions**
- Personalized federated learning
- Secure aggregation and differential privacy
- Validation on real-world multi-institution datasets

---

## 🛠 Tech Stack
- Python
- TensorFlow / Keras
- NumPy, Pandas
- Scikit-learn
- Matplotlib

---

## ▶️ How to Run
1. Place `diabetes.csv` in the project directory  
2. Install dependencies:
   ```bash
   pip install numpy pandas tensorflow scikit-learn matplotlib
