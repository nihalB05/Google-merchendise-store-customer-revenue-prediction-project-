# Google-merchendise-store-customer-revenue-prediction-project-

# Customer Revenue Prediction Project

## 📌 Overview
This project aims to predict customer revenue for the Google Merchandise Store using a large dataset of customer interactions. The dataset includes information such as website visits, session details, and revenue data. The goal is to build a machine learning model that can accurately predict customer revenue, enabling the business to optimize marketing strategies and target high-value customers effectively.

---

## 🚀 Project Structure
The repository is organized as follows:


---

## 📂 Dataset
The dataset consists of customer interactions from the Google Merchandise Store, including:
- **User Information**: `fullVisitorId`, `channelGrouping`, `device`, `geoNetwork`, etc.
- **Session Details**: `visitId`, `visitNumber`, `visitStartTime`, `totals`, `hits`, etc.
- **Revenue Data**: `totals_transactionRevenue` (target variable).

The dataset is available in two files:
- `train_v2.csv`: Training data (August 1, 2016 - April 30, 2018).
- `test_v2.csv`: Test data (May 1, 2018 - October 15, 2018).

---

## 🛠️ Preprocessing
The preprocessing steps include:
1. **Handling Missing Values**:
   - Replaced placeholders like `"not available in demo dataset"` and `"(not set)"` with `NaN`.
   - Filled missing values in categorical columns with `"unknown"`.
   - Filled missing values in numerical columns with the median.
2. **Expanding JSON Columns**:
   - Flattened nested JSON columns (`device`, `geoNetwork`, `totals`, `trafficSource`, `hits`) into separate columns.
3. **Feature Engineering**:
   - Extracted date-related features from `visitStartTime`.
   - Aggregated session-level data into user-level features.

The cleaned dataset is saved in the `data/processed/` folder.

---

## 🔍 Exploration and Visualization
The exploration notebook (`02_Exploration.ipynb`) includes:
- **Univariate Analysis**:
  - Distribution of numerical features (e.g., `totals_transactionRevenue`).
  - Frequency of categorical features (e.g., `device_browser`, `geoNetwork_country`).
- **Bivariate Analysis**:
  - Relationship between features and the target variable.
  - Correlation between numerical features.
- **Visualizations**:
  - Used `matplotlib` and `seaborn` to create insightful visualizations.

Key insights from the exploration phase are documented in the notebook.

---

## 🤖 Modeling
The modeling notebook (`03_Modeling.ipynb`) includes:
1. **Feature Engineering**:
   - Created new features (e.g., total visits, total revenue per user).
   - Encoded categorical variables using one-hot encoding.
2. **Pipeline Creation**:
   - Built a preprocessing and modeling pipeline using `sklearn.pipeline`.
3. **Model Training**:
   - Trained a Random Forest Regressor to predict customer revenue.
   - Evaluated the model using RMSE (Root Mean Squared Error).
4. **Model Saving**:
   - Saved the trained model to `models/revenue_prediction_model.pkl`.

---

## 📊 Results
The model achieved an RMSE of **X** on the validation set. Key findings include:
- **Top Features**: `totals_pageviews`, `totals_hits`, and `device_browser` were the most important features.
- **Insights**: Users from the United States and those using Chrome had the highest average revenue.

---

## 🛠️ Technologies Used
- **Python**: Primary programming language.
- **Pandas**: Data manipulation and preprocessing.
- **NumPy**: Numerical computations.
- **Matplotlib/Seaborn**: Data visualization.
- **Scikit-learn**: Machine learning modeling and evaluation.
- **Jupyter Notebook**: Interactive development environment.

---

## 🚀 How to Run the Project
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/nihalB05/Google-merchendise-store-customer-revenue-prediction-project-.git
   cd Google-merchendise-store-customer-revenue-prediction-project-
