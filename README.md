# Mis-311
Data Overview
Source of Data: The dataset comes from the sales sheet of the supermarket sales file. Each row represents a single transaction made by a customer.
Size of Dataset:
Rows: 250 transactions
Columns: 10 variables
Variables:
sale_id: Unique identifier for each transaction
branch: Branch code where the sale occurred (A or B)
city: City where the branch is located (New York, Los Angeles, Chicago)
customer_type: Type of customer (Member or Normal)
product_name: Specific product purchased (Apple, Shampoo, Notebook, Orange Juice, Detergent)
product_category: Broader product category (Fruits, Personal Care, Stationery, Household, Beverages)
quantity: Number of items purchased in the transaction
total_price: Total value of the transaction
Revenue: Recorded revenue from the transaction
Price per unit: Unit price of the product purchased
Context:
This dataset captures detailed supermarket sales across multiple branches and cities. It allows analysis of customer behavior (Member vs Normal), product performance (by category and name), and financial outcomes (quantity, total price, revenue, unit price). The data is suitable for exploratory analysis to identify spending patterns, product trends, and branch performance.

Data Cleaning
a. Missing Values
Handling Missing Values
Customer_type:
These are categorical variables → filled with the mode (most frequent value).
Product_category:
 Missing values in the product_category column were not filled using the most frequent value, as this would ignore the logical relationship between products and their categories. Instead, product categories were inferred based on the corresponding product_name, ensuring that each product was assigned to its correct and consistent category. This approach preserves the semantic accuracy of the dataset and improves the reliability of further analysis.


quantity:
 This is numerical → filled with the median quantity (11) to avoid distortion by extreme values.
b. Duplicate Rows
Duplicate rows found: 3


These rows were removed to avoid double-counting sales and inflating revenue or quantities.
Descriptive Statistics
Summary of Numerical Variables

Quantity:
The average number of items per transaction is 10.6, and the median is 11, which means the distribution is fairly balanced. However, the most frequent value (mode) is 2, showing that many customers often buy just a small number of items. The standard deviation of 5.99 indicates moderate variability, with transactions ranging from very small to quite large.
Total Price:
The average total price per transaction is about 124.2, while the median is lower at 95.43, suggesting that a few very high‑value transactions are pulling the average upward. The most common transaction value (mode) is 212.82, which appears frequently in the dataset. The standard deviation of 102.98 is quite high, reflecting significant differences in transaction sizes.

Revenue:
The average revenue per transaction is 1761.78, but the median is only 1065.19, again showing that a small number of very large transactions raise the average. The standard deviation is extremely high at 1956.73, which highlights strong variability in revenue across transactions.
Price per Unit:
The average unit price is 11.62, and the median is 11.46, which are very close, indicating a stable and balanced distribution of product prices. There is no clear mode, meaning no single price dominates the dataset. The standard deviation of 6.12 shows moderate variation, reflecting the mix of low‑priced and higher‑priced products.


VISUALIZATION

Insight 1: Members spend more than normal customers Based on the statistics, transactions from Members generally have higher average total_price and Revenue compared to Normal customers. This indicates that the membership program is effective in driving spending, suggesting that the supermarket should continue to strengthen and expand its loyalty policies.


Insight 2: Shampoo and Notebook generate many high‑value transactions Transactions involving Shampoo and Notebook often show high total_price and occur frequently. This demonstrates that the Personal Care and Stationery categories are key drivers of revenue, and the supermarket could focus its marketing efforts on these two groups to boost growth.
