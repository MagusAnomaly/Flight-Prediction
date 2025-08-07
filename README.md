# ✈️ Flight Price Prediction

This repository contains a machine learning project that predicts airline flight ticket prices using various regression algorithms and feature engineering techniques.

DataSet Source - Machine Hack

## 📁 Project Overview

This project applies several ensemble and tree-based regressors to predict flight ticket prices. The pipeline includes preprocessing steps, training multiple models, hyperparameter tuning, and evaluation using root mean squared error.

## 📊 Dataset & Features

- **Features:** Includes airline, source, destination, total stops, duration, and days left before travel.
- **Feature Processing:**
  - Categorical encoding via LabelEncoder
  - Feature scaling for numerical inputs
  - Feature segregation: numerical vs categorical

> Note: The dataset source isn't included in this notebook. Add data references or links if available.

## Machine Learning Models

Total of **7 regression models** trained:

- RandomForestRegressor
- GradientBoostingRegressor
- AdaBoostRegressor
- ExtraTreesRegressor
- DecisionTreeRegressor
- XGBRegressor
- LGBMRegressor

## 🛠️ Model Tuning

- GridSearchCV used for hyperparameter optimization  
- Evaluation based on RMSE (Root Mean Squared Error)

## 🧪 Model Evaluation Results

### 📉 Validation RMSE (Before Tuning)
| Model           | RMSE   |
|-----------------|--------|
| Random Forest   | 31.78  |
| Decision Tree   | 42.38  |
| Extra Trees     | 32.58  |

### 🛠️ After Hyperparameter Tuning
| Model           | Tuned RMSE | Best Parameters |
|-----------------|------------|-----------------|
| Random Forest   | **30.92**  | `{'max_depth': 10, 'n_estimators': 300, 'random_state': 42}` |
| Decision Tree   | 34.13      | `{'max_depth': 10, 'random_state': 42}` |
| Extra Trees     | 32.45      | `{'n_estimators': 200, 'random_state': 42}` |

### 🔁 Ensemble Averaged Model
- **Ensemble Model RMSE:** `31.46`

## 📈 Libraries Used

- pandas, numpy  
- scikit-learn  
- xgboost  
- lightgbm  
- seaborn, matplotlib  

## 📌 Recommendations

- Add data visualizations like correlation matrix, distributions, and boxplots  
- Store the best-performing model as a `.pkl` file for deployment  
- Include a performance comparison table with RMSE scores  
