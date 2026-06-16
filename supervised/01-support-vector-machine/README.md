# Support Vector Machines (SVM)

## 1. Overview

Support Vector Machine (SVM) is a powerful supervised machine learning algorithm used for classification and regression tasks. It is widely used in applications such as medical diagnosis, image recognition, spam detection, and text classification.

The main objective of SVM is to find the optimal hyperplane that separates data points belonging to different classes with the maximum possible margin. By maximizing this margin, SVM improves generalization and reduces the risk of overfitting.

In this project, SVM is implemented using both a NumPy-based approach and Scikit-Learn's built-in implementation. The Breast Cancer Wisconsin Dataset is used for binary classification.

---

# 2. Problem Statement

The objective is to classify tumors as:

* Malignant (Cancerous)
* Benign (Non-Cancerous)

using various medical measurements collected from breast cancer patients.

The model learns patterns from the training data and predicts whether a new tumor is malignant or benign.

---

# 3. Mathematical Foundation

Given a dataset:

(X₁, y₁), (X₂, y₂), ..., (Xₙ, yₙ)

where:

* X = Feature vector
* y ∈ {-1, +1}

SVM attempts to find a hyperplane:

wᵀx + b = 0

where:

* w = weight vector
* b = bias

The optimization objective is:

Minimize:

½ ||w||²

Subject to:

yᵢ(wᵀxᵢ + b) ≥ 1

The support vectors are the data points closest to the decision boundary.

---

# 4. Workflow Architecture

Dataset
↓
Data Loading
↓
Data Cleaning
↓
Feature Scaling
↓
Train-Test Split
↓
SVM Training
↓
Prediction
↓
Performance Evaluation
↓
Hyperparameter Tuning

---

# 5. Dataset Information

Dataset Used:

Breast Cancer Wisconsin Dataset

Source:

https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

Dataset Characteristics:

* 569 samples
* 30 numerical features
* Binary classification problem
* Target variable: Diagnosis

Target Classes:

* M → Malignant
* B → Benign

---

# 6. Implementation Details

The project contains two implementations:

### A. SVM From Scratch

Implemented using NumPy.

Steps:

1. Initialize weights and bias.
2. Apply gradient descent.
3. Optimize hinge loss.
4. Update weights iteratively.
5. Predict class labels.

### B. Scikit-Learn Implementation

Implemented using:

```python
from sklearn.svm import SVC
```

Advantages:

* Faster training
* Optimized implementation
* Easy hyperparameter tuning
* Better scalability

---

# 7. Model Evaluation Metrics

The following metrics are used:

### Accuracy

Measures overall correctness.

Accuracy = Correct Predictions / Total Predictions

### Precision

Measures the quality of positive predictions.

Precision = TP / (TP + FP)

### Recall

Measures the ability to identify positive samples.

Recall = TP / (TP + FN)

### F1 Score

Harmonic mean of precision and recall.

F1 = 2 × Precision × Recall / (Precision + Recall)

### Confusion Matrix

Provides a detailed breakdown of predictions.

---

# 8. Hyperparameter Tuning

The following hyperparameters were explored:

### C Parameter

Controls regularization.

* Small C → Wider margin
* Large C → Less tolerance for errors

### Kernel Types

* Linear
* Polynomial
* RBF
* Sigmoid

Performance was compared across different configurations.

---

# 9. Advantages and Limitations

## Advantages

* Effective in high-dimensional spaces.
* Works well with small and medium datasets.
* Robust against overfitting.
* Supports nonlinear classification through kernels.

## Limitations

* Computationally expensive for very large datasets.
* Requires feature scaling.
* Difficult to interpret compared to Decision Trees.
* Kernel selection can be challenging.

---

# 10. Applications

SVM is commonly used in:

* Medical diagnosis
* Face recognition
* Spam filtering
* Sentiment analysis
* Fraud detection
* Bioinformatics
* Image classification

---

# 11. Assumptions

The algorithm assumes:

* Data is reasonably separable.
* Features are scaled properly.
* Training and testing distributions are similar.
* Outliers are limited.

---

# 12. Interview Questions

1. What is a Support Vector Machine?
2. What is a hyperplane?
3. What are support vectors?
4. Why does SVM maximize margin?
5. What is the kernel trick?
6. Difference between Linear and RBF kernel?
7. What is the role of parameter C?
8. Why is feature scaling important in SVM?
9. What is hinge loss?
10. When should SVM be avoided?

---

# 13. Quick Reference

| Component     | Description                             |
| ------------- | --------------------------------------- |
| Algorithm     | Support Vector Machine                  |
| Learning Type | Supervised Learning                     |
| Task          | Classification                          |
| Dataset       | Breast Cancer Wisconsin                 |
| Framework     | NumPy, Scikit-Learn                     |
| Metrics       | Accuracy, Precision, Recall, F1         |
| Visualization | Confusion Matrix, Hyperparameter Graphs |

---

# 14. Connections to Other ML Concepts

Support Vector Machines are closely related to:

* Logistic Regression
* Decision Trees
* Random Forest
* Ensemble Learning
* Kernel Methods
* Feature Engineering
* Model Evaluation Techniques

Understanding SVM builds a strong foundation for advanced classification algorithms.

---

# 15. Conclusion

Support Vector Machines are among the most effective supervised learning algorithms for classification problems. By maximizing the margin between classes, SVM achieves strong generalization performance and often performs well even with limited training data. In this project, both a scratch implementation and a Scikit-Learn implementation were explored, demonstrating the working principles, practical usage, and evaluation of SVM on a real-world healthcare dataset.

---

# 16. References

1. Scikit-Learn Documentation
   https://scikit-learn.org

2. Kaggle Dataset
   https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

3. Pattern Recognition and Machine Learning – Christopher Bishop

4. Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow – Aurélien Géron

