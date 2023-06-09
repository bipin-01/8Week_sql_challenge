# :pizza: Case Study #2: Pizza runner - Pizza Metrics

## Case Study Questions

1. How many pizzas were ordered?
2. How many unique customer orders were made?
3. How many successful orders were delivered by each runner?
4. How many of each type of pizza was delivered?
5. How many Vegetarian and Meatlovers were ordered by each customer?
6. What was the maximum number of pizzas delivered in a single order?
7. For each customer, how many delivered pizzas had at least 1 change and how many had no changes?
8. How many pizzas were delivered that had both exclusions and extras?
9. What was the total volume of pizzas ordered for each hour of the day?
10. What was the volume of orders for each day of the week?

***

###  1. How many pizzas were ordered?

```sql
SELECT count(pizza_id) AS "Total Number Of Pizzas Ordered"
customer_orders;
``` 
#### Result set:
![image](https://github.com/bipin-01/8Week_sql_challenge/blob/main/Case%20Study%20%23%202%20-%20Pizza%20Runner/images/Q1.png)

### 2. How many unique customer orders were made?

```sql
SELECT COUNT (DISTINCT order_id) AS
unique_customer_orders from customer_orders_temp;
``` 
#### Result Image:
![image](https://github.com/bipin-01/8Week_sql_challenge/blob/main/Case%20Study%20%23%202%20-%20Pizza%20Runner/images/Q2.png)
