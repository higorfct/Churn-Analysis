# Churn Analysis


# 📊 Project: Customer Churn Analysis

## 📝 Introduction

This project aims to identify the key factors leading to customer churn in a bank operating in Germany, Spain, and France, using data analysis and machine learning techniques.

---

## 🚀 How to use

1. **Clone the repository and install dependencies:**
    ```bash
    git clone https://github.com/higorfct/Churn-Analysis
    cd Churn=Analysis
    pip install -r requirements.txt
    ```
---

## 📊 Data

The data used contains customer demographic and transactional information, including variables such as **age**, **balance**, **estimated salary**, **contracted products**, and whether the customer has left the bank.

### Steps performed:
- Importation of the dataset `Churn_treino.csv` using `;` as the separator
- Analysis of churn distribution by **geographic location**, **age**, and **gender**
- Checking for outliers
- Checking for missing values
- Encoding of categorical variables with `LabelEncoder`
- Standardization of numerical variables with `StandardScaler`
- Balancing the dataset using **SMOTE** to address class imbalance on the target variable

---

## 🤖 Predictive Modeling

Applied models:
- Neural Network (Keras)
- Logistic Regression
- Random Forest
- Naive Bayes
- SVM
- AdaBoost
- XGBoost
- KNN
- LightGBM

All models were trained using `train_test_split` and evaluated according to the metrics **accuracy**, **precision**, **recall**, and **F1-score**.

---

## 🔍 Key Insights

- Older customers tend to churn more frequently.
- Customers from **Germany** showed the highest churn rate.
- Women showed a slightly higher tendency to churn compared to men.
- The "Balance" variable alone is not sufficient to predict churn, but combined with age and number of products, its predictive power increases.
- The **XGBoost** model showed the best performance among the tested algorithms.

---

## 📈 Visualizations

- Bar chart of churn by location (`Geography`)
- Age histogram stratified by churn
- Bar chart of churn by gender
- Confusion matrix of the main models
- Metrics comparison chart for the models
- Local explanations with LIME for XGBoost model results

---

## 🛠️ Tools Used

- **Python** – Main programming language  
- **Pandas** – Data manipulation and analysis  
- **Seaborn / Matplotlib** – Graphical visualization  
- **Scikit-learn** – Predictive modeling and metrics  
- **Keras / TensorFlow** – Neural network construction  
- **XGBoost / LightGBM** – Boosting models  
- **LIME** – Model explainability  
- **Imbalanced-learn (SMOTE)** – Class balancing  
- **Jupyter Notebook** – Development environment  

---

## ✅ Results

- The **LightGBM** model achieved the best metrics. However, despite outperforming the other models in this respect, metrics such as **F1-Score** and **recall** were still quite low, indicating difficulty in identifying actual churners.
- The LIME explainable AI technique was used to uncover factors that contribute or not to customer churn.
- Factors that reduce churn risk are: **age (younger = lower risk)**, **time as a customer**, and **engagement as an active member**.
- Factors related to churn are: **high salary**, **high balance (greater ability to switch banks)**, **few contracted products**, and **below-average score (perceived insecurity)**.

---

## 💼 Financial Impact of the LightGBM Model

Defining:

- **Average revenue per customer:** €$ 100.00;
- **Metric used:** True Positives (TP) — customers who would actually leave but were correctly identified by the model;
- **Hypothesis:** all customers identified as TP are successfully retained.

The LightGBM model, even with some metrics lower than desired (Recall and Precision), showed potential to generate a **potential savings of €$ 32,600.00**

## 🧠 Conclusions

The project demonstrated how it is possible to use **data analysis and machine learning** to:

- Identify profiles with higher propensity to churn;
- Apply data balancing techniques to improve model quality;
- Assess different algorithms to find the most suitable for the problem;
- Use tools like **LIME** to interpret decisions from complex models.

---

## 🔄 Next Steps

- Deploy models to a production environment with continuous monitoring.
- Perform advanced hyperparameter tuning using **GridSearch**, **RandomSearch**, or **Bayesian Optimizer** to find better **F1-Score** and **Recall** metrics, since when these metrics are low, many churners are not detected.

---

🧑‍💻 **Author and Contact**

**Higor Roberto Coutinho Caetano**  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com  
