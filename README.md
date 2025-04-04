# MARKETING_ANALYSIS

**PROJECT OVERVIEW**
  

**Objective:**
This project is analyzing an **e-commerce customer behavior dataset** (`ecommerce_consumer.csv`) using a variety of analytics techniques in R programming:
- Descriptive & Exploratory Data Analysis (EDA)
- Inferential analysis
- Churn analysis
- Clustering
- Association rule mining
- Predictive modeling
- Business recommendations

**DATASET DETAILS**

Columns in your dataset:
1. `order_id` – Unique identifier for each order  
2. `user_id` – Unique user identifier  
3. `order_number` – The number of that order (for that user)  
4. `order_dow` – Day of week when the order was placed  
5. `order_hour_of_day` – Hour of the day the order was placed  
6. `days_since_prior_order` – Time gap from the previous order  
7. `product_id` – Unique identifier of the product  
8. `add_to_cart_order` – Sequence of items added to the cart  
9. `reordered` – Whether the product was reordered  
10. `department_id` – Department code  
11. `department` – Department name  
12. `product_name` – Name of the product  

**SETUP & LIBRARY INSTALLATION**

 Installing and loading R packages like:
- `arules`: for association rule mining
- `caret`: for machine learning
- `rpart`: for decision tree modeling
- Others likely include `ggplot2`, `dplyr`, `cluster`, `e1071`, etc.
- 
**ANALYSIS SECTIONS**

1. **Descriptive & Exploratory Data Analysis (EDA)**
- Basic summary of customer behavior
- Order frequency patterns (hour/day of week)
- Top products and departments
- Reorder rates, customer lifecycle

2. **Churn Analysis**
- Identifying customers likely to stop purchasing
- Time since last order, decrease in order frequency, etc.

3. **Clustering**
- This is the part where the clustering is done for hig-value , low-vale and occasional bulk buyers.
- Customers with small cart sizes and frequent orders, Customers with large cart sizes and frequent orders, Customers with long gaps between orders.
  
4. **Association Rule Mining**
- Using the `arules` package to find patterns like:
- “Customers who bought X also bought Y”
- Generates rules based on support, confidence, and lift
- New csv file called "rules.csv" is generated.
- The generated file is used in python programming. Gradio interface is created which accepts a user input (the user can enter a product from the dataset) and the top five products are displayed which the user is likely to buy.

5. **Predictive Modeling**
- Using classification techniques (like Decision Trees via `rpart`) to:
  - Predict whether a customer will reorder
  - Predict the next product/category purchase

6. **Recommendations**
- Based on insights from the above analyses, suggestions are made such as:
  - Which customers to target with promotions
  - Which departments have strong cross-sell potential
  - How to reduce churn and increase retention
  
7. **Inferential Analysis**
   - The Welch Two Sample t-test is used to compare the means of two groups (here, reordered vs. not reordered products) to check if there is a statistically significant difference in their order_number.
