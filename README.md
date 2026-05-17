Part 1: Data Analysis and Insight
1. Data Overview

The dataset used in this analysis is the Supermarket Sales Dataset, which contains transactional data from a supermarket.
The dataset consists of 254 rows (including rows of variables, 253 if not including rows of variables) and 8 columns, including the following variables: sale_id, branch, city, customer_type, product_name, product_category, quantity, and total_price. These variables provide detailed information about each transaction, such as where the purchase was made, the type of customer, and the products purchased, along with the quantity and total spending.

Overall, the dataset represents sales activities across different branches and cities, allowing for a comprehensive analysis of customer purchasing behaviour and revenue distribution. It enables comparisons between locations, identification of popular products and categories, and evaluation of factors that influence total sales performance.

Given its structured format and relevant business variables, this dataset is well-suited for exploratory data analysis (EDA) to uncover meaningful insights and support data-driven decision-making in a business context.

2. Data Cleaning
	
  2.1. Identify missing values and decide how to handle these missing values

Identifying Missing Values

A thorough inspection of the dataset revealed missing values in three columns across 12 cells in total: 
The quantity column (column G) had missing values at rows 22, 48, and 65.
The product_category column (column F) had missing values at rows 33, 35, 53, 72, 91, and 103.
The customer_type column (column D) had missing values at rows 34, 38, and 48.
Handling Missing Values

Two imputation methods were applied based on the data type of each column.
Mode imputation was used for product_category and customer_type, as both are categorical variables. Missing values were replaced with the most frequently occurring value in each column  "Fruits" for product_category (60 occurrences) and "Member" for customer_type (131 occurrences). Mode imputation is appropriate here because categorical variables have no numerical order, making statistical measures such as mean or median unsuitable.

Median imputation was used for quantity, as it is a numerical variable. Missing values were filled with the median value of 11. The median was chosen over the mean because it is less sensitive to outliers, providing a more stable and representative estimate, particularly important given that quantity values range widely from 1 to 20.

After applying both methods, the dataset contained no remaining missing values across all 8 columns.

2.2. Identify any duplicate rows and remove duplicate rows if necessary

A check for duplicate rows revealed 3 duplicate entries in the dataset, corresponding to sale_id 13, 26, and 40. Each of these records appeared exactly twice across all 8 columns, indicating that the transactions were accidentally recorded more than once rather than representing separate purchases. Since duplicate rows provide no additional information and could distort the analysis by inflating transaction counts and total revenue figures, all 3 duplicate rows were removed. After this step, the final cleaned dataset consists of 250 rows and 8 columns, ready for further analysis.

Result summary

<img width="621" height="264" alt="Result summary" src="https://github.com/user-attachments/assets/21e8b442-2e0d-49bc-a432-d79021b61f91" />




