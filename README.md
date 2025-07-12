## Loan Default Prediction - Project Summary

### 📌 Objective:
To build and evaluate classification models that can predict whether a customer will default on a loan using financial data.

### 📂 Dataset:
- Loaded from `Default_Fin.csv`
- Target variable: `Defaulted?` (0 = No default, 1 = Defaulted)
- Index column set as `'Index'`

### 🧪 Feature Engineering:
- Created new feature: `Savings Ratio = (Bank Balance / Annual Salary) * 100`
- Rationale: Reflects client’s financial stability

### 📊 Exploratory Data Analysis:
- Correlation analysis showed:
  - Savings Ratio & Bank Balance had a 62% positive correlation
- Visualizations:
  - Scatter plots for Bank Balance vs. Employment and Default status
  - Histograms showed bimodal salary distribution and skewed bank balance/savings ratio

### ⚖️ Class Imbalance:
- Detected imbalance in the target
- Addressed using **SMOTE** to oversample the minority class

### 📈 Modeling Approaches:
- Algorithms used:
  - Logistic Regression
  - Ridge Classifier
  - Random Forest
  - XGBoost

- Trained and evaluated under two conditions:
  1. Raw data
  2. Scaled data using StandardScaler

### 🧾 Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Custom evaluation function used for consistency across all models.

### 📌 Pipeline Summary:
1. Load & preprocess data
2. Feature engineering
3. EDA & correlation analysis
4. Split data (70/30) with stratification
5. Handle imbalance with SMOTE
6. Train & evaluate multiple classifiers
7. Re-train using scaled data

### ✅ Conclusion:
- Multiple models tested and compared
- Use of `SMOTE` and `StandardScaler` improved fairness and performance
- Recommended next steps:
  - Hyperparameter tuning
  - Cross-validation
  - Feature selection techniques
