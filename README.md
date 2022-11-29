
# Sales Insight PowerBI Project

In This project I have Build super powerful data analysis dashboards where I have used ETL techniques, Data analysis using mySQL, real time dashboards using powerBI
## Table Content

- Problem Statement

- Approach 

- Technologies Used

- Instructions to setup mysql 

- Data Analysis Using SQL Queries

- Screenshots

## Problem Statement
AtliQ Hardware which is Computer hardware manufacturer and Peripheral manufacturer company is facing issues in terms of their Sales, Profit and  Customer performance  so they hire a team of data analysts. The data analysts will first use the Aims Grid to define a problem and define strategy to tackle that problem and then they will works on data discovery.

## Approach

- Downloading Dataset from company

- Imported the dataset in my local mysql server

- Data analysis using my sql to get overview of data

- Data analysis using PowerBi : ETL, Dax queries, Realtime Dashboard

- Published both report/dashboards on web for easy access to public.
## Technologies Used
**MySQL**

**PowerBI**

**DAX**


## Instructions to setup mysql on your local computer

SQL database dump is in **db_dump.sql** file above. Download db_dump.sql file to your local computer and import it to MySQL. Also there is Advanced version of file for more insights.
## Data Analysis Using SQL Queries



**Show all customer records**

```
SELECT * FROM customers;

```

**Show total number of customers**

```
SELECT count(*) FROM customers;

```

**Show transactions for Chennai market (market code for chennai is Mark001)**

```
SELECT * FROM transactions where market_code='Mark001';

```

**Show distrinct product codes that were sold in chennai**

```
SELECT distinct product_code FROM transactions where market_code='Mark001';

```
**Show transactions where currency is US dollars**


```
SELECT * from transactions where currency="USD"

```

**Show transactions in 2020 join by date table**

```
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON
transactions.order_date=date.date where date.year=2020;

```

**Show total revenue in year 2020**
```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON
transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or
transactions.currency="USD\r";
```

**Show total revenue in year 2020, January Month**


```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON
transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and
(transactions.currency="INR\r" or transactions.currency="USD\r");
```


**Show total revenue in year 2020 in Chennai**
```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON
transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

```


![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/Quries.gif?raw=true)


## Screenshots

**Key Insight**

![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/keyinsight_I.gif?raw=true)


![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/keyinsight_II.gif?raw=true)


![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/keyinsight_III.gif?raw=true)

**Profit Analysis**

![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/profitAnalysis_I.gif?raw=true)


![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/ProfitAnalysis_II.gif?raw=true)

**Profit Insight**

![App Screenshot](https://github.com/Rohan9971/Sales_Insight_Power_BI_Project/blob/main/ScreenShots/profitInsight.gif?raw=true)
