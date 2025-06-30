
#  Smart Retail: Customer Purchase Analysis and Prediction

This project analyzes real retail transaction data to uncover customer behavior, segment customers using RFM analysis, and build machine learning models to predict future spending and customer churn. It's a full-cycle data science project including EDA, feature engineering, and ML.

---

##  Dataset

- Source: [Online Retail Dataset from UCI/Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- Contains ~500,000 UK-based online retail transactions
- Columns:
  - `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

##  Key Questions Answered

- Which countries and products drive the most revenue?
- What days and months perform best?
- Who are the most valuable customers?
- Can we predict if a customer will return?
- Can we estimate how much a customer will spend?

---

##  Workflow

### 1. Data Cleaning
- Removed missing CustomerIDs and invalid records
- Removed returns and zero-priced items
- Created `TotalPrice = Quantity × UnitPrice`
- Converted InvoiceDate to datetime format

### 2. Exploratory Data Analysis (EDA)
- Top 10 countries by revenue
- Top-selling products
- Revenue trends by time (month, weekday)
- Customer spend distribution

### 3. Feature Engineering
- Extracted date parts: day, month, year
- Created new features for analysis

### 4. RFM Analysis
- **Recency**: Days since last purchase
- **Frequency**: Number of unique purchases
- **Monetary**: Total spend
- Created RFM scores and segmented customers into:
  - `High-Value`, `Mid-Value`, `Low-Value`

### 5. Machine Learning

####  Classification: Will a customer churn?
- Target: `Churn = 1 if Recency > 90 days`
- Model: `RandomForestClassifier`
- Metrics: Accuracy, Confusion Matrix, F1-Score

####  Regression: How much will they spend?
- Target: `Monetary Value`
- Model: `LinearRegression`
- Metrics: MAE, RMSE

---

##  Results

- High-value customers discovered through RFM scoring
- Customer churn predicted with ~85% accuracy
- Revenue prediction using regression model with RMSE ~250

---

##  What I Learned

- How to clean and prepare messy retail data
- How to segment customers with real-world marketing techniques
- How to train and evaluate classification and regression models
- How to turn business problems into data science pipelines

---

##  Future Improvements

- Add time-based features like days between purchases
- Try model tuning (GridSearchCV, XGBoost)
- Build a Streamlit app or Power BI dashboard
- Deploy churn prediction model via web interface

---

##  How to Use This Project

1. Clone or download the repo
2. Open `Retail_Customer_Analysis_and_Prediction.ipynb`
3. Run the notebook step-by-step
4. Dataset: [Download from Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data)

---

