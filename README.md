# Analyzing Car CO₂ Emissions

Overview! 
This repository contains a project I worked on to explore and model CO₂ emissions from cars using multiple regression techniques. The idea was to understand what factors—especially fuel type and city mileage—affect emissions and then use that model to predict emissions for a set of shortlisted car models.

---

## 📌 Objective
The main goal of this project was to build a **multiple linear regression model** that predicts CO₂ emissions based on real-world car data. Initially, I started with a simple model using just city mileage, but later extended it by including categorical variables like fuel type to improve prediction accuracy.

---

##  What I Did

Here’s the steps I followed in the project:
### 1. **Data Exploration**
I started by examining the dataset, checking for missing values, data types and overall distribution of emissions. This helped me decide on the right features to include in the model.

### 2. **Simple Linear Regression**
To build a baseline, I first created a model using just the "City" mileage as a predictor. It performed decently but I suspected that fuel type might play an important role too.

### 3. **Encoding Categorical Variables**
"Fuel type" is a categorical feature, so I used one-hot encoding to convert it into numeric dummy variables using `pandas.get_dummies()`. I also dropped the first dummy to avoid multicollinearity (the dummy variable trap).

### 4. **Multiple Linear Regression**
Then came the real part, building the multiple linear regression model using both `City` and `Fuel type`. I added a constant to the predictors using `statsmodels` and trained the model. The `summary()` output gave a lot of insight into the model’s performance and the significance of each variable.

### 5. **Prediction on New Data**
Finally, I tested the model by predicting CO₂ emissions for four new car models from a separate test dataset. I made sure to align the test features with the training data format and used the trained model to make the predictions.

---

## 📂 Files

- `Analyzing Car CO₂ Emissions.ipynb`: The Jupyter notebook containing all the steps from exploration to prediction.
- `test_cars.csv`: A sample test dataset used for the final predictions.

---

## 📈 Libraries Used
- `pandas` for data manipulation
- `numpy` for numerical operations
- `statsmodels` for regression modeling and summaries

---

## 💡 What I Learned

- How to handle categorical variables in regression
- Interpreting statistical outputs from `statsmodels`
- Making predictions with a trained model on unseen data

---

## ✅ Future Improvements

- Add more predictors like "Engine size" or "Highway mileage" to improve the model.
- Evaluate model performance using cross-validation.

---

## 🙋‍♂️ Author

**Created by:** Sagar Shahari  
*Always happy to connect and discuss data projects or improvements!*

---

Thanks for checking this out! If you have any suggestions or feedback, feel free to drop them in. 😊
