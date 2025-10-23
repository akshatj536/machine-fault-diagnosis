# 🏷️ Bearing Fault Diagnosis Using Vibration Data

This project explores **predictive maintenance and fault diagnosis in bearings** through vibration signal analysis.  
By combining **signal transformation**, **deep learning**, and **diffusion-based data augmentation**, the notebooks demonstrate how AI can detect and classify different bearing fault types with high accuracy.  

The project uses two benchmark datasets:
- **XJTU-SY Bearing Dataset** — Includes vibration data from 15 bearings across 5 fault types (including normal), each with 3 fault severity levels.  
- **CWRU Bearing Dataset** — A standard dataset from the Case Western Reserve University, widely used for bearing fault analysis.

---

## 📘 Table of Contents
1. [Project Overview](#🏷️-bearing-fault-diagnosis-using-vibration-data)  
2. [Notebooks Overview](#📓-notebooks-overview)  
3. [Results / Output](#🧠-results--output)  
4. [Project Structure](#📂-project-structure)  

---

## 📓 Notebooks Overview

### 1. `xjtu.ipynb`
**Goal:** Classify bearing fault types using the XJTU-SY dataset.  

**Key Steps:**
- Load vibration time-series data from multiple bearings.  
- Apply **Wigner–Ville transformation** to convert 1D vibration signals into 2D time–frequency images.  
- Train a **ResNet-based CNN** model for multi-class fault classification.  
- Evaluate model accuracy and visualize performance metrics.  

**Techniques Used:**  
Signal-to-image transformation, deep CNN architectures, and supervised classification.  

---

### 2. `cwru.ipynb`
**Goal:** Detect and classify bearing faults using the CWRU dataset.  

**Key Steps:**
- Preprocess vibration signals and generate 2D representations.  
- Train a custom **CNN model (`classifier_model_8`)** built with convolutional and dense layers using **tanh activations** and **dropout regularization**.  
- Integrate **diffusion models** for synthetic data generation and signal augmentation, improving dataset diversity and robustness.  
- Evaluate classification accuracy and visualize predictions.  

**Techniques Used:**  
Diffusion-based data augmentation, tabular diffusion, and vibration feature learning through CNNs.  

---

## 🧠 Results / Output

| Notebook | Dataset | Model | Description | Test Accuracy |
|-----------|----------|--------|--------------|----------------|
| `xjtu.ipynb` | XJTU-SY | ResNet | Classified 5 bearing fault types using Wigner–Ville images | **81.4%** |
| `cwru.ipynb` | CWRU | Custom CNN (`classifier_model_8`) | Identified multiple bearing fault conditions using augmented vibration signals | **96.18%** |

**Summary:**  
The **ResNet** model effectively learned fault patterns from the XJTU dataset, while the **custom CNN** in the CWRU notebook achieved superior performance.  
Data augmentation through **diffusion techniques** significantly improved generalization and reduced overfitting.

---

## 📂 Project Structure
```bash
bearing-fault-diagnosis/
├── xjtu.ipynb                # Fault classification using XJTU dataset (ResNet)
├── cwru.ipynb                # Fault classification using CWRU dataset (Custom CNN)                 # Evaluation reports and visualizations
└── README.md                 # Project documentation
