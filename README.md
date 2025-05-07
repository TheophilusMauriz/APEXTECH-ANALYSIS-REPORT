# APEXTECH-ANALYSIS-REPORT
PostgreSQL Project
This project tackled real-world challenges in sales performance, inventory management, supplier efficiency, and customer purchasing behavior. I cleaned, transformed, and analyzed multiple datasets using PostgreSQL to answer 9 business-critical questions.

PROJECT OBJECTIVES
This project was developed to uncover actionable insights that will help optimize sales, supply chain efficiency, and customer retention strategies.
1.	Determine the companies top 5 best revenue generating products to ascertain the products that generates more funds to the company for the past 6 months.
2.	 Determine the most loyal customers who has placed the most orders.
3.	Acertain the  the month with the highest sales volumn and revenue.
4.	Investigate and identify supliers with high lead time and low reliability scores.
5.	Ascertain the most popular payment methods.
6.	Determine Customers Who Have Placed Orders but Later Canceled the Same Product
7.	Determine the Top 3 Most Efficient Suppliers Based on Lead Time & Reliability
8.	Identify Product Categories With the Highest Average Order Value
9.	Find Customers Who Have Spent the Most in a Single Transaction
10.	Provide data-driven recommendations for Sony Inc and other global electronic retailers to improve sales and future generation of revenue that would improve the companies overall productivity in coming years.

5 datasets was used for this analysis.
1.	Dim_customers
2.	Dim_dates
3.	Dim products
4.	Dim_suppliers
5.	Fact_sales
Dim_customers comprises of the following column headers
•	Customer_id
•	Customer name
•	City
•	Country
Dim_dates comprises of the following column headers
•	Date_id
•	Dates
Dim_products comprises of the following column headers
•	Product_id
•	Product_name
•	Category
•	Supplier
•	Price
Dim_suppliers comprises of the following column headers
•	Suppliers_id
•	Suppliers_name
•	Countrt
•	Reliability_score
•	Lead_time_day
Fact_sales comprises of the following column headers
•	Order_id
•	Customer_id
•	Order_date
•	Product_id
•	Quantity
•	Unit_price
•	Discount
•	Total_amount
•	Status
•	Payment_method

BUSINESS QUESTIONS
•	Find the Top 5 Revenue-Generating Products Over the Last 6 Months
•	Identify the Most Loyal Customers Who Have Placed More Than 10 Orders
•	Find the Month With the Highest Sales Volume & Revenue
•	Identify Suppliers With High Lead Times & Low Reliability Scores
•	Find the Most Popular Payment Method for High-Value Orders (> $1,000)
•	Detect Customers Who Have Placed Orders but Later Canceled the Same Product
•	Find Out-of-Stock Products That Have Been Sold Recently
•	Rank the Top 3 Most Efficient Suppliers Based on Lead Time & Reliability
•	Identify Product Categories With the Highest Average Order Value
•	Find Customers Who Have Spent the Most in a Single Transaction


DATA CLEANING
Data Cleaning was done using Excel and the following changes where made
1.	Changing Data types
2.	Renaming Column Headers
3.	Removing Duplicates
4.	Correcting errors in spellings
5.	Chganging letter cases

   
METHODOLOGY
•	Imported datasets into SQL using PostgreSQL schema.
•	Created and joined dimension and fact tables with foreign key constraints.
•	Applied data transformation and filtering (e.g., status = 'Delivered', date filters).
•	Aggregated and grouped data using GROUP BY, JOIN, HAVING, and window functions.
•	Generated insights from cleaned and queried data.



KEY PERFORMANCE INDICATORS (KPIS)
•	Total Delivered Orders: 382
•	Top Revenue-Generating Product: Law Headphones – ₦46,863.90
•	Top 5 Products by Revenue: Dominated by personal electronics (Headphones, Smartwatches, Tablets)
•	Most Loyal Customers: Joshua Robinson & Jason Jordan – 10 orders each
•	Peak Sales Month: September 2023 – ₦33,805.60 revenue
•	Highest Single Transaction: Joshua Robinson – ₦13,305.00 (Qty: 5 units)
•	Most Popular Payment Method for High-Value Orders: Credit Card – 94 transactions
•	Product Category with Highest Avg. Order Value: Tablets – ₦5,897.96
•	Customers with Canceled Orders: 40+ customers canceled specific items (e.g., Elizabeth Osborn, Ronald Gilbert)
•	Most Frequently Canceled Products: Law Headphones, Toward TV, Return TV
•	Most Efficient Suppliers:
	Phillips-Davenport – Reliability: 100, Lead Time: 19 days
	Spencer Group – Reliability: 95, Lead Time: 5 days
	Baker-Soto – Reliability: 95, Lead Time: 12 days
•	Suppliers with Low Reliability & High Lead Times:
	Owens-Reyes – Reliability: 83, Lead Time: 20 days
	Wilson, Jimenez, and Lewis – Reliability: 79, Lead Time: 11 days
•	High-Value Order Volume (>₦1,000): Driven by Credit Card, PayPal, and Debit Card usage

PROJECT OBJECTIVE RESULTS
1.	Find the Top 5 Revenue-Generating Products Over the Last 6 Months
The top 5 revenue generating products over the last 6 months are Lae Headphone geneating 46,863.9, Nothing Smartwatch generating 45,208.8, Help Tablet generating 44,890.05, Allow Tablet generating 42,163.35 and Pm tablet generating 41,511.60

2.	Identify the Most Loyal Customers Who Have Placed More Than 10 Orders.
The most loyal customers with 10 total orders are Joshua Robinson with order id CO94 and Jason Jordan with order id CO16
3.	Find the Month With the Highest Sales Volume & Revenue
The month with the highest sales volumn and revenue is September with 33,805.6 revenue generated and 4 orders made.
4.	Identify Suppliers With High Lead Times & Low Reliability Scores.
The customer with the highest lead time and low reliability scores is Owens Reyes with leadtime of 20 and reliability score of 83.
5.	Find the Most Popular Payment Method for High-Value Orders (> $1,000)
The top 5 payment methods for high value orders greater than $1,000 are Credit card with 94 order
6.	Detect Customers Who Have Placed Orders but Later Canceled the Same Product
There are a total of 388 customers who has placed orders and leter canceled the same products, the list includes their names, product that was cancelled, their customer id, product id and the status.
7.	Rank the Top 3 Most Efficient Suppliers Based on Lead Time & Reliability
The 3 most efficient suppliers based on leadtime and reliability are 
•	Philips-Davenport from Uzbekistan with reliability score of 100 and lead time of 19days
•	Spencer Group from Isreal with reliability score of 95 and lead time of 5days
•	Baker-soto from Maldives with reliability Score of 95 and leadtime of 12days
8. Identify Product Categories With the Highest Average Order Value
The product categories with the highest average order value are:  Tablet with apr 5898 avg order value, Laptop with 5151 avg order value, TV with apr  4713 avg order value, Headphone with apr 4542 order value, Mobile with 3928 avg order value and Smartwatch with 3174.8 avg order value
9.Find Customers Who Have Spent the Most in a Single Transaction
The customer who has spent the most in a single transaction is Joshua Robinson with customer id CO94 with 13,305 orders.

DATA-DRIVEN RECOMMENDATIONS
1.	ENCOURAGE PATRONAGE OF PRODUCTS THAT GENERATES LESS REVENUE
More qualified sales person should be employed to advertise the products that generates less revenue. Discounts can be given to encourage high sales and this can boost up the revenue in the future.
2.	GIVE DISCOUNTS FOR MORE ORDER PURCHASE
Only 2 people purchase above 10 orders, which is not good enough therefore discount can be given to individuals that made 2 or more orders. This would encourage patronage of bulk orders and increase the number of orders purchase over time.
3.	ENCOURAGE MORE SALES AND PURCHASE IN OTHER MONTHS OF THE YEAR.
Experts should be engaged that would look into the factors that made sales volumn and revenue to be high in the month of September, and these factors can be applied in other months of the year to improve sales and revenue. 


4.	MONITOR AND VISUALIZE SUPPLIER KPIS
What gets measured gets managed. What to Track:
•	On-time delivery rate
•	Fill rate
•	Average and variance in lead time
•	Quality metrics
•	Communication responsiveness

5.	RENEGOTIATE LEAD TIME OR PENALTY CLAUSES
Introduce penalties for delays or bonuses for early/on-time delivery. Or restructure contracts to include more agile terms for suppliers.
6.	GIVE BONUSES TO BEST CUSTOMERS
Joshua Robinson who has been the customer who has spent the most on a single transaction should be given bonuses that would encourage other customers to spend more to attract such bonuses.
7.	Bundle or Cross-Sell
Create product bundles (e.g. 3 for $10) or themed kits — this raises perceived value and average order value.
Offer "frequently bought together" suggestions or discounts.
8.	Analize the "Why" Behind Cancellations of Already Ordered Products
Analize why products are being cancelled after order, reach out to the customers, offer them discounts or free shipping.
Encourage them with a rebuy policy where they get free gift for reordering any product that they previously cancelled.



Prepared by:
IYAMA MAUREEN
Email: maureeniyama@yahoo.com
ROLE: DATA ANALYST





