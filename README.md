# 🏠 Tehran House Price Prediction

This project builds and compares machine learning models (Random Forest and XGBoost) to predict apartment prices in Tehran using real-world property data.

## 📌 Project Features

- 📊 Data Cleaning and Exploratory Data Analysis (EDA)
- 🤖 Model Training with Random Forest & XGBoost
- 🔍 Hyperparameter Tuning using RandomizedSearchCV
- 📈 Explainability using SHAP and LIME
- 📂 Structured output folders for each run and each model

## 🚀 How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Run the main pipeline
python tehran_house_price_prediction.py
```

Each model will create a timestamped subfolder inside its own results directory:

```
results/
├── RandomForest/
│   └── run_YYYYMMDD_HHMM/
│       ├── results/
│       ├── shap/
│       └── lime/
└── XGBoost/
    └── run_YYYYMMDD_HHMM/
        ├── results/
        ├── shap/
        └── lime/
```

## 📊 Model Comparison Summary

| Metric | Random Forest | XGBoost |
|--------|----------------|---------|
| MAE    | 69,562.11      | 67,749.23 |
| RMSE   | 134,415.28     | 134,490.31 |
| R²     | 0.7315         | 0.7312 |

## 🔧 Best Hyperparameters Summary

<details>
<summary>Click to expand</summary>

**Random Forest**
```json
{
  "max_depth": 9,
  "max_features": "log2",
  "min_samples_leaf": 1,
  "min_samples_split": 2,
  "n_estimators": 476
}
```

**XGBoost**
```json
{
  "colsample_bytree": 1.0,
  "gamma": 0.2,
  "learning_rate": 0.01,
  "max_depth": 6,
  "n_estimators": 724,
  "reg_alpha": 0.1,
  "reg_lambda": 2.0,
  "subsample": 1.0
}
```

</details>

---

## 📎 Notes

- You can modify the dataset by replacing `Dataset/housePrice.csv`.
- The script is optimized for reproducibility and separate model logging.

## 📄 License

The original source code and original project materials in this repository are licensed under the [PolyForm Noncommercial License 1.0.0](LICENSE).

You may use, modify, and redistribute them only for noncommercial purposes. Commercial use, selling the project, charging for access, or using it as part of a paid product or service is not permitted.

**Required attribution:** Copyright © Soroush Mohammadi Samani (smSamani). This attribution must remain with every copy, modified version, and redistribution.

Third-party dependencies, datasets, APIs, trademarks, and other materials remain subject to their own licenses and terms.
