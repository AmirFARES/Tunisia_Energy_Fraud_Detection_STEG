# Tunisia Energy Fraud Detection STEG

![Project Image](https://github.com/AmirFARES/Tunisia_Energy_Fraud_Detection_STEG/blob/main/imgs/energy_fraud_logo.png)

## Introduction 🌟

Tackle electricity and gas fraud in Tunisia 🇹🇳 using data-driven insights. Achieved top 25% in the leaderboard with an XGBoost model boasting an AUC of 0.86.

## Key Objectives 🎯

Detect and prevent fraudulent activities in electricity and gas consumption to enhance revenue and reduce losses.

## Data Sources 📊

All data is provided by the Tunisian Company of Electricity and Gas (STEG). You can access the data at [**Zindi data section**](https://zindi.africa/competitions/fraud-detection-in-electricity-and-gas-consumption-challenge/data).



## Methodology 🚀

Approach:

- Exploratory Data Analysis (EDA) on client and invoice data.
- Correlation analysis, feature engineering, and aggregation to improve model performance.
- Utilized an XGBoost classifier with tuning for optimal AUC.

## Data Preprocessing 🛠️

- Checked for NaN values.
- Transformed data types.
- And applied label and one-hot encoding to categorical columns.


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
```

## Training and Evaluation 📈

- **Optimization:** XGBoost's boosting process corrects errors of the combined ensemble.
- **Loss Function:** Binary logistic.
- **Epochs and Early Stopping:** Utilized 4000 estimators without early stopping for the final model.
- **Evaluation Metrics:** Focused on AUC, f1 score, and other relevant metrics.

## Conclusion 🎯

**Key Findings:**
- Identified significant features, including the number of counters used, counter state, counter coefficient, tarif type, and reading remarque.
- Achieved a top-performing model with an AUC of 0.8641.

## Future Work 🚧

- Fine-tune the model for better performance.
- Explore anomaly detection approaches.
- Experiment with more robust anomaly detection models.
- Address misclassified labels for improved accuracy.


## Connect with Me 📫

Feel free to reach out for any project-related inquiries, collaboration opportunities, or discussions. You can connect with me on [LinkedIn](https://www.linkedin.com/in/amir-f), explore more of my projects on [GitHub](https://github.com/AmirFARES), and check out my portfolio [here](https://amirfares.github.io/).

## Acknowledgments 🙏

I'd like to express my gratitude to Zindi the organizers of this challenge.

Thank you for visiting my project repository, and I'm excited to share more data-driven insights in the future!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/amir-f)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-orange)](https://amirfares.github.io/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-green)](https://github.com/AmirFARES)
