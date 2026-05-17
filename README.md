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

3. Descriptive Statistics

3.1. Perform descriptive statistics to summarise the main characteristics of the data and draw meaningful insights. 

Numerical variables summary

<img width="570" height="593" alt="Numerical Variable Summary" src="https://github.com/user-attachments/assets/89fc34d9-81da-4970-b17d-e96e6ba455d6" />

Descriptive statistics were conducted on the numerical variables quantity and total_price to better understand customer purchasing behaviour and sales performance.
The average quantity purchased per transaction was 10.62 items, with values ranging from 1.00 to 20.00 items. The median quantity was 11.00, indicating that most customers purchased around 11 products per transaction. The relatively high standard deviation of 5.99 suggests noticeable variation in purchasing quantities among customers.

For total_price, the average transaction value was $124.19, while the median was $95.43. The maximum transaction value reached $427.14, showing that some customers made significantly larger purchases than average. Additionally, the standard deviation of 102.98 indicates considerable variation in customer spending behaviour.

Revenue by Product Category

<img width="629" height="462" alt="Revenue by Product Category" src="https://github.com/user-attachments/assets/bebe51a2-0f66-4e5a-8269-88d486407129" />

Revenue by Branch

<img width="625" height="227" alt="Revenue by Branch" src="https://github.com/user-attachments/assets/af2ebf6a-6f90-46c0-8a85-08542fe42932" />

Revenue by Customer Type

<img width="627" height="226" alt="Revenue by Customer Type" src="https://github.com/user-attachments/assets/fc0f17ae-8ac4-4abc-acce-3a2cdc7019ee" />

Key Insight 1: Fruits leads in volume but Stationery delivers the highest average transaction value

Fruits is the top-performing category in total revenue at $8,024.90 across 64.00 transactions, reflecting strong and consistent customer demand throughout the dataset. However, when examining average revenue per transaction, Stationery ranks highest at $142.16, followed by Beverages at $137.51, indicating that customers tend to spend more per purchase in these categories despite visiting less frequently. From a business perspective, the supermarket should maintain Fruits as a high-volume driver while developing targeted upselling strategies for Stationery and Beverages to capitalise on their higher per-transaction spending potential.

Key Insight 2: Member customers consistently outspend Normal customers

Member customers contributed $17,939.55 in total revenue with an average of $133.88 per transaction, compared to Normal customers who generated $13,106.73 at an average of $112.99, a difference of approximately 18% in average spending per visit. This pattern suggests that the membership programme effectively encourages higher spending behaviour among loyal customers. As a result, the supermarket should invest further in customer retention strategies and membership acquisition campaigns to sustain and grow long-term revenue performance.

3.2.Appropriate visualisation 

<img width="716" height="526" alt="Chart 1" src="https://github.com/user-attachments/assets/8eee945b-a45c-47e4-9246-6a1ac6bb2fe5" />

<img width="866" height="507" alt="Chart 2" src="https://github.com/user-attachments/assets/365e1af3-9bb7-41b7-b9a5-184dd12fe8a0" />

4. Conclusion

This analysis successfully applied Exploratory Data Analysis (EDA) techniques to examine the Supermarket Sales Dataset and uncover meaningful business insights. The dataset was carefully cleaned and prepared by handling missing values through mode and median imputation methods and removing duplicate records to ensure data accuracy and reliability for analysis.

Descriptive statistics revealed considerable variation in both customer purchasing quantities and transaction values, indicating diverse spending behaviours among supermarket customers. Revenue analysis further showed that Fruits generated the highest total revenue due to strong customer demand, while Stationery achieved the highest average revenue per transaction, suggesting greater spending per purchase in that category. In addition, Member customers consistently outperformed Normal customers in both total revenue contribution and average spending per transaction, highlighting the effectiveness of the supermarket’s membership programme in encouraging higher customer spending and loyalty.

Overall, the findings demonstrate how business analytics and data visualisation can support data-driven decision-making by identifying sales trends, customer behaviour patterns, and revenue opportunities. These insights may help supermarket managers improve marketing strategies, customer retention programmes, and product promotion decisions to enhance overall business performance.

