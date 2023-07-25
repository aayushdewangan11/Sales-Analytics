# Sales-Analytics
 "Sales Insights using MySQL and Tableau" is a powerful and data-driven solution designed to provide comprehensive and actionable sales analytics for businesses. By leveraging the capabilities of MySQL, a reliable and efficient relational database management system, and Tableau, a leading data visualization platform, this solution enables organizations to gain valuable insights into their sales performance.

<h6>Below are listed some SQL queries:</h6>

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

<h3>DB Schema</h3>
![image](https://github.com/aayushdewangan11/Sales-Analytics/assets/79148304/55e97a53-4fa1-4686-9419-79dfc3f82846)

<h3>Dashboad Visualisation</h3>
![Dashboard](https://github.com/aayushdewangan11/Sales-Analytics/assets/79148304/6e101e7d-46f7-4b3c-8e21-bb3c8e66db3d)


