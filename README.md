# 📊 Dual Compressed Decorrelation Regularizer (DCD)

**Make Features Independent, Make Models Dependable**

📘 *CSC 591 – Deep Learning Beyond Accuracy*  
👨‍🏫 Instructor: Jung-Eun Kim  

## 👥 Authors
- Ajith Kanumuri  
- Mrudani Hada  
- Parth Parikh  

---

## 🚀 Overview

Deep neural networks often learn **redundant and overlapping features**, which:
- Waste model capacity  
- Hurt generalization  
- Reduce robustness  

This project introduces **Dual Compressed Decorrelation (DCD)** — a novel regularization framework designed to:
- Reduce feature redundancy  
- Improve representation diversity  
- Enhance model generalization and reliability  

---

## 🎯 Objectives

- Encourage **feature independence**
- Reduce **correlation between activations and weights**
- Improve **accuracy, calibration, and robustness**
- Enable **efficient training with lower computational cost**

---

## 🧠 Methodology

### 1. Activation Decorrelation (La)
- Encourages independence among hidden activations  
- Reduces redundancy in learned representations  
- Uses **Gaussian Sketching** for efficiency  

### 2. Soft Orthogonality (Lw)
- Promotes near-orthogonal convolutional filters  
- More flexible and stable than hard orthogonality  
- Lightweight and computationally efficient  

### 3. Sparsity Regularization (Ls)
- Applies **L1 regularization**  
- Encourages pruning-friendly sparse weights  

### 4. Quantization-Aware Regularization (Lq)
- Improves robustness to quantization  
- Uses **tanh-based soft rounding** for differentiability  

---

## ⚙️ Final Loss Function
L = L_task + λa * La + λw * Lw + λs * Ls + λq * Lq


Where:
- `La` → Activation decorrelation loss  
- `Lw` → Soft orthogonality loss  
- `Ls` → Sparsity loss (L1)  
- `Lq` → Quantization-aware loss  

---

## 🧪 Experimental Setup

### Models
- VGG-16  
- EfficientNet  

### Datasets
- CIFAR-10  
- CIFAR-100  

---

## 📉 Metrics Used

- **Train-Test Accuracy Gap** → Generalization  
- **Expected Calibration Error (ECE)** → Model reliability  
- **Mean Off-Diagonal Covariance (MOC)** → Feature redundancy  
- **Top-1 / Top-5 Accuracy** → Performance  
- **Validation Cross-Entropy Loss** → Training quality  

---

## 📊 Results

- 📉 **Train-Test Gap reduced by ~76.25%**
- 📉 **ECE improved by ~64.70%**
- 📉 **Feature redundancy reduced by ~30.27%**
- 📈 Improved test accuracy and validation loss  

---

## 💡 Key Insights

- Efficient alternative to expensive covariance-based methods  
- Maintains flexibility vs rigid orthogonality constraints  
- Enhances generalization and robustness  
- Supports pruning and quantization workflows  

---

## ⚠️ Challenges Faced

- Selecting optimal models for redundancy evaluation  
- Identifying impactful layers  
- Designing efficient Gaussian grouping strategy  
- Stabilizing normalization during training  

---

## 👨‍💻 Contributions

### Literature Review
- Ajith → Activation decorrelation  
- Mrudani → Soft orthogonality  
- Parth → Sparsity & quantization-aware regularization  

### Implementation
- Baseline models (VGG, EfficientNet)  
- Applied DCD across CIFAR-10 and CIFAR-100  
- Evaluation and visualization of key metrics  

---

## 🔮 Future Work

- Extend to large-scale datasets (e.g., ImageNet)  
- Apply to transformer architectures  
- Explore hardware-aware optimizations  

---

## 🙌 Acknowledgements

Thanks to CSC 591 and the instructor for guidance and support.

---
