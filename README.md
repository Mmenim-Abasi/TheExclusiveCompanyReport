Sales Report Analysis using Power BI
Overview
This repository contains the data model and analysis for a sales report designed in Power BI. The report provides insights into various dimensions of sales performance using a star schema design. The following sections describe the key tables and their relationships in the mod
DimCustomer
Description
The DimCustomer table holds customer-related data, enabling the analysis of sales performance by customer demographics, region, and other attributes.
Key Attributes
•	CustomerKey: Unique identifier for each customer.
•	FirstName: Customer’s first name.
•	LastName: Customer’s last name.
•	EmailAddress: Contact email of the customer.
•	Address: Customer’s physical address.
•	Region: Geographic region of the customer.
•	Gender: Customer’s gender either male or female. 
•	Marital Status: Customer’s marital status: either married or single.
•	Occupation: Customer’s work – clerical, management, manual, professional, and skilled manual.
•	Education: Customer’s education – bachelors, graduate degree, high school, partial college, and partial high school. 
DimDate
Description
The DimDate table provides a comprehensive date dimension for time-based analysis.
Key Attributes
•	DateKey: Unique identifier for each date.
•	FullDate: Full calendar date.
•	Day: Day of the month.
•	Month: Month name and number.
•	Quarter: Fiscal quarter.
•	Year: Calendar year.
DimProduct
Description
The DimProduct table contains product-specific information, facilitating the analysis of sales by product details.
Key Attributes
•	ProductKey: Unique identifier for each product.
•	ProductName: Name of the product.
•	ProductDescription: Brief description of the product.

DimProductCategory
Description
The DimProductCategory table organizes products into high-level categories for aggregated analysis.
Key Attributes
•	ProductCategoryKey: Unique identifier for each product category.
•	CategoryName: Name of the product category.
________________________________________
DimProductSubcategory
Description
The DimProductSubcategory table further segments product categories into subcategories, enabling detailed analysis.
Key Attributes
•	ProductSubcategoryKey: Unique identifier for each product subcategory.
•	SubcategoryName: Name of the product subcategory.
•	ProductCategoryKey: Foreign key linking to the DimProductCategory table.
________________________________________
FactInternetSales
Description
The FactInternetSales table is the central fact table in the model, storing transaction-level data for sales made over the internet.
Key Attributes
•	SalesOrderNumber: Identifier for each sales order.
•	OrderDateKey: Foreign key linking to the DimDate table.
•	CustomerKey: Foreign key linking to the DimCustomer table.
•	ProductKey: Foreign key linking to the DimProduct table.
•	Quantity: Number of units sold.
•	TotalSales: Total sales amount for the transaction.
•	Profit: Profit earned from the transaction.

Visualization
This data model is visualized using Power BI to provide insights such as:
•	Sales trends over time.
•	Regional sales performance.
•	Top-selling products and categories.
•	Customer purchase behavior.
•	Profitability by product and region.
How to Use
1.	Clone this repository.
2.	Open the Power BI file (SalesReport.pbix) in Power BI Desktop.
3.	Review the report and interact with the visuals to explore the data insights.
________________________________________
Contributing
Contributions are welcome! If you have suggestions or enhancements, feel free to create a pull request or raise an issue.


