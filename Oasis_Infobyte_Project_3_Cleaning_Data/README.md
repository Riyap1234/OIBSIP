# Data Cleaning — New York City Airbnb (Project 3)

## Overview

This project is part of my **Oasis Infobyte internship (OIBSIP Project 3)**.
**Objective:** Clean and preprocess the **New York City Airbnb 2019** dataset to ensure data accuracy, consistency, and reliability so it’s ready for analysis or modeling. The goal is to demonstrate practical data-cleaning skills (missing value handling, standardization, outlier treatment, feature engineering) and produce a reproducible notebook with clear explanations.


## Dataset

**File (local):**

```
C:\Users\as\Desktop\OIBSIP\Oasis_Infobyte_Project_3_Cleaning_Data\AB_NYC_2019.csv
```

**Source (original):** New York City Airbnb Open Data (Kaggle)

**Key columns you will work with (examples):**
`id`, `name`, `host_id`, `neighbourhood_group`, `neighbourhood`, `latitude`, `longitude`, `room_type`, `price`, `minimum_nights`, `number_of_reviews`, `last_review`, `reviews_per_month`, `calculated_host_listings_count`, `availability_365`

---

## Project Steps

1. **Data Loading & Initial Check**

   * Load CSV into `pandas`.
   * Inspect `df.shape`, `df.info()`, `df.head()` and `describe()`.

2. **Data Quality Audit**

   * Check missing values (`df.isnull().sum()`), duplicates, and unique constraints (e.g., `id`).
   * Inspect data types and obvious formatting issues (e.g., `price` as string).

3. **Cleaning & Preprocessing**

   * Convert `price` to numeric (remove `$`, commas), coerce errors to `NaN`.
   * Parse `last_review` to `datetime`.
   * Normalize categorical text (`room_type`, `neighbourhood_group`, `neighbourhood`).
   * Drop or deduplicate fully identical rows and resolve duplicate `id`s.
   * Logical imputation:

     * If `number_of_reviews == 0`, set `reviews_per_month = 0`.
     * Fill remaining `reviews_per_month` with median or a reasoned value.
   * Clip/cap unrealistic values (e.g., `minimum_nights` extreme values).
   * Filter invalid geographic coordinates (latitude/longitude outside NYC bounds).

4. **Outlier Treatment**

   * Use IQR method to detect extreme `price` outliers.
   * Option A: Drop extreme outliers for focused EDA (create `df_iqr`).
   * Option B: Cap prices into `price_capped` to retain rows but limit influence.

5. **Feature Engineering**

   * `host_size` (Solo / Small / Medium / Large) based on `calculated_host_listings_count`.
   * `days_since_last_review` using a dataset anchor date (e.g., `2019-12-31`) and fill `NaT` with `-1` or a separate flag.

6. **Exploratory Data Analysis (EDA)**

   * Price distribution (histogram, log-scale).
   * Price by `room_type` (boxplot).
   * Top neighbourhood counts (bar chart).
   * Latitude/longitude scatter colored by (capped) price.
   * Correlation heatmap of numeric features.

7. **Save & Document**

   * Export cleaned data (`AB_NYC_2019_cleaned.csv`).
   * Save the notebook `OIBSIP_Airbnb_Cleaning.ipynb` with clear comments and explanations.

8. **Present Findings & Recommendations**

   * Short actionable insights for potential stakeholders (hosts, property managers, data team).


## Key Findings (example — adapt with your exact numbers)

* Price distribution is heavily **right-skewed**; most listings are under $200 (a few high-priced outliers exist).
* **Entire home/apt** has higher median price than private rooms or shared rooms.
* A small set of neighbourhoods (many in Manhattan/Brooklyn) contain a large share of listings.
* `reviews_per_month` contains many missing values — often correlated with `number_of_reviews == 0`.
* Some rows contained invalid coordinates or extreme `minimum_nights` values which were filtered/capped.


## Recommendations (what business / stakeholders can do)

* Use cleaned data for price-prediction models or availability forecasts.
* For hosts with very high `minimum_nights`, investigate whether listing is long-term rental rather than short-term.
* Focus promotional efforts on neighbourhoods with high listing density but moderate occupancy to improve conversions.
* Monitor listings with no recent reviews (`days_since_last_review`) for quality/verification issues.


## Technologies Used

* **Python 3**
* **Jupyter Notebook**
* Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn` (optionally `folium` for interactive maps)

Install requirements:

```bash
pip install pandas numpy matplotlib seaborn
# optional: pip install folium
```


## How to Run

1. Clone your repo (or copy notebook into workspace):

```bash
git clone <your-repo-link>
cd OIBSIP
```

2. Place the dataset at:

```
C:\Users\as\Desktop\OIBSIP\Oasis_Infobyte_Project_3_Cleaning_Data\AB_NYC_2019.csv
```

or update the path in the notebook:

```python
file_path = r"C:\Users\as\Desktop\OIBSIP\Oasis_Infobyte_Project_3_Cleaning_Data\AB_NYC_2019.csv"
```

3. Open `OIBSIP_Airbnb_Cleaning.ipynb` in Jupyter and run cells in order.


## Output

* Cleaned dataset: `AB_NYC_2019_cleaned.csv`
* Notebook: `OIBSIP_Airbnb_Cleaning.ipynb` (contains all cleaning steps, explanations, and plots)
* Visualizations (examples):

  * Price distribution (histogram & log)
  * Price by room type (boxplot)
  * Top neighbourhoods (bar chart)
  * Listings map (lat/lon scatter)
  * Correlation heatmap


## Repository Structure

```
OIBSIP/
│
├─ data/
│  ├─ AB_NYC_2019.csv                 # Original (or link to Kaggle)
│  └─ AB_NYC_2019_cleaned.csv         # Cleaned output
│
├─ notebooks/
│  └─ OIBSIP_Airbnb_Cleaning.ipynb    # Main notebook with step-by-step cells
│
├─ video/
│  └─ demo.mp4                        # Short demo (60-90s)
│
├─ certificates/
│  └─ offer_letter.png
│  └─ completion_certificate.png
│
└─ README.md
```