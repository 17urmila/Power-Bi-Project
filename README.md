# Power-Bi-Project
# Walmart Sales and profit Dashboard 

## Problem Statement

This dashboard helps the Walmart e-commerce  to improve their business by analyzing the sales and profit or loss . It helps to  know if their customers are satisfied with their services or not. By analyzing the profit and loss on different product categories they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the areas from where they are getting least orders so that they can find the reasons for least order and make changes accordingly. 


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Dataset used :  

   https://raw.githubusercontent.com/LokeshKumarChauhan/DE_with_powerBI/main/Walmart.csv

- Step 3 : Python Script to download the dataset from API to Power BI
  
     import pandas as pd

     link="https://raw.githubusercontent.com/LokeshKumarChauhan/DE_with_powerBI/main/Walmart.csv"
     df=pd.read_csv(link)
     print(df)

- Step 4 : Open power query editor & in view tab under Data preview section , check "column distribution" , "column quality" and "column profile " options.
- step 5 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 6 : It was observed that in none of the columns errors & empty values were present except column named "    ".
- step 7 : A new column called "year" is added to the existing table from "order date" column to extract year and compare the sales by year.
    DAX expression for creating new column : 
     year = year(df[Order Date])

- Step 8 : In the report view, under the view tab, theme was selected.

- Step 9 : Four card visuals were added to the canvas, representing No of transactions, sum of profit, sum of sales, and number of sub-categories, no of customers.

- Step 10 : A pie chart is added to show the sum of the sales of individual subcategory, which can help to improve the sales.
- Step 11 : Since the data contains several subcategory items , a new visual was added using donut chart in the visualization pane in report view .While creating this visual, field name 'subcategory' is added to the Legends, thus sum of profit is segregated according to the category.

- Step 12 : A bar chart was also added to the report design area representing the sum of sales by year.
-Step 13 : A funnel is added to showcase the year wise profit to compare and improve the sales

- Step 14 : A bar chart was also added to show sum of sales by city.
- Step 15 : Gauge is added to represent the sum of profit of a particular subcategory.
- Step 15 : The snapshot of the report was added to the GitHub .

  
 # Insights            
 
 A single page report was created on Power BI Desktop and the report was shared in the GitHub repository.

 Following inferences can be drawn from the dashboard;

 #[1] Number of Customers = 686
 #[2] Sum of sales = 725.46K
 #[3] Sum of profit = 108.42k
 #[4] No of transactions = 3203
 #[5] No of sub-category
 #[6] Most selling products in each category

 # Furniture

 1.1) 14.03 % customers have purchased  chairs      
 1.2) 11.68 % customers have purchased  tables      
 1.3) 9.72 % customers have purchased  storage  
 1.4) Least selling product in this category is Art(1.27%)    

  # Technology

 2.1) 13.6 % customers have purchased  phones      
 2.2) 5.85 % customers have purchased  machines     
 2.3) Least selling product in this category is Appliances(4.17%) 

  # Office Supplies

 3.1) 8.42 % customers have purchased  accessories      
 3.2) 7.71 % customers have purchased  binders      
 3.3) 6.86 % customers have purchased  copiers
 3.4) Least selling product in this category is Labels(0.7%) 

Thus, more customers have purchased items from furniture category 
 
