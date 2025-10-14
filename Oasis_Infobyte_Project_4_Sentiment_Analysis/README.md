#  Twitter Sentiment Analysis

## Overview

This project focuses on performing **Sentiment Analysis** on Twitter data.
The primary goal is to classify tweets into **negative, neutral, and positive** sentiments.
This analysis helps understand public opinion, customer feedback, and social media trends.

**Dataset:**
https://www.kaggle.com/datasets/saurabhshahane/twitter-sentiment-dataset 


##  Key Concepts

* **Sentiment Analysis:** Classifying text into positive, neutral, or negative sentiments.
* **Natural Language Processing (NLP):** Text preprocessing, tokenization, lemmatization.
* **Machine Learning:** Naive Bayes classifier for sentiment prediction.
* **Feature Engineering:** TF-IDF vectorization to convert text into numeric features.
* **Data Visualization:** Word clouds and plots to explore sentiment distributions.


##  Project Steps

1. **Data Loading:** Loaded CSV file and inspected dataset structure.
2. **Exploratory Data Analysis (EDA):** Checked missing values, data types, and class distribution.
3. **Data Cleaning:** Removed URLs, special characters, stopwords; applied lemmatization.
4. **Sentiment Mapping:** Verified labels: `-1 = Negative`, `0 = Neutral`, `1 = Positive`.
5. **Feature Extraction:** Used **TF-IDF Vectorizer** to convert text to numeric features.
6. **Model Building:** Trained **Naive Bayes Classifier** for sentiment prediction.
7. **Evaluation:** Calculated **accuracy, classification report, and confusion matrix**.
8. **Visualization:**

   * Bar plot for sentiment distribution
   * Word clouds for most frequent words in each sentiment class
9. **Testing:** Predicted sentiments on sample tweets.


##  Results

* **Model Accuracy:** Achieved a strong accuracy for multi-class sentiment classification.
* **Word Clouds:** Visualized frequent words for negative, neutral, and positive tweets.
* **Insights:**

  * Negative tweets often include complaints or frustrations.
  * Positive tweets often highlight satisfaction or praise.
  * Neutral tweets are generally informational or ambiguous in tone.


##  Recommendations

* Integrate the model into a **real-time Twitter monitoring system** for brands.
* Analyze changes in sentiment over time to **track trends or detect issues early**.
* Extend the model using **deep learning approaches** like LSTM or BERT for higher accuracy.
* Use word clouds and frequency analysis to **identify common topics and concerns**.


##  Skills Learned

* Text preprocessing & NLP
* TF-IDF vectorization for feature engineering
* Naive Bayes classifier for text classification
* Data visualization using Matplotlib, Seaborn, and WordCloud
* Model evaluation using accuracy, confusion matrix, and classification report


##  Project Structure

```
Oasis_Infobyte_Project_4_Sentiment_Analysis/
│
├── archive (4)/
│   └── Twitter_Data.csv
│
├── sentiment_analysis.ipynb
├── README.md
└── output/
    ├── confusion_matrix.png
    ├── wordcloud_positive.png
    ├── wordcloud_negative.png
    └── wordcloud_neutral.png
```
