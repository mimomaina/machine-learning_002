# Second-Hand Car Price Prediction

A machine learning project to predict the prices of second-hand cars based on their features.

---

## 📝 Overview

This project uses Python and several libraries (`pandas`, `scikit-learn`) to perform exploratory data analysis, preprocessing, and modeling of car pricing data. The training pipeline includes:

- Data cleaning and handling missing values
- Feature encoding (one-hot, ordinal)
- Feature selection and importance analysis
- Dimensionality reduction using Principal Component Analysis (PCA)
- Model training with Random Forest and Gradient Boosting Regressors
- Hyperparameter tuning

---

## 🛠️ Features Used

All features are extracted from the `second_hand_cars.csv` dataset, including:
- **Company Name**, **Car Name**, **Variant**
- **Fuel Type**, **Tyre Condition**
- **Make Year**, **Mileage**, **Price per Mile**
- **Car Age**, **Registration Number**
- **Owner Type**, **Insurance**, **Registration Certificate**
- **Accessories**, **Body Color**

These features were encoded, scaled, and transformed to train predictive models.

---

## 📁 Dataset

The dataset used is available as `second_hand_cars.csv`.

It contains information about:
- Car specifications
- Pricing data
- Owner history
- Physical conditions
- Accessories and other categorical attributes

---

## 🧪 Models Evaluated

1. **Random Forest Regressor**: Assesses feature importance and provides strong baseline predictions.
2. **Gradient Boosting Regressor**: Further improves prediction accuracy by boosting weak learners.

---

## ⚙️ Technologies

- Python 3
- **pandas** - For data manipulation
- **numpy** - For numerical operations
- **scikit-learn** (`RandomForestRegressor`, `GradientBoostingRegressor`, `StandardScaler`, `PCA`)
- **matplotlib/seaborn** - For visualizations
- Google Colab (execution environment)

---

## 🔍 Highlights

- Cleaned and preprocessed data, including handling missing values and transforming categorical variables.
- Extracted important features through visualization and ranking.
- Reduced dimensionality using PCA to improve computation time and avoid overfitting.
- Evaluated multiple regressors for performance.
- Performed hyperparameter tuning to optimize model performance.

---

## 🧾 Output Example: Feature Importance

| Feature | Importance Score |
|--------|----------------|
| Fuel Type_Petrol | 0.0957 |
| Fuel Type_Diesel | 0.0869 |
| Transmission Type_Automatic | 0.0767 |
| Transmission Type_Manual | 0.0756 |

---

## 📋 Results: Evaluation Metrics

Example results for the models:
- **Gradient Boosting**: MAE = 0.8913, MSE = 1.0391

---

## 📦 Project Structure
