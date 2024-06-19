# Coffee-Sales-Analysis-Using-MS-Excel

<h1 align="center">Coffee Sales Analysis</h1>

<p align="center">
  <img src="">
</p>



### Introduction  
The Coffee Sales Analysis project aims to provide a comprehensive overview of sales performance, customer demographics, and product profitability for a coffee company. Utilizing data from three primary tables—orders, customers, and products—the project focuses on key metrics such as total sales by product, average sales prices, customer distribution, and profit margins. By employing Excel for data cleaning, aggregation, and visualization, the analysis offers valuable insights into sales trends, top-performing products, and customer loyalty patterns. This detailed examination supports strategic decision-making, enhancing marketing efforts and inventory management. 

### Project Overview
This project aims to deliver actionable intelligence to boost overall business efficiency and profitability.

### Data Sources
The dataset contains a single CSV file with 3 sheets that includes one table for each sheet and they are:
1. order
2. customer
3. product

### Tool
- MS Excel - Data Cleaning, Data analysis and creating dashboards

### Data Cleaning/Preparation
- **VLOOKUP** function in Excel used to update the Customer Name, Email, and Country columns in the orders table. By linking the orders table with the customer table through the common Email field, VLOOKUP efficiently fetches and populates the relevant customer information.
- **INDEX and MATCH** functions in Excel used to update the Coffee Type, Roast Type, and Size columns in the orders table. By leveraging these functions, the project dynamically retrieves and populates the corresponding product details from the product table based on the Product ID
-  Sales column calculated by multiplying the Unit Price with Quantity Sold for each order.
-  Formatted the Date column to the **'dd-mmm-yyyy'** format using Excel's **Custom date formatting**.  
-  Updated the Size column to display values with the unit **"kg"** using Excel's **Custom number formatting**.
-  Utilized multiple **IF** conditions to update the **Coffee Type Name** and **Roast Type Name** columns. By using **nested IF statements** in Excel, the project ensures that each code in the Coffee Type and Roast Type columns is accurately translated into its corresponding descriptive name, enhancing data clarity and usability.
-  Checked for duplicate rows.



### Data Analysis
```
1. =IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica"," "))))
```

```
2. =VLOOKUP(C3,customers!$A$2:$B$1001,2,0)

```
```
3. INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!L$1,products!$A$1:$G$1,0))
```

### Results/ Findings
- Total sales of all four variety of coffee increased in the year of 2022.  
- Analysis of the sales data revealed that the highest sales were recorded in the United States, followed by Ireland and the United Kingdom.
- The top 5 customers by sales include Allis Willimore, Benn Drundrege, and Terri Farra, highlighting these individuals as key contributors to coffee sales revenue

### Recommendation


### Dashboard 
- Check the dashboard here: 



### Acknowledgements
- This dataset was downloaded from Mo Chen YouTube channel (https://www.youtube.com/watch?v=m13o5aqeCbM&t=3001s)













