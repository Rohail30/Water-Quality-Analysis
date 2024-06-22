# Water-Quality-Analysis

---

### Introduction

This project focuses on the analysis and prediction of water quality using a dataset containing concentrations of various contaminants. Ensuring safe drinking water is crucial for public health, and predictive models can help in early detection of water safety issues. To achieve this, we utilized several machine learning algorithms to classify water samples as safe or unsafe. The chosen algorithms include Decision Tree, Multi-Layer Perceptron (MLP), K-Nearest Neighbors (KNN), and Logistic Regression. Each of these algorithms offers unique advantages and challenges, which are explored in the context of this dataset. This report provides an overview of the dataset and a brief explanation of each algorithm's methodology and suitability for the task.

---

### Dataset Overview

The dataset consists of 21 features representing the concentrations of various contaminants in water samples. The target variable is a binary indicator (`is_safe`), where 1 denotes safe water and 0 indicates unsafe water. Below is the detailed information about the features:

| Contaminant | Dangerous Threshold (ppm) |
| ----------- | ------------------------- |
| Aluminium   | 2.8                       |
| Ammonia     | 32.5                      |
| Arsenic     | 0.01                      |
| Barium      | 2                         |
| Cadmium     | 0.005                     |
| Chloramine  | 4                         |
| Chromium    | 0.1                       |
| Copper      | 1.3                       |
| Fluoride    | 1.5                       |
| Bacteria    | 0                         |
| Viruses     | 0                         |
| Lead        | 0.015                     |
| Nitrates    | 10                        |
| Nitrites    | 1                         |
| Mercury     | 0.002                     |
| Perchlorate | 56                        |
| Radium      | 5                         |
| Selenium    | 0.5                       |
| Silver      | 0.1                       |
| Uranium     | 0.3                       |
| Is_Safe     | Class attribute (0: not safe, 1: safe) |

---

### Machine Learning Algorithms

#### K-Nearest Neighbors (KNN)
**Overview**: KNN is a simple, instance-based learning algorithm where the classification of a sample is determined by the majority class among its k-nearest neighbors in the feature space. It is widely used for classification and regression tasks.

**Advantages**: 
- Simple to implement
- Intuitive to understand
- Non-parametric, meaning it makes no assumptions about the underlying data distribution.

**Disadvantages**: 
- Computationally expensive at prediction time due to the need to compute distances between the sample and all training data.
- Sensitive to the choice of k.
- Can be affected by irrelevant or redundant features.

#### Decision Tree
**Overview**: Decision Trees are hierarchical models used for classification and regression tasks. They split the data into subsets based on feature values, creating a tree structure with nodes representing feature tests and branches representing the outcome of these tests.

**Advantages**: 
- Easy to understand and interpret
- Handles both numerical and categorical data
- Requires little data preprocessing.

**Disadvantages**: 
- Prone to overfitting, especially with complex trees.
- Can be unstable due to small variations in data.

#### Multi-Layer Perceptron (MLP)
**Overview**: MLP is a type of artificial neural network consisting of an input layer, one or more hidden layers, and an output layer. Each layer is composed of neurons that are fully connected to neurons in the next layer. MLPs are used for complex pattern recognition tasks.

**Advantages**: 
- Capable of capturing complex non-linear relationships
- Highly flexible
- Can model complex data distributions.

**Disadvantages**: 
- Computationally intensive
- Sensitive to the choice of hyperparameters
- Requires a large amount of data for training
- Often considered a black-box model due to difficulty in interpreting the weights.

#### Logistic Regression
**Overview**: Logistic Regression is a linear model used for binary classification tasks. It models the probability that a given input belongs to a particular class using a logistic function. The model outputs probabilities that can be mapped to binary outcomes.

**Advantages**: 
- Simple and easy to implement
- Provides interpretable model coefficients
- Works well for linearly separable data
- Outputs probabilities which can be useful for decision making.

**Disadvantages**: 
- Assumes a linear relationship between the features and the log odds of the target.
- May not perform well with complex, non-linear data.
- Can be affected by multicollinearity among features.

---

### Conclusion

The predictive models trained on the water quality dataset have demonstrated promising performance across various machine learning algorithms. Below are the accuracy scores achieved by each model:

| ML Algorithm             | Accuracy Score        |
| ------------------------ | --------------------- |
| Multi-Layer Perceptron (MLP) | 0.9736                |
| Decision Tree            | 0.9569                |
| K-Nearest Neighbors (KNN)| 0.9038                |
| Logistic Regression      | 0.9025                |

The MLP model achieved the highest accuracy score of approximately 97.36%, indicating its effectiveness in accurately predicting water safety based on contaminant levels. Decision Tree also performed well with an accuracy score of around 95.69%. While KNN and Logistic Regression yielded slightly lower accuracy scores, they still demonstrated considerable performance in classifying water samples.

In conclusion, these models show promise in aiding the early detection of water safety issues, which is crucial for safeguarding public health. Further fine-tuning and optimization of these models could potentially enhance their predictive capabilities and contribute to more robust water quality assessment systems.

---
