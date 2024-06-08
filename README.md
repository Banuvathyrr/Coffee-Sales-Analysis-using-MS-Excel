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

  
### Exploratory Data Analysis


### Following Measures and Columns were created


### Data Analysis
```
1. =IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica"," "))))
```

```
2. =VLOOKUP(C3,customers!$A$2:$B$1001,2,0)

```
```
3. SELECT
	*,
	CASE 
		WHEN promo_type = '50% OFF' THEN base_price* 0.50
        WHEN promo_type = '25% OFF' THEN base_price* 0.75
        WHEN promo_type = '33% OFF' THEN base_price* 0.67
        WHEN promo_type = '500 Cashback' THEN base_price - 500
        ELSE base_price
	END AS base_price_after_promo
FROM 
	fact_events;
```

### Results/ Findings
- During the **Diwali campaign**, the **500 cashback** promotional offer resulted in significant **revenue**. Conversely, during the **Sankranti campaign**, the **BOGOF promotion** demonstrated notable success.
- In the case of the BOGOF promotion, it was observed that as the incremental units sold increased, the corresponding incremental revenue did not exhibit a proportional increase. 
- Instead, the relationship between incremental sold units and incremental revenue appeared to follow a linear trend with a lesser slope. 
- This suggests that while sales volume increased, the generated revenue did not rise at an equivalent rate, indicating potential factors, such as the type of product, promo-type influencing revenue generation beyond solely increasing sales volume.
- Although the product category remained the same (Combo) for both the Diwali and Sankranti campaigns in the case of the 500 cashback promotion, **the total revenue yielded during the Diwali campaign was significantly higher compared to the Sankranti campaign**. 
- This disparity may be attributed to the **timing** of the campaigns, as the Diwali campaign preceded the Sankranti campaign, allowing consumers to utilize the cashback promotion for purchasing combo sets during the Diwali campaign itself.
- During the **Sankranti campaign**, there was a **surge in purchases of groceries, home appliances, and home care products, resulting in increased quantity sold**. However, this did not translate into significantly higher revenue, as these product categories typically do not yield substantial revenue.

### Recommendation
- **Store Expansion Strategy**: Implementing a store expansion strategy by adding number of stores in each city can significantly enhance revenue generation. 
- **Streamlining Promotional Strategies**: To optimize our campaign strategy and maximize revenue potential, we propose removing the 25% off, 33% off, and 50% off promotions for both campaigns. Our analysis demonstrates that these promotions have shown to be less effective compared to the Cashback and BOGOF promotions. By reallocating resources to focus on the more successful promotions, we aim to drive greater impact and ensure the highest possible return on investment.
- **Strategic Expansion of BOGOF Promotion**: For the Diwali campaign, we propose extending the BOGOF (Buy One, Get One Free) promotion strategy to include groceries. This strategic adjustment aims to capitalize on the high demand for groceries during the festive period. 
- **Introducing 500 Cashback Offer**: During the Sankranti campaign, we propose introducing the 500 cashback promotional offer to a new set of product categories, apart from combo sets. Recognizing that customers may have already purchased combo sets during the Diwali campaign, this strategic adjustment aims to maintain consumer interest and incentivize purchases in different product categories.

### Dashboard 
- Check the dashboard here: https://www.novypro.com/project/retail-mart-promotion-analysis-power-bi

### Video Presentation link:
- Check for the presentation in google drive: https://drive.google.com/drive/folders/1F1y6BL5GIRh6MmGLdEedMCvBPxGwC36f

### Acknowledgements
- This Project is a Codebasics Resume project challenge#9 (https://codebasics.io/challenge/codebasics-resume-project-challenge)













