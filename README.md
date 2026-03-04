# 🏦 Bank Loan Status Prediction

การพยากรณ์สถานะการชำระหนี้ของลูกค้าธนาคาร ด้วย Machine Learning

🌐 **[ดู Portfolio Website](https://natpaphonnn.github.io/Bank_Loan/)**

---

## 📌 Overview

Project นี้มีเป้าหมายเพื่อสร้าง Machine Learning Model ที่สามารถคาดการณ์ได้ว่าลูกค้ารายใดจะ **ชำระหนี้ครบ (Fully Paid)** หรือ **ผิดนัดชำระ (Charged Off)** เพื่อช่วยธนาคารลดความเสี่ยงด้านสินเชื่อและตัดสินใจอย่างมีข้อมูลรองรับ

## 💡 Background

ในอุตสาหกรรมการเงิน การประเมินความเสี่ยงด้านสินเชื่อ (Credit Risk Assessment) เป็นหนึ่งในงานที่สำคัญที่สุด Project นี้เริ่มจากคำถามที่ว่า:

> *"เราสามารถใช้ข้อมูลประวัติเครดิตของลูกค้า เพื่อทำนายพฤติกรรมการชำระหนี้ในอนาคตได้หรือไม่?"*

## 📊 Dataset

| Dataset | Rows | Columns | Description |
|---------|------|---------|-------------|
| `credit_train.csv` | 100,514 | 19 | Training set พร้อม label `Loan Status` |
| `credit_test.csv` | 10,353 | 18 | Test set (ไม่มี label) |

**Features** ครอบคลุมข้อมูลส่วนตัว สินเชื่อ และประวัติเครดิต เช่น Credit Score, Annual Income, Monthly Debt, Home Ownership, Purpose เป็นต้น

## 🔍 Approach

1. **Exploratory Data Analysis (EDA)** — สำรวจ distribution, missing values, outliers, correlation
2. **Data Cleaning** — จัดการค่า 99,999,999 (placeholder), impute missing values, encode categoricals
3. **Feature Engineering** — สร้าง Debt-to-Income Ratio, Credit Utilization, Loan-to-Income Ratio
4. **Modeling** — ทดลอง 4 models: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting
5. **Hyperparameter Tuning** — GridSearchCV สำหรับ best model
6. **Evaluation** — Confusion Matrix, Classification Report, ROC Curve, Feature Importance

## 🏆 Results

- **Best Model**: Gradient Boosting (หลัง Hyperparameter Tuning)
- ประเมินด้วย Accuracy, Precision, Recall, F1 Score, AUC-ROC
- Features สำคัญที่สุด: Credit Score, Annual Income, Current Loan Amount

## 💼 Key Insights

- **Credit Score** เป็นตัวชี้วัดสำคัญที่สุดในการทำนาย default
- **Debt-to-Income Ratio** สูง → มีโอกาสผิดนัดชำระสูง
- **Short Term loans** มีอัตรา default ต่ำกว่า Long Term
- **Home Ownership** มีผลต่อพฤติกรรมการชำระ — เจ้าของบ้านมี default rate ต่ำกว่า

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-9F2B68)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

## 📁 Project Structure

```
Bank_Loan/
├── Bank_Loan_Status.ipynb   # Jupyter Notebook (EDA + Modeling)
├── index.html               # Portfolio Website
├── style.css                # Website Styles
├── script.js                # Website Interactivity
├── credit_train.csv         # Training Data
├── credit_test.csv          # Test Data
├── predictions.csv          # Model Predictions
└── assets/                  # Exported Charts
    ├── target_distribution.png
    ├── missing_values.png
    ├── numerical_distributions.png
    ├── correlation_heatmap.png
    ├── categorical_features.png
    ├── charged_off_rate.png
    ├── model_comparison.png
    ├── final_evaluation.png
    ├── feature_importance.png
    └── ...
```

## 🚀 Getting Started

```bash
# Clone repo
git clone https://github.com/Natpaphonnn/Bank_Loan.git
cd Bank_Loan

# เปิด Notebook
jupyter notebook Bank_Loan_Status.ipynb

# เปิด Website
open index.html
```

---

*Built with ❤️ and Machine Learning*
