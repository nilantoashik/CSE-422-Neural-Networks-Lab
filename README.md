# CSE-422 Neural Networks Lab

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Jupyter](https://img.shields.io/badge/Tools-Jupyter%20Notebook-orange?style=for-the-badge&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

---

## 📌 Overview

This repository contains laboratory assignments and project implementations for the **CSE-422: Artificial Intelligence (Neural Networks Section)** course.

The main objective of this repository is to understand the **core fundamentals of Neural Networks**, starting from the **Single-Layer Perceptron model**, and implementing everything manually from scratch using Python.

Instead of using external machine learning libraries, all mathematical logic, training loops, activation functions, and weight updates are implemented manually to strengthen conceptual understanding.

---

## 📂 Repository Structure

```
CSE-422-Neural-Networks-Lab/
│
├── Lab Assignment 1/
│   ├── Create ID_1007_Lab_Assignment_1_Perceptron_CSE422.ipynb
│   └── (Student Performance Predictor Implementation)
│
├── Lab Assignment 2/
│   ├── Create Id_1007_LabAssignment2.ipynb
│   └── (Fitness & Lifestyle Classifier + Analytical Report)
│
├── NN_assignment3/
│   ├── T1.png
│   ├── T2.png
│   ├── T3.png
│   ├── T4.png
│   ├── T5a.png
│   ├── T5b.png
│   ├── T6.png
│   ├── B.png
│   ├── ID_1007_NN_Assignment3.pdf
│   └── Create Neural_Network_Assignment3.ipynb
│
├── .gitattributes
├── .gitignore
└── README.md
```

---

# 📘 Assignments Breakdown

---

## 🔹 Lab Assignment 1: Student Performance Predictor

### 📚 Concept
Single Layer Perceptron (Binary Classification)

This assignment builds a perceptron model that predicts whether a student will:

- **Pass (1)**
- **Fail (0)**

based on academic habits.

---

### 📊 Features

- `Study Hours` (per day)
- `Attendance Percentage`

---

### 🧠 Ground Truth Logic

A student passes (`1`) if:

```
Study Hours > 4 AND Attendance > 70
```

Otherwise, the student fails (`0`).

---

### ⚙ Implementation Details

- **Initial Weights:** `[0.1, 0.1]`
- **Bias:** `-0.5`
- **Activation Function:** Step Function
- **Epochs:** 50
- **Learning Rule:** Perceptron Learning Rule

Weight Update Formula:

```
w = w + (learning_rate × error × input)
b = b + (learning_rate × error)
```

---

### 🎯 Learning Outcomes

- Understanding linear classification
- Manual implementation of neural networks
- Observing weight adjustment over epochs
- Error convergence analysis

---

## 🔹 Lab Assignment 2: Fitness & Lifestyle Classifier

### 📚 Concept
Single Layer Perceptron with Analytical Reporting

This assignment extends the perceptron model to classify individuals as:

- **Fit (1)**
- **Unfit (0)**

based on lifestyle habits.

---

### 📊 Features

- `Physical Activity` (hours per day)
- `Sleep` (hours per day)

---

### 🧠 Key Components

#### ✅ Custom Dataset Design
- Synthetic dataset simulating real-life lifestyle patterns
- Balanced class distribution

#### ✅ Training Loop
- Iterative weight updates
- Error monitoring per epoch
- Convergence observation

#### ✅ Interactive Testing
- User input system
- Real-time classification

#### ✅ Report Section
Includes:
- Dataset design explanation
- Labeling strategy
- Weight behavior analysis
- Model performance discussion

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/nilantoashik/CSE-422-Neural-Networks-Lab.git
```

### 2️⃣ Navigate to the Directory

```bash
cd CSE-422-Neural-Networks-Lab
```

### 3️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4️⃣ Open the Notebook

Open any `.ipynb` file from the browser interface.

---

## 🛠️ Technologies Used

- **Language:** Python 3.x
- **Environment:** Jupyter Notebook
- **Libraries:** Standard Python libraries only
- **Implementation Approach:** Manual ML logic (No external ML frameworks)

---

## 🎯 Educational Objectives

This repository demonstrates:

- Fundamental understanding of Perceptron
- Binary classification techniques
- Step activation function implementation
- Weight and bias optimization
- Training loop construction
- Model evaluation and reporting

---

## 📈 Future Enhancements

- Multi-Layer Perceptron (MLP)
- Sigmoid and ReLU activation functions
- Decision boundary visualization
- Loss function graph plotting
- NumPy optimization
- Performance comparison with scikit-learn

---

## 👤 Author

**Md. Rahmatulla Ashik**

- GitHub: https://github.com/nilantoashik
- Course: CSE-422 Neural Networks Lab
- Institution: University Lab Coursework

---

## 📄 License

This repository is created strictly for **educational purposes** as part of the CSE-422 curriculum.

---

✨ *Building Neural Networks from Scratch to Master the Fundamentals.*
