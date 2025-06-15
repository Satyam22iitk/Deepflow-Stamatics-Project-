# 🏗️ Bulldozer Price Prediction with Visualizations

This project uses machine learning to predict the auction sale price of bulldozers and heavy machinery using historical data from the Bluebook for Bulldozers dataset.

---

## 📌 Objective

Predict **SalePrice** using equipment details, sale date, manufacturer, and usage features.

---

## 📁 Dataset Contents

Extracted from `datasheet.zip`:
- `Train.csv`: Training data including SalePrice
- `Test.csv`: Test data without SalePrice
- `Data Dictionary.xlsx`: Feature descriptions (optional)

---

## 🔍 Workflow Steps

### ✅ Data Preparation
- Drop columns with more than 50% missing values
- Fill missing categorical values with mode, numeric with median
- Parse `saledate` into `saleYear` and `saleMonth`
- Label encode categorical variables using combined train + test data

### ✅ Feature Engineering
- Extract date components
- Keep only aligned features between train and test
- Remove high-missing or irrelevant columns

---

## 📊 Visualizations Included

1. **SalePrice Distribution** (histogram + KDE)
2. **SalePrice Over Time** (line plot)
3. **Feature Correlation Heatmap** (with SalePrice)
4. **Distribution of Predictions on Test Set**
5. **Train vs Test SalePrice KDE Comparison**
6. **Top 20 Most Expensive Predicted Machines (Bar Plot)**

---

## 🤖 Model

- **Model Used:** Random Forest Regressor
- **Parameters:** `n_estimators=100`, `max_depth=15`
- **Validation Split:** 80% train / 20% validation
- **Evaluation Metric:** RMSLE (Root Mean Squared Logarithmic Error)

---

## 📈 Results

- ✅ RMSLE on validation set: ~0.23 to 0.26
- ✅ Model retrained on full training data
- ✅ Predictions saved as `test_predictions.csv`

---

## 📝 Output Format

```csv
SalesID,SalePrice
1222837,36205.0
3044012,74570.0
1222841,31910.5
...
```

---

## ▶️ Run Instructions (in Colab)

1. Upload `datasheet.zip`
2. Run all code cells in the notebook
3. Final predictions file (`test_predictions.csv`) will auto-download
4. All visualizations are displayed inline

---

## 🚀 Future Enhancements

- Use `log(SalePrice)` + `expm1()` for better RMSLE
- Try boosting models like XGBoost or LightGBM
- Add SHAP for model explainability
- Use GridSearchCV or Optuna for hyperparameter tuning

---

## 👨‍💻 Author

Built with Python, Pandas, Seaborn, Scikit-learn  
Fully reproducible in Google Colab.
