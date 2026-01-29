# Mis-311
Data Overview
Source of Data: The dataset comes from the 10_Supermarket Sale.xlsx file, specifically the sales sheet. Each row represents a single customer transaction.
Size of Dataset:

Rows: 250 transactions
Columns: 10 variables
Variables:

sale_id: Unique identifier for each transaction
branch: Branch code (A or B)

city: City where the branch is located (New York, Los Angeles, Chicago)

customer_type: Type of customer (Member or Normal)

product_name: Specific product purchased (Apple, Shampoo, Notebook, Orange Juice, Detergent)

product_category: Broader product category (Fruits, Personal Care, Stationery, Household, Beverages)

quantity: Number of items purchased

total_price: Total value of the transaction

Price per unit: Unit price of the product purchased

Context:
This dataset captures detailed supermarket sales across multiple branches and cities. It allows analysis of customer behavior (Member vs Normal), product performance (by category and name), and financial outcomes (quantity, total price, unit price). The data is suitable for exploratory analysis to identify spending patterns, product trends, and branch performance.
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

