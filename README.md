# Purchase-Behavior-Analysis
## Project Intro/Objective
The purpose of this project is to gather insights about customers' shopping behavior. This project analyzes customer purchase behavior based on transactional data of 3,900 customers. It consists of data regarding various product categories, the items purchased, spending habits of the customers, whether the customer has a subscription or not etc., all of these together can help us in making strategic business decisions

-- Project Status: Completed

Methods Used
    
    Exploratory Data Analysis,
    Handled Missing Data,
    Feature Engineering,
    Column Standardization, 
    etc.

Technologies

    Python
    PostgreSQL
    Pandas, jupyter
    Power BI

## About the Dataset
The dataset consists of 3,900 rows of synthetic customer data and 18 columns. The columns are in following categories :-
    i) Customer Demographics – Age, Gender, Location, Subscription Status 
    ii) Purchase Details – Item Purchased, Purchase Amount (USD), Season, Size, Color, Category 
    iii) Shopping Behavior – Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating,                Shipping Type, Payment Behavior

## Workflow
    Exploratory Data Analysis (EDA) using Python -> Structured Analysis using SQL -> Data Visualization -> Recommendations

## EDA using Python
  1. Data Loading and Initial Exploration- Imported the dataset into Python and checked the structure and summary statistics with       .info() and .describe() using Pandas.
  2. Handling Missing Values - Checked for null values present in the Review Rating column and imputed them using the median rating     for each product category.
  3. Standardized the Column Names - Converted the column names to snake case. (Eg- Purchase Amount(USD) -> purchase_amount).
  4. Feature Engineering - Created 2 new columns, age_group and purchase_freq_days.
  5. Redundancy Check - Found that the discount_applied and promo_code_used columns were identical, so dropped promo_code_used.
  6. Database Connection - Connected to PostgreSQL and Loaded the cleaned dataframe into it for further analysis.

## Structured Analysis using PostgreSQL
  Answered the following business questions using PostgreSQL:-
    1. Total revenue by gender
    2. Customers who used discounts but still spent more than the average purchase amount
    3. Top 5 products by highest average review rating
    4. Average purchase amount: express vs standard shipping
    5. Average spend and total revenue: subscribers vs non-subscribers
    6. Top 5 products with the highest percentage of purchases made with a discount
    7. Customer segmentation into New, Returning, and Loyal based on previous purchases
    8. Top 3 most purchased products per category (window function)
    9. Whether customers with more than 5 previous purchases are likely to subscribe
    10. Revenue contribution by age group

## Dashboard
<img width="438" height="268" alt="Screenshot 2026-09-20 023141" src="https://github.com/user-attachments/assets/94a76a85-68cf-451e-aab4-bca7b759f8c1" />


## Key Findings
  1. Revenue by gender: male customers generated $156,157 versus $73,605 for female customers, about 68% of total revenue.
  2. Subscriptions: about 27% of customers are subscribed. Subscribers spend slightly more on average ($59.97 vs $58.52), but non-      subscribers contribute most of the revenue ($166,438 vs $63,324) because there are many more of them.
  3. Shipping: average purchase amounts for standard ($58.58) and express ($58.42) shipping are nearly identical.
  4. Customer segments: 3,104 customers are Loyal, 711 are Returning, and 85 are New.
  5. Age groups: revenue is spread fairly evenly, with Young Adults highest ($59,466) and Middle-aged lowest ($56,008).
  6. Top rated product: Coat (average rating 3.92).
  7. Discounts: Shorts (52%), Hoodie (50%), and Gloves (49%) have the highest share of purchases made with a discount.

## Business Recommendations
  1. Better Subscription Plans – Improve the subscription plan, give better benefits to encourage more people to get subscriptions.
  2.  Incentives for Loyal Customers – Introduce some kind of incentives for returning customers to move them into the “Loyal”           category.
  3. Best Seller Products – Promote the best-selling/ highest rated products in marketing campaigns.
  4. Targeted Marketing – Revenue is spread evenly across age groups and shipping types, so marketing does not need to favor one over   another. Segment by purchase history and subscription status instead.

## Credit 
This project was built by following a tutorial by Amlan Mohanty (video link :- https://youtu.be/5PrZvPeUw60?si=7WVK0D0ornY2rfg9). Used AI to slightly change the values within the dataset, and changed the color palette used.
