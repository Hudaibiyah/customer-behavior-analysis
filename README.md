# customer-behavior-analysis

## Project Overview
This project analyzes an ecommerce transactions dataset to extract customer and business insights such as revenue trends, product/category performance, repeat behavior, and CLV estimates.

## Dataset
- Rows: 50,000 transactions
- Columns: Transaction_ID, User_Name, Age, Country, Product_Category, Purchase_Amount, Payment_Method, Transaction_Date
  
## Key Metrics Calculated
- Total Revenue
- Average Order Value (AOV)
- Repeat Customer Rate
- Product Category Popularity
- Revenue by Product Category
- Revenue by Country
- Customer Lifetime Value (CLV proxy)
  
## Key Insights
- Total revenue is approximately **$25.16M**
- AOV is approximately **$503.16**
- **Toys** is the most purchased category by volume
- **Sports** is the highest revenue-generating category
- Top revenue countries: **France**, **Canada**, **USA**
- Churn-based CLV is not reliable in this dataset because churn evaluates to 0 using `User_Name` as customer identity
- Lifespan-based CLV proxy was used as a safer estimate
  
## Notes / Limitations
- `User_Name` is used as a customer identifier, which may not represent true unique customers.
- For production-grade retention/CLV, a stable `Customer_ID` and time-based cohort tracking are recommended.
  
## Tools Used
- Python
- Pandas
- Jupyter Notebook
