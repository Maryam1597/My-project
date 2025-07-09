ICU Mortality Prediction using MIMIC-III Dataset
This project focuses on predicting in-hospital mortality of ICU patients using a curated version of the MIMIC-III Clinical Classifier dataset. We apply machine learning techniques, emphasizing both clinical relevance and predictive performance.

📊 Dataset Description
The dataset used is a publicly available, preprocessed version of the MIMIC-III dataset, published on Kaggle by Dr. Scarlat (mimic3c.csv). It contains structured records for ICU patients, including:

Demographics: age, gender, marital status, ethnicity

Admission info: admit type, location, insurance

Clinical events: labs, medications, procedures, notes

Outcome: ExpiredHospital (target variable: binary indicator of in-hospital mortality)

This version of the dataset is de-identified and ethically sourced for open research use.

⚙️ Data Preprocessing and Feature Engineering
Key preprocessing and feature engineering steps included:

Cleaning: Removed irrelevant columns (e.g., IDs, free text fields).

Encoding: One-hot encoded categorical features like gender, insurance, ethnicity.

Normalization: Log transformation of skewed features.

Feature Engineering:

interactions_per_day: Care intensity metric.

lab_rx_ratio: Diagnostic vs. treatment indicator.

proc_diag_ratio: Procedure aggressiveness.

chart_density: Monitoring frequency.

high_intensity_flag: Binary indicator for complex cases.

Final dataset comprised cleaned numeric and engineered features, one-hot encoded categoricals, and the target variable expired.

🤖 Modeling and Evaluation
Models Used:
Logistic Regression: Interpretable baseline model.

Random Forest Classifier: Ensemble method for capturing complex interactions.

Workflow:
80/20 train-test split with stratified sampling.

Evaluation metrics:

Accuracy

Precision

Recall

F1-Score

AUC-ROC

Key Results:
Random Forest outperformed Logistic Regression in all metrics.

Important predictors: interactions_per_day, LOSdays, total events.

Visualizations:
Confusion Matrix

ROC Curve

Feature Importance Plot

