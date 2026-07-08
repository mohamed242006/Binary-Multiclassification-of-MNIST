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

The project is divided into two main phases that progressively introduce more advanced machine learning concepts, feature engineering techniques, and optimization strategies.

---

## 🔹 Phase 1 — Binary Classification (Digits 3 vs 8)

Phase 1 focuses on building a complete binary image classification pipeline using the MNIST dataset. The objective is to compare multiple machine learning algorithms implemented from scratch on a simple two-class classification problem.

### Features

- Binary classification of handwritten digits **3** and **8**
- Configurable dataset size through JSON configuration files
- Automatic data loading and preprocessing
- Pixel normalization and feature standardization
- Comparison of multiple machine learning algorithms
- Manual implementation of all learning algorithms
- Performance visualization and evaluation

### Machine Learning Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Decision Tree
- Random Forest

### Feature Engineering

- Raw Pixel Features
- Principal Component Analysis (PCA)

### Evaluation

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Model comparison reports

---

## 🔹 Phase 2 — Multiclass Classification (Digits 0–9)

Phase 2 extends the project to a complete multiclass classification problem involving all ten handwritten digits. The pipeline introduces several optimization techniques to improve execution speed while maintaining manual implementations of the core algorithms.

### Features

- Classification of all MNIST digits (0–9)
- Optimized machine learning pipeline
- Manual hyperparameter tuning
- Cross-validation for model evaluation
- Faster execution through optimized numerical computations
- Reduced search space for practical experimentation

### Pipeline Improvements

#### Logistic Regression

- Fully vectorized gradient descent
- Efficient batch processing using NumPy
- Faster convergence compared to feature-by-feature loops

#### K-Nearest Neighbors

- Manual Euclidean distance computation
- Fully vectorized distance calculations
- Faster prediction on larger datasets

#### Principal Component Analysis (PCA)

- Manual implementation using the **Dual Covariance Trick**
- Optimized specifically for high-dimensional datasets such as MNIST
- Largest runtime improvement in the project

### Hyperparameter Optimization

The improved pipeline performs manual hyperparameter tuning over a reduced search space, allowing faster experimentation while maintaining competitive performance.

### Evaluation

- Overall Accuracy
- Per-Class Precision
- Per-Class Recall
- Per-Class F1 Score
- Confusion Matrix
- Cross-Validation Performance
- Feature Comparison


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

# 🔬 Data Processing

The project includes a complete preprocessing pipeline before model training.

## Dataset

- MNIST handwritten digit dataset
- Loaded using TensorFlow/Keras
- Grayscale images (28 × 28 pixels)
- Pixel values normalized to the range **[0, 1]**

## Preprocessing

- Image normalization
- Feature standardization
- Stratified train/validation/test split
- Optional class balancing
- Configurable dataset size through JSON files

## Feature Engineering

The following feature representations are supported:

| Feature | Description |
|---------|-------------|
| Raw Pixels | Flattened 28 × 28 images |
| PCA | Manual dimensionality reduction |
| HOG | Histogram of Oriented Gradients (Phase 1) |

These feature representations allow comparison between different approaches for image classification.

# 🤖 Machine Learning Algorithms

The project implements classical Machine Learning algorithms manually rather than relying on Scikit-Learn models.

## Logistic Regression

- Binary and multiclass classification
- Mini-batch gradient descent
- Vectorized NumPy implementation
- Cross-entropy loss

---

## K-Nearest Neighbors (KNN)

- Euclidean distance
- Manual nearest-neighbor search
- Hyperparameter tuning
- Vectorized distance computation

---

## Gaussian Naive Bayes

- Gaussian probability distributions
- Manual likelihood computation
- Fast probabilistic baseline

---

## Decision Tree

- Recursive tree construction
- Gini impurity
- Information gain

---

## Random Forest

- Bootstrap aggregation (Bagging)
- Random feature selection
- Majority voting

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

# ⚙️ Configuration

The project behavior can be customized using the provided JSON configuration files.

| Configuration File | Purpose |
|-------------------|---------|
| phase1_config.json | Default Phase 1 settings |
| phase1_fast_config.json | Faster binary classification |
| phase2_fast_config.json | Faster multiclass pipeline |
| phase2_improved_config.json | Improved multiclass experiments |

Configuration options include:

- Selected digits
- Samples per class
- Learning rate
- Batch size
- Number of iterations
- PCA components
- Random seed

# 📊 Experimental Results

The following results summarize the performance of the implemented models on representative experimental runs.

## Phase 1 — Binary Classification (Digits 3 vs 8)

| Model | Feature | Test Accuracy | Macro F1 |
|------|---------|--------------:|----------:|
| Logistic Regression | **HOG** | **98.75%** | **98.75%** |
| K-Nearest Neighbors | HOG | 97.75% | 97.75% |
| Logistic Regression | Flatten | 96.75% | 96.75% |
| Logistic Regression | PCA | 96.50% | 96.50% |
| K-Nearest Neighbors | Flatten | 96.25% | 96.25% |
| K-Nearest Neighbors | PCA | 95.50% | 95.50% |
| Gaussian Naive Bayes | HOG | 93.50% | 93.49% |
| Gaussian Naive Bayes | Flatten | 85.75% | 85.63% |
| Gaussian Naive Bayes | PCA | 80.75% | 80.46% |

### 🏆 Best Performing Configuration

- **Model:** Logistic Regression
- **Feature Extraction:** HOG
- **Test Accuracy:** **98.75%**
- **Macro F1-Score:** **98.75%**

---

## Phase 2 — Multiclass Classification (Digits 0–9)

| Model | Test Accuracy | Macro F1 | Best Configuration |
|------|--------------:|---------:|-------------------|
| **KNN (Tuned)** | **91.63%** | **91.62%** | k=5, Euclidean |
| Logistic Regression (L2) | 88.50% | 88.48% | Learning Rate = 0.05 |
| Random Forest | 85.69% | 85.66% | 15 Trees, Max Depth = 12 |

### 🏆 Best Performing Configuration

- **Model:** Tuned K-Nearest Neighbors
- **Distance Metric:** Euclidean
- **Number of Neighbors:** 5
- **Test Accuracy:** **91.63%**
- **Macro F1-Score:** **91.62%**

---

# 📈 Evaluation & Visualization
The project evaluates every trained model using standard classification metrics.
### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- Macro F1 Score
- Confusion Matrix


### Generated Outputs
The pipeline automatically generates:
- Classification reports
- Confusion matrices
- Model comparison tables
- Learning curves
- Performance summaries
- Prediction outputs

All generated files are saved inside the `outputs/` directory

## 📈 Key Findings

- HOG features provided the strongest representation for binary classification.
- Logistic Regression achieved the highest binary classification accuracy.
- Hyperparameter tuning significantly improved KNN performance in the multiclass task.
- PCA successfully reduced feature dimensionality while maintaining competitive performance.
- The optimized implementation reduced execution time while preserving classification accuracy.

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

# 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| Slow training | Use the fast configuration files |
| Memory usage is high | Reduce the number of PCA components |
| Low accuracy | Increase training samples or iterations |
| Import errors | Install all required packages from `requirements_demo.txt` |
| TensorFlow dataset not loading | Verify TensorFlow installation |

# 🙏 Acknowledgements

- MNIST Dataset by Yann LeCun
- TensorFlow/Keras for dataset loading
- NumPy for numerical computations
- Matplotlib for visualization

## 🌟 Key Advantages

### Comprehensive Learning Path
- Progressive Complexity: Start with binary classification, advance to multiclass.
- Multiple Algorithms: Compare different ML approaches (Phase 1).
- Advanced Techniques: Regularization and bias-variance analysis (Phase 2).
- Feature Engineering: Understand the impact of different feature representations.

### Interactive Development
- Jupyter Notebooks: Execute code step-by-step with immediate feedback.
- Rich Visualizations: See results, plots, and metrics inline.
- Easy Experimentation: Modify parameters and re-run individual cells.
- Professional Workflow: Industry-standard data science practices.

### Educational Value
- From-Scratch Implementation: Understand algorithms at the fundamental level.
- Regularization: Learn to prevent overfitting with L1/L2/ElasticNet.
- Bias-Variance Tradeoff: Deep understanding of model behavior.
- Hyperparameter Tuning: Systematic approach to model optimization.
- Cross-Validation: Proper model evaluation and selection techniques.
- Performance Analysis: Comprehensive evaluation with multiple metrics.

### Real-World Relevance
- Complete Pipeline: End-to-end ML project structure.
- Multiple Feature Types: PCA, HOG, and raw features comparison.
- Scalable Code: Modular design for easy extension.
- Reproducible Results: Proper random seeding and documentation.
- Statistical Rigor: Bootstrap-based analysis for robust conclusions.

---

## 🔬 Advanced Topics Covered

### Regularization
- **Purpose:** Prevent overfitting by penalizing complex models.  
- **L1 (Lasso):** Encourages sparsity, useful for feature selection.  
- **L2 (Ridge):** Smooth weight distribution, better generalization.  
- **ElasticNet:** Combines benefits of L1 and L2.  
- **Implementation:** Custom gradient computation with penalty terms.

### Bias-Variance Tradeoff
- **Bias:** Error from overly simplistic assumptions (underfitting).  
- **Variance:** Error from sensitivity to training data (overfitting).  
- **Decomposition:** Bootstrap sampling to separate bias and variance.  
- **Analysis:** Visual comparison across different regularization methods.  
- **Interpretation:** Guidelines for model selection and improvement.

### Feature Engineering
- **PCA:** Dimensionality reduction while preserving variance.  
- **HOG:** Edge and gradient information for image classification.  
- **Comparison:** Systematic evaluation of feature impact on performance.


---

<div align="center">

</div>
