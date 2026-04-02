A machine learning project to detect fraudulent transactions with a focus on handling imbalanced data and making practical trade-offs between catching fraud and reducing false alarms.

What I did
Tuned an XGBoost model using RandomizedSearchCV with stratified CV
Added an anomaly score using Isolation Forest as a feature
Handled class imbalance using SMOTE (only on training data)
Evaluated using ROC-AUC and Precision–Recall curve
Tuned decision threshold instead of using default 0.5
Approach
Performed basic EDA to understand fraud distribution
Applied stratified train-test split
Tuned model using RandomizedSearchCV (no leakage)
Generated anomaly score using Isolation Forest
Applied SMOTE on training data
Trained final model with best parameters
Evaluated using probabilities and selected optimal threshold
Metrics
Recall (catch fraud)
Precision (reduce false alarms)
F1-score (balance)
ROC-AUC
Precision-Recall Curve
Key Insight

Combining anomaly detection with supervised learning improves performance, but the biggest improvement came from threshold tuning, which helped balance recall and precision effectively.

Tech Stack

Python, Scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn

Future Work
Use scale_pos_weight instead of SMOTE
Add probability calibration
Deploy using FastAPI
