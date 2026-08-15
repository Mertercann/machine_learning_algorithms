# Customer Churn Prediction

A machine learning project for predicting customer churn using classification algorithms.

## Overview

This project analyzes customer data and builds machine learning models to predict whether a customer will churn.

The workflow includes:

- Data preprocessing and exploration
- Categorical variable encoding
- Feature scaling
- Train / validation / test split
- Classification model training
- Hyperparameter optimization
- Model evaluation

## Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree

Hyperparameter tuning was performed using `GridSearchCV` with 5-fold cross-validation.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Results

KNN achieved the best validation performance after hyperparameter tuning.

**Best KNN parameters:**

```text
n_neighbors: 15
weights: distance
metric: manhattan
```

**Validation F1-score:** `0.93`

## Project Structure

```text
├── Final_odevi.ipynb
├── customer_churn_dataset-testing-master.csv
├── requirements.txt
└── README.md
```

## Installation

```bash
pip install -r requirements.txt
```

## Usage

Open `Final_odevi.ipynb` with Jupyter Notebook or VS Code and run the cells sequentially.
