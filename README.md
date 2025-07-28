# DSA-Excel-Project
This is the first section of the project that I was required to work on, as a criterion for certification at The Incubator Hub.

## Project Topic: AMAZON PRODUCT REVIEW ANALYSIS

### 1. Project Overview:

You are working as a **Junior Data Analyst** at **RetailTech Insights**, a company that provides e-commerce analytic solutions to companies like Amazon. Your team has been tasked with analysing product and customer rebiew data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

### 2. Data Description:

The dataset contains information scraped from Amazon product pages,including:

- Product details: name, category, price, discount, and ratings.
  
- Customer engagement: user reviews, titles, and content.
  
- Each row represents a unique product, with aggregated reviewer data stored as comma-separated values.
  
- Total Records: 1,465 rows.
  
- TotalFields: 16 columns.

  ### 3. Analysis Task

  Use pivot tables and calculated columns where necessary to answer the following:
  
1. What is the average discount percentage by product category?
   
2. How many products are listed under each category?
   
3. What is the total number of reviews per category?
     
4. Which products have the highest average ratings?
    
5. What is the average actual price vs the discounted price by category?
    
6. Which products have the highest number of reviews?
     
7. How many products have a discount of 50% or more?
     
8. What is the distribution of product ratings (e.g., how many products are rated 3.0, 
4.0, etc.)?
 
9. What is the total potential revenue (actual_price × rating_count) by category?
    
10. What is the number of unique products per price range bucket (e.g., <₹200, 
₹200–₹500, >₹500)?

11. How does the rating relate to the level of discount?
    
12. How many products have fewer than 1,000 reviews?
     
13. Which categories have products with the highest discounts?
     
14. Identify the top 5 products in terms of rating and number of reviews combined.

    ### 4. Final Task: Dashboard Creation 

Using your cleaned dataset and pivot outputs, build an Excel dashboard. Unleash your 
Creativity.

### 5. Execution:

The project was executed using Ms. Excel. It involved three phases which include: Data cleaning, data analysis, and data visualization.

- Data Cleaning: To clean the data, I first of all checked for duplicated values in the product_id column since the assumption is that the column should contain unique product ids. After removing duplicates, the number of rows were reduced to 1,351 from 1465. 
