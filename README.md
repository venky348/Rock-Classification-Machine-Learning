# Rock Classification Using Machine Learning

This project focuses on classifying different rock types (Igneous, Sedimentary, and Metamorphic) using machine learning models. The dataset contains physical and visual characteristics of rocks, and the goal is to develop predictive models to identify rock types with high accuracy.

---

## Overview

The repository includes:
- Data preprocessing and exploratory data analysis (EDA) to examine relationships between features.
- Implementation of machine learning classifiers:
  - **Logistic Regression (Softmax Regression)**
  - **Support Vector Machine (SVM)**
  - **Random Forest Classifier**
  - **Ensemble Voting Classifier**
- Comparison of human accuracy with model performance on both training and test datasets.

---

## Dataset Details

- **Number of Entries:** 480
- **Features:** 12 independent features representing rock characteristics such as:
  - Angular Fragments, Rounded Fragments, Stripes (Straight/Curved), Physical Layers, Texture (Oily/Shimmery, Sandy), and more.
- **Target Variable:** Rock type (Igneous, Sedimentary, Metamorphic).

---

## Key Insights from Data Analysis

1. **Feature Distributions:**
   - Most features exhibit right-skewed distributions.
   - Some features display clusters or multiple peaks.

2. **Correlation Analysis:**
   - Physical Layers and Single Translucent Crystals show the strongest positive correlation with the rock type.
   - Angular and Rounded Fragments exhibit slight positive relationships.

3. **No Null Values:** The dataset is complete, and no imputation was required.

---

## Model Implementations

### 1. Logistic Regression (Softmax)
- **Best Hyperparameters:**
  - Regularization (C): 100
  - Solver: Newton-CG
  - Max Iterations: 100
- **Test Accuracy:** 67.78%

### 2. Support Vector Machine (SVM)
- **Best Hyperparameters:**
  - C: 100
  - Kernel: RBF
  - Degree: 2
  - Gamma: Scale
- **Test Accuracy:** 68.89%

### 3. Random Forest Classifier
- **Best Hyperparameters:**
  - Number of Trees: 100
  - Max Depth: None
  - Min Samples Split: 10
  - Min Samples Leaf: 1
- **Test Accuracy:** 64.44%

### 4. Ensemble Voting Classifier
- Combines the strengths of Logistic Regression, SVM, and Random Forest.
- **Test Accuracy:** 71.11% (highest among all models).

---

## Human vs. Model Performance

1. **Training Accuracy:**
   - Human: 55.99%
   - Model (Best - Voting Classifier): 85.67%

2. **Test Accuracy:**
   - Human: 59.84%
   - Model (Best - Voting Classifier): 71.11%

The model significantly outperformed human accuracy on both training and test datasets, showcasing its ability to identify patterns more effectively.

---

## Conclusion

- The Ensemble Voting Classifier achieved the best performance, demonstrating the effectiveness of combining multiple classifiers.
- Physical Layers and Single Translucent Crystals are key features for differentiating rock types.
- This project highlights the value of machine learning in automating geological classifications.

---

