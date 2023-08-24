# Sales_Insight_DataAnalysis
Analyze Sales Data of a Peripheral Store for insights & build Dashboards

## Data Analysis Using SQL
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

## Data Model:
![Screenshot (88)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/1f2c989a-5aa3-4c4f-a802-c8154294158e)

## Dashboards:

![Screenshot (89)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/984db5a1-e267-4985-92d5-55ef965b3a86)
![Screenshot (90)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/9a134686-739b-4175-8aab-58f6096bec9d)
![Screenshot (91)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/d377c868-89d5-4f15-8914-a120dfe37837)
