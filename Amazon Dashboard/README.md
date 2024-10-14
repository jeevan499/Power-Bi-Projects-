<div align="center">
  <img src="https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Amazon%20Dashboard/Amazon%20logo.png" alt="HDFC Logo" width="180" height="80" style="float: left; margin-right: 10 px;">
  <p> <b>Amazon</b> - Unlocking trends and insights to optimize sales performance in the world's largest online marketplace..</p>
</div>

### Amazon Sales Analysis Dashboard

#### Project Overview

This project involves creating a comprehensive dashboard to analyze sales data from Amazon's fashion category. The dashboard provides insights into sales performance, product categories, and trends, enabling stakeholders to make informed decisions based on data-driven insights.

#### Table of Contents
- Introduction
- Dataset
- Key Features
- Steps Involved
- Dashboard
- Navigation
- Technologies Used
- Conclusion

#### Introduction
The Amazon Sales Analysis Dashboard is designed to help users visualize and understand sales trends within the Amazon fashion category. By transforming and analyzing the data, the dashboard highlights critical metrics such as overall sales, units sold, and delivery counts.

#### Dataset

The dataset used in this project includes:

- Amazon Fashion sales data (CSV format)
- Amazon sales report (Excel format)

#### Key Features

- **Interactive Visualizations**: View sales trends over time and across different categories.
- **Category Slicers**: Filter data by specific product categories to focus on relevant metrics.
- **Search Functionality**: Quickly find products based on names.
- **Performance Metrics**: Display key performance indicators like total sales, total units sold, and seller counts.

#### Steps Involved

**1. Data Import and Transformation**

- Import the amazon-fashion – YT CSV file and clean the dataset.
- Extract the first image from the image column and handle null values in the category column.

**2. Data Cleanup**

- Remove unnecessary columns.
- Create new formatted columns for easier analysis.
- Use Power Query to apply transformations and close the query.

**3. Creating Slicers and Visuals**

- Add slicers for categories and images.
- Set up a search bar for product filtering.
- Create navigation buttons for different dashboard pages.

**4. Sales Data Integration**

- Load the Amazon Sales Report and transform the data to use the first row as headers.
- Merge the sales price column using ASIN numbers to integrate data from both datasets.

**5. Measures and Calculations**

- Create measures for total sales and quantities.
- Develop filtering measures based on selected slicers.
- Calculate overall sales and seller counts.

**6. Visual Representation**

- Create clustered bar charts and area charts to visualize sales performance.
- Set up cards to display overall sales, filtered sales, and seller counts.

**7. Product Tooltip Page**

- Create a separate worksheet for product details with custom dimensions.
- Sync slicers based on categories for consistent filtering across views.

**8. Review Measures**

- Implement measures to handle product reviews, ensuring that a zero value is displayed instead of a blank.

#### Dashboard Navigation 

The dashboard consists of three main pages:

- **Overview**: Provides an executive summary of sales data and trends. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Amazon%20Dashboard/Amazon%20Dashboard%20PDF_page-0001.jpg">View Dashboard</a>

- **Products**: Displays detailed product information and sales metrics. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Amazon%20Dashboard/Amazon%20Dashboard%20PDF_page-0002.jpg">View Dashboard</a>

- **Product** View: Allows users to view specific product details, including images and reviews. <a href = "https://github.com/jeevan499/Power-Bi-Projects-/blob/main/Amazon%20Dashboard/Amazon%20Dashboard%20PDF_page-0003.jpg">View Dashboard</a>

#### Technologies Used
- **Power BI:** For creating interactive dashboards and visualizations.
- **Power Query:** For data transformation and cleanup.
- **DAX (Data Analysis Expressions):** For creating measures and calculations.
  
#### Dashboard

![Amazon Dashboard PDF_page-0001](https://github.com/user-attachments/assets/f0fa1537-d786-44da-b9ee-3dc39c9d9190)
![Amazon Dashboard PDF_page-0002](https://github.com/user-attachments/assets/2c2e04dc-b959-44eb-bff1-55660e5cdeb4)
![Amazon Dashboard PDF_page-0003](https://github.com/user-attachments/assets/d413e865-6256-4b67-9e50-0e46b820d609)

#### Conclusion

The Amazon Sales Analysis Dashboard provides a powerful tool for understanding sales dynamics within the Amazon fashion category. By leveraging data visualization techniques and interactive elements, users can gain insights that drive better business decisions.

