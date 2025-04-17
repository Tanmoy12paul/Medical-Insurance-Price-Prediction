# 🏥 Medical Insurance Price Predictor

This project predicts the **medical insurance cost** of an individual based on features such as age, gender, BMI, smoking habits, and region. It's built using supervised machine learning regression techniques including **Linear Regression**, **Random Forest**, and **XGBoost**. The dataset used is a popular open-source dataset often used in regression practice.

---

## 📌 Problem Statement

Given an individual's demographic and health information, predict the **charges** (medical insurance cost) they are likely to incur. This can be useful for:

- Insurance companies for policy pricing.
- Individuals to estimate their insurance needs.
- Healthcare consultants for cost predictions.

---

## 📊 Features Used

- `age`: Age of the individual
- `sex`: Gender (`male`, `female`)
- `bmi`: Body Mass Index
- `children`: Number of dependents
- `smoker`: Smoking habit (`yes`, `no`)
- `region`: Residential region
- Additional encoded features from `region`

---

## 🔧 Techniques Used

- Data Cleaning (handling outliers using Winsorization)
- Exploratory Data Analysis (EDA) with visualizations
- One-Hot Encoding for categorical variables
- Regression Models:
  - Linear Regression
  - Lasso Regression
  - Random Forest Regressor
  - XGBoost Regressor
- Model Evaluation using:
  - R² Score
  - Cross-validation
- Hyperparameter Tuning using GridSearchCV
- Model Serialization using Pickle

---

## 🧪 Model Evaluation

The models were evaluated using R² score and cross-validation. The best model was selected and saved using `pickle`.

---

## 💾 How to Use the Model (`.pkl` file)

You can load and use the saved model like this:

```python
# Import necessary libraries
import pickle

# Load the model
with open('insurancemodelf.pkl', 'rb') as file:
    model = pickle.load(file)

# Sample input data (must match training feature format)
sample_data = [[40, 1, 25.5, 2, 0, 0, 1, 0, 0]]  # age, sex, bmi, children, smoker, region_northwest, etc.

# Predict the insurance cost
prediction = model.predict(sample_data)
print("Predicted Insurance Charges:", prediction)
```

> ⚠️ Make sure your input feature order and encoding match what was used during training.

---

## 📁 How to Run

1. Clone the repository
2. Install required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
   ```
3. Open and run the `Medical_insurance_PricePredictor.ipynb` notebook
4. Modify or use the model from the saved `insurancemodelf.pkl`

---

## 📌 Author

- **Tanmoy** – Data Science Enthusiast from DIAT Pune
