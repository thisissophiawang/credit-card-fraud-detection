# Credit Card Fraud Detection

![Fraud Detection](https://github.com/thisissophiawang/credit-card-fraud-detection/blob/main/banner.png)

## 📌 Project Overview

This project implements advanced data mining techniques to detect fraudulent credit card transactions.

With global fraud losses exceeding **$28.65 billion annually**, we aim to tackle key challenges such as **imbalanced data, computational efficiency, and evolving fraud patterns**.

### 🔍 Key Challenges Addressed

- **Severe Class Imbalance**: Only **0.17%** (492 out of 284,807) transactions are fraudulent
- **Computational Complexity**: **28 PCA-transformed features** requiring efficient processing
- **Evolving Fraud Patterns**: Adapting to **changing fraud tactics** over time

## 📊 Dataset

We utilized the **[Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)** from Kaggle, which contains:

✔ **284,807 transactions** (492 fraudulent cases)  
✔ **28 principal components** (from PCA transformation)  
✔ **Time elapsed features** and **transaction amounts**  
✔ **Anonymized data** to protect user privacy

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

✅ Feature scaling with **RobustScaler**  
✅ **Correlation analysis** and feature selection  
✅ **Class Imbalance Handling**: Implemented **SMOTE (Synthetic Minority Over-sampling Technique)**  
✅ **Outlier Detection**: Used **Isolation Forest** to identify and handle anomalies  
✅ **Stratified train-test splitting**

### 2️⃣ Models Implemented

#### 🔹 Random Forest Classifier

✔ **Configuration**: 100 trees, max depth of 10, balanced class weights  
✔ **ROC-AUC Score**: 0.979  
✔ **Threshold Optimization**: Improved F1 score from 0.5784 to 0.8021 (38.67% improvement)  
✔ Feature importance analysis

#### 🔹 Neural Network

✔ **Architecture**: Three hidden layers (64, 32, 16 neurons) with batch normalization  
✔ **Activation**: ReLU for hidden layers, Sigmoid for output  
✔ **Optimization**: Adam with learning rate of 0.001  
✔ **Dropout layers** (0.3) to prevent overfitting

## 📈 Evaluation Metrics

- **Precision, Recall, and F1-Score**
- **ROC Curve and AUC**
- **Confusion Matrix Analysis**
- **Probability Distribution Analysis**

### 🚀 Results

| Model | Precision | Recall | F1-Score | AUC |
|-------|-----------|--------|----------|-----|
| Random Forest | **0.96** | 0.83 | 0.89 | 0.97 |
| Neural Network | 0.89 | **0.91** | **0.90** | 0.96 |

### 📊 Performance Insights

- **Random Forest**: Better interpretability with clearer feature importance rankings
- **Neural Network**: Superior at capturing complex fraud patterns with fewer false positives
- **Threshold Optimization**: Critical for improving model performance in imbalanced datasets

## 🔬 Key Findings

1. **Model Performance Enhancement**: Neural Network achieved high recall (0.85) and precision (0.87)
2. **SMOTE's Role**: Transformed dataset from 0.17% fraudulent transactions to a balanced distribution
3. **Comparative Insights**: Random Forest provided better interpretability while Neural Network reduced false positives

## 🔮 Future Improvements

- [ ] Implement **real-time fraud detection capability**
- [ ] Explore **ensemble methods** for improved performance
- [ ] Develop an **adaptive learning approach** for evolving fraud patterns
- [ ] Create a **web-based dashboard** for monitoring fraud detection metrics
- [ ] Implement **XAI techniques** (SHAP, LIME) for better model interpretability

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
```

### 🚀 Setup and Execution

```bash
# Clone the repository
git clone https://github.com/thisissophiawang/credit-card-fraud-detection.git
cd credit-card-fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run the preprocessing pipeline
python src/preprocessing.py

# Train and evaluate models
python src/train_models.py
```

## 📋 Project Structure

```
credit-card-fraud-detection/
├── data/                          # Dataset files
├── models/                        # Saved model files
├── notebooks/                     # Jupyter notebooks for exploration
├── src/                           # Source code
│   ├── preprocessing.py           # Data preprocessing pipeline
│   ├── models.py                  # Model implementations
│   ├── evaluation.py              # Model evaluation metrics
│   └── visualization.py           # Visualization utilities
├── requirements.txt               # Project dependencies
└── README.md                      # Project documentation
```

## 🔗 References

- Breiman, L. (2001). Random Forests. *Machine Learning*, 45(1), 5-32.
- Chawla, N. V., et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique. *Journal of Artificial Intelligence Research*, 16, 321-357.
- Dal Pozzolo, A., et al. (2015). Calibrating Probability with Undersampling for Unbalanced Classification. *IEEE Symposium Series on Computational Intelligence and Data Mining*.
- Fernández, A., et al. (2018). Learning from Imbalanced Data Sets. *Springer*.





