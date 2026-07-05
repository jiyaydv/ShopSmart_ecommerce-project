# ShopSmart Visitor Purchase Prediction

## Project Overview

The **ShopSmart Visitor Purchase Prediction System** is a Supervised Machine Learning project that predicts whether a visitor will make a purchase during an online shopping session.

ShopSmart receives thousands of visitors every day. Although users browse products and spend time on the website, only a small percentage complete a purchase. Predicting purchasing intent helps the company optimize marketing campaigns, personalize recommendations, and improve conversion rates.

This project uses a **Decision Tree Classifier** with pruning techniques to classify visitor sessions as either **Purchase (Revenue = True)** or **No Purchase (Revenue = False)**.

---

# Problem Statement

ShopSmart wants to identify visitors who are most likely to complete a purchase based on their browsing behavior.

The dataset consists of **12,330 unique user sessions** collected over one year. Each record represents a unique visitor session and includes both numerical and categorical features describing website interactions.

Since the dataset is **imbalanced**, the model is evaluated using the **F1-Score**, with a target benchmark of **0.55 or higher**.

---

# Objectives

- Perform Exploratory Data Analysis (EDA)
- Clean and preprocess the dataset
- Encode categorical variables
- Handle class imbalance
- Train a Decision Tree Classifier
- Apply pruning to reduce overfitting
- Evaluate the model using the F1-Score
- Predict whether a visitor will make a purchase

---

# Dataset Description

Each row represents one website session.

| Feature | Description |
|----------|-------------|
| Administrative | Number of administrative pages visited |
| Administrative_Duration | Time spent on administrative pages (seconds) |
| Informational | Number of informational pages visited |
| Informational_Duration | Time spent on informational pages |
| ProductRelated | Number of product pages visited |
| ProductRelated_Duration | Time spent on product pages |
| BounceRates | Percentage of single-page visits |
| ExitRates | Percentage of exits from viewed pages |
| PageValues | Average page value before purchase |
| SpecialDay | Closeness to a special shopping day |
| Month | Month of visit |
| OperatingSystems | Visitor's operating system |
| Browser | Browser used |
| Region | Visitor's region |
| TrafficType | Traffic source |
| VisitorType | Returning Visitor / New Visitor / Other |
| Weekend | Whether the visit occurred on a weekend |
| Revenue | **Target Variable (True = Purchase, False = No Purchase)** |

---

# Technology Stack

## Programming Language

- Python 3.x

## Libraries

- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib

## Development Environment

- Jupyter Notebook
- VS Code

---

# Machine Learning Workflow

1. Import Dataset
2. Exploratory Data Analysis (EDA)
3. Handle Missing Values
4. Feature Engineering
5. Encode Categorical Features
6. Train-Test Split
7. Train Decision Tree Classifier
8. Apply Tree Pruning
9. Evaluate Model
10. Save Trained Model

---

# Exploratory Data Analysis

EDA includes:

- Dataset overview
- Missing value analysis
- Duplicate record detection
- Statistical summary
- Correlation analysis
- Class distribution
- Feature distributions
- Outlier detection

---

# Data Preprocessing

- Handle missing values
- Remove duplicates
- Label Encoding / One-Hot Encoding
- Feature selection
- Convert categorical variables into numerical format

---

# Model Used

## Decision Tree Classifier

A Decision Tree Classifier is used because it:

- Is easy to interpret
- Handles both numerical and categorical data
- Captures nonlinear relationships
- Requires minimal feature scaling

### Pruning Techniques

To improve performance and reduce overfitting:

- Maximum Depth (`max_depth`)
- Minimum Samples Split (`min_samples_split`)
- Minimum Samples Leaf (`min_samples_leaf`)
- Cost Complexity Pruning (`ccp_alpha`)

---

# Evaluation Metrics

Since the dataset is imbalanced, model performance is evaluated using:

- F1-Score (Primary Metric)
- Precision
- Recall
- Accuracy
- Confusion Matrix
- Classification Report

### Target Benchmark

**F1-Score ≥ 0.55**

---

# Project Structure

```
ShopSmart-Purchase-Prediction/
│
├── dataset/
│   └── online_shoppers_intention.csv
│
├── notebooks/
│   └── EDA.ipynb
│
├── models/
│   └── decision_tree.pkl
│
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   └── predict.py
│
├── app.py
├── requirements.txt
└── README.md
```

---

# Model Training Pipeline

```
Dataset
      │
      ▼
EDA
      │
      ▼
Data Cleaning
      │
      ▼
Feature Encoding
      │
      ▼
Train-Test Split
      │
      ▼
Decision Tree Training
      │
      ▼
Tree Pruning
      │
      ▼
Model Evaluation
      │
      ▼
Purchase Prediction
```

---

# Expected Output

### Input

Visitor session details:

- Product pages visited
- Time spent
- Bounce rate
- Exit rate
- Month
- Visitor type
- Traffic source
- Weekend
- Other session features

### Output

```
Prediction: Purchase

or

Prediction: No Purchase
```

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/ShopSmart-Purchase-Prediction.git
```

Move to the project directory:

```bash
cd ShopSmart-Purchase-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run model training:

```bash
python train.py
```

Run prediction:

```bash
python predict.py
```

---

# Future Enhancements

- Compare multiple machine learning models (Random Forest, XGBoost, LightGBM)
- Hyperparameter tuning using GridSearchCV
- Handle imbalance using SMOTE
- Deploy the model using Flask or FastAPI
- Create an interactive dashboard
- Real-time purchase prediction API

---

# Learning Outcomes

After completing this project, you will understand:

- Exploratory Data Analysis (EDA)
- Feature preprocessing
- Decision Tree algorithms
- Tree pruning techniques
- Model evaluation for imbalanced datasets
- F1-Score interpretation
- End-to-end machine learning workflow

---

# Author

**Developed by:** Jiya

**Course:** Supervised Machine Learning (Assignment 4)

**Project:** ShopSmart Visitor Purchase Prediction

**Domain:** Machine Learning | Classification | E-commerce Analytics
