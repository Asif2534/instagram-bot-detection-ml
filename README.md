# Detecting Artificial Engagement on Instagram with Machine Learning

**Applied Big Data & Visualisation (CS6502) – MSc Business Analytics, University of Limerick** | Group project (6 members)

## Business problem
Bots and fake accounts inflate engagement metrics. Advertisers end up paying for fake reach, and genuine creators lose out. This project classifies users as showing normal or artificial engagement.

## Data
- Large-scale Instagram user-behaviour dataset: **1.5M+ user records**
- 58 original features, reduced to 23 selected features

## Method
- Data processing in **Spark**, then modelling in Python (pandas, scikit-learn, XGBoost)
- Feature engineering: activity intensity, interaction quality, network imbalance
- The dataset had no bot labels, so we built a rule-based target from a behavioural score
- Models compared: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, Linear SVM, XGBoost
- F1 score was the main metric because the classes are imbalanced

## Key findings
- **Gradient Boosting (after tuning) performed best**, with XGBoost close behind
- Suspicious accounts combined high activity with low interaction quality and imbalanced engagement
- **Limitation:** the target labels were rule-based and the data is synthetic, so very high scores partly reflect how the labels were built. The next step would be to validate the model on real, verified labels.

## Files
- `Applied_Big_Data_Project_Report.pdf`: full report

## Team
Alaikhya Paleti, Asif Ahmed, Chandan Reddy Yellamula, Keelan Hartigan, Sathish Venkatesh, Vasumathi Gopalakrishnan

## Skills shown
Big data processing · Spark · Feature engineering · Classification · Fraud/anomaly detection · Python
