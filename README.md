# Tunisia Energy Fraud Detection STEG

![Project Image](https://github.com/AmirFARES/Tunisia_Energy_Fraud_Detection_STEG/blob/main/imgs/energy_fraud_logo.png)

## Introduction 🌟

Tackle electricity and gas fraud in Tunisia using data-driven insights. Achieved top 25% in the leaderboard with an XGBoost model boasting an AUC of 0.86.

## Key Objectives 🎯

Detect and prevent fraudulent activities in electricity and gas consumption to enhance revenue and reduce losses.

## Data Sources 📊

All data is provided by the Tunisian Company of Electricity and Gas (STEG). You can access the training and test data from [**train.zip**](link) and [**test.zip**](link), respectively. For further details, refer to [**SampleSubmission.csv**](link).

## Methodology 🚀

Approach:

- Exploratory Data Analysis (EDA) on client and invoice data.
- Correlation analysis, feature engineering, and aggregation to improve model performance.
- Utilized an XGBoost classifier with tuning for optimal AUC.

## Data Preprocessing 🛠️

*Provide insights into how the data was cleaned, handled missing values, and any transformations performed.*

## Model Architecture 🏗️

```python
model = XGBClassifier(
    n_estimators=4000,
    learning_rate=0.01,
    max_depth=3,
    objective='binary:logistic',
    random_state=42,
    scale_pos_weight=sum(y_train == 0) / sum(y_train == 1),
    gamma=0.1,
    reg_lambda=1,
    reg_alpha=0,
)
