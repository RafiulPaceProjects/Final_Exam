# 🛡️ Online Payment Fraud Detection  
**Author:** Rafiul Haider  
**Final Exam Project | Machine Learning | 2025**

---

## 📌 Overview  
This project focuses on identifying fraudulent transactions in online payment systems using supervised machine learning. Through detailed **Exploratory Data Analysis (EDA)** and **feature engineering**, we trained multiple models to detect fraud and predict transaction amounts.

---

## 🎯 Objectives  
- Detect fraudulent transactions using classification models  
- Predict transaction `amount` using regression  
- Analyze model performance with varying data sizes  
- Identify key features that signal fraud

---

## 📊 Dataset  
The dataset includes features such as:
- `step`, `amount`, `oldbalanceOrg`, `newbalanceOrig`, `oldbalanceDest`, `newbalanceDest`,  
- `type` (e.g., `TRANSFER`, `PAYMENT`, `CASH_OUT`)  
- `isFraud` (target for classification)  
- `isFlaggedFraud` (system-flagged indicator)

---

## 🧠 Models Used  

### 🔹 Classification (`isFraud`)
| Model               | Accuracy | Precision (Fraud) | Recall (Fraud) | F1-score (Fraud) |
|--------------------|----------|-------------------|----------------|------------------|
| Logistic Regression| 99.92%   | 76%               | 33%            | 0.46             |
| Decision Tree      | 99.94%   | 96%               | 47%            | 0.63             |
| Random Forest      | 99.97%   | 96%               | 76%            | **0.85**         |

✅ **Random Forest** was the most accurate and balanced for detecting fraud.

### 🔸 Regression (`amount`)
- **Linear Regression** achieved an **R-squared score of ~0.48**  
- It captured general transaction trends, but struggled with sharp spikes and outliers.

---

## 🔧 Feature Engineering  
Key transformations:
- `diffOrig` = `newbalanceOrig` - `oldbalanceOrg`  
- `diffDest` = `newbalanceDest` - `oldbalanceDest`  
- One-hot encoding on `type` (e.g., `type_TRANSFER`, `type_PAYMENT`)  

📌 **Top Features for Fraud Detection**:
1. `type_TRANSFER`  
2. `diffDest`  
3. `newbalanceDest`  
4. `oldbalanceDest`  
5. `amount`

---

## 📈 Results & Insights  
- Machine learning models were highly effective in identifying fraud.  
- Even small fractions of the dataset yielded high accuracy.  
- Random Forest provided the **best balance of precision and recall**.  
- Linear Regression offered useful insights for modeling transaction behavior.

---

## 📂 Project Structure  
- `EDA` – Visualizations and correlation analysis  
- `Feature Engineering` – Derived features and encodings  
- `Model Training` – Logistic Regression, Decision Tree, Random Forest, Linear Regression  
- `Performance Evaluation` – Accuracy, F1-score, R², data fraction testing  
- `Visualizations` – Graphs for model accuracy and prediction tracking

---

## 💻 Requirements  
- Python 3.8+  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn

---

## 📁 Files Included  
- `FINAL_EXAM_HAIDER_RAFIUL.ipynb` – Full project notebook  
- Visualizations (Accuracy & R² graphs, prediction trends)  
- `README.md` – Project summary (this file)

---

## ✅ Conclusion  
This project shows how **machine learning can effectively detect online fraud** by analyzing patterns in transaction behavior. With the right features and models, we can build reliable systems to help protect digital payments.

---

