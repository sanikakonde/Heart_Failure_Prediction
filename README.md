# 🫀 Heart Disease Prediction Using Machine Learning

##  About the Project

This project uses machine learning to predict whether a patient has heart disease or not based on patient health information.

I performed the complete machine learning workflow, starting from data exploration and preprocessing to model training, comparison, hyperparameter tuning, and final prediction.

##  Objective

The main objective of this project is to build a classification model that can predict:

- `0` → No Heart Disease
- `1` → Heart Disease

##  Dataset

The dataset contains **918 patient records and 12 columns**.

The main features include:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise Angina
- Oldpeak
- ST Slope
- Heart Disease

### Dataset Source

The dataset was taken from Kaggle:

[Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

##  Tools and Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Kaggle

##  Exploratory Data Analysis

I performed Exploratory Data Analysis (EDA) to understand the dataset.

The analysis includes:

- Target variable distribution
- Numerical feature distributions
- Boxplots for numerical features
- Categorical feature analysis
- Heart disease distribution by chest pain type
- Correlation heatmap

##  Data Preprocessing

The following preprocessing steps were performed:

- Separated features and target variable
- Split the data into training and testing sets
- Handled numerical and categorical features separately
- Used `StandardScaler` for numerical features
- Used `OneHotEncoder` for categorical features
- Created preprocessing pipelines using `Pipeline` and `ColumnTransformer`

## 🤖 Machine Learning Models

I compared the following classification algorithms:

1. Decision Tree
2. Random Forest
3. XGBoost

I used **5-Fold Cross-Validation** to compare their performance.

Random Forest performed the best among the initial models, so I selected it for further hyperparameter tuning.

## 🎯 Hyperparameter Tuning

I used `GridSearchCV` to find the best parameters for the Random Forest model.

The best configuration was:

- `n_estimators = 200`
- `max_depth = 10`
- `max_features = sqrt`
- `min_samples_split = 2`
- `min_samples_leaf = 1`

The best cross-validation accuracy was approximately **87.87%**.

## 📈 Final Model Performance

The tuned Random Forest model achieved approximately:

**89% accuracy on the test dataset.**

I also evaluated the model using:

- Precision
- Recall
- F1-score
- Confusion Matrix
- Accuracy

## 🔮 Prediction on New Data

After training and evaluating the final model, I tested it on a sample patient record.

The model predicted:

**Heart Disease Predicted**
