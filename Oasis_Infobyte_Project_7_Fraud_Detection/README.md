#  Fraud Detection Using Machine Learning

## **Overview**

Fraud detection involves identifying and preventing deceptive activities in financial transactions. In this project, we build a machine learning system to detect fraudulent credit card transactions using the **Credit Card Fraud Detection Dataset** from Kaggle.

Key objectives:

* Detect anomalies in transaction data.
* Build predictive models to classify transactions as legitimate or fraudulent.
* Analyze feature importance to understand contributing factors.

**Dataset:** [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)


## **Key Concepts and Challenges**

1. **Anomaly Detection** – Identifying unusual patterns that indicate fraud.
2. **Imbalanced Dataset** – Only ~0.17% of transactions are fraudulent, requiring special handling.
3. **Feature Engineering** – Scaling and transforming `Amount` and `Time` for better model performance.
4. **Machine Learning Models** – Logistic Regression, Random Forest Classifier.
5. **Model Evaluation** – Accuracy, Precision, Recall, F1-score, ROC-AUC.
6. **Scalability & Real-Time Monitoring** – System design considerations for large transaction volumes.


## **Steps Covered**

1. **Project Initialization** – Defined objectives and dataset.
2. **Data Loading** – Loaded `creditcard.csv` and inspected the dataset.
3. **Exploratory Data Analysis (EDA)** – Checked class distribution and visualized features.
4. **Data Preprocessing** – Scaled `Amount` and `Time`; split data into train-test sets.
5. **Handling Imbalanced Dataset** – Used class balancing in models.
6. **Model Building** – Trained Logistic Regression and Random Forest models.
7. **Model Evaluation** – Evaluated with classification reports, confusion matrices, and ROC-AUC.
8. **Feature Importance Analysis** – Identified top features influencing fraud detection.
9. **Conclusion & Insights** – Summarized findings and model performance.
10. **Recommendations** – Provided deployment and monitoring strategies.
11. **Model Saving** – Saved the trained Random Forest model for future use.


## **Learning Objectives**

* Practical experience with **data preprocessing and feature scaling**.
* Understanding of **machine learning concepts** and handling **imbalanced datasets**.
* Experience in **model evaluation, interpretation, and feature importance analysis**.
* Insights into deploying models for **fraud detection systems**.


## **Tools & Libraries Used**

* **Python**
* **Pandas, NumPy** – Data manipulation
* **Matplotlib, Seaborn** – Data visualization
* **Scikit-learn** – Machine learning models and evaluation
* **Joblib** – Model saving and deployment


## **Project Outcome**

* Random Forest outperformed Logistic Regression for fraud detection.
* ROC-AUC score close to 1 indicates strong model performance.
* Feature analysis revealed the most significant indicators of fraud.
* The project demonstrates end-to-end workflow: **EDA → Preprocessing → Model Building → Evaluation → Insights → Deployment**.


## **Future Work / Recommendations**

* Implement **real-time fraud detection** system.
* Experiment with **XGBoost or Neural Networks** for higher performance.
* Continuously retrain the model with **new transaction data**.
* Explore **ensemble methods** for better recall-precision tradeoff.