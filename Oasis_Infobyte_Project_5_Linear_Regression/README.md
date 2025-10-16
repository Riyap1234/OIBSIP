#  Housing Price Prediction — Linear Regression

## Overview

This project predicts house prices using a **Linear Regression** model with Ridge and Lasso regularization. It includes **data preprocessing**, **exploratory data analysis (EDA)** with multiple visualizations, **model training and evaluation**, and **interpretation of results**.

The project is **intermediate-level**, making it suitable for interview discussions and practical applications.


## Dataset

* **File:** `Housing.csv`
* **Path:** `C:\Users\as\Desktop\OIBSIP\Oasis_Infobyte_Project_5_Linear_Regression\Housing.csv`
* The dataset includes **numerical and categorical features** affecting house prices.


## Steps Included

1. **Data Loading**

   * Loaded dataset and inspected basic info and descriptive statistics.

2. **Exploratory Data Analysis (EDA)**

   * Checked missing values.
   * Visualized distributions of numerical features (histograms).
   * Visualized relationships between features and target using **correlation heatmaps, pairplots, and boxplots**.
   * Examined categorical features with countplots and boxplots.

3. **Data Preprocessing**

   * Handled missing values and encoded categorical variables using **pipelines**.
   * Standardized numerical features.

4. **Train-Test Split**

   * Split dataset into training and testing sets (80-20 split).

5. **Model Training**

   * Trained **Linear Regression** baseline model.
   * Applied **Ridge and Lasso regression** with GridSearchCV for hyperparameter tuning.

6. **Model Evaluation**

   * Evaluated models using **RMSE, MAE, and R²** metrics.
   * Plotted predicted vs actual values and residuals.

7. **Feature Importance**

   * Extracted top features affecting house price from model coefficients.

8. **Model Saving & Loading**

   * Saved the trained pipeline (`linear_reg_model.pkl`) for deployment.
   * Demonstrated predictions using the saved model.

9. **Visualization**

   * All steps are accompanied by charts and plots to illustrate data patterns and model performance.


## Recommendations & Conclusion

1. The model performs well in predicting housing prices using available features.
2. **Most impactful features:** Area, number of bedrooms/bathrooms, parking, and location.
3. **Improvements for future work:**

   * Include additional features like house age, amenities, or location-specific data.
   * Explore non-linear models (Random Forest, XGBoost) for higher accuracy.
   * Apply log transformations to skewed features or target for better regression performance.
4. **Regularization** (Ridge/Lasso) helps reduce overfitting and improve generalization.
5. The model pipeline is **ready for inference** and can be deployed for basic price prediction tasks.
6. Overall, the project demonstrates **data cleaning, visualization, feature engineering, regression modeling, hyperparameter tuning, and interpretation**—skills relevant for real-world applications and interviews.


## Tools & Libraries Used

* Python 3.x
* pandas, numpy
* matplotlib, seaborn
* scikit-learn
* joblib
* scipy


## How to Run

1. Place `Housing.csv` in the root project folder.
2. Open `notebook.ipynb` in Jupyter or VS Code.
3. Run cells sequentially to reproduce EDA, model training, evaluation, and visualizations.
4. The trained model will be saved in the `models/` folder as `linear_reg_model.pkl`.
5. You can load the saved model for predictions on new data.
