🔍 Overview
This project explores a supervised machine learning approach to predicting loan approval decisions using financial and risk-based metrics. The model is trained using a decision tree classifier on a structured dataset and provides an interpretable rule-based system for decision-making.

🗂 Dataset
Source: Kaggle — Financial Risk for Loan Approval

Records: 20,000 synthetic entries

Target Variable: LoanApproved (1 = Approved, 0 = Rejected)

Features Used:

RiskScore

DebtToIncomeRatio

TotalDebtToIncomeRatio

(plus optional features for experimentation)

🎯 Project Goals
Build an accurate and interpretable loan approval model using a decision tree.

Identify the most influential features contributing to approval decisions.

Explore how model performance changes with tree depth and feature selection.

Determine if a minimalist model can perform nearly as well as a full-feature model.

⚙️ Methodology
Preprocessed categorical features with one-hot encoding (where needed).

Trained decision tree models with various depths (max_depth=None, max_depth=5, etc.).

Evaluated models using accuracy, feature importance, and visualization of the tree.

Analyzed feature correlation to assess redundancy.

Compared performance using:

RiskScore alone

Risk + Debt-to-Income ratios

All features

📈 Results
Best accuracy: ~98.7% on test set with max_depth=None using 3 features.

Single feature model (RiskScore) achieved 97.5% accuracy — making it a strong solo predictor.

Correlation analysis showed low-to-moderate correlation between RiskScore, DebtToIncomeRatio, and TotalDebtToIncomeRatio, confirming non-redundancy.

Decision tree visualizations clearly revealed interpretable thresholds like:

RiskScore <= 44.9 → likely rejection

RiskScore > 46.7 → likely approval

🧠 Key Insights
RiskScore is the dominant factor in loan approval decisions.

Debt-to-income metrics offer slight improvements but add complexity.

A simple model with a few well-chosen features can perform nearly as well as a full model.

Decision trees offer a transparent way to turn models into business rules.

📌 Next Steps (Optional)
Compare with ensemble models (e.g., Random Forests or XGBoost).

Use cross-validation for more robust evaluation.

Build a lightweight demo app to simulate predictions.

Explore fairness by evaluating performance across demographic subgroups (if data allows).

🧰 Tech Stack
Python 3

pandas, scikit-learn, matplotlib, seaborn

Jupyter Notebook
