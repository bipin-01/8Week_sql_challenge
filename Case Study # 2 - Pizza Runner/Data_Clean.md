# Data Cleaning


## Note
- As we can see the exclusion and extras columns in customer_order table are inconsistent, so we need to clean them up before       using them in queries
- There are blank spaces and null values in the rows of these tables.


#### Result set Before Cleaning:
![image](https://github.com/bipin-01/8Week_sql_challenge/blob/main/Case%20Study%20%23%202%20-%20Pizza%20Runner/images/uncleanedTable.png)

I added the following SQL code and logic to clean data and make it uniform, so that null is inserted, in every blank spaces: 

```sql
DROP TABLE IF EXISTS customer_orders_temp;

CREATE TEMPORARY TABLE customer_orders_temp AS
SELECT order_id,
       customer_id,
       pizza_id,
       CASE
           WHEN exclusions = '' THEN NULL
           WHEN exclusions = 'null' THEN NULL
           ELSE exclusions
       END AS exclusions,
       CASE
           WHEN extras = '' THEN NULL
           WHEN extras = 'null' THEN NULL
           ELSE extras
       END AS extras,
       order_time
FROM customer_orders;

SELECT * FROM customer_orders_temp;
``` 

#### Result set After Cleaning:
![image](https://github.com/bipin-01/8Week_sql_challenge/blob/main/Case%20Study%20%23%202%20-%20Pizza%20Runner/images/cleanedTable.png)
