Write Mongo query to retrieve documents from the orders in ascending order by total.
=== db.orders.find().sort({total:1})
Write Mongo query to retrieve documents from the orders in descending order by total.
=== db.orders.find().sort({total:-1})
Write Mongo query to retrieve documents from the products in ascending order by quantity.
=== db.products.find().sort({quantity:1})
Write Mongo query to retrieve documents from the products in descending order by quantity.
=== db.products.find().sort({quantity:-1})
Write Mongo query to retrieve the oldest paymentMethod from the payments collection as "_id".
=== 
Write Mongo query to retrieve the recent paymentMethod from the payments collection as "_id".
===
Write Mongo query to retrieve 2nd and 3rd buyers from the buyers collection.
=== 
Write Mongo query to retrieve 6th order to 10th order from the orders collection.
=== 
Write Mongo query to retrieve the 3rd most recent shipped order from the orders collection.
===
Write Mongo query to retrieve the less Expensive product from order_details.
===
Write Mongo query to retrieve the most Expensive product from order_details.
===
Write Mongo query to retrieve the first order from the orders as per the order_date.
===
Write Mongo query to retrieve the last 3 orders from the orders collection who have less total amount.
===
Write Mongo query to retrieve the last order from the orders as per the order_date.
===
Write Mongo query to retrieve the top 3 orders from the orders collection who have most total amount.
===
Write Mongo query to retrieve the most recent shipped order from the orders collection.
===
Write Mongo query to retrieve the less Expensive product from products.
===
Write Mongo query to retrieve the most Expensive product from products.
===
Write Mongo query to get the total revenue from all orders
===
Write Mongo query to retrieve all the orders that shipped before 2022-05-26
===
Write Mongo query to find the maximum price as maxPrice of products and their names as name for each category.
===
Write Mongo query to find Most used payment Method as paymentMethod and the number of time it is used as count.
===
Write Mongo query to find the total count of orders by status.
===
Write Mongo query to retrieve the orders grouped by customer_id with the max total
===
Write Mongo query to retrieve the orders grouped by customer_id with the average total.
===