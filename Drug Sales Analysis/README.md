![image](https://github.com/user-attachments/assets/07076f36-0aff-45fc-8a64-df1785ac082b)
# Drug Sales Analysis Dashboard
<div align="center">
  <img src="https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Drug%20Sales%20Analysis/Drug%20Sales%20Logo.jpg" alt="HDFC Logo" width="500" height="300" style="float: left; margin-right: 10 px;"> 
</div>

### Table of Contents
-	Project Overview  
-	Problem Statement    
-	Objectives      
-	Business Requirements     
-	Functional Requirements     
  o	Data Gathering and Requirements       
  o	Data Modeling      
-	Data Calculations       
  o	DAX Calculations     
-	Dashboard Design     
  o	Dashboard 1: Top/Bottom Analysis     
  o	Dashboard 2: Customer Analysis     
  o	Dashboard 3: Trend Analysis   
-	Methodology      
  o	Step 1: Requirement Gathering    
  o	Step 2: Data Modeling and Cleaning  
  o	Step 3: UI Report Creation  
  o	Step 4: Additional Information      
-	Usage    
-	Technologies Used   
-	Conclusion 



### Project Overview
The Drug Sales Analysis Dashboard is a comprehensive tool designed to analyze and visualize drug sales data within the pharmaceutical industry. By leveraging data-driven insights, the dashboard aids in identifying top and underperforming products, tracking revenue trends, and understanding customer demographics. This empowers the company to make strategic decisions that drive growth and maintain market share.

________________________________________
### Problem Statement  
In the competitive pharmaceutical industry, it is crucial to analyze drug sales to sustain growth and maintain market share. The company needs to understand top and underperforming products, track revenue trends, and analyze customer demographics. By building a comprehensive dashboard, the company will gain insights for strategic decision-making and operational improvements, driving profitability. and maintain market share.
________________________________________

### Objectives
•	**Detailed Insights:** Provide comprehensive insights into the company's drug sales performance.  
•	**Performance Identification:** Identify top and bottom-performing products and customers.      
•	**Demographic Analysis:** Analyze customer demographics and their impact on sales.    
•	**Revenue Tracking:** Monitor revenue trends and geographical distribution of sales.      
•	**Strategic Decision-Making:** Enable data-driven decisions for resource allocation and market strategies.        
________________________________________
### Business Requirements
1.	**Key Sales Metrics:** Identify and track essential sales metrics to inform business decisions. 
2.	**Dynamic Analysis:** Enable dynamic analysis of sales performance across various dimensions (product, customer, geography).    
3.	**Actionable Insights:** Provide actionable insights to enhance marketing and operational strategies.     
4.	**Sales Forecasting:** Facilitate sales forecasting based on historical trends and demographic insights.      
5.	**Resource Allocation:** Support data-driven decisions for effective resource allocation and market strategies.         
________________________________________
### Functional Requirements     
Data Gathering and Requirements     

#### Data Sources:
•	DrugLookup (CSV/Database)   
•	CustomerTable (CSV/Database)     
•	RegulatoryCompliance (CSV/Database)      
•	FactTable (CSV/Database)        
#### Task 1.1: Sales Data Loading Mechanism      
•	Develop a mechanism to load all files from the dataset folder into a single fact table seamlessly.    
•	Features:       
  -	Automatic Loading: New files are automatically loaded upon refresh.   
  -	Error Handling: The system gracefully handles missing files without failing.        
### Data Modeling      
**Task 3.1: Data Transformation**     
•	Ensure correct data types are set, especially for the date field, to facilitate accurate date-based analysis.      
**Task 3.2: Data Model Design**      
•	Establish relationships between all tables (DrugLookup, CustomerTable, RegulatoryCompliance, FactTable) with necessary joins.         
•	DateMaster Table:       
  -	Fields:        
	Date    
	Year   
	Month   
	Month Name    
	Quarter    
	Week Number     
	Weekday      
	Weekday Name      
________________________________________

### Data Calculations    
DAX Calculations    
#### Task 4.1.1: Total Revenue Calculation      
•	**Formula**: Total Revenue = Product’s Retail Price * Units Sold     
#### Task 4.1.2: Total Cost Calculation         
•	**Formula**: Total Cost = Product’s Standard Cost * Units Sold   
#### Task 4.1.3: Gross Profit Calculation     
•	**Formula: Gross Profit** = Total Revenue – Total Cost      
#### Task 4.1.4: MoM Growth Change (%)    
•	**Description:** Calculate Month-over-Month (MoM) Gross Profit growth to provide decision-making insights.     
•	**Formula:**        

**MoM_Growth** = 
  DIVIDE(
    [Gross Profit] - CALCULATE([Gross Profit], DATEADD(DateMaster[Date], -1, MONTH)),
    CALCULATE([Gross Profit], DATEADD(DateMaster[Date], -1, MONTH)),
    0)      
#### Task 4.1.5: Average Sales per Day
•	Formula: Average Sales per Day = AVERAGEX(VALUES(DateMaster[Date]), [Total Revenue])
Task 4.1.6: QoQ Growth Analysis      
•	Description: Calculate Quarter-over-Quarter (QoQ) growth for quarterly reporting.       
•	Formula:       

**QoQ_Growth =**
  DIVIDE(
    [Gross Profit] - CALCULATE([Gross Profit], DATEADD(DateMaster[Date], -1, QUARTER)),
    CALCULATE([Gross Profit], DATEADD(DateMaster[Date], -1, QUARTER)),
    0
  )
________________________________________
### Dashboard Design
###### Dashboard 1: Top/Bottom Analysis
#### Overall Sales Metrics:
•	Metrics:
- 	Quantity Sold
- 	Cost of Goods Sold (COGS)
- 	Revenue
- 	Profit
-   Profit Margin
•	Comparison: Current vs. Previous Months
#### Performance Analysis:
•	**Focus:** Dynamic identification of top and bottom-performing drugs based on various measures (e.g., sales quantity, revenue) and their percentage contributions.
Customer Performance:       
•	**Focus:**   Identification of top and underperforming customers by various measures and contributions.      
###### Dashboard 2: Customer Analysis
#### Customer Demographics:
**Metrics:**
-	Total Number of Customers
- Average Revenue per Customer
- Revenue Distribution by Country
- Buyer Type (B2B, B2C)
#### Revenue by Demographics:
•	**Breakdown:** Revenue distribution by gender and age group.   
#### Geographical Insights:    
•	**Focus:** Highlighting revenue share from the top two countries.
###### Dashboard 3: Trend Analysis
#### Yearly and Quarterly Trends:
•	**Metrics:**  
-	Revenue Trends Over Time     
-	Number of Transactions    
-	Total Revenue (KPIs)      
#### Month-over-Month Revenue Changes:
•	**Details:** Breakdown of revenue changes for each month.
#### Weekday Sales Analysis:
•	**Metrics:**   
o	Revenue Breakdown by Weekdays    
o	Top Drugs Sold per Day     
________________________________________
###  Methodology
###### Step 1: Requirement Gathering
•	Business Requirement Document (BRD):  
-	Provides a clear picture of all business needs and use cases.  
•	Functional Requirement Document (FRD):     
-	Outlines steps, calculations, and approaches to advance the report.    
•	Data Collections:      
-	Sources include databases, CSV files, and Excel spreadsheets.        
###### Step 2: Data Modeling and Cleaning    
•	Data Modeling:         
-	Create relationships between different data sources to form a cohesive data model.    
•	Data Cleaning / Data Pre-Processing:    
-	Ensure data quality by handling missing values, correcting data types, and removing duplicates.    
###### Step 3: UI Report Creation       
•	Visual Elements:  
-	Develop charts and custom visuals to represent data effectively.         
###### Step 4: Additional Information       
•	DAX Calculations:     
-	Implement complex calculations to derive meaningful metrics and insights.    
________________________________________

#### Dashboard Navigation 

The dashboard consists of three main pages:

- **Top/Bottom Analysis**: Navigate to the Top/Bottom Analysis dashboard to identify and evaluate the highest and lowest performing drugs based on key sales metrics. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Drug%20Sales%20Analysis/Drug%20Sales%20Analysis%20Dashboard%20PDF_page-0001.jpg">View Dashboard</a>

- **Customer Analysis**: Access the Customer Analysis dashboard to explore customer demographics, purchasing behaviors, and their impact on overall sales performance. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Drug%20Sales%20Analysis/Drug%20Sales%20Analysis%20Dashboard%20PDF_page-0002.jpg">View Dashboard</a>

- **Trend Analysis** Visit the Trend Analysis dashboard to monitor and visualize revenue trends, sales patterns, and growth over different time periods. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Drug%20Sales%20Analysis/Drug%20Sales%20Analysis%20Dashboard%20PDF_page-0003.jpg">View Dashboard</a>

________________________________________

### Technologies Used 
•	**Power BI:** For creating interactive dashboards and visualizations.   
•	**Power Query:** For data transformation and cleanup.    
•	**DAX (Data Analysis Expressions):** For creating measures and calculations.    
•	**SQL/Databases:** For data storage and retrieval.    
•	**CSV/Excel:** For data sources and initial data collection.        
________________________________________

#### Dashboard
![Drug Sales Analysis Dashboard PDF_page-0001](https://github.com/user-attachments/assets/13e28c46-bca6-458a-9b63-8deff445eef1)
![Drug Sales Analysis Dashboard PDF_page-0002](https://github.com/user-attachments/assets/32cd2f77-f355-48da-94a8-612fdebbd527)
![Drug Sales Analysis Dashboard PDF_page-0003](https://github.com/user-attachments/assets/57f41dbd-7159-44d7-a2c2-9395e925b569)

________________________________________

### Conclusion     
The Drug Sales Analysis Dashboard serves as a powerful tool for the pharmaceutical company to monitor and analyze sales performance comprehensively. By providing detailed insights into sales metrics, customer demographics, and revenue trends, the dashboard facilitates informed decision-making and strategic planning, ultimately driving profitability and sustaining growth in a competitive market.
________________________________________













