# 📊 Adult Census Income Classification

This project uses the **Adult Census Income** dataset from [UCI via Kaggle](https://www.kaggle.com/datasets/uciml/adult-census-income) to predict whether a person earns more than \$50K a year using a **Random Forest Classifier**.

## 🔍 Project Overview

- **Goal**: Classify income (`>50K` or `<=50K`) based on demographic and employment-related attributes.
- **Algorithm**: Random Forest Classifier  
- **Evaluation**: Accuracy (via cross-validation)

## 🧰 Tools & Libraries

- Python  
- pandas, NumPy  
- scikit-learn  
- matplotlib  

## 🧪 Workflow

1. **Data Preprocessing**
   - Missing values (represented by `?`) are replaced with `NaN` and imputed.
   - Categorical features are one-hot encoded.
   - Numerical features are standardized.

2. **Modeling**
   - A pipeline combines preprocessing and classification.
   - Multiple models are trained with varying `max_depth` from 1 to 10.
   - 5-fold cross-validation is used to assess performance.

3. **Training & Evaluation**
   - The dataset is split (75% train, 25% test).
   - The final model uses `max_depth=4`, selected based on cross-validation scores.
   - Model is trained and evaluated on the test set.

4. **Visualization**
   - Accuracy across different tree depths is plotted.

## 📁 Dataset

- Source: [Adult Census Income Dataset](https://www.kaggle.com/datasets/uciml/adult-census-income)
- File used: `adult.csv`

## 📈 Example Results

```
max_depth=1, mean accuracy=0.7964  
max_depth=2, mean accuracy=0.8182  
max_depth=3, mean accuracy=0.8373  
max_depth=4, mean accuracy=0.8441  
...
```

