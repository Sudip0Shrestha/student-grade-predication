# 🎓 Student Performance Prediction (Machine Learning Project)

## 📌 Project Overview

This project predicts students' **FinalGrade** using Machine Learning.

The model is built using:
- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib

A preprocessing pipeline is used before training a Linear Regression model.

---

## 📂 Dataset Information

The dataset contains:
- Gender
- AttendanceRate
- StudyHoursPerWeek
- PreviousGrade
- ExtracurricularActivities
- ParentalSupport
- Study Hours
- Attendance (%)
- Online Classes Taken
- FinalGrade (Target)

Dropped columns:
- Name
- StudentID

---

## 🧹 Data Cleaning & Preprocessing

### Handling Missing Values

- Numerical columns → Filled with median
- Gender → Filled manually (Male/Female alternating)
- Online Classes Taken → Filled manually (True/False alternating)
- ParentalSupport → Filled using repeating values (High/Medium/Low)

### Feature Scaling

- Numerical features → StandardScaler
- Categorical features → OrdinalEncoder

Implemented using:
- Pipeline
- ColumnTransformer

---

## 🔀 Train-Test Split

Used:
StratifiedShuffleSplit

- Test size: 20%
- Stratified based on: ParentalSupport

---

## 🤖 Model

Model Used:
LinearRegression

If model.pkl does not exist:
- Train model
- Save model.pkl
- Save pipeline.pkl

If model exists:
- Load model
- Perform inference
- Save predictions to output.csv

---

## 📊 Model Performance

Inference Results:

MAE (Mean Absolute Error): 8.1177  
MSE (Mean Squared Error): 90.8045  

---

## 📁 Project Structure

student.csv  
input.csv  
output.csv  
model.pkl  
pipeline.pkl  
Grade_pred.ipynb.py  
README.md  

---

## 🚀 How To Run

### 1. Install Dependencies

pip install pandas numpy scikit-learn joblib

### 2. Run the Script

 Grade_pred.ipynb

First run → Trains model  
Next runs → Performs inference  

---

## 🔮 Future Improvements

- Try Random Forest or XGBoost
- Apply OneHotEncoding instead of OrdinalEncoder
- Remove outliers (Attendance > 100%)
- Add Cross Validation
- Hyperparameter tuning
- Deploy as Web App

---

## 👨‍💻 Author

Linked in: https://www.linkedin.com/in/sudip-shrestha-532622372/
