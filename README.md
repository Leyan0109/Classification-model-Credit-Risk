# 💳 Credit Risk Prediction 
## A Comparative Study of Classification Models and WOE-Based Feature Transformation

This project focuses on predicting whether a client will experience **serious delinquency within the next two years** using classification models. The dataset was preprocessed to ensure high data quality, including imputation, outlier treatment, and transformation using **Weight of Evidence (WOE)** to enhance interpretability and model effectiveness—especially for logistic regression.

Three machine learning models were evaluated to identify the best-performing approach in terms of accuracy, recall, and business relevance.

---

## 🧠 Models Compared
- **Logistic Regression (with and without WOE)**
- **Random Forest Classifier**
- **XGBoost Classifier**

### 🧩 Feature Strategy
1. **Raw Features** – Cleaned but untransformed dataset  
2. **WOE-Transformed Features** – Variables transformed using Weight of Evidence to support interpretability and improve logistic regression performance

---

## 🔍 Key Findings

- **Random Forest** delivered the best balance of performance metrics:
  - **ROC AUC:** 0.8569  
  - **Recall:** 0.72  
  - **Precision:** 0.22
- **Logistic Regression** performed well with WOE-transformed features:
  - **Recall:** 0.70  
  - **Precision:** 0.19  
  - Enabled creation of an interpretable **scorecard**
- **XGBoost** had the highest precision for non-delinquents but a low recall (0.16), making it less suitable for minimizing false negatives.
- Key predictors across models included:
  - **Revolving Utilization of Unsecured Lines**
  - **Past Due Counts (30–59, 60–89, 90+)**
  - **Age**

---

## 🛠️ Tools & Libraries Used
- Python, Jupyter Notebook
- pandas, numpy, seaborn, matplotlib
- scikit-learn, XGBoost
- WOE Binning tools, scikit-plot

---

## 📁 Repository Structure
`credit-risk-prediction/`
1. data/       # Raw dataset
2. notebooks/  # Model training and evaluation (LR, RF, XGBoost)
3. results/    # Evaluation metrics, ROC curves, confusion matrices, scorecard
4. README.md   # Project overview

---

## 📌 Conclusion

This project demonstrates that:
- **Random Forest** is the most effective model for credit delinquency prediction, offering high recall and balanced precision.
- **Logistic Regression** with WOE remains highly interpretable and practical for deployment via scorecards.
- Combining **Random Forest's accuracy** with **Logistic Regression's explainability** provides a strong, business-ready solution for credit scoring systems.
