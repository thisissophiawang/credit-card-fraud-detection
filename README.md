# Credit Card Fraud Detection

![Fraud Detection](https://github.com/thisissophiawang/credit-card-fraud-detection/blob/main/images/fraud-detection-banner.png)

## 📌 Project Overview  
This project implements advanced data mining techniques to detect fraudulent credit card transactions.  
With global fraud losses exceeding **$28.65 billion annually**, we aim to tackle key challenges such as **imbalanced data, computational efficiency, and evolving fraud patterns**.  

### 🔍 Key Challenges Addressed  
- **Severe Class Imbalance**: Only **0.17%** (492 out of 284,807) transactions are fraudulent.  
- **Computational Complexity**: **28 PCA-transformed features** requiring efficient processing.  
- **Evolving Fraud Patterns**: Adapting to **changing fraud tactics** over time.  

---

## 📊 Dataset  
We utilized the **[Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)** from Kaggle, which contains:  
✔ **284,807 transactions** (492 fraudulent cases)  
✔ **28 principal components** (from PCA transformation)  
✔ **Time elapsed features** and **transaction amounts**  
✔ **Anonymized data** to protect user privacy  

---

## ⚙️ Methodology  

### 1️⃣ Data Preprocessing  
✅ Feature scaling with **RobustScaler**  
✅ **Correlation analysis** and feature selection  
✅ **Class Imbalance Handling**: Implemented **SMOTE (Synthetic Minority Over-sampling Technique)**  
✅ **Stratified train-test splitting**  

### 2️⃣ Models Implemented  

#### 🔹 Random Forest Classifier  
✔ Optimized hyperparameters using **GridSearchCV**  
✔ Feature importance analysis  

#### 🔹 Neural Network  
✔ Multi-layer architecture optimized for fraud detection  
✔ Dropout layers to **prevent overfitting**  

---

## 📈 Evaluation Metrics  
- **Precision, Recall, and F1-Score**  
- **ROC Curve and AUC**  
- **Confusion Matrix Analysis**  

### 🚀 Results  

| Model            | Precision | Recall | F1-Score | AUC  |
|-----------------|-----------|--------|----------|------|
| Random Forest   | **0.96**  | 0.83   | 0.89     | 0.97 |
| Neural Network  | 0.89      | **0.91** | **0.90** | 0.96 |

---
## 🔮 Future Improvements  
- [ ] Implement **real-time fraud detection capability**  
- [ ] Explore **ensemble methods** for improved performance  
- [ ] Develop an **adaptive learning approach** for evolving fraud patterns* 
- [ ] Create a **web-based dashboard** for monitoring fraud detection metrics


## 💻 Installation and Usage  

### 📌 Requirements  
```plaintext
numpy==1.26.4
pandas==2.2.1
scikit-learn==1.4.2
tensorflow==2.15.0
matplotlib==3.8.3
seaborn==0.13.2
imbalanced-learn==0.12.0




