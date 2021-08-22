# PowerBI_Insights

### Data Analysis Using SQL

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


### Data Relationships:

![image](https://user-images.githubusercontent.com/59439090/130356147-f0379612-c426-4c07-86f1-5d8c55d65459.png)


### Insights:


![image](https://user-images.githubusercontent.com/59439090/130356224-18f8aea1-3d7f-4d53-bd54-65cf518af3b9.png)


### Profit Analysis:


![image](https://user-images.githubusercontent.com/59439090/130357775-4fed224d-2df1-4b77-bbd4-0f3b53416ec2.png)



### Performance Insights:


![image](https://user-images.githubusercontent.com/59439090/130357838-bde72c50-9953-4e2d-9906-c20bb126ef23.png)



