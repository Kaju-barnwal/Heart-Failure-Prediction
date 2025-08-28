# 🫀 Heart Failure Prediction (ML Models)

📊 Project Goal
This project aims to build machine learning models to predict heart failure risk (Alive = 0, Died = 1) using patient clinical records. This can help healthcare providers identify high-risk patients early and take preventive measures.

## 📌 Project Overview
This project applies **Machine Learning** techniques to predict **heart failure risk** using patient clinical records.  
By identifying high-risk patients early, healthcare providers can take preventive action and improve survival rates.

Dataset: [UCI Heart Failure Clinical Records](https://raw.githubusercontent.com/Kaju-barnwal/DataSets/refs/heads/main/heart_failure_clinical_records_dataset.csv)

---
## 📂 Project Structure
- `heart_failure_prediction.py` → Main code file
- `requirements.txt` → Python dependencies
- `results/` → Confusion matrices, ROC curves, model comparison

---

Dataset Overview

Total Samples: 299

Features: 12 (age, anaemia, diabetes, ejection fraction, serum creatinine, smoking, etc.)

Target Variable: DEATH_EVENT (0 = Alive, 1 = Died)

Class Balance: Imbalanced (more Alive than Died cases)

---

## 🧪 Models Used
- **Logistic Regression** (baseline, interpretable model)  
- **Decision Tree Classifier** (handles non-linearity, depth=5)  
- **Random Forest Classifier** (ensemble of 100 trees, depth=7)  

---

## 📊 Results Summary

| Model                | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-----------------------|----------|-----------|--------|----------|---------|
| Logistic Regression   | 0.79     | 0.68      | 0.66   | 0.67     | 0.86    |
| Decision Tree         | 0.74     | 0.58      | 0.72   | 0.65     | 0.75    |
| Random Forest         | **0.83** | **0.82**  | 0.62   | 0.71     | **0.89** |

- **Random Forest** → Best overall model (highest accuracy & ROC-AUC).  
- **Decision Tree** → Best recall (catches more true positives).  
- **Logistic Regression** → Balanced performance + interpretability.  

---
# Analysis of Results: -
→ Logistic Regression performed well (ROC-AUC = 0.86), showing it captures key patterns despite being a simple linear model.
→ Decision Tree has a higher recall (0.72), meaning it is better at catching patients at risk of death, but at the cost of precision.
→ Random Forest is the best overall model with the highest accuracy (83%), precision (82%), and AUC (0.89). However, recall (0.62) indicates some true high-risk patients are still missed.

## 📈 Visualizations
- Confusion Matrices for all models  
- ROC Curve comparison with AUC scores

# Business/Healthcare Implications:-
Logistic Regression is interpretable → doctors can see which factors influence mortality.
Random Forest provides the best balance between predictive power and generalization. It could be deployed in real-world hospital settings to flag high-risk patients.
Decision Tree is simpler but less stable; however, its higher recall could be valuable if the goal is to minimise missed deaths (catch more true positives).


