# 📊Customer Churn Prediction 

Business-focused machine learning project to predict customer churn in IT services using a **cost-sensitive approach**.  
Primary goal: **minimize False Negatives** to ensure high-risk customers are not missed.

---

## Project Overview

Customer churn directly impacts revenue and long-term customer value.  
This project uses an imbalanced dataset (~20% churn) and prioritizes **actionable insights** over overall accuracy.  
Synthetic oversampling (SMOTE) is intentionally avoided to preserve the real-world data distribution and deployment reliability.

---

## Interactive Notebook

All analysis, modeling, and evaluation are included in a single notebook:  
 - [🔍 View Full Notebook on NBViewer](https://nbviewer.org/github/Sirgic7/Cost-Sensitive-Churn-Detection-No-SMOTE-FN-Optimized-/blob/main/notebook/churn-prediction.ipynb)

Contains EDA, data preprocessing, model training, threshold tuning, and evaluation.  
You can view it directly on **NBViewer** or **download** GitHub it to run locally.

---

## Approach

- **No SMOTE / No resampling** – original data distribution preserved  
- **Cost-sensitive modeling** using class weighting  
- **Decision threshold tuning** – final threshold set to **0.4**  
- **Evaluation focus** – Confusion Matrix and False Negatives over accuracy  
- **EDA** – basic exploration with heatmaps and boxplots

---

## Models

Several models were evaluated to identify churned customers effectively:

- **Logistic Regression** – served as a baseline model; achieved moderate recall but missed several churners.  
- **XGBoost Classifier** – performed well with class weighting and threshold tuning, but CatBoost ultimately gave the lowest False Negatives.  
- **Random Forest Classifier** – used as a stable benchmark alongside CatBoost.  
- **CatBoost Classifier** – final model, optimized for minimal False Negatives and reliable detection of churned customers.

All models were tuned with a cost-sensitive approach, prioritizing business-critical errors over overall accuracy.

---

## Results

- **Metric focus:** Confusion Matrix  
- CatBoost achieved the lowest False Negatives  
- Random Forest used as a stable benchmark  
- Threshold tuning improved detection of churners without heavily sacrificing overall performance

---

## Project Structure

├── notebooks/

│     └── churn-prediction.ipynb

├── data/

│     └── Telco_Cusomer_Churn.csv    

├── requirements.txt

└── README.md

---

## Tech Stack

- Python
- Jupyter Notebook
- Pandas, NumPy
- Matplotlib , seaborn , missingno
- Scikit-learn
- CatBoost , XGBoost
---

## Author

Parham Karkoubzadeh – [GitHub](https://github.com/Sirgic7)
