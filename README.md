# 🔍 Healthcare Insurance Fraud Detection System

## 🎯 Objective
This project is an end-to-end Machine Learning pipeline designed to classify fraudulent vs. genuine healthcare insurance claims. Built as part of a task by Future Interns, it processes over 550,000 historical claims to identify hidden patterns of financial risk.

## 🛠️ Tools & Technologies
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Algorithm:** Random Forest Classifier (with Class Weighting for severe imbalance)

## 📁 Dataset
Due to size constraints, the raw dataset is not hosted in this repository. 
You can download the original Healthcare Provider Fraud dataset from [Kaggle here](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis).

## ✨ Key Technical Highlights
1. **Relational Data Merging:** Combined Inpatient, Outpatient, and Beneficiary records into a unified monolithic dataset.
2. **Feature Engineering:** Extracted critical risk indicators like `ClaimDuration` and `PhysicianCount`.
3. **Imbalanced Data Handling:** Applied `class_weight='balanced'` within the Random Forest model to mathematically prioritize the rare minority class (fraud).
4. **Evaluation:** Strictly graded using Precision, Recall, and F1-Score rather than baseline accuracy.

## 📊 Business Insights
The model successfully identified that the strongest indicators of potential fraud include:
* **Inpatient Annual Reimbursement Amounts:** Exceptionally high yearly payouts.
* **Claim Duration:** Abnormally long or erratic recovery timelines.
* **Physician Count:** A high number of attending/operating doctors on routine claims (indicating potential "upcoding").
