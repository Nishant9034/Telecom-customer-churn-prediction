# 📡 Telecom Customer Churn Prediction

A machine learning project to predict whether a telecom customer will churn (leave the service), using classification models trained on customer demographic and usage data.

---

## 🗂️ Project Structure

```
telecom-churn-prediction/
│
├── telecom_churn.csv                          # Dataset
├── Telecom_customer_churn_prediction.ipynb    # Main notebook
└── README.md
```

---

## 📊 Dataset

- **Source:** Telecom customer records
- **Records:** 1,000 rows
- **Target Variable:** `Churn` (0 = No, 1 = Yes)

### Features

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `SeniorCitizen` | Whether the customer is a senior citizen (0/1) |
| `tenure` | Number of months the customer has stayed |
| `MonthlyCharges` | Monthly billing amount |
| `TotalCharges` | Total charges over the customer's tenure |
| `Contract` | Contract type (Month-to-month / One year / Two year) |
| `InternetService` | Internet service type (DSL / Fiber Optic / No) |
| `PaymentMethod` | Payment method used |
| `TechSupport` | Whether customer has tech support (Yes/No) |
| `OnlineSecurity` | Whether customer has online security (Yes/No) |

---

## 🛠️ Tech Stack

- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

---

## 🔄 Workflow

### 1. Exploratory Data Analysis (EDA)
- Churn distribution analysis
- Senior Citizen vs Churn
- Contract Type vs Churn (bar + pie charts)
- Internet Service vs Churn
- Monthly Charges and Tenure distribution

### 2. Data Preprocessing
- Dropped `customerID` (non-informative)
- One-hot encoding for categorical variables
- Feature scaling using `StandardScaler` on numerical columns
- 80/20 stratified train-test split

### 3. Model Building
Two classification models were trained and evaluated:
- **Logistic Regression**
- **Random Forest Classifier**

### 4. Hyperparameter Tuning
Both models were tuned using `GridSearchCV` for optimal performance.

### 5. Model Evaluation
Metrics used: Accuracy, ROC AUC Score, Classification Report, Confusion Matrix

---

## 📈 Results

| Model | Accuracy | ROC AUC |
|---|---|---|
| Tuned Logistic Regression | 0.690 | **0.771** |
| Tuned Random Forest | 0.655 | 0.749 |

> ✅ **Best Model: Tuned Logistic Regression** — higher accuracy and ROC AUC score, with better interpretability.

---

## 🔍 Key Findings

- **Contract Type** is a major churn driver — month-to-month customers churn significantly more
- **Senior Citizens** have a higher churn rate
- **Fiber Optic** internet service users churn more than DSL users
- Customers with **higher monthly charges** and **lower tenure** are more likely to churn
- Top features: `Contract_Two year`, `MonthlyCharges`, `TotalCharges`, `tenure`, `InternetService_Fiber optic`, `OnlineSecurity_Yes`


## 👤 Author

**Nishant Kumar**  
B.Tech, Production & Industrial Engineering  
NIT Jamshedpur  
[GitHub](https://github.com/Nishant9034)
v
