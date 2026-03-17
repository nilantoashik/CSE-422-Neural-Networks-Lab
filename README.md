```markdown
# CSE-422 Neural Networks Lab

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Jupyter](https://img.shields.io/badge/Tools-Jupyter%20Notebook-orange?style=for-the-badge&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-Educational-lightblue?style=for-the-badge)

---

## 📌 Overview

This repository contains laboratory assignments and project implementations for the **CSE-422: Artificial Intelligence (Neural Networks Section)** course. The curriculum is designed to build a comprehensive understanding of neural networks from foundational concepts to advanced implementations.

**Core Philosophy:** All implementations are developed **from scratch using vanilla Python** without external machine learning libraries. This approach ensures deep conceptual understanding of:
- Mathematical foundations of neural networks
- Activation functions and their behaviors
- Training algorithms and optimization
- Backpropagation mechanisms
- Model evaluation and performance analysis

---

## 📂 Repository Structure

```
CSE-422-Neural-Networks-Lab/
│
├── Lab Assignment 1/
│   ├── ID_1007_Lab_Assignment_1_Perceptron_CSE422.ipynb
│   └── (Student Performance Predictor - Single Layer Perceptron)
│
├── Lab Assignment 2/
│   ├── ID_1007_LabAssignment2.ipynb
│   └── (Fitness & Lifestyle Classifier - Perceptron with Analysis)
│
├── NN_assignment3/
│   ├── Neural_Network_Assignment3.ipynb
│   ├── ID_1007_NN_Assignment3.pdf
│   ├── T1.png
│   ├── T2.png
│   ├── T3.png
│   ├── T4.png
│   ├── T5a.png
│   ├── T5b.png
│   ├── T6.png
│   └── B.png
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
**Single-Layer Perceptron** | Binary Classification

This foundational assignment builds a perceptron model that predicts student academic success based on study habits.

**Prediction Task:**
- **Pass (1):** Student succeeds
- **Fail (0):** Student struggles

---

### 📊 Input Features

| Feature | Range | Description |
|---------|-------|-------------|
| Study Hours | 1-8 hrs | Daily study hours |
| Attendance | 0-100% | Class attendance percentage |

---

### 🧠 Classification Logic

A student **PASSES** if:
```
Study Hours > 4 AND Attendance > 70%
```
Otherwise → **FAILS**

---

### ⚙️ Implementation Specifications

| Parameter | Value | Notes |
|-----------|-------|-------|
| Initial Weights | [0.1, 0.1] | Random initialization |
| Initial Bias | -0.5 | Bias term |
| Activation Function | Step Function | Threshold: 0 |
| Learning Rate | 0.1 | Step size for updates |
| Total Epochs | 50 | Training iterations |
| Learning Algorithm | Perceptron Rule | Classical learning rule |

**Weight Update Formula:**
```
w_new = w_old + (η × error × input)
b_new = b_old + (η × error)

where:
  η = learning rate
  error = (expected - predicted)
```

---

### 📊 Dataset Characteristics

- **Size:** 20 training samples
- **Distribution:** Linearly separable data
- **Balance:** Mixed pass/fail cases
- **Type:** Synthetic, representative data

---

### 🎯 Learning Outcomes

✓ Understanding linear decision boundaries  
✓ Manual weight initialization and updates  
✓ Step activation function implementation  
✓ Training loop construction  
✓ Convergence analysis and error tracking  
✓ Decision boundary visualization  

---

## 🔹 Lab Assignment 2: Fitness & Lifestyle Classifier

### 📚 Concept
**Single-Layer Perceptron with Analytical Reporting** | Advanced Binary Classification

Extends Assignment 1 with comprehensive data analysis, custom dataset design, and performance reporting.

**Classification Task:**
- **Fit (1):** Healthy lifestyle
- **Unfit (0):** Sedentary lifestyle

---

### 📊 Input Features

| Feature | Range | Description |
|---------|-------|-------------|
| Physical Activity | 0-10 hrs | Daily exercise hours |
| Sleep | 4-10 hrs | Daily sleep hours |

---

### 🧠 Classification Logic

An individual is **FIT** if:
```
Physical Activity > 3 AND Sleep >= 7
```
Otherwise → **UNFIT**

---

### 🔧 Key Components

#### ✅ **Custom Dataset Design**
- Manually created synthetic dataset
- Realistic lifestyle patterns
- Balanced class distribution (50-50 split)
- Data validation and preprocessing

#### ✅ **Perceptron Implementation**
- Two input features with adjustable weights
- Bias term
- Step activation function
- Training algorithm with convergence monitoring

#### ✅ **Training & Optimization**
- 100+ epochs for convergence
- Real-time error monitoring
- Weight behavior tracking
- Decision boundary analysis

#### ✅ **Interactive Testing Interface**
- User input collection system
- Real-time classification predictions
- Confidence visualization
- Test case examples

#### ✅ **Comprehensive Report Section**
Includes:
- Dataset design methodology
- Feature selection justification
- Ground truth labeling strategy
- Weight evolution analysis over epochs
- Error rate trends
- Model decision boundaries
- Performance metrics (accuracy, precision, recall)
- Limitations and improvements discussion

---

### 📈 Expected Outcomes

- Training Accuracy: 90-100%
- Clear decision boundary separation
- Weight stabilization after ~50 epochs
- Zero classification errors on training data

---

### 🎯 Learning Outcomes

✓ Dataset creation and preprocessing  
✓ Feature engineering considerations  
✓ Training dynamics observation  
✓ Analytical thinking about model behavior  
✓ Documentation and reporting skills  
✓ Model evaluation methodologies  

---

## 🔹 Lab Assignment 3: Multi-Layer Neural Network

### 📚 Concept
**Feedforward Neural Network with Backpropagation** | Multi-class Classification

Advanced assignment introducing hidden layers, sigmoid activation, and backpropagation algorithm.

**Neural Network Architecture:**
```
Input Layer (2) → Hidden Layer(s) → Output Layer (3)
```

---

### 📊 Problem Domain

**Multi-class Classification:** 
- Predicting credit card risk assessment
- Loan approval prediction  
- Customer segmentation

**Output Classes:**
- Class 0: Approved (Low Risk)
- Class 1: Review (Medium Risk)
- Class 2: Rejected (High Risk)

---

### 🧠 Network Architecture

| Layer | Neurons | Activation | Purpose |
|-------|---------|-----------|---------|
| Input | 2 | Linear | Feature input |
| Hidden | 4-8 | Sigmoid | Feature extraction |
| Output | 3 | Sigmoid | Multi-class output |

---

### ⚙️ Implementation Specifications

| Parameter | Value | Notes |
|-----------|-------|-------|
| Activation (Hidden) | Sigmoid | σ(x) = 1 / (1 + e^-x) |
| Activation (Output) | Sigmoid | Multi-class sigmoid |
| Loss Function | MSE | Mean Squared Error |
| Learning Rate | 0.01-0.1 | Adaptive tuning |
| Epochs | 500-1000 | Until convergence |
| Batch Size | Full batch | All samples per epoch |
| Weight Initialization | Random (0.5-0.5) | Small random values |

---

### 📐 Mathematical Components

**Forward Propagation:**
```
z_h = (w_1 × x) + b_1                    [Hidden layer]
a_h = sigmoid(z_h)                       [Activation]
z_o = (w_2 × a_h) + b_2                  [Output layer]
a_o = sigmoid(z_o)                       [Output activation]
```

**Backpropagation:**
```
δ_o = (a_o - y) × sigmoid'(z_o)          [Output error]
δ_h = (w_2^T × δ_o) × sigmoid'(z_h)      [Hidden error]

dw_2 = (1/m) × (δ_o × a_h^T)             [Output weight gradient]
dw_1 = (1/m) × (δ_h × x^T)               [Hidden weight gradient]
```

**Weight Updates:**
```
w_new = w_old - η × dw                   [Gradient descent]
b_new = b_old - η × db
```

---

### 📊 Dataset Characteristics

- **Size:** 50-100 training samples
- **Features:** 2 input features
- **Classes:** 3 output classes
- **Distribution:** Balanced multi-class data
- **Type:** Synthetic, demonstrative

---

### 📈 Performance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Training Accuracy | Correct predictions on training set | >90% |
| Loss (MSE) | Average squared error | <0.1 |
| Convergence | Epochs to stability | <500 |
| Decision Regions | Clear multi-class boundaries | Well-separated |

---

### 🎯 Learning Outcomes

✓ Multi-layer network architecture design  
✓ Sigmoid activation function implementation  
✓ Forward propagation mechanics  
✓ Backpropagation algorithm  
✓ Gradient descent optimization  
✓ Weight initialization strategies  
✓ Multi-class classification techniques  
✓ Convergence analysis  
✓ Hyperparameter tuning  
✓ Network performance evaluation  

---

## 🚀 Getting Started

### Prerequisites
- Python 3.6+
- Jupyter Notebook
- Basic understanding of linear algebra and calculus

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/nilantoashik/CSE-422-Neural-Networks-Lab.git
```

### 2️⃣ Navigate to Directory

```bash
cd CSE-422-Neural-Networks-Lab
```

### 3️⃣ Install Jupyter (if needed)

```bash
pip install jupyter notebook
```

### 4️⃣ Launch Jupyter

```bash
jupyter notebook
```

### 5️⃣ Open Assignment Notebooks

Navigate to the Jupyter browser interface and open:
- `Lab Assignment 1/ID_1007_Lab_Assignment_1_Perceptron_CSE422.ipynb`
- `Lab Assignment 2/ID_1007_LabAssignment2.ipynb`
- `NN_assignment3/Neural_Network_Assignment3.ipynb`

---

## 🛠️ Technologies & Tools

| Category | Details |
|----------|---------|
| **Language** | Python 3.x |
| **Environment** | Jupyter Notebook |
| **Core Libraries** | Standard Python (no ML frameworks) |
| **Math Libraries** | NumPy (optional for Assignment 3) |
| **Visualization** | Matplotlib (for plots and graphs) |
| **Implementation** | Pure Python - Manual NN logic |

---

## 📋 Implementation Approach

### Pure Python Implementation
- **No scikit-learn**
- **No TensorFlow/PyTorch**
- **No pre-built neural network libraries**

### Manually Implemented Components
✓ Activation functions (Step, Sigmoid)  
✓ Forward propagation  
✓ Backpropagation algorithm  
✓ Weight initialization  
✓ Loss functions  
✓ Optimization algorithms  
✓ Data preprocessing  
✓ Model evaluation metrics  

---

## 🎯 Educational Objectives

This repository demonstrates comprehensive understanding of:

1. **Foundational Concepts**
   - Perceptron theory and training
   - Linear separability
   - Binary classification

2. **Mathematical Foundations**
   - Activation functions
   - Forward propagation
   - Backpropagation
   - Gradient descent

3. **Practical Implementation**
   - Weight initialization
   - Training loops
   - Convergence criteria
   - Performance evaluation

4. **Advanced Topics**
   - Multi-layer networks
   - Multi-class classification
   - Hyperparameter tuning
   - Model regularization

5. **Analysis & Reporting**
   - Performance metrics
   - Decision boundary visualization
   - Training dynamics
   - Comparative analysis

---

## 📊 Progression Path

```
Assignment 1: Single Perceptron (Linear)
        ↓
Assignment 2: Single Perceptron (Analysis)
        ↓
Assignment 3: Multi-layer Network (Non-linear)
        ↓
[Advanced Topics]: Deep Learning Concepts
```

---

## 📈 Future Enhancements & Extensions

### Potential Improvements
- [ ] Convolutional Neural Networks (CNN)
- [ ] Recurrent Neural Networks (RNN/LSTM)
- [ ] Regularization techniques (L1/L2, Dropout)
- [ ] Batch normalization
- [ ] Advanced optimizers (Adam, RMSprop)
- [ ] Cross-validation techniques
- [ ] Hyperparameter optimization
- [ ] Real-world dataset applications

### Code Optimizations
- [ ] NumPy vectorization for efficiency
- [ ] Computational performance benchmarking
- [ ] Memory optimization
- [ ] Parallel processing capabilities

### Visualization Enhancements
- [ ] Interactive 3D decision boundaries
- [ ] Training animation/progress visualization
- [ ] Real-time loss curves
- [ ] Weight distribution heatmaps
- [ ] Gradient flow visualization

---

## 📚 Learning Resources

### Recommended Reading
- "Neural Networks and Deep Learning" by Michael Nielsen
- "Deep Learning" by Goodfellow, Bengio, and Courville
- MIT OpenCourseWare - Introduction to Deep Learning

### Key Topics
- Perceptron Convergence Theorem
- Universal Approximation Theorem
- Backpropagation Algorithm
- Vanishing Gradient Problem
- Activation Function Selection

---

## 🔍 Debugging & Troubleshooting

### Common Issues

**Issue: Model not converging**
- Solution: Adjust learning rate (try 0.01 - 0.1)
- Check: Data normalization
- Verify: Weight initialization

**Issue: Weights oscillating**
- Solution: Reduce learning rate
- Check: Dataset has linearly separable classes

**Issue: Poor accuracy on test data**
- Solution: Check dataset size
- Verify: Feature scaling
- Consider: Additional hidden layers

---

## 📄 File Descriptions

### Assignment Files
- `.ipynb` files: Complete implementations with explanations
- `.pdf` files: Formal reports and analysis documents
- `.png` files: Screenshots and visualization outputs

### Configuration Files
- `.gitattributes`: Git attribute settings
- `.gitignore`: Excluded file patterns

---

## 👤 Author Information

**Md. Rahmatulla Ashik**
- GitHub: [@nilantoashik](https://github.com/nilantoashik)
- Course: CSE-422 Neural Networks Laboratory
- Institution: University Coursework
- Student ID: 1007

---

## 📝 Citation

If you use this repository for learning or reference:

```
@misc{CSE422NeuralNetworksLab,
  author = {Md. Rahmatulla Ashik},
  title = {CSE-422: Neural Networks Lab - From Scratch Implementations},
  year = {2024-2025},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/nilantoashik/CSE-422-Neural-Networks-Lab}},
}
```

---

## 📄 License & Usage

**License Type:** Educational Use Only

**Permissions:**
- ✅ Study and learning
- ✅ Educational reference
- ✅ Course assignments
- ✅ Personal understanding

**Restrictions:**
- ❌ Commercial use
- ❌ Direct copying for submissions
- ❌ Distribution without attribution
- ❌ Removal of original author credits

This repository is created strictly for **educational purposes** as part of the CSE-422 curriculum.

---

## 🤝 Contributing & Feedback

If you have suggestions, improvements, or corrections:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

---

## 📞 Support & Questions

For questions about the implementations or course content, please:
- Check the detailed comments in notebook files
- Review the corresponding PDF reports
- Consult course materials
- Reach out to the instructor

---

✨ **Building Neural Networks from Scratch to Master the Fundamentals** ✨

### Key Takeaway
> This repository demonstrates that understanding neural networks deeply requires implementing them yourself. Through manual implementation, you'll gain insights that no black-box framework can provide.

---

**Last Updated:** March 2025  
**Repository Status:** Active & Maintained  
**Course Status:** Ongoing
```

---

