<div align="center">

# 🧠 Binary & Multiclass MNIST Classification

### Manual Machine Learning Algorithms from Scratch

A complete implementation of classical Machine Learning algorithms built **from scratch**, featuring custom preprocessing, feature engineering, dimensionality reduction, evaluation pipelines, and optimized execution.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Vectorized-orange?style=for-the-badge&logo=numpy)
![TensorFlow](https://img.shields.io/badge/Dataset-MNIST-red?style=for-the-badge&logo=tensorflow)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

</div>

---

# 📖 Overview

This project demonstrates how classical Machine Learning algorithms work **under the hood** by implementing them manually rather than relying on pre-built Scikit-Learn models.

The project consists of two experimental pipelines:

- 🔹 **Phase 1:** Binary Classification (Digits **3 vs 8**)
- 🔹 **Phase 2:** Multiclass Classification (Digits **0–9**)

The implementation focuses on:

- Manual algorithm implementation
- Feature engineering
- Model comparison
- Performance evaluation
- Computational optimization

---

# ✨ Features

## 🤖 Machine Learning Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Gaussian Naive Bayes

---

## 📊 Feature Engineering

- Raw Pixel Features
- Principal Component Analysis (PCA)

---

## 📈 Evaluation

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Cross Validation
- Hyperparameter Search

---

# ⚡ Performance Optimizations

Although every algorithm remains implemented from scratch, several optimizations significantly reduce execution time.

### 🚀 Logistic Regression

- Fully vectorized gradient computation
- NumPy batch operations
- Eliminated feature-by-feature Python loops

### 🚀 K-Nearest Neighbors

- Manual implementation
- Fully vectorized Euclidean distance computation
- Faster predictions using NumPy array operations

### 🚀 Principal Component Analysis (PCA)

PCA is implemented manually using the **Dual Covariance Trick**, making it much more efficient for MNIST where:

```text
Number of Samples << Number of Features
```

This optimization provides the largest performance improvement in the project.

### 🚀 Hyperparameter Search

Phase 2 uses a reduced manual search grid to keep experimentation practical while maintaining strong performance.

---

# 📂 Project Structure

```text
.
├── src/
│   ├── models/
│   │   ├── logistic_regression.py
│   │   ├── knn.py
│   │   ├── decision_tree.py
│   │   ├── random_forest.py
│   │   └── gaussian_nb.py
│   │
│   ├── data.py
│   ├── preprocess.py
│   ├── features.py
│   ├── metrics.py
│   ├── validation.py
│   ├── visualization.py
│   └── experiments.py
│
├── outputs/
├── main.py
├── app.py
├── phase1_config.json
├── phase1_fast_config.json
├── phase2_fast_config.json
├── phase2_improved_config.json
├── README.md
└── requirements_demo.txt
```

---

# 🚀 Installation

```bash
git clone https://github.com/yourusername/Binary-Multiclassification-of-MNIST.git

cd Binary-Multiclassification-of-MNIST

pip install -r requirements_demo.txt
```

---

# ▶ Running the Project

## Phase 1

```bash
python main.py --phase 1 --config phase1_fast_config.json --mnist-loader tensorflow
```

This phase performs:

- Dataset loading
- Feature extraction
- Model training
- Performance evaluation
- Result visualization

---

## Phase 2 (Improved Pipeline)

```bash
python main.py --phase 2 --improved --config phase2_fast_config.json --mnist-loader tensorflow
```

Runs the optimized machine learning pipeline with faster execution and manual hyperparameter tuning.

---

# ⚙️ Fast Configuration

## Phase 1

| Setting | Value |
|---------|------:|
| Classes | 3 & 8 |
| Samples per Class | 300 |

## Phase 2

| Setting | Value |
|---------|------:|
| Classes | 0–9 |
| Samples per Class | 40 |

---

# 📊 Outputs

The project automatically generates:

- Performance metrics
- Predictions
- Confusion matrices
- Visualizations
- Experimental results

All outputs are saved inside:

```text
outputs/
```

---

# 📈 Expected Results

### Binary Classification (Digits 3 vs 8)

| Model | Expected Accuracy |
|------|------------------:|
| Logistic Regression | ~99% |
| K-Nearest Neighbors | ~98% |
| Gaussian Naive Bayes | High |
| Decision Tree | High |
| Random Forest | High |

### Multiclass Classification (Digits 0–9)

| Feature Type | Expected Accuracy |
|-------------|------------------:|
| PCA Features | ~92% |
| Raw Pixels | ~90% |

> Actual performance may vary depending on dataset size and selected hyperparameters.

---

# 🛠 Technologies

- Python
- NumPy
- TensorFlow (MNIST Loader)
- Matplotlib
- Pandas

---

# 📦 Dependencies

- NumPy
- TensorFlow
- Matplotlib
- Pandas
- tqdm

---

# 🎓 Educational Value

This project demonstrates a complete end-to-end Machine Learning workflow:

- Data preprocessing
- Feature engineering
- Manual model implementation
- Model evaluation
- Hyperparameter tuning
- Performance optimization

The emphasis is on understanding the mathematics behind classical Machine Learning algorithms rather than relying on high-level libraries.

---

# 📌 Highlights

- ✅ Manual ML implementations
- ✅ No Scikit-Learn models
- ✅ Vectorized numerical computations
- ✅ Optimized PCA implementation
- ✅ Modular project architecture
- ✅ Binary & multiclass classification
- ✅ Fast experimentation
- ✅ Educational implementation

---

<div align="center">

</div>
