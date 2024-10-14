
# Ice-cream Sales Analysis
**Business / Functional Requirement Document**

### 1.	Data Gathering / Requirement:
Assemble a sales report with different visuals to best show the Sales Insights in one page Dashboard. Feel free to use your imagination to best represent the data you have available.

1.	Categories (Excel)
2.	Geography (Excel)
3.	SalesRep (Excel)
4.	Product (CSV / Database)
5.	SubCategories (Excel)
6.	Sales (folder by year)


Task 1.1:
Create a mechanism to load all the files from the sales folder in a single Sales fact table.
The mechanism needs to be resilient as:
	-removing a file from the sales folder does not create an error for missing files.
	-adding a new yearly sales file will automatically be loaded in the fact query upon refresh.

### 2.	Data Modeling:
Task 2.1: 
Do the respective transformations to the Sales fact table in order to split the Country form the City in field “Location”. Make sure you set up the correct Data Type to allow Geo maps.
Do the necessary updates in the Date field to make sure you can setup the Date format.
Task 2.2: 
Create unique key (GeoKey) in Sales and Geography table

Task 2.3:
The Dimensional queries SalesRep and Sub Category need additional treatment. Some ID columns have the following format:
 
Create a small function that removes the “ID - ” part of these columns that you can invoke and reuse for these two queries to clean the IDs.
Task 2.4: 
Create the Data Model connecting all tables 
To Perform Time intelligence function Create Date Master so you can find Week wise sales, Month wise sales 
Create a new table called DateMaster using calendar datatype 
(Date, Year, Month, Month Name, Qtr, Week Number, Week Day, Week Day Name)

### 3.	DAX calculations (Data Analysis Expression) 
Task 3.1:
Calculate Total Revenue in Sales table, using the Product’s Retail Price, and multiplying it by the Units.
Task 3.2:
 Calculate Total Cost in Sales table, using the Product’s Standard Cost, and multiplying it by the Units.
Task 3.3:
Calculate Gross Profit in Sales: Total Revenue – Total Cost
Task 3.4:
Calculate a Gross profit MoM growth Change% measure that could benefit us in decision making
Task 3.5:
Calculate a measure for AVG sales per day – this is the average sum of Total Revenue per day based on the Dates of actual Sales.	
Task 3.7: 
-	Breakdown Analysis by Product (drop or increase)
Calculate the following time measures:
-	This is QBR Report. So QoQ Growth is required

### 4. Dashboard Details
Use the measures and calculations to assemble a sales reports with different visuals to best show the Sales Insights in one page Dashboard. Feel free to use your imagination to best represent the data you have available.
If you plot Month on x-axis, make sure the months are sorted from Jan-Dec.

1.	Create a slicer for Country, Year, Month Name
2.	Create a card for Total Revenue, Gross Profit, Unit Sold
3.	Create a Pie Chart on Total Revenue by Subcategory Name 
4.	Create a Donut Chart on Total Revenue by Category
5.	Using Multi-row card get the top 5 Sales representative
6.	Create a scroller by Product Name and Total Revenue
7.	Breakdown Analysis by Product over the year by Total Revenue
8.	Total Revenue by Product name and Subcategory Name using stacked column chart 
9.	Create a QoQ Growth using line chart
10.	 Create a MoM Growth using line chart

- Dashboard Interaction <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Ice%20Cream%20Sales%20Analysis/Ice%20Cream%20Dashboard_page-0001.jpg">View Dashboard</a>

### Dashboard

![Ice Cream Dashboard_page-0001](https://github.com/user-attachments/assets/c35ea58e-3b65-417e-90ff-5a74194ebb3d)




