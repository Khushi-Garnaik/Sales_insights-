Sales Insights Project using Microsoft Power-Bi 


About Project 

Performed India based hardware company sales insights - A Data Analysis project.

Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design star schema data model on Power-Bi .

Developed a Power-Bi dashboard to perform analysis, producing quantitative visualizations to draw valuable insights based on different parameters affecting the company performance year on year 

Technologies used - 

Advance Excel excel

MySQL mysql | SQL Server sql-server

Microsoft Power-Bi 

Statistics 


Problem Statements -

Atli hardware is a company which sells computer hardware and peripheral manufacturers . 
They are facing challenges in a dynamically changing market. Sales director decides to invest in a data analysis project and he would like to build a Power BI dashboard that can give him real time sales insights.


Q1. Revenue and Sales quantity distribution based on customer and market .

Q2. Revenue breakdown by years & months.

Q3. Top 5 customers by revenue & sales quantity.

Q4. Top 5 Products by revenue.

Q5. Net Profit & Profit Margin by Market

Q6. Profit Analysis - Revenue Contribution , Profit Margin Contribution 

Q7. Brick-motors Vs E-commerce 

Q8. Performance Insights according to Target 



Approach - Project Planning & Aims Grid - 

1. Purpose: What? Why? What do we want to achieve?

To unlock sales insights that are not visible before for the sales team for decision support & automate them to reduce manual time spent in data gathering.

2. Stakeholders: Who will be involved?

Sales Director,
I.T. Team,
Customer Service Team,
Data & Analytics Team.

3. End Result: What do we want to achieve?

An automated dashboard providing quick & latest sales insights in order to support data driven decision making.

4. Success Criteria: What will be our success criteria?

Dashboards uncovering sales order insights with latest data available.
Sales team able to make better decisions & prove 10% cost savings of total spend.
Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.

Data Analysis Using SQL - 

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


