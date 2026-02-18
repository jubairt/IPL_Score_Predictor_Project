# 🏏 IPL Score Predictor

## 📌 Project Overview

IPL Score Predictor is a machine learning web application built using Streamlit.  
This project predicts the final score of a team in an ongoing IPL match using current match conditions.

The prediction is made after at least 5 overs are completed to ensure better accuracy and reliability.

This project demonstrates a complete end-to-end machine learning workflow including:

- Data cleaning  
- Feature selection  
- Exploratory data analysis  
- Model training  
- Model comparison  
- Model evaluation  
- Web deployment using Streamlit  

---

# 🎯 Objective

The goal of this project is to:

- Predict the final innings score in an IPL match  
- Use current match statistics as input  
- Apply multiple regression models  
- Compare model performances  
- Deploy the best-performing model as a web application  

---

# 📊 Dataset Information

The dataset used in this project contains ball-by-ball IPL match data from 2008 to 2020.

Each row in the dataset represents one ball in a match.

**Dataset File:** `ipl_data.csv`

---

## 📁 Features Description

Below are the columns present in the dataset:

- **mid** – Unique match ID  
- **date** – Date when the match was played  
- **venue** – Stadium where the match was played  
- **bat_team** – Batting team  
- **bowl_team** – Bowling team  
- **batsman** – Name of the batsman on strike  
- **bowler** – Name of the bowler  
- **runs** – Current total runs at that ball  
- **wickets** – Total wickets fallen till that ball  
- **overs** – Over number at that point  
- **runs_last_5** – Runs scored in the previous 5 overs  
- **wickets_last_5** – Wickets fallen in the previous 5 overs  
- **striker** – Current striker's personal score  
- **non-striker** – Non-striker's personal score  
- **total** – Final innings total (Target Variable)  

---

# 🧹 Data Preprocessing Steps

To improve model performance, the following preprocessing steps were applied:

### 1️⃣ Removed Irrelevant Columns

The following columns were dropped because they were not useful for prediction:

- mid  
- date  
- venue  
- batsman  
- bowler  
- striker  
- non-striker  

### 2️⃣ Selected Consistent Teams

Only the 8 main IPL teams were retained to avoid inconsistency and imbalance in the dataset.

### 3️⃣ Removed Early Overs

All records before 5 overs were removed because early innings data is unstable and leads to unreliable predictions.

### 4️⃣ Categorical Encoding

The categorical columns `bat_team` and `bowl_team` were converted using One-Hot Encoding so that machine learning models can understand them.

---

# 📈 Exploratory Data Analysis (EDA)

Several visualizations were created to understand the dataset better:

- Wickets Distribution  
- Final Score Distribution  
- Correlation Heatmap  

### Key Observations:

- Most IPL scores lie between 140–190 runs.  
- Runs scored in the last 5 overs have strong correlation with final score.  
- Wickets have a negative correlation with total score.  
- Momentum plays an important role in final score prediction.  

---

# 🤖 Machine Learning Models Used

The following regression algorithms were trained and evaluated:

- Linear Regression  
- K-Nearest Neighbor Regressor  
- Support Vector Regressor (SVR)  
- Decision Tree Regressor  
- Random Forest Regressor  
- XGBoost Regressor  

---

# 📊 Model Performance

**Decision Tree**  
Train Score: 99.98%  
Test Score: 86.29%  

**Random Forest**  
Train Score: 99.04%  
Test Score: 93.07%  

**XGBoost**  
Train Score: 88.71%  
Test Score: 84.84%  

### ✅ Best Model: Random Forest Regressor

Random Forest was selected as the final model because:

- It achieved the highest test accuracy  
- It generalizes well  
- It reduces overfitting compared to Decision Tree  

---

# 🌐 Streamlit Web Application

The trained model was deployed using Streamlit.

The web application allows users to:

- Select the batting team  
- Select the bowling team  
- Enter current overs  
- Enter current runs  
- Enter wickets fallen  
- Enter runs scored in the last 5 overs  
- Enter wickets fallen in the last 5 overs  

The app then predicts the final score range.

---

## ✅ Input Validation

The application includes validation checks:

- Minimum overs must be greater than 5  
- Over format must be valid (6 balls per over)  
- Batting and bowling teams must be different  
- Logical constraints on runs and wickets  

---

# 🖥️ Streamlit App Screenshot

_Add your Streamlit app screenshot below:_


---

# 🚀 Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  
- Streamlit  

---

# 🎓 Learning Outcomes

Through this project, the following concepts were applied:

- Data preprocessing  
- Feature engineering  
- Regression modeling  
- Model evaluation  
- Model comparison  
- Web app deployment  
- Input validation logic  

---

# 📌 Conclusion

This project successfully demonstrates an end-to-end machine learning pipeline for sports analytics.

The model effectively predicts IPL scores using match context and momentum-based features.

Random Forest achieved the best performance with strong generalization ability.
