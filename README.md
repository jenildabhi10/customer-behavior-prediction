# 🛍️ Customer Behavior Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green?style=flat-square&logo=pandas)
![Scikit-learn](https://img.shields.io/badge/ScikitLearn-ML-red?style=flat-square&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

An end-to-end machine learning project that analyzes customer purchase behavior, segments customers using K-Means clustering, and predicts churn — helping businesses retain high-value customers.

---

## 📌 Project Overview

Businesses lose revenue when they can't identify customers likely to churn. This project:

- Cleans and explores messy real-world customer transaction data
- Segments customers into meaningful groups using **K-Means Clustering**
- Predicts **customer churn** using Logistic Regression & Random Forest
- Surfaces actionable business insights from the analysis

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Customer Segments Found | 3 |
| Churn Prediction Accuracy | ~88% |
| Best Model | Random Forest |
| F1 Score (Churn Class) | ~0.84 |
| Top Churn Indicator | Low purchase frequency + high return rate |

---

## 🗂️ Project Structure

```
customer-behavior-prediction/
│
├── Customer Analysis.ipynb            # Full pipeline: EDA → Segmentation → Prediction  
├── data/
│   ├── messy_customer_purchases.csv   # Raw dataset
│   └── cleaned_customer_purchases.csv # Cleaned dataset
├── requirements.txt
└── README.md
```

---

## 📂 Dataset

| Property | Details |
|----------|---------|
| Source | Synthetic customer purchase data |
| Records | ~1,000 customers |
| Features | Age, Gender, Purchase Amount, Frequency, Return Rate, Category |
| Target | Churn (Yes/No) |

---

## 🔍 Approach

### 1. 🧹 Data Cleaning
- Removed duplicate records and null values
- Fixed inconsistent data types (dates, categories)
- Capped outliers in purchase amount using IQR method

### 2. 📊 Exploratory Data Analysis
- Distribution of spending across age groups and categories
- Correlation heatmap between features
- Purchase frequency vs churn rate analysis

### 3. 🔵 Customer Segmentation (K-Means)
- Applied elbow method to find optimal k=3 clusters
- **Segment A** — High spenders, loyal, low churn risk
- **Segment B** — Medium spenders, occasional buyers
- **Segment C** — Low spenders, high return rate, high churn risk

### 4. 🤖 Churn Prediction
- Trained Logistic Regression and Random Forest classifiers
- Handled class imbalance using SMOTE
- Evaluated using Precision, Recall, F1, and AUC-ROC

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.8+ |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Environment | Jupyter Notebook |

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/jenildabhi10/customer-behavior-prediction.git
cd customer-behavior-prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter and run the notebook
jupyter notebook "Customer Analysis.ipynb"
```

---

## 💡 Business Insights

- Customers with fewer than 2 purchases/month and over 20% return rate are 3x more likely to churn
- High-value Segment A customers generate 65% of total revenue despite being only 28% of users
- Targeting Segment C with retention campaigns could reduce churn by an estimated 18%

---

## 🚀 Future Improvements

- Build an interactive Streamlit dashboard for real-time churn prediction
- Add RFM (Recency, Frequency, Monetary) analysis
- Deploy as a REST API using FastAPI

---

## 👤 Author

**Jenil Dabhi** — [@jenildabhi10](https://github.com/jenildabhi10)

---

## 📄 License

This project is licensed under the MIT License.
