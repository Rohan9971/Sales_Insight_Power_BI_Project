
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


![keyinsight_I](https://user-images.githubusercontent.com/112953571/205956523-d2c73fbd-c487-4fcd-962c-1ae2ebf6b100.gif)


![keyinsight_II](https://user-images.githubusercontent.com/112953571/205956559-3998f3e1-19e0-43dc-9884-e2cbf1355005.gif)


![keyinsight_III](https://user-images.githubusercontent.com/112953571/205956632-507ad198-4436-4496-9c9c-a7f88836caec.gif)


**Profit Analysis**


![profitAnalysis_I](https://user-images.githubusercontent.com/112953571/205956790-16f7cdd0-ab9b-48d6-b7bf-998e81134254.gif)


![ProfitAnalysis_II](https://user-images.githubusercontent.com/112953571/205956874-c3d561a8-511e-49d5-909c-ad83068e69ec.gif)




**Profit Insight**


![profitInsight](https://user-images.githubusercontent.com/112953571/205957221-9a519aff-f800-4989-9d7e-6d5899932cc2.gif)



