<h1 align="center">
  <a href="https://www.mysql.com/products/workbench/" target="_blank">
    <img src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/mysql_logo.jpg" alt="MySQL" width="50" height="50" style="vertical-align: middle;"/>
  </a>
  <strong>A Deep Dive into Indian Hardware Company's Sales Performance: Profit and Revenue Analysis with SQL and Tableau"</strong>
  <a href="https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis" target="_blank">
    <img src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/tableau_logo.jpg" alt="Tableau" width="50" height="50" style="vertical-align: middle;"/>
  </a>
</h1>


<p  align="center"><img width="80%" src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/salesinsight.PNG" /></a></p>

<h4>In this project, I tackled a business problem faced by an India-based hardware company by employing a data-driven approach, using SQL and Tableau to provide actionable insights and effective solutions.</h4>

## Business Problem

AtliQ is a hardware company that operates by supplying computer hardware and peripherals to clients throughout India, with a head office located in Delhi and regional offices situated in various locations across the country.

The sales director is facing numerous challenges due to rapid market changes and strong competition, making sales tracking difficult. The sales director needs more accurate insights about the company's sales to make data-driven decisions.

<h4><i> Business scenario: </i></h4>

<i> The sales director requires comprehensive information about sales performance across all operations, but the current data provided by regional sales managers is insufficient. Merely hearing numbers or receiving large amounts of Excel files is not effective in obtaining a reliable overview of the business. The sales director desires a more effective way to view and understand the data to gain immediate insights into the company's sales performance. </i>

<h4> Solution </h4>
Non-complex and interactive dashboard uncovering sales insights with latest data available.

## Approach - Project Planning & <a href ="https://www.youtube.com/watch?v=6118I9HViuQ">Aims Grid 

<b>1. Purpose - </b> To uncover previously unseen sales insights and provide decision support to the sales team, while also automating the process to reduce manual data gathering time.

<b>2. Stakeholders - </b> sales director, marketing team, customer service team, data analytics team, and IT personnel.

<b>3. End Result - </b> An automated dashboard to provide real-time sales insights, facilitating data-driven decision making for the stakeholders.

<b>4. Success Criteria - </b>
- Dynamic dashboards reveal real-time sales order insights.
- Improved decision-making results in 10% reduction in total spend.
- Sales analysts save 20% of their time previously spent on manual data gathering.

<h3> Data Analysis -Approach </h3>

<p  align="center"> <img width="80%" src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/approach.PNG" /></a></p>


### Setup Process
Step 1: Download file: db_dump.sql or db_dump.xlsx

Step 2: Import it in MySql : Data Exploration

Step 3: Download [Tableau Public](https://www.tableau.com/products/public/download) (Free) or [Tableau Desktop](https://www.tableau.com/products/desktop/download) (14 days trial) to perform ETL <i> (Extract,tranform and load) </i> and visualization

Step 4: Connect Tableau with MySql database or Excel database

Step 5: Save the file as (.twb or .twbx)


## Data Analysis Using SQL 

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

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

## Data Analysis Using Tableau 
  
### Tableau Public Dashboards: [Revenue & Profit Analysis](https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis)  <a href="https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/mrankitgupta/mrankitgupta/a768d6bf0a001f03327578ae12f8867e4056cbaf/tableau-software.svg" alt="tableau" width="40" height="20"/> </a>

#### Create Star Schema in Tableau
	
<p  align="center"><img width="80%" src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/star_schema.PNG" /></a></p>

#### Tableau Dashboard - [Revenue Analysis](https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis)
	
<p  align="center"><a href="https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis"><img width="100%" src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/revenue%20analysis.PNG" /></a></p>

#### Tableau Dashboard - [Profit Analysis](https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis)
	
<p  align="center"><a href="https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis"><img width="100%" src="https://github.com/roopadm/Sales-Performance-Analysis-using-SQL-and-Tableau-AtiQ/blob/main/images/profit%20analysis.PNG" /></a></p>
  
## Project References: 🔗

|**Sr.No. 🔢**|**References 👨‍💻**| **Links :link:**|
|------|--------------------|---------------------|
|1| **Tableau Project Dashboard :** Sales Insights | [Dashboard](https://public.tableau.com/app/profile/roopa.d.moorthy/viz/Sales_Insight_AtliQ/ProfitAnalysis)| 
|2| MySQL installation | [Javatpoint](https://www.javatpoint.com/how-to-install-mysql) |
|3| OLTP & OLAP | [Geeks for Geeks](https://www.geeksforgeeks.org/difference-between-olap-and-oltp-in-dbms/) | 
|4| Star Schema: Fact Table & Dimension Table | [Microsoft docs.](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema) | 


## Check out my other projects too : :mag: 👨‍💻 🛰️

<code>[Data-Driven Marketing Strategies for Rider Conversion : Rider Usage Analysis with R and Tableau](https://github.com/roopadm/Google-Capstone-Project-R-Tableau-Cyclistic/edit/main/README.md)</code> 📊

<code>[An Analysis of Developer Communities: Insights from the 2022 Stack Overflow global Survey](https://github.com/roopadm/AnalyzingDevSurvey-Data-analysis-using-Python)</code> 📊
