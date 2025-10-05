# Bearing Fault Detection and Severity Classification

This project implements a **vibration-based bearing fault diagnosis system** that combines signal processing and deep learning for automated **fault detection**, **severity estimation**, and **classification**. It processes raw vibration data collected from rotating machinery to identify the health state of bearings and distinguish between different fault types and severities.

---

## 🔍 Overview

The workflow begins with **signal preprocessing**, followed by **fault onset and severity detection** using gradient-based and RMS-based analysis. Once fault regions are identified, the system converts them into **time–frequency representations** using the **Wigner–Ville Distribution (WVD)**. These WVD images are then used to train a **ResNet-based Convolutional Neural Network (CNN)** for fault classification.

This approach integrates traditional vibration analysis with deep learning to provide an end-to-end diagnostic framework.

---

## ⚙️ Key Components

- **Signal Normalization & Gradient Estimation** – Detects early deviations indicating potential faults.  
- **RMS Window Analysis** – Measures vibration energy variations to identify fault progression.  
- **Fault Segmentation** – Divides vibration signals into “Normal”, “Medium Severity”, and “High Severity” segments.  
- **Wigner–Ville Distribution (WVD)** – Generates time–frequency representations for deep learning input.  
- **ResNet Model** – Classifies faults using a deep CNN architecture trained on WVD images.  
- **Performance Evaluation** – Tracks model accuracy, loss, and visualizes classification results.

---

## 🧠 Tech Stack

- **Python**
- **NumPy**, **Pandas**, **Matplotlib**
- **TensorFlow / Keras**
- **Scikit-learn**
- **tqdm**

---

## 📈 Outcome

The trained model successfully classifies vibration signals into different fault categories and severity levels, enabling early detection of bearing defects.  
This system demonstrates how **signal processing + deep learning** can be integrated for effective **predictive maintenance** in rotating machinery.

---

*Developed as an experimental research project for vibration-based condition monitoring and fault classification.*
