# Predictive Modeling for Telecom Customer Churn

## 🎯 Project Goal

This project aims to solve a critical business problem for **Interconnect**, a telecommunications provider: **proactively predicting customer churn**. By leveraging machine learning, the goal is to identify customers who are likely to cancel their service. This allows the marketing team to deploy targeted retention strategies, such as offering promotional codes and special plans, to improve customer loyalty and reduce revenue loss.

---

## 🛠️ Tech Stack

* **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, CatBoost, Matplotlib, Seaborn
* **Modeling:** Logistic Regression, Gradient Boosting (CatBoost)
* **Techniques:** Exploratory Data Analysis (EDA), Feature Engineering, Hyperparameter Tuning (`GridSearchCV`), Model Evaluation (AUC-ROC, Accuracy)

---

## 📈 Project Workflow & Key Steps

1.  **Data Preparation & EDA:** The project began by merging four distinct data sources (`contract`, `personal`, `internet`, and `phone`) into a unified dataset. I performed a thorough exploratory data analysis to understand data distributions, handle missing values, and create a key predictive feature: `tenure` (customer lifetime).

2.  **Model Development:** I developed two models to compare performance:
    * A **Logistic Regression** model as a robust baseline.
    * A **CatBoost Classifier** as a more advanced gradient-boosting model.

3.  **Hyperparameter Optimization:** After an initial evaluation, the CatBoost model's performance was systematically improved using `GridSearchCV`. This process of fine-tuning was crucial to find the optimal parameters and prevent overfitting, significantly boosting the model's predictive power.

---

## 🏆 Results

The final optimized **CatBoost model** was selected as the best performer, achieving an **AUC-ROC score of 0.849**. This high level of quality indicates that the model is highly effective at distinguishing between customers who will churn and those who will not, providing a reliable tool for the marketing team's retention campaigns.

| Model | AUC-ROC | Accuracy |
| :--- | :--- | :--- |
| **CatBoost (Optimized)** | **0.849** | **0.801** |
| Logistic Regression | 0.846 | 0.807 |
| CatBoost (Initial) | 0.837 | 0.792 |

---

## 📂 Repository Structure

* `01_Churn_EDA_and_Project_Plan.ipynb`: Contains the initial data exploration, analysis, and strategic plan.
* `02_Churn_Model_Development.ipynb`: The core of the project, detailing data preprocessing, feature engineering, model training, and hyperparameter tuning.
* `03_Churn_Solution_Report.ipynb`: A clean, non-technical summary of the project's findings, difficulties, and final recommendations, intended for a business audience.
