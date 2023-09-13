# Analysis-For-Northwind-Traders-using-Power-BI
Analysis carried out on the Northwind Traders dataset aimed to provide an exhaustive and thorough understanding of the company's sales and operational performance.

## Introduction
The analysis conducted on the Northwind Traders dataset was both comprehensive and in-depth, covering a wide range of critical aspects related to the sales and operational performance of Northwind Traders. The primary goal of this analysis was to extract valuable insights into the business by thoroughly exploring all pertinent variables present in the datasets. Some of the key variables that were meticulously examined during the analysis encompassed various aspects of the company's operations. 
## Data Set
In this analysis, seven distinct data files in CSV format were utilized. Each of these data sets corresponds to a distinct record, encompassing pertinent variables concerning transactions. These datasets are organized with columns that hold various pieces of information for each individual record. Listed below are the dataset 
Categories
Customers
Employees
order_details
Orders
Products
Shippers 

## Data Preprocessing/Cleaning
The datasets were imported into power query editor one after the other in other to transform the data. To ensure the integrity of the dataset, I check for any duplicate entries.  Invalid entries, missing values, incorrect data. No duplicates were found, and incorrect column data types were adjusted the data types of each column to align them with their intended use. Twenty one “Null” values were found in the “shipped date” column of the “orders” table these null records were deleted to ensure accuracy in the analysis.
A new column was added using custom column with the Dax function “=[Unit Price] * (1-[Discount]) * [Quantity]” named “Total Revenue” 

## Data Modeling 
In this project, I created a robust data model using the Customers, Employees, Order Details, Orders, Products, and Shippers datasets. This data model serves as the backbone of our analysis, providing us with the tools to gain valuable insights into the operations of Northwind Traders.
-	Defining Relationships:
One of the key steps in building this data model was establishing relationships between the various tables. These relationships are essential for connecting data from different tables and performing meaningful analysis. Here are the relationships we identified and established:
1.	The "Orders" table had foreign keys for "Customer ID" and "Employee ID," linked respectively to the "Customers" and "Employees" tables.
2.	The "Order Details" table featured foreign keys for "Order ID" and "Product ID," connecting it to the "Orders" and "Products" tables.
3.	The "Customers" table contained a foreign key for "Company Name" that linked to the "Shippers" table.
4.	The "Categories" table contained a foreign key for "Category ID” that linked to the "products" table.
![](Dataset1.jpg)
## Key Performance Indicators (KPIs)
Before delving into specific analysis findings, let's review the KPIs:
1.	Total Revenue: The total revenue generated by Northwind Traders is $1.35 million.
2.	Average Shipping Days: The average days it takes to ship orders is 8 days.
3.	Total Discount: The total amount of discounts applied to orders is $117
4.	Average Shipping Cost: The average cost incurred for shipping is $79
5.	Total Products: Northwind Traders offers a total of 77 unique products.

The analysis of the Northwind Traders data aims to gain valuable insights into the operational performance. By exploring all relevant variables available in the dataset, few business questions were answered to better understand and optimize the Northwind Traders operations. Here are a few such questions:
-	What are the top 5 bestselling product in terms of revenue ?
-	Which of the categories make more sales ?
-	Analyze revenue trends over time (Monthly)
-	Which shipping company is more preferable by customers?

![](Dataset1.jpg)

### WHAT ARE THE TOP 5 BESTSELLING PRODUCT IN TERMS OF REVENUE?
In the visualization section, the x-axis featured product names, while the y-axis displayed total revenue, creating a chart to depict their relationship. To spotlight the top revenue earners, a "Top N" filter was applied, revealing the leading 5 products. A clustered column chart was chosen for its suitability in comparing product names side by side. The result was a clustered column chart with product names on the x-axis and their corresponding revenue on the y-axis, effectively showcasing the top 5 selling products by revenue.
Below is a screenshot of the resulting visualization:
![](Dataset1.jpg) 
In this screenshot, you can see the clustered column chart displaying the top 5 selling products in terms of revenue, with the product names on the x-axis and their respective revenue on the y-axis.

-Insight 

The analysis identifies high-impact products in Northwind Traders' inventory, highlighting those with substantial revenue potential and significant market demand. For instance, Côte de Blaye, a top performer, demonstrates exceptional sales compared to other products, likely due to its unique features, competitive pricing, or strong market demand. Leveraging such standout products becomes a crucial strategy for Northwind Traders to drive revenue and enhance profitability.
### WHICH OF THE CATEGORIES MAKE MORE SALES?
A Clustered Bar Chart was utilized for visualization, focusing on depicting the categories that contribute to sales. This was achieved by configuring the chart as follows:
The "Category Name" was placed on the Y-axis, categorizing the data vertically.
The "Total Revenue" was positioned on the X-axis, representing the total revenue horizontally.
This configuration produces a Clustered Bar Chart that effectively illustrates the relationship between product categories (on the Y-axis) and their corresponding total revenue values (on the X-axis). This visual representation aids in identifying which categories are the primary drivers of sales within the dataset.
Below is a screenshot of the resulting visualization:
![](Dataset1.jpg)

Insight 
"Beverages" lead revenue, suggesting strong demand. "Dairy Products" follow closely, indicating popularity. "Confections" also perform well. "Meat & Poultry" and "Seafood" contribute notably. "Condiments" and "Produce" provide substantial but slightly lower revenue. "Grains & Cereals" record the lowest revenue, possibly requiring focused marketing efforts. 

### ANALYZE REVENUE TRENDS OVER TIME (MONTHLY)
A line chart was employed to examine revenue trends over time. The "Order Day" table was placed on the X-axis, while total revenue was positioned on the Y-axis in the visualization section. To focus solely on monthly trends, the hierarchy of the order table was adjusted to display data at the month level. 
Below is a screenshot illustrating the resulting visualization

![](Dataset1.jpg)

Insight 
The data depicts monthly revenue, revealing trends and fluctuations throughout the year. 
Key points:
January kicks off strong in revenue.
April sees a significant surge in revenue, possibly due to seasonal factors.
Summer months (May, June) show a dip in revenue.
Revenue gradually rises from July to October.
November maintains robust revenue, likely influenced by holiday sales.
December concludes the year on a high note with revenue peaking. These insights can inform marketing and inventory strategies, capitalizing on peak months and addressing slower periods.

### WHICH SHIPPING COMPANY IS MORE PREFERABLE BY CUSTOMERS?
Utilizing a doughnut chart, I gained insights into the preferred shipping company among customers. This was achieved by placing the shipping cost data in the Value section and the shipping company names in the details section, allowing for a clear visualization of customer preferences for shipping providers.
Below is a screenshot of the resulting visualization:
![](Dataset1.jpg)

Insight 
The data reveals varying total shipping costs associated with different companies. United Package stands out with the highest cost of $27,556.76, suggesting it's a preferred choice among customers. Federal Shipping follows at $20,363.10, indicating competitive appeal. Speedy Express records lower costs at $16,035.16 but remains a significant shipping option.
## Tool Used 
This analysis was conducted utilizing Power BI.


## Recommendations:
To enhance revenue, explore product expansion within high-performing categories and execute tailored marketing initiatives.
Prioritize the promotion of best-selling items and explore sales-boosting strategies like promotions and bundles.
Investigate the drivers of seasonal revenue fluctuations and devise strategies to counteract slow months, including seasonal product introductions.
Optimize shipping expenses by negotiating favorable terms with United Package, while retaining relationships with Federal Shipping and Speedy Express, keeping a watchful eye on costs.

## Conclusion 
The examination of the Northwind Traders dataset yielded vital insights into category-based revenue, top-performing products, customer-favored shipping providers, and monthly revenue trends. These revelations can empower Northwind Traders to streamline operations, enhance customer contentment, and thrive in the competitive food distribution sector. To ensure continual growth and profitability, persistent monitoring and data-guided choices are imperative. Implementing the suggested enhancements can aid Northwind Traders in refining its sales and marketing approaches, consequently elevating revenue performance. A continuous vigilance over these metrics remains indispensable for sustained achievements in the long run.







