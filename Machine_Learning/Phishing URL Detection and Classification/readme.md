# 🚀 Phishing URL Detection Using Machine Learning

## 📌 Project Overview
Phishing attacks are a growing cybersecurity threat, tricking users into sharing sensitive information. Traditional blacklist-based detection methods fail to keep up with evolving phishing tactics. This project leverages **machine learning** to build an intelligent phishing URL detection system that **learns, adapts, and accurately classifies phishing URLs**.

## 🎯 Business Value
- **Proactive Threat Detection:** Identifies phishing URLs dynamically, outperforming static blacklists.
- **Scalable & Deployable:** Designed for real-time integration into security platforms.
- **Explainable AI:** Uses **SHAP analysis** to ensure transparency in model decisions.
- **Applicable to Industries:** Financial institutions, e-commerce, and cybersecurity firms can leverage this model to **reduce fraud and protect user data**.

---

## 🔍 Dataset & Preprocessing
- **Dataset:** ~11,000 labeled URLs (55% phishing, 45% legitimate) with **30 key features** related to URL structure, domain metadata, and content analysis.
- **EDA & Feature Engineering:**
  - **Univariate Analysis & Pairplots:** Explored key features like `URL_Length` and `Abnormal_URL`.
  - **Correlation Heatmap:** Identified feature relationships and removed redundant features.
  - **Feature Selection:** Retained high-impact features like `SFH`, `Abnormal_URL`, and `Redirect` for optimal performance.

---

## 🏆 Model Selection & Performance
Multiple machine learning models were tested, and **XGBoost** emerged as the best performer.

| Model                | Accuracy  | Precision | Recall  | F1-Score |
|----------------------|----------|-----------|---------|----------|
| Logistic Regression | 93.4%     | 0.93      | 0.92    | 0.92     |
| Random Forest       | 94.3%     | 0.95      | 0.95    | 0.95     |
| Gradient Boosting   | 94.3%     | 0.95      | 0.95    | 0.95     |
| **XGBoost**         | **94.7%** | **0.95**  | **0.96**| **0.95** |   |
| KNN                 | 93.3%     | 0.93      | 0.95    | 0.94     |
| Naive Bayes         | 67.6%     | 0.57      | 1.00    | 0.73     |

🔹 **Hyperparameter Tuning:**  
- Used **GridSearchCV** to optimize `n_estimators`, `max_depth`, `learning_rate` (XGBoost), and `max_features` (Random Forest).  
- Improved model performance and reduced overfitting.

---

## 🧐 Explainability & SHAP Analysis
To ensure model transparency, **SHAP (SHapley Additive exPlanations)** was used to interpret predictions:
- **Key Features:** `URL_Length`, `SFH`, and `Abnormal_URL` were the most impactful.
- **Visualizing Feature Contributions:** SHAP summary plots explained how each feature influenced phishing predictions.

![SHAP Analysis](images/shap_analysis.png)

---

## 🚀 Deployment & Future Improvements
✔ **Deployment Ready:** The model can be integrated into **real-time phishing detection systems**.  
✔ **Scalable & Adaptable:** Works for enterprises, security providers, and cloud-based platforms.  
✔ **Next Steps:**
  - Implement **real-time detection API**.
  - Address class imbalance using synthetic data.
  - Explore **transfer learning for improved generalization**.

---

### 📂 Clone the Repository
```bash
git clone https://github.com/PriyaNutulapati/ML-AI-Projects)/phishing-url-detection.git
cd phishing-url-detection
