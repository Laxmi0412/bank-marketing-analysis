Exploratory data analysis, feature engineering, clustering, and classification on the UCI Bank Marketing Dataset to predict whether a client will subscribe to a term deposit.

📁 Dataset Overview
FieldDetailsSourceUCI Machine Learning RepositoryRecords~45,211Features17 columnsTargety — Has the client subscribed to a term deposit? (yes/no)Key FieldsAge, job, marital status, education, balance, campaign calls, previous outcome

🛠️ Methods
1. Exploratory Data Analysis (EDA)

Descriptive statistics for all numeric and categorical features
Correlation heatmap across numeric columns
Distribution plots for age, balance, and campaign contacts
Class balance check on target variable (yes vs no)
Bar charts for categorical features (job, education, marital status)

2. Feature Engineering

Encoding categorical variables (Label Encoding / One-Hot Encoding)
Handling missing/unknown values
Outlier detection and treatment for balance and duration
New derived features (e.g., contact frequency, previous campaign outcome flag)

3. K-Means Clustering
Applied K-Means unsupervised clustering to segment clients based on financial and demographic features.

Features standardized with StandardScaler
Optimal k selected using the Elbow Method
Cluster profiles analyzed against subscription rate

4. Classification (Predict Subscription)
Predicting whether a client will subscribe to a term deposit (y = yes/no).

Train/test split (80/20)
Models to evaluate: Logistic Regression, Decision Tree, Random Forest
Evaluation metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC
Handle class imbalance with SMOTE or class weighting


📊 Key Visualizations

Subscription Rate by Job Type
Age & Balance Distribution
Correlation Heatmap
Campaign Contacts vs Subscription Outcome
K-Means Cluster Profiles
ROC Curve (Classification)
Confusion Matrix


🚀 Getting Started
Prerequisites
bashpip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
Load the Dataset
pythonimport pandas as pd

url = "https://archive.ics.uci.edu/ml/machine-learning-databases/00222/bank.zip"
df = pd.read_csv("bank-full.csv", sep=";")
df.head()

📦 Dependencies
LibraryPurposepandasData loading & manipulationnumpyNumerical operationsmatplotlibPlottingseabornStatistical visualizationsscikit-learnClustering & classification modelsimbalanced-learnHandle class imbalance (SMOTE)

📌 Notes

The dataset is imbalanced (~88% No, ~12% Yes) — use appropriate metrics beyond accuracy
duration (last contact duration) strongly predicts outcome but is unknown before the call — consider dropping for realistic modeling
unknown values appear in job, education, and contact — handle carefully during preprocessing


📄 License
Data is publicly available via the UCI Machine Learning Repositor
