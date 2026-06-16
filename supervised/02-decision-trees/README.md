# Decision Trees

## 1. Overview

Decision Tree is a supervised machine learning algorithm used for both classification and regression tasks. It works by recursively splitting the dataset into smaller subsets based on feature values until a decision can be made.

The structure resembles a tree where:

* Root Node represents the initial dataset.
* Internal Nodes represent decision rules.
* Branches represent outcomes of decisions.
* Leaf Nodes represent final predictions.

Decision Trees are popular because they are easy to understand, interpret, and visualize.

---

# 2. Problem Statement

The objective of this project is to classify breast tumors as:

* Malignant (Cancerous)
* Benign (Non-Cancerous)

using medical measurements from the Breast Cancer Wisconsin Dataset.

The model learns decision rules from training data and predicts the class of unseen samples.

---

# 3. Mathematical Foundation

Decision Trees split data based on impurity measures.

## Gini Index

Gini measures how often a randomly chosen element would be incorrectly classified.

Gini = 1 − Σ(pi²)

Where:

* pi = probability of class i

Lower Gini indicates purer nodes.

---

## Entropy

Entropy measures uncertainty in a dataset.

Entropy = −Σ(pi log₂ pi)

Where:

* pi = probability of class i

Lower entropy indicates less disorder.

---

## Information Gain

Information Gain determines the best split.

Information Gain = Parent Entropy − Weighted Child Entropy

The feature with the highest information gain is selected for splitting.

---

# 4. Workflow Architecture

Dataset
↓
Data Loading
↓
Data Cleaning
↓
Train-Test Split
↓
Decision Tree Training
↓
Node Splitting
↓
Tree Generation
↓
Prediction
↓
Performance Evaluation
↓
Feature Importance Analysis

---

# 5. Dataset Information

Dataset Used:

Breast Cancer Wisconsin Dataset

Source:

https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

Dataset Characteristics:

* 569 observations
* 30 numerical features
* Binary classification problem

Target Variable:

Diagnosis

Classes:

* M → Malignant
* B → Benign

---

# 6. Implementation Details

This project includes:

### A. Scratch Implementation

A simplified Decision Stump was implemented using NumPy concepts.

Steps:

1. Select feature.
2. Calculate threshold.
3. Split data.
4. Generate predictions.

Purpose:

* Understand tree logic.
* Learn splitting concepts.

---

### B. Scikit-Learn Implementation

Implemented using:

```python
from sklearn.tree import DecisionTreeClassifier
```

Benefits:

* Fast execution
* Built-in optimization
* Tree visualization support
* Feature importance calculation

---

# 7. Model Evaluation Metrics

The following metrics are used:

## Accuracy

Measures overall correctness.

Accuracy = Correct Predictions / Total Predictions

---

## Precision

Measures quality of positive predictions.

Precision = TP / (TP + FP)

---

## Recall

Measures ability to identify positive samples.

Recall = TP / (TP + FN)

---

## F1 Score

Balances precision and recall.

F1 = 2 × Precision × Recall / (Precision + Recall)

---

## Confusion Matrix

Provides a detailed prediction breakdown.

---

# 8. Hyperparameter Tuning

The following hyperparameters were explored.

## Maximum Depth

Controls tree complexity.

* Small depth → Underfitting
* Large depth → Overfitting

---

## Criterion

Two criteria were compared:

### Gini

Faster computation.

### Entropy

Based on information theory.

Performance differences were analyzed.

---

# 9. Feature Importance

One of the major advantages of Decision Trees is their ability to estimate feature importance.

Feature importance indicates:

* Which features influence predictions the most.
* Which variables contribute significantly to classification.

The most important features were visualized using bar charts.

---

# 10. Tree Visualization

Decision Trees can be represented graphically.

Visualization helps:

* Understand model decisions.
* Interpret decision paths.
* Explain predictions to non-technical users.

This project includes a complete tree diagram generated using Scikit-Learn.

---

# 11. Advantages and Limitations

## Advantages

* Easy to understand.
* Easy to visualize.
* Handles nonlinear relationships.
* No feature scaling required.
* Supports feature importance analysis.

---

## Limitations

* Can overfit training data.
* Sensitive to small data changes.
* May create complex trees.
* Less stable than ensemble methods.

---

# 12. Applications

Decision Trees are widely used in:

* Medical diagnosis
* Customer segmentation
* Credit scoring
* Fraud detection
* Risk assessment
* Marketing analytics
* Recommendation systems

---

# 13. Assumptions

Decision Trees assume:

* Training data is representative.
* Important patterns can be captured through recursive splits.
* Features contain predictive information.

Unlike SVM, Decision Trees do not require feature scaling.

---

# 14. Interview Questions

1. What is a Decision Tree?
2. What is Gini Index?
3. What is Entropy?
4. What is Information Gain?
5. How does a tree decide where to split?
6. Why do Decision Trees overfit?
7. What is pruning?
8. Difference between Gini and Entropy?
9. What is feature importance?
10. Difference between Decision Tree and Random Forest?

---

# 15. Quick Reference

| Component     | Description                      |
| ------------- | -------------------------------- |
| Algorithm     | Decision Tree                    |
| Learning Type | Supervised Learning              |
| Task          | Classification                   |
| Dataset       | Breast Cancer Wisconsin          |
| Framework     | NumPy, Scikit-Learn              |
| Metrics       | Accuracy, Precision, Recall, F1  |
| Visualization | Tree Diagram, Feature Importance |

---

# 16. Connections to Other ML Concepts

Decision Trees form the foundation of many advanced algorithms:

* Random Forest
* Extra Trees
* Gradient Boosting
* XGBoost
* LightGBM
* CatBoost

Understanding Decision Trees is essential before learning ensemble methods.

---

# 17. Workflow Diagram

Add your workflow image here:

```markdown
![Decision Tree Workflow](workflow.png)
```

Store the image in the same folder as the README.

---

# 18. Conclusion

Decision Trees are powerful and interpretable supervised learning algorithms. They provide a transparent decision-making process and can handle complex datasets with minimal preprocessing. In this project, Decision Trees were implemented and evaluated using the Breast Cancer Wisconsin Dataset. Performance metrics, feature importance analysis, hyperparameter tuning, and visualization techniques demonstrated how Decision Trees can be effectively applied to real-world classification problems.

---

# 19. References

1. Scikit-Learn Documentation
   https://scikit-learn.org

2. Kaggle Dataset
   https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

3. Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow – Aurélien Géron

4. Pattern Recognition and Machine Learning – Christopher Bishop

5. Introduction to Statistical Learning
