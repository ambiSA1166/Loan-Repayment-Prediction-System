# 🏦 Loan Repayment Prediction System

## 📌 Overview

This project presents the development of a **Machine Learning-based Loan Repayment Prediction System** designed to predict whether a borrower is likely to **repay a loan or default**. The model utilizes financial and demographic data to generate reliable predictions that can support **data-driven decision-making** in lending institutions.

The project was developed as a significant academic work during my **4th semester**, with a focus on applying machine learning concepts to a real-world financial risk assessment problem. It demonstrates a complete end-to-end workflow, from data preprocessing to model evaluation.

---

## 🎯 Problem Statement

Loan defaults represent a major financial risk for banks and lending organizations. Traditional decision-making processes may not fully capture complex patterns in borrower behavior.

This project aims to address the key question:

> **“Can we accurately predict whether a borrower will repay a loan based on their financial and personal attributes?”**

By solving this problem, financial institutions can reduce losses, improve efficiency, and enhance credit risk management.

---

## 📊 Dataset

* **Total Records:** ~20,000
* **Type:** Structured tabular dataset

### Target Variable:

* `loan_paid_back`

  * **1 → Loan Repaid**
  * **0 → Loan Defaulted**

### Feature Set Includes:

* Credit Score
* Annual Income
* Loan Amount
* Debt-to-Income Ratio
* Employment Status
* Education Level
* Gender
* Marital Status
* Delinquency History

---

## ⚙️ Project Workflow

### 1️⃣ Data Exploration & Cleaning

Initial data exploration was performed using:

* `.info()` and `.describe()` to understand structure and statistics
* Missing value analysis to identify incomplete data
* Removal of duplicate entries
* Validation and correction of data types

This step ensured the dataset was clean, consistent, and ready for analysis.

---

### 2️⃣ Exploratory Data Analysis (EDA)

EDA was conducted to uncover patterns, relationships, and insights within the data.

#### 📊 Univariate Analysis

* Distribution of numerical features analyzed using histograms
* Identified skewness in features such as income and loan amount
* Observed general trends and variability in data

#### 🔍 Bivariate Analysis

* Used boxplots and countplots to analyze relationships with the target variable

Key observations:

* Higher **credit scores** are strongly associated with successful loan repayment
* Higher **debt-to-income ratios** indicate increased default risk
* **Employment status** significantly influences repayment behavior

---

### ⚠️ Class Imbalance Analysis

* Approximately **80%** of borrowers repaid loans
* Around **20%** defaulted

This imbalance influenced model evaluation strategy, leading to the use of:

* **Recall**
* **F1-score**

instead of relying solely on accuracy.

---

### 🔥 Correlation Analysis

* A correlation heatmap was used to identify relationships between features
* Strong multicollinearity observed between:

  * Annual income and monthly income

To avoid redundancy and improve model performance:

* Highly correlated features were removed

---

### 📉 Scatter & Pair Analysis

* Explored relationships between variables such as income and loan amount
* Identified weak or non-linear relationships
* Helped validate feature relevance for modeling

---

## 🧪 Feature Engineering

To enhance predictive performance, new features were created:

### ✅ Income-to-Loan Ratio

* Measures borrower’s repayment capacity relative to loan size

### ✅ Credit Utilization

* Reflects how much credit a borrower is currently using

### ✅ EMI-to-Income Ratio

* Indicates financial burden of loan repayment

These engineered features provided deeper insights into borrower behavior and improved model effectiveness.

---

## 🧹 Feature Selection & Encoding

* Removed redundant features to reduce multicollinearity
* Applied one-hot encoding using `pd.get_dummies()` for categorical variables
* Ensured all features were in numerical format for model compatibility

---

## 🤖 Model Building

Multiple classification models were implemented and compared:

* Logistic Regression
* Decision Tree
* K-Nearest Neighbors (KNN)

Each model was trained on processed data and evaluated using appropriate performance metrics.

---

## 📈 Model Performance

### 🏆 Best Model: Logistic Regression

* **F1-score:** 0.92
* **Recall:** 0.96

The high recall indicates that the model effectively identifies most defaulters, which is critical in minimizing financial risk.

---

## 🔍 Confusion Matrix Insights

* The model correctly classifies the majority of repayment cases
* Some **false positives** are present
* Performance can be further improved through:

  * Decision threshold tuning
  * Cost-sensitive learning approaches

---

## 🧠 Key Insights

* Credit score is the most influential predictor of loan repayment
* Financial ratios provide stronger predictive power than raw values
* Borrowers with past delinquency are more likely to default
* Class imbalance significantly impacts evaluation metrics
* Feature selection improves both performance and interpretability

---

## 💡 Business Impact

This system provides practical value by:

* Enabling **risk-based lending decisions**
* Reducing **loan default rates**
* Improving **efficiency of credit evaluation processes**
* Supporting **data-driven financial strategies**

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/loan-repayment-prediction.git
cd loan-repayment-prediction
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Notebook

```bash
jupyter notebook
```

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## 📌 Future Improvements

* Address class imbalance using SMOTE or class weighting
* Perform hyperparameter tuning for optimized performance
* Deploy the model using Flask or Streamlit
* Develop a user interface for real-time predictions
* Enhance model interpretability using SHAP or LIME

---

## 🙌 Conclusion

This project demonstrates a comprehensive application of machine learning in solving a real-world financial problem. It highlights the importance of data preprocessing, feature engineering, and appropriate evaluation techniques in building reliable predictive models. The system can serve as a foundation for more advanced credit risk analysis solutions.

---

## 📬 Contact

I am open to feedback, suggestions, and collaboration opportunities. Feel free to connect!
