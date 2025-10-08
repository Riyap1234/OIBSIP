# 🛍️ Customer Segmentation Analysis

## Overview

This project is part of my **Oasis Infobyte internship (OIBSIP Project 2)**.
The objective is to perform **customer segmentation analysis** for an e-commerce company using the **iFood marketing dataset**.
By analyzing customer behavior, spending patterns, and demographic data, we group customers into distinct segments to enable **targeted marketing and improved business strategies**.


## Dataset

The dataset used in this project is the **iFood marketing dataset**, containing customer information, purchase history, and demographic data.
**Source:** [Kaggle - iFood Dataset](https://www.kaggle.com/datasets/jackdaoud/marketing-data)

**Key columns include:**

* `Income`, `Age`, `Marital Status`, `Education`
* `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`
* `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumDealsPurchases`
* `Recency`, `Total_Spent`
* Other behavioral and demographic features


## Project Steps

1. **Data Loading & Cleaning**

   * Checked for missing values, duplicates
   * Filled missing values (e.g., Income) with median
   * Standardized column names

2. **Exploratory Data Analysis (EDA)**

   * Visualized distributions: Income, Age, Marital Status, Education
   * Product spending patterns per category
   * Purchase channel analysis
   * Recency vs total spending
   * Correlation analysis

3. **Feature Preparation**

   * Selected relevant numeric features
   * Standardized data using `StandardScaler` for clustering

4. **Clustering**

   * Applied **K-Means clustering**
   * Determined optimal clusters using **Elbow Method** and **Silhouette Score**
   * Visualized clusters using **PCA**

5. **Cluster Profiling & Insights**

   * Analyzed average income, spending, and purchase behavior per cluster
   * Identified high-value, moderate, low-value, and inactive customer segments

6. **Recommendations**

   * Personalized marketing strategies for each cluster
   * Loyalty programs, bundle offers, and reactivation campaigns


## Key Findings

* Majority of customers are **middle-income (20k–40k)**
* Most customers are **Married** and have **Graduation or Master’s level education**
* Customers spend **most on Wines and Meat products**
* **Recently active customers spend more**, while inactive customers spend less
* Clusters identified:

  1. **High-income, high-spending** → Premium segment
  2. **Moderate spenders** → Standard segment
  3. **Low-income, low engagement** → Price-sensitive segment
  4. **Recently inactive** → Needs reactivation


## Technologies Used

* **Python 3**
* **Jupyter Notebook**
* Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`


## How to Run

1. Clone this repository:

```bash
git clone <your-repo-link>
```

2. Open `Customer_Segmentation.ipynb` in Jupyter Notebook
3. Update the dataset path if needed:

```python
path = r"C:\path\to\ifood_df.csv"
```

4. Run all cells step by step
5. Explore charts, clusters, and insights


## Output

* Customer segments saved as: `segmented_customers.csv`
* Visualizations include:

  * Income & Age distribution
  * Marital Status & Education
  * Spending patterns per product category
  * Purchase channels
  * Clusters visualized using PCA


## Repository Structure

```
OIBSIP/
│
├─ Customer_Segmentation.ipynb   # Main notebook
├─ segmented_customers.csv       # Clustered customer data
├─ README.md                     # Project description
```


## Notes

* This project is completed as part of **Oasis Infobyte Internship (OIBSIP)**
* Insights and recommendations are based on **data exploration and cluster profiling**
* Can be extended with **additional features or other clustering algorithms**
