#  Wine Quality Prediction

## **Overview**

This project focuses on predicting the **quality of wine** based on its chemical properties using machine learning. By analyzing attributes like **alcohol content, acidity, density, and sulphates**, the project builds models to estimate wine quality ratings.

The objective is to provide practical insights for **winemakers** and demonstrate **end-to-end machine learning skills**, including data preprocessing, visualization, model training, evaluation, and deployment.


## **Dataset**

* **File:** `WineQT.csv`
* **Path:** `C:\Users\as\Desktop\OIBSIP\Oasis_Infobyte_Project_5_Wine_Prediction\WineQT.csv`
* **Features:** Fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol
* **Target:** Quality (numerical ratings)
* **Source:** [Kaggle Wine Quality Dataset](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)


## **Steps Covered**

1. **Data Collection**

   * Loaded dataset with chemical properties and quality ratings.

2. **Data Exploration & Cleaning**

   * Checked for missing values, data types, and summary statistics.
   * Verified dataset is clean and ready for modeling.

3. **Exploratory Data Analysis (EDA)**

   * Visualized distribution of wine quality ratings.
   * Explored relationships between features and quality using boxplots and correlation heatmaps.

4. **Data Preprocessing**

   * Split features (`X`) and target (`y`).
   * Performed train-test split (80%-20%).
   * Applied **StandardScaler** for models sensitive to feature magnitude (SVC, SGD).

5. **Model Building**

   * Linear Regression for continuous quality prediction.
   * Random Forest Classifier, Support Vector Classifier (SVC), and Stochastic Gradient Descent (SGD) Classifier for categorical prediction.

6. **Model Evaluation**

   * Used metrics: **R², MSE** for regression; **accuracy, precision, recall, F1-score** for classification.
   * Compared models using a bar chart.

7. **Model Interpretation**

   * Identified important features influencing quality (alcohol, volatile acidity, density).
   * Analyzed chemical patterns correlating with high-quality wines.

8. **Model Saving & Deployment**

   * Saved the best-performing Random Forest model using `joblib` for future predictions.

## **Key Findings**

* **Random Forest Classifier** achieved the highest accuracy for predicting wine quality.
* **Linear Regression** captures the overall trend but is less precise for exact quality labels.
* **Important features:** Alcohol content, volatile acidity, sulphates, and density strongly influence wine quality.
* Higher alcohol and balanced acidity generally correspond to better-quality wines.

## **Libraries Used**

* **Data Handling:** Pandas, Numpy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (LinearRegression, RandomForestClassifier, SVC, SGDClassifier)
* **Model Persistence:** Joblib

## **Visualizations**

* Distribution of wine quality ratings
* Correlation heatmap of features
* Boxplots for feature vs quality
* Model performance comparison bar chart

## **Conclusion & Recommendations**

* Random Forest is the most effective model for predicting wine quality.
* The chemical composition of wine significantly impacts quality ratings.
* Winemakers can use this model to predict wine quality early, optimizing production and reducing costs.
* Future improvements: Hyperparameter tuning, cross-validation, and testing ensemble models like **XGBoost**.

## **How to Use**

1. Clone the repository.
2. Place `WineQT.csv` in the specified path.
3. Run the Jupyter Notebook to train models and visualize results.
4. Use the saved model (`wine_quality_rf_model.pkl`) for predicting new wine samples.