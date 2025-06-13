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

| Model         | MAE       | RMSE      | R² Score |
|---------------|-----------|-----------|----------|
| Random Forest | [filled by script] | [filled by script] | [filled by script] |
| XGBoost       | [filled by script] | [filled by script] | [filled by script] |

---

## 📎 Notes

- You can modify the dataset by replacing `Dataset/housePrice.csv`.
- The script is optimized for reproducibility and separate model logging.
