# Customer Segmentation Analysis
**Objective**: The goal of this project is to analyze customer data to identify distinct segments based on purchasing behavior, demographics, and other relevant features. This analysis will help tailor marketing strategies and improve customer engagement.

**Dataset**: Online Retail II dataset from UCI, containing transactions from an online retail store.

## Data Loading and Initial Exploration
The dataset was loaded into a pandas DataFrame for analysis. Key features include `Invoice`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `Price`, `CustomerID`, and `Country`.

We inspect the first few rows of the data to understand its structure and identify any potential issues.

## Data Cleaning
Data cleaning was performed to ensure the quality of the dataset. We handled missing values in the `CustomerID` column by removing those rows, as `CustomerID` is essential for segmentation. Duplicate entries were also removed to prevent skewing the analysis.

## Feature Engineering
New features were engineered to capture key aspects of customer behavior:

- `TotalPrice`: Calculated as `Quantity` * `Price`, representing the total value of each transaction.
- `Recency`: Number of days since the customer's last purchase, indicating how recently they interacted with the store.
- `Frequency`: Total number of transactions made by each customer, reflecting their purchasing behavior.
- `Monetary`: Total spending by each customer, highlighting their value to the business.

## Exploratory Data Analysis (EDA)
EDA was conducted to understand the distribution of the newly engineered features. For example, we observed that most customers had low `Recency` scores, indicating recent purchases. The distribution of `Monetary` values showed that a small percentage of customers accounted for a significant portion of total sales.

## Customer Segmentation
K-Means clustering was applied to segment customers based on the `Recency`, `Frequency`, and `Monetary` features. We selected 4 clusters after evaluating the inertia and silhouette scores. The resulting clusters represent distinct groups of customers with similar purchasing behaviors.

## Insights and Recommendations
The analysis identified four distinct customer segments:

- **Segment 1**: High-value, frequent shoppers. Recommendation: Offer loyalty programs and exclusive discounts.
- **Segment 2**: Recent, low-frequency shoppers. Recommendation: Send targeted email campaigns to encourage repeat purchases.
- **Segment 3**: Infrequent, low-value customers. Recommendation: Focus on acquisition strategies to convert them into more valuable customers.
- **Segment 4**: Dormant customers. Recommendation: Re-engagement campaigns with special offers or reminders.

## Conclusion
This customer segmentation analysis provided valuable insights into customer behavior, allowing for more targeted marketing efforts. While the analysis was comprehensive, further research could explore the impact of seasonality on purchasing patterns or integrate additional data sources to refine the segments.
