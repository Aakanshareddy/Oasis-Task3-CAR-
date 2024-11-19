# Oasis-Task3-CAR-

# Car Price Prediction with Machine Learning

This project aims to predict the selling price of cars using machine learning techniques. Below is an overview of the process, key steps, and results.

## **Objective**
To build a machine learning model that predicts car prices based on various features like year of manufacture, present price, kilometers driven, fuel type, and more.

---

## **Dataset Overview**
The dataset consists of 301 entries and 9 columns:
- **Features**:
  - `Year`: Manufacturing year of the car.
  - `Present_Price`: Current market price of the car (in lakhs).
  - `Driven_kms`: Total kilometers the car has been driven.
  - `Fuel_Type`: Type of fuel (Petrol/Diesel/CNG).
  - `Selling_type`: Dealer or Individual.
  - `Transmission`: Manual or Automatic.
  - `Owner`: Number of previous owners.
- **Target**: `Selling_Price` (price of the car when sold).

---

## **Steps and Implementation**

### **1. Libraries Used**
- `pandas`, `numpy`: For data manipulation and preprocessing.
- `matplotlib`, `seaborn`: For data visualization.
- `sklearn`: For model building and evaluation.

---

### **2. Data Preprocessing**
- **Missing Values**: No missing values in the dataset.
- **Categorical Encoding**: Used `pd.get_dummies` to encode categorical columns, adding 97 new columns.
- **Feature Scaling**: Applied `StandardScaler` to scale features for better model performance.

---

### **3. Data Visualization**
- Pairplots were generated to explore relationships between features and target variables.
- Boxplots were used to inspect the scaled features.

---

### **4. Model Building**
- **Split Data**: 
  - 80% training, 20% testing.
- **Model**: Linear Regression.
  - Scaled features using `StandardScaler`.
  - Fit the model on training data.

---

### **5. Model Evaluation**
- **Metrics Used**:
  - **Mean Squared Error (MSE)**:
    - Train: `1.336`
    - Test: `1.395e+25` (very high, indicating overfitting or data issue).
  - **R² Score**:
    - Train: `0.949` (excellent fit on training data).
    - Test: `-6.056e+23` (negative, indicating poor generalization).

---

## **Key Observations**
1. **Overfitting Issue**: 
   - The model performed well on the training data but failed to generalize on the test data.
   - This suggests possible multicollinearity, overfitting, or data leakage.

2. **Feature Engineering Needed**:
   - Reducing dimensionality or selecting key features might improve results.

---

## **Next Steps**
1. Analyze and remove highly correlated or less impactful features.
2. Experiment with other regression algorithms (Ridge, Lasso, Decision Trees).
3. Perform hyperparameter tuning to improve model performance.
4. Investigate anomalies in data and address potential outliers.
