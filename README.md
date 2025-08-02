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

#### - Data Cleaning: 

To clean the data, I first of all checked for duplicated values in the product_id column since the assumption is that the column should contain unique product IDs. After removing duplicates, the number of rows were reduced to 1,351 from 1465.

Next, the category column contained different category levels separated by a vertical bar (|). So, using the 'text-to-column' feature, I separated the entries into columns and then chose the first category level for the analysis. I copied the selected column, and pasted it in my dataset. I then hid the mother column for category.

I did the same thing for the review_id column. However, after separating each review into columns, I then copied all the columns and pasted it in my dataset, before hiding the mother column for review_id.

The next step was to check for errors, and blank cells in the columns containing values using the filter feature. 

I corrected the errors, and replaced blank cells with '0' (as instructed) using the 'find and replace' feature.


#### - Data Analysis:

I had to create new columns for:

- Potential revenue:
  =Actual price * Rating count.
  
- Discount of >= 50%:
  =IF(Discount % >=50%,"YES","NO").
  
- Price range (<1000,1000-10,000, >10,000):
 =IFS(E2<1000,"<₹1000",E2<=10000,"₹1000 - ₹10000",E2>10000,">₹10000").
  
- Rating count <1000:
  =IF([@[rating_count]]<1000,"YES","NO").
  
- Combination of rating and no. of reviews:
  =[@rating]+([@[review count per product]]/8).
  
- Discount % range (0-10%, 11-20%,...,91-100%):

  =IFS(
  [@[discount_percentage]]<=0.1, "0-10%",
  [@[discount_percentage]]<=0.2, "11-20%",
  [@[discount_percentage]]<=0.3, "21-30%",
  [@[discount_percentage]]<=0.4, "31-40%",
  [@[discount_percentage]]<=0.5, "41-50%",
  [@[discount_percentage]]<=0.6, "51-60%",
  [@[discount_percentage]]<=0.7, "61-70%",
  [@[discount_percentage]]<=0.8, "71-80%",
  [@[discount_percentage]]<=0.9, "81-90%",
  [@[discount_percentage]]<=1,   "91-100%"
  ).
  
- Review count per product:
  =COUNTA(U2:AB2).

After adding the columns, I put the dataset into a table.

Then, I made use of pivot tables and some other excel functions (Sum, Count...e.t.c) to summarize the data and obtain the necessary information needed for data visualization.

#### - Data Visualization:

Using line charts, pie charts, bar charts, column charts, and some formatting and design tools, I created a dashboard to provide a visual representation of key information obtained from the analysis. The dashboard was designed to be easy to interpret thereby, aiding effective finanacial decision making.

#### View Dashboard here:
[Amazon case study(AutoRecovered).xlsx](https://github.com/user-attachments/files/21559345/Amazon.case.study.AutoRecovered.xlsx)
