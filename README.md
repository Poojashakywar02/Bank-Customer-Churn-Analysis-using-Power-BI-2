# Bank-Customer-Churn-Analysis-using-Power-BI-2
Business Problem

A retail bank was experiencing customer attrition (churn) but lacked clear insights into:

Which customers are most likely to churn
Key factors driving churn (geography, behavior, account details)
Trends in customer retention over time
High-risk customer segments

The objective of this project was to analyze customer data and build an interactive dashboard to identify churn patterns and provide actionable strategies to improve customer retention.

Dataset Overview

The dataset contains customer-level information, including:

Customer Demographics – Geography (Germany, France, Spain), Age, Gender
Account Information – Balance, Tenure, Number of Products
Customer Behavior – Activity status, credit card ownership
Churn Indicator – Whether the customer exited or stayed
Customer Count Metrics – Total customers, churned customers
Approach & Methodology
1. Data Cleaning & Transformation (Power Query)
Imported raw customer dataset into Power BI
Handled missing/null values and ensured data consistency
Converted categorical variables (e.g., Geography, Gender) into usable formats
Created derived columns such as:
Churn Flag (0/1)
Age Groups
Balance Segments
2. Data Modeling
Structured the dataset into a clean analytical model
Established relationships (if multiple tables used)
Optimized model for fast querying and dashboard performance
3. Key Metrics & DAX Calculations

Total Customers

Total Customers = COUNT(Customer[CustomerId])

Churned Customers

Churned Customers = CALCULATE(COUNT(Customer[CustomerId]), Customer[Exited] = 1)

Churn Rate

Churn Rate = DIVIDE([Churned Customers], [Total Customers])

Active Customers

Active Customers = CALCULATE(COUNT(Customer[CustomerId]), Customer[IsActiveMember] = 1)
4. Dashboard Development

Built an interactive Power BI dashboard with the following components:

KPI Cards
Total Customers (~1,409)
Churned Customers (~500+)
Churn Rate (%)
Visualizations
Customer Distribution by Geography (Donut Chart)
Germany (~40%)
France (~39%)
Spain (~20%)
Churn Trend Analysis (Line + Bar Chart)
Tracks customer count vs churn over time
Customer Segmentation
By geography
By activity status
By account balance
Churn Drivers Analysis
Active vs inactive customers
Credit card ownership
Number of products
Comparative Analysis
Churn rate across countries
Customer behavior patterns
Key Insights & Findings
Total Customers: ~1,409
High Churn Volume: Over 500 customers have churned
Geographical Insight:
Germany has the highest churn rate, despite similar customer distribution
Customer Behavior:
Inactive customers are significantly more likely to churn
Product Usage:
Customers with fewer products show higher churn tendency
Balance Trend:
Customers with higher balances tend to churn more (possible dissatisfaction or better offers elsewhere)
Business Recommendations
Target High-Risk Regions:
Focus retention strategies in Germany where churn is highest
Improve Customer Engagement:
Re-engage inactive customers through personalized offers and communication
Product Bundling Strategy:
Encourage customers to adopt multiple products to increase retention
Loyalty Programs:
Offer incentives for high-balance customers to reduce churn risk
Predictive Analytics:
Implement churn prediction models to proactively retain customers
Tools & Technologies Used
Power BI – Data Visualization & Dashboarding
Power Query – Data Cleaning & Transformation
DAX – KPI & Metric Calculations
Excel/CSV – Data Source
Impact

This dashboard helped the bank to:

Identify high-risk churn segments
Understand customer behavior patterns
Improve customer retention strategy
Enable data-driven decision-making
