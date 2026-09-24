# Driver Drowsiness Detection Using CNN and Computer Vision

## 📌 Project Overview

This project implements a **real-time driver drowsiness detection system** using **Convolutional Neural Networks (CNN)** and **computer vision techniques**.

The system detects whether a driver's eyes are **open or closed** and uses this information to determine whether the driver may be experiencing drowsiness. The project combines a trained CNN model with **Dlib facial landmark detection** to locate and analyze the driver's eyes in real time.

---

## 📂 Dataset

The dataset used in this project is publicly available on Kaggle:

**Dataset Source:**
https://www.kaggle.com/datasets/dheerajperumandla/drowsiness-dataset

### Dataset Information

The dataset contains **1,452 images**, divided equally into two classes:

| Class       | Number of Images |
| ----------- | ---------------: |
| Open Eyes   |              726 |
| Closed Eyes |              726 |
| **Total**   |        **1,452** |

The balanced dataset is used to train a binary classification model capable of distinguishing between open and closed eyes.

---

## 🧠 Methodology

The project consists of two main stages:

### 1. Eye State Classification

A **Convolutional Neural Network (CNN)** is developed using the **PyTorch framework** to perform binary classification.

The model classifies eye images into two categories:

* **Open**
* **Closed**

The trained CNN model is then used for real-time eye-state prediction.

### 2. Real-Time Eye Detection

For real-time detection, the project uses **Dlib's 68-point facial landmark detector** to identify facial landmarks and locate the driver's eyes.

The detected eye regions are passed to the trained CNN model, which continuously predicts whether the eyes are open or closed.

The system monitors the driver's eye state over a **10-second observation window**. The predictions collected during this period are analyzed to estimate the driver's drowsiness level.

If the detected drowsiness exceeds the defined threshold, the system can identify the driver as **drowsy** and trigger an appropriate notification or alert.

---

🤖 Trained Model Weights

The trained CNN weights are available through Google Drive.

Download the trained model weights:
https://drive.google.com/drive/folders/1LT3-sAuOni_ViaxP9ZUAPNi4IqyJr0Dd?usp=sharing

Download the weights and place the model file in the appropriate project directory before running the real-time detection system.

Note: The trained weights are hosted externally and are not included directly in this repository

## 🛠️ Technologies Used

* **Python**
* **PyTorch**
* **Convolutional Neural Networks (CNN)**
* **OpenCV**
* **Dlib**
* **Computer Vision**
* **Facial Landmark Detection**
* **Kaggle Dataset**

---

## 📁 Project Structure

```text
.
├── README.md
├── change_file_name.py
├── cnn_model.py
├── eye_detection.py
├── model.py
└── shape_predictor_68_face_landmarks.dat
```

### File Description

* `cnn_model.py` — CNN architecture and model-related implementation.
* `model.py` — Model training and prediction functionality.
* `eye_detection.py` — Real-time eye detection using computer vision and facial landmarks.
* `change_file_name.py` — Utility script for managing or modifying dataset/image filenames.
* `shape_predictor_68_face_landmarks.dat` — Dlib's pre-trained 68-point facial landmark model.

---

## 🔄 System Workflow

```text
Input Image
        ↓
Face Detection
        ↓
Dlib Facial Landmark Detection
        ↓
Eye Region Extraction
        ↓
CNN Model
        ↓
Open / Closed Classification
        ↓
10-Second Observation
        ↓
Drowsiness Analysis
        ↓
Driver Alert / Status
```

---

## 🎯 Objective

The primary objective of this project is to develop a computer vision-based system that can monitor a driver's eye state in real time and identify potential signs of drowsiness.

The approach demonstrates how **deep learning and facial landmark detection** can be combined to build an automated driver monitoring system.

---

## 📌 Conclusion

This project demonstrates the application of **PyTorch-based CNN classification** and **Dlib facial landmark detection** for real-time driver drowsiness monitoring.

By combining eye-state classification with continuous observation over a defined time interval, the system provides a practical approach for detecting potential driver fatigue and improving road safety.
