# Excel-Coffee_Sales_Analysis_Project



## Problem Statement

This dashboard helps the coffee company to understand their sales performance better. It helps the company recognize its loyal customers are satisfied with their services. It also helps analyze product preference (Coffee types, Roast types) and formulate strategies to improve sales.

It allows identifying:
Best-selling products, Best-performing countries, Top customers, Revenue generation trends.

Since, certain countries & products dominate sales, the company can now plan to expand similar products in underperforming countries.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Checked for null/missing values. Few records in 'Email' column were missing for customers.No critical missing values found in 'orders' or 'products' affecting analysis.

- Step 4 : Changed data types of 'Order Date' to  Date, Removed duplicate rows, Standardized Coffee Types and Roast Types.

- Step 5 : Gathered the Customer data like 'Customer Name', 'Email' 'Country' using following 'XLOOKUP' formula.
                              For Customer Name- =XLOOKUP(C2,customers!$A$2:$A$1001,customers!$B$2:$B$1001,,0,)

- Step 6 : Gathered the Product data like 'Coffee Type', 'Roast Type', 'Size', 'Unit Price' using 'INDEX MATCH'.
                             For Coffee Type-=INDEX(Table1,MATCH(orders!$D2,products!$A$2:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

- Step 7 : Calculated 'Sales' by multiplying 'Quantity' and 'Unit Price'.

- Step 8 : Number formatted the 'Size', 'Sales', 'Unit Price' column for better readability.

- Step 9 : Converted the range to a table for the creation of pivot table and charts.

- Step 10 : A pivot table named 'TotalSales' created having 'years' and 'month' in Rows and 'Coffee Type' in columns showcasing sum of sales. A line chart is created.

![Image](https://github.com/user-attachments/assets/a12aff6f-1082-4b24-8443-dddbe2902722)
  
- Step 11 : A bar chart is created having 'Country' in rows and 'Sales' in values box, named as 'Sales By Country'.

![Image](https://github.com/user-attachments/assets/65b8bdf1-ed26-4e2b-a447-e06f50add1d8)

- Step 12 : Another pivot table is created of 'Customer Name' and 'Sales' and a bar chart is created showcasing Top 5 Customers by sales.

![Image](https://github.com/user-attachments/assets/05d0c206-95c5-436a-9c4e-d8bb8f6d51f5)

- Step 13 : Inserted the timeline 'Order Date' on 'Totalsales By Country' line chart and done some formatting. 

![Image](https://github.com/user-attachments/assets/61df8171-56d5-4067-b0e7-2ce060129e96)


- Step 14 : Updated the data by creating the 'Roast Type Name', 'Loyalty Card' columns for the visualization purpose like for slicers.

        
- Step 15 : Inserted the slicers 'Size', 'Roast Type Name', 'Loyalty Card' on the dashboard.
  

![Image](https://github.com/user-attachments/assets/0d69b389-629f-4097-bcf4-48ead0189adf)
        
 - Step 16 : Color and font formatted the charts and created a visually appealing dashboard.
 
  
 
 
 Snap of dashboard
 
![Image](https://github.com/user-attachments/assets/1311778e-c5a0-42fd-b369-6872590f4bd5)

 


# Insights

A single page report was created on Excel.

Following inferences can be drawn from the dashboard;

### [1] Sales Trend

    a) Significant spike observed during festive season (Nov-Dec).
    b) Dips in sales during mid-year months (June-July).
    c) Total Sales = $ 1.04 Million (approx.)


           
### [2] Best Selling Countries

    a) United States contributed the highest sales (approx. 70% of total sales)
    b) Ireland and others had significantly lower contribution.
   
   
  
### [3] Coffee Type Performance 
  
    a) Robusta and Excelsa were top-selling coffee types.
    b) Arabica sales were relatively lower but showed higher profit margins.

### [3] Customer Analysis 
  
    a) Most top customers were Loyalty Card holders.
    b) Customers generally bought 2.5kg packs of Excelsa and Robusta in festive seasons (Nov-Dec).

### [4] Loyalty Program Insights

    Around 68% of sales came from Loyalty Card holders, confirming effectiveness of the loyalty program.



     
 
 
