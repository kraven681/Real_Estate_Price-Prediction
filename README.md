# 🏚️Real_Estate_Price-Prediction Machine Learning Project
## 📌 1. Introduction
This project aims to develop a predictive model to estimate housing prices based on various input features such as location, square footage, number of bathrooms, and BHK (bedrooms, hall, kitchen). The dataset appears to be sourced from a real estate platform in India, particularly focusing on properties in Bangalore.

The objectives of this project are:
- To clean and preprocess the raw dataset.

- To perform exploratory data analysis (EDA) and identify key trends.

- To build a machine learning model that predicts housing prices.

- To evaluate model performance and provide actionable insights.

## 📊 2. Data Analysis & Processing
## 🔹 Dataset Overview
The dataset contains the following key features:

- location

- total_sqft

- bath

- bhk

- price (in lakhs)

## 🔹 Key Data Cleaning Steps
- Removed outliers in price per square foot.

- Filtered out unrealistic BHK to bathroom ratios.

- Converted total_sqft from range strings (e.g., “2100 - 2850”) to float using the average.

- Removed locations with very few data points to avoid high variance noise.

## 🔹 Feature Engineering
- Created a new column price_per_sqft.

- Used one-hot encoding for the location feature after grouping rare locations into “other”.

- Final features used for modeling: total_sqft, bath, bhk, and location dummies.

## 📈 3. Exploratory Data Analysis (EDA)
## 🔹 Price per Square Foot Analysis
- Highly skewed across locations.

- Some locations showed very high or low price per sqft due to anomalies or outliers.

## 🔹 BHK vs Price Trend
- As expected, price generally increases with BHK.

-  However, price per sqft sometimes decreases with more BHKs due to larger areas being undervalued.

## 🔹 Location Impact
- Certain prime locations (e.g., Indira Nagar, Koramangala) command significantly higher prices.

- Some less-known or outer locations have low average prices, as seen in the boxplots.

## 🤖 4. Model Building
## 🔹 Algorithms Tested
- Linear Regression (Primary model)

- Lasso Regression (for regularization)

- Decision Tree Regressor

## 🔹 Model Selection via GridSearchCV
- Grid search was used to identify the best model among:

- Linear Regression

- Lasso (with varying alpha)

- Decision Tree (with max_depth tuning)

 ## 🔹 Best Model: Linear Regression
- Linear Regression outperformed others in terms of interpretability and cross-validation score.

## ✅ Model Evaluation
- R² Score: Good linear correlation between predicted and actual price.

- Prediction Accuracy: Reasonable for mid-range properties; some variance in premium locations.

## 🧠 5. Prediction Interface
A function predict_price(location, sqft, bath, bhk) was created that:

- Accepts user input.

- Transforms it using the same preprocessing steps.

- Uses the trained model to return a price prediction.

## ✅ 6. Key Insights
- Total_sqft and location are the most significant predictors of price.

- Properties with unrealistic sqft/BHK ratios are typically mispriced.

- Cleaning and grouping sparse locations drastically improved model performance.

## 📌 7. Recommendations
- Improve model accuracy using ensemble methods (e.g., Random Forest, XGBoost).

- Include additional features like year built, furnishing status, and amenities.

- Deploy the model using Flask/Django for user-friendly web access.

- Integrate real-time pricing data from property websites for continuous learning.

## 📎 8. File Attachment
- The original notebook (Real Estate Price Prediction.ipynb) contains:

- Complete code

- Visualizations

- Data preprocessing

- Model training and prediction

📁 [/content/Real_Estate.csv] /mnt/data/Real Estate Price Prediction.ipynb

## 🚀 Skills Applied
1.Data Cleaning & Feature Engineering

- Handled missing values, removed outliers, and transformed complex fields like total_sqft into usable numerical features. Created new variables such as price_per_sqft and grouped low-frequency locations to reduce model noise.

2.Exploratory Data Analysis (EDA)

- Used visualizations (scatter plots, histograms, boxplots) and statistical analysis to uncover patterns, outliers, and correlations between features like BHK, sqft, location, and price.

3.Machine Learning Model Development & Evaluation

- Implemented Linear Regression, Lasso, and Decision Tree models. Utilized GridSearchCV for hyperparameter tuning and selected the best-performing model based on accuracy and interpretability.

## 💡 What I Learned
Here are three short pointers on what you learned from the project:

1. **Importance of data cleaning** — Accurate predictions depend heavily on handling outliers and inconsistent entries.
2. **Location significantly impacts price** — One-hot encoding and grouping rare locations improved model performance.
3. **Model selection matters** — Linear Regression provided a balance of simplicity and performance compared to complex models.

## 📬 Contact

📧 Email:(mohdsamiali758@gmail.com)

🔗 LinkedIn:(www.linkedin.com/in/sami-ali-datascientist)
