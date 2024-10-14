
<div align="center">
  <img src="https://github.com/user-attachments/assets/d7c2c803-0fb2-49ed-87d8-3334f0400f37" alt="HDFC Logo" width="150" height="80" style="float: left; margin-right: 10 px;">
  <p> <b>HDFC Bank</b> - Leading provider of financial services, offering a wide range of banking products and financial solutions.</p>
</div>



## Customer Churn Analysis at HDFC Bank
**Business/Functional Requirement Document**

## Problem Statement: -
Identify the key factors influencing customer churn at HDFC Bank to help design effective retention strategies and loyalty programs, reducing the rate of client attrition and improving overall customer satisfaction.
Data Dictionary

•	RowNumber - Corresponds to the record (row) number and has no effect on the output.  
•	CustomerId - Contains random values and has no effect on customer leaving the bank.  
•	Surname - The surname of a customer has no impact on their decision to leave the bank.   
•	CreditScore - Indicates the customer's creditworthiness, used to assess the likelihood of default and influence financial decisions within the bank.    

**Credit score:**     
•	Excellent: 800–850     
•	Very Good: 740–799    
•	Good: 670–739  
•	Fair: 580–669  
•	Poor: 300–579 
  
•	Geography - Specifies the customer's country or region, used to analyze location-based trends and patterns in customer behaviour.    
•	Gender - Denotes the customer's gender, used to analyze demographic trends and their impact on banking behaviour and churn rates.    
•	Age - Represents the customer's age, used to identify age-related trends and preferences in banking behaviour and product usage.    
•	Tenure - Refers to the number of years that the customer has been a client of the bank. Normally.     
o	Balance - Shows the customer's current account balance, used to evaluate financial stability and its influence on account activity and retention.     
o	NumOfProducts - Refers to the number of products that a customer has purchased through the bank.      
o	HasCrCard - Denotes whether or not a customer has a credit card      
•	1 represents credit card holder    
•	0 represents non credit card holder    
o	IsActiveMember - Active customers are less likely to leave the bank.     
•	1 represents Active Member        
•	0 represents Inactive Member    
o	Estimated Salary - Represents the customer's projected annual income, used to assess financial capacity and its impact on banking relationships and behaviour.   
o	Exited - whether or not the customer left the bank.     
  0 represents Retain    
  1 represents Exit    
o	Bank DOJ - Date when the Customer associated/joined  with the bank.     

### 1. Data Gathering / Requirement:   
Create a comprehensive one-page dashboard to visualize and analyze key banking metrics, using various visuals to effectively represent the data and uncover critical insights that drive informed decision-making in the banking sector.

Please use the following data assets to pull the data related to Bank customer and associated details.
o	ActiveCustomer (Excel) – Dimension Table   
o	Bank_Churn (CSV) – Fact Table    
o	CreditCard (Excel) – Dimension Table    
o	CustomerInfo (CSV) – Dimension Table    
o	ExitCustomer (Excel) – Dimension Table     
o	Gender (Excel) – Dimension Table     
o	Geography (Excel) – Dimension Table     

#### Task 1:-
1. Remove RowNumber from bank_churn table because it has no effect on customer churn. 

### 2. Data Modeling:

#### Task 2:-
Create the Data Model connecting all tables
 To Perform Time intelligence function Create Date Master so you can find Week wise Churn, Month wise Churn 
Create a new table called DateMaster using calendar datatype 
(Date, Qtr, Year, Month, Month Name, Week Number, Week Day, Week Day Name)

### 3. DAX calculations (Data Analysis Expression)

#### Task 3:-
Create a new table to store all the DAX calculations to perform calculated fields.   
-	Create a New Table -> Calculations = {1}       
-	Create a New Measures Total Customers, Active Customers, Inactive Customers, Credit Card Holders, Non Credit Card Holders, Exit Customers, Retain Customers, and Previous Month Exit Customers.   
-	Total Customers = COUNT(Bank_Churn[CustomerId])      
-	Active Customers = CALCULATE(COUNT(Bank_Churn[CustomerId]),ActiveCustomer[ActiveCategory] = "Active Member")      
-	Inactive Customers = [Total Customers] - [Active Customers]      
-	Credit Card Holders = CALCULATE(COUNT(Bank_Churn[CustomerId]),CreditCard[Category] = "credit card holder")     
-	Non Credit Card Holders = CALCULATE(COUNT(Bank_Churn[CustomerId]),CreditCard[Category] = "non credit card holder")     
-	Exit Customers = CALCULATE([Total Customers],ExitCustomer[ExitCategory] = "Exit")     
-	Retain Customers = CALCULATE([Total Customers], ExitCustomer[ExitCategory] = "Retain")      
-	Previous Month Exit Customers = CALCULATE([Exit Customers], PREVIOUSMONTH(DateMaster[Date]))        

- **Dashboard Interaction** <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/HDFC%20Customer%20Churn%20Analysis/HDFC%20Report_page-0001.jpg">View Dashboard</a>

### Dashboard

![HDFC Report_page-0001](https://github.com/user-attachments/assets/8d9a0249-bca9-43ad-a0a8-1f3ed0df203c)






