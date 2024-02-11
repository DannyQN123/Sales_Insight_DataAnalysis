# Analyze Sales Data of a Peripheral Store for Insights & build Dashboards.  
The purpose is to understand the sales profile of the company. Some of the questions asked are:
- Which region has the highest revenue ?
- Which products are sold the most ?
- Which regions are declining in revenues ?
- Show the revenue trend of the company over the years.

## Flow of analysis
- Explore the data with SQL in MySQL database  
- Connect MySQL database with PowerBI (Tableau), and use Power Query to process data.
- Building DashBoards.

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
PowerBI
![Screenshot (88)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/1f2c989a-5aa3-4c4f-a802-c8154294158e)

Tableau
![Screenshot (94)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/d7f66425-e825-4c63-8567-69e0287af5d2)


## Dashboards:
PowerBI
![Screenshot (89)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/984db5a1-e267-4985-92d5-55ef965b3a86)
![Screenshot (90)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/9a134686-739b-4175-8aab-58f6096bec9d)
![Screenshot (91)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/d377c868-89d5-4f15-8914-a120dfe37837)

Tableau
![Screenshot (93)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/8ebce609-e159-4fd2-966d-bf7bc9f1df84)
![Screenshot (95)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/cb6d1a9a-2bd0-4002-b941-2d66538b8ea5)
![Screenshot (96)](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/517d4824-7860-4139-9d72-8c2c3ba8e567)

## Some Insights from the DashBoard: 
- The ***Revenue Trend*** declines overtime, and as we look deeper into the revenue trend of each markets (in the ***Revenue by Markets*** section), we see that revenue trend of the top 3 markets (Delhi NCR, Mumbai, Ahmed) also in decline as well.

![Screenshot 2024-02-11 115622](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/67162b56-15ff-4b89-a765-df94f7f219e4)
![Screenshot 2024-02-11 115656](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/e3941a3f-002e-4362-89c2-97c52af197ab)
![Screenshot 2024-02-11 115740](https://github.com/DannyQN123/Sales_Insight_DataAnalysis/assets/107457149/0c1f851d-4c35-4f17-98e2-ca344c289210)  

- Looking deeper, we will see that Revenue from top products in each of these markets are also declining over-time. What we can conclude is that the decline in ***Revenue Trend*** happens company wide, and further information is needed to derive any more specific conclusion (more informations about ***market demands***, for examples, or ***market trend***, as the decline in Revenue happens company-wide)  

    
