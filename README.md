# 🏦 Bank Marketing Optimization: Term Deposit Prediction

## 📌 Business Context & Objective
Direct marketing campaigns, specifically telemarketing, are resource-intensive and expensive. Calling customers who are unlikely to subscribe to a term deposit results in wasted resources. The objective of this project is to optimize these campaigns by building a predictive model to identify customers with a high propensity to subscribe (`y=1`), thereby increasing conversion rates and significantly reducing operational costs.

## 🛠️ Analytical Approach
1. **Data Preparation:** Addressed class imbalance (88% No / 12% Yes) using Stratified Sampling to ensure consistent training and testing environments. Prevented data leakage by dropping the `poutcome` variable.
2. **Feature Engineering:** Utilized One-Hot Encoding to convert categorical text variables into numerical dummy variables, dropping the first column to avoid multicollinearity. 
3. **Modeling:** Trained and evaluated multiple classification algorithms, including Logistic Regression, Decision Trees, Random Forest, and Gradient Boosting. 
4. **Evaluation Metrics:** Focused strictly on **AUC (Area Under the Curve)** rather than accuracy due to the highly imbalanced nature of the target variable. Monitored the Train-Test Gap to prevent model overfitting.

## 🚀 Key Results & Business Recommendations
* The **Gradient Boosting Classifier** emerged as the champion model, providing the optimal balance of highest Test AUC and predictive stability.
* **Actionable Insight:** The marketing team should transition away from mass-calling and focus telemarketing efforts strictly on the top decile (top 10%) of customers identified by this model's "Probability to Subscribe" to maximize Return on Investment (ROI).

## 💻 Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Scikit-Learn (Pipelines, Standard Scaler, Classification Metrics), Matplotlib, Seaborn
