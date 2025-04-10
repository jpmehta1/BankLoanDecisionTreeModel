🔍 Overview
This project explores a supervised machine learning approach to predict loan approval outcomes based on financial and credit-related variables. By using a decision tree classifier, the model produces human-readable rules, helping both developers and stakeholders understand how decisions are made.

🗂 Dataset
Source: Kaggle - Financial Risk for Loan Approval

Size: 20,000 synthetic records

Target Variable: LoanApproved

1 = Approved

0 = Rejected

🔢 Key Features Used
RiskScore

DebtToIncomeRatio

TotalDebtToIncomeRatio

(Plus additional optional features explored for experimentation)

🎯 Goals
Develop an accurate and interpretable decision tree model for loan approval prediction

Identify the most influential financial indicators

Understand how tree depth and feature selection impact performance

Evaluate whether a minimalist model can rival a full-feature model

⚙️ Methodology
One-hot encoded categorical features where necessary

Trained decision tree classifiers with various depths (max_depth=None, max_depth=5, etc.)

Evaluated using:

Accuracy

Feature importance

F1-score, precision, recall

Decision tree visualization

Performed feature correlation analysis to evaluate redundancy

Compared performance across different feature subsets:

RiskScore alone

RiskScore + Debt Ratios

All available features

📈 Results
Best accuracy: ~98.7% with max_depth=None using just 3 features

Minimal model (only RiskScore) achieved 97.5% accuracy

Feature correlation showed RiskScore, DebtToIncomeRatio, and TotalDebtToIncomeRatio are not strongly redundant (low-moderate correlation)

Interpretable rules extracted from tree visualization:

RiskScore <= 44.9 → likely rejection

RiskScore > 46.7 → likely approval

🧠 Key Insights
RiskScore is by far the most influential predictor in the dataset

Debt ratio features contribute marginal improvements

Simpler models can achieve competitive performance while remaining interpretable

Decision trees provide a transparent and explainable path to automated decision systems

🔮 Next Steps (Planned: Phase 2 & 3)
Phase 2: Compare against ensemble models such as:

Random Forest

Gradient Boosting (XGBoost / LightGBM)

Apply cross-validation and hyperparameter tuning for robust evaluation

Explore model fairness across subgroups (if demographic data is available)

Build a lightweight CLI or web demo for real-time predictions

Phase 3: Explore deep learning architectures to uncover deeper feature interactions and non-linear patterns using:

Fully connected neural networks

Additional hidden layers and optimizers

Performance comparison with traditional ML models

🧰 Tech Stack
Python 3

pandas, scikit-learn, matplotlib, seaborn

Jupyter Notebook / HTML Report
